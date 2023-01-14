### Chuleta de control de versiones con git

Guía de Estudio para el Control de Versiones
Guía de Estudio de la parte de Gestión de la Documentación - Control de Versiones. Indica qué tenemos que saber y saber hacer en la asignatura de Proyectos de Sistemas Electrónicos.
### Conceptos mínimos que tenemos que saber sobre el control de versiones:
Definir brevemente en qué consiste el control de versiones.
Es la práctica de rastrear y gestionar los cambios en el código de software. Los sistemas de control de versiones son herramientas de software que ayudan a los equipos de software a gestionar los cambios en el código fuente a lo largo del tiempo.
Explicar los siguientes conceptos:
-  repositorio local: la carpeta donde se encuentran los archivos de tu proyecto
- copia local: Cuando creas un repositorio en GitHub.com, este existe como un repositorio remoto. Puedes clonar tu repositorio para crear una copia local en tu computadora y sincronizarla entre las dos ubicaciones.
-  repositorio remoto: son versiones de tu proyecto que están hospedadas en Internet o en cualquier otra red.
- log:

 ![image](https://user-images.githubusercontent.com/105022032/212482127-fb654bc7-a638-489e-a3b3-59938cf08f4d.png)
-  conflicto:  surgen cuando dos personas han cambiado las mismas líneas de un archivo o si un desarrollador ha eliminado un archivo mientras otro lo estaba modificando. En estos casos, Git no puede determinar automáticamente qué es correcto.
Explicar los siguientes estados de un fichero:
-	Sin seguimiento: archivos que solo son locales y no existen en el repositorio remoto.

-	Confirmado (git commit): Es el archivo que ya está almacenado en el repositorio. La última versión y la copia loca son iguales.

 ![image](https://user-images.githubusercontent.com/105022032/212482207-5dbe122a-de42-45ad-9330-866404ba586d.png)


-	Modificado (modified file): Es el fichero modificado en la copia local y existe una diferencia entre la copia local y la última versión en el repositorio.

-	Preparado (staged file): Es la copia del fichero modificado preparada para ser confirmada en la próxima operación de confirmación (commit).La zona de preparación (staging área or index) contiene todos los ficheros preparados.

-	Ignorado (ignored file): Es el fichero que está en el directorio local pero que deliberadamente no se somete a control de versi0ones.

Explicar las siguientes operaciones:
-	Clone (Clonar):
 ![image](https://user-images.githubusercontent.com/105022032/212482247-97710c92-7764-446e-aa8c-3ccfd5a95066.png)

-	Add (Añadir):
 ![image](https://user-images.githubusercontent.com/105022032/212482275-8d663b8b-979d-4be7-b345-e17cc0a2b117.png)

-	Commit (Confirmar):
 ![image](https://user-images.githubusercontent.com/105022032/212482286-67b865f4-7588-4c78-b2d0-9d0469218f80.png)

-	Push (Enviar):
 ![image](https://user-images.githubusercontent.com/105022032/212482295-9d1eca01-74b5-4315-8e69-8a6ce0b29ae5.png)

-	Pull (Traer):

 ![image](https://user-images.githubusercontent.com/105022032/212482304-9841b46c-aa45-4e52-af0e-8395f30b8a0e.png)

-	Fork (Duplicado): Crear una copia de un repositorio. Esto es especialmente útil para modificar proyectos sin afectar al proyecto original.

-	Pull Request (entre repositories): Petición que hace el desarrollador de que los cambios hechos en su repositorio clonado mediante un FORK sean incorporados al repositorio original.

Nombrar al menos dos servicios de repositorio remoto para el control de versiones:
-	GitHub
-	GitLab
-	BitBucket
Nombrar al menos un cliente gráfico (GUI) para el control de versiones:
-	Gitg
-	Gitkraken
-	Gitblade
-	sourcetree



### En el intérprete de comandos de git-bash
Mostrar en qué directorio estamos.
Para saber en qué directorio estamos hay que poner el comando pwd.

### Crear un directorio.
Para crear un directorio hay que introducir el comando mkdir seguido del nombre que se le quiera poner al nuevo directorio.
Ejemplo: mkdir miscosas

### Cambiar de directorio

Para cambiar de directorio hay que introducir cd seguido del nombre del directorio al que se quiere ir.
Ejemplo: cd Escritorio

### Mostrar la lista de ficheros de un directorio

Con el fichero ls se muestra la lista de ficheros que hay en el directorio.

### Borrar un fichero

Con el comando rm eliminamos un fichero.
Ejemplo: rm prueba.txt

### Cambiar (mover) un fichero de directorio

Para mover un fichero de un directorio a otro, se utiliza el comando mv.
Con mv también se puede renombrar.
Ejemplo: mv prueba.txt nuevo.txt  -> cambia el nombre de prueba.txt a nuevo.txt
Ejemplo: mv prueba.txt directorio/ -> mueve el fichero prueba.txt a directorio




### En control de versiones local

### Crear un repositorio local en nuestra maquina

Utilizando el comando “git init” se creará un nuevo repositorio en el directoria actual utilizado. Para agregar los archivos en el repositorio, utiliza el comando “git add”. También puedes añadirlo archivos específicos utilizando su nombre
Ejemplo: “git add archivo.txt”

### Preparar ficheros para ser confirmados en un repositorio local

Utilizamos el comando “cd” para ver en el directorio del repositorio local.
Con el comando “git status” se mostrará una lista de archivos nuevos o modificados que no han sido confirmados todavía.
Utilizando el comando “git commit” se quedarán registrado en el historial del repositorio y ya no podrán ser eliminados.
Para revisar tus commits y ver el historial del repositorio utiliza el comando “git log”

### Configurar cambios en un repositorio local

Para configurar cambios en un repositorio Git local, puedes seguir estos pasos:

Asegúrate de estar en el directorio del repositorio local. Puedes hacer esto utilizando el comando "cd" seguido del nombre del directorio.

Verifica el estado actual de tu repositorio con el comando "git status". Esto te mostrará una lista de archivos nuevos o modificados que no han sido confirmados todavía.

Realiza los cambios necesarios en los archivos.

Verifica el estado del repositorio nuevamente con el comando "git status" esto te indicara los archivos que han sido modificados y estan listos para ser confirmados.

Agrega los archivos modificados al stage area utilizando el comando "git add" con los archivos modificados específicos o "git add ." para agregar todos los cambios.

Haz un "commit" de los cambios utilizando el comando "git commit" seguido de un mensaje que describa los cambios que estás agregando. 

Con estos pasos ya tendrás configurado tus cambios en el repositorio local y estarán listos para ser confirmados.

### Deshacer la operación de reparar

Se puede utilizar los comando “git revert” o “git reset”

Utilizando el comando "git revert" crea un nuevo commit que deshace los cambios de un commit específico. Por ejemplo, si deseas deshacer el último commit, puedes utilizar el comando "git revert HEAD".

El comando "git reset" deshace los cambios de un commit específico, pero en lugar de crear un nuevo commit, los cambios se revierten directamente en el directorio de trabajo y en el área de stage. Si deseas deshacer el último commit, puedes utilizar el comando "git reset HEAD~" para deshacer el commit anterior, esto también eliminará el commit en cuestión del historial del repositorio.

Es importante mencionar que al usar "git reset" se pierde de forma permanente el commit y los cambios relacionados con él, si se desea mantener un registro de dicho commit es mejor usar "git revert"

### Deshacer la operación de confirmar

Para deshacer una operación de confirmar (commit) en un repositorio Git local, hay varias opciones disponibles:

Utilizar el comando "git reset" para deshacer el último commit y mantener los cambios en el área de stage. Por ejemplo, para deshacer el último commit y mantener los cambios en el área de stage, puedes utilizar el comando "git reset HEAD~" o "git reset HEAD^" esto permitirá que vuelvas a editar los cambios y hacer un nuevo commit con los cambios deseados.

Utilizar el comando "git reset" con la opción "--soft" para deshacer el último commit y mantener los cambios tanto en el área de stage como en el directorio de trabajo. Por ejemplo, para deshacer el último commit y mantener los cambios en el área de stage y en el directorio de trabajo, puedes utilizar el comando "git reset --soft HEAD~"

Utilizar el comando "git reset" con la opción "--hard" para deshacer el último commit y eliminar los cambios tanto en el área de stage como en el directorio de trabajo. Este comando elimina los cambios y modificaciones realizadas en el repositorio de forma permanente y no podrán ser recuperadas, por lo que se recomienda hacer una copia de seguridad antes de utilizar este comando.

Utilizar el comando "git revert" para crear un nuevo commit que deshace los cambios del commit previo, manteniendo la trazabilidad de los commits realizados y permitiendo revertirlos en caso de ser necesario.

Es importante mencionar que al usar "git reset" con la opción "--hard" se pierde de forma permanente el commit y los cambios relacionados con el, si se desea mantener un registro de dicho commit es mejor usar "git revert"

En cualquier caso es recomendable hacer un backup o un clone antes de realizar cualquier cambio en el repositorio ya que estos comandos pueden causar pérdida de información.

### Identificar el estado de un fichero o ficheros en un repositorio local

Puedes utilizar el comando "git status" junto con el nombre del archivo o archivos.

Este comando te mostrará información sobre los archivos específicos, como si están en el área de stage, si han sido modificados, si tienen conflictos, entre otros.
Ejemplo: "git status nombre_del_archivo.txt"

Te mostrará el estado del archivo especificado, si está en el stage area, si ha sido modificado, etc.

Tambien puedes utilizar el comando "git diff" para ver las diferencias entre los cambios realizados y los cambios confirmados.
Ejemplo: "git diff nombre_del_archivo.txt"

Este comando te mostrará las diferencias entre el archivo actual y la última versión confirmada del mismo.

Con estos comandos podrás identificar el estado de cualquier archivo en tu repositorio local, te ayudarán a saber si un archivo está listo para ser confirmado, si ha sido modificado pero no está en el stage area, etc.

### Descartar los cambios de un fichero de trabajo mediante la recuperación de una versión almacenada en el repositorio local

Puedes utilizar el comando "git checkout" junto con el nombre del archivo.

Este comando te permite deshacer cualquier cambio realizado en el archivo y recuperar la última versión confirmada del mismo.
Ejemplo: "git checkout nombre_del_archivo.txt"
Con este comando descartaras los cambios realizados en el archivo "nombre_del_archivo.txt" y se recuperara la última versión confirmada del mismo.


### Crear una rama en un repositorio local

Para crear una rama en un repositorio local, puedes utilizar el comando git branch seguido del nombre de la rama que deseas crear. 
Ejemplo: “git branch nueva-rama”

Este comando creará una nueva rama en el repositorio local, pero no te moverá a ella. Si deseas moverte a la nueva rama después de crearla, puedes utilizar el comando “git checkout” seguido del nombre de la rama:
Ejemplo: “git checkout nueva-rama”

También puedes crear una rama y moverte a ella en un solo comando usando la opción “-b” del comando “git checkout” 
Ejemplo: “git checkout -b nueva-rama”

Una vez que estés en la nueva rama, puedes comenzar a realizar cambios en el repositorio y luego utilizar los comandos “git add” y “git commit” para registrar los cambios en la rama.

Ten en cuenta que una rama creada en el repositorio local solo estará disponible en tu copia local del repositorio, si deseas compartir esa rama con los demás colaboradores del proyecto necesitaras usar el comando “git push” seguido del nombre de la rama y la url del repositorio remoto
Ejemplo: “git push origin nueva-rama”

Es importante verificar que estás trabajando en la rama correcta antes de realizar cualquier cambio o hacer un push, una buena práctica es antes de comenzar a trabajar en una nueva rama asegurarte de haber actualizado la rama actual y haber cambiado a la rama en la que deseas trabajar

### Cambiar de rama en la copia local

Para cambiar de rama en un repositorio local, puedes utilizar el comando “git checkout” seguido del nombre de la rama a la que deseas cambiar. 
Ejemplo: “git checkout develop”

Es importante tener en cuenta que si tienes cambios no guardados en la rama actual, git te pedirá que primero guardes o descartes los cambios antes de cambiar de rama.
Si tienes un cambio que no deseas perder puedes guardarlo en una nueva rama antes de cambiar a la rama deseada

Es recomendable antes de cambiar de rama, asegurarte de haber actualizado la rama actual con los últimos cambios y de haber guardado todos los cambios realizados en la rama actual.

Puedes verificar en que rama te encuentras actualmente usando el comando “git branch”, esto te mostrara las ramas existentes y la rama actual estará marcada con un asterisco (*). 
Ejemplo:
“git branch “
* develop
  master
  feature-branch
En este ejemplo estamos en la rama "develop"

Cambiando de rama se cambia el conjunto de archivos del repositorio, por lo que es recomendable verificar la integridad de los cambios al cambiar de rama, especialmente si estás trabajando en un equipo o en una rama con mucho tráfico de cambios.


### Control de versiones centralizado

•	Configurar git para que trabaje tras un proxy

	Configurar el proxy para Git globalmente en tu sistema:
	git config --global http.proxy 				http://proxyuser:proxypass@proxy.server.com:8080

Configurar el proxy para Git para un repositorio específico:

	cd /path/to/repo
	git config http.proxy http://proxyuser:proxypass@proxy.server.com:8080

Reemplaza proxyuser, proxypass y proxy.server.com con los datos de tu proxy

Si deseas desactivar el proxy:

		git config --global --unset http.proxy

				ó

		git config --unset http.proxy


•	Replicar un repositorio remoto localmente en nuestra máquina.
	
Para replicar un repositorio remoto en tu máquina local, puedes usar el comando ‘git clone’. Este comando descarga una copia completa del repositorio en tu máquina, y también establece una conexión con el repositorio remoto original, para que puedas sincronizar tus cambios con él.

La sintaxis básica del comando es la siguiente:

				git clone <URL del repositorio>

donde <URL del repositorio> es la dirección web del repositorio que quieres clonar. 

 
El comando creará una nueva carpeta con el nombre del repositorio y descargará todos los archivos dentro de él.
Puedes agregar opcionalmente -b para especificar una rama en específico de la cual quieres clonar

			git clone -b <branch> <URL del repositorio>

También puede utilizar la opcional -depth para limitar la cantidad de commits a los cuales se descarga:
		
		git clone --depth <numero> <URL del repositorio>

 
Una vez que hayas clonado el repositorio, podrás utilizar comandos como ‘git pull’ y ‘git push’ para sincronizar tus cambios con el repositorio remoto.


•	Replicar un repositorio local en un servidor remoto.

Para replicar un repositorio local en un servidor remoto, primero debes crear un repositorio vacío en el servidor remoto.

					git init –bare

Una vez que el repositorio remoto esté creado, puedes agregarlo como un remoto en tu repositorio local. Para hacerlo, utiliza el comando ‘git remote add’:

		git remote add <nombre_remoto> <URL del repositorio remoto>

Donde nombre_remoto es un nombre que elijas para identificar el repositorio remoto, y URL del repositorio remoto es la URL del repositorio remoto recién creado.



•	Traer los cambios de un repositorio remoto a un repositorio local.

Para traer los cambios de un repositorio remoto a un repositorio local, puedes utilizar el comando ‘git pull’. Este comando combina los pasos de ‘git fetch’ y ‘git merge’ para descargar los cambios del repositorio remoto y combinarlos con tu versión local.
La sintaxis básica del comando es la siguiente:
		
			git pull <nombre_remoto> <branch>

Donde <nombre_remoto> es el nombre que le diste al repositorio remoto cuando lo agregaste con ‘git remote add’, y ‘<branch>’ es la rama que deseas traer los cambios. Si no especificas una rama, por defecto se usará la rama principal


•	Resolver los conflictos que se puedan producir al traerse estos cambios.
Pasos para resolver un conflicto:

1.	Usa el comando ‘git status’ para ver los archivos con conflictos
2.	Edita los archivos en conflicto y resuelve los problemas marcados por las etiquetas especiales. Puedes hacerlo con cualquier editor de texto o con un programa de merge especializado.
3.	Una vez que hayas resuelto los conflictos en el archivo, guarda los cambios.
4.	Usa el comando ‘git add’ para agregar el archivo resuelto
5.	Utiliza el comando ‘git commit’ para guardar los cambios locales y finalizar el merge.

•	Enviar los cambios de un repositorio local a uno remoto.

Utiliza el comando ‘git push’ para enviar los cambios al repositorio remoto. Asegúrate de especificar la rama correcta. 

Es recomendable previamente hacer un ‘git pull’ para asegurar tener la última versión del repositorio remoto y evitar conflictos.

•	Enviar una rama local al repositorio remoto.

Utiliza el comando ‘git push’ para enviar los cambios de la rama local al repositorio remoto. Asegúrate de especificar la rama correcta. Por ejemplo, si estás enviando los cambios de la rama "nueva_caracteristica" al repositorio remoto, puedes usar ‘git push origin nueva_caracteristica’.

Es recomendable previamente hacer un ‘git pull’ para asegurar tener la última versión del repositorio remoto y evitar conflictos.


•	Incorporar a ramas locales cambios que se producen en el repositorio remoto.

Para incorporar cambios que se producen en el repositorio remoto a ramas locales, puedes utilizar el comando ‘git pull’. El comando ‘git pull’ es una combinación de dos comandos: ‘git fetch’ y ‘git merge’. ‘git fetch’ recupera los cambios del repositorio remoto, mientras que ‘git merge’ los aplica a tu rama local.



•	Realizar un pull request entre dos ramas de un repositorio remoto.
1.	Haz un fork del repositorio remoto al cual quieres enviar el pull request.
2.	Clona el repositorio remoto forked en tu ordenador local.
3.	Crea una rama local para contener los cambios que quieres proponer.
4.	Realiza los cambios y haz un commit en tu rama local.
5.	Haz un push de tu rama local al repositorio remoto forked.
6.	Vete a la página de GitHub del repositorio remoto original y haz un pull request desde tu rama forked.
7.	Revisa las diferencias y envia el pull request.
8.	Este puede ser revisado y si es aceptado se mergea a la rama principal del repositorio remoto.                                                                                        


Recuerda que cada repositorio remoto puede tener configuraciones y requerimientos diferentes.






### Control de versiones distribuido

### •	Realizar un pull request entre dos repositorios que resultaron de un Fork.
Para realizar un pull request entre dos repositorios que resultaron de un fork, primero debes asegurarte de que tienes acceso de escritura al repositorio al que quieres hacer el pull request (el "repositorio principal"). Si no tienes acceso de escritura, no podrás hacer un pull request directamente.
Una vez que tienes acceso de escritura al repositorio principal, debes seguir estos pasos:

1.	Haz un fork del repositorio principal en tu cuenta de GitHub. Esto creará una copia del repositorio en tu cuenta.
2.	Clona el repositorio que acabas de forkear a tu computadora local usando el comando git clone.
3.	Agrega el repositorio original como una "fuente remota" de tu repositorio local, utilizando el comando git remote add upstream.
4.	Crea una nueva rama en tu repositorio local donde harás los cambios necesarios, usando git branch y luego git checkout
5.	Haz tus cambios en esa rama y luego utiliza git add y git commit para guardarlos en tu repositorio local.
6.	Haz git push para subir tus cambios a tu repositorio en GitHub.
7.	Vete a la página de GitHub de tu repositorio y haz click en el boton de "New pull request".
8.	Selecciona la rama donde hiciste los cambios y envia el pull request.

