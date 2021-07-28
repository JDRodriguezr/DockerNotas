Se montó una plataforma de jenkins. Para esto seguimos los pasos vistos en la
clase 

Comenzamos utilizando el repositorio del profe, clonamos el repositorio con el comando

git clone https://github.com/jsgiraldoh/Jenkins

Entramos en el directorio descargado

cd Jenkins

Usamos docker-compose para levantar el archivo yml usando el siguiente comando

sudo docker-compose -f docker-compose-jenkins.yml up

Esperamos un error de permisos con el comando anterior, porque una vez creados los archivos
podemos cambiar los permisos para ahora si poder montar todo con los siguientes 2 comandos

'sudo chown usuario:usuario jenkins_home/'

'sudo chmod 2777 jenkins_home/'

con esto ya esta todo preparado para iniciar el servidor local, por lo que lo iniciamos con el comando

'sudo docker-compose -f docker-compose-jenkins.yml up -d'

Con eso queda iniciado el servidor, ahora toca usar el comando 

'docker logs -f jenkins'

Y asi podemos encontrar la clave para luego ingresarla en el navegador (accediendo con la ip enconrtada con el comando ip a s)
copiamos la clave y la ingresamos en el sitio
Y con esto ya queda montado el proyecto



