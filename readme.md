## Curso Git desde cero
Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos.

### Zonas de Git
1. Directorio de trabajo
2. Área de preparación
3. Directorio Git

### Flujo de trabajo básico en Git
1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

### Configurando Git por primera vez
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --list
```

Esta línea fue creada en la rama master.

###Comandos
git init
git add nombreArchivo
git add . * Para hacer commit a todos los archivos
git add -A * Agrega archivos que ya seguimos y estan en el directorio de preparacion.
git commit -m "Comment"
git reset HEAD nombreArchivo * Para sacar archivos del directorio de preparacion
git status
git log
git diff - Para saber que tenemos en el directorio de trabajo.
git diff --staged - Para saber lo que tenemos en el directorio de preparacion.