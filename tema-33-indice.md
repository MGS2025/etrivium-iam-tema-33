# Tema 33 — Índice

> **Título oficial**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.
>
> **Bloque**: Parte II — Técnico (Temas 11-40)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

---

## Estructura del tema

1. **Conceptos generales de telecomunicaciones y modelo de comunicación**
   1.1. Elementos del sistema de transmisión y perturbaciones en el canal
   1.2. Transmisión analógica y digital: ancho de banda y velocidad de transmisión

2. **Medios de transmisión**
   2.1. Medios de transmisión guiados
   2.1.1. Par trenzado, cable coaxial y fibra óptica
   2.2. Medios de transmisión no guiados
   2.2.1. Espectro radioeléctrico, radiofrecuencia, microondas e infrarrojos
   2.3. Parámetros de caracterización y calidad en medios de transmisión

3. **Modos de comunicación**
   3.1. Modos según la direccionalidad: simplex, half-duplex y full-duplex
   3.2. Modos según el sincronismo: transmisión síncrona y asíncrona
   3.3. Modos según la forma de transmisión: serie y paralelo

4. **Equipos terminales y de red**
   4.1. Equipos terminales de datos y equipos de conversión
   4.2. Equipos de interconexión y conmutación de red
   4.2.1. Repetidores, concentradores, puentes, conmutadores y encaminadores
   4.2.2. Pasarelas y puntos de acceso inalámbricos

5. **Redes de comunicaciones**
   5.1. Clasificación por cobertura geográfica: PAN, LAN, MAN y WAN
   5.2. Topologías de red físicas y lógicas

6. **Redes de conmutación y redes de difusión**
   6.1. Redes de conmutación
   6.1.1. Conmutación de circuitos, de mensajes y de paquetes
   6.2. Redes de difusión
   6.2.1. Principios de difusión, direcciones broadcast y multicast

7. **Redes e infraestructuras inalámbricas**
   7.1. Redes de área personal y local inalámbricas
   7.2. Redes de área metropolitana y extensa inalámbricas

8. **Comunicaciones móviles**
   8.1. Evolución y arquitectura de redes celulares móviles
   8.2. Tecnologías consolidadas y de alta capacidad

9. **Seguridad y normativa en la Administración Pública**
   9.1. Aspectos de seguridad e integridad en redes inalámbricas
   9.2. Marco normativo y regulatorio de telecomunicaciones en el ámbito público

---

## Conceptos clave para memorizar

| Concepto | Dato clave |
|---|---|
| Telecomunicación (definición legal) | *«Toda transmisión, emisión o recepción de signos, señales, escritos, imágenes, sonidos o informaciones de cualquier naturaleza por hilo, radioelectricidad, medios ópticos u otros sistemas electromagnéticos»* — anexo II, apartado **79**, de la Ley 11/2022. Es la definición que hay que poder reproducir |
| Elementos del modelo de Shannon | **Cinco**: fuente → transmisor → **canal** (donde entra el ruido) → receptor → destino. El **ruido** ataca al canal, no al mensaje |
| Perturbaciones del canal | **Atenuación** (pérdida de potencia con la distancia) · **distorsión** (deformación de la señal, típicamente por retardo diferencial) · **ruido** (energía ajena añadida: térmico, de intermodulación, **diafonía** y **impulsivo**) · **interferencia** · **eco**. El ruido **térmico** es inevitable; el **impulsivo** es el más dañino en transmisión digital |
| Ancho de banda vs velocidad | **Ancho de banda** = rango de frecuencias, en **hercios (Hz)**. **Velocidad de transmisión** = bits por segundo (**bps**). **Velocidad de modulación** = símbolos por segundo (**baudios**). **Baudio ≠ bit/s**: solo coinciden si cada símbolo lleva **un** bit |
| Nyquist y Shannon | **Nyquist** (canal sin ruido): `C = 2·B·log₂(M)`. **Shannon** (canal con ruido): `C = B·log₂(1 + S/N)`. Shannon fija el **límite absoluto**; ningún esquema de modulación lo supera |
| Muestreo | **Teorema del muestreo**: `fm ≥ 2·fmax`. La telefonía digital muestrea la voz (300-3.400 Hz) a **8.000 muestras/s** con **8 bits** → **64 kbps**, que es el **canal E0** de la MIC/PCM |
| Módem, códec y adaptador | **Módem** = analógico ↔ digital sobre el medio (modula y demodula). **Códec** = digital ↔ analógico de la fuente (codifica y decodifica). Son operaciones **inversas**, no sinónimos |
| Medios guiados | **Par trenzado** (UTP/FTP/STP, categorías 5e a 8, conector **RJ-45**, **100 m** máximo en Ethernet) · **Coaxial** (malla apantallada, 50 Ω o 75 Ω) · **Fibra óptica** (inmune a interferencias electromagnéticas, sin diafonía, gran ancho de banda) |
| Fibra monomodo vs multimodo | **Multimodo** (**OM1-OM5**, núcleo 50 o 62,5 µm, LED o VCSEL, **distancias cortas**, más barata). **Monomodo** (**OS1/OS2**, núcleo ≈ 9 µm, láser, **decenas o centenares de kilómetros**). A mayor núcleo, más **dispersión modal** y menos alcance |
| Espectro radioeléctrico (definición legal) | *«Ondas electromagnéticas, cuya frecuencia se fija convencionalmente por debajo de 3.000 GHz, que se propagan por el espacio sin guía artificial»* — anexo II.21 de la Ley 11/2022. Es **bien de dominio público**, de titularidad y administración **estatal** (art. 85.1) |
| Bandas de la UIT | VLF, LF, **MF** (ondas medias), **HF** (onda corta, propagación ionosférica), **VHF** (30-300 MHz), **UHF** (300 MHz-3 GHz), **SHF** (3-30 GHz, microondas y satélite), EHF (30-300 GHz, ondas milimétricas). Cada banda decádica multiplica por diez la anterior |
| Regla física clave | **A más frecuencia**: más ancho de banda disponible y más capacidad, pero **menos alcance** y **peor penetración** en obstáculos. Explica por qué el 5G de 700 MHz da cobertura y el de 26 GHz da capacidad |
| Parámetros de calidad | **Ancho de banda** · **latencia** (retardo) · **fluctuación o *jitter*** (variación de la latencia) · **tasa de error de bit (BER)** · **relación señal-ruido (S/N, en dB)** · **atenuación (dB/km)** · **pérdida de paquetes**. El **decibelio** es **logarítmico**: 3 dB ≈ el doble de potencia; 10 dB = diez veces |
| Direccionalidad | **Símplex** (un solo sentido: radiodifusión, TDT) · **semidúplex** o *half-duplex* (los dos sentidos, **alternando**: walkie-talkie, **TETRA**) · **dúplex** o *full-duplex* (los dos sentidos **a la vez**: telefonía, Ethernet conmutado) |
| Síncrona vs asíncrona | **Asíncrona**: carácter a carácter, con **bit de arranque y de parada**, sin reloj común → sobrecarga de **≈ 20-30 %**, barata. **Síncrona**: bloques o tramas con **sincronismo de reloj** y delimitadores, mucho más eficiente en volumen |
| Serie vs paralelo | **Serie**: un bit detrás de otro por un único canal. **Paralelo**: varios bits a la vez por hilos distintos. A alta velocidad **gana el serie**, porque el paralelo sufre **desviación temporal (*skew*) y diafonía**. Por eso PCI Express, SATA, USB y Ethernet son **serie** |
| Equipos terminales (ETD/ETCD) | **ETD (DTE)**: origen o destino de los datos (ordenador, terminal). **ETCD (DCE)**: adapta la señal al medio y suele aportar el reloj (módem, ONT, adaptador de terminal). El límite entre ambos es el **punto de terminación de red** |
| Dispositivos por capa | **Capa 1**: repetidor, concentrador (*hub*), **transceptor**. **Capa 2**: puente, **conmutador (*switch*)**, punto de acceso inalámbrico. **Capa 3**: **encaminador (*router*)**, conmutador de capa 3. **Capas superiores**: **pasarela (*gateway*)**, cortafuegos de aplicación |
| Concentrador vs conmutador | El **concentrador** repite por todos los puertos: **un solo dominio de colisión**, medio compartido, semidúplex. El **conmutador** reenvía **solo al puerto destino** según la tabla MAC: **un dominio de colisión por puerto** y dúplex. **El conmutador NO divide el dominio de difusión**; eso solo lo hacen el **encaminador** o las **VLAN** |
| Dominios de colisión y de difusión | **Repetidor/hub**: 1 dominio de colisión, 1 de difusión. **Switch**: N dominios de colisión (uno por puerto), 1 de difusión. **Router**: N dominios de colisión y **N dominios de difusión** |
| Redes por cobertura | **PAN** (metros: Bluetooth, NFC, Zigbee) · **LAN** (edificio o recinto) · **CAN** (campus) · **MAN** (área metropolitana) · **WAN** (país o continente). Añadidos modernos: **BAN** (corporal), **SAN** (almacenamiento) y **WLAN/WPAN/WMAN/WWAN** para sus versiones inalámbricas |
| Topologías | **Bus** (troncal común, terminadores) · **anillo** (testigo, doble anillo en FDDI) · **estrella** (nodo central; **la más usada en LAN**) · **árbol** (estrella jerárquica) · **malla** (redundante; completa = **n(n−1)/2** enlaces) · **mixta**. Distinguir **topología física** (cableado) de **topología lógica** (recorrido de la señal): Ethernet moderno es **estrella física** con lógica de **bus conmutado** |
| Conmutación de circuitos | Reserva un **camino físico dedicado** durante toda la comunicación. Tres fases: **establecimiento, transferencia y liberación**. Retardo constante, sin fluctuación, pero **desaprovecha** la capacidad en los silencios. Ejemplo canónico: la **RTC** |
| Conmutación de paquetes | Divide en **paquetes** que se encaminan de forma independiente y compiten por el enlace: **multiplexación estadística**, aprovechamiento máximo, pero **fluctuación** y posible pérdida. Dos variantes: **datagrama** (sin conexión, cada paquete decide su ruta, pueden desordenarse) y **circuito virtual** (ruta fijada al inicio, orden garantizado; X.25, Frame Relay, ATM, MPLS) |
| Conmutación de mensajes | **Almacenamiento y reenvío** del mensaje **completo**, sin fragmentar, sin camino reservado. Retardos altos y necesidad de mucha memoria en los nodos: **hoy en desuso** como técnica de red, sobrevive en la lógica del correo electrónico |
| Difusión y multidifusión | **Unidifusión** (uno a uno) · **multidifusión** (uno a un grupo suscrito) · **difusión** (uno a todos) · **anydifusión** (al más cercano del grupo, propia de **IPv6**). **IPv6 no tiene broadcast**: lo sustituye por multidifusión a `ff02::1` |
| Direcciones de difusión | MAC de difusión: **FF:FF:FF:FF:FF:FF**. IPv4 limitada: **255.255.255.255** (no se encamina). Multidifusión IPv4: **224.0.0.0/4** (clase D), con MAC **01:00:5E:…**. Protocolo de suscripción: **IGMP** en IPv4 y **MLD** en IPv6 |
| Tormenta de difusión | Exceso de tráfico de difusión que satura el dominio; se agrava con **bucles de nivel 2** porque la trama Ethernet **no tiene TTL**. Remedios: **STP/RSTP**, **VLAN** para acotar el dominio y control de tormentas en el conmutador |
| Wi-Fi: generaciones | **Wi-Fi 4** = 802.11n · **Wi-Fi 5** = 802.11ac · **Wi-Fi 6** = 802.11ax · **Wi-Fi 6E** = 802.11ax en **6 GHz** · **Wi-Fi 7** = **802.11be**, publicado el **22 de julio de 2025** (canales de **320 MHz**, **4096-QAM** y **operación multienlace, MLO**) · **Wi-Fi 8** = 802.11bn, previsto para **2028** |
| Wi-Fi: modos y elementos | **BSS** (una celda con su punto de acceso) · **ESS** (varias celdas con el mismo **SSID**) · **modo *ad hoc*/IBSS** (sin punto de acceso). Acceso al medio: **CSMA/CA** (no CSMA/CD: en radio no se puede detectar la colisión mientras se transmite) |
| Otras redes inalámbricas | **Bluetooth** (WPAN, 2,4 GHz, piconet de 1 maestro y hasta 7 esclavos activos) · **NFC** (13,56 MHz, **≈ 10 cm**) · **Zigbee** (802.15.4, malla, domótica) · **LoRaWAN y NB-IoT** (LPWAN: poco caudal, mucho alcance, años de batería) · **WiMAX** (802.16, WMAN, hoy residual) |
| Satélite | **GEO** (35.786 km, fijo respecto a la Tierra, **≈ 250 ms** de ida y vuelta) · **MEO** (2.000-35.786 km; GPS y Galileo) · **LEO** (300-2.000 km, latencia baja, exige **constelaciones**). Bandas **C, Ku, Ka** |
| Generaciones móviles | **1G** analógica (TACS) · **2G GSM** digital, conmutación de circuitos, **SMS**, **SIM**; **GPRS (2.5G)** y **EDGE** añaden paquetes · **3G UMTS** (WCDMA), **HSPA** · **4G LTE**, **todo IP y solo paquetes**, voz por **VoLTE** · **5G NR** (eMBB, URLLC, mMTC) |
| Célula y reutilización | La red **celular** divide el territorio en celdas con **reutilización de frecuencias**: celdas no adyacentes repiten canal. El **traspaso (*handover*)** mantiene la llamada al cambiar de celda; el **itinerancia (*roaming*)** permite usar la red de otro operador |
| 5G: las tres familias de uso | **eMBB** (banda ancha móvil mejorada) · **URLLC** (comunicaciones ultrafiables de baja latencia) · **mMTC** (comunicaciones masivas entre máquinas). Habilitadores: **MIMO masivo**, **haces (*beamforming*)**, ***network slicing*** y **computación en el borde (MEC)** |
| Espectro 5G en España | Tres bandas prioritarias: **700 MHz** (cobertura; liberada por el **segundo dividendo digital**, RD **391/2019**, migración de la TDT completada el **31-10-2020**) · **3,5 GHz** (banda de capacidad y cobertura equilibradas) · **26 GHz** (ondas milimétricas, subastada en **2022**). La banda **470-694 MHz** queda para TDT **al menos hasta 2030** |
| Seguridad inalámbrica | **WEP** (RC4, roto: **no usar**) · **WPA** (TKIP, transitorio) · **WPA2** (**AES-CCMP**, 802.11i) · **WPA3** (**SAE**, sustituye al PSK; **192 bits** en modo Enterprise; **OWE** para redes abiertas). Empresarial: **802.1X + EAP + RADIUS**, autenticación por usuario y no por clave compartida |
| Wi-Fi en el ENS | **`mp.com.4.2`**: si se emplean comunicaciones inalámbricas, será **en un segmento separado**. **`mp.com.2`** (confidencialidad, dimensión **C**) y **`mp.com.3`** (integridad y autenticidad, dimensión **IA**) exigen **VPN cifrada** fuera del dominio propio y, desde nivel MEDIO, **algoritmos autorizados por el CCN** |
| Marco legal español | **Ley 11/2022, de 28 de junio, General de Telecomunicaciones**: 8 títulos, 114 artículos y 3 anexos. Las telecomunicaciones son **servicios de interés general en libre competencia** (art. 2.1); **solo** son servicio público los del **art. 4** (seguridad nacional, defensa, seguridad pública, seguridad vial y protección civil) |
| Servicio universal | Art. **37**: acceso adecuado a **internet de banda ancha en ubicación fija** con velocidad mínima de **10 Mbit/s** en sentido descendente, escalable por real decreto a **30 Mbit/s**, más **comunicaciones vocales**. El **anexo III** lista los **once** servicios que debe soportar |
| Administraciones públicas y redes | Art. **13**: cuando una Administración instala y explota redes públicas debe respetar el **principio de inversor privado**, con **separación de cuentas**, neutralidad, transparencia, no distorsión de la competencia y no discriminación. Excepción con **fallo de mercado** declarado: la **TDT en zonas sin cobertura** |
| Reguladores | **CNMC** (regulación *ex ante* de mercados, resolución de conflictos, supervisión de precios del servicio universal) · **Ministerio** competente en telecomunicaciones (espectro, inspección, incidentes del art. 63) · **UIT** en el plano internacional · **CEPT/ECC** y **RSPG** en el europeo |
