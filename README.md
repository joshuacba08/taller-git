![portada](https://res.cloudinary.com/dnge4qorr/image/upload/v1707116606/academy/taller-git-portada_qaebzg.png)

# Taller de GIT

## Profesor:

- [Josue Oroya](https://github.com/joshuacba08)

## Objetivos:

- Entender el concepto de control de versiones
- Conocer y manipular los comandos básicos de GIT en la terminal
- Aprender a trabajar de forma colaborativa en un proyecto.
- Usar un repositorio remoto para almacenar el código de un proyecto.

## Contenido:

1. Git y la línea de comandos
2. Repositorios locales

## Git y la línea de comandos

### ¿Qué es Git?

Git es un sistema de control de versiones distribuido, gratuito y de código abierto diseñado para manejar todo, desde proyectos pequeños hasta muy grandes, con velocidad y eficiencia. Para entender mejor que es un sistema de control de versiones, es necesario ver un poco de historia.

Hasta hace unos años, cuando se trabajaba en un proyecto de software, se guardaba el código en una carpeta y se iban creando copias de esta carpeta a medida que se iban haciendo cambios. Esto funcionaba bien para proyectos pequeños, pero cuando se trataba de proyectos grandes, se volvía un problema. Obviamente la situación se tornaba más caótica cuando se trabajaba en equipo, ya que cada miembro del equipo tenía su propia copia del proyecto y cuando se quería integrar los cambios de cada uno, se volvía un problema.

Es ahí cuando nacen los sistemas de control de versiones, que son herramientas que permiten llevar un registro de los cambios realizados sobre un archivo o conjunto de archivos a lo largo del tiempo, de tal manera que sea posible recuperar versiones específicas más adelante. Además, permiten trabajar en equipo de forma colaborativa, ya que permiten integrar los cambios de cada miembro del equipo.

### Instalación de Git

Para instalar Git, es necesario ir a la página oficial de [Git](https://git-scm.com/) y descargar el instalador correspondiente a tu sistema operativo. Una vez descargado, se debe seguir el proceso de instalación.

Podremos comprobar que la instalación fue exitosa si vemos disponible Git Bash entre nuestros programas recien instalados o si ejecutamos el siguiente comando en la terminal:

```bash
git --version
```

### La terminal de comandos

Antes de continuar aprendiendo Git, es necesario entender un poco sobre la terminal de comandos. La terminal de comandos es una interfaz de texto que permite interactuar con el sistema operativo mediante comandos. En el caso de Windows, la terminal de comandos es el programa llamado "Símbolo del sistema" o "cmd". En el caso de Mac o Linux, la terminal de comandos es el programa llamado "Terminal".

Como recomendación, si somos usuarios de Windows y queremos trabajar con Git, es recomendable usar Git Bash, ya que es una terminal de comandos que viene incluida con la instalación de Git y que nos permite trabajar con comandos de Linux. Aunque si vas a ser un desarrollador con Windows, no hay nada más potente que PowerShell.

### Comandos básicos de la terminal

Vamos a abrir la terminal de comandos que quieras usar, dependiendo si estás en Windows, Mac o Linux. A continuación, vamos a ver algunos comandos básicos que nos permitirán movernos por el sistema de archivos y realizar algunas operaciones básicas.

- `pwd`: Nos permite ver el directorio en el que nos encontramos.
- `ls`: Nos permite ver el contenido del directorio en el que nos encontramos.
- `cd`: Nos permite cambiar de directorio.
- `mkdir`: Nos permite crear un directorio.
- `touch`: Nos permite crear un archivo.
- `rm`: Nos permite eliminar un archivo.
- `rmdir`: Nos permite eliminar un directorio.
- `mv`: Nos permite mover un archivo o directorio.
- `cp`: Nos permite copiar un archivo o directorio.
- `clear`: Nos permite limpiar la terminal.
- `cat`: Nos permite ver el contenido de un archivo.
- `echo`: Nos permite escribir en un archivo.
- `man`: Nos permite ver el manual de un comando.
- `exit`: Nos permite salir de la terminal.
- `history`: Nos permite ver el historial de comandos.

A medida que vayamos avanzando en el taller, iremos viendo los usos y utilidades de cada uno de estos comandos con ejemplos prácticos.

### Configuración de Git

Antes de empezar a trabajar con Git, es necesario configurar nuestro nombre de usuario y correo electrónico. Esto es necesario para que Git pueda identificar quién es el autor de los cambios que se hagan en el proyecto. Para configurar nuestro nombre de usuario y correo electrónico, debemos ejecutar los siguientes comandos en la terminal:

```bash
git config --global user.name "Tu nombre"
git config --global user.email "email@email.com"
```

De esta forma, cada acción que realicemos en el repositorio, quedará registrada con nuestro nombre y correo electrónico.

## Repositorios locales

Los repositorios locales son aquellos que se encuentran en nuestra máquina. En estos repositorios es donde se trabaja en el código de un proyecto. A continuación, vamos a ver cómo podemos crear un repositorio local, cómo podemos hacer cambios en el código y cómo podemos guardar estos cambios en el repositorio.

### Crear un repositorio local

Para crear un repositorio local, es necesario ir a una ubicación en la que querramos guardar nuestro proyecto. Antes que nada, vamos a crear una nueva carpeta en la que guardaremos nuestro proyecto. Para ello, vamos a abrir la terminal de comandos y vamos a ejecutar el siguiente comando:

```bash
mkdir 01-hello-git
```

Este comando creará una nueva carpeta llamada "01-hello-git". Ahora, vamos a movernos a esta carpeta con el siguiente comando:

```bash
cd 01-hello-git
```

Una vez que estemos en la carpeta, vamos a inicializar un repositorio de Git con el siguiente comando:

```bash
git init
```

Este comando inicializa un repositorio de Git en la carpeta en la que nos encontramos. Ahora, si ejecutamos el comando `ls`, veremos que se ha creado una carpeta oculta llamada ".git". Esta carpeta es la que contiene toda la información del repositorio. Además, veremos que la terminal nos mostrará el nombre de la rama en la que nos encontramos, que por defecto es "master". Esto se debe a que una inicialización de Git crea una rama por defecto llamada "master", de allí crearemos nuevas ramas para trabajar en nuestro proyecto.

**Nota:** Si queremos ver los archivos ocultos en la terminal, podemos ejecutar el comando `ls -a`. También podemos ver los archivos ocultos en el explorador de archivos si habilitamos la opción de "Mostrar archivos ocultos".

### Hacer cambios en el código

Ahora que ya tenemos un repositorio local, vamos a hacer cambios en el código. Para ello, vamos a crear un archivo llamado "README.md" en la carpeta del proyecto. Para crear este archivo, vamos a ejecutar el siguiente comando:

```bash
touch README.md
```

Los archivos con extensión ".md" son archivos de texto que se utilizan para escribir documentación. En este caso, vamos a utilizar el archivo "README.md" para escribir la documentación del proyecto. Una vez que hayamos creado el archivo, vamos a abrirlo con un editor de texto, en  este caso VSCode.

Podemos abrir todo el contenido de la carpeta `01-hello-git` en VSCode con el siguiente comando:

```bash
code .
```

Una vez que hayamos abierto el archivo "README.md", vamos a escribir el siguiente contenido:

```markdown
# Taller de GIT

## Profesor:
- [Josue Oroya](https://github.com/joshuacba08)

## Alumno:
- [Tu nombre](Link a tu perfil de GitHub)
```

Una vez que hayamos escrito el contenido, vamos a guardar el archivo y vamos a cerrar el editor de texto. Ahora que hemos hecho cambios en el código, vamos a ver cómo podemos guardar estos cambios en el repositorio.

### Guardar cambios en el repositorio

Para guardar los cambios en el repositorio, es necesario seguir los siguientes pasos:

1. Añadir los archivos al área de preparación.
2. Hacer un commit con los cambios.
3. Ver el historial de commits.
4. Ver el estado del repositorio.

#### Añadir los archivos al área de preparación

El área de preparación es un espacio en el que se guardan los cambios que se quieren guardar en el repositorio. Para añadir los archivos al área de preparación, es necesario ejecutar el siguiente comando:

```bash
git add README.md
```

Este comando añade el archivo "README.md" al área de preparación. Si queremos añadir todos los archivos al área de preparación, podemos ejecutar el siguiente comando:

```bash
git add .
```

#### Hacer un commit con los cambios

Un commit es una operación que guarda los cambios que se han hecho en el repositorio. Para hacer un commit con los cambios, es necesario ejecutar el siguiente comando:

```bash
git commit -m "Añadir archivo README.md"
```

Este comando hace un commit con los cambios que se han añadido al área de preparación. El mensaje que se añade con la opción `-m` es un mensaje que describe los cambios que se han hecho en el commit. Es importante que este mensaje sea descriptivo, ya que nos permitirá saber qué cambios se han hecho en el proyecto.

A continuación, veremos un diagrama que muestra cómo se guardan los cambios en un repositorio de Git.

![r/git - Git workflow diagram showcasing the role of remote-tracking refs (origin/*)](https://preview.redd.it/nm1w0gnf2zh11.png?width=960&crop=smart&auto=webp&s=7614ee78c39285ee1d157c97ebb545430c030cb0)

#### Ver el historial de commits

El historial de commits es una lista de todos los commits que se han hecho en el repositorio. Para ver el historial de commits, es necesario ejecutar el siguiente comando:

```bash
git log
```

Este comando muestra una lista de todos los commits que se han hecho en el repositorio. Cada commit tiene un identificador único, un autor, una fecha y un mensaje que describe los cambios que se han hecho en el commit.

#### Ver el estado del repositorio

El estado del repositorio es una lista de los archivos que se han modificado, añadido o eliminado en el repositorio. Para ver el estado del repositorio, es necesario ejecutar el siguiente comando:

```bash
git status
```

Este comando muestra una lista de los archivos que se han modificado, añadido o eliminado en el repositorio. Además, muestra si los archivos han sido añadidos al área de preparación o no.

### Resumen

En este capítulo, hemos aprendido qué es Git, cómo instalarlo, cómo usar la terminal de comandos, cómo configurar Git, cómo crear un repositorio local, cómo hacer cambios en el código y cómo guardar estos cambios en el repositorio. En el próximo capítulo, veremos cómo podemos trabajar de forma colaborativa en un proyecto y cómo podemos usar un repositorio remoto para almacenar el código de un proyecto.

### Ejercicios

1. Crear un repositorio local en una carpeta llamada "01-hello-git".
2. Crear un archivo llamado "README.md" con el siguiente contenido:

```markdown
# Taller de GIT

## Profesor:

- [Josue Oroya](https://github.com/joshuacba08)

## Alumno:

- [Tu nombre](Link a tu perfil de GitHub)
```

3. Añadir el archivo "README.md" al área de preparación.
4. Hacer un commit con los cambios.
5. Ver el historial de commits.

## Branches (Ramas)

Para trabajar con Git es necesario imaginarse un árbol, donde la rama principal es la rama `master` y de ella se desprenden otras ramas que son las que contienen los cambios que se van a hacer en el proyecto. Posteriormente, estas ramas se pueden integrar a la rama `master` para que los cambios se vean reflejados en el proyecto.

Un ejemplo muy común de uso de ramas es cuando se quiere trabajar en una nueva funcionalidad del proyecto. En este caso, se crea una nueva rama a partir de la rama `master` y se hacen los cambios necesarios en la nueva rama. Una vez que los cambios estén listos, se integran a la rama `master` y se eliminan la rama que se creó.

En mi experiencia en la industria, he aplicado una modalidad de trabajo llamada `Git Flow` que es una forma de trabajar con ramas en Git. En esta modalidad, se crean dos ramas principales: `master` y `develop`. La rama `master` contiene el código que se encuentra en producción y la rama `develop` contiene el código que se encuentra en desarrollo. A partir de la rama `develop` se crean nuevas ramas para trabajar en nuevas funcionalidades del proyecto. Una vez que los cambios estén listos, se integran a la rama `develop` y posteriormente a la rama `master`.

![Flujo de trabajo de Git: ramas de función](https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=1427)

Como se puede apreciar en este gráfico, el flujo de trabajo de Git con ramas es muy flexible y permite trabajar de forma colaborativa en un proyecto.

**Rama Main (Master)**: Es la rama principal del proyecto. Contiene el código que se encuentra en producción.

**Rama Develop**: Es la rama que contiene el código que se encuentra en desarrollo. A partir de esta rama se crean nuevas ramas para trabajar en nuevas funcionalidades del proyecto.

**Features**: Son las ramas que se crean a partir de la rama `develop` para trabajar en nuevas funcionalidades del proyecto. Se integran a la rama `develop` una vez que los cambios estén listos.

En un grupo de trabajo, cada miembro puede crear una rama a partir de la rama `develop` para trabajar en una nueva funcionalidad del proyecto. Una vez que los cambios estén listos, se integran a la rama `develop` y posteriormente a la rama `master`. Veremos esta dinámica más adelante en el taller.

### Crear una nueva rama

Para crear una nueva rama en Git, es necesario ejecutar el siguiente comando:

```bash
git branch nombre-de-la-rama
```

Este comando crea una nueva rama con el nombre que le indiquemos. Una vez que hayamos creado la rama, podemos ver una lista de todas las ramas que se han creado en el repositorio con el siguiente comando:

```bash
git branch
```

Este comando muestra una lista de todas las ramas que se han creado en el repositorio. La rama que se encuentra resaltada es la rama en la que nos encontramos. Para cambiar de rama, es necesario ejecutar el siguiente comando:

```bash
git checkout nombre-de-la-rama
```

Este comando cambia de rama a la rama que le indiquemos. Una vez que hayamos cambiado de rama, podemos hacer cambios en el código y guardarlos en la rama. A continuación, veremos un ejemplo de cómo crear una nueva rama y cómo cambiar de rama.

### Ejemplo

Vamos a crear una nueva rama llamada "feature-readme" y vamos a cambiar a esta rama. Para ello, vamos a ejecutar los siguientes comandos:

```bash
git branch feature-readme
git checkout feature-readme
```

Una vez que hayamos cambiado a la rama "feature-readme", vamos a hacer cambios en el archivo "README.md". Vamos a añadir nuestro nombre a la lista de alumnos. Una vez que hayamos hecho los cambios, vamos a guardarlos en la rama "feature-readme". A continuación, veremos cómo hacer esto.

### Hacer cambios en la rama

Una vez que hayamos cambiado a la rama en la que queremos trabajar, podemos hacer cambios en el código y guardarlos en la rama. Para hacer cambios en el código, es necesario seguir los siguientes pasos:

1. Hacer cambios en el código.
2. Añadir los archivos al área de preparación.
3. Hacer un commit con los cambios.
4. Ver el estado del repositorio.

Todos estos pasos están explicados en el capítulo anterior, por lo que no los vamos a explicar de nuevo. Sin embargo, es importante recordar que cada rama tiene su propio historial de commits, por lo que los cambios que se hagan en una rama no afectan a las demás ramas.

### Resumen

En este capítulo, hemos aprendido qué son las ramas en Git, cómo crear una nueva rama, cómo cambiar de rama y cómo hacer cambios en la rama. En el próximo capítulo, veremos como unir ramas y resolver conflictos.

### Ejercicios

1. Crear una nueva rama llamada "feature-readme".
2. Cambiar a la rama "feature-readme".
3. Hacer cambios en el archivo "README.md".
4. Añadir los cambios al área de preparación.
5. Hacer un commit con los cambios.
6. Ver el historial de commits.
7. Ver el estado del repositorio.

## Unir ramas y resolver conflictos (Merge)

Una vez que se han hecho cambios en una rama y se quieren integrar a otra rama, es necesario unir las ramas. Este proceso se llama "merge" y consiste en integrar los cambios de una rama a otra rama. En este proceso, es posible que se presenten conflictos, que son situaciones en las que dos ramas han hecho cambios en las mismas líneas de código. En este caso, es necesario resolver los conflictos para poder unir las ramas.

### Unir ramas

Supongamos que hemos terminado todo lo que queríamos hacer en nuestra rama `feature-readme` y queremos integrar los cambios a la rama `master`. Para hacer esto, es necesario seguir los siguientes pasos:

1. Cambiar a la rama a la que queremos integrar los cambios.
2. Unir la rama con los cambios.
3. Ver el historial de commits.
4. Ver el estado del repositorio.
5. Resolver conflictos (si es necesario).
6. Hacer un commit con los cambios.

**Nota:** En este caso, vamos a unir la rama `feature-readme` a la rama `master`. Sin embargo, en la metodología `Git Flow` se uniría a la rama `develop` y posteriormente a la rama `master`. En este caso, vamos a unir la rama `feature-readme` a la rama `master` para simplificar el proceso.

### Ejemplo

Vamos a unir la rama `feature-readme` a la rama `master`. Para ello, vamos a cambiar a la rama `master` y vamos a unir la rama `feature-readme` a la rama `master`. A continuación, veremos cómo hacer esto.

### Cambiar a la rama a la que queremos integrar los cambios

Para cambiar a la rama a la que queremos integrar los cambios, es necesario ejecutar el siguiente comando:

```bash
git checkout master
```

Este comando cambia a la rama `master`. Una vez que hayamos cambiado a la rama `master`, podemos unir la rama `feature-readme` a la rama `master`. A continuación, veremos cómo hacer esto.

### Unir la rama con los cambios

Para unir la rama `feature-readme` a la rama `master`, es necesario ejecutar el siguiente comando:

```bash
git merge feature-readme
```

Este comando une la rama `feature-readme` a la rama `master`. Si no hay conflictos, los cambios se integrarán a la rama `master` y se mostrará un mensaje que indica que la unión se ha hecho correctamente. Si hay conflictos, se mostrará un mensaje que indica que hay conflictos y será necesario resolverlos para poder unir las ramas.

### Ver el historial de commits

Una vez que hayamos unido la rama `feature-readme` a la rama `master`, podemos ver el historial de commits con el siguiente comando:

```bash
git log
```

Este comando muestra una lista de todos los commits que se han hecho en el repositorio. Si la unión se ha hecho correctamente, veremos que los commits de la rama `feature-readme` se han integrado a la rama `master`. A continuación, veremos cómo ver el estado del repositorio.

### Ver el estado del repositorio

Una vez que hayamos unido la rama `feature-readme` a la rama `master`, podemos ver el estado del repositorio con el siguiente comando:

```bash
git status
```

Este comando muestra una lista de los archivos que se han modificado, añadido o eliminado en el repositorio. Si la unión se ha hecho correctamente, veremos que no hay archivos pendientes de añadir al área de preparación ni de hacer un commit. A continuación, veremos cómo resolver conflictos.

### Resolver conflictos

Si hay conflictos al unir las ramas, es necesario resolverlos para poder unir las ramas. Para resolver conflictos, es necesario tener en cuenta que los conflictos están marcados en el código con la siguiente estructura:

```markdown
<<<<<<< HEAD
Código de la rama actual
=======
Código de la rama que se quiere unir
>>>>>>> nombre-de-la-rama
```

Un conflicto sucede cuando dos ramas han modificado la misma línea de código. En este caso, es necesario decidir qué cambios se quieren conservar y cuáles se quieren eliminar. Una vez que hayamos resuelto los conflictos, es necesario añadir los archivos al área de preparación y hacer un commit con los cambios.

Si me paro en la rama `master` y hago un `merge` con la rama `feature-readme`, los cambios entrantes o tambien llamados `incoming changes` son los cambios que se encuentran en la rama `feature-readme` y los cambios salientes o también llamados `current changes` son los cambios que se encuentran en la rama `master`.

**Nota:** Es necesario resolver los conflictos que se puedan producir al unir las ramas. Si no se resuelven los conflictos, no se podrán unir las ramas.

### Resumen

En este capítulo, hemos aprendido cómo unir ramas en Git, cómo cambiar de rama, cómo ver el historial de commits, cómo ver el estado del repositorio y cómo resolver conflictos. En el próximo capítulo, veremos cómo trabajar de forma colaborativa en un proyecto y cómo usar un repositorio remoto para almacenar el código de un proyecto.

### Ejercicios

1. Cambiar a la rama "master".
2. Unir la rama "feature-readme" a la rama "master".
3. Ver el historial de commits.
4. Ver el estado del repositorio.
5. Resolver conflictos (si es necesario).
6. Hacer un commit con los cambios.
7. Ver el historial de commits.
8. Ver el estado del repositorio.

## Repositorios remotos

Los repositorios remotos son aquellos que se encuentran en un servidor remoto. En estos repositorios es donde se almacena el código de un proyecto y se trabaja de forma colaborativa. Existen muchos servicios que ofrecen repositorios remotos, como GitHub, GitLab, Bitbucket, entre otros. De acuerdo a mi experiencia, he trabajado con estos tres servicios y me han parecido muy buenos, sin embargo abordaremos el uso de GitHub debido a que hoy en día es el más popular y el que más se utiliza en la industria.

### Crear un repositorio remoto

Para crear un repositorio remoto en GitHub, es necesario seguir los siguientes pasos:

1. Crear una cuenta en GitHub.
2. Crear un nuevo repositorio.
3. Usar la bateria de comandos que GitHub nos proporciona para subir nuestro repositorio local a GitHub.
