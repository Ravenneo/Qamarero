#Instalar Sunmi por WiFi
-Conectamos la impresora por USB
-Abrimos la consola de comandos de Windows ( buscamos CMD en la barra de tareas de Windows), escribimos “ipconfig”. Esto nos dará la ip del pc, nos fijamos en el tercer numero, esta es la red de nuestro PC, numero que siemore debe ser igual (en este caso la red es 8).

-Instalamos y abrimos los drivers de sunmi cloud para configurar la impresora (https://drive.google.com/file/d/1DotYU_S6c5FYAaqD4R7-evBgHBFJMM5C/view)
-Abrimos los drivers, clicamos en la rueda de ajustes y lo ponemos en ingles, cerramos y abrimos para que nos salga en ingles.
-Ahora clicamos en “Connect”, seleccionando la opción de USB.

-Vamos a la pestaña de WIFI, aquí damos una ip estatica en la misma red que nuestro equipo, en este caso el tercer numero debe ser 8. La netmask siempre será la misma (255.255.255.0) y la Gateway siempre acaba en 1 en la mima red que la ip (192.168.8.1).Tambien añadimos los datos del wifi del cliente, siempre en una red 2.4G. Clicamos en Save y salimos, si todo ha ido bien, la Sunmi tendrá una luz azul y si probamos a conectar de nuevo, aparece la opción de network.

-Cerramos el programa y vamos a Qamarero, una vez instalado JSPrintManager ya podemos agregar la impresora por ip a la plataforma.

