# Configuración y puesta en marcha de Ansible con Jenkins

Receta para despliegue de una estructura básica de automatización con Ansible

# COMPONENTES

<kbd></kbd>Virtualbox

<kbd></kbd>VM1: Centos 7.4 con Ansible + Jenkins

IP Add: 10.0.2.2/24

GW: 10.0.2.1

DNS: 10.0.2.3/8.8.8.8


<kbd></kbd>VM2: Centos 7.4 con Docker de Pruebas

IP Add: 10.0.2.3/24

GW: 10.0.2.1

DNS: 127.0.0.1

domain: jenkinslab.local

Container: Bind 9 -- Servicio local de DNS


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
