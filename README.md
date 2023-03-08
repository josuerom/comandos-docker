# Consulta Docker

El presente documento contiene una lista de los comandos de docker para aprender y aplicar.

## Comandos de Imágenes

```bash
docker images
```
Devuelve una lista de las imágenes que se tengan instaladas.

```bash
docker pull node
docker pull node:18
```
Descarga las imágenes que le indiquemos junto con la versión que deseemos. Además, para conocer cual es el nombre de la imagen que queremos descargar se debe ingresar a [dockerhub](https://hub.docker.com/) y allí buscarla.

En dado caso que, al intentar instalar alguna imagen se genere un error (más que todo sucede en Mac con chips M1), se debe indicar la plataforma.
```bash
docker pull --platform linux/x86_64 mysql
```
Para desinstalar alguna imagen
```bash
docker rm node:18
```

## Comandos de Contenedores
Crea un container y arroja su ID.
```bash
docker create ubuntu
or
docker container create mongo
```

Para encender el contenedor
```bash
docker start <id-del-contenedor>
```
Devuelve una tabla la cual contiene varios datos interesantes sobre todas la imágenes, como lo son el id, imagen, comando, fecha de creación, estado, puerto y el nombre.

Crear contenedor con parámetros de ajuste
```bash
docker run -dit --name Josue -p 9090:80 ubuntu /bin/bash
```
Para habilitar el contenedor, mientras este apagado
```bash
docker start <name-container>
```

Para entrar a un contenedor
```bash
docker exec -it <name-container> /bin/bash
```
Para salir del contenedor
```bash
exit
```

```bash
docker 
```

```bash
docker network connect <id-container> <name-container> 
```

```bash
docker network inspect <name-container> 
```

Para enviar un archivo desde el SO local a una maquina virtual, desde Windows
```bash
scp <ruta-del-archivo-local> <nombre-servidor>@<ip-del-servidor>:/home/minutero
```
Aún esta incompleta, ver vídeo [Aprende Docker ahora!](https://youtu.be/4Dko5W96WHg?t=1915)
