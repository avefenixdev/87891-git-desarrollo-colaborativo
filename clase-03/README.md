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

El pop recupera el último stash y si no hay conflicto lo elimina.

```sh
git stash pop
```

## Borrar un stash

```sh
git stash drop <numero-stash>
git stash drop 1
```

## Aplicar un stash en particular

Aplicar el stash elegido y no lo elimina.

```sh
git stash apply <numero-stash>
git stash apply 2
```

## Mostrar el contenido del stash

```sh
git show stash@{0}
```

## Colocarle un mensaje descriptivo al stash

```sh
git stash -m "Mesaje descriptivo"
```
