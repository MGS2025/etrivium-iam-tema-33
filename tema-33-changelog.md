# Tema 33 — Changelog

> **Título oficial**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.

---

## v1.4 — 2026-10-06 — Revisión de diagramas

**Motivo**: barrido de los diagramas de los 40 temas tras la revisión jurídica y de normas.

### Cambios

- Revisión visual de todos los diagramas, captura a captura (la medición automática no detecta contraste, flechas mal dirigidas ni textos pegados al borde): corregidos textos que se salían de su caja o del lienzo, cajas que se tocaban, flechas que no llegaban a su destino y textos con poco contraste. Sin cambios de contenido.

---

## v1.3 — 2026-10-02 — Normas vigentes y correcciones comunes de la revisión

**Motivo**: revisión de la serie del 01-10-2026 (decisiones de Joan y María): normas caducadas con el patrón de dos filas en Fuentes y correcciones comunes (referencias al cliente y al origen del material, promesas sobre el examen, AP → AAPP; en este tema no hay «AP» administrativo).

### Cambios

- Fuera las promesas sobre el examen («se pregunta», «muy preguntado», «materia de examen», «alta probabilidad de aparecer en el test oficial»…): unas 54 frases en contenido, índice, diagramas, fuentes y validación, conservando el dato. Las frases en condicional («una opción que afirme… es falsa») se mantienen.
- Test: 1 explicación(es) sin la coletilla de examen; enunciados, opciones y respuestas intactos.
- Pestaña Inicio: la caja «Cómo estudiar» (escrita en el builder) sin promesas sobre el examen.
- Fuera las referencias internas al origen del material (rutas `Test_Prompting/…`, «esqueleto oficial», notas de secuencia de la serie) en validación.
- Títulos de las cajas homogeneizados con los temas 1-10 (revisión jurídica): «Dato clave», «Ejemplo de aplicación en el Ayto» y «Relación con otros temas»; las cajas «Ejercicio resuelto» no cambian.

---

## v1.2 — 2026-09-06 — Marcado del apartado complementario

**Estado**: pendiente de validación por el IAM.

**Motivo**: criterio de literalidad del título fijado por el IAM (Jesús Cuadrado, 02-09-2026).

### Alcance

- El apartado final que **el enunciado oficial del tema no nombra** queda marcado como **material complementario**, en el índice y al principio del propio apartado, con la advertencia de que lo exigible es lo que enumera el título.
- **Sin cambios de contenido**: el apartado se mantiene íntegro.

---

## v1.1 — 2026-09-06 — Ficha de extensión y tiempo de estudio

**Estado**: sin cambios de contenido. Solo se añade información sobre el propio tema.

**Motivo**: petición del IAM (Jesús Cuadrado, 02-09-2026) al validar el Tema 30. Acepta la extensión de los temas «compuestos» a condición de que se informe de «su extensión en palabras y tiempo estimado de estudio». Al revisarlo se vio que ese dato solo aparecía en 16 de los 40 temas, y que faltaba justo en los más largos.

### Alcance

- Ficha bajo la cabecera del tema, y al final de la pestaña Índice donde esa pestaña existe:
  - **Extensión**: ~26.000 palabras · 18 diagramas · 60 preguntas de test
  - **Tiempo estimado de estudio**: 22-24 horas (primera vuelta completa, sin contar repasos)
- La cifra de palabras de la tabla de entregables se sincroniza con la ficha, para que el tema no muestre dos recuentos distintos.
- Las horas salen de una fórmula común a los 40 temas, para que sean comparables entre sí: contenido a 1.500 palabras/hora (ritmo de estudio activo), diagramas a una hora por cada cinco y test a dos minutos por pregunta. Se publica como intervalo de dos horas.
- Generado con `_tools-qa/ficha_estudio.py`, idempotente y reejecutable tras cualquier regeneración con `build_tNN.py`.

---

## v1.0 — 2026-08-27 — Primera versión

Generación completa del tema desde el esqueleto oficial `Test_Prompting/temas agosto/33.md`, siguiendo el patrón de la serie técnica (plantilla de referencia: **T32**).

### Alcance de la v1.0

| Entregable | Cantidad |
|---|---|
| Contenido teórico | 9 secciones · 20 subsecciones · 6 epígrafes de tercer nivel · **~24.500 palabras** |
| Diagramas SVG inline | **18** |
| Banco de test | **60 preguntas** A/B/C, balanceadas **20/20/20** |
| Casos prácticos | **3**, de 10 puntos cada uno |
| Fuentes | 25 Tier 1 · 10 Tier 2 · 3 Tier 3 |
| Pestañas del `index.html` | 8 (Inicio, Contenido, Índice, Diagramas, Test, Casos, Validación, Fuentes) |

### Decisiones de generación

1. **Mapeo del esqueleto: 3 bloques a 9 secciones numeradas.** El esqueleto trae tres bloques temáticos de primer nivel, nueve subapartados, veinte epígrafes y seis subepígrafes. Se ha mapeado `###` → sección, `####` → N.M y `#####` → N.M.K, con lo que las **nueve secciones numeradas se corresponden una a una con las materias del enunciado oficial** y se conservan los tres niveles de numeración de toda la serie. Es el mismo problema estructural de **T27** (4 bloques → 8 secciones) y **T30** (5 niveles → 3), y **sigue pendiente de un criterio uniforme**. Anotado como observación 1 de validación.

2. **Toda la Ley 11/2022 verificada contra el BOE.** Se descargó el PDF del texto consolidado (`BOE-A-2022-10757`) y se extrajo con `pdftotext -layout`. De ahí proceden **literalmente y no de memoria**: las definiciones del **anexo II** (19 equipo terminal, 21 espectro radioeléctrico, 61-64 redes, 70 servicio de comunicaciones electrónicas, 79 telecomunicaciones), el **art. 37** íntegro del servicio universal con sus **10 Mbit/s** escalables a 30, el **anexo III** con sus once servicios, y los arts. **2** (interés general y libre competencia), **4** (los únicos servicios públicos), **13** (Administraciones públicas como operadoras y la excepción de fallo de mercado en TDT), **55** (ICT), **63** (integridad y seguridad de las redes, con sus cinco parámetros de impacto) y **85** (dominio público radioeléctrico). También de ahí sale el recuento exacto de la estructura: **8 títulos, 114 artículos, 30 disposiciones adicionales, 7 transitorias, 1 derogatoria, 6 finales y 3 anexos**.

3. **ENS verificado contra el BOE.** PDF consolidado (`BOE-A-2022-7191`). Verificadas literalmente `mp.com.1` a `mp.com.4` con sus requisitos, sus refuerzos y sus tablas de aplicación, incluidos el requisito **`mp.com.4.2`** —*«si se emplean comunicaciones inalámbricas, será en un segmento separado»*— y el desglose del **refuerzo R1** en las tres subredes mínimas (usuarios, servicios y administración), que es el respaldo normativo directo de la §9.1 y del Caso 3.

4. **Otras verificaciones en línea.** Fecha de publicación de **IEEE 802.11be (Wi-Fi 7)**: 22 de julio de 2025. Calendario de **802.11bn (Wi-Fi 8)**: trabajos desde noviembre de 2023, borrador 1.0 en julio de 2025, publicación prevista en **2028**. Versión vigente del **núcleo Bluetooth**: **6.3**, de 6 de mayo de 2026. **RD 391/2019** (segundo dividendo digital, banda de 700 MHz, migración de la TDT antes del 31-10-2020, banda 470-694 MHz para TDT hasta al menos 2030) y subasta de **26 GHz** de 2022. Definición de **múltiplex** de la **Ley 13/2022**.

5. **Fronteras explícitas con T34, T35, T36, T37, T38 y T39.** El tema declara desde las «Convenciones» qué remite a cada uno y por qué, en una tabla. La frontera con el **T37** es la más delicada de toda la serie técnica, porque ambos enunciados citan los dispositivos de interconexión: aquí se desarrollan los equipos —el enunciado del T33 los pide expresamente— y se remiten al T37 los **métodos de acceso al medio** y el detalle de la trama Ethernet. Recogido como observación 2 de validación.

6. **Sin fragmentos de código.** Decisión deliberada, igual que en T26, T28, T29, T30 y T32: el enunciado no menciona ningún lenguaje y lo memorizable son frecuencias, distancias, normas IEEE, direcciones y artículos. Se han concentrado en tablas y en los diagramas D3, D5, D9, D10, D14, D15 y D17.

7. **Secuencia de letras del test fijada antes de redactar.** Aplicando la lección de T23, se definió de antemano la secuencia de 60 respuestas correctas con 20 de cada letra. Resultado: **20/20/20 a la primera**, verificado por script antes de dar el test por bueno.

8. **Validación XML de los SVG antes de medir nada.** Aplicando el **tercer falso OK del QA** documentado en T32 —un `</text>` sin cerrar hace que el elemento mida 0×0, con lo que «ni desborda ni colisiona» y `getBBox` devuelve un falso «0 desbordes»—, los 18 diagramas se han validado con `ET.fromstring()` **antes** de generar el `index.html` y **antes** de la sonda de composición. Los 18 pasan.

9. **Bug del conversor ya incorporado.** El `build_t33.py` nace con el `inline()` corregido —la negrita admite cursiva anidada—, sin arrastrar el bug detectado en T26 y T27.

10. **Acentuación de los SVG revisada específicamente.** El texto visible y los `aria-label` de los 18 diagramas se han revisado con un barrido dirigido, aplicando la lección de las tildes perdidas en SVG detectada en T22.

### Fuera del alcance de la v1.0

- No se desarrollan los **modelos OSI y TCP/IP** ni el **direccionamiento IP** (Tema 34), los **servicios de internet** (Tema 35), la **seguridad perimetral, los cortafuegos y las VPN de acceso remoto** (Tema 36), los **métodos de acceso al medio** de la red local (Tema 37) ni el **sistema TETRA** (Tema 38).
- La evolución hacia **6G / IMT-2030** se cita como prospectiva, no como normativa.
