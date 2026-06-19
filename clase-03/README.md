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

# Extensión de Visual Studio Code

- GitLens <eamodio.gitlens>

# Git Reset

Me permite descartar commits y enviarlos a diferentes zonas o eliminar definitivamente el commit y sus cambios.

# soft

Elimina los commits y los cambios guardados dentro de esos commits se envían al staging area

```sh
git reset --soft <numero-hash>
```

# mixed (default)

Elimina los commit/s seleccionados y los cambios dentro de esos commits quedan en el working directory

```sh
git reset <numero-hash>
git reset --mixed <numero-hash>
```

# hard (CUIDADITO)

Elimina los commit/s seleccionados y los cambios los descarta, los pierdo.

```sh
git reset --hard <numero-hash>
```
