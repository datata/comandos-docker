# version docker

```sh
$ docker -v
```

# buscar imagenes de docker en el repositorio docker hub
```sh
$ docker search node
```

# listar imagenes
```sh
$ docker images
```

# listar contenedores activos
```sh
$ docker ps
```
# listar todos los contenedores
```sh
$ docker ps -a
```

# crear contenedor de una imagen
```sh
$ docker run hello-world
```

# eliminar imagen
```sh
$ docker rmi <id-imagen>
```

# dar un nombre a un contenedor
```sh
$ docker run --name nombre-contenedor ubuntu
```

# Modo inteactivo
```sh
$ docker run --name nombre-contenedor -it ubuntu bash
```

# detener contendor
```sh
$ docker stop <nombre-del-contenedor>
$ docker stop <id-del-contenedor>
```

# poner en marcha el contendor
```sh
$ docker start <nombre-del-contenedor>
$ docker start <id-del-contenedor>
```

# añadir un directorio de trabajo
```sh
$ docker run --name nombre-contenedor -w /app -it ubuntu bash
```

# Bindeo de carpetas, como compartir codigo entre mi equipo y el contenedor
```sh
$ docker run --name nombre-contenedor -w /app -v ${PWD}:/app -it ubuntu bash
```

# bindeo de puertos para acceder al servicio desde nuestro equipo
```sh
$ docker run --name nombre-contenedor -e MYSQL_ROOT_PASSWORD=1234 -p 3307:3306 mysql
```

# modo detach una vez nos crea el contenedor nos devuelve a nuestra linea de comandos en lugar de mostrar la consola de mysql en este ejemplo
```sh
$ docker run --name nombre-contenedor -p 3307:3306 -e MYSQL_ROOT_PASSWORD=1234 -d mysql
```

