  ![](https://git-scm.com/images/logo@2x.png)
# Curso de GIT

Este es un curso de GIT y la correcta utilización de sus comandos además de la creación del **README.md**.

## Comandos de Git 

    git config --global user.name "Jose Leonardo Valenzuela"
    git config --global user.email "leonvalen@gmail.com"
    git config --list

### Para inicializar un repositorio en una carpeta o proyecto 
    git init

> En este momento nuestro proyecto se encuentra en el status **Working   
> Directory**

Para pasarlo al proximo estado (**stage state**) debemos ejecutar

    git add .
  
 También podemos utilizar 

    git add archivo.ext
	git add -all

 Para saber el estatus de nuestros archivos o saber en que estado se ecuentra nuestro proyectos se ejecuta el siguiente comando:

    git status

Ahora debemos pasar del estado 2 (stage) a **commited**

    git commit -m "Creacion del archivo README.md"

Podemos hacer modificaciones a nuestros archivos y de nuevo ejecutar 

    git add .

De nuevo tendremos que hacer un commit

    git commit -m "modificacion de README.md"

Si queremos ver el estado de los commits debemos ejecutar 

    git log
se veria algo parecido a esto:

commit dfe02f37ae309e9590340bee39df647b2c61c358 (HEAD -> master)
Author: Jose Leonardo Valenzuela <leonvalen@gmail.com>
Date:   Tue Mar 10 23:36:48 2020 -0300

    modificacion de README.md

commit b17f89a6cb9c9af1fa9d9b9de7bf90974de90609
Author: Jose Leonardo Valenzuela <leonvalen@gmail.com>
Date:   Tue Mar 10 23:33:42 2020 -0300

    Creaci<C3><B3>n del archivo README.md

### Conectarse a github.com 

> Se necesita tener una cuenta cread en github.com y creamos un repositorio, para este curso crearemos CursoGit

ya hemos ejecutado varios comandos git, por lo que solo debemos ejecutar

    git remote add origin https://github.com/leonvalen/CursoGit.git

Para poder ver los estados fetch y push podemos ejecutar:

    git remote -v

y para poder hacer nuestro primer push ejecutamos 

    git push origin master 

En caso de que nos pida las credenciales de GitHub Login (usename y password y lo cerramos, y escribimos nuestro usuario y contraseña por la consola.

## Buscar cambios en nuestro repositorio

Si trabajamos con varias personas en nuestro proyecto debemos buscar esos supuestos cambios en nuestro repositorio. Esto se hace con el comando 
En nuestro caso como estamos haciendo pruebas solos, vamos a ahcer algo que no es aconsejable y es realizar cambios directamente en el servidor seleccionando nuestro archivo README.md y editandolo colocamos algún cambio, luego colocamos un **Commit changes** y le damos al botón Commit changes. De esta manera tendremos un cambio que obtener de nuestro servidor.

Ahora desde nuestra carpeta de proyecto para poder obtener lso cambios ejecutamos el siguiente comando:

    git pull origin master

prueba de camnio en servidor y bajarlo a local
