# Write-up del armado de un ambiente de pruebas de aplicaciones. 

### Introducción
Este Write-up describe el proceso de configuración de un ambiente de pruebas en una máquina virtual con Kali Linux. Este entorno se utilizará para realizar pruebas de seguridad en aplicaciones web. En particular, configuraremos una máquina virtual en VirtualBox, instalaremos un proxy de interceptación llamado BurpSuite, configuraremos Docker, ejecutaremos OWASP Juice Shop en un contenedor y finalmente, verificaremos el tráfico a través del proxy.

### 1. Instalaciones necesarias
  1. Software de virtualización: [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  2. [Maquina virtual de Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines) en VirtualBox.
  3. [Docker](https://docs.docker.com/desktop/install/linux-install/).
  4. Contenedor de Docker de [OWASP Juice Shop](https://hub.docker.com/r/bkimminich/juice-shop).

>[!NOTE]
   >
   >Burp Suite viene instalado de forma predeterminada en Kali Linux.

