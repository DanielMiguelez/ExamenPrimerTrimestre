# Daniel Miguelez Documentación

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

3. Creamos el documento con el comando 

touch DanielMiguelez.txt

Yo he utilizado esto para crearlo y nombrarlo : 

echo "$(whoami)" > DanielMiguelez.txt

4. Escribo el comando para entrar : 

nano DanielMiguelez.txt 

5. Escribo El usuario, y escribo who, para saber quien está conectado.

### IMAGENES DEL PROCESO.

#### Aquí una breve descripcion en imagenes de los comandos utilizados.

[IMAGEN 1](./media/Pasos1.png)
[IMAGEN 2](./media/Pasos2.png)
[IMAGEN 3](./media/Pasos3.png)