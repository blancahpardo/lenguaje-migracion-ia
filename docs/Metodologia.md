# Metodología

## Diseño

Estudio comparativo de corte cualitativo sobre las respuestas de cuatro asistentes conversacionales de propósito general a una batería idéntica de consultas en español. Replica el procedimiento aplicado por el grupo en un trabajo previo sobre lenguaje bélico y comunicación oncológica, con las adaptaciones que impone el nuevo objeto. Las frecuencias léxicas se ofrecen como apoyo descriptivo; la inferencia principal es interpretativa y descansa en la lectura contextual de cada aparición.

## Herramientas y condiciones

Se seleccionaron **ChatGPT** (OpenAI), **Gemini** (Google), **Claude** (Anthropic) y **DeepSeek**, este último a efectos de contraste con un sistema no occidental. Se descartaron los asistentes orientados a la búsqueda bibliográfica (tipo Perplexity), por interesar el diálogo generalista.

Todas las consultas se realizaron con las versiones **gratuitas** y con **cuentas de nueva creación**, abiertas desde una dirección de correo creada para el estudio. Se verificó, herramienta por herramienta, la desactivación de la memoria y de la personalización, y que las instrucciones personalizadas estuvieran vacías. Se registraron, por herramienta y repetición, la fecha y hora exactas, la versión del modelo visible, el tipo de cuenta, el idioma, la ubicación de acceso y el orden de los prompts. Toda la recogida se concentró en una **única jornada** (19 de julio de 2026), para minimizar la deriva del modelo.

## Batería de prompts

El principio rector es que los prompts **no siembren** el fenómeno diana: ningún enunciado de los bloques A y A′ contiene los lexemas del inventario ni alusión a la corrección lingüística, para no inducir por efecto espejo lo que se pretende observar. La pregunta metalingüística se reserva para el cierre.

- **Bloque A** (posición de la sociedad receptora, hilo único, tres iteraciones): P1 consulta espontánea con carga emocional; P2 consulta informativa; P3 solicitud de fuentes; P4 pregunta metalingüística sobre guías.
- **Bloque A′** (posición de la persona migrante en situación irregular, una vez): sonda de contraste sobre denominación y registro.
- **Bloque B** (hilo aparte, una vez): tras un arranque idéntico a P1, inyecta el marco problemático —agua, invasión, presión y el calificativo *ilegal*— y pide conformidad, para medir la **orientabilidad**.

El corpus resultante asciende a **20 conversaciones** (4 herramientas × [3 A + 1 A′ + 1 B]). El texto literal de los prompts está en `Protocolo_recogida.md`.

## Instrumentos de análisis

Recogidos en `instrumentos/Libro_de_codigos_analisis.xlsx`:

1. **Rejilla léxico-metafórica.** Presencia, frecuencia y cita literal de cada aparición, clasificada según los siete dominios fuente (Mendelsohn y Budak, 2025) cruzados con el léxico español (Montagut y Moragas-Fernández, 2020), con categoría de control (viaje/acogida). Cada aparición se codifica como **uso** o como **mención**.
2. **Matriz de adherencia.** Cada respuesta frente a las 18 recomendaciones de `Patron_referencia.md` (cumple / parcial / incumple / no aplica) con nota de evidencia.
3. **Rúbrica dimensional.** Siete dimensiones: metáfora deshumanizadora, accesibilidad, empatía y acompañamiento, registro y tecnicismo, fiabilidad e invenciones, orientabilidad (bloque B) y detección de guías (P4).
4. **Verificación de fuentes.** Comprobación de que las organizaciones, informes y URL ofrecidos en P3 existen realmente.

**Distinción uso/mención.** Muchas apariciones de los términos del inventario no los usan, sino que los mencionan (entrecomillados, para rechazarlos), sobre todo en P4 y en el bloque B. Un recuento automático de frecuencias, ciego al contexto, computaría esas apariciones como reproducción del marco cuando lo que hacen es combatirlo. Ambos recuentos se informan por separado.

**Fiabilidad.** Primera pasada de quien analiza, doble codificación de una submuestra con κ de Cohen y validación conjunta entre las autoras antes de dar la codificación por definitiva.

## Ética y transparencia

No hay sujetos humanos: el material son salidas de sistemas de IA. Las transcripciones pueden contener contenido estigmatizante generado por los propios sistemas (sobre todo en el bloque B) y se conservan sin corregir por ser el objeto de estudio. Los enunciados del bloque B ponen en boca de la investigadora formulaciones que no comparte, con función de sonda experimental. Se declara el uso de herramientas de IA en las fases del trabajo en que se han empleado.
