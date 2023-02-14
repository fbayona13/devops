## SEGURIDAD DE JENKINS

Algunas recomendaciones
- no usar admin-admin en produccion
- proteger Jenkins de internet
- establecer reglas de firewall
- poner a Jenkins atras de una VPN
- bloquear puertos para solo acceder por vpn de la empresa
- agregar una whitelist (github, gitlab, ...)
- establecer autenticaciones y autorizaciones 
- mantener Jenkins y sus plugins siempre actualizado

## INSTALACION CON DOCKER 
Lo que vemos aca es como usar docker para levantar una imagen y docker-compose para mostrarla

    1) Levantamos el servidor que vamos a utilizar
    2) Instalamos git, docker y docker-compose

        Puede aparecer un error que te deniega el acceso cuando tratas de conectar con Docker Engine.
        Se soluciona creando un grupo y agregandote como usuario:

            https://docs.docker.com/engine/install/linux-postinstall/
    
    3) Se clona el repositorio 

        para el ejercicio) https://github.com/roxsross/practica-jenkins

        3.1) En el directorio vamos a <practica-jenkins/recursos/jenkins-docker/>. Mientras exista un dockerfile y un docker-compose podemos seguir

    4) Generamos la imagen base y la construimos
    
        docker-compose up -d --build
            up --> descarga y levanta la imagen del contenedor (docker hub)
            -d --> lo hace en segundo plano 
            --build --> construye la imagen 

    5) hacemos un curl a cualquier pagina para tener nuestra ip publica 
    6) en el navegador ponemos nuestra ip publica y el puerto que estamos usando (para el caso el 8080), o podemos directamente hacer un localhost:8080
    7) Nos va a pedir una contraseña para inicializar jenkins de forma segura. La contraseña suele estar en /var/jenkins_home/secrets/initialAdminPassword

        7.1) podemos acceder a ella haciendo
            docker exec -it <image-name> bash
            cat /var/jenkins_home/secrets/initialAdminPassword

## PLUGINS RECOMENDADOS EN UNA PRIMERA ETAPA

    ssh agent
    docker 
    aws global configuration
    pipeline utilities steps
    generic webhook trigger
    multibranch scan webhook trigger

## EXTRAS

00.53.28