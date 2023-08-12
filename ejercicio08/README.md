## Ejecución

Correr el comando `docker-compose up --scale web=2` para que se levanten dos instancias del contenedor web. Probarlo luego con un GET a localhost:3001/health

## Aclaraciones

Cada instancia del servicio web expone su puerto 3000. Sin embargo, de cada al usuario, el puerto que está expuesto es el del servicio nginx, que es el 3001. Uno envía su request a nginx y es esta aplicación la que redirige el tráfico hacia `http://web:3000`. Esto se puede ver en el archivo nginx.conf.

Docker cuenta con un server dns interno que es el que resuelve ese "web" al host correcto donde está levantado el servicio web.