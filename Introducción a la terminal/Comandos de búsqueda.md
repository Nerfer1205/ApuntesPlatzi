A veces necesitas localizar varios archivos del mismo tipo que ocupan espacio innecesario en tu disco duro.

Por ejemplo, algunos programas que funcionan desde la consola, como npm, guardan sus errores en archivos de extensión “.log” y si no estás pendiente de eliminarlos se van acumulando en tu disco duro.

## ¿Cuáles son los comandos de búsqueda en la terminal?

El comando which muestra el path completo de los comandos en la shell:

```shell 
which cd
/usr/bin/cd
```

Para encontrar archivos de forma efectiva, usa el comando `find`, el cual buscará en la ruta que le indiques el tipo de archivos que necesitas. Su sintaxis es:

``` shell
find [rutaDesdeDondeEmpezarBuscar] [opciones]
```

### Segmentar por el nombre (-name)

Veamos un ejemplo, voy a buscar en mi carpeta home todos los archivos que tenga una extensión “.png”.

``` shell
find ./ -name *.png
```

![ejemplo-comando-name.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28149%29.png)

El punto indica que debe empezar desde la carpeta en la que está y la opción `-name` es para especificar el nombre que debe buscar.

### Segmentar por el tipo (-type)

También puedes segmentar por el tipo, si es un archivo o si es un directorio utilizando la opción `-type`, el cual acepta `f` para archivos, `d` para directorios y `l` para enlaces simbólicos.

Si quieres usar más de una opción lo separas por comas.

``` shell
find ./ -type f -name "f*"
```

![usar-comando-type-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28150%29.png)

Esto me muestra todos los archivos que comiencen con la letra “f”.

Veamos un ejemplo buscando archivos y directorios.

``` shell
find ./ -type f,d -name "D*"
```

![buscar-archivos-direcorios-con-comando-type-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28151%29.png)

### Segmentar por tamaño (-size)

Con la opción `-size` podemos segmentar por tamaño ingresando el peso que queremos buscar. Esta opción tiene un uso un tanto especial. Primero que todo hay que colocar la unidad de peso **c** para byte, **k** para Kilobyte, **M** para Megabyte y **G** para Gygabyte.

Entonces, si escribes en la terminal:

``` shell
find ./ -size 4k
```

Buscará los archivos que pesen exactamente 4kb. Pero claro, atinar el peso exacto de un archivo no es para nada sencillo, así que podemos especificar que sea ese peso en adelante con el símbolo **+** o de ese peso para abajo con el símbolo **-**.

``` shell
find ./ -size +4k
```

Busca los archivos que pesen 4kb o más.

``` shell
find ./ -size -4k
```

Busca los archivos que pesen 4kb o menos.

### Buscar vacíos (-empty)

Para buscar los archivos vacíos usamos la opción empty que es fácil de usar, no tienes que especificarle nada, solo escribirla.

Por ejemplo, si quisiera buscar todas las carpetas vacías, habría que escribir:

``` shell
find ./ -type d -empty
```

![como-buscar-carpetas-vacias-en-la-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28152%29.png)

### Limitar la búsqueda (-maxdepth -mindepth)

Puede que no queramos buscar en absolutamente todas las carpetas del sistema, sino que queremos únicamente un pedacito. Para eso limitamos la profundidad de carpetas a la que el comando debe buscar, esto se hace con la opción `-maxdepth` seguido de la profundidad.

``` shell
find ./ -type d -maxdepth 2
```

Continuando, a veces ya conocemos más o menos la estructura de nuestras carpetas, así que nos queremos saltar niveles, por lo que le asignamos una profundidad mínima al comando.

``` shell
find ./ -type d -mindepth 2
```

Una última cosa, es recomendable pasar el output al comando `less`, así:

``` shell
find ./ | less
```

De esta forma podrás usar esa interfaz de `less` para buscar tus archivos.

## Tabla de comandos de búsqueda

|Opción|Función|
|-------|--------|
|-size|Busca por el peso|
|-mindepth|Asigna una profundidad mínima|
|-maxdepth|Asigna una profundidad máxima|
|-type|Busca por el tipo de archivo|
|-name|Busca por el nombre del archivo|

## Ejercicio de práctica

El hábito hace al monje y la terminal al buen programador.

Crea el comando `find` para cada uno de estos casos:

1.  Busca tus archivos mayores a 100Mb, con una profundidad máxima de 4, que comiencen por la letra d.
2.  Busca los archivos que tengan extensión “.pdf” con una profundidad mínima de 2.
3.  Busca todas las carpetas que comiencen por la letra “A” con una profundidad máxima de 5, que estén vacías.
4.  Busca todo lo que tenga una letra “j” que pese más de 1b. Luego guarda la salida en un archivo llamado “LosArchivosJ.txt” y cuando termine de hacer todo eso imprime un mensaje que diga “Comando terminado con éxito”.