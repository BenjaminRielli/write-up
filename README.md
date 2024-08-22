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
  1. Abrir el navegador y confirmar que esté configurado para utilizar el proxy de Burp Suite.
  2. Iniciar el contenedor de Docker.
     ![Iniciando contenedor](/assets/images/contenedor.png)
  4. Navega a la ruta que se especifica -> Ejemplo `http://localhost:3000`.
  5. Abre Burp Suite.
  6. Para interceptar cualquier petición, navega a la pestaña proxy y enciende el intercept.


### 3. Ejemplos de intercepciones
