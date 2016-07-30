# Tutorial GIT (Básico)

## 1. Crear Repositorio
Para crear un repositorio lo primero que debemos tener es una cuenta en cualquier servidor GIT, hay muchos servidores, pero en este tutorial no concentraremos en GitHub, si no tienes cuenta puedes crearla completamente gratis [aquí](https://github.com/join?source=header-home).
* Lo primero que vamos a hacer es dar clic en el simbolo "+" ubicado en la parte superior derecha de la pantalla y enseguida darle clic en "New repository" como se muestra en la siguiente imagen.

![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/01.png?raw=true)
* Despues de dar clic "New Repository" nos redireccionará a la página de creación de nuevo repositorio donde deberás introducir el nombre del repositorio, una breve descripción, el tipo de acceso, el tipo de licencia y si lo deseas puedes iniciar con un archivo README.md (este ultimo es muy importante ya que en este se ingresa información importante a cerca del proyecto realizado en este repositorio).

  La siguiente imagen muestra un ejemplo de como rellenar los campos.

  Una vez rellando los campos le damos clic en el botón verde
  llamado "Create repository" que se encuentra en la parte inferior de la página.

![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/02.png?raw=true)
* Una vez que le demos clic en el botón "Create repository" la página nos redireccionará a la raíz de nuestro repositorio.

  En este apartado le vamos a dar clic en el boton verde llamado "Clone or download".

![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/03.png?raw=true)
* Se nos abrirá una pequeña ventana donde se mostrará una URL para clonar el repositorio, debemos seleccionarla y copiar el enlace.

![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/04.png?raw=true)
* Bien, ya tenemos creado nuesto repositorio, ahora es el momento de pasar a la terminal, vamos a crear un directorio en el escritorio (Puede ser en cualquier directorio del PC, solo se tendra que colocar el comando `cd` seguido de la ruta, por ejemplo: `cd Documents/Repositorios/`).

  Para crear el directorio simplemente nos posicionamos es la carpeta deseada (en este caso el escritorio) con `cd Desktop` y crearemos el nuevo directorio con el comando `mkdir nombre-del-directorio` en este ejemplo le pondremos "Repositorios".
  ![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/5.png?raw=true)

* Para comprobar si se creó el directorio simplemente escribimos el comando `ls` para ver los subdirectorios que tenemos en el directorio actual como vemos en la siguiente imagen.
![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/06.png?raw=true)

* Hemos comprobado que se creó el directorio llamado Repositorios, ahora simplemente nos dirigimos hacia allá con el comando `cd Repositorios`.
![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/07.png?raw=true)

* Ya estamos en el nuevo directorio llamado "Repositorios", ahora ha llegado el momento de clonar el Repositorio que creamos en GitHub, ¿recuerdas el enlace que copiamos? pues lo usaremos, escribimos el comando `git clone` y despues pegamos la URL que copiamos de GitHub, seria

  `git clone https://github.com/FreddyRuben/Repository-Example.git`

  Aquí tienes una imagen de ejemplo.

  ![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/08.png?raw=true)

* Ahora comprobaremos la clonación identificando el nuevo directorio que se creó dentro de "Repositorios", para eso escribimos nuevamente `ls` y podremos identificar un nuevo directorio con el nombre del repositorio.
![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/09.png?raw=true)

* Listo, hemos comprobado que el repositorio se clonó correctamente, ahora solo tendremos que movernos a ese nuevo directorio con `cd Repository-Example`, como lo muestra la siguiente imagen.
![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/10.png?raw=true)
* Hasta aquí hemos terminado con la creación del repositorio.

## 2. Flujo de trabajo de GIT
* Una vez que estemos dentro del repositorio que creamos vamos a analizar los archivos que estan dentro del directorio, para eso solo escribimos nuevamente `ls` para ver los archivos que se encuentran dentro del directorio.

  ![Sin titulo](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/11.png?raw=true)

* Como podemos observar solo hay dos archivos, "LICENSE"  y "README.md".

  Ahora procederemos a revisra las ramas (branches), para eso solo escribimos el comando
  `git branch`

  ![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/12.png?raw=true)

  si se dan cuenta nos mostró la unica rama que tenemos actualmente en nuestro repositorio llamada master, que es la rama en donde enviaremos nuestro proyecto cuando esté en una version estable (esto es muy importante ya que será el protyecto que saldrá en producción).
  Así que para trabajar crearemos una nueva rama con el comando `git branch nombre-de-la-rama`
  en este caso a nuestra rama le llamaremos "develop" por lo que el comando a escribir debe ser el siguiente:

  `git branch develop`

  y si volvemos a escribir el comando git branch notaremos que ahora hay 2 ramas, "master" y "develop" como lo muestra la siguiente imagen.

  ![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/13.png?raw=true)

* Si nos fijamos bien la rama llamada "master inicia con un " * " (asterisco), eso es porque "master" es la rama en la que estamos ubicados, y como mencionamos anteriormente, la rama "master" no debe ser tocada al menos que vayamos a lanzar nuestro proyecto oficialmente.
Entonces lo que debemos hacer es cambiarnos a la rama develop, para eso escribimos el comando:

  `git checkout develop`

  Escribimos develop ya que es el nombre de la rama a la que deseamos cambiarnos, la imagen nos muestra lo que nos deberá mostrar en pantalla despues de cambiarnos de rama.

  ![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/14.png?raw=true)

* Ahora si escribimos `git branch` nos mostrará que estamos en la rama develop, sin embargo para trabajar localmente es muy recomendable trabajar con una rama temporal que lleve un nombre que haga referencia a los cambios que se van a realizar en el proyecto, así que crearemos otra rama, en este ejmplo le pondremos "temp-branch", para lo cual escribiremos el siguiente comando:

  `git branch temp-branch`

  ahora escribimos `git branch` y nos debe mostrar las 3 ramas que tenemos creadas.

  ![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/15.png?raw=true)

* Tendremos que cambiarnos de rama como lo hicimos anteriormente, con el comando `git checkout nombre-de-la-rama`, entonces ejecutamos el siguiente comando.

  `git checkout temp-branch`

  y con esto ya habremos cambiado a la rama "temp-branch" y es aquí en donde trabajaremos de manera local.
  Ahora para que GIT de seguimiento de nuestro proyecto vamos a proceder a modificar el archivo "README.md" que es el que se creó por defecto en nuestro repositorio, solo agregaremos una descripción de lo que trata el proyecto, guardamos y cerramos.

  Si escribimos el comando `git status` nos mostrará algo como esto.

      ➜  Repository-Example git:(temp-branch) git status
      On branch temp-branch
      Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      ( use "git checkout -- <file>..." to discard changes in working directory)

      modified:   README.md

      no changes added to commit (use "git add" and/or "git commit -a")

* Lo que GIT nos dice es que es que hay archivos que fueron modificados y que necesitan ser agregados para que se le pueda dar seguimiento, y poderle hacer commit, para lo cual escribimos `git add nombre-del-archivo`, en nuestro caso sería de la siguiente manera:

  `git add README.md`

  Ahora escribiremos `git status` para comprobar que el archivo ya está en seguimiento y listo para hacer commit, nos debe mostrar algo como esto.

        ➜  Repository-Example git:(temp-branch) ✗ git status
        On branch temp-branch
        Changes to be committed:
        (use "git reset HEAD <file>..." to unstage)

        modified:   README.md

* A continuación escribiremos en consola `git commit -v nombre-del-archivo` para que nos abra una ventana de texto donde debemos escribir una breve descripción de los cambios que se le hicieron al proyecto.

  `➜  Repository-Example git:(temp-branch) ✗ git commit -v
[develop 7adc3ef] commit de prueba
1 file changed, 2 insertions(+)`

* Ahora solo tenemos que hacerle push al repositorio y lo hacemos de la siguiente manera:

  `git push origin temp-branch`

  y si todo salió bien nos saldrá algo como esto:

      ➜  Repository-Example git:(temp-branch) git push origin temp-branch
      Counting objects: 4, done.
      Delta compression using up to 4 threads.
      Compressing objects: 100% (4/4), done.
      Writing objects: 100% (4/4), 482 bytes | 0 bytes/s, done.
      Total 4 (delta 0), reused 0 (delta 0)
      To https://github.com/FreddyRuben/Repository-Example.git
      *   [new branch]      temp-branch -> temp-branch

## 3. Volviendo a GitHub

* Si llegamos a este punto es porque ya tenemos todo listo para para enviar los cambios a la rama develop, lo que tenemos que hacer ahora es ingresar a la pagina de GitHub nuevamente, ¿Recuerdas como? si no es así te recuerdo, es ingresar a [www.github.com](www.github.com) e ingresamos a nuestro repositorio (si no has ingresado con tu cuenta hazlo, ya que de lo contrario no podrás continuar), y en nuestro repositorio le damos clic en el enlace que dice "branches", si no lo ubicas aqui tienes una imagen.

![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/16.png?raw=true)

* Bien, una vez dentro de "branches" vamos a identificar la rama "temp-branch" y vamos a darle clic en el boton "New pull request" como se muestra a continuación.

![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/17.png?raw=true)

* Ahora nos muestra una pagina donde tenemos que ser muy cuidadoso, ya que en base debe quedar como develop (no master). Y en compare debe quuedar "temp-branch", si bajamos la ventana podremos visualizar los cambios efectuados como se muestra en la siguiente imagen.

![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/19.png?raw=true)

* Bien ahora tendremos que darle clic en el boton verde llamado "Create pull request" y listo, habremos hecho el merge correctamente a develop.

* Hecho todo lo anterior habremos terminado, sin embargo no es necesario tener la branch "temp-branch" así que procederemos a eliminar esa branch.

para ello solo nos volvemos a dirigir a "branches" y le damos en el el cesto de basura correspondiente a "temp-branch" como se muestra en la siguiente imagen.

![](https://github.com/FreddyRuben/Tatooine-HDH/blob/develop/SPRINT-2/02-GIT/image/21.png?raw=true)

* Listo, ahora sabes lo básico de GIT.
