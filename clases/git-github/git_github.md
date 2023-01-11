## CONTROL DE VERSIONES 
Git/Github nos permite tener un producto e ir largando diferentes versiones con mejoras de manera global

    Centralizado --> gitbucket nos permite tener un repositorio en un solo lugar y cada usuario/developer puede acceder a el, generar una copia del trabajo, y generar un update del codigo.

    Descentralizado --> github nos permite hacer lo mismo que el centralizado, con la diferencia que cada usuario/developer va a tener su propio repositorio local, y el repositorio remoto es el proyecto en si.

## REPOSITORIO REMOTO



## Estado de ficheros 

    Untracked (U)--> Git sabe del archivo nuevo pero Git no lo esta siguiendo.
    Modified (M)--> Git tiene un cambio sobre un archivo que sigue.
    |
    | git add ...
    v
    Staged (A)--> Git le asigna un id a todo el conjunto de cambios.
    |
    | git commit -m ...
    v
    Unmodified --> Git nos dice que el archivo no ha sido modificado
