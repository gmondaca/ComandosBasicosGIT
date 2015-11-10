## Comandos Básicos de Git

### Buscando Ayuda
Muestra la ayuda para ese comando

```git
git help comando
```

```git
git comando --help
```

### Creación de un repositorio
Crea un repositorio en el directorio actual

```git
git init
```
Clona un repositorio remoto dentro de un directorio
```git
git clone url
```

### Operaciones sobre Archivos
Adiciona un archivo o un directorio de manera recursiva

```git
git add path
```

 Remueve un archivo o directorio del árbol de trabajo
 -f : Fuerza la eliminación de un archivo del repositorio

```git
git rm ruta
```

Mueve el archivo o directorio a una nueva ruta
-f : Sobre-escribe los archivos existentes en la ruta destino

```git
git mv origen destino
```

Recupera un archivo desde la rama o revisión actual
-f : Sobre-escribe los cambios locales no guardados

```git
git checkout [rev] archivo
```

### Trabajando sobre el código
Imprime un reporte del estado actual del árbol de trabajo local

```git
git status
```

Muestra la diferencia entre los cambios en el árbol de trabajo local

```git
git diff [ruta]
```

Muestra las diferencias entre los cambios registrados y los no registrados

```git
git diff HEAD ruta
```

Selecciona el archivo para que sea incluido en el próximo commit

```git
 git add path
```

Marca el archivo para que no sea incluido en el próximo commit

```git
 git reset HEAD ruta
```

 Realiza el commit de los archivos que han sido registrados (con git-add)
-a : Automáticamente registra todos los archivos modificados

```git
git commit
```

Deshace commit & conserva los cambios en el árbol de trabajo local
```git
git reset --soft HEAD^
```

Restablece el árbol de trabajo local a la versión del ultimo commit
```git
git reset --hard HEAD^
```

Elimina archivos desconocidos del árbol de trabajo local
```git
git clean
```

Elimina archivos desconocidos del árbol de trabajo local
```git
git clean
```

### Examinando el histórico
Muestra el log del commit, opcionalmente de la ruta especifica
```git
git log [ruta]
```





































