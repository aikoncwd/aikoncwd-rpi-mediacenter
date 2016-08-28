# Centro multimedia Kodi+Recalbox

Ya que AikonCWD abandonó el centro multimedia para RPi1 decidí crear el mio propio con su idea y su contenido, a partir del proyecto de arranque dual Librelec(Kodi)+Recalbox(Emuladores), con la instalación a partir de NOOBS, el instalador oficial de Raspberry. He incluido la mayoría de add-ons que Aikon incluye en su centro multimedia, pero descartando los que pienso que no me harían falta a mi en el mío. Copio y pego parte de su README descartando lo no incluido.

Fuentes:

* http://www.matthuisman.nz
* https://github.com/aikoncwd/aikoncwd-rpi-mediacenter
* http://www.kodimania.com/

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
* SuperRepoh ttp://srp.nu
* TVAddons

# VIDEO

* Catoal -> Canales de TV en streaming, contenido nacional e internacional
* AdryanList -> Canales de TV en streaming, contenido nacional e internacional
* pelisalacarta -> El mejor addon para ver películas, con acceso a EliteTorrent, Divxatope, ...
* Quasar -> El mejor reproductor, visualiza contenido sin esperar a completar la descarga
* Plexus-Streams -> Reproductor de enlaces AceStream y SopCast, para contenido deportivo
* tvalacarta -> Acceso a todo el contenido de la TV bajo demanda (a la carta)
* PleXBMC -> Cliente de Plex para Kodi, gestiona y visualiza toda tu biblioteca Plex
* XBMCtorrent -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
* Torrenter -> Igual que Quasar, permite ver contenido torrent sin esperar a descargar
* YouTube -> Cliente para visualizar videos de Youtube, reproduce contenido VEVO también

# PROGRAMAS

* AddonInstaller -> Instalador gráfico de addons
* Recalbox -> Cierra Kodi y ejecuta RecalBox
* Maintenance Tool -> Varios tweaks para limpiar la cache y optimizar la memoria de Kodi
* Quasar Providers -> ExtraTorrent + KickAss + Magnetdl + ThePirateBay + TorrentZ + Yourbittorrent + 1333x
* Provider Manager -> Edita simultaneamente todos los providers de Quasar
* XBMC Library AutoUpdate -> Mantiene actualizada y limpia la biblioteca de Kodi

# MUSICA

*TuneIn Radio -> Acceso a cualquier radio online de todo el mundo, música en directo
*MP3 Streams -> Reproductor de musica en streaming, es un clon ruso de Spotify

# SUBTITULOS

* Addic7ed.com
* OpenSubtitles.org
* Subdivx.com
* Subtitulos.es

# LETRAS/LYRIC

* CU LRC Lyrics

# SCRAPERS

* The Movie atabase
* The TVDB

Los scrapers descargan automáticamente la información, portada, sinopsis, reparto, puntuaciones, .... de cualquier película o serie que visualicemos

# Más información

* Configuración personalizada en Castellano: Teclado, Zona Horaria, Layout y Subtítulos
* Ethernet con IP automática (DHCP)
* Protocolos SSH y SMB (Samba) habilitados (usuario = root / password = aikoncwd)
* Kodi con Skin Confluence
* Transmission tuneado para maximizar su velocidad de torrents
* Acceso por Zeroconf habilitado (para control remoto desde smartphone)
* Protocolo AirPlay deshabilitado (mejora rendimiento)
* Addon de ElTiempo deshabilitado (mejora rendimiento)
* Lector de noticias RSS deshabilitado (mejora rendimiento)
* Biblioteca compartida por UPnP deshabilitado (mejora rendimiento)
* Librería Python libtorrent instalada para acelerar streaming
* Librería librtmp actualizada

# 1. Habilitar Transmission con Docker

Editaremos el fichero /storage/Dockerfiles-master/arm/transmission/transmission.service. Identificar las líneas --volume que acaban en /downloads y /incomplete. En /incomplete es donde Transmission va descargando los ficheros y en /downloads donde los va a dejar al acabar. Por defecto cuelga de /storage, que como suele ser la SD donde se instala LibreElec, puede ser demasiado pequeña para esto. Si tenéis un disco conectado por USB, hay que indicar el directorio correcto. 

Por ejemplo:
--volume=/var/media/sda1/Torrents:/downloads

Para habilitar e iniciar el servicio:

* systemctl enable /storage/Dockerfiles-master/arm/transmission/transmission.service
* systemctl start transmission

La dirección es http://x.y.z.t:9091 (IP de la Rpi).
