# Docker

## ¿Por qué necesitas Docker?
Docker es útil cuando necesitas desplegar un proyecto full stack que usa diferentes tipos de tecnologías sin tener que preocuparte por la compatibilidad con el host, ya sea por las dependencias o el sistema operativo.

Docker asegura de que una aplicación corra de la misma manera en cualquier host sin tener que preocuparse por los requisitos.

Con Docker puedes correr cada una de las aplicaciones de un proyecto dentro de un contenedor (container) con sus propias librerías y sus propias dependencias, todo en el mismo host. 

### ¿Qué es un container?
Los "containers" son entornos completamente aislados donde pueden tener sus propios procesos, servicios e interfaces en la red, muy parecido a una máquina virtual, con la diferencia de que todos compartan el mismo kernel.

Docker está basado en LXC (Linux Containers). Aún cuando LXC es de bajo nivel, Docker es fácil de usar.

### Compartiendo el kernel

Docker corre containers encima del Kernel de Linux, por lo que puedes tener containers basados en otras distribuciones de Linux, siempre y cuando comparta el mismo kernel. Por esta razón, no puedes crear contenedores de Windows a menos que uses Windows Server (no es tan popular, pero si lo instalas en Windows, puedes emular el kernel de Linux para poder correr contenedores de Linux)

El propósito de Docker es el de empaquetar aplicaciones asegurando de que corran en cualquier entorno con docker instalado.

### VM vs Container

No se tiene que confundir una Maquina Virtual con un Container: Las maquinas virtuales necesitan un Hypervisor para poder emular toda la funcionalidad de un SO por lo que consume más espacio y demora más en encender a diferencia de un container, que usa la funcionalidades del Kernel actual, ocupando mb de espacio y encender un app en cuestión de segundos.

La gran mayoría de organizaciones ya tienen su aplicación lista para funcionar dentro de containers, Docker Hub contiene las imagenes de estos containers listos para ser descargados y desplegados

## ¿Cómo funciona Docker?
Después de instalar docker, correr una aplicación de Docker es tan fácil como correr el comando `run` con el nombre de la imágen que quieres usar.

Si quisiera correr una instancia de Node.js usaría `docker run nodejs`, lo mismo va para MongoDB `docker run mongodb`, Redis `docker run redis` o Ansible `docker run Ansible` por mencionar algunos ejemplos.

### Container vs Image

Las imagenes (Image) es un paquete o una plantilla usado para crear uno o más contenedores, los contenedores corren instancias de contenedores que están aislados conteniendo sus propios procesos.

Como hemos visto antes, varios productos ya tiene una imágen disponible en Docker Hub: Incluso si no encuentras algún software, puedes crear tu propia imágen y publicarlo en algún Docker registry para que sea público. 

## Versiones de Docker

En este documento se va a usar la versión de Comunidad (Community Edition) disponible en Linux, Mac y Windows. Docker corre de manera nativa en Linux pero puedes instalarlo en Mac usando Docker Desktop y en Windows usando Docker Desktop o usando una máquina virtual de Linux.

## Instalando Docker en Linux

No brainer, C&P:
```bash
curl -fsSL https://get.docker.com | bash
```
