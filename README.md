# Disclaimer
*Éste proyecto pretende explicar como configurar un centro multimedia (mediacenter) completo, una estación de juegos y un servidor de descargas. Todo en uno. __Queda prohibido cualquier uso orientado a piratear/robar contenido con derechos de autor/terceros sin expreso consentimiento.__ Éste proyecto está basado en un conjunto de software gratuito que se puede encontrar fácilmente en internet. Éste proyecto no tiene ningún fin lucrativo, su único fin es enseñar y educar sobre la configuración y uso de los distintos programas.*

# Introducción
Éste proyecto permite instalar en pocos minutos una imagen pre-configurada para **Raspberry 2** y **Raspberry 3** con las siguientes opciones:

- **Centro multimedia** usando *Kodi 16.1 Jarvis*
- **Centro de juegos y emuladores** usando *RetroPie 4.0*
- **Centro de juegos en streaming** usando *Moonlight 2.2.1*
- **Centro de descargas** usando *Transmission* y *PyLoad*
- **Estación de trabajo** con *XFCE* y navegador *Firefox*
- Reproductor de vídeos para **películas y series en streaming** (con subtítulos)
- Reproductor de **canales de TV a la carta y en streaming**
- Reproductor de **contenido multimedia deportivo** usando *AceStream* y *SopCast*
- Reproductor de **música, videoclips y radio online**
- Herramientas: *Cliente IRC, wavemon, tmux, crawl, y mucho más...*

# Materiales necesarios
- [**Raspberry Pi 3**](https://www.amazon.es/Raspberry-Modelo-GHz-Quad-core-Cortex-A53/dp/B01CD5VC92/ref=sr_1_1?ie=UTF8&qid=1469090832&sr=8-1&keywords=raspberry) - Quadcore 1200MHz @ 1Gb RAM
- Tarjeta **microSD SDHC** 6Gb, recomiendo [SanDisk SDSQXNE-032G-GN6AA](https://www.amazon.es/gp/product/B013CP5A0Y/ref=oh_aui_detailpage_o02_s00?ie=UTF8&psc=1)
- Cargador de corriente micro USB, **5V** y **3A**, recomiendo [éste modelo](https://www.amazon.es/Aukru-3000mA-Cargador-Adaptador-Raspberry/dp/B01566WOAG/ref=sr_1_13?ie=UTF8&qid=1469090832&sr=8-13&keywords=raspberry)
- **Caja** protectora, recomiendo [ésta caja con **ventilador**](https://www.amazon.es/TRIXES-transparente-ventilador-enfriamiento-Raspberry/dp/B01BKIQJD2/ref=sr_1_22?ie=UTF8&qid=1469090864&sr=8-22&keywords=raspberry)
- [Cable **HDMI** 2.0](https://www.amazon.es/AmazonBasics-Cable-velocidad-est%C3%A1ndar-reciente/dp/B014I8SSD0/ref=sr_1_1?s=electronics-accessories&ie=UTF8&qid=1469091932&sr=1-1&keywords=cable+hdmi)

# Materiales recomendados
- [Interruptor **USB**](http://www.ebay.es/itm/Switched-microUSB-extension-lead-Raspberry-Pi-etc-Power-Cable/171305347085?_trksid=p2047675.c100005.m1851&_trkparms=aid%3D222007%26algo%3DSIC.MBE%26ao%3D1%26asc%3D20140620091323%26meid%3Dd9ed3dfdcbda43208e646caa71adf5b5%26pid%3D100005%26rk%3D3%26rkt%3D6%26mehot%3Dpp%26sd%3D171411830547) para apagar la Raspberry
- Disipadores de [**cobre**](https://www.amazon.es/enfriamiento-disipador-t%C3%A9rmico-disipadores-Raspberry/dp/B00LSF9ZKW/ref=sr_1_64?ie=UTF8&qid=1469090886&sr=8-64&keywords=raspberry) o [aluminio](https://www.amazon.es/Aukru-Disipador-Raspberry-aluminio-unidades/dp/B00ILK6DMA/ref=sr_1_9?ie=UTF8&qid=1469090832&sr=8-9&keywords=raspberry)
- Teclado inalámbrico, recomiendo [Logitech **K400**](https://www.amazon.es/Logitech-K400-Plus-inal%C3%A1mbrico-incorporado/dp/B00XYTTEAQ/ref=sr_1_1?ie=UTF8&qid=1469090931&sr=8-1&keywords=logitech+k400)
- [Mando XBOX 360](https://www.amazon.es/Microsoft-Xbox-Common-Controller-Windows/dp/B004JU0JSK/ref=sr_1_5?ie=UTF8&qid=1469115260&sr=8-5&keywords=xbox+360) (**cable USB**)

Recomiendo hacer el montaje usando **cable de red ethernet**. Si no disponemos de conexión por cable en el salón, podemos realizar el montaje usando el **wifi** integrado de la Raspberry 3, pero no lo recomiendo ya que el streaming se podría cortar.

# Contenido del MediaCenter
**Mediacenter Kodi 16.1 Jarvis**, *compilación arm7*  
Válido **RaspberryPi 2** y **RaspberryPi 3**

**REPOSITORIOS**
- Kodi Addon Repo
- Popcornmix Repo
- Shanis Repo
- SuperRepo
- TVAddons

**PROGRAMAS**
- AddonInstaller -> Instalador gráfico de addons
- Desktop -> Cierra Kodi y ejecuta el escritorio XCFE
- Emulationstation -> Cierra Kodi y ejecuta Retropie (Emulationstation)
- Wifi Config -> Cierra Kodi y permite configurar el Wifi y el Bluetooth
- Maintenance Tool -> Varios tweaks para limpiar la cache y optimizar la memoria de Kodi
- Quasar Providers -> ExtraTorrent + KickAss + Magnetdl + ThePirateBay + TorrentZ + Yourbittorrent + 1333x
- Provider Manager -> Edita simultaneamente todos los providers de Quasar
- XBMC Library AutoUpdate -> Mantiene actualizada y limpia la biblioteca de Kodi

**MUSICA**
- TuneIn Radio -> Acceso a cualquier radio online de todo el mundo, música en directo
- MP3 Streams -> Reproductor de musica en streaming, es un clon ruso de Spotify

**VIDEO**
- Catoal -> Canales de TV en streaming, contenido nacional e internacional
- AdryanList -> Canales de TV en streaming, contenido nacional e internacional
- pelisalacarta -> El mejor addon para ver películas, con acceso a EliteTorrent, Divxatope, ...
- Quasar -> El mejor reproductor, visualiza contenido sin esperar a completar la descarga
- Plexus-Streams -> Reproductor de enlaces AceStream y SopCast, para contenido deportivo
- tvalacarta -> Acceso a todo el contenido de la TV bajo demanda (a la carta)
- PleXBMC -> Cliente de Plex para Kodi, gestiona y visualiza toda tu biblioteca Plex
- XBMCtorrent -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
- Torrenter -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
- YouTube -> Cliente para visualizar videos de Youtube, reproduce contenido VEVO también

**SCRAPERS**
- The Movie atabase
- The TVDB
Los scrapers descargan automáticamente la información, portada, sinopsis, reparto, puntuaciones, .... de cualquier película o serie que visualicemos

**SUBTITULOS**
- Addic7ed.com
- OpenSubtitles.org
- Subdivx.com
- TuSubtitulo

**LETRAS/LYRIC**
- CU LRC Lyrics

# Más información
- Viene todo preconfigurado para **enchufar y usar**
- Configuración personalizada en **Castellano**: Teclado, Zona Horaria, Layout y Subtítulos
- Ethernet con **IP automática** (DHCP)
- Protocolos **SSH** y **SMB** (Samba) habilitados (usuario = **root** / password = **aikoncwd**)
- Kodi con Skin **Confluence**
- Transmission tuneado para **maximizar su velocidad de torrents**
- Acceso por **Zeroconf** habilitado (para control remoto desde smartphone)
- Protocolo **AirPlay** deshabilitado (mejora rendimiento)
- Addon de **ElTiempo** deshabilitado (mejora rendimiento)
- Lector de noticias **RSS** deshabilitado (mejora rendimiento)
- Biblioteca compartida por **UPnP** deshabilitado (mejora rendimiento)
- Librería Python **libtorrent** instalada para acelerar streaming
- Librería **librtmp** actualizada

---

# PASO 1: Instalación
1. Descargar la imágen preconfigurada [**Mediacenter-AikonCWD-v6.img**](https://github.com/aikoncwd/aikoncwd-rpi-mediacenter/raw/master/Mediacenter-AikonCWD-v6.torrent)
2. Grabar la imagen en tu tarjeta **microSD**:
  - **Windows**: Utilizar el programa [win32diskimager](https://sourceforge.net/projects/win32diskimager/)
  - **Linux/Mac**: `sudo dd if=/path/Mediacenter-AikonCWD-v6.img of=/dev/mmcblk0 bs=4M`
3. Introduce tu **microSD** con la imagen grabada en tu Raspberry
4. Enchufa el **cable de alimentación**
5. La Raspberry se encenderá, aparecerá la imágen inicial de *garlic-dog*
6. La Raspberry se **reiniciará automáticamente**, volverás a ver la imagen inicial de *garlic-dog*
7. El mediacenter **Kodi** arrancará automáticamente
8. Pulsamos el botón situado en la *esquina inferior izquierda*, seleccionamos **salir** para cerrar **Kodi**
9. Verificar que la partición ocupa el **100% de tu microSD** con el comando `df -h` (opcional)

Tras salir de Kodi estaremos en la **consola**, si en lugar de la consola vemos el fondo totalmente negro es posible que haya saltado el salvapantallas, pulsa una tecla en tu teclado y la consola aparecerá de nuevo.

# PASO 2: Configurar IP Estática
1. Editamos el fichero de configuración con el comando `nano /etc/dhcpcd.conf`
2. Quitamos el comentario (**#**) que hay al principio de cada línea:
```
interface eth0
static ip_address=192.168.1.100/24
static routers=192.168.1.1
static domain_name_servers=8.8.8.8
```
Puede que el router de tu casa tenga otra dirección (por ejemplo **192.168.0.1**), personaliza éste fichero para adaptarlo según el caso. Si tienes intención de utilizar el **wifi**, repite los mismos pasos aplicándo a la sección **interface wlan0**

Una vez finalizado, guarda los cambios en el fichero, para ello pulsa: <kbd>CTRL</kbd>+<kbd>X</kbd>, luego <kbd>Y</kbd> y finalmente <kbd>Intro</kbd>.

#PASO 3: Cambiar el password de root
El usuario por defecto de ésta imagen es **root**, la contraseña original es **aikoncwd**. Recomiendo encarecidamente que cambies ese password, para ello escribe el comando `passwd root`, a continuación escribe tu nuevo password 2 veces. Recuerda que éste usuario/password lo utilizarás para acceder a la Raspberry por **SSH** o **sFTP** (FileZilla), también lo usarás si pretendes controlar Kodi desde tu **smartphone**, etc...

#PASO 4: Configurar Transmission (opcional)
**Transmission** es un programa que permite transformar tu Raspberry en un servidor de descargas **BitTorrent**. El daemon de transmission está instalado y configurado, pero **se encuentra deshabilitado por defecto** ya que no todos los usuarios necesitan utilizarlo. Si quieres habilitar y utilizar transmission... sigue leyendo:

Primero de todo vamos a configurar el daemon para que se auto-ejecute al encender la **Raspberry**. Edita el fichero de auto-arranque con el comando:

    nano /etc/rc.local

El fichero tiene comentarios, básicamente tienes que localizar y eliminar la línea `service transmission-daemon stop`. Pulsando <kbd>CTRL</kbd>+<kbd>K</kbd> borrarás la línea actual. Salva los cambios en el fichero `/etc/rc.local` pulsando las teclas: <kbd>CTRL</kbd>+<kbd>X</kbd>, luego <kbd>Y</kbd> y finalmente <kbd>Intro</kbd>.

Asegurate que el **daemon** de transmission está **detenido**, ejecuta los siguientes commandos:

    service transmission-daemon stop
    /etc/init.d/transmission-daemon stop

Edita el fichero de **configuación**:

    nano /root/.config/transmission-daemon/settings.json

Los campos importantes a modificar son:

| Campo | Significado |
|---|---|
| "download-dir": "/root/Downloads", | Ruta de descarga por defecto |
| "rpc-authentication-required": true, | Proteger acceso a tranmission con password |
| "rpc-password": "root", | Password para acceder a transmission |
| "rpc-username": "root", | Usuario para acceder a transmission |

Salva los cambios en el fichero `settings.json` pulsando las teclas: <kbd>CTRL</kbd>+<kbd>X</kbd>, luego <kbd>Y</kbd> y finalmente <kbd>Intro</kbd>. Activa el daemon **manualmente** con el comando:

    service transmission-daemon start

El daemon de Transmission estará activo en el **puerto 9091**, con usuario y password **root**. Podrás comprobar el daemon si accedes a través de un explorador web a la dirección http://ip_raspberry:9091, por ejemplo **http://192.168.1.100:9091** Pulsamos el botón de configuración *llave inglesa* para editar las preferencias. La configuración de descargas está configurado para ser lo más óptima posible. Encontrarás agregada una URL de **ip-block** para mejorar la descarga de ficheros torrents en transmission. Puedes controlar transmission desde tu smartphone, hay una [app](https://play.google.com/store/apps/details?id=com.neogb.rtac&hl=es) para ello (también en iOS). 

#PASO 5: Configurar PyLoad (opcional)
**PyLoad** es un programa que permite transformar tu Raspberry en un servidor de **descargas directas**. El daemon de PyLoad está instalado y configurado, pero **se encuentra deshabilitado por defecto** ya que no todos los usuarios necesitan utilizarlo. Si quieres habilitar y utilizar PyLoad... sigue leyendo:

Primero de todo vamos a configurar el daemon para que se auto-ejecute al encender la **Raspberry**. Edita el fichero de auto-arranque **cron** con el comando:

    crontab -e

Nos situamos en la parte inferior, localiza la línea `#@reboot pyLoadCore -daemon` y quita el **comentario** del principio, deberá quedar asi: `@reboot pyLoadCore --daemon` (**tienes que poner los 2 guiones delante de la palabra daemon**). Salva los cambios pulsando las teclas: <kbd>CTRL</kbd>+<kbd>X</kbd>, luego <kbd>Y</kbd> y finalmente <kbd>Intro</kbd>

Tendrás que reiniciar tu Raspberry para tener el daemon de pyLoad en ejecución, recuerda que Kodi se enciende automáticamente, deberás cerrarlo para volver a la consola.

Accedemos a PyLoad a través de un explorador web usando el **puerto 8000**, por ejemplo: **http://192.168.1.100:8000**  
El usuario por defecto es **root** y password **root**. En el menu superior puedes *administrar* el usuario y cambiar el password (recomendado), justo abajo encontrarás la *configuración* donde podrás editar la configuración, los plugins de captchas etc... y añadir cualquier cuenta premium que poseas de los diferentes hosts.

![](http://i.imgur.com/o8A62oq.png)

# Acceder por Samba (SMB)
El servicio samba está habilitado por defecto, se han compartido las principales carpetas para que puedas acceder desde cualquier equipo de tu red:

![](http://i.imgur.com/esv0wx3.png)

Para ello simplemente escribe la dirección \\\\MEDIACENTER-V6 o \\\\192.168.1.100 (la IP de tu Raspberry). Desde aquí podrás transferir ficheros y configuraciones, así como roms de juegos para RetroPie

# Recomendaciones
- Configura una **IP manual** a tu Raspberry
- Abre el puerto **51413** para aumentar la velocidad de **Transmission** (torrents)
- Abre el puerto **9091** para administrar **Transmission** desde fuera de casa, establece un password!
- Abre el puerto **8000** para administrar **PyLoad** desde fuera de casa, establece un password!
- Abre el puerto **6881** para aumentar la velocidad de **Torrenter**
- Abre los puertos **6889 hasta 7000** para aumentar la velocidad de **Quasar**
- Abre los puertos **62062, 9000 y 9001** para aumentar la velocidad de **Plexus-Streams**

Todos esos puertos deberás abrirlos en tu router (NAT). Otra opción más sencilla sería configurar DMZ contra la ip fija de tu raspberry:

![](http://i.imgur.com/WqyCmzC.png)

Puedes controlar remotamente Kodi usando el mando de tu TV (siempre y cuando sea CEC compatible). Si tu TV no es CEC, puedes descargar una [app para tu smartphone](https://itunes.apple.com/es/app/official-kodi-remote/id520480364?mt=8):

![](http://i.imgur.com/Or9Ofnx.png)

# Pelisalacarta: Visualizar pelísculas en streaming
Dentro de Kodi dispones del addon pelisalacarta (en versión UI o normal). Te recomiendo que explores por canales, a veces el buscador va algo lento. Mi provider favorito es EliteTorrent (puedes utilizar el que quieras), selecciona una película, pulsa `Ver el vídeo magnet: [torrent]`:

![]()

Dispondrás de 5 servicios para descargar y visualizar el torrent. Mi favorito es Quasar y XBMCtorrent, a cada usuario le funciona mejor uno u otro, usa el que más te guste. Ésta nueva versión incluye 2 clientes internos basados en libtorrent, yo los he probado y no me han funcionado demasiado bien.

# Jugar con los emuladores (RetroPie)
*Primero de todo necesitarás copiar alguna rom para jugar, la carpeta por defecto es `/root/RetroPie/roms/`, si no copias ninguna rom, no te aparecerán los emuladores para jugar!*

Desde el menu de Kodi puedes ejecutar Emulationstation (el menu de RetroPie) para jugar a juegos y emuladores. Si estás en la consola puedes escribir el comando `emulationstation` directamente. La primera vez que accedas te detectará el controlador/joystick que tengas (o el teclado USB), sigue el tutorial para configurar los botones.

![](https://cloud.githubusercontent.com/assets/10035308/7110173/0f2ea784-e16a-11e4-9c6f-5fe7c594b05a.png)
![](http://i.imgur.com/Dx3Tqw7.jpg)

Una vez dentro tendrás un menú con 2 sistemas (Steam + RetroPie) y tantos emuladores como roms diferentes hayas copiado. Tienes que copiar las roms antes de ejecutar emulationstation para que las detecte correctamente.

![](http://i.imgur.com/j9ruih6.jpg)

Por defecto las roms no vienen identificadas, tendrás que scrapear la información. Pulsamos start y seleccionamos el menu de scraper. Automáticamente buscará cada rom en internet y nos preguntará que información queremos usar en cada rom, tras finalizar el aspecto de nuestro emulador de SuperNintendo será más profesional:

![](http://i.imgur.com/94JhBUL.jpg)

El uso de los emuladores es fácil e intuitivo. A continuación os dejo un par de resumenes para que aprendáis las combinaciones de teclas. Para salir de un juego hay que pulsar Start+Select a la vez.

![](http://i.imgur.com/I6XZ19a.png)

Desde el menú RetroPie podrás cambiar todas las configuraciones de los emuladores. Desde el menú Steam podrás ejecutar juegos en streaming desde tu PC/Steam (lo explicaré más adelante).

# Juegos de PC STEAM (Moonlight)
Seguimos con los juegos, ahora toca hablar de Moonlight. Si tienes la suerte de tener un PC con una tarjeta gráfica de la serie NVIDIA 600 (o superior) podrás juegas a los juegos de tu PC directamente en tu Raspberry! Toda tu biblioteca de Steam y cualquier otro juego que tengas fuera de Steam podrá ser jugado en tu salón desde la Raspberry, empecemos:

Instala NVIDIA GeForce Experience 2.11.4.0  
Asegurate que tu GFE está capacitado para el protocolo SHIELD (es el streaming). Entra en la configuración y añade cualquier ruta adicional para indicar a tu GFE donde guardas los juegos, yo lo tengo así:

![](http://i.imgur.com/VVfVSHC.png)

Ahora vuelve a tu RPi y desde consola empareja tu RPi con GFE, usa el siguiente comando:

    moonlight pair

Se generará un certificado y un código numérico de 4 cifras, ve a tu PC y añade el codigo en el recuadro correspondiente:

![](http://i.imgur.com/DYmlxn8.png)

Vuelve a tu RPi y la verás correctamente emparejada, ahora puedes listar los juegos que tienes instalados, usa el comando:

    moonlight list
    
![]()

Antes de lanzarte a jugar, es recomendable que configures tu joystick. Algunos juegos no serán compatibles con un mando y requieren de Teclado y ratón. En esos juegos puedes lanzar el stream directamente pues el teclado y ratón no requieren ninguna configuración previa. Para configurar nuestro mando de XBOX 360 usb lanzaremos el siguiente comando:

    moonlight map /root/xbox.map

![]()

Completa las indicaciones al pie de la letra y tendrás tu mando correctamente configurado. Ahora ya podemos lanzar moonlight usando nuestro "mapping" personalizado del mando, la sintaxis sería:

    moonlight stream -mapping /root/xbox.map

![](http://i.imgur.com/mlv2u6y.jpg)

Disponemos de varios parametros para personalizar moonlight, por ejemplo podemos arrancar a 30fps o 60fps, 720 o 1080, etc... Si queremos lanzar un juego que tenemos en el listado pero no en Steam haremos lo siguiente:

    moonlight stream -mapping /root/xbox.map -app "League of Legends"

Para evitar introducir comandos, encontrarás un emulador llamado Steam dentro de RetroPie/Emulationstation, dicho emulador tiene 4 scripts para lanzar Steam con resolución 720, 1080, 30fps o 60fps. Los scripts funcionan tal cual, pero si has creado un fichero *.map para tu controlador/joystick sería bueno que edites los 4 ficheros y añadas al final el texto `-mapping /root/xbox.map`

Los 4 ficheros están en la ruta `/root/RetroPie/roms/moonlight`, puedes editarlos desde la consola de la Raspberry, por SSH/Putty o accediendo por samba: \\\\192.168.1.100\\roms\\moonlight o \\\\MEDIACENTER-V6\\roms\\moonlight  
Añade al final el comando -mapping y la ruta del *.map, a mi me ha quedado así:

    moonlight stream -1080 -60fps -app Steam -mapping /root/xbox.map

Haz lo mismo para los 4 ficheros. Por último ejecuta el siguiente coamdno para dar permisos:

    chmod +x /root/RetroPie/roms/moonlight/*

El resultado es impecable:

![](http://i.imgur.com/xISo1l6.jpg)
![](http://i.imgur.com/I8nBbDp.jpg)
![](http://i.imgur.com/NI09B6p.jpg)
![](http://i.imgur.com/uGeJZil.jpg)

# PASO 0: Overclocking
Recomiendo habilitar un poco de overclock, conseguirás más fluidez al moverte por los menús de Kodi y potenciarás notablemente el rendimiento a la hora de jugar a emuladores. Tu CPU podrá realizar cálculos más rápidos y el acceso a la memoria ram o al disco microSD tendrán tiempos de respuesta más bajos.  
Recomiendo encarecidamente que utilices algún método de ventilación/refrigeración para evitar alcanzar los 85ºC, ya que la RPi bajará su velocidad si alcanza esa temperatura

Si quieres puedes ejecutar un benchmark (diagnóstico) para testear tu nivel de overclock, ejecuta el siguiente comando:

    curl https://raw.githubusercontent.com/aikoncwd/rpi-benchmark/master/rpi-benchmark.sh | sudo bash

### Raspberry Pi 3: Overclock settings

Edita tu fichero `/boot/config.txt` y pega el siguiente código, puedes ajustar los valores para tener más o menos overclock:

```
force_turbo=0                   #Enable cpu-overclock over 1300MHz (default 0)
avoid_pwm_pll=1                 #Enable no-relative freq between cpu and gpu cores (default 0)

arm_freq=1300                   #Frequency of ARM processor core in MHz (default 1200)
core_freq=550                   #Frequency of GPU processor core in MHz (default 400)
over_voltage=6                  #ARM/GPU voltage adjust, values over 6 voids warranty (default 0)

sdram_freq=575                  #Frequency of SDRAM in MHz (default 450)
sdram_schmoo=0x02000020         #Set SDRAM schmoo to get more than 500MHz freq (default unset)
over_voltage_sdram_p=6          #SDRAM phy voltage adjust (default 0)
over_voltage_sdram_i=4          #SDRAM I/O voltage adjust (default 0)
over_voltage_sdram_c=4          #SDRAM controller voltage adjust (default 0)

gpu_mem=256                     #GPU memory in MB. Memory split between ARM and GPU (default 64?)
gpu_freq=550                    #Sets core_freq h264_freq isp_freq v3d_freq together (default 300)
v3d_freq=500                    #Frequency of 3D block in MHz (default ?)
h264_freq=350                   #Frequency of hardware video block in MHz (default ?)

dtparam=sd_overclock=75         #Clock in MHz to use for MMC micrSD (default 50)
dtparam=audio=on                #Enables the onboard ALSA audio (always use this ON)
dtparam=spi=on                  #Enables the SPI interfaces (default OFF)

temp_limit=80                   #Overheat protection. Disable overclock if SoC reaches this temp
initial_turbo=60                #Enables turbo mode from boot for the given value in seconds

hdmi_drive=2                    #Normal HDMI mode. Sound will be sent if supported and enabled (default 2)
hdmi_ignore_cec_init=1          #Avoids bringing TV out of standby and channel switch when booting (default 0)
hdmi_ignore_cec=0               #Pretends CEC is not supported. No CEC functions will be supported (default 0)
hdmi_force_hotplug=1            #Pretends HDMI hotplug signal is asserted (default 0)

start_x=1                       #Enable software decoding (MPEG-2, VC-1, VP6, VP8, Theora, etc. default 0)
overscan_scale=1                #Video Output will respect the overscan settings (default 1)
disable_overscan=0              #Disable overscan configuration. Set 1 if you see black lines on TV (default 0)
disable_splash=1                #Avoids the rainbow splash screen on boot (default 0)
avoid_warnings=1                #Disable warnings (Red=over-temperature ; Rainbow=under-voltage). (default 0)

gpu_mem_256=128
gpu_mem_512=256
gpu_mem_1024=256
```
Lee bien los comandos, es posible que te interese modificar algunos para personalizar tu imagen.

### Raspberry Pi 2: Overclock settings

Edita tu fichero `/boot/config.txt` y pega el siguiente código, puedes ajustar los valores para tener más o menos overclock:

    gpu_mem=256
    gpu_mem_256=128
    gpu_mem_512=256
    gpu_mem_1024=256
    
    arm_freq=1100
    core_freq=550
    sdram_freq=483
    over_voltage=6
    over_voltage_sdram=2
    temp_limit=70
    force_turbo=0
    initial_turbo=60
    
    hdmi_drive=2
    hdmi_ignore_cec=0
    hdmi_ignore_cec_init=1
    hdmi_ignore_hotplug=0
    hdmi_force_hotplug=1
    
    #disable_overscan=0
    #overscan_scale=1
    
    #overscan_left=49
    #overscan_right=49
    #overscan_top=29
    #overscan_bottom=25
    
    max_usb_current=1
    dtparam=audio=on
    dtparam=spi=on

Encontrarás un script llamado bcmstat que permite medir con exactitud el estado del hardware de tu Raspberry, podrás ver a que velocidad va tu CPU y a que temperatura está, para ello ejecuta:

    /root/bcmstat.sh

![](http://imgur.com/o8I3dXw.png)

# Estación de trabajo: XFCE Desktop
Ésta imagen incluye un escritorio muy muy ligero pero funcional al 100%, se ha cuidado una estética minimalista. En el menú superior podrás encontrar software variado organizado por categorías. La consola (terminal) arranca con tmux por defecto, podrás partir tu área de trabajo y ejecutar diferentes aplicaciones a la vez, aquí os dejo un ejemplo con un cliente IRC (irssi), un juego dungeon crawler (crawl) y el reloj:

![]()

El programa principal del desktop es Firefox, el conocido navegador web disponible ahora en tu Raspberry. Con soporte HTML5 y compatible con Youtube:

![]()

# Software para la consola
La imagen incluye una pequeña selección personal de herramientas y utilidades para la consola:
- tmux: Multiplexor de terminales, permite dividir la consola
- irssi: Cliente IRC en consola
- crawl: Juego tipo dungeon crawler para la consola
- htop: Process Manager, para gestionar procesos y recursos
- wavemon: Monitor de redes wifi, gráficos de señal, etc...

# Cosas que me falta escribir:
- Plex
- Hyperion
