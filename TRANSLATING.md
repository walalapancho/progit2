# Traducción de Pro Git (2ª Edición)

Las traducciones se gestionan de manera descentralizada. Cada equipo de traducción mantiene su propio proyecto. Cada traducción reside en un repositorio independiente; el equipo de Pro Git simplemente extrae los cambios y los compila en el sitio web https://git-scm.com cuando estén listos.

## Guía general para la traducción de Pro Git

Pro Git es un libro sobre una herramienta técnica, por lo que traducirlo resulta más complejo comparado con una traducción no técnica.

Los siguientes son lineamientos para guiarle:
* Antes de comenzar, lea el libro completo de Git Pro en inglés, para estar al tanto del contenido y familiarizarse con el estilo empleado.
* Asegúrese de tener un conocimiento práctico sólido de Git, para que la explicación de los términos técnicos sea factible.
* Manténgase adherido a un estilo y formato consistentes para toda la traducción.
* Revise y comprenda los conceptos básicos del formateo [Asciidoc](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/). No seguir la sintaxis de AsciiDoc puede provocar problemas con la construcción/compilación de los archivos pdf, epub y html necesarios para el libro.

## Traducción del libro a otro idioma

### Colaboración en un proyecto existente

* Consulte si ya existe un proyecto listado en la siguiente tabla.
* Acceda a la página del proyecto en GitHub.
* Cree un *issue*, preséntese e indique dónde puede colaborar.

| Language     | GitHub page     |
| :------------- | :------------- |
| العربية | [progit2-ar/progit2](https://github.com/progit2-ar/progit2) |
| Беларуская  | [progit/progit2-be](https://github.com/progit/progit2-be) |
| български език | [progit/progit2-bg](https://github.com/progit/progit2-bg) |
| Čeština    | [progit-cs/progit2-cs](https://github.com/progit-cs/progit2-cs) |
| English    | [progit/progit2](https://github.com/progit/progit2) |
| Español    | [progit/progit2-es](https://github.com/progit/progit2-es) |
| فارسی | [progit2-fa/progit2](https://github.com/progit2-fa/progit2) |
| Français   | [progit/progit2-fr](https://github.com/progit/progit2-fr) |
| Deutsch    | [progit/progit2-de](https://github.com/progit/progit2-de) |
| Ελληνικά   | [progit2-gr/progit2](https://github.com/progit2-gr/progit2) |
| Indonesian | [progit/progit2-id](https://github.com/progit/progit2-id) |
| Italiano   | [progit/progit2-it](https://github.com/progit/progit2-it) |
| 日本語   | [progit/progit2-ja](https://github.com/progit/progit2-ja) |
| 한국어   | [progit/progit2-ko](https://github.com/progit/progit2-ko) |
| Македонски | [progit2-mk/progit2](https://github.com/progit2-mk/progit2) |
| Bahasa Melayu| [progit2-ms/progit2](https://github.com/progit2-ms/progit2) |
| Nederlands | [progit/progit2-nl](https://github.com/progit/progit2-nl) |
| Polski | [progit2-pl/progit2-pl](https://github.com/progit2-pl/progit2-pl) |
| Português (Brasil) | [progit/progit2-pt-br](https://github.com/progit/progit2-pt-br) |
| Русский   | [progit/progit2-ru](https://github.com/progit/progit2-ru) |
| Slovenščina  | [progit/progit2-sl](https://github.com/progit/progit2-sl) |
| Српски   | [progit/progit2-sr](https://github.com/progit/progit2-sr) |
| Svenska  | [progit2-sv/progit2](https://github.com/progit2-sv/progit2) |
| Tagalog   | [progit2-tl/progit2](https://github.com/progit2-tl/progit2) |
| Türkçe   | [progit/progit2-tr](https://github.com/progit/progit2-tr) |
| Українська| [progit/progit2-uk](https://github.com/progit/progit2-uk) |
| Ўзбекча  | [progit/progit2-uz](https://github.com/progit/progit2-uz) |
| 简体中文  | [progit/progit2-zh](https://github.com/progit/progit2-zh) |
| 正體中文  | [progit/progit2-zh-tw](https://github.com/progit/progit2-zh-tw) |

### Inicio de una traducción nueva

Si no existe un proyecto para su idioma, puede iniciar su propia traducción.

Base su trabajo en la segunda edición del libro, disponible [aquí](https://github.com/progit/progit2). Para hacerlo:
 1. Seleccione el código correcto según [ISO 639](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) para su idioma.
 2. Cree una [organización de GitHub](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch), por ejemplo: `progit2-[su código]` en GitHub.
 3. Cree un proyecto llamado `progit2`.
 4. Copie la estructura de progit/progit2 (este proyecto) a su proyecto y comience con la traducción.

### Actualización del estado de su traducción

En https://git-scm.com, las traducciones están divididas en tres categorías. Una vez que alcance uno de estos niveles, contacte a los mantenedores de https://git-scm.com/ para que puedan extraer (pull) los cambios.

| Category | Completion     |
| :------------- | :------------- |
| Translation started for | Introduction translated, no much else. |
| Partial translations available in | up to chapter 6 has been translated. |
| Full translation available in |the book is (almost) fully translated. |

## Integración Continua con GitHub Actions

GitHub Actions es un servicio de [integración continua](https://en.wikipedia.org/wiki/Continuous_integration) que se integra con GitHub. GitHub Actions se utiliza para garantizar que una *pull-request* no rompa la compilación ni el proceso de *build*. GitHub Actions también puede proporcionar versiones compiladas del libro.

La configuración de GitHub Actions se encuentra en el directorio `.github/workflows`, y si trae la rama `main` del repositorio principal, obtendrá las acciones de forma gratuita.
Sin embargo, si creó su repo de traducción mediante *fork* del repo raíz, debe completar un paso adicional (si no hizo *fork*, puede saltarse esta parte).
GitHub asume que los *forks* se utilizarán para contribuir al repo desde el cual fueron creados; por lo tanto, deberá visitar la pestaña "Actions" en su repo *forkeado* y hacer clic en el botón "I understand my workflows" para permitir la ejecución de las acciones.

## Configuración de una cadena de publicación para e-books

Esta es una tarea técnica; por favor contacte a @jnavila para empezar con la publicación en formato epub.

## Más allá de Pro Git

Traducir el libro es el primer paso. Una vez finalizado, podría considerar traducir la interfaz de usuario (UI) de Git en sí mismo.

Esta tarea requiere un conocimiento técnico más profundo de la herramienta que el del libro. Ojalá que, tras haber traducido el contenido completo del libro, pueda comprender los términos empleados en la aplicación. Si se siente técnicamente capacitado para ello, el repo es [aquí](https://github.com/git-l10n/git-po) y solo tiene que seguir la [guía](https://github.com/git-l10n/git-po/blob/master/po/README.md).

Tenga cuidado, sin embargo, de que:

 * necesitará utilizar herramientas más específicas para gestionar los archivos po de localización (como editarlos con [poedit](https://poedit.net/)) y fusionarlos (*merge*). Podría ser necesario compilar `git` para verificar su trabajo.
 * se requiere un conocimiento básico sobre cómo funciona la traducción de aplicaciones, lo cual es significativamente diferente a traducir libros.
 * el proyecto central de Git utiliza [procedimientos](https://github.com/git-l10n/git-po/blob/master/Documentation/SubmittingPatches) más estrictos para aceptar contribuciones; asegúrese de cumplirlos.
