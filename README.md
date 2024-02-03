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
mkdir taller-git
```

Este comando crear una nueva carpeta llamada "01-hello-git". Ahora, vamos a movernos a esta carpeta con el siguiente comando:

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


