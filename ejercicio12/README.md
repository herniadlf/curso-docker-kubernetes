- Escribí el descriptor deployment.yml con las tres replicas.
- Apliqué el descriptor con `kubectl apply -f deployment.yml`
- Escribí el descriptor del servicio ingress.yml para abrir al exterior la aplicación
- Apliqué el descriptor con `kubectl apply -f ingress.yml`
- Me genera el siguiente endpoint público, donde verifiqué que funcione la app: https://password-api-herniadlf.cloud.okteto.net/