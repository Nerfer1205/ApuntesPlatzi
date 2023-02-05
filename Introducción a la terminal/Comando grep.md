
## ¿Qué significa grep?


“Grep” significa **G**lobal **R**egular **E**xpression **P**rint.
La sintaxis es sencilla: comando, lo que quieres buscar, archivo:

``` shell
grep [ExpresiónRegular] [archivoDondeBuscar]
```

En los recursos tienes un archivo llamado “movies.csv”; vamos a buscar palabras dentro de ese archivo:

``` shell
grep the movies.csv
```

![usar-comando-grep.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28153%29.png)

## Cómo usar el comando grep

### Ignorar case sensitive (-i)

Puede que queramos buscar la palabra “Action” pero eso dará exclusivamente las coincidencias con la “A” mayúscula. Esto lo podemos ignorar con la opción -i, que buscará independientemente de si la letra “A” es mayúscula o minúscula.

``` shell
grep -i Action movies.csv
```

### Contar ocurrencias (-c)

Si quieres saber cuántas veces se repite una palabra, usa la opción `-c` seguida de la palabra que quieres buscar.

``` shell
grep -c Drama movies.csv
```

![usar-comando-grep-para-ocurrencias.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28155%29.png)

### Excluir una expresión (-v)

Para saber cuáles son los resultados que NO coinciden con tu expresión regular, usas la opción `-v`.

Por ejemplo, si queremos contar todas las películas que no son de drama, escribimos:

``` shell
grep -cv Drama movies.csv
```

![usar-grep-para-excluir-expresion.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28156%29.png)

### Limitar la búsqueda (-m)

Para no buscar en todo el archivo, sino las primeras ocurrencias, podemos limitar la búsqueda en líneas con la opción `-m` seguida del número de líneas que queremos encontrar.

Por ejemplo, si queremos buscar las primeras 10 líneas que concuerden con la palabra “Fan” escribimos:

``` shell
grep -m 10 Fan movies.csv
```

![usar-grep-para-limitar-busqueda.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28157%29.png)

## Tabla de funciones de grep

|Opción|Función|
|-------|---------|
|-m|Limita las líneas de la búsqueda|
|-c|Cuenta las ocurrencias|
|-v|Excluye las ocurrencias|
|-i|Ignora él case sensitive|
