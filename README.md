# README PROXY INVERSO EN DOCKER
## DOCKER-COMPOSE
1. Instalamos una máquina virtual de Ubuntu, podemos utilizar Hyper-V, Oracle VM VirtualBox...

2. Una vez instalado Ubuntu pasamos a la instalación con los siguientes comandos:

   &nbsp;**sudo apt update**

   &nbsp;**sudo apt install docker-ce**

3. Hecho esto pasamos a instalar Docker Compose:

   &nbsp;**sudo apt install docker-compose**

4. Creamos un archivo donde al ejecutarlo cargamos la imagen y los volúmenes de las dos páginas webs, la extensión de este archivo debe de ser **.yml**

5. Lanzamos el archivo con el siguiente comando:

   &nbsp;**docker-compose up -d**

6. Comprobamos el site1 y el site 2, para ello utilizaremos el siguiente comando:

   &nbsp;**curl -H “Host: site1.com” localhost**

   &nbsp;**curl -H “Host: site2.com” localhost** 

## BALANCE DE CARGA CON NGINX
1. Instalamos Nginx.  <br> 
&nbsp;**sudo apt install nginx**

2. Entramos el contenedor de Docker de las páginas 1 y 2, luego introducimos los siguientes comandos:<br> 
&nbsp;**rm -rf /usr/share/nginx/html/index.html**<br> 
&nbsp;**nano /usr/share/nginx/html/index.html** (archivo subido)<br>

3. Configuramos un balanceador de carga Nginx. Eliminamos el archivo de configuración predeterminado de Nginx y creamos un nuevo archivo de configuración del balanceador de carga:<br>
&nbsp;**rm -rf /etc/nginx/conf.d/default.conf**<br> 
&nbsp;**nano /etc/nginx/conf.d/load-balancing.conf** (archivo subido)<br>

4. Reiniciamos Nginx en el contenedor y comprobamos en el navegador:<br> 
&nbsp;**sudo docker exec -i -t dc2 /bin/bash**<br>
