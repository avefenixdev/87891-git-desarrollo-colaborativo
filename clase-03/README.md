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

## Gist

Compartir código, pasar snippets a otras personas o información que quiero compartir. Pueden tener varios archivos y sus revisiones

<https://gist.github.com/>

- SECRETOS -> Solo la persona que tenga el link va a poder verlo. No son privados.
- PÚBLICOS -> Se van indexar en los motores de búsqueda

## Proyectos

Son tableros visuales tipo Kanban donde podemos organizar y visualizar el progreso de nuestras tareas asociar tareas a resolución de issues.

## Issues (Posibles problemas, solución de temas)

Nos permiten tener un seguimiento sobre posibles bugs o errores en nuestras aplicaciones.

## Trabajar colaborativamente con personas que no conozco (Fork y Pull Request)

Me permite trabajar colaborativamente en proyectos donde no conozco a las personas o no tengo la suficiente confianza para darle permisos al repositorio de trabajo.

Normalmente cuando trabajo con Fork y Pull Request lo hago en proyectos Open Source.

- Fork es una copia del respositorio remoto de alguien a mi cuenta de GitHub.
- Pull Request. Solicitud a los dueños originales del repositorio para proponerles un cambio. Es una propuesta de cambio a alguien que no conozco pero quiero ayudar.

1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.

---

5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

   git remote add upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

   git pull upstream <rama-que-quiero-actualizar>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

   git push origin <rama-a-actualizar>
