# Ejercicio 3: Git. Trabajando con ramas y uniones
## Introducción 
En estas tareas se trabajarán algunos aspectos sobre el uso de las ramas siendo las principales funciones a trabajar la creación de ramas, la fusión de ramas, la eliminación de ramas y los conflictos que estas acciones pueden conllevar.
## Desarrollo
Para realizar este ejercicio el primer paso es hacer un **git branch primera** para crear una rama que se llame primera. Para comprobar que se ha creado correctamente la rama he hecho un **git branch** para poder ver las ramas que existen. También he hecho un **ls** para saber qué archivos hay en el repositorio.    

![Paso 1](./Imagenes/Ej2_Captura1.png)

Como hay que crear un archivo en la rama primera lo que he hecho ha sido cambiar la rama con un **git checkout primera** para posteriormente hacer un **git branch** para comprobar que se ha cambiado correctamente de rama.  
  
![Paso 2](./Imagenes/Ej2_Captura2.png)  

Tras asegurarme de estar en la rama correcta he creado el archivo con **nano archivo.txt** con el que entro en el archivo para poder añadirle contenido. Después de crear el archivo he hecho un **git add .** para preparar los cambios y un **git commit -m “Creado aerchivo.txt”** para guardar los cambios realizados.   
 
![Paso 3](./Imagenes/Ej2_Captura3.png)   

![Paso 3.1](./Imagenes/Ej2_Captura3.1.png)

A continuación, he hecho un **git checkout main** para volver a la rama main y desde allí con un **git merge primera** fusionar el contenido de ambas ramas.  

![Paso 4](./Imagenes/Ej2_Captura4.png)  

No se ha producido ningún conflicto ya que el archivo creado en la rama primera (archivo.txt) solo existe en esa rama mientras que los archivos de la rama main solo existen en la rama main por lo que el git puede juntar los archivos de ambas ramas sin problema.  

Para eliminar la rama primera primero me he asegurado de que me encuentro situada en la rama main utilizando un **git branch** para después ejecutar un **git branch -d primera** para eliminar la rama, posteriormente he ejecutado un **git branch** para asegurarme de que la rama primera ya no existe.    

![Paso 5](./Imagenes/Ej2_Captura5.png)

Para crear la rama segunda he utilizado un **git branch segunda**. Para poder realizar el ejercicio correctamente he hecho un **ls** cuando aún me encontraba en la rama main para saber qué archivos hay en esta rama. A continuación, he cambiado de rama yendo de la rama main a la rama segunda con el comando **git checkout segunda**.   

![Paso 6](./Imagenes/Ej2_Captura6.png)  

Tras los pasos anteriores he elegido un archivo de los que se encuentran en la rama segunda el cual voy a modificar que en este caso será el archivo de texto llamado archivo.   

Para modificar el archivo he hecho un **nano archivo.txt** y he modificado el contenido de este archivo. Después he hecho un **git add .** para preparar los cambios y un **git commit -m “Modificado archivo.txt”** para guardar los cambios realizados.  

![Paso 7](./Imagenes/Ej2_Captura7.png)   

![Paso 7.1](./Imagenes/Ej2_Captura7.1.png)  

Tras haber cambiado el contenido de archivo.txt he vuelto a la rama main con el comando **git checkout main** y he intentado fusionar el contenido de ambas ramas con el comando **git merge segunda** lo que ha dado un conflicto porque el contenido del archivo archivo.txt de segunda y el contenido del archivo archivo.txt de main es diferente.  

![Paso 8](./Imagenes/Ej2_Captura8.png)  

Para solucionar el conflicto he entrado en el archivo que da problemas con un **nano archivo.txt** y he modificado su contenido para que solo tenga la información que deseo que en este caso será la información proveniente de la rama main.

![Paso 9](./Imagenes/Ej2_Captura9.png)    

![Paso 9.1](./Imagenes/Ej2_Captura9.1.png)  

![Paso 9.2](./Imagenes/Ej2_Captura9.2.png)

Tras haber resuelto el conflicto se podrá hacer un **git add .** , un **git commit -m “Solucionado el conflicto”** y un **git push origin main** para actualizar el repositorio que se encuentra en github y posteriormente cuando sea necesario poder hacer un git pull en el Debian 13 para actualizar también su repositorio.  

![Paso 10](./Imagenes/Ej2_Captura10.png)    

![Paso 11](./Imagenes/Ej2_Captura11.png)   

Podemos observar en las imagenes que se muestran a continuación como se ha dispuesto el repositorio de github tras habrle realizado los cambios exigidos en el presente ejercicio.  
En la primera imagen podemos ver como estan estructuradas las ramas y en el segundo podemos ver como esta estructurado el repositorio utilizado en el ejercicio.   

![Paso 12.1](./Imagenes/Ej2_Captura12.1.png)  

![Paso 12](./Imagenes/Ej2_Captura12.png)