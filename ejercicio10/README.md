# CMD vs ENTRYPOINT

La instrucción `ENTRYPOINT` define qué es lo que se va a ejecutar cuando se corra el contenedor con  `docker run`. Muchas veces se podrá ver ausente en un Dockerfile debido a que por defecto se toma el entrypoint `/bin/bash -c`.

Por otro lado, la instrucción `CMD` hace referencia a los parámetros con los que se ejecutará el contenedor. Por lo tanto, creo que es más común ver Dockerfiles que solo definen un CMD, debido a que se da por sentado que se ejecuta /bin/bash (entrypoint vacío) y uno solo le define los argumentos en la descripción de la imagen.

De todas formas, el CMD puede ser sobreescrito si cuando se ejecuta se agregan los argumentos con `docker run <contenedor> <argumentos>`. Esto dependerá si el uso del contenedor está pensado para darle flexibilidad al usuario del mismo (se esperan argumentos al correr la imagen), o si el creador de la imagen quiso especificar un comportamiento bastante definido por defecto (entonces están definidos más explicitamente en el dockerfile.