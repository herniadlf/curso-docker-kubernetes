## HEALTHCHECK

Se utiliza para pasarle al demonio de docker cómo verificar el estado de un container, por ejemplo, si el container tiene corriendo una api, pasandole un curl a un endpoint de ping o similar.

## ONBUILD

Es una instrucción que se usa cuando la imagen es usada como base para otra imagen, es decir, al terminar el build de la imagen base, se dispara la instrucción onbuild, antes de ejecutar el buildeo de las intrucciones siguientes.

## VOLUME

Un volumen es almacenamiento persistido que se mantiene vivo más allá de si el container está corriendo o no. Al colocar la instrucción VOLUME en el dockerfile es como definir un "puntero" a donde va a estar la información con la que va a comunicarse dicho contenedor. Incluso distintos contenedores pueden acceder al mismo volumen.