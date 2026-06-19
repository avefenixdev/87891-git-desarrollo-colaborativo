# Clase 03 - Git Desarrollo Colaborativo

## .gitkeep

Al crear el archivo dentro de una carpeta vacía permite que git vea esa carpeta y pueda versionarla.

## Git Stash

Es una zona temporal donde voy a guardar cambios que aún no están funcioando o están incompletos para poder seguir trabajando normalmente en otra cosa. O para solucionar algo urgente.

````sh
git stash
## Listar los stashes

```sh
git stash list
````

## Recuperar el último stash

```sh
git stash pop
```
