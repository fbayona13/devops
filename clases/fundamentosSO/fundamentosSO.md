# Sistema operativo

aplicacion que se encuentra entre usuario y hardware, que le permite al usuario una mejor administracion del hardware.

## Llamada a sistema (system calls)
Si estamos en Visual Studio usando python y llamamos una libreria que usa I/O, esta libreria usa comandos de aplicacion que ejecutan llamadas al sistema operativo con POSIX (SO basados en UNIX).

    POSIX --> Es una interfaz a nivel sistema operativo que le permite al usuario hacer llamadas al sistema operativo de forma ordenada y segura. win32 para el caso de windows.

Aplicación y usuario --> modo usuario 
Sistema operativo y hardware --> modo kernel (no es admin::root)

El estandar de linux para procesos, siempre responde a esta regla cuando se crea un proceso
(para linux todo es un archivo)

            | stdin <-- tty
    proceso | stdout | pantalla
            | stderr | 

*context switching*

## SHELL (bash)
*ver wsl para powershell de windows*

terminal/consola: es una consola para ejecutar comandos de forma local o remota
interprete de comandos(SHELL): recibe todos los comandos de una terminal y lo ejecuta

Usuario
|
|
v                                       | Docker
Int. comandos (SHELL)   |   PowerShell  | WSL
|---------------------------------------| maq.virtual
| llamada al sistema    |               |
v                       |   Windows     |
Sistema Operativo       |               |
|
|
v
Hardware

## GNU/Linux

/ --> path absoluto

sudo --> mientras sea sudo soy usuario root
su --> si ya soy usuario root
cat --> para ver el contenido
etc/passwd --> cuentas de usuario
etc/shadow --> contrasenas "encriptadas"
etc/group --> diferentes grupos
/var/log.syslog --> muestra logs del sistema
/tmp/ --> es una carpeta que borra todo cuando reiniciamos la computadora
id --> nos permite ver la información de usuario
man --> el manual de cualquier comando
pwd --> indica el directory donde estoy parado
ls --> listar archivos

    ls - --> es el comando listar con modificadores
        ls -l --> listar en formato long, mas información
        ls -lh --> lo mismo que -l solo que lo traduce para el entendimiento humano 

cd --> cambia directory

    cd - --> vuelve para atras 

mkdir --> crea un nuevo directory

    mkdir -p --> permite crear todo el arbol de directory

rmdir --> borrar directory solo si esta vacio
rm --> borrar archivos o directory

    rm -r --> borrar todo del directory y todo lo que este adentro
    rm -rv --> lo mismo que r pero va mostrando que hace 
    rm -rf --> lo mismo que r pero forzado (f es forzado)

touch --> crea un archivo


## Hardlink & Softlink 

cada directory tiene un nombre y un i-nodo

    i-nodo --> es un indice que guarda toda la metadata (UID, GID, tipo de archivo, puntero a bloques de disco)

Hardlink --> seria crear un archivo con i-nodo identico a otro archivo. Esto crea una copia del archivo y toda su información. Seria crear un archivo con puntero al otro archivo.
Si borramos un archivos, el otro conserva la información.
Si modificamos la información de un archivo, el otro tambien recibe la información.

    command) ln fichero1 fichero2 --> haria un hardlink

Softlink --> seria como un acceso directo, la diferencia esta en que este si se rompe no podemos recuperar la información.

    command) ln -s fichero1 fichero2 --> haria un softlink