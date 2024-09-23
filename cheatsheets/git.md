---
title: Git-GitHub
image: "/assets/images/git.svg"
---

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

## Índice

- [Índice](#índice)
- [¿Qué es?](#qué-es)
- [Comandos básicos](#comandos-básicos)
  - [Crear un nuevo repositorio](#crear-un-nuevo-repositorio)
  - [Clonar un repositorio](#clonar-un-repositorio)
  - [Añadir un archivo](#añadir-un-archivo)
  - [Añadir todos los archivos](#añadir-todos-los-archivos)
  - [Hacer un commit](#hacer-un-commit)
  - [Hacer un push](#hacer-un-push)
  - [Hacer un pull](#hacer-un-pull)
  - [Ver el estado del repositorio](#ver-el-estado-del-repositorio)
  - [Ver el historial de commits](#ver-el-historial-de-commits)
- [Branches](#branches)
  - [Nueva branch](#nueva-branch)
  - [Ver branches existentes](#ver-branches-existentes)
  - [Moverse entre branches](#moverse-entre-branches)
  - [Moverse a una branch remota](#moverse-a-una-branch-remota)
  - [Mergear branches](#mergear-branches)
  - [Eliminar una branch](#eliminar-una-branch)
- [GitHub](#github)
  - [Crear un nuevo repositorio en GitHub](#crear-un-nuevo-repositorio-en-github)
  - [Clonar un repositorio de GitHub](#clonar-un-repositorio-de-github)
  - [Añadir un colaborador](#añadir-un-colaborador)


## ¿Qué es?

Git es un sistema de control de versiones distribuido, es decir, que cada usuario tiene una copia completa del repositorio. Esto nos permite trabajar de forma local y sincronizar los cambios con el repositorio remoto cuando queramos.

## Comandos básicos

### Crear un nuevo repositorio

```bash
git init
```

### Clonar un repositorio

```bash
git clone https://www.github.com/username/repo.git
```

### Añadir un archivo

```bash
git add file.txt
```

### Añadir todos los archivos

```bash
git add .
```

### Hacer un commit

```bash
git commit -m "Mensaje del commit"
```

Descripción completa

```bash
git commit -m "Mensaje del commit" -m "Descripción del commit"
```

### Hacer un push

```bash
git push origin main
```

Puede también ser en repositorios más viejos que sea `git push origin master`. Master o Main son los nombres de la branch que están pusheando, y puede variar si están pusheando otra branch.

### Hacer un pull

```bash
git pull origin main
```

Al igual que en push, en repositiorios más viejos puede ser `git pull origin master`

### Ver el estado del repositorio

```bash
git status
```

### Ver el historial de commits

```bash
git log
```

## Branches

### Nueva branch

```bash
git switch -c <nombre-de-branch>
```

La opción -c es para crear la branch, de otra forma `switch` solo nos deja movernos entre branches existentes. Si se quiere crear una branch sin movernos, es `git branch <nombre-de-branch>`.

### Ver branches existentes

```bash
git branch
```

### Moverse entre branches

```bash
git switch <nombre-de-branch>
```

### Moverse a una branch remota

```bash
git fetch
git switch <nombre-de-branch>
```

Se hace `git fetch` antes del `switch` para que el repositorio local conozca que existe esa branch en el repositorio remoto.

### Mergear branches

```bash
git merge <nombre-de-branch-a-mergear>
```

Se mergea sobre la branch actual la branch a mergear. **NO** elimina la branch a mergear.

### Eliminar una branch

```bash
git branch -D <nombre-de-branch>
```

La opción `-D` es para eliminar la branch, de otra forma `branch` solo crea esa branch, que falla si la branch ya existía. 

## GitHub

GitHub es una plataforma de desarrollo colaborativo que permite alojar proyectos utilizando el sistema de control de versiones Git.

### Crear un nuevo repositorio en GitHub

Para crear un nuevo repositorio deberemos ir a la página de [GitHub](https://github.com/) y hacer click en el botón `New repository`.

<img src="/assets/images/home.png"  width="100%" alt="Home">
<img src="/assets/images/home_create.png"  width="100%" alt="Home Create Highlight">
<img src="/assets/images/new.png"  width="100%"  alt="New">
<img src="/assets/images/new_bottom.png"  width="100%" alt="New Button">
<img src="/assets/images/new_bottom_button.png"  width="100%" alt="New Highlight">

### Clonar un repositorio de GitHub

Para clonar un repositorio deberemos ir a la página del repositorio y hacer click en el botón `Clone or download`.

### Añadir un colaborador

Para añadir un colaborador deberemos ir a la página del repositorio y hacer click en `Settings`. Una vez dentro, deberemos ir a la sección `Collaborators` y añadir el nombre de usuario del colaborador.
