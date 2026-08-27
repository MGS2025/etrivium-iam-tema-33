# Tema 33 — Validación

> **Título oficial**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.
>
> **Versión**: v1.0 — **Pendiente de validación por María, Ana y el IAM**
> **Fecha**: 2026-08-27

---

## 1. Cobertura del temario oficial

El enunciado oficial (BOAM 10.032, tema 33) enumera **siete materias**. Correspondencia con las secciones del contenido:

| Enunciado oficial | Sección | Estado |
|---|---|---|
| Comunicaciones | §1 | ✅ Completo |
| Medios de transmisión | §2 | ✅ Completo |
| Modos de comunicación | §3 | ✅ Completo |
| Equipos terminales y equipos de interconexión y conmutación | §4 | ✅ Completo |
| Redes de comunicaciones | §5 | ✅ Completo |
| Redes de conmutación y redes de difusión | §6 | ✅ Completo |
| Comunicaciones móviles e inalámbricas | §7 y §8 | ✅ Completo |
| *(no está en el enunciado oficial; lo añade el esqueleto de partida)* Seguridad y normativa en la Administración Pública | §9 | ✅ Completo |

El **esqueleto de partida** (`Test_Prompting/temas agosto/33.md`) se ha seguido **literalmente**. Ver la observación 1 sobre el mapeo de niveles.

## 2. Contenido teórico

- **9 secciones · 20 subsecciones · 6 epígrafes de tercer nivel** (numeración de tres niveles, `N.M.K`, coherente con el resto de la serie técnica).
- **~24.500 palabras** medidas con `wc -w`. Es el **segundo tema más extenso de toda la serie**, solo por detrás de T32 (≈25.000) y por delante de T29 (≈21.200) y T30 (≈21.400). La causa es estructural y no de estilo: el enunciado oficial reúne **siete materias** y el tema funciona como cimiento de todo el bloque de redes (T34-T38).
- **4 tipos de callout** y **71 cajas** en total: `[DATO CLAVE EXAMEN]`, `[EJERCICIO RESUELTO]`, `[EJEMPLO AYTO MADRID]` y `[REFERENCIA CRUZADA]`.
- **Caso de referencia transversal**: la red que conecta una Oficina de Atención a la Ciudadanía de distrito con el CPD del IAM, que atraviesa las nueve secciones y enlaza con los tres casos prácticos.
- Cierre con un bloque de **«los ocho datos que no se pueden fallar»**, no numerado, a modo de resumen memorístico.
- **Sin fragmentos de código**, por la misma decisión adoptada en T26, T28, T29, T30 y T32: el enunciado no menciona ningún lenguaje y lo memorizable son frecuencias, distancias, normas IEEE, direcciones y artículos. Se ha concentrado en tablas y en los diagramas D3, D5, D9, D10, D14, D15 y D17.

## 3. Fuentes

- **Tier 1**: 25 referencias (Ley 11/2022, ENS, UIT-R y UIT-T, Shannon, Nyquist, familias IEEE 802.1/802.3/802.11/802.15/802.16, ISO/IEC 11801 y 18092, RFC del IETF, 3GPP, IMT de la UIT, ETSI TETRA, RD 391/2019, Ley 13/2022, Reglamento (UE) 2015/2120, RD 346/2011, Ley 40/2015).
- **Tier 2**: 10 referencias (Tanenbaum, Stallings, Kurose, Forouzan, Wi-Fi Alliance, GSMA, LoRa Alliance, CCN-STIC, Bluetooth SIG, ONTSI).
- **Tier 3**: 3 referencias de contexto municipal.
- **Verificación contra fuente oficial** (no de memoria):
  - **Ley 11/2022**: descargado el PDF del texto consolidado del BOE (`BOE-A-2022-10757`) y extraído con `pdftotext -layout`. De ahí proceden **literalmente** las definiciones del **anexo II** (apartados 19 equipo terminal, 21 espectro radioeléctrico, 61-64 red de comunicaciones electrónicas, de alta y de muy alta capacidad y red pública, 70 servicio de comunicaciones electrónicas y 79 telecomunicaciones), el **art. 37** completo del servicio universal, el **anexo III** con sus once servicios, y los arts. **2**, **4**, **13**, **55**, **63** y **85**. También de ahí sale el recuento exacto de la estructura de la ley: 8 títulos, 114 artículos, 30 disposiciones adicionales, 7 transitorias, 1 derogatoria, 6 finales y 3 anexos.
  - **ENS**: descargado el PDF consolidado del BOE (`BOE-A-2022-7191`). Verificadas literalmente las medidas **`mp.com.1`** a **`mp.com.4`** con sus requisitos, sus refuerzos y sus tablas de aplicación por categoría y por nivel, incluido el requisito `mp.com.4.2` sobre comunicaciones inalámbricas y el desglose del refuerzo R1 en las tres subredes mínimas (usuarios, servicios y administración).
  - **IEEE 802.11be (Wi-Fi 7)**: fecha de publicación —**22 de julio de 2025**— verificada en línea.
  - **IEEE 802.11bn (Wi-Fi 8)**: inicio de los trabajos en noviembre de 2023, borrador 1.0 en julio de 2025 y **publicación prevista en 2028**, verificados en línea.
  - **Bluetooth**: versión vigente del núcleo en agosto de 2026, **6.3**, publicada el 6 de mayo de 2026, verificada en línea.
  - **Espectro 5G en España**: **RD 391/2019** (segundo dividendo digital, banda de 700 MHz, migración de la TDT antes del **31-10-2020**, banda 470-694 MHz garantizada para TDT **hasta al menos 2030**) y subasta de la banda de **26 GHz** en 2022 (12 concesiones estatales y 38 autonómicas, 20 años prorrogables), verificados en línea.
  - **Ley 13/2022, General de Comunicación Audiovisual**: definición de **múltiplex** verificada en línea.

## 4. Test (60 preguntas)

- **60 preguntas** de 3 opciones (A/B/C), formato oficial de la oposición, con penalización de **1/3** en el motor de corrección.
- **Distribución de la respuesta correcta: 20 A / 20 B / 20 C**, conseguida **a la primera** por haber fijado la secuencia de letras **antes** de redactar (lección aprendida en T23) y verificada por script.
- Reparto por materia: P1-P8 conceptos, señal, ancho de banda y capacidad · P9-P17 medios de transmisión · P18-P24 modos de comunicación · P25-P33 equipos terminales y de interconexión · P34-P39 redes y topologías · P40-P47 conmutación y difusión · P48-P54 redes inalámbricas y móviles · P55-P60 seguridad y normativa.
- Verificación automática: 60 preguntas, 3 opciones únicas por pregunta, **coincidencia exacta** entre el texto de la opción correcta y el de la solución, y referencia a epígrafe y fuente en las 60.
- **Ocho preguntas son de cálculo o de aplicación numérica** (P8, P9, P19, P22, P37, P43 y las de datos duros P11, P12), no solo de memoria.

## 5. Casos prácticos

- **3 casos**, de **10 puntos** cada uno, con enunciado, cuestiones puntuadas, solución orientativa y criterios de evaluación desglosados.
- Los tres recorren el mismo supuesto —la red de una Oficina de Atención a la Ciudadanía de distrito y su enlace con el CPD del IAM— desde tres ángulos: **medios, modos y calidad** (Caso 1), **equipos, topología y difusión** (Caso 2) y **despliegue inalámbrico, seguridad y normativa** (Caso 3).
- El Caso 2 incorpora un **incidente real y frecuente** —la tormenta de difusión por un latiguillo mal conectado— porque obliga a razonar y no solo a recordar.

## 6. Diagramas

- **18 diagramas SVG** embebidos, todos con `viewBox`, `role="img"` y `aria-label` descriptivo en español.
- Clases CSS con **sufijo numérico único** por diagrama (`.t1`…`.n18`) para evitar el bug sistémico de colisión de estilos detectado en T5.
- Los 18 se han **validado como XML** con `ET.fromstring()` antes de generar el `index.html`, aplicando la lección del **tercer falso OK del QA** documentada en T32: un SVG mal formado no se pinta, mide 0×0 y por tanto «ni desborda ni colisiona», de modo que `getBBox` devolvería un falso «0 desbordes».
- Todos llevan la línea de atribución `[Fuente: …]` con margen respecto al borde inferior del `viewBox` y respecto al último elemento dibujado.

## 7. Refs cruzadas validadas contra el temario oficial

Se han citado y verificado contra el enunciado oficial de BOAM 10.032: **T11** (informática básica, buses y representación de la información), **T12** (periféricos y conectividad), **T13** (formatos de información y ficheros), **T26** (almacenamiento, para situar la SAN), **T30** (administración de redes de área local), **T31** (cloud, para la computación en el borde), **T32** (seguridad, criptografía y protocolos seguros), **T34** (modelos OSI y TCP/IP), **T35** (internet y sus servicios), **T36** (seguridad en redes, perimetral y VPN), **T37** (redes locales: tipología, técnicas de transmisión, métodos de acceso y dispositivos de interconexión), **T38** (TETRA) y **T39** (ENS y ENI). **Las trece son correctas.**

---

## 8. Observaciones y puntos abiertos a validar

### Observación 1 — Mapeo del esqueleto: 3 bloques a 9 secciones numeradas

El `Test_Prompting/temas agosto/33.md` trae **tres bloques de primer nivel** (`##`), nueve subapartados (`###`), veinte epígrafes (`####`) y seis subepígrafes (`#####`). Se ha mapeado así:

| Nivel del esqueleto | Nivel del contenido |
|---|---|
| `##` (3 bloques temáticos) | **Desaparece como nivel numerado**; su contenido se reparte en secciones |
| `###` (9) | **Secciones §1 a §9** |
| `####` (20) | Subsecciones **N.M** |
| `#####` (6) | Epígrafes **N.M.K** |

La razón: conservar los **tres niveles de numeración** que usa toda la serie técnica (`1.1.1.`) sin llegar a `1.1.1.1.`, y hacer que las secciones numeradas se correspondan una a una con las materias del enunciado oficial. **Es el mismo problema de estructura que se planteó en T27 (4 bloques → 8 secciones) y en T30 (5 niveles → 3), y sigue sin resolverse de forma uniforme para toda la serie. Conviene que María y Jesús fijen un criterio único de una vez, aplicable retroactivamente a T27, T30 y T33.**

### Observación 2 — Frontera con el Tema 37, que es la más delicada de este tema

El T37 («Redes locales. Tipología. Técnicas de transmisión. Métodos de acceso. Dispositivos de interconexión») **solapa con este tema en dos puntos**: las topologías y los dispositivos de interconexión. El criterio aplicado ha sido:

- **Los equipos de interconexión SÍ se desarrollan aquí** (§4.2), porque el enunciado del T33 los menciona expresamente —«equipos terminales y equipos de interconexión y conmutación»— y porque sin ellos no se entiende la difusión de §6.2.
- **Los métodos de acceso al medio NO se desarrollan aquí**: CSMA/CD, paso de testigo y el detalle de la trama Ethernet se remiten al T37. De CSMA/CA solo se explica **por qué** en radio no se puede usar CSMA/CD, que es una consecuencia del modo semidúplex de §3.1 y pertenece a este tema.
- **Las topologías se desarrollan aquí** (§5.2) en su formulación general, dejando al T37 su aplicación concreta a la red local.

**A validar**: si María o el IAM prefieren un reparto distinto, el candidato natural sería mover §4.2 al T37 y dejar aquí solo los equipos terminales, aunque eso contradiría el enunciado oficial del T33.

### Observación 3 — Frontera con los Temas 34, 36 y 39

- **T34 (OSI y TCP/IP)**: las capas se usan aquí **solo** como criterio de clasificación de equipos. No se desarrolla ni el modelo ni el direccionamiento IP. Sí se citan direcciones de difusión y multidifusión concretas, porque el enunciado del T33 pide expresamente «redes de difusión» y sin esas direcciones el epígrafe queda vacío. **A validar si ese nivel de detalle de direccionamiento debe quedarse aquí o remitirse al T34.**
- **T36 (seguridad en redes)**: solo se ha desarrollado la seguridad **específicamente inalámbrica** (§9.1), que es la que sitúa el esqueleto en este tema y que ningún otro cubre. Cortafuegos, IDS/IPS y VPN de acceso remoto se remiten al T36.
- **T39 (ENS y ENI)**: se citan únicamente las medidas `mp.com`, por ser las específicas de las comunicaciones. **A validar el nivel de detalle del ENS aquí frente al T39**, que es la misma pregunta abierta que dejaron T30, T31 y T32.

### Observación 4 — La sección 9 no está en el enunciado oficial

El bloque «Seguridad y normativa en la Administración Pública» del esqueleto **no figura en el enunciado oficial de BOAM 10.032**, que termina en «comunicaciones móviles e inalámbricas». Se ha desarrollado igualmente por tres razones: (a) está en el esqueleto de partida; (b) el marco de la Ley 11/2022 es materia razonablemente preguntable en un tema titulado «Comunicaciones»; y (c) es la parte del tema con más valor diferencial para el puesto, porque delimita **lo que el Ayuntamiento puede y no puede hacer** con una red. **A validar si debe mantenerse con este peso (≈ 15 % del tema), reducirse o suprimirse.**

### Observación 5 — Datos sensibles a la obsolescencia

Este es, junto al **T24** y al **T31**, uno de los temas más expuestos a quedarse desactualizado. **Reverificar antes de cada convocatoria**:

1. **Velocidad mínima del servicio universal**: la Ley 11/2022 prevé expresamente su escalado a **30 Mbit/s** por real decreto. En abril de 2026 hay un **proyecto de reglamento del servicio universal** en información pública en el portal del Ministerio para la Transformación Digital; si se aprueba y modifica la cifra, **hay que actualizar §9.2, el índice, el test (P59) y el Caso 3**.
2. **Wi-Fi 8 (802.11bn)**: publicación prevista en **2028**. Hasta entonces, todo equipo comercializado es «preestándar».
3. **Versión del núcleo Bluetooth**: se actualiza dos veces al año.
4. **Estado del 5G SA en España** y evolución hacia **IMT-2030 (6G)**, que a agosto de 2026 es prospectiva y no normativa.
5. **Bandas de espectro**: las atribuciones se revisan en cada Conferencia Mundial de Radiocomunicaciones de la UIT.

### Observación 6 — Extensión

El tema ha quedado en **≈ 24.500 palabras**, el segundo más extenso de la serie. La causa es el enunciado, no el estilo: son **siete materias** y el tema es el cimiento de otros cinco. Aun así, si María considera que resulta excesivo para un opositor, los dos candidatos naturales a recorte son **§9.2** (marco normativo, si se decide en la observación 4) y el detalle de las **generaciones móviles anteriores a 4G** en §8.2, que hoy tienen valor histórico más que operativo. **No se recomienda recortar** §4.2 ni §6, que son el núcleo preguntable.
