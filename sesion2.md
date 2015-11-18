## Ejercicio 1

### Crea el siguiente árbol de directorios a partir de tu directorio de usuario (donde usuario representa tu nombre de usuario o login en el sistema operativo). Crea también los ficheros vacíos pg1 y ma51ik en los directorios que se indican en la ilustración

![alt text](https://github.com/louri91/FS201516/raw/master/img/ej1.png "Ejercicio1")

```bash
mkdir ug1
touch pg1
cd ug1
mkdir ee51vn
touch ma51ik
cd ee51vn
mkdir docs pics
```

## Ejercicio 2

### Mueve el directorio pics dentro del directorio ug1. Renombra finalmente dicho directorio a imagenes. Copia el directorio docs dentro de ug1.


```bash
cd $HOME
mv ./ug1/ee51vn/pics ./ug1/imagenes
cp -r ./ug1/ee51vn/docs ./ug1
```

## Ejercicio 3

### Liste los archivos que estén en su directorio actual y fíjese en alguno que no disponga de la fecha actualizada, es decir, el día de hoy. Ejecute la orden touch sobre dicho archivo y observe qué sucede sobre la fecha del citado archivo cuando se vuelva a listar

```bash
ls -lF
touch prueba.docs

ls -lF
```
Se actualiza la fecha del archivo

## Ejercicio 4

### La organización del espacio en directorios es fundamental para poder localizar fácilmente aquello que estemos buscando. En ese sentido, realice las siguientes acciones dentro de su directorio home (es el directorio por defecto sobre el que trabajamos al entrar en el sistema):

#### a) Obtener en nombre de camino absoluto (pathname absoluto) de tu directorio home. ¿Es el mismo que el de tu compañero/a?

```bash
echo $HOME
```
No, no es el mismo que el del compañero

#### b) Crear un directorio para cada asignatura en la que se van a realizar prácticas de laboratorio y, dentro de cada directorio, nuevos directorios para cada una de las prácticas realizadas hasta el momento.

```bash
mkdir FS
mkdir FS/sesion2 FS/sesion3 FS/sesion4 FS/sesion5
```

#### c) Dentro del directorio de la asignatura fundamentos del software (llamado FS) y dentro del directorio creado para esta sesión, copiar los archivos host y passwd que se encuentran dentro del directorio /etc.

```bash
cp /etc/hosts $HOME/FS
cp /etc/passwd $HOME/FS
```

#### d) Mostrar el contenido de cada uno de los archivos.

```bash
cat FS/hosts
cat FS/passwd
```

## Ejercicio 5
### Desplacémonos hasta el directorio /bin, genere los siguientes listados de archivos (siempre de la forma más compacta y utilizando los metacaracteres apropiados):

```bash
cd /bin
```

#### a) Todos los archivos que contengan sólo cuatro caracteres en su nombre.

```bash
ls ????
```

#### b) Todos los archivos que comiencen por los caracteres d, f.

```bash
ls -l [df]*
```

#### c) Todos los archivos que comiencen por las parejas de caracteres sa, se, ad.

```bash
ls -l {sa, se, ad}*
```

#### d) Todos los archivos que comiencen por t y acaben en r.

```bash
ls -l t*r
```

## Ejercicio 6

### Liste todos los archivos que comiencen por tem y terminen por .gz o .zip :

#### a) de tu directorio home

```bash
ls -l ~/tem*.{gz,zip}
```

#### b) del directorio actual

```bash
ls -l ./tem*.{gz,zip}
```

#### c)¿hay alguna diferencia en el resultado de su ejecución? Explique el por qué si o el por qué no.

Sí, `~/` ejecuta rutas absolutas mientras que `./` ejecuta rutas relativas

## Ejercicio 7

### Muestre del contenido de un archivo regular que contenga texto:

#### a) las 10 primeras líneas.

```bash
head -n 10 prueba.txt
```

#### b) las 5 últimas líneas.

```bash
tail -n 5 prueba.txt
```

## Ejercicio 8
### Ordene el contenido de un archivo de texto según diversos criterios de ordenación.

#### a) Por orden alfabetico:
```bash
sort archivo.txt
```

#### b) Por orden numerico:
```bash
sort -n archivo.txt
```

#### c) Al reves:
```bash
sort -r archivo.txt
```

#### d) Aleatoriamente:
```bash
sort -R archivo.txt
```

## Ejercicio 9
### ¿Cómo puedes ver el contenido de todos los archivos del directorio actual que terminen en .txt o .c?

```bash
cat *.{txt,c}
```
