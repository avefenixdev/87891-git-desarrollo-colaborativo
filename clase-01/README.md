# Clase 01 - Git Desarrollo Colaborativo

## Verificar que se haya instalado GIT

```sh
git --version
```  

## Configurando GIT por primera y única vez

```sh
git config --global user.name <nombre-del-usuario>
git config --global user.name "Ave Fenix Dev"
git config --global user.email <correo-electronico-github>
git config --global user.email "avefenixdev@gmail.com"
git config --global user.mail "avefenixdev@gmail.com"
```

## Controlar que la configuración exista y saber cuál es

```sh
git config --global --get-regexp <regex-expression>
git config --global --get-regexp user
git config --global --list
```

## Borrar configuraciones

```sh
git config --global --unset <nombre-configuración>
git config --global --unset user.mail
```

## Ver estado del archivos y área en la que están mis archivos

```sh
git status
```

## Los archivos pueden estar en varios estado dentro del proyecto

* untracked -> El archivo existe, git sabe que existe pero no le está dando seguimiento.