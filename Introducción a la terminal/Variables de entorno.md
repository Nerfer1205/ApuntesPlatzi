Las variables de entorno son útiles cuando necesitamos que cierta información prevalezca para poder trabajar más rápido o necesitamos guardar información para no tener que recordarla constantemente.

Para ver todas las variables de entorno:

``` shell
printenv
```

Ver valor de la variable:

```shell
echo $HOME
```

## Variables de entorno en Linux

En linux hay varias variables de entorno que ya están preestablecidas, para verlas desde la consola es tan simple como usar el comando seguido de la variable de entorno.

Por cierto, todas las variables de entorno se mandan a llamar con un signo de peso por delante, de lo contrario se interpretará como un comando.

|Variable|Contenido|
|---------|----------|
|HOME|Indica el home del usuario|
|PATH|Indica las direcciones de donde están los binarios que usa el sistema|
|BASH_VERSION|Indica la versión del bash que estás utilizando|
|SHELL|Dirección de la shell que estás utilizando|


Hay muchas más, pero estas son las que te pueden interesar. Por cierto, por convención las variables de entorno se crean en mayúsculas.

## ¿Cómo crear tus propias variables de entorno?

En el home de tu usuario debe haber un archivo oculto llamado “.bashrc”, lo puedes ver ejecutando el comando `ls -la` la opción `-a` es de all.

``` shell
ls -la
```

![ejemplo-como-crear-variables-entorno.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/Sin%20t%C3%ADtulo%288%29.png)

Ábrelo utilizando el comando `code .bashrc`, si tienes instalado VS Code esto te mostrará el documento en el editor. Si estás en WSL y no te funciona, ve a la cmd, ejecuta el comando `wsl` y vuélvelo a intentar desde ahí.

Cuando lo abras ten cuidado con lo que tocas, podrías dañar la shell, pero desde ahí puedes crear una variable de entorno, por ejemplo, como yo estoy usando WSL, voy a crear una variable de entorno que me de la ruta de mi carpeta en Windows sin que tenga que escribir toda la ruta.

![ejemplo-al-ejecutar-variables-entorno.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28130%29.png)  
Ahora guardo el archivo, reinicio la terminal y ejecuto:

``` shell
cd $WINDOWS
```

Pero se puede hacer mejor porque también puedo crear un alias que no se borre cuando cierre la terminal.

![ejemplo-configuracion-variable-entorno.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/Sin%20t%C3%ADtulo%289%29.png)

![ejemplo-configuracion-variables-de-entorno.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28132%29.png)

Ahora solo tengo que ejecutar `cc` para ir a mi carpeta en Windows sin necesidad de escribir la variable de entorno.

Ahora crea las variables o alias que necesites para ser más eficiente tu trabajo, por ejemplo, podrías crear un alias que ejecute VS Code y lo abra en la carpeta que requieres.