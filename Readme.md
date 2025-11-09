# EJERCICIO GIT

## Primeros pasos: Configuración local

Creacion del repositorio local a partir del repositorio remoto de ejemplo suministrado en los apuntes.

Todo ha funcionado segun lo esperado excepto las primeras veces que lance el comando N p.m. Start lo host no funcionaba y viendo la terminal, estaba fallando la build.

No había modificado en ningún caso el archivo package.json pero lanzaba este error:

> **Ruta del proyecto**/package.json:5:11
>
> 4 | "description": "",
>
> 5 | "main": "index.js",
>
> | ^^^^^^^^^^ Target declared here
>
> 6 | "scripts": {
>
> 7 | "build": "rimraf dist && parcel ./src/index.html",
>
> 💡 The "main" field is meant for libraries, not applications. Either remove the "main" field or choose a different target name.

Trasteando por la red se sugería que la solución sería:

1. Añadir:

   > "targets": {
   >
   > "app": {
   >
   > "source": "src/index.html"
   >
   > }
   >
   > },

2. Eliminar:

> "main": "index.js"

Desconozco si es una buena práctica, pero funcionó.

Tras esta configuración se realizan los primeros commits para añandir los archivos base al repositorio local y añadir este readme.

## Creación del repositorio remoto y sincronización con local

Coneto local con remoto sin problemas y me doy cuenta de que la ubicación del readme no es la correcta.

![Captura de pantalla mostrando el editor y el resultado de la conexión en el navegador](src/contents/Conexion-local-remoto.png)

Creo la carpeta contents para añadir capturas de pantalla y se actualiza el readme.
