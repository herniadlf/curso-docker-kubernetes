1. Correr `docker build -t prueba-nginx .` para construir la imagen.
1. Correr `docker run --name test-nginx -p 8080:80 prueba-nginx` para levantar el contenedor.
1. Navegar a `http://localhost:8080/hi.html` para ver el contenido de la static page.
