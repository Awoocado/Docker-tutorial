# Docker

## Porque necesitas Docker?
Docker es util cuando necesitas desplegar un proyecto full stack que usa diferentes tipos de tecnologias sin tener que preocuparte por la compatibilidad con el host ya sea por las dependencias o el sistema operativo.

Docker asegura de que una aplicacion corra de la misma manera en cualquier host sin tener que preocuparse por los requisitos.

Con Docker puedes correr cada una de las aplicaciones de un proyecto dentro de un contenedor (container) con sus propias librerias y sus propias dependencias, todo en el mismo host. 

### Que es un container?
Un container son entornos completamente aislados donde pueden tener sus propios procesos, servicios e interfaces en la red, muy parecido a una maquina virtual con la diferencia de que todos compartan el mismo kernel.

Docker esta basado en LXC (Linux Containers). Aún cuando LXC es de bajo nivel, Docker es fácil de usar.

### Compartiendo el kernel

Docker corre containers encima del Kernel de Linux por lo que puedes tener containers basados en otras distribuciones de Linux, siempre y cuando comparta el mismo kernel. Por esta razón, no puedes crear contenedores de Windows a menos que uses Windows Server (no es tan popular, pero si lo instalas en Windows, puedes emular el kernel de Linux para poder correr contenedores de Linux)

El propósito de Docker es el de empaquetar aplicaciones asegurando de que corran en cualquier entorno con docker instalado.

### VM vs Container

No se tiene que confundir una Maquina Virtual con un Container: Las maquinas virtuales necesitan un Hypervisor para poder emular toda la funcionalidad de un SO por lo consume mas espacio y demora mas en encender a diferencia de un container, que usa la funcionalidades del Kernel actual, ocupando mb de espacio y encender un app en cuestión de segundos.

La gran mayoria de organizaciones ya tienen su aplicacion lista para funcionar dentro de containers, Docker hub contiene las imagenes de estos containers listos para ser descargados y desplegados

## Como funciona Docker?
Despues de instalar docker, correr una aplicacion de Docker es tan facil como correr el comando `run` con el nombre de la imagen que quieres usar.

Si quisiera correr una instancia de Node.js usaria `docker run nodejs`, lo mismo va para MongoDB `docker run mongodb`, Redis `docker run redis` o Ansible `docker run Ansible` por mencionar algunos ejemplos.

### Container vs Image

Las imagenes (Image) es un paquete o una plantilla usado para crear uno o mas contenedores, los contenedores corren instancias de contenedores que estan aislados conteniendo sus propios procesos.

Como hemos visto antes, varios productos ya tiene una imagen disponible en Docker Hub: Incluso si no encuentras algun software, puedes crear tu propia imagen y publicarlo en algun Docker registry para que sea publico. 

## Versiones de Docker

En este documento se va a usar la version de Comunidad (Community Edition) disponible en Linux, Mac y Windows. Docker corre de manera nativa en Linux pero puedes instalarlo en Mac usando Docker Desktop y en Windows usando Docker Desktop o usando una maquina virtual de Linux.

## Instalando Docker en Linux

No brainer, C&P:
```bash
curl -fsSL https://get.docker.com | sudo sh
```
