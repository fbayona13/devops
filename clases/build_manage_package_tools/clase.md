## GIRHUB BRANCHES

Las branches que por lo general vamos a encontrar en un proyecto y las que tenemos que usar 

    Main--> main/master branch
    Develop--> La aplicacion que se esta desarrollando
    Hotfix --> Errores criticos y emergencia, son parches inmediatos de codigo 
    Feature--> Nuevas features que vamos agregando y modificando. Despues se hace merge a Release. Requiere estabilizar release.
    Nofeature-->
    Release--> 

## GIT FLOW

Esto seria la parte de git y github)

    - git pull repositorio
    - git checkout -b feature/ticket
    - se edita el <archivo> especifico 
    - git add <archivo>
    - git push (automaticamente GH nos tira un PR)
        esto pasa porque estamos trabajando una branch sobre otra (feature sobre developer)



## COMO USAR SSH EN VEZ DE HTTPS

- ssh-keygen -t rsa (enter a todo)
- cd .ssh 
- ls <la carpeta en /c/ donde esta la carpeta>
- cat id_rsa.pub (genera la key y la copiamos)

en el repo)
    settings)
        ssh and gpg keys) 
            creamos la key) se usa la clave publica, nunca la privada.

- pwd 
- git clone git@github.com:<usuario>/<repositorio>.git