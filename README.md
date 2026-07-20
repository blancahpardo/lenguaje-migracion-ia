# Lenguaje, migración e inteligencia artificial generativa

**Corpus de respuestas de cuatro asistentes conversacionales (ChatGPT, Gemini, Claude y DeepSeek) ante consultas sobre migración**

Conjunto de datos que acompaña a la investigación del grupo sobre el lenguaje de la migración. Reúne las respuestas de cuatro asistentes de inteligencia artificial generativa a una misma batería de consultas relacionadas con la migración, recogidas de forma controlada, con el fin de analizar en qué medida reproducen o evitan las **metáforas deshumanizadoras** (agua y desastre natural, invasión, alimaña, mercancía, presión) y en qué medida se ajustan a las **recomendaciones lingüísticas** de las guías institucionales y deontológicas vigentes.

- **Autoría:** Blanca Hernández Pardo, Carmen María Cedillo Corrochano y María Amparo Soler Bonafont
- **Recogida y curación de datos:** Blanca Hernández Pardo
- **Fecha de recogida:** 19 de julio de 2026
- **Idioma de las consultas:** español · **Ubicación de acceso:** España
- **Licencia:** CC BY 4.0 (véase [`LICENSE`](LICENSE))
- **Versión:** 1.0.0

> Este conjunto de datos replica el procedimiento del corpus [*Lenguaje, cáncer e inteligencia artificial generativa*](https://doi.org/10.5281/zenodo.21419368) sobre un tema distinto (migración) y un fenómeno lingüístico distinto (metáforas deshumanizadoras en lugar de lenguaje bélico).

---

## 1. Qué contiene este repositorio

Para cada uno de los cuatro asistentes se recogieron **tres iteraciones del bloque principal (A)**, **una sonda de contraste desde la posición de la persona migrante (bloque A′)** y **una consulta dirigida (bloque B)**, siempre sobre cuentas limpias y gratuitas. En total: **20 conversaciones**, con su transcripción y, cuando existen, sus capturas de pantalla con fecha y hora.

```
lenguaje-migracion-ia/
├── README.md
├── LICENSE
├── CITATION.cff              · cómo citar este conjunto de datos
├── .zenodo.json             · metadatos para el archivado en Zenodo (DOI)
├── CHANGELOG.md
├── docs/
│   ├── Metodologia.md        · apartado de metodología del artículo
│   ├── Protocolo_recogida.md · protocolo paso a paso de la recogida
│   ├── Patron_referencia.md  · las 18 recomendaciones consolidadas (patrón de adherencia)
│   └── diccionario_de_datos.md
├── instrumentos/
│   └── Libro_de_codigos_analisis.xlsx  · plantilla de análisis
└── datos/
    ├── condiciones_de_recogida.csv     · tabla-resumen de las 20 recogidas
    ├── chatgpt/  · claude/  · gemini/  · deepseek/
    │   ├── bloqueA_iteracion1/
    │   │   ├── transcripcion.md         · conversación con turnos marcados
    │   │   ├── transcripcion_bruta.txt  · captura textual original (verbatim)
    │   │   ├── ficha.md                 · condiciones de esa recogida
    │   │   └── capturas/                · capturas .png (nombre = hora exacta)
    │   ├── bloqueA_iteracion2/ …
    │   ├── bloqueA_iteracion3/ …
    │   ├── bloqueAprima_persona_migrante/ …
    │   └── bloqueB_consulta_dirigida/ …
```

## 2. Diseño en breve

La batería de estímulos se compone de tres bloques (el texto literal está en `docs/Protocolo_recogida.md`):

| Código | Bloque | Contenido |
|---|---|---|
| **P1** | A | Consulta espontánea y con carga emocional, desde la posición de una persona de la sociedad receptora, indecisa ante lo que oye en su barrio. |
| **P2** | A | Consulta informativa sobre la situación migratoria en España y sus causas. |
| **P3** | A | Solicitud de fuentes, organizaciones e informes fiables. |
| **P4** | A | Pregunta metalingüística sobre guías para hablar de la migración (al cierre). |
| **P1′–P2′** | A′ | Sonda de contraste desde la posición de una persona migrante en situación irregular que pide orientación. |
| **B1** | B | Arranque idéntico a P1, en un hilo independiente. |
| **B2** | B | Consulta dirigida que inyecta el marco problemático (avalancha / invasión / desbordamiento / ilegales) para observar la orientabilidad del asistente. |

El bloque A se administra en un único hilo por herramienta (P1 → P2 → P3 → P4) y se repite tres veces en conversaciones nuevas y limpias. El bloque A′ y la consulta dirigida (B) se administran una vez por herramienta, en hilos aparte.

## 3. Modelos y condiciones

Todas las consultas se hicieron el 19 de julio de 2026, en español, desde España, con versiones gratuitas y cuentas limpias (memoria y personalización desactivadas, sin instrucciones personalizadas). La versión del modelo se consigna tal como aparecía en la interfaz en el momento de la recogida:

| Asistente | Empresa | Modelo / versión visible |
|---|---|---|
| ChatGPT | OpenAI | No identificable en la interfaz (versión gratuita; sin selector de modelo visible) |
| Gemini | Google | 3.5 Flash |
| Claude | Anthropic | Claude Sonnet (plan gratuito) |
| DeepSeek | DeepSeek | Modo «Instant» (sin «Pensamiento Profundo») |

La tabla completa con las horas exactas de cada recogida está en [`datos/condiciones_de_recogida.csv`](datos/condiciones_de_recogida.csv) y en la `ficha.md` de cada carpeta.

## 4. Cómo leer las transcripciones

Cada `transcripcion.md` está normalizada para su lectura: cabecera con las condiciones y, luego, los turnos marcados como **Usuario (P1/P2/…)** y **[nombre del asistente]**. El archivo `transcripcion_bruta.txt` conserva la captura textual sin marcado de lectura, para trazabilidad. En la normalización solo se han retirado etiquetas de interfaz y artefactos ajenos a la respuesta; no se ha alterado el contenido. Las referencias a fuentes web que los asistentes insertan como «chips» de fundamentación se conservan entre corchetes, p. ej. `[INE]`, `[ACNUR]`.

Cada conversación se conserva además como enlace público en la cabecera de su transcripción y en su ficha.

**Nota sobre las capturas.** El bloque A dispone de cuatro capturas por conversación y el bloque A′ de dos; el bloque B se conserva solo como enlace público (sin capturas). En el bloque A′ de ChatGPT, la captura de la segunda respuesta se conserva **pixelada**, porque el asistente mostró un mapa con la ubicación aproximada de la usuaria; el mapa mismo no forma parte de la transcripción textual y su aparición se documenta en la `ficha.md` correspondiente.

## 5. Análisis

El análisis cualitativo se apoya en la plantilla [`instrumentos/Libro_de_codigos_analisis.xlsx`](instrumentos/Libro_de_codigos_analisis.xlsx). Contempla siete dimensiones (metáfora deshumanizadora, accesibilidad, empatía y acompañamiento, registro y tecnicismo, fiabilidad e invenciones, orientabilidad y detección de guías) y el contraste de cada respuesta con las **dieciocho recomendaciones** consolidadas en [`docs/Patron_referencia.md`](docs/Patron_referencia.md). El recuento del fenómeno diana distingue en todo momento entre **uso** y **mención** de cada término.

## 6. Consideraciones éticas y de transparencia

El estudio no recaba datos de participantes humanos: el material son respuestas generadas por los asistentes ante una batería de consultas diseñada por las autoras. Las transcripciones pueden contener afirmaciones inexactas propias de estos sistemas; se conservan sin corregir precisamente porque son el objeto de estudio, y no deben tomarse como información fiable sobre migración. Los enunciados del bloque B ponen en boca de la investigadora formulaciones deshumanizadoras que **no** comparte, con función de sonda experimental.

## 7. Cómo citar

Referencia en APA (7.ª ed.):

> Hernández Pardo, B., Cedillo Corrochano, C. M. y Soler Bonafont, M. A. (2026). *Lenguaje, migración e inteligencia artificial generativa: corpus de respuestas de cuatro asistentes conversacionales (ChatGPT, Gemini, Claude y DeepSeek) ante consultas sobre migración* (Versión 1.0.0) [Conjunto de datos]. Zenodo. [DOI pendiente de asignación]

Véase también [`CITATION.cff`](CITATION.cff).
