# Ejercicio 1: Introducción a git y GitHub
## Introducción
En este ejercicio se creará un repositorio local en Windows con dos archivos el cual habrá que conectar con github y posteriormente habrá que clonar en una máquina virtual Debian 13. Además, se realizarán cambios desde el repositorio local de Windows haciendo que posteriormente haya que actualizar tanto el repositorio de github como el repositorio de Debian 13.
## Desarrollo del ejercicio
Para crear el repositorio prueba2_Alicia de forma local en Windows lo primero que he hecho ha sido entrar en git bash y con he cd para ir al lugar adecuado donde crear el repositorio. Para crear el repositorio he utilizado el comando **mkdir prueba2_Alicia** tras lo cual he inicializado el repositorio con el comando **git init**.     

![Paso 1](<./imagenes/Ej1_Captura 1.png>) 

Tras tener el repositorio creado he entrado en él con el comando **cd prueba2_Alicia** y en el he creado dos archivos de texto utilizando el comando **echo “Nuevo archivo1”>archivo1.txt** para el primero y **echo “Nuevo archivo2”>archivo2.txt** para el segundo.  

![Paso 2](<./Imagenes/Ej1_Captura 2.png>)  

Tras haber creado los archivos he hecho un **git add .** para añadir los cambios realizados en el repositorio y posteriormente he hecho un **git commit -m “Se han creado los archivos archivo1 y archivo2”** para registrar los cambios que le he hecho al repositorio que en este caso sería añadirle dos archivos.    

![Paso 3](<./Imagenes/Ej1_Captura 3-2.png>)  

Para realizar el siguiente paso primero hay que ir a github y crear un nuevo repositorio para lo cual habrá que ir a Repositories y clicar el icono verde New para que salga una pantalla en la cual deberás colocar la información del repositorio que quieras crear y clicar en el botón verde Create repository. En este caso la información que se colocará será en Repository name pondre Prueba2_Alicia, en Description pondré Repositorio para el ejercicio1 Punto14 y en Configuration no modificaré nada dejando el repositorio público y no añadiendoni  README ni .gitignore ni license.  

![Paso 4](<./Imagenes/Ej1_Captura 4-1.png>)     

Como se puede comprobar en esta imagen se ha creado correctamente el repositorio en GitHub.  

![Paso 4.1](<./Imagenes/Ej1_Captura 4.1.png>)  

Teniendo el repositorio correctamente formado y con los elementos deseados he utilizado el comando **git remote add origin https:// AliciaSP2004:gpg.......@github. com/AliciaSP2004/Prueba2_Alicia.git** para conectar el repositorio local con el repositorio que he creado previamente. Para este comando es importante destacar que he utilizado la URL de un repositorio de github añadiéndole después del https:// el nombre del usuario al que se desea conectar y después de los : el token del usuario para que así se le permita al usuario modificar aspectos del repositorio.  

![Paso 5](<./Imagenes/Ej1_Captura 5-1.png>)  

Por último, para tener en los dos repositorios la misma información habrá que utilizar el comando **git push origin master** donde origin será el alias del repositorio remoto y master será el nombre de la rama.
![Paso 6](<./Imagenes/Ej1_Captura 6-1.png>)    

Como se puede comprobar en esta imagen  se han añadido los cambios al repositorio en GitHub de forma correcta.  

![Paso 6.1](<./Imagenes/Ej1_Captura 6.1-1.png>)
Para tener el repositorio en la máquina virtual de Debian 13 he accedido a este de forma remota utilizando Visual Studio Code tas lo cual he ejecutado el comando **git clone https: //AliciaSP2004:gpg.......@github. com/AliciaSP2004/Prueba2_Alicia. git** para clonar el repositorio de github en la máquina virtual.  

![Paso 7](<./Imagenes/Ej1_Captura 7-2.png>)  

De vuelta en git bash de Windows he comprobado que estoy en el repositorio prueba2_Alicia y he utilizado el comando **echo “Se crea el archivo3”>archivo3.txt** para crear el archivo de texto archivo3, además he utilizado el comando **nano archivo2.txt** para modificar el contenido del archivo de texto archivo2.   

![Paso 8](<./Imagenes/Ej1_Captura 8 -1.png>)  
  
![Paso 8.1](<./Imagenes/Ej1_Captura 8.1.png>)  

Tras modificar un archivo y crear otro he utilizado el comando **git add .** para añadir los cambios y el comando **git commit -m “Creado archivo3 y modificado archivo2”** para registrar los cambios que en este caso son modificar el archivo2 y añadir el archivo3.    

![Paso 9](<./Imagenes/Ej1_Captura 9.png>)

Para terminar en Windows he utilizado el comando **git push origin master** para añadir los cambios del repositorio local al repositorio remoto de github.  

![Paso 10](<./Imagenes/Ej1_Captura 10.png>)  
  
  Como se puede comprobar en esta imagen  se han añadido los cambios al repositorio en GitHub de forma correcta.  
  
![Paso 10.1](<./Imagenes/Ej1_Captura 10.1.png>)  

Al haberse hecho cambios en el repositorio local de Windows los cuales he subido al repositorio de github podemos observar que el repositorio que se encuentra en la máquina virtual de Debian 13 no está actualizado. Para actualizar el repositorio local del Debian 13 he ido a la conexión remota qué tengo en Visual Studio Code y utilizado el comando **git pull origin master**.

![Paso 11](<./Imagenes/Ej1_Captura 11.png>)  
