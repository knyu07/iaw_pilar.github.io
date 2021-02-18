# Práctica: Creación de blogs con Jekyll y GitHub Pages: 

Jekyll es un generador de sitios web estáticos que nos permite crear de forma sencilla blogs, sitios webs personales o webs para proyectos. Los sitios webs generados con Jekyll no usan una base de datos, el contenido del sitio web está escrito en archivos de texto plano en formato Markdown (o Textile) y plantillas Liquid.

Jekyll es el motor de GitHub Pages, un servicio que ofrece GitHub a sus usuarios para que puedan publicar sitios webs estáticos alojados en los repositorios que tienen en GitHub.

Existen 3 imágenes oficiales con Jekyll:

- jekyll/jekyll: Default image.
- jekyll/minimal: Very minimal image.
- jekyll/builder: Includes tools.

## Requisitos: 
Instalamos docker y docker compose.

Para consultar todos los comandos ejecutamos: 
```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll
```
## PASOS A SEGUIR

Este comando nos permite crear la estructura de directorios y los archivos necesarios de un nuevo proyecto Jekyll.
```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog
```

Este comando nos permite generar un sitio HTML estático a partir del contenido del proyecto Jekyll. (Este comando debe usarse dentro del directorio donde esté el contenido del blog).
```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll build
```
La opción --force_polling permite que el contenido del sitio se vaya generando automáticamente cuando existe algún cambio en los archivos del proyecto.
```
docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling
```
:smiley_cat: