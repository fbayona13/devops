# CONTINUOS INTEGRATION / CONTINUOS DEPLOYMENT

Introduccion a CI / CD

    Codigo Fuente
    |
    |
    v
    Herramienta Build   <-- Repo de librerias externas 
    (manual / Jenkins)
    |
    |
    v 
    Unidad de deploy    --> Herramienta de packaging    --> Package     --> Repository
    (Imagen)

Pipeline de CI) que esto se debe hacer en ambientes de desarrollo

    clono code --> revision de code --> revision de seguridad --> revision de seguridad --> creo Imagen --> test de seguridad Imagen --> subo la Imagen al repositorio (Nexus)

Pipeline de CD) 

## PAQUETE / ARTIFACT

    Es un contenedor de la unidad de deploy para que la misma pueda ser distribuida en los sistemas/instancias en la que deba ser instalada

## REPOSITORIO DE SOFTWARE

    Es donde se almacenan los paquetes que despues van a ser promovidos y/o instalados en entornos o instancias. 

## NEXUS REPOSITORY MANAGER 

    Es un repositorio de software con soporte para repositorios de varios tipos, lo cual facilita la organizacion y administracion de los repositorios. Por ejemplo: 

        - Maven para Java
        - Imagenes de Docker
        - paquetes NPM de JavaScript
        - librerias de Go
        - modulos de Python 

    Nexus OSS --> la version de codigo abierto. gracias a sus funciones de proxy, permite que componentes de repositorios publicos se almacenen en una cache interna.

### tipos de repositorios Nexus

    Hosted: los repositorios que alojan artefactos que se suben despues del proceso de build.

    Proxy: obtiene artefactos de un repositorio publico y los guarda internamente. 

    Group: es una agrupacion de varios repositorios.

### alternativas a Nexus

    Harbor
    DockerHub
    los cloud tienen sus propios repos

### COMANDOS

    docker volume --> crea un volumen que almacena la informacion del contenedor antes de crear el contenedor
    docker inspect volume <nombre del volumen> --> hace una inspeccion sobre el volumen que creamos
    