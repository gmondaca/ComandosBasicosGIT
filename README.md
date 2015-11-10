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

Muestra el log del commit para un rango de revisiones dado

--stat : Lista el reporte de diferencias de cada revisión
      
-S'pattern' : Busca el historial de cambios que concuerden con el patrón de búsqueda

```git
git log [desde [..hasta]]
```

Muestra el archivo relacionado con las modificaciones realizadas
```git
git blame [archivo]
```

### Repositorios remotos

Trae los cambios desde un repositorio remoto
```git
git fetch [remote]
```

Descarga y guarda los cambios realizados desde un repositorio remoto
```git
git pull [remote]
```

Guarda los cambios en un repositorio remoto
```git
git push [remote]
```

Lista los repositorios remotos
```git
git remote
```

Añade un repositorio remoto a la lista de repositorios registrados
```git
git remote add remote url
```
### Ramas

Cambia el árbol de trabajo local a la rama indicada

-b rama : Crea la rama antes de cambiar el árbol de trabajo local a dicha rama

```git
git checkout rama
```

Lista las ramas locales
```git
git branch
```

Sobre-escribe la rama existente y comienza desde la revisión
```git
git branch -f rama rev
```

Guarda los cambios desde la rama
```git
git merge rama
```

### Exportando e importando

Aplica el parche desde consola (stdin)
```git
git apply - < archivo
```

Formatea un parche con un mensaje de log y un reporte de diferencias (diffstat)
```git
git format-patch desde [..hasta]
```

Exporta resumen de la revisión (snapshot) a un archivo

--prefix=dir/ : Anida todos los archivos del snapshot en el directorio
      
--format=[tar|zip] : Especifica el formato de archivo a utilizar: tar or zip
      
```git
git archive rev > archivo
```

### Etiquetas

Crea una etiqueta para la revisión referida

-s : Firma la etiqueta con su llave privada usando GPG

-l [patrón] : Imprime etiquetas y opcionalmente los registros que concuerden con el patrón de busqueda

```git
git tag name [revision]
```

### Banderas de Estado de los Archivos

M (modified) : El archivo ha sido modificado

C (copy-edit) : El archivo ha sido copiado y modificado

R (rename-edit) : El archivo ha sido renombrado y modificado

A (added) : El archivo ha sido añadido

D (deleted) : El archivo ha sido eliminado

U (unmerged) : El archivo presenta conflictos después de ser guardado en el servidor (merge)







































