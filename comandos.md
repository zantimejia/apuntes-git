# Comandos

### Para iniciar un proyecto
```
git init
git add nombreArchivo
```

### Set de comandos para Commit's
```
git add . * Para hacer commit a todos los archivos
git add -A * Agrega archivos que ya seguimos y estan en el directorio de preparacion.
git commit
git commit -m "Comment"
git commit -a -m "Comment" * Solo agrega los archivos que ya estamos siguiendo.
git commit --amend * Para modificar un commit, ya sea un comentario o agregar un archivo olvidado a ese commit. Para este ultimo se debe primero hacer add del archivo olvidado para que el amend lo coja y lo lleve al area de preparacion.
git reset HEAD nombreArchivo * Para sacar archivos del directorio de preparacion.
```

### Set de comandos para conocer estados e hisrotial
```
git status
git log
git log oneline * Muestra los logs abreviados
git log graph * Muestra los logs con pequeños graficos ASCII
git log --pretty=format: "%h - %an, %ar : %s" * Darle formato a los logs, %h hash, %an autor, %ar fecha relativa y %s comentario.
git log --after,before="fecha a filtrar"
git diff - Para saber que tenemos en el directorio de trabajo.
git diff --staged - Para saber lo que tenemos en el directorio de preparacion.
```

### Set de comandos para etiquetas
```
git tag nombreEtiqueta * [Etiqueta Ligera], crea una etiqueta y se la asigna al ultimo commit que se realizo. [Usadas para destacar algo con importancia baja]
git tag -a nombreEtiqueta -m "Comment" *  [Etiqueta Anotada], crea una etiqueta y se la asigna al ultimo commit que se realizo. [Usadas para destacar commit's con importancia alta como una version]
git tag nombreEtiqueta hash * Le asigna una etiqueta a algun punto escogido en la historia.
git tag * para listar las etiquetas que tengamos
git show nombreEtiqueta o hash * Muestra el commit al que le hemos asignado la etiqueta
```

### Set de comandos relacionados con Ramas - Branch
```
git branch nombreRama * Crea una nueva rama a partir del commit donde estemos ubicados. [Mundo paralelo]
git branch * Lista las ramas y en que rama estamos actualmente.
git branch -v * Nos muestra las ramas y el ultimo commit de cada una de estas.
git branch -d nombreRama * Elimina una rama solo si ya la hemos fusionado con otra.
git branch -D nombreRama * Elimina una rama sin importar si ya la hemos fusionado con otra.
git branch --no-merged * Nos indica que ramas no hemos fusionado con la rama actual.
git branch --merged * Nos indica que ramas se han fusionado.
git merge nombreRama * Incorpora otraRama en la Rama actual.
git checkout -b nombreRama * Crea una nueva rama a partir del commit donde estemos ubicados y saltamos hacia ella. [Mundo paralelo]
git checkout -- nombreArchivo, hash, etiqueta o rama * En caso de que eliminemos un archivo, asi lo podemos recuperar del directorio de git o usando el hash de algun punto especifico del tiempo.
```

### Set de comandos para subir nuestro proyecto a un repositorio remoto

### Creando repositorio desde CLI
```
echo "# apuntes-git" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/zantimejia/apuntes-git.git * Url del repositorio
git push -u origin master
```

### Repositorio existente
```
git remote add origin https://github.com/zantimejia/apuntes-git.git * Url del repositorio
git push -u origin master
```

### Otros comandos
```
git rm nombreArchibo * Elimina archivos ratreados del direcotrio de preparacion y de nuestro directorio de trabajo.
git mv nombreArchivo * Renombra un archivo.
git clone url del repositorio * Copia el repositorio remoto.
git fetch origin nombreRama * Nos trae los cambio desde el repositorio remoto y a continuacion se debe hacer un merge entre la rama local y la que trajimos con los cambios.
git push origin --delete nombreRama * Elimina una rama remota.
git pull origin master * Nos trae los cambio y nos hace merge con la rama local [Nos evita usar el fetch y despues merge].
git remote --verbose * Nos muestra los repositorios remotos que tengamos configurados.
git remote add nombreRepo URL * Nos agrega un nuevo repositorio remoto a la configuracion.
git revert HEAD * Para revertir un commit que hayamos hecho.
```
