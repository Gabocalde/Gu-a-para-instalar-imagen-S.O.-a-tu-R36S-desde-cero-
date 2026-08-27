# Guia-para-instalar-imagen-S.O.-a-tu-R36S-desde-cero-
instalar ArkOS en una microSD nueva para una R36S, arrancar la consola correctamente y después pasar tus ROMs, BIOS y partidas guardadas.  Esta guía está pensada especialmente para quienes quieren dejar de usar la microSD original de la R36S y hacer una instalación limpia en una tarjeta nueva.
Antes de empezar

Necesitas:

Una R36S.
Una microSD nueva o una tarjeta de buena calidad. En esta guía se utiliza una de 64 GB.
Un PC con Windows.
Un lector/adaptador de microSD.
La microSD original de la R36S solamente para recuperar tus juegos y archivos.
Una segunda microSD donde instalarás ArkOS.

MUY IMPORTANTE

No hagas la instalación sobre la microSD original si todavía no tienes una copia de seguridad.

La tarjeta original puede contener:

ROMs
BIOS
partidas guardadas
configuraciones
archivos del emulador

Lo recomendable es conservar la tarjeta original intacta mientras preparas la nueva.

1. Haz primero una copia de seguridad

La primera dificultad que puede aparecer es que Windows no siempre muestra todas las carpetas de la microSD de la R36S.

La R36S utiliza particiones que pueden ser legibles en Linux pero no necesariamente visibles de la misma manera en Windows.

Por ejemplo, en Linux puedes encontrarte con carpetas como:

roms
bios
saves
backup
savestates

Mientras que en Windows puede que solamente aparezca una partición de arranque.

¿Qué hacer?

Si Windows no muestra tus ROMs, utiliza Linux para hacer la copia de seguridad.

Guarda al menos:

roms
bios
saves / save
backup
savestates

Si tienes suficiente espacio, es todavía mejor conservar una copia completa de la partición de datos que Linux pueda leer.

Consejo

No borres nada de la tarjeta original.

La microSD original debe quedarse como respaldo hasta que hayas comprobado que todo funciona en la nueva.

2. Descarga la imagen de ArkOS para R36S

Para R33S/R35S/R36S/R36H existe una imagen MultiPanel de ArkOS. El repositorio comunitario de ArkOS identifica la versión ArkOS R3XS V2.0 (11072025) como la versión archivada más reciente para estos dispositivos.

Nota de actualidad: ese repositorio indica que ArkOS dejó de mantenerse y que el proyecto ha sido reemplazado por dArkOS. Esta guía documenta la instalación de ArkOS porque es el sistema utilizado en este procedimiento.

La imagen puede venir comprimida como:

.img.xz

Por ejemplo:

ArkOS_R35S-R36S_v2.0_11072025_MultiPanel.img.xz
 https://www.mediafire.com/file/i672xysm7j62kde/ArkOS_R35S-R36S_v2.0_11072025_MultiPanel.img.xz/file

 3. Instala 7-Zip

Si la imagen termina en:

.img.xz

hay que descomprimirla antes de grabarla.

Instala 7-Zip en Windows y utiliza:

Clic derecho
→ 7-Zip
→ Extraer aquí

Al terminar debes tener un archivo parecido a:

ArkOS_R35S-R36S_v2.0_11072025_MultiPanel.img

Ese archivo .img será el que grabaremos en la microSD.

4. Instala Rufus

Para esta instalación puedes utilizar Rufus para escribir la imagen en la microSD.

Descarga Rufus desde su página oficial:

https://rufus.ie/

Rufus puede utilizarse directamente desde el ejecutable en Windows
5. Introduce la microSD NUEVA

Introduce la microSD nueva de 64 GB en el PC.

En Rufus debería aparecer algo parecido a:

NO_LABEL (64 GB)

Esto es normal si la tarjeta está nueva y no tiene nombre.

----CUIDADO-----

Comprueba muy bien la capacidad.

Si tu microSD es de 64 GB, Rufus debería mostrar aproximadamente esa capacidad.

No selecciones por error el disco interno de Windows
6. Graba ArkOS con Rufus

Abre Rufus.

En Dispositivo, selecciona:

NO_LABEL (64 GB)

En Selección de arranque, pulsa:

SELECCIONAR

y selecciona:

ArkOS_R35S-R36S_v2.0_11072025_MultiPanel.img

Después pulsa:

EMPEZAR

Rufus mostrará advertencias porque la tarjeta será sobrescrita.

Acepta solamente si has comprobado que estás usando la microSD nueva.

No te asustes después de terminar

Una vez finalizado, Rufus puede volver a mostrar la pantalla inicial.

Eso no significa que tengas que pulsar "Empezar" otra vez.

Después de grabar la imagen es normal que Windows reconozca una partición llamada algo como:

BOOT

y que puedas ver archivos de ArkOS dentro.

7. Expulsa la microSD

Cuando Rufus termine:

Cierra Rufus.
Expulsa la microSD desde Windows.
Retírala correctamente del PC.

No retires la tarjeta mientras todavía esté escribiéndose.

8. Primer arranque de la R36S

Asegúrate de que la consola esté apagada.

Introduce la microSD nueva en la R36S.

Enciéndela.

Si todo salió correctamente deberías ver:

ArkOS

y después una serie de mensajes de instalación/configuración.

 MUY IMPORTANTE

El primer arranque puede tardar bastante.

La documentación de la imagen MultiPanel indica que el primer arranque puede tardar hasta unos 10 minutos porque el sistema está realizando su configuración inicial.

Durante ese proceso:

No retires la microSD.
No apagues la consola.
No intentes cambiar el panel de pantalla inmediatamente.

Espera a que termine.
9. Si la pantalla funciona, no cambies el DTB

Una de las ventajas de la imagen MultiPanel es que está preparada para diferentes paneles de pantalla de las R36S.

La documentación incluye un Panel Picker Mode para seleccionar diferentes paneles.

Si tu pantalla funciona correctamente

No necesitas cambiar archivos .dtb.

En nuestro caso, la consola arrancó correctamente y la pantalla funcionó, por lo que no fue necesario tocar ningún DTB.

Si la pantalla queda negra

No empieces a reemplazar archivos al azar.

La imagen MultiPanel ofrece un modo de selección de panel.

10. Comprueba que ArkOS funciona antes de copiar juegos

Una vez que llegues al menú principal, comprueba:

Pantalla
Botones
Cruceta
Sonido
Menús
Apagado/reinicio

Haz esta comprobación antes de copiar cientos de juegos.

En nuestro caso, la R36S arrancó correctamente y ArkOS funcionó al 100%.

11. Copiar tus juegos

Una vez comprobado que ArkOS funciona, conecta la microSD nueva al PC.

ArkOS crea las carpetas necesarias para los sistemas.

La regla es:

Cada ROM va en la carpeta correspondiente a su sistema.

Ejemplos:

roms/nds
roms/psx
roms/neogeo
roms/arcade
roms/gba
roms/snes
roms/gb
roms/gbc
12. Nintendo DS

Los juegos de Nintendo DS van en:

roms/nds

Por ejemplo:

roms/nds/
├── Lego Batman.nds
├── Juego 2.nds
└── Juego 3.nds
IMPORTANTE

Dentro de nds puedes encontrar carpetas especiales como:

backup
bg
cheats
optional
savestates
slot2

No metas los juegos dentro de esas carpetas.

Los archivos .nds deben quedar directamente dentro de:

roms/nds

Durante esta instalación probamos un juego de Nintendo DS (LEGO Batman) y funcionó correctamente. 
16. No copies todo sin revisar

Este fue uno de los errores más fáciles de cometer durante el proceso.

No conviene copiar toda una carpeta vieja directamente sobre la nueva instalación sin saber qué contiene.

Por ejemplo, dentro de una carpeta pueden aparecer:

juego.zip
juego.png
juego.fs
juego.hi

No todos esos archivos son necesariamente la ROM principal.

La regla sencilla es:

Copia los archivos de juego y conserva las carpetas especiales del sistema de ArkOS.

17. Partidas guardadas y BIOS

Después de comprobar que las ROM funcionan, el siguiente paso es recuperar:

bios
save
saves
backup
savestates
Recomendación

No copies estas carpetas a ciegas.

Primero comprueba dónde está guardando ArkOS las partidas de cada emulador y luego pasa tus partidas antiguas a la ubicación correspondiente.

Esto es especialmente importante con:

Nintendo DS
PlayStation
Emuladores que utilizan savestates

Así reduces el riesgo de sobrescribir configuraciones nuevas o colocar una partida en una ruta incorrecta.

18. Orden recomendado para instalar todo

Una forma segura de hacerlo es:

1. Respaldar la SD original
        ↓
2. Preparar SD nueva
        ↓
3. Descargar imagen ArkOS MultiPanel
        ↓
4. Extraer .img.xz → .img
        ↓
5. Escribir .img con Rufus
        ↓
6. Primer arranque
        ↓
7. Esperar configuración inicial
        ↓
8. Comprobar pantalla/botones/sonido
        ↓
9. Copiar unas pocas ROM
        ↓
10. Probarlas
        ↓
11. Copiar el resto de ROM que quieras
        ↓
12. Recuperar BIOS
        ↓
13. Recuperar partidas guardadas
19. Resultado final

Al terminar deberías tener una R36S funcionando con una instalación limpia de ArkOS y una estructura similar a:

roms/
├── arcade/
├── gba/
├── gb/
├── gbc/
├── nds/
├── neogeo/
├── psx/
├── snes/
└── ...

Y dentro de cada carpeta solamente los juegos que realmente quieras.

Por ejemplo:

roms/
├── nds/
│   └── Lego Batman.nds
│
├── neogeo/
│   ├── mslug.zip
│   ├── mslug2.zip
│   └── mslug3.zip
│
├── psx/
│   └── Castlevania - Symphony of the Night.chd
│
└── arcade/
    └── qbert.zip


    Nota: ArkOS-R3XS es un proyecto comunitario y su repositorio actual está archivado; la propia página recomienda consultar proyectos sucesores para versiones futuras. Esta guía documenta específicamente el procedimiento realizado con la imagen MultiPanel de ArkOS 2.0.11072025.

Fuentes
Repositorio comunitario de ArkOS-R3XS: https://github.com/AeolusUX/ArkOS-R3XS
Releases de ArkOS-R3XS: https://github.com/AeolusUX/ArkOS-R3XS/releases
Información de emuladores y carpetas de ROM de ArkOS: https://github.com/christianhaitian/arkos/wiki/ArkOS-Emulators-and-Ports-information
