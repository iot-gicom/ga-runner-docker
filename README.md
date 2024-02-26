# ga-runner-docker

Este repositorio proporciona runners autohospedados de GitHub en un contenedor Docker.

**Nota:** Para utilizar este contenedor, es necesario generar un personal access token de GitHub con las siguientes propiedades: `repo`, `workflow` y `admin:org`.

## Uso

Para construir la imagen Docker, ejecuta el siguiente comando:

```shell
docker build -t gicom/ga-runner .
```

Para levantar el servicio, puedes hacerlo de dos maneras:

1. Utilizando Portainer:
   - Importa el archivo docker-compose.yml en Portainer y despliega el servicio.

2. Utilizando Docker Stack:
```shell
docker stack deploy -c docker-compose.yml ga-runner-docker
```