#Ejercicio 1
##Crea el siguiente árbol de directorios a partir de tu directorio de usuario (donde usuario representa tu nombre de usuario o login en el sistema operativo). Crea también los ficheros vacíos pg1 y ma51ik en los directorios que se indican en la ilustración

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

#Ejercicio 2
##Mueve el directorio pics dentro del directorio ug1. Renombra finalmente dicho directorio a imagenes. Copia el directorio docs dentro de ug1.


```bash
cd $HOME
mv ./ug1/ee51vn/pics ./ug1/imagenes
cp -r ./ug1/ee51vn/docs ./ug1
```
