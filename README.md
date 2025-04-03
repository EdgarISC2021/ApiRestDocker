# ApiRestDocker

## Unidad 4 - Gestión de Contenedores en el Desarrollo Móvil
### Actividad 10 - Instalación de Docker y despliegue de una aplicación FastAPI en contenedor

### Objetivo
El objetivo de esta actividad es que el estudiante instale Docker en su equipo local y cree una imagen de contenedor que ejecute una aplicación web desarrollada con FastAPI, con el fin de familiarizarse con la contenerización de aplicaciones.

## Requisitos
- Docker (Instalado en el sistema)
- Python 3.11 o superior

## Guía Paso a Paso

### Parte 1: Instalación de Docker

#### 1.1 En Windows o MacOS
1. Descargar e instalar Docker Desktop desde el sitio oficial:
   [Docker Desktop](https://www.docker.com/products/docker-desktop)
2. Ejecutar Docker Desktop y verificar que esté funcionando correctamente.

#### 1.2 En Linux (Ubuntu)
Ejecuta los siguientes comandos en la terminal para instalar Docker en Ubuntu:

```bash
sudo apt update
sudo apt install ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
docker --version
