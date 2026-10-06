# Tema 33 — Test de Autoevaluación

> **Título**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.
> **Formato**: 60 preguntas tipo test A/B/C (formato oficial oposición)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid
> **Versión**: v1.0 — Pendiente validación
> **Fecha**: 2026-08-27
> **Fuentes**: ver tema-33-fuentes.md

---

## Instrucciones

- Cada pregunta tiene **3 opciones** (A, B, C). Solo una es correcta.
- Penalización en examen real: respuesta incorrecta descuenta **1/3** del valor de una correcta.
- Tiempo orientativo: 1 minuto por pregunta.
- Distribución: Conceptos, señal, ancho de banda y capacidad (P1-P8), Medios de transmisión (P9-P17), Modos de comunicación (P18-P24), Equipos terminales y de interconexión (P25-P33), Redes y topologías (P34-P39), Conmutación y difusión (P40-P47), Redes inalámbricas y móviles (P48-P54), Seguridad y normativa (P55-P60).

---

### Pregunta 1

**Según el anexo II de la Ley 11/2022, General de Telecomunicaciones, ¿qué se entiende por «telecomunicación»?**

A) La transmisión de datos digitales entre equipos informáticos a través de una red pública
B) Toda transmisión, emisión o recepción de signos, señales, escritos, imágenes, sonidos o informaciones de cualquier naturaleza por hilo, radioelectricidad, medios ópticos u otros sistemas electromagnéticos
C) La emisión de información a distancia por medios electromagnéticos, siempre que exista un canal de retorno

<details><summary>Respuesta</summary>

**Correcta: B) Toda transmisión, emisión o recepción de signos, señales, escritos, imágenes, sonidos o informaciones de cualquier naturaleza por hilo, radioelectricidad, medios ópticos u otros sistemas electromagnéticos** Es la definición literal del apartado 79 del anexo II. Tres rasgos: es indiferente el **contenido**, es indiferente el **medio** y cubre las **tres operaciones** —transmitir, emitir y recibir—. No exige que la información sea digital ni que haya canal de retorno.

*Referencia: §1.1.1 [LGT]*
</details>

---

### Pregunta 2

**En el modelo de comunicación de Shannon, ¿sobre qué elemento actúa la fuente de ruido?**

A) Sobre el canal
B) Sobre el transmisor, en el momento de la codificación
C) Sobre el mensaje, antes de entrar en el sistema

<details><summary>Respuesta</summary>

**Correcta: A) Sobre el canal** El ruido se suma a la señal **durante su tránsito** por el medio de transmisión. De ahí que todas las técnicas de protección —codificación de canal, corrección de errores, regeneración— se apliquen antes de entrar al canal y después de salir de él.

*Referencia: §1.1.1 [SHANNON]*
</details>

---

### Pregunta 3

**¿Qué diferencia a un módem de un códec?**

A) Ninguna: son dos nombres para el mismo equipo de conversión
B) El módem convierte entre señal analógica y digital, y el códec comprime la información
C) El módem adapta datos digitales a un medio analógico, y el códec convierte una señal analógica de la fuente en digital

<details><summary>Respuesta</summary>

**Correcta: C) El módem adapta datos digitales a un medio analógico, y el códec convierte una señal analógica de la fuente en digital** Hacen operaciones **inversas**. Regla mnemotécnica: el **módem mira al medio** (modula y demodula sobre el canal); el **códec mira a la fuente** (codifica y decodifica la señal original). La compresión es una función que un códec puede incorporar, pero no lo define.

*Referencia: §1.1.1 [STALLINGS]*
</details>

---

### Pregunta 4

**Señale el orden correcto de los pasos de digitalización de una señal analógica.**

A) Muestreo, cuantificación y codificación
B) Cuantificación, muestreo y codificación
C) Codificación, muestreo y cuantificación

<details><summary>Respuesta</summary>

**Correcta: A) Muestreo, cuantificación y codificación** Primero se toman muestras a intervalos regulares, después cada muestra se aproxima al nivel más cercano de una escala finita —donde aparece el **ruido de cuantificación**— y por último cada nivel se representa con una combinación de bits.

*Referencia: §1.1.1 [STALLINGS]*
</details>

---

### Pregunta 5

**¿Cuál de los siguientes tipos de ruido es el más dañino en transmisión digital?**

A) El ruido térmico, porque está presente en todos los medios y no se puede eliminar
B) El ruido impulsivo, porque un pico de corta duración destruye un bloque entero de bits
C) El ruido de intermodulación, porque genera componentes espurias en toda la banda

<details><summary>Respuesta</summary>

**Correcta: B) El ruido impulsivo, porque un pico de corta duración destruye un bloque entero de bits** El ruido térmico es inevitable pero previsible y acotado; el impulsivo es esporádico pero devastador en digital. En una comunicación analógica el mismo pico solo produciría un chasquido audible.

*Referencia: §1.1.1 [STALLINGS]*
</details>

---

### Pregunta 6

**Un enlace de par trenzado presenta acoplamiento no deseado entre pares próximos. ¿Cómo se denomina esa perturbación y cómo se combate en el diseño del cable?**

A) Interferencia electromagnética; se combate aumentando la potencia de emisión
B) Distorsión de retardo; se combate con ecualizadores
C) Diafonía; se combate trenzando los pares, y a más vueltas por metro mayor rechazo

<details><summary>Respuesta</summary>

**Correcta: C) Diafonía; se combate trenzando los pares, y a más vueltas por metro mayor rechazo** La diafonía (*crosstalk*) es un tipo de **ruido**, y se mide con los parámetros **NEXT** y **FEXT**. El trenzado hace que las interferencias captadas por cada hilo tiendan a cancelarse en el par.

*Referencia: §1.1.1 [STALLINGS]*
</details>

---

### Pregunta 7

**¿Cuál es la unidad del ancho de banda de un canal?**

A) Bits por segundo
B) Baudios
C) Hercios

<details><summary>Respuesta</summary>

**Correcta: C) Hercios** El **ancho de banda** es un rango de **frecuencias** y se mide en hercios. La **velocidad de transmisión** se mide en bits por segundo y la **velocidad de modulación**, en baudios. Son tres magnitudes distintas que el lenguaje corriente confunde.

*Referencia: §1.2 [STALLINGS]*
</details>

---

### Pregunta 8

**Un canal tiene un ancho de banda de 3.000 Hz y una relación señal-ruido de 20 dB. Según Shannon, ¿cuál es su capacidad aproximada?**

A) Unos 60.000 bps, aplicando C = 2·B·log₂(M)
B) Unos 20.000 bps, porque 20 dB equivalen a una relación de 100 veces
C) Unos 6.000 bps, porque hay que dividir el ancho de banda entre la relación señal-ruido

<details><summary>Respuesta</summary>

**Correcta: B) Unos 20.000 bps, porque 20 dB equivalen a una relación de 100 veces** Primero se convierten los decibelios: `S/N = 10^(20/10) = 100`. Después, `C = 3.000 · log₂(1 + 100) = 3.000 · 6,66 ≈ 20.000 bps`. El error más frecuente es introducir los decibelios directamente en la fórmula. La opción A corresponde a Nyquist, que es la fórmula del canal **sin** ruido.

*Referencia: §1.2 [SHANNON]*
</details>

---

### Pregunta 9

**El canal telefónico digital básico es de 64 kbit/s. ¿De dónde procede esa cifra?**

A) De muestrear la voz a 8.000 muestras por segundo y codificar cada muestra con 8 bits
B) De dividir los 2,048 Mbit/s del enlace primario entre 32 canales
C) De aplicar el teorema de Shannon a un canal de 3.100 Hz con 30 dB de relación señal-ruido

<details><summary>Respuesta</summary>

**Correcta: A) De muestrear la voz a 8.000 muestras por segundo y codificar cada muestra con 8 bits** `8.000 × 8 = 64.000 bit/s`. La frecuencia de muestreo procede del teorema del muestreo aplicado a una voz limitada a 3.400 Hz, con margen de guarda. La opción B invierte la relación: el **E1** de 2,048 Mbit/s se obtiene agrupando **32 intervalos** de 64 kbit/s, no al revés.

*Referencia: §1.2 [UIT-T]*
</details>

---

### Pregunta 10

**¿Cuál es el criterio que distingue los medios de transmisión guiados de los no guiados?**

A) La naturaleza analógica o digital de la señal transmitida
B) La distancia que puede cubrir el enlace
C) La existencia o no de una guía artificial que confine la señal

<details><summary>Respuesta</summary>

**Correcta: C) La existencia o no de una guía artificial que confine la señal** Un radioenlace punto a punto de 40 km es **no guiado** pese a ser direccional; un cable submarino de 6.000 km es **guiado**. La propia Ley 11/2022 usa ese criterio al definir el espectro radioeléctrico como ondas «que se propagan por el espacio **sin guía artificial**».

*Referencia: §2 [LGT]*
</details>

---

### Pregunta 11

**En Ethernet sobre par trenzado, ¿cuál es la longitud máxima normalizada del enlace y cómo se desglosa?**

A) 100 metros: 90 de cable horizontal fijo más 10 de latiguillos en ambos extremos
B) 185 metros, heredados del segmento de coaxial fino
C) 100 metros de cable horizontal más 10 metros adicionales por cada latiguillo

<details><summary>Respuesta</summary>

**Correcta: A) 100 metros: 90 de cable horizontal fijo más 10 de latiguillos en ambos extremos** Es el dato numérico clave del cableado. Superarlo no produce un fallo limpio, sino **errores intermitentes**. Los 185 metros de la opción B corresponden al segmento de **10BASE2**, ya en desuso.

*Referencia: §2.1.1 [ISO11801]*
</details>

---

### Pregunta 12

**¿Qué categoría de cable de par trenzado garantiza 10 Gbit/s a la distancia completa de 100 metros?**

A) La categoría 6, con 250 MHz de ancho de banda
B) La categoría 6A, con 500 MHz de ancho de banda
C) La categoría 8, con 2.000 MHz de ancho de banda

<details><summary>Respuesta</summary>

**Correcta: B) La categoría 6A, con 500 MHz de ancho de banda** La categoría 6 solo alcanza 10 Gbit/s hasta unos 55 metros. La categoría 8, pese a tener mucho más ancho de banda, está limitada a **30 metros** y se usa en centro de datos: al subir la frecuencia, baja el alcance.

*Referencia: §2.1.1 [ISO11801]*
</details>

---

### Pregunta 13

**Señale la afirmación correcta sobre la fibra óptica monomodo y multimodo.**

A) La monomodo tiene un núcleo mayor, lo que le permite alcanzar más distancia
B) La multimodo usa diodo láser y la monomodo usa LED, por eso esta última es más barata
C) La monomodo tiene un núcleo de unas 9 micras y alcanza decenas o centenares de kilómetros; la multimodo, de 50 o 62,5 micras, se limita a distancias cortas por la dispersión modal

<details><summary>Respuesta</summary>

**Correcta: C) La monomodo tiene un núcleo de unas 9 micras y alcanza decenas o centenares de kilómetros; la multimodo, de 50 o 62,5 micras, se limita a distancias cortas por la dispersión modal** La regla, contraintuitiva, es que **a mayor núcleo, más modos, más dispersión modal y menos alcance**. La monomodo emplea **diodo láser** y la multimodo **LED o VCSEL**, justo al revés de lo que dice la opción B.

*Referencia: §2.1.1 [OM-OS]*
</details>

---

### Pregunta 14

**¿Cuál de las siguientes NO es una ventaja de la fibra óptica frente al cobre?**

A) Inmunidad total a las interferencias electromagnéticas
B) Capacidad de alimentar eléctricamente los equipos remotos por el propio cable
C) Ausencia de diafonía y dificultad para ser interceptada sin detección

<details><summary>Respuesta</summary>

**Correcta: B) Capacidad de alimentar eléctricamente los equipos remotos por el propio cable** La fibra **no transporta energía**: no existe «PoE óptico». Un equipo conectado por fibra necesita alimentación propia, lo que es precisamente uno de sus inconvenientes prácticos frente al par trenzado con **PoE**.

*Referencia: §2.1.1 [OM-OS]*
</details>

---

### Pregunta 15

**Según el anexo II de la Ley 11/2022, el espectro radioeléctrico se define como ondas electromagnéticas cuya frecuencia se fija convencionalmente por debajo de:**

A) 3.000 GHz
B) 300 GHz
C) 30 GHz

<details><summary>Respuesta</summary>

**Correcta: A) 3.000 GHz** Es decir, 3 THz. La definición añade el otro requisito: que se propaguen «por el espacio **sin guía artificial**». Los 300 GHz de la opción B son el límite superior de la banda **EHF**, y los 30 GHz, el de la banda **SHF**.

*Referencia: §2.2.1 [LGT]*
</details>

---

### Pregunta 16

**¿Qué banda del espectro se caracteriza por la propagación ionosférica, que permite alcances intercontinentales?**

A) HF, de 3 a 30 MHz
B) VHF, de 30 a 300 MHz
C) UHF, de 300 MHz a 3 GHz

<details><summary>Respuesta</summary>

**Correcta: A) HF, de 3 a 30 MHz** Es la onda corta: la señal se refleja en las capas ionizadas de la atmósfera y vuelve a la Tierra. Depende de la hora, la estación y la actividad solar, lo que la hace poco fiable para servicios comerciales. A partir de **VHF** domina la propagación por **visión directa**.

*Referencia: §2.2.1 [UIT-R]*
</details>

---

### Pregunta 17

**Al aumentar la frecuencia de trabajo de un sistema radio, ¿qué ocurre?**

A) Aumentan a la vez la capacidad y el alcance, por eso el 5G usa 26 GHz para cobertura rural
B) Disminuyen tanto la capacidad como el alcance, por eso se prefieren las bandas bajas
C) Aumenta la capacidad disponible pero disminuyen el alcance y la penetración en obstáculos

<details><summary>Respuesta</summary>

**Correcta: C) Aumenta la capacidad disponible pero disminuyen el alcance y la penetración en obstáculos** Es la regla de oro de la radio y explica el reparto de bandas del 5G: **700 MHz para cobertura** —rural y en interiores— y **26 GHz para capacidad** en puntos calientes urbanos. Las antenas, además, son tanto más pequeñas cuanto mayor es la frecuencia.

*Referencia: §2.2.1 [UIT-R]*
</details>

---

### Pregunta 18

**En un acuerdo de nivel de servicio para telefonía IP, ¿qué parámetro es más crítico y por qué?**

A) El ancho de banda, porque la voz digitalizada exige un caudal elevado
B) La fluctuación o *jitter*, porque la variación del retardo produce cortes y voz metálica
C) La tasa de error de bit, porque un solo bit erróneo interrumpe la llamada

<details><summary>Respuesta</summary>

**Correcta: B) La fluctuación o *jitter*, porque la variación del retardo produce cortes y voz metálica** La voz consume muy poco caudal (del orden de decenas de kbit/s) y tolera errores aislados. Lo que no tolera es la irregularidad del retardo: los amortiguadores antifluctuación la convierten en latencia, que es el mal menor.

*Referencia: §2.3 [KUROSE]*
</details>

---

### Pregunta 19

**Un enlace pierde 30 dB de potencia. ¿Cuántas veces se ha reducido la potencia de la señal?**

A) 30 veces
B) 300 veces
C) 1.000 veces

<details><summary>Respuesta</summary>

**Correcta: C) 1.000 veces** El decibelio es **logarítmico**: `dB = 10·log₁₀(P₁/P₂)`, de modo que 30 dB equivalen a `10³ = 1.000`. Valores de referencia: 3 dB ≈ 2 veces, 10 dB = 10 veces, 20 dB = 100 veces. Las atenuaciones en decibelios de tramos sucesivos **se suman**.

*Referencia: §2.3 [STALLINGS]*
</details>

---

### Pregunta 20

**¿En qué modo de direccionalidad opera una red Wi-Fi?**

A) Semidúplex, porque una radio que transmite no puede escuchar su propia frecuencia
B) Dúplex, porque el usuario puede navegar y subir ficheros simultáneamente
C) Símplex, porque el punto de acceso es siempre el emisor y el cliente el receptor

<details><summary>Respuesta</summary>

**Correcta: A) Semidúplex, porque una radio que transmite no puede escuchar su propia frecuencia** Es una limitación **física**, no de diseño. La misma razón explica por qué el Wi-Fi usa **CSMA/CA** —evitación de colisiones— y no CSMA/CD: no puede detectar la colisión mientras se produce.

*Referencia: §3.1 [IEEE802.11]*
</details>

---

### Pregunta 21

**Señale la afirmación correcta sobre el dúplex por división de tiempo (TDD).**

A) Es una modalidad de transmisión semidúplex, porque los extremos se turnan
B) Ofrece un servicio percibido como dúplex, porque los turnos se alternan en el orden de los microsegundos
C) Solo es posible en medios guiados, porque exige dos canales físicos independientes

<details><summary>Respuesta</summary>

**Correcta: B) Ofrece un servicio percibido como dúplex, porque los turnos se alternan en el orden de los microsegundos** El semidúplex es una limitación **visible** para el usuario, que debe esperar su turno. El TDD, en cambio, es una técnica de implementación del dúplex sobre un único canal, alternativa al **FDD**, que sí usa dos bandas de frecuencia.

*Referencia: §3.1 [FOROUZAN]*
</details>

---

### Pregunta 22

**En transmisión asíncrona con 8 bits de datos, 1 bit de arranque, 1 de paridad y 1 de parada, ¿cuál es la eficiencia?**

A) 100 %, porque los bits de servicio no consumen tiempo de canal
B) 88,9 %, porque solo el bit de arranque es sobrecarga
C) 72,7 %, porque de cada 11 bits transmitidos solo 8 son útiles

<details><summary>Respuesta</summary>

**Correcta: C) 72,7 %, porque de cada 11 bits transmitidos solo 8 son útiles** `8/11 = 0,727`. La sobrecarga del **27,3 %** es constante e independiente del volumen, y es lo que hace inviable la transmisión asíncrona para grandes volúmenes de datos. La transmisión **síncrona** amortiza sus bits de servicio sobre bloques de miles de bits.

*Referencia: §3.2 [STALLINGS]*
</details>

---

### Pregunta 23

**¿Qué mecanismo permite al receptor mantener el sincronismo en una transmisión síncrona sin línea de reloj dedicada?**

A) Una codificación de línea autosincronizante, como Manchester, de la que se extrae el reloj
B) La inserción de un bit de arranque al principio de cada carácter
C) El envío periódico de tramas vacías que reinician el contador del receptor

<details><summary>Respuesta</summary>

**Correcta: A) Una codificación de línea autosincronizante, como Manchester, de la que se extrae el reloj** Manchester fuerza una transición en el centro de cada bit; otros esquemas —4B/5B, 8B/10B, 64B/66B— insertan bits redundantes con el mismo fin. El bit de arranque de la opción B es propio de la transmisión **asíncrona**.

*Referencia: §3.2 [STALLINGS]*
</details>

---

### Pregunta 24

**¿Por qué la transmisión paralela ha sido desplazada por la serie a alta velocidad?**

A) Porque el paralelo no permite corrección de errores
B) Porque el paralelo exige apantallamiento individual de cada hilo, lo que encarece el cable
C) Porque la desviación temporal entre hilos (*skew*) y la diafonía se hacen intolerables al subir la frecuencia

<details><summary>Respuesta</summary>

**Correcta: C) Porque la desviación temporal entre hilos (*skew*) y la diafonía se hacen intolerables al subir la frecuencia** Los bits que salieron a la vez no llegan a la vez, y cuanto más alta es la frecuencia menor es el periodo de bit y antes resulta intolerable esa diferencia. Por eso PCI pasó a PCI Express, PATA a SATA y el puerto paralelo a USB.

*Referencia: §3.3 [TANENBAUM]*
</details>

---

### Pregunta 25

**En la terminología clásica de la UIT-T, ¿qué caracteriza al ETCD (o DCE)?**

A) Es el equipo que constituye el origen o el destino final de los datos
B) Es el equipo que adapta la señal al medio de transmisión y suele proporcionar la señal de reloj
C) Es el equipo que interconecta dos redes con arquitecturas distintas traduciendo entre ellas

<details><summary>Respuesta</summary>

**Correcta: B) Es el equipo que adapta la señal al medio de transmisión y suele proporcionar la señal de reloj** El **ETD (DTE)** es el origen o destino de los datos —opción A—; el **ETCD (DCE)** los adapta al circuito. La opción C describe una **pasarela**. El punto donde termina la red del operador es el **punto de terminación de red**, frontera de responsabilidad.

*Referencia: §4.1 [UIT-T]*
</details>

---

### Pregunta 26

**Un concentrador (*hub*) con ocho equipos conectados, ¿cuántos dominios de colisión y de difusión crea?**

A) Un dominio de colisión y un dominio de difusión
B) Ocho dominios de colisión y un dominio de difusión
C) Ocho dominios de colisión y ocho dominios de difusión

<details><summary>Respuesta</summary>

**Correcta: A) Un dominio de colisión y un dominio de difusión** El concentrador es un **repetidor multipuerto** de capa 1: repite por todos los puertos sin mirar direcciones, de modo que todos los equipos comparten el medio, reparten el ancho de banda y funcionan en semidúplex. La opción B describe un **conmutador**.

*Referencia: §4.2.1 [TANENBAUM]*
</details>

---

### Pregunta 27

**¿Cuál de estas afirmaciones sobre el conmutador (*switch*) es correcta?**

A) Divide tanto el dominio de colisión como el de difusión, uno por cada puerto
B) Divide el dominio de colisión —uno por puerto— pero no el de difusión, salvo que se configuren VLAN
C) No divide ningún dominio, porque opera en la capa física igual que el concentrador

<details><summary>Respuesta</summary>

**Correcta: B) Divide el dominio de colisión —uno por puerto— pero no el de difusión, salvo que se configuren VLAN** Es la pregunta de equipos de red más repetida del temario. Una trama de difusión (`FF:FF:FF:FF:FF:FF`) se propaga por todos los puertos del conmutador. Solo el **encaminador** y las **VLAN** dividen el dominio de difusión.

*Referencia: §4.2.1 [IEEE802.1]*
</details>

---

### Pregunta 28

**Un conmutador recibe una trama cuya dirección MAC de destino no figura en su tabla. ¿Qué hace?**

A) La descarta y envía un mensaje de error al emisor
B) La retiene en memoria hasta que aprenda la dirección por otra vía
C) La inunda por todos los puertos excepto por aquel por el que llegó

<details><summary>Respuesta</summary>

**Correcta: C) La inunda por todos los puertos excepto por aquel por el que llegó** Es la operación de **inundación** (*flooding*), una de las cuatro del conmutador junto con aprender, reenviar y envejecer. Hace lo mismo con las tramas de difusión y de multidifusión.

*Referencia: §4.2.1 [IEEE802.1]*
</details>

---

### Pregunta 29

**¿Qué modo de conmutación de un switch ofrece la menor latencia y a costa de qué?**

A) El modo directo (*cut-through*), a costa de no detectar las tramas erróneas, porque reenvía tras leer solo la MAC de destino
B) El modo de almacenamiento y reenvío, a costa de consumir más memoria
C) El modo libre de fragmentos, a costa de descartar las tramas de menos de 64 bytes

<details><summary>Respuesta</summary>

**Correcta: A) El modo directo (*cut-through*), a costa de no detectar las tramas erróneas, porque reenvía tras leer solo la MAC de destino** El modo de **almacenamiento y reenvío** espera a la trama completa y comprueba el **CRC**, con mayor latencia pero filtrando lo erróneo. El modo **libre de fragmentos** lee los primeros 64 bytes, en un punto intermedio.

*Referencia: §4.2.1 [TANENBAUM]*
</details>

---

### Pregunta 30

**¿Por qué un bucle de nivel 2 entre dos conmutadores es tan destructivo, mientras que un bucle de encaminamiento en capa 3 no lo es de forma indefinida?**

A) Porque en capa 2 no existe tabla de reenvío y las tramas se replican al azar
B) Porque la trama Ethernet no tiene campo TTL, mientras que el paquete IP sí lo tiene y acaba descartándose
C) Porque los conmutadores no pueden ejecutar protocolos de prevención de bucles

<details><summary>Respuesta</summary>

**Correcta: B) Porque la trama Ethernet no tiene campo TTL, mientras que el paquete IP sí lo tiene y acaba descartándose** Sin TTL, una única trama de difusión da vueltas indefinidamente y se multiplica en cada nodo: es la **tormenta de difusión**. Los conmutadores sí ejecutan protocolos de prevención —**STP** y **RSTP**—, que es justamente el remedio.

*Referencia: §4.2.1, §6.2.1 [IEEE802.1]*
</details>

---

### Pregunta 31

**En su acepción estricta, ¿qué es una pasarela (*gateway*)?**

A) La dirección IP del encaminador que se configura en cada equipo para salir de la red local
B) Un conmutador capaz de encaminar entre VLAN a velocidad de cable
C) El equipo de interconexión que opera en las capas superiores y traduce entre redes con arquitecturas o protocolos distintos

<details><summary>Respuesta</summary>

**Correcta: C) El equipo de interconexión que opera en las capas superiores y traduce entre redes con arquitecturas o protocolos distintos** Ejemplos: pasarela de voz entre la red telefónica y la telefonía IP, pasarela de IoT entre Zigbee e IP. La opción A describe la **puerta de enlace predeterminada**, que es un encaminador, y la B, un **conmutador de capa 3**.

*Referencia: §4.2.2 [TANENBAUM]*
</details>

---

### Pregunta 32

**Varios puntos de acceso que anuncian el mismo SSID y entre los que un cliente puede desplazarse forman:**

A) Un ESS (*Extended Service Set*)
B) Un BSS (*Basic Service Set*)
C) Un IBSS o red en modo *ad hoc*

<details><summary>Respuesta</summary>

**Correcta: A) Un ESS (*Extended Service Set*)** El **BSS** es **una sola celda**: un punto de acceso y sus clientes, identificado por el **BSSID**. El **IBSS** o modo *ad hoc* es la comunicación entre clientes **sin** punto de acceso.

*Referencia: §4.2.2, §7.1 [IEEE802.11]*
</details>

---

### Pregunta 33

**¿Qué equipo desempeña la función de repartir la configuración, los canales y la potencia de una flota de puntos de acceso inalámbricos?**

A) El conmutador de capa 3 del núcleo de la red
B) El controlador de red inalámbrica (WLC)
C) El servidor RADIUS de autenticación

<details><summary>Respuesta</summary>

**Correcta: B) El controlador de red inalámbrica (WLC)** En instalaciones profesionales los puntos de acceso son **ligeros** y se gestionan centralizadamente desde el controlador, que además coordina la itinerancia rápida y la detección de puntos de acceso no autorizados. El **RADIUS** valida credenciales, pero no configura la radio.

*Referencia: §4.2.2 [IEEE802.11]*
</details>

---

### Pregunta 34

**Según el anexo II de la Ley 11/2022, una red de comunicaciones electrónicas de «alta capacidad» es la capaz de prestar acceso de banda ancha a velocidades de al menos:**

A) 30 Mbps
B) 100 Mbps
C) 10 Mbps

<details><summary>Respuesta</summary>

**Correcta: A) 30 Mbps** La red de **muy alta capacidad**, por su parte, es la compuesta totalmente de elementos de fibra óptica al menos hasta el punto de distribución, o la capaz de ofrecer un rendimiento similar. Los **10 Mbps** de la opción C son la velocidad mínima del **servicio universal** (art. 37).

*Referencia: §5 [LGT]*
</details>

---

### Pregunta 35

**Más allá de la extensión geográfica, ¿cuál es el criterio estructural que distingue una LAN de una WAN?**

A) La tecnología empleada: Ethernet en LAN y siempre fibra óptica en WAN
B) El número de equipos conectados, que en una WAN supera siempre los mil
C) La titularidad del medio: en la LAN el cableado es propiedad de quien la explota, mientras que en la WAN se contrata a un operador porque atraviesa dominio público

<details><summary>Respuesta</summary>

**Correcta: C) La titularidad del medio: en la LAN el cableado es propiedad de quien la explota, mientras que en la WAN se contrata a un operador porque atraviesa dominio público** A ese criterio se suman la **velocidad y latencia** —gigabits y microsegundos frente a menos caudal por euro y milisegundos— y la **tasa de error**, mayor en la WAN por atravesar medios heterogéneos.

*Referencia: §5.1 [TANENBAUM]*
</details>

---

### Pregunta 36

**En una topología en bus, ¿qué consecuencia tiene un corte en el cable troncal?**

A) Solo quedan aislados los equipos situados más allá del corte
B) Toda la red deja de funcionar, porque el medio es único y compartido
C) La red sigue funcionando gracias a los terminadores, que reencaminan la señal

<details><summary>Respuesta</summary>

**Correcta: B) Toda la red deja de funcionar, porque el medio es único y compartido** Es el gran defecto del bus, y la razón de que desapareciera de las redes locales. Los **terminadores** de sus extremos evitan las reflexiones de la señal, no aportan redundancia alguna.

*Referencia: §5.2 [FOROUZAN]*
</details>

---

### Pregunta 37

**¿Cuántos enlaces requiere una malla completa de 10 nodos?**

A) 45
B) 90
C) 100

<details><summary>Respuesta</summary>

**Correcta: A) 45** Se aplica `n(n−1)/2 = 10 · 9 / 2 = 45`. El crecimiento es **cuadrático**, motivo por el que la malla completa no escala y en la práctica se emplea la **malla parcial** o el **doble anillo**, que con n enlaces ya garantiza dos caminos entre cualquier par de nodos.

*Referencia: §5.2 [TANENBAUM]*
</details>

---

### Pregunta 38

**Una red Ethernet moderna sobre conmutador presenta:**

A) Topología física de anillo y topología lógica de estrella
B) Topología física y lógica coincidentes, ambas en bus
C) Topología física de estrella y topología lógica de bus conmutado

<details><summary>Respuesta</summary>

**Correcta: C) Topología física de estrella y topología lógica de bus conmutado** Todos los cables van radialmente al armario —estrella física— mientras que cada puerto es un enlace punto a punto dedicado. El caso histórico inverso es **Token Ring**: estrella física, con los cables a la MAU, y **anillo lógico**.

*Referencia: §5.2 [FOROUZAN]*
</details>

---

### Pregunta 39

**Señale la afirmación correcta sobre la conmutación de circuitos.**

A) No requiere fase de establecimiento, porque la ruta se decide paquete a paquete
B) Reserva un camino dedicado durante toda la comunicación, con retardo constante y sin fluctuación, aunque desaprovecha la capacidad en los silencios
C) Almacena el mensaje completo en cada nodo antes de reenviarlo al siguiente

<details><summary>Respuesta</summary>

**Correcta: B) Reserva un camino dedicado durante toda la comunicación, con retardo constante y sin fluctuación, aunque desaprovecha la capacidad en los silencios** Sus **tres fases** son establecimiento, transferencia y liberación. La opción C describe la conmutación de **mensajes**; la A, la de **paquetes** en modo datagrama.

*Referencia: §6.1.1 [TANENBAUM]*
</details>

---

### Pregunta 40

**¿Cuál es el principal inconveniente de la conmutación de mensajes que resolvió la conmutación de paquetes?**

A) Que no permitía establecer prioridades entre distintos mensajes
B) Que producía bloqueo cuando no había recursos disponibles en la ruta
C) Que exigía almacenar el mensaje completo en cada nodo y que un mensaje grande monopolizaba el enlace, sin posibilidad de encauzamiento

<details><summary>Respuesta</summary>

**Correcta: C) Que exigía almacenar el mensaje completo en cada nodo y que un mensaje grande monopolizaba el enlace, sin posibilidad de encauzamiento** Fragmentar en paquetes pequeños reduce la memoria necesaria y permite el **encauzamiento**: mientras un nodo reenvía un paquete, el anterior ya le está enviando el siguiente. El **bloqueo** de la opción B es propio de la conmutación de **circuitos**.

*Referencia: §6.1.1 [TANENBAUM]*
</details>

---

### Pregunta 41

**En una red de conmutación de paquetes en modo datagrama:**

A) Cada paquete lleva la dirección completa de destino y elige su ruta en cada nodo, por lo que pueden llegar desordenados
B) Se establece previamente un camino que todos los paquetes siguen, garantizando el orden de llegada
C) Se reservan recursos físicos en cada nodo del trayecto durante toda la comunicación

<details><summary>Respuesta</summary>

**Correcta: A) Cada paquete lleva la dirección completa de destino y elige su ruta en cada nodo, por lo que pueden llegar desordenados** Es el modo de funcionamiento de **IP**. La opción B describe el **circuito virtual** (X.25, Frame Relay, ATM, MPLS), que sigue siendo conmutación de **paquetes**; la C, la conmutación de **circuitos**.

*Referencia: §6.1.1 [TANENBAUM]*
</details>

---

### Pregunta 42

**Señale la afirmación correcta sobre MPLS.**

A) Es una técnica de conmutación de circuitos que reserva capacidad extremo a extremo
B) Es conmutación de paquetes con lógica de circuito virtual, basada en el reenvío por etiquetas cortas
C) Es un protocolo de difusión que replica el tráfico en los puntos de bifurcación de la red

<details><summary>Respuesta</summary>

**Correcta: B) Es conmutación de paquetes con lógica de circuito virtual, basada en el reenvío por etiquetas cortas** El **circuito virtual no es un circuito**: no hay reserva de recursos físicos ni camino dedicado, solo una ruta preacordada identificada por una etiqueta. Es con lo que los operadores construyen hoy las redes privadas virtuales corporativas.

*Referencia: §6.1.1 [TANENBAUM]*
</details>

---

### Pregunta 43

**Un mensaje de 12.000 bits atraviesa 3 enlaces de 4.000 bps, fragmentado en paquetes de 4.000 bits. Despreciando propagación y proceso, ¿cuál es el retardo total?**

A) 9 segundos, igual que en conmutación de mensajes
B) 3 segundos, porque el primer paquete llega en ese tiempo
C) 5 segundos, aplicando la fórmula del encauzamiento

<details><summary>Respuesta</summary>

**Correcta: C) 5 segundos, aplicando la fórmula del encauzamiento** Cada paquete tarda `4.000/4.000 = 1 s` por enlace, y hay 3 paquetes y 3 enlaces: `T = (3 + 3 − 1) × 1 = 5 s`. En conmutación de **mensajes** habrían sido `3 s × 3 enlaces = 9 s`, que es la opción A. El encauzamiento reduce el retardo casi a la mitad sin cambiar un solo cable.

*Referencia: §6.1.1 [TANENBAUM]*
</details>

---

### Pregunta 44

**¿Cuál es la dirección MAC de difusión en Ethernet?**

A) 01:00:5E:00:00:01
B) FF:FF:FF:FF:FF:FF
C) 00:00:00:00:00:00

<details><summary>Respuesta</summary>

**Correcta: B) FF:FF:FF:FF:FF:FF** Los 48 bits a uno. La dirección de la opción A pertenece al rango **01:00:5E**, reservado para la correspondencia de la **multidifusión IPv4** sobre MAC; la de la opción C no es una dirección de difusión.

*Referencia: §6.2.1 [RFC1112]*
</details>

---

### Pregunta 45

**Señale la afirmación correcta sobre la difusión en IPv6.**

A) IPv6 suprime la difusión y la sustituye por multidifusión al grupo ff02::1, además de incorporar la anydifusión
B) IPv6 mantiene la difusión pero cambia su dirección a ::1
C) IPv6 solo admite unidifusión, por lo que ARP se sustituye por consultas al DNS

<details><summary>Respuesta</summary>

**Correcta: A) IPv6 suprime la difusión y la sustituye por multidifusión al grupo ff02::1, además de incorporar la anydifusión** El prefijo de toda la multidifusión IPv6 es `ff00::/8`, y la suscripción a grupos se hace con **MLD**, equivalente a IGMP. Es una de las preguntas más frecuentes sobre IPv6.

*Referencia: §6.2.1 [RFC4291]*
</details>

---

### Pregunta 46

**¿Por qué un equipo que arranca sin dirección IP necesita usar difusión?**

A) Porque el protocolo DHCP exige cifrar la petición y solo la difusión lo permite
B) Porque la difusión es más rápida que la unidifusión en redes conmutadas
C) Porque sin dirección propia ni conocimiento del servidor no puede dirigirse a ningún destinatario concreto

<details><summary>Respuesta</summary>

**Correcta: C) Porque sin dirección propia ni conocimiento del servidor no puede dirigirse a ningún destinatario concreto** Es el «problema del arranque» que la difusión resuelve, igual que en **ARP**, donde se pregunta a todos qué equipo tiene una IP determinada. Por eso la difusión no es un residuo, sino un mecanismo imprescindible.

*Referencia: §6.2.1 [RFC826]*
</details>

---

### Pregunta 47

**En televisión digital terrestre, ¿qué es un múltiplex o múltiple digital?**

A) El conjunto de repetidores que cubren una misma demarcación territorial
B) La señal compuesta transmitida en una frecuencia radioeléctrica que, mediante tecnología digital, permite incorporar las señales de varios servicios de comunicación audiovisual y de comunicaciones electrónicas
C) El equipo receptor que separa la señal de vídeo de la de audio en el domicilio del usuario

<details><summary>Respuesta</summary>

**Correcta: B) La señal compuesta transmitida en una frecuencia radioeléctrica que, mediante tecnología digital, permite incorporar las señales de varios servicios de comunicación audiovisual y de comunicaciones electrónicas** Es decir, **un canal radioeléctrico que transporta varios canales de televisión**. Esa ganancia de la multiplexación digital es la que permitió liberar espectro: el **dividendo digital**.

*Referencia: §6.2.1 [L13-2022]*
</details>

---

### Pregunta 48

**¿Cuántos canales sin solapamiento hay disponibles en la banda de 2,4 GHz para Wi-Fi con canales de 20 MHz?**

A) Tres: los canales 1, 6 y 11
B) Trece, uno por cada canal numerado
C) Ocho, coincidiendo con los de la banda de 5 GHz

<details><summary>Respuesta</summary>

**Correcta: A) Tres: los canales 1, 6 y 11** Cada canal ocupa 20 MHz pero los canales numerados están separados solo 5 MHz, de modo que se solapan. Es el dato que explica la mayor parte de los problemas de rendimiento del Wi-Fi y el criterio básico de planificación: **celdas adyacentes nunca en el mismo canal**.

*Referencia: §7.1 [IEEE802.11]*
</details>

---

### Pregunta 49

**¿Cuál es el rasgo distintivo de IEEE 802.11be (Wi-Fi 7), publicado en julio de 2025?**

A) La incorporación de OFDMA y de la modulación 1024-QAM
B) El uso de la banda de 6 GHz, que no estaba disponible en generaciones anteriores
C) La operación multienlace (MLO), que permite usar varias bandas simultáneamente, junto con canales de 320 MHz y modulación 4096-QAM

<details><summary>Respuesta</summary>

**Correcta: C) La operación multienlace (MLO), que permite usar varias bandas simultáneamente, junto con canales de 320 MHz y modulación 4096-QAM** El MLO aporta sobre todo **fiabilidad**: si una banda se degrada, el tráfico sigue por las otras. OFDMA y 1024-QAM son de **Wi-Fi 6**, y la banda de 6 GHz ya la abrió **Wi-Fi 6E**.

*Referencia: §7.1 [IEEE802.11]*
</details>

---

### Pregunta 50

**Indique la frecuencia de trabajo y el alcance operativo característicos de NFC.**

A) 2,4 GHz y unos 10 metros
B) 13,56 MHz y unos 10 centímetros
C) 868 MHz y varios kilómetros

<details><summary>Respuesta</summary>

**Correcta: B) 13,56 MHz y unos 10 centímetros** El alcance corto **es la característica de seguridad**, no una limitación: obliga a una aproximación deliberada y hace impracticable la interceptación a distancia. Los 868 MHz de la opción C corresponden a **LoRaWAN** en Europa.

*Referencia: §7.1 [ISO-NFC]*
</details>

---

### Pregunta 51

**¿Cuál es la altura de la órbita geoestacionaria y qué latencia de ida y vuelta implica aproximadamente?**

A) 35.786 km y unos 250 ms
B) 2.000 km y unos 20 ms
C) 20.200 km y unos 100 ms

<details><summary>Respuesta</summary>

**Correcta: A) 35.786 km y unos 250 ms** La señal recorre ida y vuelta unos 72.000 km. Por eso el satélite **GEO** es excelente para difusión de televisión, que tolera cualquier retardo, y malo para tiempo real. La opción B corresponde al límite de las órbitas **LEO** y la C, al entorno de las **MEO** de los sistemas de navegación.

*Referencia: §7.2 [TANENBAUM]*
</details>

---

### Pregunta 52

**¿Qué distingue a LoRaWAN de NB-IoT dentro de las tecnologías LPWAN?**

A) Que LoRaWAN ofrece mucho mayor caudal, y NB-IoT está limitado a mensajes de unos pocos bytes
B) Que LoRaWAN admite movilidad y voz, mientras que NB-IoT es exclusivamente estático
C) Que LoRaWAN opera en bandas de uso común y permite desplegar red propia, mientras que NB-IoT es una tecnología 3GPP sobre espectro licenciado del operador

<details><summary>Respuesta</summary>

**Correcta: C) Que LoRaWAN opera en bandas de uso común y permite desplegar red propia, mientras que NB-IoT es una tecnología 3GPP sobre espectro licenciado del operador** Es la disyuntiva de cualquier proyecto de sensórica urbana: red propia sin coste por dispositivo pero sin garantías de calidad, frente a servicio del operador con cobertura y calidad contratadas. **LTE-M** es el que admite movilidad y voz.

*Referencia: §7.2 [LORA]*
</details>

---

### Pregunta 53

**¿Cuál fue el salto arquitectónico que introdujo 4G/LTE respecto de 3G?**

A) La aparición de la tarjeta SIM y del servicio de mensajes cortos
B) La desaparición de la conmutación de circuitos: la red pasa a ser todo IP y la voz se transporta como datos mediante VoLTE
C) La introducción de la conmutación de paquetes junto a la de circuitos, facturando por volumen

<details><summary>Respuesta</summary>

**Correcta: B) La desaparición de la conmutación de circuitos: la red pasa a ser todo IP y la voz se transporta como datos mediante VoLTE** Es el salto conceptual más profundo de la serie. La **SIM** y el **SMS** llegaron con **2G/GSM**, y la coexistencia de circuitos y paquetes con facturación por volumen es de **GPRS (2.5G)**.

*Referencia: §8.2 [3GPP]*
</details>

---

### Pregunta 54

**Un servicio municipal exige latencia acotada y fiabilidad garantizada sobre red móvil. ¿Qué se necesita?**

A) Un despliegue 5G autónomo (SA), con núcleo 5G propio, que es el único que habilita el fraccionamiento de red y URLLC reales
B) Basta con cualquier despliegue 5G, porque la norma garantiza 1 ms de latencia en todos los casos
C) Un despliegue 5G no autónomo (NSA), que aprovecha el núcleo 4G y aporta menor latencia

<details><summary>Respuesta</summary>

**Correcta: A) Un despliegue 5G autónomo (SA), con núcleo 5G propio, que es el único que habilita el fraccionamiento de red y URLLC reales** El despliegue **NSA** se apoya en el núcleo 4G y solo aporta más velocidad, es decir, **eMBB**. Es la distinción que separa el «5G comercial» del «5G que transforma servicios».

*Referencia: §8.2 [3GPP]*
</details>

---

### Pregunta 55

**¿Cuál de las siguientes medidas NO aporta seguridad real a una red Wi-Fi?**

A) Emplear WPA3 con autenticación SAE
B) Autenticar a los usuarios con 802.1X contra un servidor RADIUS
C) Ocultar el SSID y filtrar por dirección MAC

<details><summary>Respuesta</summary>

**Correcta: C) Ocultar el SSID y filtrar por dirección MAC** Son **medidas cosméticas**: el SSID viaja en claro en las tramas de asociación de cualquier cliente que se conecte, y las direcciones MAC circulan en claro y se clonan trivialmente. Además complican la operación y dan una falsa sensación de protección.

*Referencia: §9.1 [CCN-STIC-816]*
</details>

---

### Pregunta 56

**¿Qué aporta el mecanismo SAE de WPA3 frente a la clave precompartida de WPA2?**

A) Sustituye el cifrado AES por un algoritmo de curva elíptica más rápido
B) Impide el ataque de diccionario fuera de línea aunque la contraseña sea débil, y proporciona confidencialidad directa
C) Permite prescindir de contraseña, cifrando el enlace de forma oportunista en redes abiertas

<details><summary>Respuesta</summary>

**Correcta: B) Impide el ataque de diccionario fuera de línea aunque la contraseña sea débil, y proporciona confidencialidad directa** Con **SAE**, capturar el tráfico hoy y descubrir la clave mañana ya no permite descifrarlo. La opción C describe **OWE** (*Wi-Fi Enhanced Open*), que es otra aportación distinta de WPA3.

*Referencia: §9.1 [WIFI-ALLIANCE]*
</details>

---

### Pregunta 57

**¿Qué exige la medida `mp.com.4` del anexo II del Esquema Nacional de Seguridad respecto de las comunicaciones inalámbricas?**

A) Que se empleen en un segmento de red separado
B) Que se prohíban en sistemas de categoría MEDIA o superior
C) Que se cifren siempre con productos certificados, en cualquier categoría

<details><summary>Respuesta</summary>

**Correcta: A) Que se empleen en un segmento de red separado** Es el requisito `mp.com.4.2`, literal. La medida `mp.com.4` (separación de flujos de información en la red) **no aplica** en categoría BÁSICA, exige `+[R1 o R2 o R3]` en MEDIA y `+[R2 o R3] + R4` en ALTA. El refuerzo **R1** implementa los segmentos mediante **VLAN**, con un mínimo de tres subredes: usuarios, servicios y administración.

*Referencia: §9.1 [ENS]*
</details>

---

### Pregunta 58

**Conforme al artículo 2 de la Ley 11/2022, las telecomunicaciones son:**

A) Servicios públicos de titularidad estatal, prestados en régimen de concesión
B) Servicios de interés general prestados en régimen de libre competencia, teniendo la consideración de servicio público únicamente los regulados en el artículo 4
C) Servicios privados sin obligaciones de interés general, salvo pacto contractual con la Administración

<details><summary>Respuesta</summary>

**Correcta: B) Servicios de interés general prestados en régimen de libre competencia, teniendo la consideración de servicio público únicamente los regulados en el artículo 4** Esos servicios del art. 4 son los de **seguridad nacional, defensa nacional, seguridad pública, seguridad vial y protección civil**. Por tanto, la telefonía y el acceso a internet **no son servicio público** en España: son servicios en competencia sujetos a **obligaciones** de servicio público.

*Referencia: §9.2 [LGT]*
</details>

---

### Pregunta 59

**¿Qué velocidad mínima de acceso a internet de banda ancha garantiza el servicio universal según el artículo 37 de la Ley 11/2022?**

A) 30 Mbit/s en sentido descendente, en ubicación fija o móvil
B) 100 Mbit/s simétricos en ubicación fija
C) 10 Mbit/s en sentido descendente, en ubicación fija, escalables a 30 Mbit/s mediante real decreto

<details><summary>Respuesta</summary>

**Correcta: C) 10 Mbit/s en sentido descendente, en ubicación fija, escalables a 30 Mbit/s mediante real decreto** La ley prevé expresamente ese escalado «tan pronto como sea posible en función de la extensión de las redes y del estado de la técnica». El servicio universal es de **ubicación fija**: **no** garantiza cobertura móvil. El **anexo III** enumera los once servicios que la conexión debe soportar, entre ellos la administración electrónica.

*Referencia: §9.2 [LGT]*
</details>

---

### Pregunta 60

**Cuando un ayuntamiento instala y explota redes públicas de comunicaciones electrónicas o presta servicios disponibles al público, ¿a qué régimen queda sujeto según el artículo 13 de la Ley 11/2022?**

A) Debe cumplir el principio de inversor privado, con separación de cuentas y conforme a los principios de neutralidad, transparencia, no distorsión de la competencia y no discriminación
B) Queda exento de cualquier condición, por tratarse de una Administración pública que actúa en interés general
C) Necesita una concesión demanial otorgada por la CNMC previa licitación pública

<details><summary>Respuesta</summary>

**Correcta: A) Debe cumplir el principio de inversor privado, con separación de cuentas y conforme a los principios de neutralidad, transparencia, no distorsión de la competencia y no discriminación** Debe respetar además la normativa de **ayudas de Estado** (arts. 107 y 108 del TFUE). La ley contempla una excepción expresa: la difusión de **televisión digital en zonas sin cobertura de TDT**, donde declara que se produce un **fallo de mercado**.

*Referencia: §9.2 [LGT]*
</details>
