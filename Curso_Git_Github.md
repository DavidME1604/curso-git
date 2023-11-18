# Curso de Git y GitHub

Git es independiente de GitHUb, pero GitHub si depende de Git

---

## Que es git?

Git es un sistema de control de versiones distribuido.
Nos ayuda a llevar los historiales de nuestros proyecto. Existe una linea de tiempo en la que podemos incluso volver a versiones anteriores de nuestros proyectos.

## Conceptos de git

---
Primero debemos incializar y crear repositorio, esto se logra con git init.

* Ramas: Es una version independiente de tu codigo, puedes crear una rama para modificar la estructura de tu codigo y asi no afectar al original.
* Untracked: Sabe que existe, pero git no los tiene guardados.
* Ingnorar ficheros: Sirve para que en el status deje de mostrarme ficheros que no queremos tener en cuenta.

## Comandos principales para bash

* **ls**: Listar los ficheros
* **cd**: Mover entre directorios
* **pwd**: Directorio actual
* **mkdir**: Crear carpeta

---

## Comandos de configuracion de Git

* **git config --global user.name "nombreUsuario"**: Afecta de forma global al git con tu nombre de usuario.
* **git config --global user.email "email"**: Configurar el email de forma global

---

## Comandos Git

* **git init**: Le decimos a git que vamos a incializar y crear un repositorio en la carpeta en la que me encuentro

* **git status**: Te muestra como estan tus ficheros en la rama.

* **git add**: Nos ayuda a agregar los ficheros a git, pero eso no quiere decir que ya le hayamos hecho nuestra primera fotografia.

* **git commit -m**: Para lanzar la fotografia del fichero, el -m es para asignarle un nombre al commit, no se puede mandar commit sin un nombre

* **git log**: Para saber que se ha hecho

* **git checkout**: Para volver a puntos anteriores (cuando hemos hecho commits) de nuestros ficheros

* **git reset (--soft --mixed --hard)**: Para ver que se hace con los cambios, con soft descarto los cambios pero no los elimino, con mixed decarto los cambios, los elimino pero se pueden recuperar, con hard decarto y elimino los cambios definitivamente.

* **git config --global alias.nombreDelNuevoComando "el comando que va a ejecutar" (git config --global alias.tree " log --graph --decorate --all --oneline")**: Esto nos ayuda a resumir comados con paralabras como en este caso tree y no tener que aprendernos comandos largos

* **git diff**: Nos dice que cambios ha hecho en que ficheros. Tambien sirve para comparar ramas.

* **git checkout (y el hash del commit)**: Nos ayuda a movernos en la rama y a volver a los commits anteriores para volver a versiones anteriores.

* **git checkout head**: esto le indica que ahora nuestro head es el commit en el que nos encontramos.

* **git reset --hard hashCommit**: Si la fregue en el codigo y quiero regresarme a un commit y borrar los anteriores commits, pero ojo si nos equivoco y quiero volver al commit pues hago otra vez el mismo comando y va para adelante.

* **git reflog**: Es el hisotrial de todo, si hacemos un reset --hard, pues ahi sigue el hash de nuestro ultimo commit, no se borra.

* **git tag**: Anadimos como vinetas que marcan puntos importantes de nuestra rama. Generalmente por convension se pone todo en minusculas y espacios con _.

* **git checkout tags/nombreTag**: Me mueve al commit que tenga el nombre del tag

Hasta aqui se ha trabajado con una rama

---
Creando ramas

* **git branch nombreRama**: Crea nuevas ramas
* **git switch**: Cambia entre ramas.

![Flujo de git con dos ramas](img/Screenshot%202023-11-18%20095449.png)

* **git merge**: Fusiona ramas.

![Flujo de git con dos ramas](img/Screenshot%202023-11-18%20100458.png)

* **git stash**: Cuando me quiero cmabiar de rama, pero estaba desarrollando y no quiero hacer commit porque no he acabado, pero tambpoco quiero perder el avance

* **git stash list**: muestra si tenemos un cambio guardado en local pero pendiente de commit

* **git stash pop**: Recupera lo del stash

* **git stash drop**: Borra lo que este en el stash
* **git branch -d**: Acabo de desarrollar la future, mergeo las ramas y ahi si utilizo esto para eliminar la rama.

Hasta ahora Git no ayudado hacer versiones de forma local

---

## GitHub

## Que es?

Es una plataforma que corre por debajo Git, pero funciona de forma remota y me hace posible ver las versiones que hecho de mi codigo.
