Puedes manejar los procesos como visualizar, eliminar o filtrar desde la terminal de un modo diferente a usar ctrl + alt +suprimir. Te explicamos cómo lograrlo.

## Ver los procesos activos en la terminal (ps)

El comando `ps` muestra los procesos que están activos en una tabla muy sencilla de entender, donde el la primera columna tenemos el process ID y en la última el nombre.

![ejemplo-de-procesos-activos-en-la-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28179%29.png)

## Ver procesos más detallados (top)

Si quieres ver una lista más detallada de los procesos con su consumo en CPU y en RAM, además del usuario que lo activó, usamos el comando `top`.

![uso-del-comando-top-en-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28180%29.png)

Aquí podemos filtrar por _user_. Si presionas la tecla “u” podrás escribir el nombre de usuario por el cual quieres buscar y si presionas la tecla “h” te mostrará un cuadro de ayuda para más opciones. Para salir presiona “q”.

## Matar un proceso (kill)

Para matar un proceso usamos el comando `kill` seguido del PID del proceso que queremos matar.

Si estás usando Windows y tienes varias aplicaciones abiertas podrás usar la terminal para cerrarlas, pero para los que estamos usando WSL solo podemos acceder a los procesos que se ejecuten en la terminal.

Pero la teoría es la misma, buscamos el PID del proceso que queremos matar y lo matamos.

![usar-comando-kill-de-la-terminal.png](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%28181%29.png)

En este caso si ejecuto el comando `kill 595` voy a cerrar la terminal.

## Tabla de comandos para manejo de procesos en la terminal

|Comando|Función|
|-------|----------|
|ps|Muestra una tabla con los procesos que se están ejecutando|
|top|Muestra una interfaz con los procesos que se están ejecutando más los recursos que consumen información adicional|
|kill|Mata el proceso que le indiques|
