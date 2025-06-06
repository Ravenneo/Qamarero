La **HPRT T808** es una impresora térmica profesional de tickets de 80mm, ideal para entornos de hostelería y retail. En nuestro caso, la utilizamos principalmente con sistemas Windows (USB, Ethernet y WiFi) y con Android exclusivamente vía **WiFi o Ethernet** (no compatible con Android vía USB en nuestro entorno).

### Características principales:
- **Velocidad de impresión**: hasta 250mm/s
- **Interfaces**: USB, Ethernet, WiFi (algunos modelos también incluyen Bluetooth)
- **Ancho de papel**: 80mm
- **Compatibilidad**: 
  - ✅ Windows (USB, Ethernet, WiFi)
  - ✅ Android (WiFi, Ethernet)
  - ❌ No compatible con iOS en nuestro entorno
- **Corte automático de papel**
- **Diseño compacto y robusto**

En este repositorio encontrarás:
- **HPRT POS Driver** para instalar impresoras.
- **HPRT Utility** para configurarlas.
- **Guías de instalación** en formato texto y video.

### 📂 Archivos disponibles:
- 📜 **[Añadir Printers](./Añadir_Printers.md)** → Explica cómo agregar la impresora.
- 📜 **[Guía WiFi](./Conectar_WiFi.md)** → Instrucciones para conectar la impresora a WiFi.
- 📜 **[Manual HPRT TP808](./Manual-HPRT-TP808-_Rev.1.5.pdf)** → Documento oficial de referencia.
- 🖥️ **[HPRT POS Printer Driver v2.7.4.3](./HPRT%20POS%20Printer%20Driver%20v2.7.4.3.zip)** → Driver necesario para la instalación.
- 🎥 **[Guía visual de instalación WiFi](./hprt-conexion-wifi_6vJQzefo.mp4)** → Video demostrativo del proceso de configuración WiFi.
-  **[Guía Instalar T808 en SUNMI D3 PRO](https://github.com/Ravenneo/Qamarero/blob/main/Printers/TP808/Instalar_Android_D3_PRO.md)** → Video demostrativo del proceso de configuración WiFi.

### 🔧 Orden de Instalación:
1. **Instalar HPRT Utility** ([Descargar aquí](https://drive.google.com/file/d/1G491OdeUZmzqntHzH4JZ0fueDveS3Ggz/view?usp=sharing))
2. **Instalar HPRT POS Driver**.
3. **Añadir la impresora a QPos**.

### Guias de Instalacion:
## Instalacion por USB:
- Conectar la impresora por usb.
- Instalar los drivers.
- Abrir la config de Windows y comprobar que funciona correctamente.
En caso de que tengamos que instalar dos o mas iguales:
- Abrimos HPRT Utility
- Agregamos las impresoras por wifi.
- Cambiamos los puertos por los que se conectan, eligiendo COM como opcion.
- Comprobar que tienen los mismos puertos en la config de Windows.

## Instalacion por WiFi:
- Conectamos la impresora por usb.
- Instalamos los drivers.
- Abrimos HPRT Utility
- Agregamos la impresora por usb seleccionando el modelo.
- Configuracion avanzada -> Configuracion de Conmutacion -> WiFi, clicamos en SET.
- Configuracion avanzada -> Configuracion WiFi.
- Clicamos en READ y cambiamos el modo a STA.
- Clicamos en scan, seleccionamos el WiFi del cliente,DHCP Enable y añadimos la contraseña, clicamos en SET.
- Nos dara una IP libre, clicamos en read para verla (es la que ira en el puerto de Windows)
- Cambiamos el DHCP a Disable para fijar la ip,grabamos con SET.
- Agregamos la impresora de nuevo, esta vez por TCP/IP, escribimos la ip obtenida anteriormente.
- Vamos a la config de impresoras de Windows, cambiamos el puerto de la impresora a la ip que tenemos.

📌 La **[Guía WiFi](./Conectar_WiFi.md)** también contiene el enlace de descarga para la Utility y explica cómo usarla correctamente.

## Instalacion por Ethernet (Impresora conectada al router):
- Conectar la impresora por usb.
- Vemos nuestra ip: Abrimos cmd -> ipconfig.
- Abrir HPRT Utility y añadir la impresora por USB.
- Advanced settings -> Ethernet Settings.
- Cambiamos DHCP Setting -> Static IP model
- Cambiamos la ip address a una ip de la misma red, los tres numeros de la ip debe ser el mismo (EJ: mi ip: 192.168.2.100, ip de la impresora: 192.168.2.105).
- Guardamos y volvemos al menu principal, pinchamos la impresora y vamos a select port.
- Cambiamos la conexion a TCP/IP, usando la ip que hemos dado a la impresora.+
- Probamos la conexion, si es correcta vamos a la config de Windows y cambiamos el puerto de la impresora a la ip que le hemos dado.

## Instalacion por Android:Conectar por Bluetooth configurando solo en Android.
- Descargamos la app de Pos Utility de Htpr, disponible en su pagina web.
- Abrimos la app y conectamos a la impresora por bluetooth, normalmente la contraseña es 1234, si no imprimir ticket de configuración.
- Vamos a “Settings”, en el apartado “Port settings” vamos a Wifi. 
- La configuración es la siguiente: 
  - Wifi Model: STA
  - Hotspot name: escaneamos y conectamos la wifi del cliente.
  - Enable DHCP: Activado
  - Encryption mode: WPA2PSK
  - Hotspot password: Contraseña del wifi del cliente.
- Guardamos la configuración en la esquina superior derecha “Save”. Sonara la impresora.
- Reiniciamos la impresora y volvemos a conectarla por bluetooth.
-	Volvemos a la configuración del wifi, solo que ahora en IP ADD tendremos una ip fija de nuestra impresora.
-	Activamos JSPrintManager, vamos a camarero y añadimos la impresora por red, con la ip que aparece en la configuración.
- 🎥 **[Guía visual de instalación por android](https://youtu.be/nqBECMQXF9w)**




### Recursos y documentación:
- [Página oficial de HPRT T808](https://www.hprt.com/product/thermal-receipt-printer/t800)  
- [Drivers y utilidades (Windows, Android SDK, etc)](https://www.hprt.com/support/download-center)
- [Guía de instalación (PDF)](https://www.hprt.com/Uploads/202203/623c0ac7a812a.pdf)
- [SDK Android](https://www.hprt.com/support/sdk-center)

> ⚠️ *Importante: asegúrate de utilizar los drivers específicos de tu modelo de T808 (WiFi, Ethernet, USB) desde la web oficial para garantizar una instalación correcta.*

