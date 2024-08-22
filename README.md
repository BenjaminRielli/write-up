# Write-up del armado de un ambiente de pruebas de aplicaciones. 

### Introducción
Este Write-up describe el proceso de configuración de un ambiente de pruebas en una máquina virtual con Kali Linux. Este entorno se utilizará para realizar pruebas de seguridad en aplicaciones web. En particular, configuraremos una máquina virtual en VirtualBox, instalaremos un proxy de interceptación llamado BurpSuite, configuraremos Docker, ejecutaremos OWASP Juice Shop en un contenedor y finalmente, verificaremos el tráfico a través del proxy.

### 1. Instalaciones necesarias
  1. Software de virtualización: VirtualBox.
  2. Maquina virtual de Kali Linux en VirtualBox.
  3. Docker.
  4. Contenedor de Docker de OWASP Juice Shop.
     
### 1.1 Instalaciones no necesarias
  1. Burp Suite viene instalado de forma predeterminada en Kali Linux.
