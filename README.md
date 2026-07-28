# Guía de programación (XMLTV) — Argentina y Latinoamérica

Guía electrónica de programación en formato XMLTV, lista para usar en cualquier
reproductor de IPTV.

## Cómo usarla

Pegá esta dirección donde tu reproductor pida la guía o el "EPG":

```
https://jarap.github.io/iptv-epg-argentina/epg.xml.gz
```

Funciona en Zapping, IPTV Pro, TiviMate, Kodi y cualquier otro que acepte XMLTV.
El archivo viene comprimido con gzip, que es lo que todos esperan.

## Qué trae ahora

| | |
|---|---|
| Canales | 154 |
| Programas | 17846 |
| Desde | 2026-07-28 02:40 |
| Hasta | 2026-08-12 00:00 |
| Tamaño | 1097 KB comprimido |
| Actualizada | 2026-08-08 04:20 -03 |

## De dónde salen los datos

De las tablas EIT que los propios canales emiten dentro de su señal. No se toman
de sitios de terceros ni se copian de otras guías: es la programación que anuncia
cada canal, en español y con los horarios en hora argentina.

Un servidor [Astra](https://cesbo.com/astra/) recibe las señales, extrae el EIT y
arma el XMLTV; de ahí se publica acá una vez por día.

## Cómo se identifican los canales

Cada canal tiene un identificador corto y estable:

```xml
<channel id="a0fc">
    <display-name>Encuentro</display-name>
</channel>
```

Si tu lista M3U trae ese mismo valor en `tvg-id`, el reproductor empareja solo,
sin tener que adivinar por el nombre.

## Actualización

Se renueva todos los días de madrugada. La rama se reescribe en cada publicación
para que el repositorio no crezca sin control: acá siempre está la guía vigente,
no el archivo histórico.
