# Clase 02 - Git Desarrollo Colaborativo

## Forma corta de visualizar el status

```sh
git status --short
```

# Ramas (Branches)

```sh
git branch
```

## Crear rama

```sh
git branch <nombre-rama>
git branch feature/branches
```

## Cambiar de rama

```sh
git switch <nombre-rama>
git switch feature/branches
git switch - # Moverse entre las últimas ramas que estuvimos
```

## Borrar una rama

```sh
git branch -d <nombre-rama>
git branch -d feature/branches
```

## Creamos y nos movemos a la rama

```sh
git switch -c <nombre-rama>
git switch -c feature/branches
```
