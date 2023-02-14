- maven
- integracion con sonarqube
    veracode pipeline --> alternativa a sonarqube
- generacion de imagenes - commit 
- docker history . dive - modelado de imagen 
    dive --> es un software que hace ingenieria inversa sobre la imagen de docker para ver como esta construido 


## LABORATORIOS PRACTICO EN KILLERCODA
- https://killercoda.com/tercermundo/scenario/jenkins-principiante

Creamos una imagen de Jenkins pero sin el wizzard. Aprovechando que esto es bastante rapido.

    docker build -t qqjenkins .

y una vez que la tenemos, lanzamos el contenedor, usando el modo Host para que se pueda accesar luego.

    docker run -dit -p 8080:8080 --network=host -v /var/run/docker.sock:/var/run/docker.sock --name jenkins-curso qqjenkins

Esperamos un rato

Ahora lo que vamos a hacer, es clonar un repo

    git clone https://github.com/mguazzardo/devopsNinja

y luego nos vamos al directorio

    cd devopsNinja/CentosDocker/DebianSSH

y ahi generamos la imagen de docker con ssh, y luego la lanzamos

    docker build -t debian .

y la lanzamos

    docker run -d --name debian debian

Luego probamos de entrar por ssh, el pass es master

    ssh devops@172.17.0.2 

- https://killercoda.com/tercermundo/scenario/dive