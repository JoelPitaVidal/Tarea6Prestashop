#Instalacion e inicio del servicio

Al ejecutar el comando -`sudo docker compose up -d`, nos aparecerá una lista de pulls
que se están realizando y terminará  el proceso diciendo que los dos contenedores, tanto del
prestashop como de la base de datos están funcionando.

Accedemos al menú de instalación desde el navegador, poniendo lo siguiente:
-`http://192.168.0.30:9800`

![Texto alternativo](inicio-copia.png)

Seleccionamos el idioma y le damos a siguiente

![Texto alternativo](licencias.png)

Aceptamos todos los acuerdos y licencias pertinentes

![Texto alternativo](informacion-copia.png)

Introducimos la información sobre nuestra tienda, el nombre y el país, 
y los datos de la cuenta:
-Nombre.
-Apellidos. 
-Contraseña.
-Mail.

![Texto alternativo](modulos.png)

Instalamos los módulos adicionales

![Texto alternativo](ConexionBD-copia.png)

introducimos las credenciales de la base de datos:
-Dirección del servidor.
-Nombre.
-Usuario.
-Contraseña.
-Prefijo de las tablas.

![Texto alternativo](instalacion.png)

Y finalmente esperamos a que la instalación termine.

Es necesario hacer dos cosas en la terminal antes de 
acceder a la tienda ya que si no no permite hacerlo.

1:Eliminar la carpeta install donde está el contenedor ejecutándose de prestashop
-`docker exec -it nombre_o_id_del_contenedor_prestashop rm -rf /var/www/html/install`

2:#Renombrar la carpeta admin de dentro del contenedor donde está ejecutandose prestashop, es una medida de seguridad extra
-`docker exec -it <nombre_o_id_del_contenedor_prestashop> mv /var/www/html/admin /var/www/html/admin896sjdin1230jdndi`


