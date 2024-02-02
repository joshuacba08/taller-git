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

