# Instrucciones

- Descargué el archivo de conexión a okteto.
- Definí la variable de ambiente KUBECONFIG que apunte a dicho archivo.
- Confirmé la conexión a okteto corriendo `kubectl version`.
- Escribí el archivo `pod.yml` siguiendo el ejemplo de clase y agregando la variable de ambiente TELEGRAM_TOKEN.
- Ejecuté `kubectl apply -f pod.yml` para levantar el pod.