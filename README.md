# README-PROXY-INVERSO-EN-DOCKER
1. Instalamos una máquina virtual de Ubuntu, podemos utilizar Hyper-V, Oracle VM VirtualBox...

2. Una vez instalado Ubuntu pasamos a la instalación con los siguientes comandos:

   &nbsp;**sudo apt update**

   &nbsp;**sudo apt install docker-ce**

3. Hecho esto pasamos a instalar Docker Compose:

   &nbsp;**sudo apt install docker-compose**

4. Creamos un archivo donde al ejecutarlo cargamos la imagen y los volúmenes de las dos páginas webs, la extensión de este archivo debe de ser .yml

5. Lanzamos el archivo con el siguiente comando:

   &nbsp;**docker-compose up -d**

6. Comprobamos el site1 y el site 2, para ello utilizaremos el siguiente comando:

   &nbsp;**curl -H “Host: site1.com” localhost**

   &nbsp;**curl -H “Host: site2.com” localhost** 
