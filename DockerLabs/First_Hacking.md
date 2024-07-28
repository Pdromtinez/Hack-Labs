# Maquina First-Hacking 

### Empezamos con el reconocimiento a la IP designada

Empezamos con el escaneo de puertos usando la herramienta nmap:

![Escaneo realizado con nmap](/home/pedro/Imágenes/First-Hacking-IMAGES/2024-07-25_13-10_1.png)

En el resultado del escaneo, se identifica que el puerto 21 está abierto, lo que indica que el servicio FTP está activo con la versión "vsftpd 2.3.4" y se está ejecutando en un sistema operativo Unix.

![ServicioFTP](/home/pedro/Imágenes/First-Hacking-IMAGES/2024-07-25_13-16.png)

Procedemos a utilizar la herramienta Metasploit para determinar si existen vulnerabilidades asociadas a la versión del servicio detectado.

![metasploit-Console](/home/pedro/Imágenes/First-Hacking-IMAGES/2024-07-25_14-27.png)

Una vez identificado el exploit correspondiente para el servicio, seleccionamos la opción que nos permitirá obtener acceso, configurando el objetivo a vulnerar:

        msf6 exploit(unix/ftp/vsftpd_234_backdoor) > set RHOSTS (IP de la máquina)

![metasploitConsole](/home/pedro/Imágenes/First-Hacking-IMAGES/2024-07-25_15-31.png)

Metasploit ejecutará el script y obtendrá acceso al servicio FTP, permitiéndonos interactuar como el usuario indicado.

![fpt-terminal](/home/pedro/Imágenes/First-Hacking-IMAGES/2024-07-25_15-36.png)

Con estos pasos, hemos logrado un reconocimiento efectivo y la explotación exitosa de la vulnerabilidad detectada en el servicio FTP.

