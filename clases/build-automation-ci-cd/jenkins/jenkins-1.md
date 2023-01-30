# CI / CD

## QUE ES

Sus siglas son Continous Integration / Continous Delivery.
Es un metodo para distribuir aplicaciones a los clientes con frecuencia mediante el uso de la automatizacion en las etapas de desarrollo de aplicacion.

    plan    |   code    |   build   |   test    |   release     |    deploy     |   operate
            |                                   |                               |
            |     Continous Integration         |      Continous Delivery       |

## ETAPAS DE DESARROLLO: Automatizacion

    Construccion --> Compilacion --> Prueba 

## COMO FUNCIONA

- son un conjunto de pasos 
- de naturaleza interactiva
- que conforman una cadena 
- y se puede llevar a cabo con Jenkins

Los desarrolladores tiran un repo en Git, de Git va a Jenkins y este genera un Artifact.

## JENKINS (arquitectura y funcionamiento)

Es una herramienta que nos puede ayudar a crear pipelines. Lo que se conoce como servidor de integracion continua o CI server. Tambien permite definir pasos para continuos delivery y continous deployment.
Lo que permite configurar el pipeline para los componentes de software que tengamos.

## COMPONENTES JENKINS

    PROYECTS:  contienen la descripcion del trabajo que Jenkins debe ejecutar, dicha descripcion es basicamente el pipeline del software

    BUILD: el resultado de una ejecucion de un proyecto 

    AGENT: es una maquina o contenedor que esta conectada al controlador Jenkins y se encarga de ejecutar las tareas del proyecto. 

El worker es una maquina que se encarga de compilar, mientras que el agent se encarga de la ejecucion de tareas del proyecto.

## INSTALACION Y PROYECTOS 

Se instala sobre un contenedor, por lo que es necesario tener instalado docker en nuestra maquina.

    PROYECTO ESTILO LIBRE 
        Nos permite automatizar tareas que podrian ser repetitivas, permitiendonos ejecutarlas cada cierto tiempo determinado desde algun repositorio o con algun tipo de parametro. Automatizar configuracion o tareas que deben ser planificadas.

    PROYECTO ESTILO LIBRE PARAMETRIZADO 
        Nos permite automatizar diferentes tareas para poder realizar una accion. Dicha accion puede tener parametros de entrada. Jenkins tiene un mecanismo que nos permite usar los nombres de los parametros y personalizarlos.

### Otras herramientas similares a Jenkins

    En el cloud: 
        Azzure devops 
        Gitlab CI
        Gitlab runner 
        Harness --> Muy nueva, desconfia. No necesita codificar
        cloudbees --> Jenkins empresarial, con integracion y soporte