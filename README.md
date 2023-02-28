# Uso de Gradle (básico)

## Descripción
Uso de Gradle para convertir un archivo Markdown a un archivo HTML utilizando **Gradle Markdown Plugin**.

## Requerimientos
- Plugin [Gradle Markdown](https://github.com/kordamp/markdown-gradle-plugin)

1. Primero debe crearse el archivo *build.gradle* en la raíz del proyecto.
2. Dentro de gradle colocamos lo siguiente: 
``plugins{
   id 'org.kordamp.gradle.markdown' version '2.2.0'
   }``.
   1. En donde ``plugins{}`` hace referencia un bloque de código en donde colocaremos el identificador del plugin que 
   vamos a utilizar.
   2. ``id 'org.kordamp.gradle.markdown' version '2.2.0'`` indica el identificador del plugin, así como también la 
   versión que se utilizará.
3. Una vez hecho lo anterior, debemos crear en la raíz del proyecto la siguiente estructura de carpetas: 
   ``src/markdown`` y colocar el archivo ``.md`` a convertir.
4. En la terminal nos posicionamos dentro del directorio en el cual tenemos nuestro archivo ``build.gradle``
5. Para convertir el archivo ``.md`` a un archivo ``.html`` ejecutamos en la terminal la siguiente línea:\
``gradle task markdownToHtml``
6. Con esto se nos generará el archivo ``.html`` dentro de la carpeta ``build/gen-html`` del directorio raíz.
