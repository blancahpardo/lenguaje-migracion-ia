# Diccionario de datos

## Convención de nombres

- **Herramientas** (carpetas de primer nivel en `datos/`): `chatgpt`, `gemini`, `claude`, `deepseek`.
- **Bloques e iteraciones** (subcarpetas):
  - `bloqueA_iteracion1`, `bloqueA_iteracion2`, `bloqueA_iteracion3` — el bloque principal (P1→P2→P3→P4), repetido tres veces, desde la posición de una persona de la sociedad receptora.
  - `bloqueAprima_persona_migrante` — la sonda de contraste (P1′→P2′), una vez por herramienta, desde la posición de una persona migrante en situación irregular.
  - `bloqueB_consulta_dirigida` — la consulta dirigida (B1→B2), una vez por herramienta.
- **Códigos de prompt:** `P1`–`P4` (bloque A), `P1'`–`P2'` (bloque A′) y `B1`–`B2` (bloque B). `B1` es idéntico a `P1`.
- **Capturas:** `capturas/*.png`. El nombre incluye la hora exacta de la captura (CEST, España), que coincide con la hora que muestra la propia captura.

## Archivos por carpeta de recogida

| Archivo | Contenido |
|---|---|
| `transcripcion.md` | Conversación normalizada para lectura: cabecera de condiciones + turnos marcados **Usuario (código)** / **[asistente]**. |
| `transcripcion_bruta.txt` | Captura textual sin marcado de lectura (verbatim). |
| `ficha.md` | Tabla con las condiciones exactas de esa recogida. |
| `capturas/` | Capturas de pantalla de la conversación (bloques A y A′; el bloque B no tiene capturas). |

## `datos/condiciones_de_recogida.csv`

Una fila por recogida (20 en total). Campos:

| Campo | Descripción |
|---|---|
| `herramienta` | Nombre del asistente (ChatGPT, Gemini, Claude, DeepSeek). |
| `empresa` | Empresa proveedora. |
| `bloque` | `A` (bloque principal), `A'` (sonda persona migrante) o `B` (consulta dirigida). |
| `iteracion` | 1, 2, 3 para el bloque A; `-` para A′ y B. |
| `modelo_version` | Modelo/versión tal como aparecía en la interfaz. |
| `tipo_cuenta` | Siempre «Gratuita». |
| `memoria_off` | «Sí»: memoria y personalización desactivadas. |
| `idioma` | Idioma de la consulta (español). |
| `ubicacion` | País de acceso (España). |
| `fecha` | Fecha de la recogida (2026-07-19). |
| `hora_inicio` | Hora de la primera captura de la recogida (vacío en el bloque B, sin capturas). |
| `hora_fin` | Hora de la última captura de la recogida (vacío en el bloque B). |
| `orden_prompts` | Orden de aplicación de los prompts. |
| `n_capturas` | Número de capturas de pantalla. |
| `url_publica` | Enlace público a la conversación. |

## `instrumentos/Libro_de_codigos_analisis.xlsx`

Plantilla de análisis. Pestañas: instrucciones, registro de condiciones, rejilla léxico-metafórica del fenómeno diana (con distinción uso/mención), matriz de adherencia a las dieciocho recomendaciones, rúbrica de las siete dimensiones y verificación de fuentes. Véase `docs/Metodologia.md` y `docs/Patron_referencia.md` para su fundamentación.
