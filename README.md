# README-PROXY-INVERSO-EN-DOCKER
<p>1. Instalamos una máquina virtual de Ubuntu, podemos utilizar Hyper-V, Oracle VM VirtualBox...</p>
<p>2. Una vez instalado Ubuntu pasamos a la instalación con los siguientes comandos:</p>
<p>&nbsp; sudo apt update</p>
<p>&nbsp; sudo apt install docker.io</p>
<p>3. Hecho esto pasamos a instalar Docker Compose:</p>
<p>&nbsp; sudo apt install docker-compose</p>
<p>4. Creamos un archivo donde al ejecutarlo cargamos la imagen y los volúmenes de las dos páginas webs, la extensión de este archivo debe de ser .yml</p>
<p>5. Lanzamos el archivo con el siguiente comando:</p>
<p>&nbsp; docker-compose up -d</p>
<p>6. Comprobamos el site1 y el site 2, para ello utilizaremos el siguiente comando:</p>
<p>&nbsp; curl -H “Host: site1.com” localhost</p>
<p>&nbsp; curl -H “Host: site2.com” localhost</p>
