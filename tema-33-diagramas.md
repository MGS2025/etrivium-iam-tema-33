# Tema 33 — Catálogo de Diagramas

> **Título oficial**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.
>
> **Versión**: v1.0
> **Fecha**: 2026-08-27
> **Autor**: ETRIVIUM
> **Formato**: SVG inline (zero-dependencias, escalable, imprimible, accesible con role/aria-label)
> **Paleta**: Ayuntamiento de Madrid #0055a0 (primario) + #d13c3c (alertas) + #2d8659 (ventajas) + #e89822 (callouts)
> **Nota técnica**: las clases CSS de cada SVG llevan sufijo numérico único (`.t1`, `.h1`…) para evitar colisiones de estilos entre los 18 diagramas embebidos en la misma página.

---

## Índice de diagramas

| ID | Título | Sección | Tipo | Formato |
|---|---|---|---|---|
| D1 | El modelo de comunicación de Shannon: los cinco elementos | §1.1.1 | Flujo | 680×300 |
| D2 | Perturbaciones del canal: atenuación, distorsión, ruido e interferencia | §1.1.1 | Comparativa | 680×340 |
| D3 | De la señal a los bits: muestreo, Nyquist y Shannon | §1.2 | Flujo + fórmulas | 680×330 |
| D4 | Los tres medios de transmisión guiados comparados | §2.1.1 | Comparativa | 680×356 |
| D5 | El espectro radioeléctrico: bandas de la UIT y regla de la frecuencia | §2.2.1 | Escala + regla | 680×352 |
| D6 | Parámetros de calidad de un enlace y qué degrada cada uno | §2.3 | Tabla visual | 680×330 |
| D7 | Símplex, semidúplex y dúplex | §3.1 | Comparativa | 680×300 |
| D8 | Sincronismo y forma de transmisión: asíncrona/síncrona y serie/paralelo | §3.2 y §3.3 | Estructura + comparativa | 680×336 |
| D9 | Equipos de interconexión clasificados por capa | §4.2.1 | Capas | 680×344 |
| D10 | Dominios de colisión y dominios de difusión | §4.2.1 | Esquema | 680×330 |
| D11 | Redes por cobertura geográfica: PAN, LAN, MAN y WAN | §5.1 | Escala | 680×326 |
| D12 | Topologías físicas de red y su tolerancia a fallos | §5.2 | Comparativa | 680×352 |
| D13 | Conmutación de circuitos, de mensajes y de paquetes | §6.1.1 | Comparativa + tiempos | 680×360 |
| D14 | Modos de entrega y direcciones de difusión y multidifusión | §6.2.1 | Esquema + tabla | 680×344 |
| D15 | Redes inalámbricas: escala, arquitectura Wi-Fi y generaciones | §7 | Capas + escalera | 680×356 |
| D16 | La red celular: principio celular y evolución de 1G a 5G | §8.1 y §8.2 | Esquema + línea temporal | 680×360 |
| D17 | Seguridad inalámbrica: de WEP a WPA3 y medidas `mp.com` del ENS | §9.1 | Escalera + tabla | 680×356 |
| D18 | La Ley 11/2022: estructura, servicio universal y art. 13 | §9.2 | Capas | 680×352 |

---

## D1 · El modelo de comunicación de Shannon: los cinco elementos

**Sección**: §1.1.1 — Elementos del sistema de transmisión y perturbaciones en el canal
**Propósito**: Fijar los cinco elementos en su orden correcto y, sobre todo, dejar claro que el ruido ataca **al canal**, que es el detalle de dibujo clave.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Modelo de comunicación de Shannon con sus cinco elementos en cadena: fuente de información, transmisor, canal, receptor y destino, con la fuente de ruido actuando sobre el canal y no sobre el mensaje">
  <style>.t1{font:700 10.5px system-ui,sans-serif;fill:#fff}.s1{font:8.5px system-ui,sans-serif;fill:#fff}.d1{font:9px system-ui,sans-serif;fill:#333}.h1{font:700 13px system-ui,sans-serif;fill:#0055a0}.k1{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n1{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a1" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="#666"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h1">Los cinco elementos y dónde entra el ruido</text>
  <rect x="20" y="46" width="120" height="52" rx="5" fill="#0055a0"/><text x="80" y="66" text-anchor="middle" class="t1">FUENTE</text><text x="80" y="80" text-anchor="middle" class="s1">genera el</text><text x="80" y="92" text-anchor="middle" class="s1">mensaje</text>
  <rect x="150" y="46" width="120" height="52" rx="5" fill="#0055a0"/><text x="210" y="66" text-anchor="middle" class="t1">TRANSMISOR</text><text x="210" y="80" text-anchor="middle" class="s1">codifica y</text><text x="210" y="92" text-anchor="middle" class="s1">modula</text>
  <rect x="280" y="46" width="120" height="52" rx="5" fill="#e89822"/><text x="340" y="66" text-anchor="middle" class="t1">CANAL</text><text x="340" y="80" text-anchor="middle" class="s1">medio de</text><text x="340" y="92" text-anchor="middle" class="s1">transmisión</text>
  <rect x="410" y="46" width="120" height="52" rx="5" fill="#0055a0"/><text x="470" y="66" text-anchor="middle" class="t1">RECEPTOR</text><text x="470" y="80" text-anchor="middle" class="s1">demodula y</text><text x="470" y="92" text-anchor="middle" class="s1">decodifica</text>
  <rect x="540" y="46" width="120" height="52" rx="5" fill="#0055a0"/><text x="600" y="66" text-anchor="middle" class="t1">DESTINO</text><text x="600" y="80" text-anchor="middle" class="s1">recibe el</text><text x="600" y="92" text-anchor="middle" class="s1">mensaje</text>
  <path d="M140 72 L146 72" stroke="#666" stroke-width="1.5" marker-end="url(#a1)"/>
  <path d="M270 72 L276 72" stroke="#666" stroke-width="1.5" marker-end="url(#a1)"/>
  <path d="M400 72 L406 72" stroke="#666" stroke-width="1.5" marker-end="url(#a1)"/>
  <path d="M530 72 L536 72" stroke="#666" stroke-width="1.5" marker-end="url(#a1)"/>
  <path d="M340 146 L340 104" stroke="#d13c3c" stroke-width="2" marker-end="url(#a1)"/>
  <rect x="250" y="150" width="180" height="34" rx="5" fill="#d13c3c"/><text x="340" y="171" text-anchor="middle" class="t1">FUENTE DE RUIDO</text>
  <rect x="20" y="200" width="640" height="26" rx="4" fill="#fdf3e3"/>
  <text x="340" y="217" text-anchor="middle" class="d1">El ruido se suma a la señal DURANTE su tránsito por el canal, no en el mensaje ni en los equipos</text>
  <rect x="20" y="238" width="640" height="42" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="255" text-anchor="middle" class="k1">Versión de 7 elementos (modelo de comunicación de datos)</text>
  <text x="340" y="270" text-anchor="middle" class="n1">emisor · receptor · mensaje · medio · protocolo, más la codificación y la decodificación</text>
  <text x="670" y="294" text-anchor="end" class="n1">[Fuente: SHANNON, 1948]</text>
</svg>
```

---

## D2 · Perturbaciones del canal: atenuación, distorsión, ruido e interferencia

**Sección**: §1.1.1 — Elementos del sistema de transmisión y perturbaciones en el canal
**Propósito**: Separar con precisión las cinco familias de perturbación, que se confunden entre sí, e identificar el remedio de cada una.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Las cinco familias de perturbaciones del canal: atenuación, distorsión, ruido con sus cuatro tipos, interferencia y eco, con la definición y el remedio de cada una y el aviso de que el ruido impulsivo es el más dañino en transmisión digital">
  <style>.t2{font:700 10.5px system-ui,sans-serif;fill:#fff}.s2{font:8.5px system-ui,sans-serif;fill:#fff}.d2{font:9px system-ui,sans-serif;fill:#333}.h2{font:700 13px system-ui,sans-serif;fill:#0055a0}.k2{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n2{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h2">Qué le pasa a la señal por el camino</text>
  <text x="26" y="42" class="k2">PERTURBACIÓN</text><text x="220" y="42" class="k2">QUÉ HACE</text><text x="470" y="42" class="k2">REMEDIO</text>
  <rect x="20" y="50" width="180" height="34" rx="4" fill="#0055a0"/><text x="110" y="71" text-anchor="middle" class="t2">ATENUACIÓN</text>
  <rect x="208" y="50" width="250" height="34" rx="4" fill="#eef3f8"/><text x="333" y="71" text-anchor="middle" class="d2">Pierde potencia con la distancia</text>
  <rect x="466" y="50" width="194" height="34" rx="4" fill="#f5f5f5"/><text x="563" y="71" text-anchor="middle" class="d2">Repetidor regenerador</text>
  <rect x="20" y="90" width="180" height="34" rx="4" fill="#0055a0"/><text x="110" y="111" text-anchor="middle" class="t2">DISTORSIÓN</text>
  <rect x="208" y="90" width="250" height="34" rx="4" fill="#eef3f8"/><text x="333" y="111" text-anchor="middle" class="d2">Se deforma: retardo diferencial e ISI</text>
  <rect x="466" y="90" width="194" height="34" rx="4" fill="#f5f5f5"/><text x="563" y="111" text-anchor="middle" class="d2">Ecualizador</text>
  <rect x="20" y="130" width="180" height="34" rx="4" fill="#d13c3c"/><text x="110" y="151" text-anchor="middle" class="t2">RUIDO</text>
  <rect x="208" y="130" width="250" height="34" rx="4" fill="#fbeaea"/><text x="333" y="151" text-anchor="middle" class="d2">Se le suma energía ajena</text>
  <rect x="466" y="130" width="194" height="34" rx="4" fill="#f5f5f5"/><text x="563" y="151" text-anchor="middle" class="d2">Códigos correctores, blindaje</text>
  <rect x="20" y="170" width="180" height="34" rx="4" fill="#e89822"/><text x="110" y="191" text-anchor="middle" class="t2">INTERFERENCIA</text>
  <rect x="208" y="170" width="250" height="34" rx="4" fill="#fdf3e3"/><text x="333" y="191" text-anchor="middle" class="d2">Otro emisor se superpone</text>
  <rect x="466" y="170" width="194" height="34" rx="4" fill="#f5f5f5"/><text x="563" y="191" text-anchor="middle" class="d2">Plan de frecuencias, fibra óptica</text>
  <rect x="20" y="210" width="180" height="34" rx="4" fill="#7a2f8a"/><text x="110" y="231" text-anchor="middle" class="t2">ECO Y FLUCTUACIÓN</text>
  <rect x="208" y="210" width="250" height="34" rx="4" fill="#eef3f8"/><text x="333" y="231" text-anchor="middle" class="d2">Vuelve reflejada o llega irregular</text>
  <rect x="466" y="210" width="194" height="34" rx="4" fill="#f5f5f5"/><text x="563" y="231" text-anchor="middle" class="d2">Cancelador de eco, memoria intermedia</text>
  <text x="26" y="264" class="k2">LOS CUATRO TIPOS DE RUIDO</text>
  <rect x="20" y="272" width="155" height="30" rx="4" fill="#eef3f8"/><text x="97" y="291" text-anchor="middle" class="d2">Térmico: inevitable</text>
  <rect x="182" y="272" width="155" height="30" rx="4" fill="#eef3f8"/><text x="259" y="291" text-anchor="middle" class="d2">Intermodulación</text>
  <rect x="344" y="272" width="155" height="30" rx="4" fill="#eef3f8"/><text x="421" y="291" text-anchor="middle" class="d2">Diafonía entre pares</text>
  <rect x="506" y="272" width="154" height="30" rx="4" fill="#fbeaea"/><text x="583" y="291" text-anchor="middle" class="d2">Impulsivo: el peor</text>
  <text x="340" y="320" text-anchor="middle" class="n2">El ruido impulsivo es el más dañino en transmisión DIGITAL: destruye bloques enteros de bits</text>
  <text x="670" y="334" text-anchor="end" class="n2">[Fuente: STALLINGS]</text>
</svg>
```

---

## D3 · De la señal a los bits: muestreo, Nyquist y Shannon

**Sección**: §1.2 — Transmisión analógica y digital: ancho de banda y velocidad de transmisión
**Propósito**: Reunir en una sola imagen las tres fórmulas que hay que saber de memoria y el cálculo del canal de 64 kbps, que es el ejercicio numérico más repetido del bloque.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 330" role="img" aria-label="Digitalización de una señal analógica en tres pasos, muestreo cuantificación y codificación, con el teorema del muestreo, las fórmulas de capacidad de Nyquist y de Shannon y el cálculo del canal telefónico digital de 64 kilobits por segundo">
  <style>.t3{font:700 10.5px system-ui,sans-serif;fill:#fff}.s3{font:8.5px system-ui,sans-serif;fill:#fff}.d3{font:9px system-ui,sans-serif;fill:#333}.h3{font:700 13px system-ui,sans-serif;fill:#0055a0}.k3{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n3{font:8.5px system-ui,sans-serif;fill:#666}.f3{font:700 11px ui-monospace,monospace;fill:#0055a0}</style>
  <defs><marker id="a3" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="#666"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h3">Del sonido al bit, y cuánto cabe por el canal</text>
  <text x="26" y="42" class="k3">DIGITALIZAR: TRES PASOS EN ESTE ORDEN</text>
  <rect x="20" y="50" width="200" height="40" rx="5" fill="#0055a0"/><text x="120" y="68" text-anchor="middle" class="t3">1 · MUESTREO</text><text x="120" y="82" text-anchor="middle" class="s3">tomar valores periódicos</text>
  <rect x="240" y="50" width="200" height="40" rx="5" fill="#0055a0"/><text x="340" y="68" text-anchor="middle" class="t3">2 · CUANTIFICACIÓN</text><text x="340" y="82" text-anchor="middle" class="s3">aproximar a niveles</text>
  <rect x="460" y="50" width="200" height="40" rx="5" fill="#0055a0"/><text x="560" y="68" text-anchor="middle" class="t3">3 · CODIFICACIÓN</text><text x="560" y="82" text-anchor="middle" class="s3">asignar bits</text>
  <path d="M220 70 L236 70" stroke="#666" stroke-width="1.5" marker-end="url(#a3)"/>
  <path d="M440 70 L456 70" stroke="#666" stroke-width="1.5" marker-end="url(#a3)"/>
  <text x="26" y="118" class="k3">LAS TRES FÓRMULAS</text>
  <rect x="20" y="126" width="206" height="46" rx="5" fill="#eef3f8"/><text x="123" y="144" text-anchor="middle" class="f3">fm &gt;= 2 · fmax</text><text x="123" y="162" text-anchor="middle" class="n3">teorema del muestreo</text>
  <rect x="237" y="126" width="206" height="46" rx="5" fill="#eef3f8"/><text x="340" y="144" text-anchor="middle" class="f3">C = 2·B·log2(M)</text><text x="340" y="162" text-anchor="middle" class="n3">Nyquist: canal SIN ruido</text>
  <rect x="454" y="126" width="206" height="46" rx="5" fill="#fdf3e3"/><text x="557" y="144" text-anchor="middle" class="f3">C = B·log2(1+S/N)</text><text x="557" y="162" text-anchor="middle" class="n3">Shannon: canal CON ruido</text>
  <rect x="20" y="182" width="640" height="24" rx="4" fill="#fbeaea"/>
  <text x="340" y="198" text-anchor="middle" class="d3">En Shannon, S/N va EN VECES, no en decibelios: 30 dB = 1000 veces · 20 dB = 100 · 10 dB = 10 · 3 dB = 2</text>
  <text x="26" y="230" class="k3">EL CANAL TELEFÓNICO DIGITAL, PASO A PASO</text>
  <rect x="20" y="238" width="155" height="40" rx="4" fill="#2d8659"/><text x="97" y="256" text-anchor="middle" class="t3">Voz 300-3400 Hz</text><text x="97" y="270" text-anchor="middle" class="s3">fmax = 3400</text>
  <rect x="182" y="238" width="155" height="40" rx="4" fill="#2d8659"/><text x="259" y="256" text-anchor="middle" class="t3">8000 muestras/s</text><text x="259" y="270" text-anchor="middle" class="s3">normalizado</text>
  <rect x="344" y="238" width="155" height="40" rx="4" fill="#2d8659"/><text x="421" y="256" text-anchor="middle" class="t3">8 bits/muestra</text><text x="421" y="270" text-anchor="middle" class="s3">256 niveles</text>
  <rect x="506" y="238" width="154" height="40" rx="4" fill="#e89822"/><text x="583" y="256" text-anchor="middle" class="t3">64 kbit/s = E0</text><text x="583" y="270" text-anchor="middle" class="s3">32 E0 = E1 2,048 Mbit/s</text>
  <text x="340" y="306" text-anchor="middle" class="n3">Ancho de banda en HERCIOS · velocidad de transmisión en BITS/S · velocidad de modulación en BAUDIOS</text>
  <text x="670" y="324" text-anchor="end" class="n3">[Fuente: NYQUIST; SHANNON; UIT-T G.704]</text>
</svg>
```

---

## D4 · Los tres medios de transmisión guiados comparados

**Sección**: §2.1.1 — Par trenzado, cable coaxial y fibra óptica
**Propósito**: Poner en la misma escala los tres medios guiados y anclar los datos numéricos clave: los 100 metros del cobre, los diámetros de núcleo y las ventanas de la fibra.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 356" role="img" aria-label="Comparación de los tres medios de transmisión guiados: par trenzado con sus categorías y el límite de cien metros, cable coaxial de cincuenta y setenta y cinco ohmios, y fibra óptica monomodo y multimodo con sus diámetros de núcleo y sus ventanas de trabajo">
  <style>.t4{font:700 10.5px system-ui,sans-serif;fill:#fff}.s4{font:8.5px system-ui,sans-serif;fill:#fff}.d4{font:9px system-ui,sans-serif;fill:#333}.h4{font:700 13px system-ui,sans-serif;fill:#0055a0}.k4{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n4{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h4">Cobre trenzado, coaxial y luz</text>
  <rect x="20" y="34" width="206" height="30" rx="5" fill="#0055a0"/><text x="123" y="54" text-anchor="middle" class="t4">PAR TRENZADO</text>
  <rect x="237" y="34" width="206" height="30" rx="5" fill="#0055a0"/><text x="340" y="54" text-anchor="middle" class="t4">CABLE COAXIAL</text>
  <rect x="454" y="34" width="206" height="30" rx="5" fill="#2d8659"/><text x="557" y="54" text-anchor="middle" class="t4">FIBRA ÓPTICA</text>
  <rect x="20" y="70" width="206" height="94" rx="4" fill="#eef3f8"/>
  <text x="123" y="88" text-anchor="middle" class="d4">Dos hilos trenzados; el trenzado</text><text x="123" y="102" text-anchor="middle" class="d4">cancela la diafonía</text>
  <text x="123" y="120" text-anchor="middle" class="d4">UTP · FTP · STP · S/FTP</text>
  <text x="123" y="138" text-anchor="middle" class="d4">Cat 5e · 6 · 6A · 7 · 8</text>
  <text x="123" y="156" text-anchor="middle" class="d4">Conector RJ-45 · admite PoE</text>
  <rect x="237" y="70" width="206" height="94" rx="4" fill="#eef3f8"/>
  <text x="340" y="88" text-anchor="middle" class="d4">Conductor central más malla</text><text x="340" y="102" text-anchor="middle" class="d4">apantallada concéntrica</text>
  <text x="340" y="120" text-anchor="middle" class="d4">50 ohmios: digital banda base</text>
  <text x="340" y="138" text-anchor="middle" class="d4">75 ohmios: TV y cable</text>
  <text x="340" y="156" text-anchor="middle" class="d4">Topología natural: BUS</text>
  <rect x="454" y="70" width="206" height="94" rx="4" fill="#e8f4ee"/>
  <text x="557" y="88" text-anchor="middle" class="d4">Núcleo y revestimiento; la luz</text><text x="557" y="102" text-anchor="middle" class="d4">avanza por reflexión total</text>
  <text x="557" y="120" text-anchor="middle" class="d4">Inmune a interferencias</text>
  <text x="557" y="138" text-anchor="middle" class="d4">Sin diafonía · no radia</text>
  <text x="557" y="156" text-anchor="middle" class="d4">No transporta energía</text>
  <rect x="20" y="176" width="640" height="26" rx="4" fill="#fdf3e3"/>
  <text x="340" y="193" text-anchor="middle" class="d4">LÍMITE DEL COBRE EN ETHERNET: 100 m de enlace = 90 m de cable horizontal + 10 m de latiguillos</text>
  <text x="26" y="226" class="k4">MONOMODO FRENTE A MULTIMODO</text>
  <rect x="20" y="234" width="315" height="70" rx="4" fill="#0055a0"/>
  <text x="177" y="252" text-anchor="middle" class="t4">MULTIMODO — OM1 a OM5</text>
  <text x="177" y="268" text-anchor="middle" class="s4">Núcleo 50 o 62,5 micras · LED o VCSEL</text>
  <text x="177" y="282" text-anchor="middle" class="s4">Dispersión modal · decenas o cientos de metros</text>
  <text x="177" y="295" text-anchor="middle" class="s4">Vertical de edificio y centro de datos</text>
  <rect x="345" y="234" width="315" height="70" rx="4" fill="#2d8659"/>
  <text x="502" y="252" text-anchor="middle" class="t4">MONOMODO — OS1 y OS2</text>
  <text x="502" y="268" text-anchor="middle" class="s4">Núcleo 9 micras aprox. · diodo láser</text>
  <text x="502" y="282" text-anchor="middle" class="s4">Decenas o cientos de kilómetros</text>
  <text x="502" y="295" text-anchor="middle" class="s4">Enlaces entre sedes, acceso FTTH, troncal</text>
  <rect x="20" y="312" width="640" height="24" rx="4" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="328" text-anchor="middle" class="k4">A MAYOR NÚCLEO, MÁS MODOS, MÁS DISPERSIÓN Y MENOS ALCANCE · ventanas 850, 1310 y 1550 nm</text>
  <text x="670" y="350" text-anchor="end" class="n4">[Fuente: ISO/IEC 11801; IEEE 802.3]</text>
</svg>
```

---

## D5 · El espectro radioeléctrico: bandas de la UIT y regla de la frecuencia

**Sección**: §2.2.1 — Espectro radioeléctrico, radiofrecuencia, microondas e infrarrojos
**Propósito**: Ordenar las bandas decádicas con su uso característico y dejar grabada la regla de oro —a más frecuencia, más capacidad y menos alcance—, que explica todas las decisiones de espectro del tema.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="Bandas del espectro radioeléctrico según la Unión Internacional de Telecomunicaciones, de muy baja frecuencia a extra alta frecuencia, con el uso característico de cada una y la regla de que a mayor frecuencia hay más capacidad pero menos alcance y peor penetración">
  <style>.t5{font:700 10px system-ui,sans-serif;fill:#fff}.s5{font:8.5px system-ui,sans-serif;fill:#fff}.d5{font:9px system-ui,sans-serif;fill:#333}.h5{font:700 13px system-ui,sans-serif;fill:#0055a0}.k5{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n5{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a5" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h5">Ocho bandas decádicas y una sola regla</text>
  <text x="26" y="42" class="k5">BANDA</text><text x="140" y="42" class="k5">FRECUENCIAS</text><text x="300" y="42" class="k5">USO CARACTERÍSTICO</text>
  <rect x="20" y="50" width="106" height="26" rx="3" fill="#8fa9c4"/><text x="73" y="67" text-anchor="middle" class="t5">VLF · LF</text>
  <rect x="132" y="50" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="67" text-anchor="middle" class="d5">3 kHz - 300 kHz</text>
  <rect x="288" y="50" width="372" height="26" rx="3" fill="#eef3f8"/><text x="474" y="67" text-anchor="middle" class="d5">Submarinos, radionavegación, onda larga</text>
  <rect x="20" y="80" width="106" height="26" rx="3" fill="#7196b8"/><text x="73" y="97" text-anchor="middle" class="t5">MF</text>
  <rect x="132" y="80" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="97" text-anchor="middle" class="d5">300 kHz - 3 MHz</text>
  <rect x="288" y="80" width="372" height="26" rx="3" fill="#eef3f8"/><text x="474" y="97" text-anchor="middle" class="d5">Radiodifusión en onda media (AM) · onda de superficie</text>
  <rect x="20" y="110" width="106" height="26" rx="3" fill="#5384ac"/><text x="73" y="127" text-anchor="middle" class="t5">HF</text>
  <rect x="132" y="110" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="127" text-anchor="middle" class="d5">3 - 30 MHz</text>
  <rect x="288" y="110" width="372" height="26" rx="3" fill="#eef3f8"/><text x="474" y="127" text-anchor="middle" class="d5">Onda corta · propagación IONOSFÉRICA intercontinental</text>
  <rect x="20" y="140" width="106" height="26" rx="3" fill="#3571a0"/><text x="73" y="157" text-anchor="middle" class="t5">VHF</text>
  <rect x="132" y="140" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="157" text-anchor="middle" class="d5">30 - 300 MHz</text>
  <rect x="288" y="140" width="372" height="26" rx="3" fill="#eef3f8"/><text x="474" y="157" text-anchor="middle" class="d5">Radio FM, aviación, marina · empieza la visión directa</text>
  <rect x="20" y="170" width="106" height="26" rx="3" fill="#0055a0"/><text x="73" y="187" text-anchor="middle" class="t5">UHF</text>
  <rect x="132" y="170" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="187" text-anchor="middle" class="d5">300 MHz - 3 GHz</text>
  <rect x="288" y="170" width="372" height="26" rx="3" fill="#fdf3e3"/><text x="474" y="187" text-anchor="middle" class="d5">TDT, móvil 700 MHz, TETRA, Wi-Fi de 2,4 GHz</text>
  <rect x="20" y="200" width="106" height="26" rx="3" fill="#e89822"/><text x="73" y="217" text-anchor="middle" class="t5">SHF</text>
  <rect x="132" y="200" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="217" text-anchor="middle" class="d5">3 - 30 GHz</text>
  <rect x="288" y="200" width="372" height="26" rx="3" fill="#fdf3e3"/><text x="474" y="217" text-anchor="middle" class="d5">Microondas y satélite · Wi-Fi de 5 y 6 GHz · 5G de 26 GHz</text>
  <rect x="20" y="230" width="106" height="26" rx="3" fill="#d13c3c"/><text x="73" y="247" text-anchor="middle" class="t5">EHF</text>
  <rect x="132" y="230" width="150" height="26" rx="3" fill="#f5f5f5"/><text x="207" y="247" text-anchor="middle" class="d5">30 - 300 GHz</text>
  <rect x="288" y="230" width="372" height="26" rx="3" fill="#fbeaea"/><text x="474" y="247" text-anchor="middle" class="d5">Ondas milimétricas · radioenlaces de gran capacidad</text>
  <path d="M40 270 L640 270" stroke="#0055a0" stroke-width="2" marker-end="url(#a5)"/>
  <text x="40" y="286" class="n5">menos frecuencia</text>
  <text x="640" y="286" text-anchor="end" class="n5">más frecuencia</text>
  <rect x="20" y="294" width="640" height="34" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="309" text-anchor="middle" class="k5">A MAYOR FRECUENCIA: más ancho de banda y capacidad, antenas más pequeñas</text>
  <text x="340" y="323" text-anchor="middle" class="n5">pero MENOS alcance, PEOR penetración en obstáculos y más sensibilidad a la lluvia</text>
  <text x="670" y="346" text-anchor="end" class="n5">[Fuente: UIT-R; LGT art. 85 y anexo II.21]</text>
</svg>
```

---

## D6 · Parámetros de calidad de un enlace y qué degrada cada uno

**Sección**: §2.3 — Parámetros de caracterización y calidad en medios de transmisión
**Propósito**: Fijar la unidad de cada parámetro y separar latencia de fluctuación, que es la confusión más frecuente al interpretar un acuerdo de nivel de servicio.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 330" role="img" aria-label="Parámetros de calidad de un enlace con su unidad de medida: ancho de banda en hercios, caudal en bits por segundo, atenuación y relación señal ruido en decibelios, latencia y fluctuación en milisegundos, tasa de error de bit y pérdida de paquetes, con la advertencia de que el decibelio es logarítmico">
  <style>.t6{font:700 10px system-ui,sans-serif;fill:#fff}.s6{font:8.5px system-ui,sans-serif;fill:#fff}.d6{font:9px system-ui,sans-serif;fill:#333}.h6{font:700 13px system-ui,sans-serif;fill:#0055a0}.k6{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n6{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h6">Qué se mide, en qué unidad y qué lo estropea</text>
  <text x="26" y="42" class="k6">PARÁMETRO</text><text x="200" y="42" class="k6">UNIDAD</text><text x="330" y="42" class="k6">QUÉ LO DEGRADA</text>
  <rect x="20" y="50" width="170" height="24" rx="3" fill="#0055a0"/><text x="105" y="66" text-anchor="middle" class="t6">Ancho de banda</text>
  <rect x="196" y="50" width="120" height="24" rx="3" fill="#eef3f8"/><text x="256" y="66" text-anchor="middle" class="d6">hercios (Hz)</text>
  <rect x="322" y="50" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="66" text-anchor="middle" class="d6">Es una propiedad física del medio</text>
  <rect x="20" y="78" width="170" height="24" rx="3" fill="#0055a0"/><text x="105" y="94" text-anchor="middle" class="t6">Caudal efectivo</text>
  <rect x="196" y="78" width="120" height="24" rx="3" fill="#eef3f8"/><text x="256" y="94" text-anchor="middle" class="d6">bits/s</text>
  <rect x="322" y="78" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="94" text-anchor="middle" class="d6">Cabeceras, colisiones, retransmisiones</text>
  <rect x="20" y="106" width="170" height="24" rx="3" fill="#e89822"/><text x="105" y="122" text-anchor="middle" class="t6">Atenuación</text>
  <rect x="196" y="106" width="120" height="24" rx="3" fill="#fdf3e3"/><text x="256" y="122" text-anchor="middle" class="d6">dB o dB/km</text>
  <rect x="322" y="106" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="122" text-anchor="middle" class="d6">Distancia y frecuencia</text>
  <rect x="20" y="134" width="170" height="24" rx="3" fill="#e89822"/><text x="105" y="150" text-anchor="middle" class="t6">Relación señal-ruido</text>
  <rect x="196" y="134" width="120" height="24" rx="3" fill="#fdf3e3"/><text x="256" y="150" text-anchor="middle" class="d6">dB</text>
  <rect x="322" y="134" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="150" text-anchor="middle" class="d6">Ruido térmico e interferencias</text>
  <rect x="20" y="162" width="170" height="24" rx="3" fill="#2d8659"/><text x="105" y="178" text-anchor="middle" class="t6">Latencia</text>
  <rect x="196" y="162" width="120" height="24" rx="3" fill="#e8f4ee"/><text x="256" y="178" text-anchor="middle" class="d6">milisegundos</text>
  <rect x="322" y="162" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="178" text-anchor="middle" class="d6">Distancia, número de saltos, encolamiento</text>
  <rect x="20" y="190" width="170" height="24" rx="3" fill="#2d8659"/><text x="105" y="206" text-anchor="middle" class="t6">Fluctuación (jitter)</text>
  <rect x="196" y="190" width="120" height="24" rx="3" fill="#e8f4ee"/><text x="256" y="206" text-anchor="middle" class="d6">milisegundos</text>
  <rect x="322" y="190" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="206" text-anchor="middle" class="d6">Colas variables y rutas distintas</text>
  <rect x="20" y="218" width="170" height="24" rx="3" fill="#d13c3c"/><text x="105" y="234" text-anchor="middle" class="t6">Tasa de error (BER)</text>
  <rect x="196" y="218" width="120" height="24" rx="3" fill="#fbeaea"/><text x="256" y="234" text-anchor="middle" class="d6">adimensional</text>
  <rect x="322" y="218" width="338" height="24" rx="3" fill="#f5f5f5"/><text x="491" y="234" text-anchor="middle" class="d6">Ruido, interferencia, atenuación excesiva</text>
  <rect x="20" y="252" width="316" height="42" rx="5" fill="#eef3f8"/>
  <text x="178" y="270" text-anchor="middle" class="k6">LATENCIA vs FLUCTUACIÓN</text>
  <text x="178" y="286" text-anchor="middle" class="n6">La transferencia sufre con la latencia; la VOZ, con la fluctuación</text>
  <rect x="344" y="252" width="316" height="42" rx="5" fill="#fdf3e3"/>
  <text x="502" y="270" text-anchor="middle" class="k6">EL DECIBELIO ES LOGARÍTMICO</text>
  <text x="502" y="286" text-anchor="middle" class="n6">3 dB = doble · 10 dB = x10 · 20 dB = x100 · 30 dB = x1000</text>
  <text x="340" y="312" text-anchor="middle" class="n6">Las atenuaciones en decibelios de tramos sucesivos SE SUMAN, no se multiplican</text>
  <text x="670" y="326" text-anchor="end" class="n6">[Fuente: STALLINGS; UIT-T]</text>
</svg>
```

---

## D7 · Símplex, semidúplex y dúplex

**Sección**: §3.1 — Modos según la direccionalidad: símplex, half-dúplex y full-dúplex
**Propósito**: Separar los tres modos por la **simultaneidad** —no por la bidireccionalidad— y justificar por qué el Wi-Fi es semidúplex, que es la trampa recurrente.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Los tres modos de direccionalidad: símplex en un solo sentido, semidúplex en los dos sentidos alternando y dúplex en los dos sentidos a la vez, con ejemplos y con la explicación de por que el Wi-Fi es semidúplex">
  <style>.t7{font:700 10.5px system-ui,sans-serif;fill:#fff}.s7{font:8.5px system-ui,sans-serif;fill:#fff}.d7{font:9px system-ui,sans-serif;fill:#333}.h7{font:700 13px system-ui,sans-serif;fill:#0055a0}.k7{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n7{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a7" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h7">Lo que separa los tres modos es la SIMULTANEIDAD</text>
  <rect x="20" y="36" width="206" height="28" rx="5" fill="#0055a0"/><text x="123" y="55" text-anchor="middle" class="t7">SÍMPLEX</text>
  <rect x="237" y="36" width="206" height="28" rx="5" fill="#e89822"/><text x="340" y="55" text-anchor="middle" class="t7">SEMIDÚPLEX (half)</text>
  <rect x="454" y="36" width="206" height="28" rx="5" fill="#2d8659"/><text x="557" y="55" text-anchor="middle" class="t7">DÚPLEX (full)</text>
  <rect x="20" y="70" width="206" height="76" rx="4" fill="#eef3f8"/>
  <text x="123" y="88" text-anchor="middle" class="d7">Un solo sentido, siempre el mismo</text>
  <path d="M50 104 L196 104" stroke="#0055a0" stroke-width="2" marker-end="url(#a7)"/>
  <text x="123" y="124" text-anchor="middle" class="d7">Radio, TDT, panel informativo</text>
  <text x="123" y="138" text-anchor="middle" class="n7">no hay canal de vuelta</text>
  <rect x="237" y="70" width="206" height="76" rx="4" fill="#fdf3e3"/>
  <text x="340" y="88" text-anchor="middle" class="d7">Los dos sentidos, ALTERNANDO</text>
  <path d="M267 100 L413 100" stroke="#0055a0" stroke-width="2" marker-end="url(#a7)"/>
  <path d="M413 112 L267 112" stroke="#888" stroke-width="2" stroke-dasharray="4 3" marker-end="url(#a7)"/>
  <text x="340" y="128" text-anchor="middle" class="d7">Walkie-talkie, TETRA, Wi-Fi</text>
  <text x="340" y="140" text-anchor="middle" class="n7">hace falta arbitrar el turno</text>
  <rect x="454" y="70" width="206" height="76" rx="4" fill="#e8f4ee"/>
  <text x="557" y="88" text-anchor="middle" class="d7">Los dos sentidos, A LA VEZ</text>
  <path d="M484 100 L630 100" stroke="#0055a0" stroke-width="2" marker-end="url(#a7)"/>
  <path d="M630 112 L484 112" stroke="#0055a0" stroke-width="2" marker-end="url(#a7)"/>
  <text x="557" y="128" text-anchor="middle" class="d7">Telefonía, Ethernet conmutado</text>
  <text x="557" y="140" text-anchor="middle" class="n7">dos canales, o FDD, o TDD</text>
  <rect x="20" y="156" width="640" height="26" rx="4" fill="#fbeaea"/>
  <text x="340" y="173" text-anchor="middle" class="d7">EL WI-FI ES SEMIDÚPLEX: una antena que transmite no puede escuchar su propia frecuencia</text>
  <rect x="20" y="192" width="640" height="26" rx="4" fill="#eef3f8"/>
  <text x="340" y="209" text-anchor="middle" class="d7">Por esa misma razón la radio usa CSMA/CA (evitación) y no CSMA/CD (detección de colisión)</text>
  <rect x="20" y="230" width="640" height="42" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="247" text-anchor="middle" class="k7">TDD NO ES SEMIDÚPLEX</text>
  <text x="340" y="263" text-anchor="middle" class="n7">El TDD alterna turnos en microsegundos y el servicio percibido es dúplex; el semidúplex se nota</text>
  <text x="670" y="294" text-anchor="end" class="n7">[Fuente: FOROUZAN; IEEE 802.11]</text>
</svg>
```

---

## D8 · Sincronismo y forma de transmisión: asíncrona/síncrona y serie/paralelo

**Sección**: §3.2 — Modos según el sincronismo · §3.3 — Modos según la forma de transmisión
**Propósito**: Mostrar la estructura real de un carácter asíncrono —de donde sale la sobrecarga del 27 %— y justificar por qué el paralelo perdió la batalla a alta velocidad.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 336" role="img" aria-label="Estructura de un carácter en transmisión asíncrona con bit de arranque, ocho bits de datos, paridad y bit de parada, comparada con la trama síncrona, y comparación entre transmisión serie y paralelo con las tres razones por las que el paralelo no escala">
  <style>.t8{font:700 10px system-ui,sans-serif;fill:#fff}.s8{font:8.5px system-ui,sans-serif;fill:#fff}.d8{font:9px system-ui,sans-serif;fill:#333}.h8{font:700 13px system-ui,sans-serif;fill:#0055a0}.k8{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n8{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h8">Cómo se delimita y cómo se lanza cada bit</text>
  <text x="26" y="42" class="k8">ASÍNCRONA · UN CARÁCTER, ONCE BITS</text>
  <rect x="20" y="50" width="58" height="30" rx="3" fill="#2d8659"/><text x="49" y="69" text-anchor="middle" class="t8">START</text>
  <rect x="82" y="50" width="380" height="30" rx="3" fill="#0055a0"/><text x="272" y="69" text-anchor="middle" class="t8">8 BITS DE DATOS</text>
  <rect x="466" y="50" width="90" height="30" rx="3" fill="#e89822"/><text x="511" y="69" text-anchor="middle" class="t8">PARIDAD</text>
  <rect x="560" y="50" width="100" height="30" rx="3" fill="#d13c3c"/><text x="610" y="69" text-anchor="middle" class="t8">STOP</text>
  <text x="340" y="96" text-anchor="middle" class="d8">Eficiencia = 8/11 = 72,7 % · SOBRECARGA = 27,3 % del canal, siempre, independiente del volumen</text>
  <text x="26" y="120" class="k8">SÍNCRONA · UNA TRAMA, MILES DE BITS</text>
  <rect x="20" y="128" width="110" height="30" rx="3" fill="#2d8659"/><text x="75" y="147" text-anchor="middle" class="t8">PREÁMBULO</text>
  <rect x="134" y="128" width="410" height="30" rx="3" fill="#0055a0"/><text x="339" y="147" text-anchor="middle" class="t8">BLOQUE DE DATOS</text>
  <rect x="548" y="128" width="112" height="30" rx="3" fill="#d13c3c"/><text x="604" y="147" text-anchor="middle" class="t8">CRC · FIN</text>
  <text x="340" y="174" text-anchor="middle" class="d8">Reloj común o extraído de la señal (Manchester, 4B/5B, 8B/10B) · sobrecarga despreciable</text>
  <text x="26" y="198" class="k8">SERIE FRENTE A PARALELO</text>
  <rect x="20" y="206" width="316" height="76" rx="5" fill="#0055a0"/>
  <text x="178" y="224" text-anchor="middle" class="t8">SERIE — un bit detrás de otro</text>
  <text x="178" y="240" text-anchor="middle" class="s8">Pocos hilos · gran distancia · muy alta frecuencia</text>
  <text x="178" y="255" text-anchor="middle" class="s8">USB, SATA, PCIe, Ethernet, fibra, radio</text>
  <text x="178" y="273" text-anchor="middle" class="s8">Para ir más rápido: agrupar varios canales serie</text>
  <rect x="344" y="206" width="316" height="76" rx="5" fill="#8a8a8a"/>
  <text x="502" y="224" text-anchor="middle" class="t8">PARALELO — n bits a la vez</text>
  <text x="502" y="240" text-anchor="middle" class="s8">Un hilo por bit · distancia muy corta</text>
  <text x="502" y="255" text-anchor="middle" class="s8">Frena por: desviación temporal, diafonía y coste</text>
  <text x="502" y="273" text-anchor="middle" class="s8">Residual: buses internos muy cortos</text>
  <rect x="20" y="292" width="640" height="24" rx="4" fill="#fdf3e3"/>
  <text x="340" y="308" text-anchor="middle" class="d8">PCI a PCI Express · PATA a SATA · puerto paralelo a USB · SCSI a SAS: todo migró a SERIE</text>
  <text x="670" y="330" text-anchor="end" class="n8">[Fuente: STALLINGS; TANENBAUM]</text>
</svg>
```

---

## D9 · Equipos de interconexión clasificados por capa

**Sección**: §4.2.1 — Repetidores, concentradores, puentes, conmutadores y encaminadores
**Propósito**: Ordenar todos los equipos del enunciado por la capa en la que operan y por la dirección que usan para decidir.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 344" role="img" aria-label="Equipos de interconexión ordenados por capa: en capa uno repetidor concentrador y transceptor que trabajan con señales, en capa dos puente conmutador y punto de acceso que usan direcciones MAC, en capa tres encaminador y conmutador de capa tres que usan direcciones IP, y en capas superiores la pasarela que traduce entre arquitecturas distintas">
  <style>.t9{font:700 10.5px system-ui,sans-serif;fill:#fff}.s9{font:8.5px system-ui,sans-serif;fill:#fff}.d9{font:9px system-ui,sans-serif;fill:#333}.h9{font:700 13px system-ui,sans-serif;fill:#0055a0}.k9{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n9{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h9">Cuanto más alta es la capa, más sabe el equipo</text>
  <rect x="20" y="34" width="130" height="52" rx="5" fill="#7a2f8a"/><text x="85" y="54" text-anchor="middle" class="t9">CAPAS 4 a 7</text><text x="85" y="70" text-anchor="middle" class="s9">aplicación</text><text x="85" y="82" text-anchor="middle" class="s9">y superiores</text>
  <rect x="158" y="34" width="502" height="52" rx="5" fill="#f3ecf6"/>
  <text x="409" y="54" text-anchor="middle" class="d9">PASARELA (gateway): traduce entre arquitecturas o protocolos DISTINTOS</text>
  <text x="409" y="70" text-anchor="middle" class="d9">Pasarela de voz, de correo, de IoT, de pago · también cortafuegos de aplicación y proxy</text>
  <text x="409" y="82" text-anchor="middle" class="n9">Ojo: la puerta de enlace predeterminada NO es esto, es un encaminador</text>
  <rect x="20" y="94" width="130" height="52" rx="5" fill="#0055a0"/><text x="85" y="114" text-anchor="middle" class="t9">CAPA 3 — RED</text><text x="85" y="130" text-anchor="middle" class="s9">direcciones IP</text><text x="85" y="142" text-anchor="middle" class="s9">paquetes</text>
  <rect x="158" y="94" width="502" height="52" rx="5" fill="#eef3f8"/>
  <text x="409" y="114" text-anchor="middle" class="d9">ENCAMINADOR (router) y CONMUTADOR DE CAPA 3</text>
  <text x="409" y="130" text-anchor="middle" class="d9">Unen redes distintas · tabla de encaminamiento · NAT · fragmentación</text>
  <text x="409" y="142" text-anchor="middle" class="n9">DETIENE LA DIFUSIÓN y descarta bucles gracias al TTL</text>
  <rect x="20" y="154" width="130" height="52" rx="5" fill="#2d8659"/><text x="85" y="174" text-anchor="middle" class="t9">CAPA 2 — ENLACE</text><text x="85" y="190" text-anchor="middle" class="s9">direcciones MAC</text><text x="85" y="202" text-anchor="middle" class="s9">tramas</text>
  <rect x="158" y="154" width="502" height="52" rx="5" fill="#e8f4ee"/>
  <text x="409" y="174" text-anchor="middle" class="d9">PUENTE · CONMUTADOR (switch) · PUNTO DE ACCESO INALÁMBRICO</text>
  <text x="409" y="190" text-anchor="middle" class="d9">Aprender, reenviar, inundar y envejecer · tabla MAC · STP contra bucles</text>
  <text x="409" y="202" text-anchor="middle" class="n9">Segmenta el dominio de COLISIÓN, no el de DIFUSIÓN</text>
  <rect x="20" y="214" width="130" height="52" rx="5" fill="#e89822"/><text x="85" y="234" text-anchor="middle" class="t9">CAPA 1 — FÍSICA</text><text x="85" y="250" text-anchor="middle" class="s9">señales</text><text x="85" y="262" text-anchor="middle" class="s9">sin direcciones</text>
  <rect x="158" y="214" width="502" height="52" rx="5" fill="#fdf3e3"/>
  <text x="409" y="234" text-anchor="middle" class="d9">REPETIDOR · CONCENTRADOR (hub) · TRANSCEPTOR · CONVERTIDOR DE MEDIO</text>
  <text x="409" y="250" text-anchor="middle" class="d9">Regeneran la señal, no la amplifican: el ruido acumulado vuelve a cero</text>
  <text x="409" y="262" text-anchor="middle" class="n9">El concentrador repite por TODOS los puertos: un solo dominio de colisión</text>
  <rect x="20" y="278" width="640" height="34" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="293" text-anchor="middle" class="k9">EL ROUTER DEL OPERADOR SON TRES EQUIPOS EN UNA CAJA</text>
  <text x="340" y="307" text-anchor="middle" class="n9">módem u ONT que termina la línea + encaminador + conmutador con punto de acceso</text>
  <text x="670" y="338" text-anchor="end" class="n9">[Fuente: TANENBAUM; IEEE 802.1]</text>
</svg>
```

---

## D10 · Dominios de colisión y dominios de difusión

**Sección**: §4.2.1 — Repetidores, concentradores, puentes, conmutadores y encaminadores
**Propósito**: Resolver de un vistazo la distinción central del temario de redes: qué equipo segmenta qué dominio.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 330" role="img" aria-label="Comparación de concentrador, conmutador y encaminador según los dominios de colisión y de difusión que crean: el concentrador deja un único dominio de colisión y uno de difusión, el conmutador crea un dominio de colisión por puerto pero mantiene uno solo de difusión, y el encaminador crea un dominio de difusión por interfaz">
  <style>.t10{font:700 10.5px system-ui,sans-serif;fill:#fff}.s10{font:8.5px system-ui,sans-serif;fill:#fff}.d10{font:9px system-ui,sans-serif;fill:#333}.h10{font:700 13px system-ui,sans-serif;fill:#0055a0}.k10{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n10{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h10">Quién segmenta qué</text>
  <text x="26" y="42" class="k10">EQUIPO</text><text x="250" y="42" class="k10">DOMINIOS DE COLISIÓN</text><text x="470" y="42" class="k10">DOMINIOS DE DIFUSIÓN</text>
  <rect x="20" y="50" width="200" height="46" rx="5" fill="#e89822"/><text x="120" y="70" text-anchor="middle" class="t10">CONCENTRADOR (hub)</text><text x="120" y="86" text-anchor="middle" class="s10">capa 1 · semidúplex</text>
  <rect x="228" y="50" width="200" height="46" rx="5" fill="#fbeaea"/><text x="328" y="70" text-anchor="middle" class="d10">UNO SOLO</text><text x="328" y="86" text-anchor="middle" class="n10">todos compiten por el medio</text>
  <rect x="436" y="50" width="224" height="46" rx="5" fill="#fbeaea"/><text x="548" y="70" text-anchor="middle" class="d10">UNO SOLO</text><text x="548" y="86" text-anchor="middle" class="n10">la difusión llega a todos</text>
  <rect x="20" y="104" width="200" height="46" rx="5" fill="#2d8659"/><text x="120" y="124" text-anchor="middle" class="t10">CONMUTADOR (switch)</text><text x="120" y="140" text-anchor="middle" class="s10">capa 2 · dúplex</text>
  <rect x="228" y="104" width="200" height="46" rx="5" fill="#e8f4ee"/><text x="328" y="124" text-anchor="middle" class="d10">UNO POR PUERTO</text><text x="328" y="140" text-anchor="middle" class="n10">enlace dedicado a cada equipo</text>
  <rect x="436" y="104" width="224" height="46" rx="5" fill="#fbeaea"/><text x="548" y="124" text-anchor="middle" class="d10">UNO SOLO — salvo VLAN</text><text x="548" y="140" text-anchor="middle" class="n10">cada VLAN es un dominio distinto</text>
  <rect x="20" y="158" width="200" height="46" rx="5" fill="#0055a0"/><text x="120" y="178" text-anchor="middle" class="t10">ENCAMINADOR (router)</text><text x="120" y="194" text-anchor="middle" class="s10">capa 3 · dúplex</text>
  <rect x="228" y="158" width="200" height="46" rx="5" fill="#e8f4ee"/><text x="328" y="178" text-anchor="middle" class="d10">UNO POR INTERFAZ</text><text x="328" y="194" text-anchor="middle" class="n10">—</text>
  <rect x="436" y="158" width="224" height="46" rx="5" fill="#e8f4ee"/><text x="548" y="178" text-anchor="middle" class="d10">UNO POR INTERFAZ</text><text x="548" y="194" text-anchor="middle" class="n10">detiene la difusión</text>
  <rect x="20" y="216" width="640" height="26" rx="4" fill="#fdf3e3"/>
  <text x="340" y="233" text-anchor="middle" class="d10">EL CONMUTADOR NO DIVIDE EL DOMINIO DE DIFUSIÓN: solo lo hacen el encaminador y las VLAN</text>
  <rect x="20" y="252" width="640" height="56" rx="5" fill="none" stroke="#d13c3c" stroke-width="1.5"/>
  <text x="340" y="270" text-anchor="middle" class="k10">POR QUÉ IMPORTA: la tormenta de difusión</text>
  <text x="340" y="286" text-anchor="middle" class="n10">La trama Ethernet NO tiene TTL, así que un bucle de nivel 2 la multiplica sin fin. Remedios: STP/RSTP,</text>
  <text x="340" y="299" text-anchor="middle" class="n10">VLAN para acotar el dominio y control de tormentas por puerto</text>
  <text x="670" y="324" text-anchor="end" class="n10">[Fuente: IEEE 802.1; TANENBAUM]</text>
</svg>
```

---

## D11 · Redes por cobertura geográfica: PAN, LAN, MAN y WAN

**Sección**: §5.1 — Clasificación por cobertura geográfica
**Propósito**: Fijar la escala completa y, sobre todo, los tres criterios que de verdad separan una LAN de una WAN más allá de los kilómetros.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 326" role="img" aria-label="Escala de redes por cobertura geográfica desde la red de área personal de metros hasta la red de área extensa de alcance continental, pasando por la red local, la de campus y la metropolitana, con los tres criterios que separan una red local de una red extensa: titularidad del medio, velocidad y latencia, y tasa de error">
  <style>.t11{font:700 10.5px system-ui,sans-serif;fill:#fff}.s11{font:8.5px system-ui,sans-serif;fill:#fff}.d11{font:9px system-ui,sans-serif;fill:#333}.h11{font:700 13px system-ui,sans-serif;fill:#0055a0}.k11{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n11{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a11" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h11">De los metros a los continentes</text>
  <rect x="20" y="38" width="124" height="58" rx="5" fill="#7a2f8a"/><text x="82" y="58" text-anchor="middle" class="t11">PAN</text><text x="82" y="73" text-anchor="middle" class="s11">metros</text><text x="82" y="87" text-anchor="middle" class="s11">Bluetooth, NFC</text>
  <rect x="152" y="38" width="124" height="58" rx="5" fill="#0055a0"/><text x="214" y="58" text-anchor="middle" class="t11">LAN</text><text x="214" y="73" text-anchor="middle" class="s11">edificio</text><text x="214" y="87" text-anchor="middle" class="s11">Ethernet, Wi-Fi</text>
  <rect x="284" y="38" width="124" height="58" rx="5" fill="#2d8659"/><text x="346" y="58" text-anchor="middle" class="t11">CAN</text><text x="346" y="73" text-anchor="middle" class="s11">campus</text><text x="346" y="87" text-anchor="middle" class="s11">varios edificios</text>
  <rect x="416" y="38" width="124" height="58" rx="5" fill="#e89822"/><text x="478" y="58" text-anchor="middle" class="t11">MAN</text><text x="478" y="73" text-anchor="middle" class="s11">ciudad</text><text x="478" y="87" text-anchor="middle" class="s11">anillo de fibra</text>
  <rect x="548" y="38" width="112" height="58" rx="5" fill="#d13c3c"/><text x="604" y="58" text-anchor="middle" class="t11">WAN</text><text x="604" y="73" text-anchor="middle" class="s11">país o mundo</text><text x="604" y="87" text-anchor="middle" class="s11">internet, SARA</text>
  <path d="M40 110 L640 110" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <text x="40" y="126" class="n11">metros</text><text x="640" y="126" text-anchor="end" class="n11">miles de kilómetros</text>
  <text x="26" y="150" class="k11">LOS TRES CRITERIOS QUE DE VERDAD SEPARAN LAN DE WAN</text>
  <rect x="20" y="158" width="206" height="52" rx="5" fill="#eef3f8"/>
  <text x="123" y="176" text-anchor="middle" class="k11">1 · TITULARIDAD</text>
  <text x="123" y="192" text-anchor="middle" class="n11">LAN: el cable es propio</text><text x="123" y="204" text-anchor="middle" class="n11">WAN: se contrata al operador</text>
  <rect x="237" y="158" width="206" height="52" rx="5" fill="#eef3f8"/>
  <text x="340" y="176" text-anchor="middle" class="k11">2 · VELOCIDAD Y LATENCIA</text>
  <text x="340" y="192" text-anchor="middle" class="n11">LAN: gigabits, microsegundos</text><text x="340" y="204" text-anchor="middle" class="n11">WAN: menos por euro, milisegundos</text>
  <rect x="454" y="158" width="206" height="52" rx="5" fill="#eef3f8"/>
  <text x="557" y="176" text-anchor="middle" class="k11">3 · TASA DE ERROR</text>
  <text x="557" y="192" text-anchor="middle" class="n11">LAN: medio controlado</text><text x="557" y="204" text-anchor="middle" class="n11">WAN: medios heterogéneos</text>
  <text x="26" y="234" class="k11">CATEGORÍAS POR OTROS CRITERIOS, QUE NO SON DE ESCALA</text>
  <rect x="20" y="242" width="155" height="34" rx="4" fill="#f5f5f5"/><text x="97" y="257" text-anchor="middle" class="d11">SAN</text><text x="97" y="270" text-anchor="middle" class="n11">por función: almacenamiento</text>
  <rect x="182" y="242" width="155" height="34" rx="4" fill="#f5f5f5"/><text x="259" y="257" text-anchor="middle" class="d11">VPN</text><text x="259" y="270" text-anchor="middle" class="n11">por arquitectura: túnel cifrado</text>
  <rect x="344" y="242" width="155" height="34" rx="4" fill="#f5f5f5"/><text x="421" y="257" text-anchor="middle" class="d11">BAN</text><text x="421" y="270" text-anchor="middle" class="n11">sensores sobre el cuerpo</text>
  <rect x="506" y="242" width="154" height="34" rx="4" fill="#f5f5f5"/><text x="583" y="257" text-anchor="middle" class="d11">W + PAN/LAN/MAN/WAN</text><text x="583" y="270" text-anchor="middle" class="n11">versión inalámbrica de cada una</text>
  <text x="340" y="298" text-anchor="middle" class="n11">Red de ALTA capacidad = al menos 30 Mbps · red de MUY ALTA capacidad = fibra hasta el punto de distribución</text>
  <text x="670" y="320" text-anchor="end" class="n11">[Fuente: LGT, anexo II.61-63; TANENBAUM]</text>
</svg>
```

---

## D12 · Topologías físicas de red y su tolerancia a fallos

**Sección**: §5.2 — Topologías de red físicas y lógicas
**Propósito**: Dibujar las cinco topologías básicas con su punto único de fallo, y separar el plano físico del lógico, que es la distinción clave.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="Las cinco topologías físicas de red: bus, anillo, estrella, árbol y malla, dibujadas con sus nodos y enlaces, indicando en cada una el punto único de fallo, y la distinción entre topología física y topología lógica con el ejemplo de Ethernet conmutado y de Token Ring">
  <style>.t12{font:700 10px system-ui,sans-serif;fill:#fff}.d12{font:9px system-ui,sans-serif;fill:#333}.h12{font:700 13px system-ui,sans-serif;fill:#0055a0}.k12{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n12{font:8.5px system-ui,sans-serif;fill:#666}.ln12{stroke:#0055a0;stroke-width:1.6;fill:none}</style>
  <text x="340" y="20" text-anchor="middle" class="h12">Cinco formas de unir los mismos nodos</text>
  <rect x="20" y="34" width="124" height="20" rx="3" fill="#0055a0"/><text x="82" y="48" text-anchor="middle" class="t12">BUS</text>
  <rect x="152" y="34" width="124" height="20" rx="3" fill="#0055a0"/><text x="214" y="48" text-anchor="middle" class="t12">ANILLO</text>
  <rect x="284" y="34" width="124" height="20" rx="3" fill="#0055a0"/><text x="346" y="48" text-anchor="middle" class="t12">ESTRELLA</text>
  <rect x="416" y="34" width="124" height="20" rx="3" fill="#0055a0"/><text x="478" y="48" text-anchor="middle" class="t12">ÁRBOL</text>
  <rect x="548" y="34" width="112" height="20" rx="3" fill="#0055a0"/><text x="604" y="48" text-anchor="middle" class="t12">MALLA</text>
  <path class="ln12" d="M30 96 L134 96"/>
  <circle cx="48" cy="96" r="5" fill="#0055a0"/><circle cx="82" cy="96" r="5" fill="#0055a0"/><circle cx="116" cy="96" r="5" fill="#0055a0"/>
  <path class="ln12" d="M48 96 L48 78 M82 96 L82 78 M116 96 L116 78"/>
  <circle cx="48" cy="74" r="4" fill="#888"/><circle cx="82" cy="74" r="4" fill="#888"/><circle cx="116" cy="74" r="4" fill="#888"/>
  <path class="ln12" d="M182 74 L246 74 L246 112 L182 112 Z"/>
  <circle cx="182" cy="74" r="5" fill="#0055a0"/><circle cx="246" cy="74" r="5" fill="#0055a0"/><circle cx="246" cy="112" r="5" fill="#0055a0"/><circle cx="182" cy="112" r="5" fill="#0055a0"/>
  <circle cx="346" cy="93" r="8" fill="#e89822"/>
  <path class="ln12" d="M346 93 L306 72 M346 93 L386 72 M346 93 L306 114 M346 93 L386 114"/>
  <circle cx="306" cy="72" r="5" fill="#0055a0"/><circle cx="386" cy="72" r="5" fill="#0055a0"/><circle cx="306" cy="114" r="5" fill="#0055a0"/><circle cx="386" cy="114" r="5" fill="#0055a0"/>
  <circle cx="478" cy="70" r="7" fill="#e89822"/>
  <path class="ln12" d="M478 70 L446 94 M478 70 L510 94 M446 94 L432 114 M446 94 L460 114 M510 94 L496 114 M510 94 L524 114"/>
  <circle cx="446" cy="94" r="5" fill="#0055a0"/><circle cx="510" cy="94" r="5" fill="#0055a0"/>
  <circle cx="432" cy="114" r="4" fill="#888"/><circle cx="460" cy="114" r="4" fill="#888"/><circle cx="496" cy="114" r="4" fill="#888"/><circle cx="524" cy="114" r="4" fill="#888"/>
  <path class="ln12" d="M574 74 L634 74 L634 112 L574 112 Z M574 74 L634 112 M634 74 L574 112"/>
  <circle cx="574" cy="74" r="5" fill="#2d8659"/><circle cx="634" cy="74" r="5" fill="#2d8659"/><circle cx="634" cy="112" r="5" fill="#2d8659"/><circle cx="574" cy="112" r="5" fill="#2d8659"/>
  <text x="26" y="146" class="k12">PUNTO ÚNICO DE FALLO</text>
  <rect x="20" y="154" width="124" height="40" rx="4" fill="#fbeaea"/><text x="82" y="170" text-anchor="middle" class="d12">El troncal</text><text x="82" y="185" text-anchor="middle" class="n12">un corte tumba todo</text>
  <rect x="152" y="154" width="124" height="40" rx="4" fill="#fbeaea"/><text x="214" y="170" text-anchor="middle" class="d12">Cualquier nodo</text><text x="214" y="185" text-anchor="middle" class="n12">salvo doble anillo</text>
  <rect x="284" y="154" width="124" height="40" rx="4" fill="#fdf3e3"/><text x="346" y="170" text-anchor="middle" class="d12">El nodo central</text><text x="346" y="185" text-anchor="middle" class="n12">el resto queda aislado</text>
  <rect x="416" y="154" width="124" height="40" rx="4" fill="#fdf3e3"/><text x="478" y="170" text-anchor="middle" class="d12">Los nodos altos</text><text x="478" y="185" text-anchor="middle" class="n12">aíslan su rama</text>
  <rect x="548" y="154" width="112" height="40" rx="4" fill="#e8f4ee"/><text x="604" y="170" text-anchor="middle" class="d12">NINGUNO</text><text x="604" y="185" text-anchor="middle" class="n12">caminos alternativos</text>
  <rect x="20" y="206" width="640" height="26" rx="4" fill="#eef3f8"/>
  <text x="340" y="223" text-anchor="middle" class="d12">Malla COMPLETA: n(n−1)/2 enlaces · crece al cuadrado y no escala · en la práctica, malla PARCIAL o doble anillo</text>
  <text x="26" y="256" class="k12">TOPOLOGÍA FÍSICA FRENTE A TOPOLOGÍA LÓGICA</text>
  <rect x="20" y="264" width="316" height="46" rx="5" fill="#0055a0"/>
  <text x="178" y="282" text-anchor="middle" class="t12">Ethernet conmutado</text>
  <text x="178" y="299" text-anchor="middle" class="n12" style="fill:#dfe9f3">estrella física · bus conmutado lógico</text>
  <rect x="344" y="264" width="316" height="46" rx="5" fill="#7a2f8a"/>
  <text x="502" y="282" text-anchor="middle" class="t12">Token Ring</text>
  <text x="502" y="299" text-anchor="middle" class="n12" style="fill:#efe4f3">estrella física (MAU) · anillo lógico</text>
  <text x="340" y="330" text-anchor="middle" class="n12">La topología física dice por dónde va el cable; la lógica, por dónde va la señal</text>
  <text x="670" y="346" text-anchor="end" class="n12">[Fuente: FOROUZAN; TANENBAUM]</text>
</svg>
```

---

## D13 · Conmutación de circuitos, de mensajes y de paquetes

**Sección**: §6.1.1 — Conmutación de circuitos, de mensajes y de paquetes
**Propósito**: Comparar las tres técnicas en ocho rasgos clave y visualizar el encauzamiento, que es la razón numérica de que la conmutación de paquetes gane.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Comparación de las tres técnicas de conmutación: de circuitos con camino reservado y tres fases, de mensajes con almacenamiento y reenvío del mensaje completo, y de paquetes con multiplexación estadística y encauzamiento, más la distinción entre datagrama y circuito virtual">
  <style>.t13{font:700 10.5px system-ui,sans-serif;fill:#fff}.s13{font:8.5px system-ui,sans-serif;fill:#fff}.d13{font:9px system-ui,sans-serif;fill:#333}.h13{font:700 13px system-ui,sans-serif;fill:#0055a0}.k13{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n13{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h13">Qué se conmuta y cuándo se decide la ruta</text>
  <rect x="20" y="34" width="206" height="28" rx="5" fill="#0055a0"/><text x="123" y="53" text-anchor="middle" class="t13">CIRCUITOS</text>
  <rect x="237" y="34" width="206" height="28" rx="5" fill="#8a8a8a"/><text x="340" y="53" text-anchor="middle" class="t13">MENSAJES</text>
  <rect x="454" y="34" width="206" height="28" rx="5" fill="#2d8659"/><text x="557" y="53" text-anchor="middle" class="t13">PAQUETES</text>
  <rect x="20" y="68" width="206" height="108" rx="4" fill="#eef3f8"/>
  <text x="123" y="86" text-anchor="middle" class="d13">Camino físico RESERVADO</text>
  <text x="123" y="102" text-anchor="middle" class="n13">Tres fases: establecimiento,</text><text x="123" y="114" text-anchor="middle" class="n13">transferencia y liberación</text>
  <text x="123" y="132" text-anchor="middle" class="n13">Retardo CONSTANTE, sin fluctuación</text>
  <text x="123" y="148" text-anchor="middle" class="n13">Desaprovecha en los silencios</text>
  <text x="123" y="166" text-anchor="middle" class="n13">Si no hay recursos: BLOQUEO</text>
  <rect x="237" y="68" width="206" height="108" rx="4" fill="#f2f2f2"/>
  <text x="340" y="86" text-anchor="middle" class="d13">Mensaje COMPLETO, sin partir</text>
  <text x="340" y="102" text-anchor="middle" class="n13">Almacenamiento y reenvío</text><text x="340" y="114" text-anchor="middle" class="n13">íntegro en cada nodo</text>
  <text x="340" y="132" text-anchor="middle" class="n13">Retardos altos y variables</text>
  <text x="340" y="148" text-anchor="middle" class="n13">Exige mucha memoria en los nodos</text>
  <text x="340" y="166" text-anchor="middle" class="n13">EN DESUSO como técnica de red</text>
  <rect x="454" y="68" width="206" height="108" rx="4" fill="#e8f4ee"/>
  <text x="557" y="86" text-anchor="middle" class="d13">PAQUETES independientes</text>
  <text x="557" y="102" text-anchor="middle" class="n13">Multiplexación estadística</text><text x="557" y="114" text-anchor="middle" class="n13">y encauzamiento</text>
  <text x="557" y="132" text-anchor="middle" class="n13">Aprovechamiento máximo del enlace</text>
  <text x="557" y="148" text-anchor="middle" class="n13">Con fluctuación y posible pérdida</text>
  <text x="557" y="166" text-anchor="middle" class="n13">Si se satura: DEGRADACIÓN</text>
  <text x="26" y="200" class="k13">DENTRO DE LA CONMUTACIÓN DE PAQUETES</text>
  <rect x="20" y="208" width="316" height="60" rx="5" fill="#0055a0"/>
  <text x="178" y="226" text-anchor="middle" class="t13">DATAGRAMA — sin conexión</text>
  <text x="178" y="242" text-anchor="middle" class="s13">Cada paquete elige ruta en cada nodo</text>
  <text x="178" y="256" text-anchor="middle" class="s13">Pueden desordenarse · se reencaminan solos · IP</text>
  <rect x="344" y="208" width="316" height="60" rx="5" fill="#7a2f8a"/>
  <text x="502" y="226" text-anchor="middle" class="t13">CIRCUITO VIRTUAL — con conexión</text>
  <text x="502" y="242" text-anchor="middle" class="s13">Ruta fijada al inicio, identificador corto</text>
  <text x="502" y="256" text-anchor="middle" class="s13">Orden garantizado · X.25, Frame Relay, ATM, MPLS</text>
  <rect x="20" y="278" width="640" height="24" rx="4" fill="#fbeaea"/>
  <text x="340" y="294" text-anchor="middle" class="d13">EL CIRCUITO VIRTUAL NO ES UN CIRCUITO: no reserva recursos, solo preacuerda la ruta</text>
  <rect x="20" y="312" width="640" height="26" rx="5" fill="none" stroke="#2d8659" stroke-width="1.5"/>
  <text x="340" y="329" text-anchor="middle" class="k13">ENCAUZAMIENTO: T = (n.º de enlaces + n.º de paquetes − 1) × tiempo de un paquete</text>
  <text x="670" y="354" text-anchor="end" class="n13">[Fuente: TANENBAUM; STALLINGS]</text>
</svg>
```

---

## D14 · Modos de entrega y direcciones de difusión y multidifusión

**Sección**: §6.2.1 — Principios de difusión, direcciones broadcast y multicast
**Propósito**: Reunir los cuatro modos de entrega con las direcciones exactas de cada uno, que son datos de memorización literal, y marcar la supresión de la difusión en IPv6.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 344" role="img" aria-label="Los cuatro modos de entrega: unidifusión a uno, multidifusión a un grupo suscrito, difusión a todos y anydifusión al más cercano, con las direcciones de difusión y multidifusión en Ethernet, IPv4 e IPv6, y la advertencia de que IPv6 no tiene difusión">
  <style>.t14{font:700 10.5px system-ui,sans-serif;fill:#fff}.s14{font:8.5px system-ui,sans-serif;fill:#fff}.d14{font:9px system-ui,sans-serif;fill:#333}.h14{font:700 13px system-ui,sans-serif;fill:#0055a0}.k14{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n14{font:8.5px system-ui,sans-serif;fill:#666}.m14{font:700 9.5px ui-monospace,monospace;fill:#0055a0}</style>
  <text x="340" y="20" text-anchor="middle" class="h14">A uno, a un grupo, a todos o al más cercano</text>
  <rect x="20" y="36" width="155" height="56" rx="5" fill="#0055a0"/><text x="97" y="56" text-anchor="middle" class="t14">UNIDIFUSIÓN</text><text x="97" y="72" text-anchor="middle" class="s14">uno a UNO</text><text x="97" y="85" text-anchor="middle" class="s14">la mayoría del tráfico</text>
  <rect x="182" y="36" width="155" height="56" rx="5" fill="#2d8659"/><text x="259" y="56" text-anchor="middle" class="t14">MULTIDIFUSIÓN</text><text x="259" y="72" text-anchor="middle" class="s14">uno a un GRUPO</text><text x="259" y="85" text-anchor="middle" class="s14">hay que suscribirse</text>
  <rect x="344" y="36" width="155" height="56" rx="5" fill="#e89822"/><text x="421" y="56" text-anchor="middle" class="t14">DIFUSIÓN</text><text x="421" y="72" text-anchor="middle" class="s14">uno a TODOS</text><text x="421" y="85" text-anchor="middle" class="s14">sin suscripción</text>
  <rect x="506" y="36" width="154" height="56" rx="5" fill="#7a2f8a"/><text x="583" y="56" text-anchor="middle" class="t14">ANYDIFUSIÓN</text><text x="583" y="72" text-anchor="middle" class="s14">al MÁS CERCANO</text><text x="583" y="85" text-anchor="middle" class="s14">propia de IPv6</text>
  <text x="26" y="116" class="k14">DIRECCIONES QUE HAY QUE SABER DE MEMORIA</text>
  <rect x="20" y="124" width="130" height="26" rx="3" fill="#0055a0"/><text x="85" y="141" text-anchor="middle" class="t14">Ethernet</text>
  <rect x="158" y="124" width="502" height="26" rx="3" fill="#eef3f8"/><text x="409" y="141" text-anchor="middle" class="m14">Difusión FF:FF:FF:FF:FF:FF · multidifusión IPv4 sobre MAC 01:00:5E:...</text>
  <rect x="20" y="154" width="130" height="26" rx="3" fill="#0055a0"/><text x="85" y="171" text-anchor="middle" class="t14">IPv4</text>
  <rect x="158" y="154" width="502" height="26" rx="3" fill="#eef3f8"/><text x="409" y="171" text-anchor="middle" class="m14">Difusión limitada 255.255.255.255 (no se encamina) · multidifusión 224.0.0.0/4</text>
  <rect x="20" y="184" width="130" height="26" rx="3" fill="#d13c3c"/><text x="85" y="201" text-anchor="middle" class="t14">IPv6</text>
  <rect x="158" y="184" width="502" height="26" rx="3" fill="#fbeaea"/><text x="409" y="201" text-anchor="middle" class="m14">SIN DIFUSIÓN · todos los nodos del enlace = ff02::1 · prefijo ff00::/8</text>
  <rect x="20" y="222" width="316" height="60" rx="5" fill="#e8f4ee"/>
  <text x="178" y="240" text-anchor="middle" class="k14">PARA QUÉ SIRVE LA DIFUSIÓN</text>
  <text x="178" y="256" text-anchor="middle" class="n14">ARP y DHCP: hablar con quien aún no se conoce</text>
  <text x="178" y="270" text-anchor="middle" class="n14">Descubrimiento de servicios y de vecinos</text>
  <rect x="344" y="222" width="316" height="60" rx="5" fill="#fbeaea"/>
  <text x="502" y="240" text-anchor="middle" class="k14">TORMENTA DE DIFUSIÓN</text>
  <text x="502" y="256" text-anchor="middle" class="n14">Bucle de nivel 2 + trama Ethernet sin TTL</text>
  <text x="502" y="270" text-anchor="middle" class="n14">Remedios: STP/RSTP, VLAN, control de tormentas</text>
  <rect x="20" y="292" width="640" height="26" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="309" text-anchor="middle" class="k14">Suscripción a grupos: IGMP en IPv4 · MLD en IPv6 · en el conmutador, vigilancia de IGMP</text>
  <text x="670" y="338" text-anchor="end" class="n14">[Fuente: RFC 1112; RFC 4291; RFC 826]</text>
</svg>
```

---

## D15 · Redes inalámbricas: escala, arquitectura Wi-Fi y generaciones

**Sección**: §7 — Redes e infraestructuras inalámbricas
**Propósito**: Situar cada tecnología inalámbrica en su escala de cobertura y fijar la tabla de generaciones de Wi-Fi con las dos fechas clave: 2025 para Wi-Fi 7 y 2028 para Wi-Fi 8.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 356" role="img" aria-label="Redes inalámbricas ordenadas por cobertura, de la red de área personal con Bluetooth NFC y Zigbee a la red de área extensa con redes celulares satélite y LPWAN, con la arquitectura Wi-Fi de celda BSS y conjunto extendido ESS, y la tabla de generaciones de Wi-Fi 4 a Wi-Fi 8 con sus años">
  <style>.t15{font:700 10px system-ui,sans-serif;fill:#fff}.s15{font:8.5px system-ui,sans-serif;fill:#fff}.d15{font:9px system-ui,sans-serif;fill:#333}.h15{font:700 13px system-ui,sans-serif;fill:#0055a0}.k15{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n15{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h15">La misma escala, ahora sin cable</text>
  <rect x="20" y="34" width="120" height="24" rx="3" fill="#7a2f8a"/><text x="80" y="50" text-anchor="middle" class="t15">WPAN</text>
  <rect x="148" y="34" width="512" height="24" rx="3" fill="#f3ecf6"/><text x="404" y="50" text-anchor="middle" class="d15">Metros · Bluetooth · NFC 13,56 MHz y 10 cm · Zigbee · Thread · UWB</text>
  <rect x="20" y="62" width="120" height="24" rx="3" fill="#0055a0"/><text x="80" y="78" text-anchor="middle" class="t15">WLAN</text>
  <rect x="148" y="62" width="512" height="24" rx="3" fill="#eef3f8"/><text x="404" y="78" text-anchor="middle" class="d15">Decenas o cientos de metros · Wi-Fi (IEEE 802.11) en 2,4, 5 y 6 GHz</text>
  <rect x="20" y="90" width="120" height="24" rx="3" fill="#e89822"/><text x="80" y="106" text-anchor="middle" class="t15">WMAN</text>
  <rect x="148" y="90" width="512" height="24" rx="3" fill="#fdf3e3"/><text x="404" y="106" text-anchor="middle" class="d15">Kilómetros · WiMAX (IEEE 802.16), hoy residual · radioenlaces de microondas</text>
  <rect x="20" y="118" width="120" height="24" rx="3" fill="#d13c3c"/><text x="80" y="134" text-anchor="middle" class="t15">WWAN</text>
  <rect x="148" y="118" width="512" height="24" rx="3" fill="#fbeaea"/><text x="404" y="134" text-anchor="middle" class="d15">Regional o global · celular 2G-5G · satélite GEO/MEO/LEO · LPWAN</text>
  <text x="26" y="164" class="k15">ARQUITECTURA WI-FI</text>
  <rect x="20" y="172" width="206" height="44" rx="5" fill="#eef3f8"/><text x="123" y="189" text-anchor="middle" class="d15">BSS = una celda</text><text x="123" y="205" text-anchor="middle" class="n15">un punto de acceso + sus clientes (BSSID)</text>
  <rect x="237" y="172" width="206" height="44" rx="5" fill="#eef3f8"/><text x="340" y="189" text-anchor="middle" class="d15">ESS = varias celdas</text><text x="340" y="205" text-anchor="middle" class="n15">mismo SSID · itinerancia entre ellas</text>
  <rect x="454" y="172" width="206" height="44" rx="5" fill="#fdf3e3"/><text x="557" y="189" text-anchor="middle" class="d15">Acceso al medio: CSMA/CA</text><text x="557" y="205" text-anchor="middle" class="n15">con ACK y, si hace falta, RTS/CTS</text>
  <text x="26" y="238" class="k15">GENERACIONES</text>
  <rect x="20" y="246" width="124" height="44" rx="4" fill="#8fa9c4"/><text x="82" y="263" text-anchor="middle" class="t15">Wi-Fi 4 — 802.11n</text><text x="82" y="278" text-anchor="middle" class="s15">2009 · MIMO</text>
  <rect x="152" y="246" width="124" height="44" rx="4" fill="#5384ac"/><text x="214" y="263" text-anchor="middle" class="t15">Wi-Fi 5 — 802.11ac</text><text x="214" y="278" text-anchor="middle" class="s15">2013 · 160 MHz</text>
  <rect x="284" y="246" width="124" height="44" rx="4" fill="#0055a0"/><text x="346" y="263" text-anchor="middle" class="t15">Wi-Fi 6 / 6E — ax</text><text x="346" y="278" text-anchor="middle" class="s15">2021 · OFDMA · 6 GHz</text>
  <rect x="416" y="246" width="124" height="44" rx="4" fill="#2d8659"/><text x="478" y="263" text-anchor="middle" class="t15">Wi-Fi 7 — 802.11be</text><text x="478" y="278" text-anchor="middle" class="s15">2025 · MLO · 4096-QAM</text>
  <rect x="548" y="246" width="112" height="44" rx="4" fill="#8a8a8a"/><text x="604" y="263" text-anchor="middle" class="t15">Wi-Fi 8 — 802.11bn</text><text x="604" y="278" text-anchor="middle" class="s15">previsto 2028</text>
  <rect x="20" y="300" width="640" height="24" rx="4" fill="#fdf3e3"/>
  <text x="340" y="316" text-anchor="middle" class="d15">En 2,4 GHz solo hay TRES canales sin solape: 1, 6 y 11 · celdas adyacentes nunca en el mismo canal</text>
  <text x="670" y="350" text-anchor="end" class="n15">[Fuente: IEEE 802.11; Wi-Fi Alliance]</text>
</svg>
```

---

## D16 · La red celular: principio celular y evolución de 1G a 5G

**Sección**: §8.1 — Evolución y arquitectura de redes celulares móviles · §8.2 — Tecnologías consolidadas y de alta capacidad
**Propósito**: Explicar la reutilización de frecuencias y encadenar las cinco generaciones con el salto conceptual de cada una y las tres familias de uso del 5G.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Principio celular con reutilización de frecuencias en celdas hexagonales no adyacentes, traspaso e itinerancia, evolución de las generaciones móviles de 1G analógica a 5G, y las tres familias de uso del 5G: banda ancha mejorada, comunicaciones ultrafiables de baja latencia y comunicaciones masivas entre máquinas">
  <style>.t16{font:700 10px system-ui,sans-serif;fill:#fff}.s16{font:8.5px system-ui,sans-serif;fill:#fff}.d16{font:9px system-ui,sans-serif;fill:#333}.h16{font:700 13px system-ui,sans-serif;fill:#0055a0}.k16{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n16{font:8.5px system-ui,sans-serif;fill:#666}.c16{font:700 11px system-ui,sans-serif;fill:#fff}</style>
  <text x="340" y="20" text-anchor="middle" class="h16">Celdas que reutilizan las mismas frecuencias</text>
  <polygon points="80,36 108,52 108,84 80,100 52,84 52,52" fill="#0055a0"/><text x="80" y="72" text-anchor="middle" class="c16">A</text>
  <polygon points="136,36 164,52 164,84 136,100 108,84 108,52" fill="#2d8659"/><text x="136" y="72" text-anchor="middle" class="c16">B</text>
  <polygon points="192,36 220,52 220,84 192,100 164,84 164,52" fill="#e89822"/><text x="192" y="72" text-anchor="middle" class="c16">C</text>
  <polygon points="248,36 276,52 276,84 248,100 220,84 220,52" fill="#0055a0"/><text x="248" y="72" text-anchor="middle" class="c16">A</text>
  <polygon points="304,36 332,52 332,84 304,100 276,84 276,52" fill="#2d8659"/><text x="304" y="72" text-anchor="middle" class="c16">B</text>
  <rect x="348" y="36" width="312" height="30" rx="4" fill="#eef3f8"/><text x="504" y="55" text-anchor="middle" class="d16">Celdas NO adyacentes repiten el mismo grupo de canales</text>
  <rect x="348" y="70" width="152" height="30" rx="4" fill="#f5f5f5"/><text x="424" y="83" text-anchor="middle" class="d16">TRASPASO</text><text x="424" y="95" text-anchor="middle" class="n16">dentro del operador, en curso</text>
  <rect x="508" y="70" width="152" height="30" rx="4" fill="#f5f5f5"/><text x="584" y="83" text-anchor="middle" class="d16">ITINERANCIA</text><text x="584" y="95" text-anchor="middle" class="n16">entre operadores distintos</text>
  <rect x="20" y="110" width="640" height="24" rx="4" fill="#fdf3e3"/>
  <text x="340" y="126" text-anchor="middle" class="d16">Para aumentar la capacidad se REDUCE el tamaño de la celda: micro, pico y femtoceldas</text>
  <text x="26" y="156" class="k16">CINCO GENERACIONES, CUATRO SALTOS</text>
  <rect x="20" y="164" width="124" height="52" rx="4" fill="#8a8a8a"/><text x="82" y="182" text-anchor="middle" class="t16">1G — TACS</text><text x="82" y="197" text-anchor="middle" class="s16">analógica</text><text x="82" y="210" text-anchor="middle" class="s16">solo voz</text>
  <rect x="152" y="164" width="124" height="52" rx="4" fill="#5384ac"/><text x="214" y="182" text-anchor="middle" class="t16">2G — GSM</text><text x="214" y="197" text-anchor="middle" class="s16">digital · SMS · SIM</text><text x="214" y="210" text-anchor="middle" class="s16">GPRS añade paquetes</text>
  <rect x="284" y="164" width="124" height="52" rx="4" fill="#0055a0"/><text x="346" y="182" text-anchor="middle" class="t16">3G — UMTS</text><text x="346" y="197" text-anchor="middle" class="s16">WCDMA · IMT-2000</text><text x="346" y="210" text-anchor="middle" class="s16">HSPA</text>
  <rect x="416" y="164" width="124" height="52" rx="4" fill="#2d8659"/><text x="478" y="182" text-anchor="middle" class="t16">4G — LTE</text><text x="478" y="197" text-anchor="middle" class="s16">TODO IP, solo paquetes</text><text x="478" y="210" text-anchor="middle" class="s16">la voz es VoLTE</text>
  <rect x="548" y="164" width="112" height="52" rx="4" fill="#d13c3c"/><text x="604" y="182" text-anchor="middle" class="t16">5G — NR</text><text x="604" y="197" text-anchor="middle" class="s16">IMT-2020</text><text x="604" y="210" text-anchor="middle" class="s16">NSA y SA</text>
  <text x="26" y="240" class="k16">LAS TRES FAMILIAS DE USO DEL 5G</text>
  <rect x="20" y="248" width="206" height="52" rx="5" fill="#0055a0"/><text x="123" y="266" text-anchor="middle" class="t16">eMBB</text><text x="123" y="281" text-anchor="middle" class="s16">banda ancha mejorada</text><text x="123" y="294" text-anchor="middle" class="s16">20 Gbit/s de pico</text>
  <rect x="237" y="248" width="206" height="52" rx="5" fill="#d13c3c"/><text x="340" y="266" text-anchor="middle" class="t16">URLLC</text><text x="340" y="281" text-anchor="middle" class="s16">ultrafiable, baja latencia</text><text x="340" y="294" text-anchor="middle" class="s16">1 ms en la interfaz radio</text>
  <rect x="454" y="248" width="206" height="52" rx="5" fill="#2d8659"/><text x="557" y="266" text-anchor="middle" class="t16">mMTC</text><text x="557" y="281" text-anchor="middle" class="s16">máquinas masivas</text><text x="557" y="294" text-anchor="middle" class="s16">10⁶ dispositivos/km²</text>
  <rect x="20" y="310" width="640" height="26" rx="5" fill="none" stroke="#d13c3c" stroke-width="1.5"/>
  <text x="340" y="327" text-anchor="middle" class="k16">SIN NÚCLEO 5G AUTÓNOMO (SA) NO HAY NI FRACCIONAMIENTO DE RED NI URLLC REALES</text>
  <text x="670" y="354" text-anchor="end" class="n16">[Fuente: 3GPP; UIT-R IMT-2020]</text>
</svg>
```

---

## D17 · Seguridad inalámbrica: de WEP a WPA3 y medidas `mp.com` del ENS

**Sección**: §9.1 — Aspectos de seguridad e integridad en redes inalámbricas
**Propósito**: Encadenar la evolución de los protocolos con su estado actual, descartar expresamente las dos medidas cosméticas y anclar las cuatro medidas `mp.com` del ENS con su nivel de exigencia.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 356" role="img" aria-label="Evolución de los protocolos de seguridad inalámbrica desde WEP roto hasta WPA3 con autenticación SAE, medidas que no aportan seguridad real como ocultar el SSID o filtrar por dirección MAC, y las cuatro medidas de protección de las comunicaciones del Esquema Nacional de Seguridad con su nivel de exigencia">
  <style>.t17{font:700 10px system-ui,sans-serif;fill:#fff}.s17{font:8.5px system-ui,sans-serif;fill:#fff}.d17{font:9px system-ui,sans-serif;fill:#333}.h17{font:700 13px system-ui,sans-serif;fill:#0055a0}.k17{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n17{font:8.5px system-ui,sans-serif;fill:#666}.m17{font:700 9.5px ui-monospace,monospace;fill:#0055a0}</style>
  <text x="340" y="20" text-anchor="middle" class="h17">En radio hay que suponer siempre que alguien escucha</text>
  <rect x="20" y="36" width="155" height="54" rx="5" fill="#d13c3c"/><text x="97" y="54" text-anchor="middle" class="t17">WEP · 1999</text><text x="97" y="70" text-anchor="middle" class="s17">RC4 · ROTO</text><text x="97" y="83" text-anchor="middle" class="s17">prohibido su uso</text>
  <rect x="182" y="36" width="155" height="54" rx="5" fill="#e89822"/><text x="259" y="54" text-anchor="middle" class="t17">WPA · 2003</text><text x="259" y="70" text-anchor="middle" class="s17">TKIP · transitorio</text><text x="259" y="83" text-anchor="middle" class="s17">obsoleto</text>
  <rect x="344" y="36" width="155" height="54" rx="5" fill="#5384ac"/><text x="421" y="54" text-anchor="middle" class="t17">WPA2 · 2004</text><text x="421" y="70" text-anchor="middle" class="s17">AES-CCMP · 802.11i</text><text x="421" y="83" text-anchor="middle" class="s17">vigente pero atacable</text>
  <rect x="506" y="36" width="154" height="54" rx="5" fill="#2d8659"/><text x="583" y="54" text-anchor="middle" class="t17">WPA3 · 2018</text><text x="583" y="70" text-anchor="middle" class="s17">SAE · 192 bits</text><text x="583" y="83" text-anchor="middle" class="s17">EL RECOMENDADO</text>
  <rect x="20" y="98" width="640" height="26" rx="4" fill="#e8f4ee"/>
  <text x="340" y="115" text-anchor="middle" class="d17">WPA3 aporta SAE (sin diccionario fuera de línea), modo Enterprise de 192 bits y OWE para redes abiertas</text>
  <rect x="20" y="134" width="640" height="26" rx="4" fill="#fbeaea"/>
  <text x="340" y="151" text-anchor="middle" class="d17">NO SON SEGURIDAD: ocultar el SSID ni filtrar por dirección MAC · ambas se saltan en minutos</text>
  <rect x="20" y="170" width="640" height="26" rx="4" fill="#eef3f8"/>
  <text x="340" y="187" text-anchor="middle" class="d17">MODELO EMPRESARIAL: 802.1X + EAP + RADIUS · credencial por PERSONA, no clave compartida</text>
  <text x="26" y="218" class="k17">LO QUE EXIGE EL ENS (anexo II, protección de las comunicaciones)</text>
  <rect x="20" y="226" width="150" height="26" rx="3" fill="#0055a0"/><text x="95" y="243" text-anchor="middle" class="m17" style="fill:#fff">mp.com.1</text>
  <rect x="178" y="226" width="482" height="26" rx="3" fill="#eef3f8"/><text x="419" y="243" text-anchor="middle" class="d17">Perímetro seguro · todo el tráfico lo atraviesa · aplica en las TRES categorías</text>
  <rect x="20" y="256" width="150" height="26" rx="3" fill="#0055a0"/><text x="95" y="273" text-anchor="middle" class="m17" style="fill:#fff">mp.com.2 — dim. C</text>
  <rect x="178" y="256" width="482" height="26" rx="3" fill="#eef3f8"/><text x="419" y="273" text-anchor="middle" class="d17">VPN cifrada fuera del dominio propio · MEDIO: +R1 algoritmos autorizados por el CCN</text>
  <rect x="20" y="286" width="150" height="26" rx="3" fill="#0055a0"/><text x="95" y="303" text-anchor="middle" class="m17" style="fill:#fff">mp.com.3 — dim. IA</text>
  <rect x="178" y="286" width="482" height="26" rx="3" fill="#eef3f8"/><text x="419" y="303" text-anchor="middle" class="d17">Integridad y autenticidad del canal · MEDIO: +R1+R2 · ALTO: +R1+R2+R3+R4</text>
  <rect x="20" y="316" width="150" height="26" rx="3" fill="#e89822"/><text x="95" y="333" text-anchor="middle" class="m17" style="fill:#fff">mp.com.4</text>
  <rect x="178" y="316" width="482" height="26" rx="3" fill="#fdf3e3"/><text x="419" y="333" text-anchor="middle" class="d17">Si hay comunicaciones INALÁMBRICAS, en SEGMENTO SEPARADO · R1 VLAN, R2 VPN, R3 física</text>
  <text x="670" y="352" text-anchor="end" class="n17">[Fuente: ENS, anexo II; IEEE 802.11i; Wi-Fi Alliance]</text>
</svg>
```

---

## D18 · La Ley 11/2022: estructura, servicio universal y art. 13

**Sección**: §9.2 — Marco normativo y regulatorio de telecomunicaciones en el ámbito público
**Propósito**: Dar la estructura de la ley y aislar los tres preceptos que un técnico municipal debe conocer literalmente: el art. 2, el art. 37 y el art. 13.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="Estructura de la Ley 11 de 2022 General de Telecomunicaciones con sus ocho títulos, el principio de que las telecomunicaciones son servicios de interés general en libre competencia, el contenido del servicio universal con diez megabits por segundo, y el régimen del artículo 13 para las Administraciones públicas que instalan redes">
  <style>.t18{font:700 10px system-ui,sans-serif;fill:#fff}.s18{font:8.5px system-ui,sans-serif;fill:#fff}.d18{font:9px system-ui,sans-serif;fill:#333}.h18{font:700 13px system-ui,sans-serif;fill:#0055a0}.k18{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n18{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h18">Ley 11/2022 · 8 títulos · 114 artículos · 3 anexos</text>
  <rect x="20" y="34" width="78" height="34" rx="3" fill="#8fa9c4"/><text x="59" y="48" text-anchor="middle" class="t18">I</text><text x="59" y="62" text-anchor="middle" class="s18">generales</text>
  <rect x="106" y="34" width="78" height="34" rx="3" fill="#7196b8"/><text x="145" y="48" text-anchor="middle" class="t18">II</text><text x="145" y="62" text-anchor="middle" class="s18">redes y servicios</text>
  <rect x="192" y="34" width="78" height="34" rx="3" fill="#0055a0"/><text x="231" y="48" text-anchor="middle" class="t18">III</text><text x="231" y="62" text-anchor="middle" class="s18">servicio público</text>
  <rect x="278" y="34" width="78" height="34" rx="3" fill="#7196b8"/><text x="317" y="48" text-anchor="middle" class="t18">IV</text><text x="317" y="62" text-anchor="middle" class="s18">equipos</text>
  <rect x="364" y="34" width="78" height="34" rx="3" fill="#0055a0"/><text x="403" y="48" text-anchor="middle" class="t18">V</text><text x="403" y="62" text-anchor="middle" class="s18">espectro</text>
  <rect x="450" y="34" width="78" height="34" rx="3" fill="#7196b8"/><text x="489" y="48" text-anchor="middle" class="t18">VI</text><text x="489" y="62" text-anchor="middle" class="s18">administración</text>
  <rect x="536" y="34" width="60" height="34" rx="3" fill="#8fa9c4"/><text x="566" y="48" text-anchor="middle" class="t18">VII</text><text x="566" y="62" text-anchor="middle" class="s18">tasas</text>
  <rect x="604" y="34" width="56" height="34" rx="3" fill="#8fa9c4"/><text x="632" y="48" text-anchor="middle" class="t18">VIII</text><text x="632" y="62" text-anchor="middle" class="s18">sanciones</text>
  <rect x="20" y="80" width="640" height="40" rx="5" fill="#eef3f8"/>
  <text x="340" y="97" text-anchor="middle" class="k18">ART. 2 · LAS TELECOMUNICACIONES SON SERVICIOS DE INTERÉS GENERAL EN LIBRE COMPETENCIA</text>
  <text x="340" y="113" text-anchor="middle" class="n18">Solo son SERVICIO PÚBLICO los del art. 4: seguridad nacional, defensa, seguridad pública, seguridad vial y protección civil</text>
  <rect x="20" y="130" width="640" height="58" rx="5" fill="#e8f4ee"/>
  <text x="340" y="147" text-anchor="middle" class="k18">ART. 37 · SERVICIO UNIVERSAL — la principal obligación de servicio público</text>
  <text x="340" y="163" text-anchor="middle" class="n18">(a) Acceso a internet de banda ancha en UBICACIÓN FIJA: mínimo 10 Mbit/s descendentes, escalables por real decreto a 30</text>
  <text x="340" y="176" text-anchor="middle" class="n18">(b) Servicios de comunicaciones vocales · el anexo III enumera los ONCE servicios que debe soportar la conexión</text>
  <rect x="20" y="198" width="640" height="58" rx="5" fill="#fdf3e3"/>
  <text x="340" y="215" text-anchor="middle" class="k18">ART. 13 · CUANDO UNA ADMINISTRACIÓN INSTALA Y EXPLOTA REDES PÚBLICAS</text>
  <text x="340" y="231" text-anchor="middle" class="n18">Principio de INVERSOR PRIVADO · separación de cuentas · neutralidad, transparencia, no distorsión y no discriminación</text>
  <text x="340" y="244" text-anchor="middle" class="n18">Excepción: TDT en zonas sin cobertura, donde la ley declara que hay FALLO DE MERCADO</text>
  <rect x="20" y="266" width="640" height="30" rx="5" fill="#fbeaea"/>
  <text x="340" y="285" text-anchor="middle" class="d18">ART. 85 · El espectro es BIEN DE DOMINIO PÚBLICO, de titularidad y administración ESTATAL</text>
  <rect x="20" y="306" width="206" height="26" rx="4" fill="#f5f5f5"/><text x="123" y="323" text-anchor="middle" class="d18">UIT · mundial</text>
  <rect x="237" y="306" width="206" height="26" rx="4" fill="#f5f5f5"/><text x="340" y="323" text-anchor="middle" class="d18">Ministerio · espectro e incidentes</text>
  <rect x="454" y="306" width="206" height="26" rx="4" fill="#f5f5f5"/><text x="557" y="323" text-anchor="middle" class="d18">CNMC · mercados y conflictos</text>
  <text x="670" y="346" text-anchor="end" class="n18">[Fuente: Ley 11/2022, arts. 2, 4, 13, 37 y 85 y anexo III]</text>
</svg>
```
