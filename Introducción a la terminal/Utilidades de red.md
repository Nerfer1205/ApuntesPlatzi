El manejo de redes es bastante amplio, de hecho, es toda una rama de la informática. Aquí aprenderás comandos básicos de utilidades de la red para que puedas obtener la información que necesites.

## Configuración de tus dispositivos (ifconfig)

Ve a tu consola, escribe el comando `ifconfig` y miremos el resultado.

Cuando ingresamos el comando podemos ver el nombre del dispositivo de red, en este caso es “eth0”, y su configuración, tenemos su dirección IPv4 e IPv6 y su máscara de red.

También tienes la opción del comando `netstat` solo que te lo mostrará de forma más amigable usando una tabla.

## Enviar solicitudes a una página (ping)

A veces queremos saber si una página está disponible desde nuestra dirección IP. Para esto escribimos el comando seguido de la URL a la que queremos acceder.

El comando `ping` envía paquetes a esa página y evalúa el tiempo de respuesta.

Por defecto, el comando se ejecutará indefinidamente, así que tienes que detenerlo con ctrl + c.

``` shell
ping www.google.com
```

De esta salida obtuvimos la dirección IP de esa URL, también cuanto tiempo tardó en responder la página medida en milisegundos y en la parte de abajo tenemos el total de paquetes que se enviaron, los paquetes que se recibieron, el porcentaje de paquetes perdidos y el tiempo de respuesta promedio de las consultas.

Vamos a ver unas pocas opciones más de este comando.

### Limitar los paquetes enviados (-c)

Para limitar la cantidad de paquetes que enviamos, usamos la opción `-c` seguida del número de paquetes por enviar.

``` shell
ping -c 4 www.google.com
```

![uso-de-ping-para-limitar-paquetes-enviados.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28162%29.png)

### Especificar el tamaño de los paquetes (-s)

Para probar la conectividad con paquetes de diferentes tamaños se utiliza la opción `-s` seguido del tamaño del paquete que desees usar. El tamaño debe ser en bytes.

Para hacer pruebas con paquetes de 20 bytes escribimos:

``` shell
ping -s 20 www.google.com
```

![uso-de-ping-especificar-tamaño-de-paquetes.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28163%29.png)

## Obtener el archivo de una página (curl | wget)

Podemos obtener archivos que nos proporcione un sitio web o dirección IP con el comando `curl`. Este te mostrará la información que haya encontrado en la consola.

``` shell
curl www.google.com
```

Al ejecutar este comando te dará el documento “.html” de Google, el cual lo verás como un montón de letras locas si estás empezando.

El comando `wget` hace algo similar, solo que en vez de mostrar lo que h obtenido por consola lo guarda en el archivo que le especifiques.

``` shell
wget www.google.com
```

![uso-de-comando-wget.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28164%29.png)

La última línea de la salida del comando `wget` dice que la información fue guardada en el archivo “index.html”, el cual podemos ver al listar los archivos.

También podemos específicar varias direcciones para descargar varias páginas al mismo tiempo.

``` shell
wget www.google.com www.platzi.com
```

![ejemplo-uso-wget.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28165%29.png)

Aquí vemos como se guardó la página de Google en “index.html.1” y la de Platzi en “index.html.2”.

## Ruta de acceso a la página (traceroute)

Cuando nos conectamos a una página en internet no nos conectamos directamente a los servidores en los que está almacenada esa página, sino que primero pasamos por otros servidores que son como intermediarios entre tu computadora y el servidor.


## Tabla de comandos de utilidades de red

|Comando|Función|
|------------|-------|
|ifconfig|Muestra la configuración de los dispositivos de red|
|ping|Envía paquetes a una dirección para comprobar su conectividad|
|curl|Muestra por consola el archivo devuelto por la dirección|
|wget|Guarda el archivo devuelto por la dirección|
