## DOCKER
Docker es un software que permite desplegar aplicaciones en entornos aislados e independientes del hardware en que corren. 

    Abstraccion --> cuando hablamos de Docker estamos virtualizando aplicaciones no maquinas, los SO no nos interesan. Si mi infraestructura corre en una maquina, va a correr en cloud. 

    Automatizacion --> si tengo un sistema de deploy automatizado, si lo deployo en el ambiente de testing, va a funcionar en produccion (es muy raro que no funcione) 

    Imagen --> Es como un objeto de solo lectura, no se puede modificar. Un plano arquitectonico de la aplicacion.
    Contenedor --> Es una instancia de la Imagen.


Las consecuencias de usar Docker:

    portabilidad --> lo voy a poder desplegar en cualquier lado.

    ligereza --> solamente tenemos lo necesario para correr la aplicacion.

    autosuficiencia --> no contiene todo un sistema, sino aquellas librerias, archivos y configuraciones necesarias para desplegar las funcionalidades del servicio que contenga.

## DOCKER ENGINE
DockerEngine 
|
|
v
namespace (pid)
namespace(network)
namespace(disco)
Kernel

## DOCKER CLI
Docker CLI:

    i docker run mi-aplicacion --> el CLI de docker es simplemente docker. De esta forma mi-aplicacion se conecta con la API de docker engine.
        
        docker container run -d --name spaghettidocker -p 80:80 davidpigna/spaghettidocker
            docker container run --> le decimos a Daemon que ejecute el contenedor 
            -d / --detached --> ejecuta el contenedor en segundo plano
            --name --> le damos el nombre al contenedor, por default le asigna un nombre aleatorio
            -p / --publish --> mapea los puertos del host al puerto del contenedor
            davidpigna/spaghettidocker --> es la direccion en la que se encuentra este contenedor 

## DOCKER HUB
Es muy parecido a github, mientras en github esta el repositorio de la aplicacion, en docker hub esta la imagen de la aplicacion.
Los tags en github y docker hub muestran los releases de las aplicaciones, muchas veces coinciden las versiones por paralelismo.

## DOCKER COMMANDS
    docker --version --> ver la version de docker 
    docker help --> la ayuda de docker 
        docker login --help --> la ayuda del verbo login
    docker login -u --> el usuario de docker 
    docker pull --> lo mismo que para github
    docker run --> levanta la libreria
        docker run -d --> detached desconecta el proceso, ejecuta el container en segundo plano
        docker run -p --> mapea los puertos del host al puerto del container
    docker ps --> muestra los containers 
        docker ps -a --> muestra todos los containers
    docker stop <nombre> --> para el contenedor
    docker start <nombre> --> arranca el contenedor
    docker rmi <tag> --> borra la imagen
    docker rm <nombre/id> --> borra el container
    docker image prune --> borra todas las imagenes
    docker container prune --> borra todos los contenedores
    docker system prune --> borra todo
        docker system prune -a --> borra todo lo que no tenga un container asociado
    
01.38.14

## Extras
Los 3 tipos de virtualizacion

    full virtualization --> hipervisor (maquina guest) simula enteramente a una computadora.

    virtualization --> en linux DocSend

    paravirtualization --> tanto maquina virtual, como el SO y las otras virtual machines funcionan todo al mismo nivel. Solaris