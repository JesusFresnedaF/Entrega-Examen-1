# Examen Entornos de desarrollos GIT

## Parte A: Repetir la tarea 1

El primer paso es inicializar el repositorio de la tarea con el comando:

~~~
git init
~~~

![](init.png)

Después, pasamos el repositorio a la fase de "index" con el comando:


~~~
git add .
~~~

O

~~~
git add fichero.archivo
~~~

![](add.png)

A continuación, para poner nuestro repositorio en la fase de "local repository" debemos ejecutar el comando commit:

~~~
git commit -m "commit"
~~~
![](commit.png)

En este momento, nuestro repositorio está en fase de "local repository".

Finalmente, para pasar de local repository a remote repository:

~~~
git branch -M main
git remote add origin "enlace repositorio github"
~~~

![](origin-main.png)

~~~
git push -u origin main
~~~

![](push.png)

Y con éstos pasos conseguimos subir un repositorio a Github desde Git Bash.

## Parte B: Repetir la tarea 2

Para revisar los commits realizados, utilizaremos los siguientes comandos.

Primero, comprobemos los distintos commits que tenemos en este repositorio: 

~~~
git log --oneline --all
~~~

![](oneline.png)

Esos son los commits que tiene nuestro repositorio actualmente. Para comprobar que hay en cada uno:

~~~
git checkout *cabecera
~~~

Por ejemplo, en el commit "segundo commit":

![](checkout1.png)

En el commit "primer commit":

![](checkout2.png)

~~~
git checkout main
~~~

![](checkoutactual.png)

Y de esta forma podemos navegar entre los distintos commits de nuestro repositorio y ver los datos que había en esos instantes.

## Parte C: Áreas de un repositorio Git:

1. Directorio de un trabajo (Working directory):
   El directorio de un trabajo es la carpeta donde estamos trabajando y queremos crear el repositorio para subirlo a Github.
 
2. Área de preparación (Staging area):
   
3. Repositorio local (Directorio .git):
   Repositorio local es la fase en la que tenemos nuestro repositorio creado y comentado, pero aún no está listo para pasarlo a repositorio remoto (Github). Para entrar en esta fase, previamente tenemos que haber ejecutado los comandos: "add" y "commit".