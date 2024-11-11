# Daniel Miguelez Documentación EJERCICIO 2 - SSH COMANDOS

Ejercicio 2 - SSH + Command line (3 puntos) Documenta todos los pasos realizados en un archivo MarkDown. 
Accede a la máquina remota (el profesor facilitará la IP) mediante ssh:
Deberás ir al escritorio y crear un archivo de texto que contenga como nombre de archivo, 
tu nombre propio y apellido sin espacios y con extensión txt (por ejemplo ArnoldSchwarzenegger.txt) 
escribe en su interior el resultado de whoami. Después, mediante otro comando, concatena al final del
archivo el nombre del comando necesario para saber quién está conectado a la máquina mediante ssh.

1. Ejecutamos el primer comando para conectarnos al usuario del profesor : 

ssh usuario@192.168.0.185

CONTRASENA INTRODUCIDA : DAMWDAWM

2. Comando ls para ver donde estamos ubicados : 

ls

Descargas  Documentos  Imágenes  Plantillas  snap
Desktop    Escritorio  Música    Público     Vídeos

2.5. hice cd Desktop y todo el proceso, pero me confundi porque era en Escritorio.

cd Escritorio.

3. Creamos el documento con el comando 

touch DanielMiguelez.txt

Yo he utilizado esto para crearlo y nombrarlo : 

echo "$(whoami)" > DanielMiguelez.txt

4. Escribo el comando para entrar : 

nano DanielMiguelez.txt 

5. Escribo El usuario, y escribo who, para saber quien está conectado.

echo "who" >> DanielMiguelez.txt

### IMAGENES DEL PROCESO.

#### Aquí una breve descripcion en imagenes de los comandos utilizados.

[IMAGEN 1](./media/Pasos1.png)
[IMAGEN 2](./media/Pasos2.png)
[IMAGEN 3](./media/Pasos3.png)


# MEMORIA DEL VIRTUALHOST

Documenta todos los pasos realizados en un archivo MarkDown. Crea en tu máquina un virtualhost donde escribiendo “daw.ejercicio3.com” nos envíe a una web local ubicada en /var/www/miWeb, y que el correo de administrador sea el tuyo. No cierres la máquina al acabar el examen para poder comprobar su funcionamiento.


1. Creamos dentro de la carpeta var/www el directorio miWeb:

sudo mkdir -p /var/miWeb

2. Nos aseguramos de que sea accesible para apache : 

sudo chown -R www-data:www-data /var/miWeb

3. Crear el archivo de configuración del VirtualHost

sudo nano /etc/apache2/sites-available/daw.ejercicio3.com.conf

4. Cambiamos el virtual host data a lo siguiente : 

[Virtual host con datos nuevos](./media/VirtualHostChanges.png)

5. Configurar el archivo de hosts

Debemos asociar el dominio daw.ejercicio3.com a 127.0.0.1 (localhost) en el archivo /etc/hosts.

sudo nano /etc/hosts

Agrega la siguiente línea al final del archivo:

127.0.0.1 daw.ejercicio3.com

[Virtual host con datos nuevos](./media/anyadiendoPuerto.png)

6. Una vez configurado el archivo, habilita el sitio en Apache:

sudo a2ensite daw.ejercicio3.com.conf

7. Reiniciar Apache

Para que los cambios tengan efecto, reinicia Apache:

sudo systemctl restart apache2

8. Verificar el funcionamiento

Asegúrate de que Apache esté funcionando correctamente y que el sitio esté accesible. Puedes abrir un navegador web e ir a:

[Virtual host con datos nuevos](./media/FInal%20imagen%20.png)

[Enlace del texto](http://daw.ejercicio3.com/index.txt)





