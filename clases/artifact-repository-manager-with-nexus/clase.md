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