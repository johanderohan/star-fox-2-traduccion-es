# Star Fox 2 — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/super-nintendo/star-fox-2)**.

Traducción al **castellano de España** de *Star Fox 2*, para la ROM japonesa comercial de Super Nintendo incluida en Classic Mini y Switch Online. Se ha traducido desde el japonés del juego; los menús, avisos y créditos que ya estaban en inglés se han traducido desde ese original.

Se distribuye un **parche**, no el juego. Necesitas tu propia copia original.

## Estado

Versión **[v1.0](../../releases/tag/v1.0)**, en revisión.

Incluye comunicaciones de los personajes, tutorial, menús, configuración de mandos, mapa, indicadores de combate, resultados, récords, avisos de mando/región y cargos de los créditos. Los carteles funcionales también están adaptados, incluido **FIN con letras tridimensionales**.

Se mantienen los logotipos, la música y los nombres originales de personajes y de los modelos de la galería de créditos. La ROM conserva su tamaño de **1 MiB**.

### Comprobaciones y límites

- Construcción reproducible y auditoría de la ROM terminada: punteros, controles, límites de texto y fuente, geometría, tablas gráficas y checksum. Los gráficos se han contrastado también ejecutando el descompresor Super FX original.
- Pruebas en Snes9x mediante libretro: arranque y atracción, menús, caracteres españoles, mandos A–D, mapa, nave nodriza, combate, pausa y récords. Se creó una firma, se recuperó al reiniciar con la SRAM, se comprobó la cancelación del borrado y el borrado persistente.
- Controles terrestres Walker comprobados en un tramo dirigido con recarga de escudo; finales, créditos, resultados y FIN en NORMAL, HARD y EXPERT revisados mediante recorridos de depuración. Se diferencian de los tramos jugados normalmente con el mando.
- El parche se reaplica al original y reproduce la candidata byte a byte.

**No se ha jugado una partida completa ni se ha probado en consola física.** La traducción y la revisión están asistidas por IA; no hay revisión humana independiente. La etiqueta «en revisión» describe esas limitaciones.

## Cómo aplicar el parche

1. Descarga `star-fox-2-snes-es-v1.0.zip` de **[Releases](../../releases)** y extrae el parche `.xdelta` y sus licencias.
2. Comprueba tu ROM japonesa original, sin cabecera de copiadora:

   | Dato | Valor |
   |---|---|
   | Tamaño | 1.048.576 bytes |
   | MD5 | `e7de4068dd0577ec5567783739839a76` |
   | SHA-256 | `835b6a45b55086d199ecadeb1ee32f9ae77a986251dfb4343bbf1e33d1221550` |

   Las versiones estadounidenses, los prototipos y las ROMs ya modificadas no son la base de este parche.
3. Aplica el `.xdelta` con [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases) o con xdelta3, guardando el resultado en un archivo nuevo:

   ```sh
   xdelta3 -d -s "original.sfc" star-fox-2-snes-es-v1.0.xdelta "Star Fox 2 (Castellano).sfc"
   ```
4. Comprueba el resultado:

   | Dato | Valor |
   |---|---|
   | Tamaño | 1.048.576 bytes |
   | MD5 | `2fb4988237a40197c615145a37a59a6f` |
   | SHA-256 | `00abab97de737b3a8adf31e1c6c2f1e6a6221d61991ece46c0b98481c9580386` |

5. Cárgalo en un emulador compatible con Super FX. Cada versión del parche se aplica sobre el original limpio, no sobre una traducción anterior.

SHA-256 del parche `.xdelta`: `4df976d31d3f97033b98fd69d5e58a2b942d8e33f9bdcb83943d2863e3256eb7`.

## Cambios de v1.0

Primera publicación: textos y rótulos en castellano, fuentes con signos españoles, maquetación revisada y FIN tridimensional. Conserva el tamaño original y el funcionamiento del guardado de récords comprobado en emulador.

## Créditos técnicos

Herramientas de [arqhive](https://github.com/arqhive/star-fox-2-korean-translation), con licencia MIT; fuente de diálogo derivada de Galmuri9, de Lee Minseo/quiple, con licencia SIL OFL 1.1. Las licencias se incluyen junto al parche. Se utilizó [SuperFX Object Dumper](https://github.com/Hordeking/sfxObjectDump), de JD Fenech, para comprobar de forma independiente los modelos. No se reutiliza la traducción coreana.

## Aviso

Proyecto de aficionados, sin relación con Nintendo ni Argonaut. Star Fox y Star Fox 2 pertenecen a sus titulares. No se distribuye la ROM: el parche modifica una copia propia. Puedes comunicar erratas o problemas en [Issues](../../issues), indicando la versión y la situación del juego.
