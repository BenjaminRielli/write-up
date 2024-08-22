# Write-up del armado de un ambiente de pruebas de aplicaciones. 

### Introducción
Este Write-up describe el proceso de configuración de un ambiente de pruebas en una máquina virtual con Kali Linux. Este entorno se utilizará para realizar pruebas de seguridad en aplicaciones web. En particular, configuraremos una máquina virtual en VirtualBox, instalaremos un proxy de interceptación llamado BurpSuite, configuraremos Docker, ejecutaremos OWASP Juice Shop en un contenedor y finalmente, verificaremos el tráfico a través del proxy.

### 1. Instalaciones necesarias
  1. Software de virtualización: [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  2. [Maquina virtual de Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines) en VirtualBox.
*Ya iniciada la maquina virtual:*
  4. [Docker](https://docs.docker.com/desktop/install/linux-install/).
  5. Contenedor de Docker de [OWASP Juice Shop](https://hub.docker.com/r/bkimminich/juice-shop).

>[!IMPORTANT]
   >Burp Suite viene instalado de forma predeterminada en Kali Linux.

### 2. Proceso de configuración  
  1. Iniciar el contenedor de Docker.     

![Iniciando contenedor](/assets/iniciando.png)

  2. Abre Burp Suite.
  3. Navega a la pestaña proxy, presiona abrir el navegador y enciende el intercept.
  4. En el navegador abierto navegue a la ruta que se especifica -> Ejemplo `http://localhost:3000`.


## DEMOS
Se realizaron algunas intercepciones a modo de demostrar algunas vulnerabilidades de la web. A continuación detalladamente se mostraran con imágenes.

### Demo N°1
Interceptamos el envío de un feedback del cliente, para así modificar el valor del rating que está limitado del 1 al 5. 

![Interceptando petición](/assets/interceptor.png "Petición del envio del formulario")

Al modificar la request, notamos que se logra modificar a gusto el valor del rating.

![Modificando rating](/assets/rating0.png)

### Demo N°2
También, interceptamos la petición del form del login.

![Envio login](/assets/login.png)

