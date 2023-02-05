Puedes aprender a crear archivos comprimidos .zip o .tar que vemos en nuestro sistema operativo. Estos encapsulan muchos archivos e incluso carpetas.

## Comprimiendo archivos con formato .tar

El formato .tar es un tipo de compresión bastante usado en UNIX. Originalmente era utilizado para almacenar información en cintas magnéticas, así que está hecho especialmente para comprimir los archivos de forma lineal.

Para comprimir con este formato en la terminal usamos el comando `tar` que tiene ciertas opciones para aprender.

Sintaxis:

``` shell
tar [opciones] [nombreDelArchivoComprimido] [archivoAComprimir]
```

### Comprimir (-c)

Para comprimir un archivo utilizamos la opción `-c`. En todos los casos hay que usar la opción `-f` para indicar que estamos comprimiendo o descomprimiendo archivos.

``` shell
tar -cf compressed.tar Documents/toCompress/
```

![comprimir-archivo-con-tar.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28173%29.png)

### Ver lo que está haciendo el comando (-v)

Si queremos ver lo que el comando está comprimiendo a medida que se va ejecutando, usamos la opción `-v`. Por cierto la opción `-v` es de “Verbose” y muchos comandos la usan, también te la puedes encontrar como `--verbose`.

``` shell
tar -cvf compressed.tar Documents/toCompress/
```

![comprimir-con-tar-verbose.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28174%29.png)

### Comprimir con formato “.tar.gz” (-z)

El formato “.tar.gz” o también “.tgz” es una versión extendida del formato tradicional de compresión “.zip” que puede manejar y comprimir archivos más grandes.

Para manejar la compresión de archivos “.tar.gz” o “.tgz” se usa la opción `-z` además de tener que especificar en el nombre de archivo la extensión que quieres usar.

``` shell
tar -czvf compressed.tar.gz Documents/toCompress/
```

![ejemplo-para-comprimir-con-tar.gz.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28175%29.png)

### Descomprimir (-x)

Para descomprimir es mucho más sencillo, solo hay que especificar la opción `-x` y el archivo comprimido que se quiere descomprimir.

Si se quiere descomprimir un archivo de extensión “.tar.gz” o “.tgz” hay que especificar la opción `-z` también.

``` shell
tar -xzvf compressed.tar.gz
```

![ejemplo-para-descomprimir-tar.gz.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28176%29.png)

## Comprimiendo archivos .zip

Para comprimir usamos el comando `zip` con el nombre que quieres que tenga y lo que quieres comprimir.

Si quieres comprimir una carpeta con archivos dentro, tienes que especificar la opción `-r` de “recursive”.

``` shell
zip -r copressed.zip Documents/toCompress/
```

![como-comprimir-con-zip.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28178%29.png)

Y para descomprimir es incluso más fácil, solo escribe el comando `unzip` seguido de lo que quieres descomprimir.

``` shell
unzip compressed.zip
```

## Tabla de comandos tar y zip

### Opciones del comando tar

Recuerda siempre colocar la opción `-f`.

|Opción|Función|
|--------|---------|
|c|Comprimir|
|x|Descomprimir|
|z|Especifica que lo que se va a comprimir o descomprimir tiene extensión “.tar.gz” o “.tgz”|
|v|Muestra lo que está comprimiendo o descomprimiendo|

### Comando zip

Recuerda que si lo que vas a comprimir es una carpeta tienes que usar la opción `-r`.

|Comando|Función|
|----------|--------|
|zip|Comprimir|
|unzip|Decomprimir|
