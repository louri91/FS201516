## Ejercicio 1
### Crear un árbol de directorios

```bash
mkdir FS FS/Ejer1 FS/Ejer2 FS/Ejer3 FS/Ejer4 FS/Ejer1/Ejer1.a FS/Ejer1/Ejer1.b
```

## Ejercicio 2
### Copiar el archivo /etc/profile en la carpeta anteriormente creada Ejer1.b

```bash
cp /etc/profile FS/Ejer1/Ejer1.b
```

## Ejercicio 3
### Crear un alias llamado búsqueda que encuentre todos los archivos con extensión .tex en el directorio /usr y los liste

```bash
alias busqueda='cd /usr ; ls -l *.{tex}'
busqueda
```

## Ejercicio 4
### Crear un script que, dado un **único parámetro** compruebe si es un archivo con permisos de escritura, si los tiene, muestra el contenido del archivo. Incluir la comprobación de parámetros

```bash
#!/bin/bash
if [ $# = 1]
  then
    if test -w ./$1
      then cat $1
    else echo "No tengo permisos de escritura"
    fi
else
  echo "Por favor, introduce solo un parametro"
fi
```

## Ejercicio 5
### Crear un script que, dado un **único parámetro** copie el contenido del directorio actual en el directorio pasado por parámetro

```bash
#!/bin/bash
if [ $# = 1]
  then
    if test -d $1
      then cp -r ./* ./$1
    else mkdir $1
      cp -r ./* ./$1
    fi
else
  echo "Por favor, introduce solo un parámetro"
fi
```
