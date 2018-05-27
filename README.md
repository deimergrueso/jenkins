# Configuración y puesta en marcha de Ansible con Jenkins

Receta para despliegue de una estructura básica de automatización con Ansible

# COMPONENTES

![Arquitectura](https://raw.githubusercontent.com/deimergrueso/jenkins/master/Archivos%20varios/Arq_LAB.png)




<kbd>VM1: Centos 7.4 con Ansible + Jenkins</kbd>

IP Add: 192.168.122.10/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: orquestador.labansible.local

<kbd>VM2: Centos 7.4 con Docker de Pruebas</kbd>

IP Add:  192.168.122.20/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: testing.labansible.local

Container: Bind 9 -- Servicio local de DNS

<kbd>VM3: Centos 7.4 con Docker de Producción</kbd>

IP Add:  192.168.122.30/24

GW:  192.168.122.1

DNS:  192.168.122.30/8.8.8.8

NM: produccion.labansible.local


# Instalación de componentes

Instalación de Ansible en Centos 7.4

Pre-requisitos:
    -Usuario administrador

    -Git

    -Python PIP

    -Conexión a internet


# Scripts de despliegue con Ansible

 - VM1: Instalacion de prerequisitos

sudo yum -y update

Instalar PIP

curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py" && sudo python get-pip.py

**Instalar Ansible en VM1**

sudo pip install ansible

mkdir labansible && cd labansible

sudo cp /etc/ansible/ansible.cfg ~/labansible/

**Editar el archivo host**

sudo nano /etc/host y agregar las direcciones de los servidores remotos:

127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

192.168.122.10  orquestador.labansible.local

192.168.122.20  testing.labansible.local

192.168.122.30  produccion.labansible.local


**Generar las llaves SSH y copiarlas a cada uno de los host que pertenecen al laboratorio**

ssh-keygen

ssh-copy-id orquestador.labansbile.local

ssh-copy-id testing.labansbile.local

ssh-copy-id produccion.labansbile.local

Agregar los permisos de ejecución sin inserción de password
/etc/sudoers.d/ansible
ansible ALL = (ALL) NOPASSWD: ALL

**Instalar Jenkiins en el orquestador**
# Scripts con Jenkins

# Descarga y automatización del repositorio
