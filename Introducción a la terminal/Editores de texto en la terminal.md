Una de las utilidades más importantes de la terminal es el editor de texto. Hay diferentes opciones, pero Vim es uno de los más sencillos y populares. También está Emacs y Nano 🤔. Veamos con más detalle el uso de Vim.

## Cómo usar Vim en la terminal

Para abrir o crear un archivo utilizando Vim escribe el comando

``` shell
vim [nombre del archivo]
```

En mi caso voy a abrir uno que ya está creado.

![ejemplo-de-uso-de-vim.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28183%29.png)

Por defecto no podrás escribir hasta que actives el modo de inserción. Para hacerlo usa la tecla `i`.

![ejemplo-usode-vim-2.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/Sin%20t%C3%ADtulo%2812%29.png)

Para salir del modo de inserción presiona la tecla `escape`. En el modo normal (en el que no puedes escribir) si escribes el slash `/` activarás un buscador similar al del comando `less`.

![uso-de-escape-en-vim.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/Sin%20t%C3%ADtulo%2813%29.png)

Para borrar una línea, estando el modo normal, tienes que ubicarte sobre ella y presionar `dd`.

Para guardar y salir presiona estando en el modo normal, activa los comandos usando `:` y escribe “wq”. La letra “w” es para guardar y la letra “q” es para salir, también los puedes usar por separado.

![ejemplo-de-uso-de-vim.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/Sin%20t%C3%ADtulo%2814%29.png)

Luego podemos revisar el contenido con el comando cat.

![comando-cat-en-vim.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28184%29.png)

## Tabla de comandos para uso de Vim

|Comando|Función|
|----------|-------|
|vim|Abre el archivo especificado. Si no existe lo crea|
|:q|Cierra el editor|
|:w|Guarda los cambios|
|/búsqueda]|Busca dentro del texto|
|dd|En el modo normal, selecciona una línea y la borra|

## Ejercicio de práctica

Si ya sabes un poco de programación, entonces para que practiques usando Vim te dejo este ejercicio.

1.  Crea una calculadora en tu lenguaje de programación de preferencia.
