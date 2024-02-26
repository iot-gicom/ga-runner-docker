# ga-runner-docker

Este repositorio proporciona runners autohospedados de GitHub en un contenedor Docker.

**Nota:** Para utilizar este contenedor, es necesario generar un personal access token de GitHub con las siguientes propiedades: `repo`, `workflow` y `admin:org`.

Actualizar `RUNNER_VERSION` con la ultima version disponible antes de generar la imagen.
[Link](https://github.com/actions/runner/releases "Latest runner version here.")

## Uso

Para construir la imagen Docker, ejecuta el siguiente comando:

```shell
docker build -t gicom/ga-runner .
```

## Despliegue

Añadir las variables de entorno de GitHub al archivo `.env` (`.env_emplate` es un ejemplo):

```shell
USER=agustinbene
REPO=back-access-control-gicom
TOKEN=token
```


Para levantar el servicio, puedes hacerlo de dos maneras:

1. Utilizando Portainer:
   - Importa el archivo docker-compose.yml en Portainer y despliega el servicio.

2. Utilizando Docker Stack:
```shell
docker stack deploy -c docker-compose.yml ga-runner-docker
```

