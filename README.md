## Aplicación web desarrollada en equipo.
Evelyn Daniela Naranjo Herrera IDSM41 - 02 Ocutbre 2026

## Rol del líder
El líder administra el repositorio, asigna las tareas mediante Issues y coordina la integración de los cambios.
Las ramas `main` y `develop` deben mantenerse protegidas.


## Organización de ramas
- `main`: versión estable de la aplicación.
- `develop`: integración de las funciones antes de su publicación.
- `feature/nombre-funcion`: desarrollo de nuevas funcionalidades.
- `fix/nombre-correccion`: solución de errores.

## Reglas
- No trabajar directamente en `main` ni en `develop`.
- Crear una rama personal desde `develop`.
- Realizar commits claros y relacionados con la tarea.
- Integrar los cambios mediante Pull Request.
- Solicitar al menos una revisión de otro integrante antes del merge.
- Corregir los comentarios de la revisión.
- Aprobar las pruebas automáticas antes de integrar los cambios.

## Política de commits
Los mensajes deben indicar el tipo de cambio y una descripción breve.

Ejemplos:
- `feat: agregar formulario de tareas`
- `fix: validar campos vacíos`
- `docs: actualizar README`
- `test: agregar pruebas de tareas`

## Roles del equipo
- **Líder:** configura el repositorio y coordina el merge a `main`.
- **Desarrolladores:** implementan las tareas asignadas en sus ramas.
- **Revisores:** revisan Pull Requests de otros integrantes y solicitan correcciones.

## Herramientas
- **Git:** historial de cambios y gestión de ramas.
- **GitHub:** repositorio, Issues y Pull Requests.
- **Visual Studio Code:** edición del código.
- **GitHub Actions:** pruebas y despliegue automatizados.
- **GitHub Pages:** publicación de la aplicación estática.

Justificacion: Se eligen estas herramientas porque facilitan la colaboración a distancia y permiten gestionar el código, las revisiones y la automatización desde una misma plataforma.

## Ejecución local
Una vez incluidos los archivos HTML, CSS y JavaScript del proyecto, abrir `index.html` en el navegador.
También se puede utilizar la extensión Live Server de Visual Studio Code.

## Flujo DevOps
1. Clonar el repositorio.
2. Actualizar la rama `develop`.
3. Crear una rama personal desde `develop`.
4. Resolver el Issue asignado.
5. Probar los cambios y realizar commits claros.
6. Subir la rama a GitHub.
7. Crear un Pull Request hacia `develop`.
8. Recibir una revisión y corregir si es necesario.
9. Integrar los cambios cuando la revisión y las pruebas sean satisfactorias.
10. Crear un Pull Request de `develop` hacia `main` cuando la versión esté lista.
11. Revisar e integrar la versión estable.
12. Publicar la aplicación mediante el flujo de despliegue.

## Estrategia de despliegue
Se propone utilizar CI/CD con GitHub Actions y GitHub Pages.

Los Pull Requests hacia `develop` y `main` ejecutarán las pruebas automáticas.

Al realizar un merge a `main`:
1. GitHub Actions descargará el código.
2. Ejecutará las pruebas del proyecto.
3. Si las pruebas pasan, publicará el sitio en GitHub Pages.
4. Si fallan, detendrá el despliegue y conservará la versión publicada.

Esta automatización requiere configurar el workflow, las pruebas y GitHub Pages en el repositorio.

