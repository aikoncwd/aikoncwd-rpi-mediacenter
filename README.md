
# Disclaimer

*Este proyecto pretende explicar como configurar un centro multimedia (mediacenter) completo, una estación de juegos y un servidor de descargas. Todo en uno. __Queda prohibido cualquier uso orientado a piratear/robar contenido con derechos de autor/terceros sin expreso consentimiento.__ Éste proyecto está basado en un conjunto de software gratuito que se puede encontrar fácilmente en internet. Éste proyecto no tiene ningún fin lucrativo, su único fin es enseñar y educar sobre la configuración y uso de los distintos programas.*

# Centro multimedia Kodi+Recalbox

Ya que **AikonCWD** abandonó el centro multimedia para RPi1 decidí crear el mio propio con su idea y su contenido, a partir del proyecto de arranque dual Librelec(Kodi)+Recalbox(Emuladores), con la instalación a partir de NOOBS, el instalador oficial de Raspberry. He incluido la mayoría de add-ons que *AikonCWD* incluye en su centro multimedia, pero descartando los que pienso que no me harían falta a mi en el mío. Copio y pego  su README descartando lo no incluido y añadiendo lo nuevo.

Fuentes:

* http://www.matthuisman.nz
* https://github.com/aikoncwd/aikoncwd-rpi-mediacenter
* http://www.kodimania.com/index.php?topic=7650.0


Descarga: https://mega.nz/#!rpUnSDzL!vfiMDYrP62-gL46Rce2YTcDzu_fKwO_qzgv9mfUkCws


Los contenidos del centro multimedia de momento son:

Raspberry 1:

* Centro multimedia usando Libreelec con Kodi Jarvis 16.1
* Centro de juegos y emuladores usando Recalbox 4.0.0 Beta5
* Centro de descargas usando Transmission y PyLoad
* Reproductor de vídeos para películas y series en streaming (con subtítulos)
* Reproductor de canales de TV a la carta y en streaming
* Reproductor de contenido multimedia deportivo usando AceStream y SopCast
* Reproductor de música, videoclips y radio online


Contenido del MediaCenter

* Mediacenter Kodi 16.1 Jarvis, compilación ARM
* *Válido RaspberryPi 1 (de momento)*

# REPOSITORIOS

* Kodi Addon Repo
* Popcornmix Repo
* Shanis Repo
* SuperRepo
* TVAddons

# VIDEO

* Catoal 5.3.5 Especial Edición-> Canales de TV en streaming, contenido nacional e internacional
* La Liga -> Stream de los partidos de la liga española.
* AdryanList -> Canales de TV en streaming, contenido nacional e internacional
* pelisalacarta -> El mejor addon para ver películas, con acceso a EliteTorrent, Divxatope, ...
* Quasar -> El mejor reproductor, visualiza contenido sin esperar a completar la descarga
* Plexus-Streams -> Reproductor de enlaces AceStream y SopCast, para contenido deportivo
* tvalacarta -> Acceso a todo el contenido de la TV bajo demanda (a la carta)
* PleXBMC -> Cliente de Plex para Kodi, gestiona y visualiza toda tu biblioteca Plex
* XBMCtorrent -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
* Torrenter -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
* YouTube -> Cliente para visualizar videos de Youtube.
* Vevo - > Plugins para videos musicales.
* Sportsdevil -> Streaming de programas deportivos

# PROGRAMAS

* AddonInstaller -> Instalador gráfico de addons
* Recalbox -> Cierra Kodi y ejecuta RecalBox
* Maintenance Tool -> Varios tweaks para limpiar la cache y optimizar la memoria de Kodi
* Quasar Providers -> ExtraTorrent + KickAss + Magnetdl + ThePirateBay + TorrentZ + Yourbittorrent + 1333x
* Provider Manager -> Edita simultaneamente todos los providers de Quasar
* XBMC Library AutoUpdate -> Mantiene actualizada y limpia la biblioteca de Kodi
* Backup -> Haz tu backup de la configuración de Kodi.
* OpenELEC Config -> Frontend para configurar config.txt sin consola.
* Transmission Addon -> para controlar las descargas desde Kodi.
* Unrar Plugin

# MUSICA

* TuneIn Radio -> Acceso a cualquier radio online de todo el mundo, música en directo
* MP3 Streams -> Reproductor de musica en streaming, es un clon ruso de Spotify

# SUBTITULOS

* Addic7ed.com
* OpenSubtitles.org
* Subdivx.com
* Subtitulos.es

# LETRAS/LYRIC

* CU LRC Lyrics

# SCRAPERS

* The Movie Database
* The TVDB

Los scrapers descargan automáticamente la información, portada, sinopsis, reparto, puntuaciones, .... de cualquier película o serie que visualicemos

# Más información

* Configuración personalizada en Castellano: Teclado, Zona Horaria, Layout y Subtítulos
* Ethernet con IP automática (DHCP)
* Protocolos SSH y SMB (Samba) habilitados (usuario = root / password = libreelec)
* Kodi con Skin Confluence
* Acceso por Zeroconf habilitado (para control remoto desde smartphone)
* Protocolo AirPlay deshabilitado (mejora rendimiento)
* Addon de ElTiempo deshabilitado (mejora rendimiento)
* Lector de noticias RSS deshabilitado (mejora rendimiento)
* Biblioteca compartida por UPnP deshabilitado (mejora rendimiento)
* Librería Python libtorrent instalada para acelerar streaming

# 1. INSTALACIÓN

Para hacerlo desde windows:

* Instala el SD Card Formater https://www.sdcard.org/downloads/formatter_4/
* Formatea la SD con la opción FORMAT SIZE ADJUSTEMENT=ON
* Descarga el rar y descomprímelo
* Copía el contenido del rar en la raíz de la tarjeta SD
* Introduce la SD en la Rpi apagada y arráncala
* Arrancará el instalador NOOBS
* Te saldrán dos sistemas operativos o varios, según tengas o no conectada la PI a internet. Selecciona los SO: RecalBoxOS-LibreElec y RecalboxOS-rpi1.
* Ahora a esperar que acabe y selecciona el SO desde el cual quieres arrancar primero.

Por defecto arrancará desde Kodi, para cambiar esto
* Saca la SD y metela en tu PC con windows.
* Abre el archivo autoboot.txt y cambia el número de partición
* Para arrancar desde NOOBS, boot_partition=0
* Para arrancar desde KODI, boot_partition=6    (Default)
* Para arrancar desde Recalbox, boot_partition=8

# 2. Espacio en la SD

He configurado las particiones de LibreELEC y Recalbox para que se autoexpandan, por lo que ocuparan la mitad de la SD cada uno.

Si quieres configurarlo de otra manera edita /os/nombre_os/partitions.json y cambia "want_maximised" a false en la partición EXT4 que no quieras que se expanda. Por otra parte puedes configurar manualmente el espacio que ocupe con "partition_size_nominal" en MB.
Para cambiar esto tendrás que reinstalarlo todo otra vez una vez instalado.

# 3. Habilitar Transmission con Docker

Editaremos el fichero /storage/Dockerfiles-master/arm/transmission/transmission.service. Identificar las líneas --volume que acaban en /downloads y /incomplete. En /incomplete es donde Transmission va descargando los ficheros y en /downloads donde los va a dejar al acabar. Por defecto cuelga de /storage, que como suele ser la SD donde se instala LibreElec, puede ser demasiado pequeña para esto. Si tenéis un disco conectado por USB, hay que indicar el directorio correcto. 

Por ejemplo:
--volume=/var/media/sda1/Torrents:/downloads

Para habilitar e iniciar el servicio:

* systemctl enable /storage/Dockerfiles-master/arm/transmission/transmission.service
* systemctl start transmission

La dirección es http://x.y.z.t:9091 (IP de la Rpi).
