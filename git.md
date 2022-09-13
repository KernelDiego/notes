# **GIT**
---

![Imagen del Funcionamiento de Git](https://miro.medium.com/max/700/1*3A2vetz_lc3VKDApRSUrQg.png)

---
## Configurar autor de los commit

```console
git config --global user.name "DiegoKernel"
```

```console
git config --global user.email "gonzalezdiego.contact@gmail.com"
```

---
## Iniciar repositorio git
```console
git init
```

---
## Agregar seguimiento de todo los archivos. Área de ensayo(staging area)
```console
git add .
```

---
## Agregar un commit con los cambios realizados
```console
git commit -m "Modifique x"
```

---
## Hacer un staging area y commit a la vez
```console
git commit -am "Modifique x"
```

---
## Subir repositorio nuevo a GitHub 
```console
git remote add origin https://github.com/kerneldiego/nombre_proyecto
```

---
## Subir repositorio a GitHub
```console
git push origin -u main
```

## Cargar repositorio de GitHub
```console
git pull origin -u main
```
> **Para hacerlo con la rama en la que te encuentras**

```console
git push/pull
```

---
## Comprobar estado del repositorio
```console
git status -s
```

---
## Ver los commit
```console
git log --oneline
```

---
## Editar commit
```console
git commit  --amend
```

---
## Eliminar commit
```
git rebase -i 3w38jef
```

> Cambiar el "pick" por "drop" del commit a eliminar

---
## Ver las ramas(branch)
```console
git branch
```

---
## Crear una nueva rama
```console
git switch -c "nombreDeRama" 
```

---
## Cambiar de rama
```console
git switch main
```

---
## Ver ramas de manera visual
```
git log --oneline --decorate --all --graph
```

---
## Cambiar de rama o commit
```console
git checkout main
git checkout 47hfxxx
```

---
## Fusionar dos ramas
```console
git merge development
```

> Posicionarse en la rama master para traer los cambios de otra rama

---
## Borrar rama(branch)
```console
git branch -d rama
```

---
## Agregar un tag(Versiones)
```console
git tag 31-8-22v1 -m "Versión 1 del proyecto"
```

---
## Subir los tags a GitHub
```console
git push --tags
```
