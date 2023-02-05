metLas wildcards o comodines son una serie de caracteres especiales que nos permiten encontrar patrones o realizar búsquedas más avanzadas. Es aplicable para archivos y directorios.

Las wildcards te sirven para realizar seccionamiento de archivos o directorios, ademas de `ls` los wildcards tambien pueden usarse con cualquier comando que realice la manipulación de archivos como `mv`, `cp` y `rm` .

## Tipos de wildcards

### Buscar todo (\*)

El asterisco te ayuda a buscar toda la información dentro de una carpeta, pero puedes limitar su uso. Si por ejemplo quieres buscar los archivos que tengan una extensión “.png”, escribes:

``` bash
ls -l *.png
```

También lo puedes poner al final, si quisieras buscar, todos los archivos que comiencen por unos caracteres específicos, entonces escribes esos caracteres y luego el asterisco.

Por ejemplo, si quisieras buscar todos los archivos que comiencen por “fotosDe”, habría que escribir:

``` shell
ls -l fotoDe*
```

### Buscar por cantidad de caracteres (?)

Si dentro de tus archivos tuvieras una especie de código para guardar tus fotos, algo así como “foto1.png”, “foto2.png”, “foto3.png”, etc. En este caso, sabemos que primero tenemos el string “foto”, luego un solo número y por último la extensión “.png”.

Si quisieras buscar esas fotos escribirías:

``` shell
ls -l foto?.png
```

Pero si sabes que no tiene un solo caracter, sino que tiene varios, entonces escribes tantos signos de interrogación como caracteres existan. Por ejemplo, si quieres buscar las fotos que tengan esta estructura “foto11.jpg”, escribes:

``` shell
ls -l foto??.jpg
```

### Buscar por caracteres específicos ([])

Si quieres buscar por varios caracteres específicos se usan corchetes. Para utilizarlos tienes que colocar dentro de los corchetes los caracteres que quieres buscar.

Por ejemplo, si quisieras buscar los archivos que comiencen por las letras “c” o “i”, entonces escribes:

``` shell
ls -l [ci]*
```

Lo que indica el comando es que busque los archivos que comiencen por la letra “c” o por la letra “i” y que tengan lo que sea por delante. Cuando buscamos con esta wildcard ten en cuenta que es _case sensitive_, por lo que la letra “i” no es lo mismo que la letra “I”.

``` shell
ls -l [cCiI]*
```

Por último, si quieres buscar por rango de números también tienes que usar esta wildcard. Para hacerlo, escribe el rango de números que quieres buscar separados por un guion.

``` shell
ls -l foto[2-6]*
```

Para buscar sólo directorios que empiezan por mayúscula:

``` shell
ls -d [[:upper:]]*
```

... por minúscula:

``` shell
ls -d [[:lower:]]*
```

## Tabla de wildcards

| WIldcard | Función |
|----------|---------|
|   \*     | Busca todo|
|?|Busca por cantidad de caracteres|
|[]|Busca por caracteres específicos|
