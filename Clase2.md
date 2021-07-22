# Clase 2 de docker

Se siguieron los pasos especificados en la guia de docker https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository ademas de la resolucion de muchos problemas que se iban presentando durante la sesion

Empezamos haciendo la instalacion usando la maquina virtual. Primero actualizamos la version usando el comando 

`$ sudo apt-get update`

Luego se utiliza el siguiente comando para usar un repositorio usando HTTPS

`$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release`
    
Se añade la clave GPG oficial dada por docker

`$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`

Se utiliza el siguiente comando para configurar y definir el repositorio estable (stable) 

`$ echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
  
# Instalar el motor de Docker

` $ sudo apt-get update
 $ sudo apt-get install docker-ce docker-ce-cli containerd.io`
 
Tambien se especificó que se puede instalar una version en especifico si quisieramos, pero como queriamos utilizar la ultima version estable, descargamos la ultima dada por el sistema y leugo actualizamos con el comando

`$ sudo apt-get update`

#Herramientas adicionales

Utilizamos la herramienta de MobaXterm para conectarse con la maquina virtual pero teniendo acceso a los comandos de nuestro equipo principal. Esto con el fin de evitar errores al introducir las lineas de codigo previamente mostradas. 

