# apache

Reemplace `$ALUMNO` por el nombre de su nombre de usuario en www.tecnologoinformatico.com

EJ: `dmascheroni`

1. Cree el directorio ~/repositorios y dentro clone el
repositorio: `https://github.com/TecnologoInformatico/AdmInf-web.git`
2. Actualice el repositorio de la lista de paquetes.
    `apt update`
3. Instalar el servidor Apache mediante apt.
4. Cree el directorio /var/www/$ALUMNO
5. Asigne como propietario del directorio su usuario.
6. Configure un nuevo Virtual host. (copiando el archivo de configuración por defecto)
  6.1. ServerName $ALUMNO.tecnologoinformatico.com
  6.2. Correo de contacto con el administrador.
  6.3. El root de la aplicación. (/var/www/$ALUMNO)
7. Modifique el archivo /etc/hosts de modo que el ServerName coincida con este equipo `127.0.0.1`.
8. Reinicie el servidor apache para que los cambios tengan efecto.
9. Copie el contenido del directorio ~/repositorios/AdmInf-web a /var/www/$ALUMNO, de tal modo que el contenido del repositorio antes clonado se encuentre en el root de la aplicación.
10. Verifique que el servidor funcione correctamente.
11. Ingrese la IP del servidor y el servername a continuación:

```json
{
    "serverName": "",
    "ip": ""
}
```
1.	mkdir repositorio
	cd repositorio/
	git clone https://github.com/TecnologoInformatico/AdmInf-web.git
2.	sudo apt update
3.	 sudo apt install apache2
4.	sudo mkdir /var/www/ninthamoussu
5.	sudo chown ubuntu: ninthamoussu
6.	cd /etc/apache2/sites-available/
//sudo cp 000-default.conf ninthamoussu.conf
     sudo nano ninthamoussu.conf
//(cambio los campos #ServerName (ninthamoussu.tecnologoinformatico.com),
//#DocumentRoot (/var/www/ninthamoussu))
	sudo nano ninthamoussu.conf
	sudo nano /etc/hosts
//(cambio localhost poner ip(en mi caso 168.138.133.31)
//y en la ultima linea 127.0.0.1 ninthamoussu.tecnologoinformatico.com)
	sudo a2ensite ninthamoussu.conf
	sudo nano index.html
	sudo systemctl reload apache2.service
	curl 168.138.157.115 
//no muestra bien asi xq teng otro usuario
 y muestra al primero x defecto.
	al hacer curl ninthamoussu.tecnologoinformatico.com
//sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
//ahi si se mustra.
Ingrese la IP del servidor y el servername a continuación:
{
    "serverName":  ninthamoussu.tecnologoinformatico.com "",
    "ip":  168.138.157.115""
}


