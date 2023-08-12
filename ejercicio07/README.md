## ¿Cuántos contenedores se están ejecutando? (pueden verlo en el archivo docker-compose.yml y también ejecutando docker ps)

Se ejecutan dos contenedores: uno llamado web y otro llamado db.

## ¿Cuales son las imágenes en las que están basados los mencionados contenedores?

El contenedor web se basa en la imagen `nicopaez/jobvacancy-ruby:1.3.0` y el contenedor db se basa en la imagen `postgres:14.4-alpine`.

## ¿Puedes leer el docker-compose.yml y describir lo que hace cada una de sus lineas?

Se declaran dos servicios, el primero es el web. Se declara la imagen de base que requiere, se indica con el "links" que tiene que estar conectado con el otro servicio, se hace el mapeo de puertos, se declaran variables de ambiente y el depends_on entiendo que declara que primero debe levantarse el otro servicio.

Para la `db` las instrucciones son más sencillas: solo se define la imagen y una variable de ambiente.

## Dado que cada contenedor corre en forma aislada ¿Cómo es posible que esos contenedores se vean entre sí?

La instrucción links en la definición del servicio web define que este contenedor debe poder acceder al otro contenedor. Podríamos decir que la db no ve al web service, pero el web service sí puede ver al servicio db.