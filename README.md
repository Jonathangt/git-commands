# git-commands

### **==== Configuraciones Iniciales =====**

    git version
sirve para obtener la version de Git en uso.

    git config --global user.name "Nombre_de_usuario"
    git config --global user.email "correo"

Se ingresa el usuario  y su correo el cual hará los cambios en el proyecto o  en los archivos


    git config --global user.name                         
Muestra el resultado


    git config --global -l
    git config --global --list   

Muestra los datos de configuracion ingresados.


    git config --global color.ui true            

Confirma el uso de colores por Git. --> COMPROBARLO

    git config --global alias.letra "comando por cambiar" 

Sirve para poner un alias a comandos ya predefinidos. ---> COMPROBARLO


### **==== Comandos principales =====**

    git init  

Es para empezar a monitorear nuestro proyecto (solo se ejecuta una vez)

    git status 

Nos indica el estado de nuestro proyecto, es decir, si estan listos para guardar o no.


### **==== Comandos para añadir el archivo al Stage =====**


    git add -A                                    
    git add .
    git add --all

Decimos que archivos estan listo para seguir el monitoreo o para hacerles "commit".
		      
    git add nombre_archivo.extension  
    git add carpeta/*.extension	


Agregar archivos que terminan con esa extension.

### **==== Comandos para quitar el archivo de Stage =====**

    git reset nombre_archivo.extension	
    git reset carpeta/*.extension	      

Este comando sirve para deshacer lo de "add" (quitar del stage)

    git reset --hard


Este comando sirve para deshacer tus cambios y regresar al ultimo commit realizado ---*****

### **==== Comitear los archivos ==============**

    git commit -m "Mensaje de referencia"  
Sirve para guardar los cambios que se han hecho en algun hito en el tiempo con un mensaje de referencia.


    git commit --amend -m "Nueva referncia editada"

Con este comando se modifica un comit ya establecido.

### **==== Comandos para interactuar con archivos =====**

    mkdir nombre_carpeta				      

Con este comando se crea un una carpeta.

    touch nombre_archivo.extencion			      

-> Permite crear archivos de cualquier extension en la carpeta ubicada actualmente

    git mv archivo.ext nombre_nuevo.ext		      

-> Se modifica el nombre del archivo.

    git rm archivo.ext				      

-> Elimina el archivo de la carpeta.



    git reset --soft <id(codigo de commit)>		      

-> No se recupera ningun archivo cuando se ubica en el commit deseado.

    git reset --hard <id(codigo de commit)>		      

-> Con eso se ubica al commit deseado recuperando archivos recuperados o desahciendo todos los cambios depsues de ese commit

    git reset --mixed <id(codigo de commit)>	      

-> Aqui se regresa a otro commit pero sin ver los commits realizados despues del commit al que se esta retornando.

### **======== Visualizacion de Cambios ===============**

    git reflog					      

-> Visualizacion total de cambios.

    git log                                               

-> Nos da una lista de todos los "commits" creados  con las fechas de los cambios (Se muestran del ultimo cambio al primero de forma descendente).

    git diff					      

-> Sirve para poder ver que cambios se han hecho a nivel de archivo.

    git log --oneline --decorate --all --graph	      

-> Lista compacta de cambios realizados incluido cambios con ramas.


### **==== Trabajo con Ramas ==================**

    git branch					      

-> Se muestra todas las ramas.

    git branch -a					      

-> Muestra todas las ramas incluidads las ocultas.


    git branch nombre_de_rama			      

-> Aqui se crea una nueva rama

    git merge rama					      

-> Con este codigo se une la rama seleccionada a la rama actual en la que se encuentra

    git branch -d nombre_rama			      

-> Se elimina la rama seleccionada


    git checkout -b nombre_rama			      

-> Se crea una rama y automaticamente se dirige a esa rama

    git checkout (nombre_de_rama / codigo_hash_commit)    

-> Con este comando podemos viajar o navegar entre los diferentes commits o ramas creados o diferentes lugares en el tiempo donde guardamos nuestro proyecto.git checkout .


### **==== Etiquetas===========================**

    git tag nombre_etiqueta				      
-> etiquetar un commit.

    git tag						      
-> Muestra la etiqueta actual.

    git tag -d nombre_etiqueta			      
-> Elimira la etiqueta mencionada.

    git tag -a version/mensaje1 -m "mensaje2"	      
-> Version ar archivos.

    git show version/mensaje			      
-> Sirve para tener detalles del commit

    git tag -a version/mensaje indentificador -m mensj2   
-> Etiquetar un commit ya pasado

### **==== Git y GitHub ========================**

    git clone direccion_github			      
-> Sirve para clonar un repositorio de github.

    git remote add origin direccion_github		      
-> Sirve para añadir un repositorio local al repositorio github (en si es como una conexion al nuevo repositorio)

    git push -u origin master		              
-> Para actualizar y subirlo

    git push origin master				      
-> Se mandan cambios al github.

    git pull					      
-> Sirve para actualizar nuestra carpeta local despues de haber hecho cambios en github

    git remote -v					      
-> Sirve para poder ver los remotos (origin) a las cuales se esta enlazados aún

    git remote remove origin

-> Sirve para eliminar a los los origin a los cuales se esta enlazado.



### **=== Extras: ====**
    cd Desktop/Nombre_de_carpeta                          

-> Es para ir a la ruta de la carpeta del proyecto o repositorio.
