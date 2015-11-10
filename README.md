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