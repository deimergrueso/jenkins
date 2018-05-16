# Configuración y puesta en marcha de Ansible con Jenkins

Receta para despliegue de una estructura básica de automatización con Ansible

# COMPONENTES

![Arquitectura](https://drive.google.com/open?id=1MpWgV_qcVzA3sUJklutUZbt8UnQkr5bE)
<kbd></kbd>Virtualbox

<kbd></kbd>VM1: Centos 7.4 con Ansible + Jenkins

IP Add: 192.168.122.10/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: orquestador.labansible.local

<kbd></kbd>VM2: Centos 7.4 con Docker de Pruebas

IP Add:  192.168.122.20/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: testing.labansible.local

Container: Bind 9 -- Servicio local de DNS

<kbd></kbd>VM3: Centos 7.4 con Docker de Producción

IP Add:  192.168.122.30/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: produccion.labansible.local


# Instalación de componentes

Instalación de Ansible en Centos 7.4

Requisitos:
    -Usuario administrador

    -Git

    -Python PIP

    -Conexión a internet




# Scripts de despliegue con Ansible

# Scripts con Jenkins

# Descarga y automatización del repositorio
