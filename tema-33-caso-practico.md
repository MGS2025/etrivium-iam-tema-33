# Tema 33 — Casos Prácticos

> **Título oficial**: Comunicaciones. Medios de transmisión. Modos de comunicación. Equipos terminales y equipos de interconexión y conmutación. Redes de comunicaciones. Redes de conmutación y redes de difusión. Comunicaciones móviles e inalámbricas.
>
> **Formato**: 3 casos prácticos sobre supuestos reales del Ayuntamiento de Madrid. Cada caso suma **10 puntos**.
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

Los tres casos recorren el supuesto de referencia del tema (ver tema-33-contenido.md, «Convenciones»): la **red de comunicaciones que conecta una Oficina de Atención a la Ciudadanía de un distrito con el centro de proceso de datos del IAM**. El **Caso 1** trabaja los **medios de transmisión, los modos y los parámetros de calidad**; el **Caso 2**, los **equipos de interconexión, las topologías y la difusión**; y el **Caso 3**, el **despliegue inalámbrico y móvil** y su encaje en el **marco normativo y de seguridad**.

---

## Caso 1 — Medios de transmisión, modos y calidad del enlace de una oficina de distrito

### Enunciado

El IAM va a reformar la **Oficina de Atención a la Ciudadanía** de un distrito y debe rediseñar sus comunicaciones. Datos del supuesto:

- El edificio tiene **tres plantas**. En cada planta hay un armario de comunicaciones y el puesto más alejado está a **78 metros** de cable desde su armario.
- En la planta baja hay **40 puestos de trabajo**, **12 teléfonos IP**, **6 cámaras de videovigilancia IP**, **4 pantallas de gestión de turnos** y **una impresora multifunción**.
- Los armarios de las tres plantas deben unirse entre sí; la distancia vertical entre el armario de la planta baja y el de la segunda es de **60 metros** de recorrido de cable, atravesando dos cuadros eléctricos distintos.
- El edificio debe conectarse con el **centro de proceso de datos del IAM**, situado a **6 kilómetros**.
- Existe además una **caseta de control** en el patio trasero, a **300 metros**, sin canalización disponible, con presupuesto y plazo muy ajustados y con visión directa despejada desde la azotea.
- La aplicación de tramitación exige un caudal modesto, pero se va a implantar **telefonía IP** y **videoconferencia** con las juntas de distrito.

### Cuestiones

**Cuestión 1 — Elección de medios (3 puntos).** Indique y **justifique** el medio de transmisión adecuado para cada uno de los cuatro tramos: horizontal de planta, vertical entre armarios, acometida al CPD y caseta del patio.

**Cuestión 2 — Datos numéricos y límites (2 puntos).** Para el tramo horizontal, indique la **categoría** mínima de cable, la **longitud máxima** normalizada del enlace y su desglose, y qué norma de **alimentación por Ethernet** hace falta para los teléfonos, las cámaras y las pantallas.

**Cuestión 3 — Modos de comunicación (2 puntos).** Clasifique según los **tres criterios** de modo de comunicación (direccionalidad, sincronismo y forma de transmisión): (a) el enlace Ethernet de un puesto de trabajo; (b) el enlace de la caseta del patio; (c) la megafonía de avisos de la sala de espera.

**Cuestión 4 — Parámetros de calidad (3 puntos).** Redacte los **cinco parámetros** que debe recoger el acuerdo de nivel de servicio del circuito contratado al operador para el enlace con el CPD, indicando **unidad** y **por qué** importa cada uno para los servicios previstos. Explique además por qué el caudal real medido en el Wi-Fi de la oficina será muy inferior al anunciado.

### Solución orientativa

- **C1**: (§2.1.1, §2.2.1, §2.3)

| Tramo | Medio propuesto | Justificación |
|---|---|---|
| **Horizontal de planta** | **Par trenzado Cat 6A (F/UTP o U/FTP)** | Los 78 m están dentro del límite de 100 m; coste bajo por punto; y sobre todo **permite PoE**, que es imprescindible para teléfonos, cámaras y pantallas. La fibra al puesto sería técnicamente válida pero dejaría a esos terminales **sin alimentación** y multiplicaría el coste |
| **Vertical entre armarios** | **Fibra óptica multimodo OM4** | 60 m está dentro del alcance de la multimodo; y hay una razón adicional decisiva: al atravesar **dos cuadros eléctricos distintos** interesa el **aislamiento galvánico** que da un medio dieléctrico, que evita transportar diferencias de potencial y sobretensiones entre plantas |
| **Acometida al CPD (6 km)** | **Fibra monomodo OS2**, normalmente en forma de **circuito contratado a un operador** | El cobre queda descartado por atenuación (tres órdenes de magnitud fuera del límite); la multimodo también, por dispersión modal. A 6 km por vía pública lo realista es contratar el circuito, porque el trazado atraviesa **dominio público** |
| **Caseta del patio (300 m)** | **Radioenlace de microondas punto a punto**, o Wi-Fi exterior direccional en banda de uso común | Es la respuesta correcta **precisamente porque no hay canalización**: abrir zanja tiene un coste y un plazo incomparablemente mayores. Condiciones que hay que declarar: exige **visión directa** —que el enunciado confirma— y, por ser medio compartido, obliga a **cifrar el enlace** |

  Conviene añadir la observación general: **la elección del medio no la decide la velocidad, sino la distancia, la necesidad de alimentación y quién es el titular del suelo por el que discurre el cable**.

- **C2**: (§2.1.1)
  - **Categoría mínima: Cat 6A**, con 500 MHz de ancho de banda. Se justifica no por la necesidad actual —1 Gbit/s basta— sino porque es la que garantiza **10GBASE-T a los 100 m completos**, y el cableado horizontal es el elemento de la instalación con **vida útil más larga** (15-20 años) y el más caro de sustituir. La Cat 6 solo da 10 Gbit/s hasta unos 55 m, y la Cat 8 está limitada a 30 m y es de centro de datos.
  - **Longitud máxima del enlace: 100 m**, desglosados en **90 m de cable horizontal fijo** (del armario a la roseta) **más 10 m** repartidos entre los latiguillos de ambos extremos. Los 78 m del enunciado dejan margen suficiente. Hay que advertir de que superar el límite **no produce un fallo limpio**, sino errores intermitentes muy difíciles de diagnosticar.
  - **Alimentación por Ethernet**: los teléfonos IP y las pantallas se cubren con **802.3af (PoE, 15,4 W)**; las **cámaras** con motorización, calefactor o iluminación infrarroja requieren **802.3at (PoE+, 30 W)**. Si se previera algún punto de acceso Wi-Fi 6E/7 de gama alta o un domo con más consumo, habría que dimensionar **802.3bt**. Consecuencia de diseño que conviene señalar: **el conmutador pasa a ser también un equipo eléctrico crítico**, y debe dimensionarse su presupuesto de potencia PoE y respaldarse con SAI.

- **C3**: (§3.1, §3.2, §3.3)

| Enlace | Direccionalidad | Sincronismo | Forma |
|---|---|---|---|
| **(a) Ethernet del puesto** | **Dúplex**, porque hay pares separados de transmisión y recepción y el equipo del otro extremo es un **conmutador** (con un concentrador sería semidúplex) | **Síncrona**: trama con preámbulo y reloj extraído de la señal por codificación de línea | **Serie** |
| **(b) Radioenlace de la caseta** | **Semidúplex** si es Wi-Fi exterior (una radio no puede escuchar mientras transmite); un radioenlace de microondas profesional puede ser **dúplex** por **FDD**, con una banda por sentido | **Síncrona** | **Serie** |
| **(c) Megafonía de avisos** | **Símplex**: un solo sentido y sin canal de retorno | Analógica en su versión clásica; **síncrona** si es megafonía sobre IP | Serie |

  La conclusión que se espera es que **los tres criterios son independientes y se combinan**: casi todo lo moderno es **síncrono y serie**, y lo que de verdad varía de un enlace a otro es la **direccionalidad**.

- **C4**: (§2.3)

| Parámetro | Unidad | Por qué importa aquí |
|---|---|---|
| **Caudal garantizado** | Mbit/s | Debe cubrir la tramitación, la telefonía IP y la videoconferencia simultáneas; conviene que sea **garantizado**, no «hasta» |
| **Latencia máxima** | ms | La videoconferencia con las juntas de distrito deja de ser natural por encima de unos 150 ms de extremo a extremo |
| **Fluctuación (*jitter*) máxima** | ms | **Es el parámetro crítico para la voz**: la variación del retardo produce cortes y voz metálica, mientras que una latencia alta pero estable se tolera |
| **Pérdida de paquetes** | % | Degrada la voz y el vídeo de forma inmediata y muy visible |
| **Disponibilidad y tiempo de resolución** | % y horas | Una oficina de atención presencial sin red **no puede atender**: hay que fijar disponibilidad, ventana de servicio y plazo máximo de reparación |

  Cabe añadir, con buen criterio, **la exigencia de cifrado del circuito**, que en un sistema sujeto al ENS deriva de `mp.com.2` y `mp.com.3`, y la **notificación de incidentes** por parte del operador.

  **Por qué el caudal real del Wi-Fi es muy inferior al anunciado**: porque el medio radio es **compartido y semidúplex**, la capacidad se reparte entre todos los clientes activos, cada trama debe **confirmarse con un ACK**, el mecanismo **CSMA/CA** consume tiempo en escuchas y esperas aleatorias, y a ello se suman las cabeceras de todos los protocolos. Un caudal real en torno a **la mitad o menos** de la velocidad nominal **no es una avería**: es el funcionamiento normal, y conviene decírselo así a quien reclama.

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Los cuatro medios correctamente elegidos **y justificados por distancia, alimentación y titularidad del suelo** | 3 |
| Categoría 6A, límite de 100 m con desglose 90 + 10 y normas PoE correctas | 2 |
| Clasificación correcta en los tres criterios, señalando que son independientes | 2 |
| Cinco parámetros con su unidad y su justificación funcional | 2 |
| Explicación correcta de la diferencia entre caudal real y nominal en Wi-Fi | 1 |

---

## Caso 2 — Equipos de interconexión, topología y una tormenta de difusión

### Enunciado

La red de la Oficina de Atención a la Ciudadanía se encuentra, tras años de crecimiento sin plan, en el siguiente estado:

- Un **encaminador de frontera** con **3 interfaces activas** conecta con el CPD del IAM.
- De la primera interfaz cuelga un **conmutador de 24 puertos** con 24 equipos, **sin VLAN**.
- De la segunda cuelga un **concentrador antiguo de 8 puertos** que sobrevive en el archivo, con 8 equipos.
- De la tercera cuelga un **conmutador de 12 puertos** en el que se han configurado **3 VLAN**.
- Toda la red comparte **un mismo espacio de direccionamiento** salvo en el último conmutador.
- Un lunes por la mañana, un técnico conecta **un latiguillo entre dos puertos libres del conmutador de 24 puertos** por error. En pocos segundos, **toda la red de la oficina deja de funcionar**, incluidos los equipos que no estaban comunicándose con nadie. La actividad de la interfaz del encaminador se dispara al 100 %.

### Cuestiones

**Cuestión 1 — Recuento de dominios (2 puntos).** Calcule cuántos **dominios de colisión** y cuántos **dominios de difusión** hay en la red descrita, detallando el razonamiento.

**Cuestión 2 — Diagnóstico del incidente (3 puntos).** Explique **qué ha ocurrido** el lunes por la mañana, **por qué** un solo latiguillo puede tumbar toda la red y por qué el mismo error en la capa 3 no tendría ese efecto de forma indefinida.

**Cuestión 3 — Remedios (2 puntos).** Proponga **tres medidas** de distinta naturaleza para que el incidente no se repita, indicando en qué equipo se aplica cada una.

**Cuestión 4 — Rediseño (3 puntos).** Proponga el rediseño de la red indicando: **topología** objetivo y por qué; qué hacer con el **concentrador**; y qué **equipo de interconexión** resuelve cada una de estas tres necesidades: (a) separar el tráfico de las cámaras del de los puestos de trabajo, (b) llegar al CPD y (c) integrar un sistema de control de accesos que habla un protocolo propietario no IP.

### Solución orientativa

- **C1**: (§4.2.1)

  **Dominios de colisión.** Cada puerto activo de un conmutador es un dominio; el concentrador entero es **uno solo**, porque no segmenta.
  - Conmutador de 24 puertos: **24** puertos con equipo **+ 1** puerto de subida al encaminador = **25**.
  - Concentrador: **1** (los 8 equipos y el enlace al encaminador comparten el medio).
  - Conmutador de 12 puertos: **12 + 1** = **13**.
  - **Total: 25 + 1 + 13 = 39 dominios de colisión.**

  **Dominios de difusión.** Uno por interfaz de encaminador, salvo que haya VLAN, que multiplican.
  - Interfaz 1 (conmutador plano, sin VLAN): **1**.
  - Interfaz 2 (concentrador): **1**.
  - Interfaz 3 (conmutador con 3 VLAN): **3**.
  - **Total: 5 dominios de difusión.**

  La lectura que se espera: el **concentrador es un desastre en colisiones** pero indiferente en difusión; el **conmutador arregla lo primero y no toca lo segundo**; y solo las **VLAN** y el **encaminador** actúan sobre la difusión.

- **C2**: (§4.2.1, §6.2.1)
  - **Qué ha ocurrido**: el latiguillo ha creado un **bucle de nivel 2** en el conmutador de 24 puertos, y con él una **tormenta de difusión**.
  - **Por qué tumba toda la red**: una única trama de difusión —basta una petición ARP o un DHCP— entra en el bucle y **se multiplica en cada vuelta**, porque el conmutador la inunda por todos los puertos menos el de entrada. La causa técnica de que no se detenga es que **la trama Ethernet no tiene campo TTL**. En segundos el enlace se satura, y como **toda la interfaz 1 es un único dominio de difusión**, la avalancha alcanza a los 24 equipos, que además **procesan cada trama en su CPU**. De ahí que caigan también los equipos que no estaban comunicándose: no es que su tráfico no pase, es que **su procesador está ocupado descartando difusión**.
  - **Por qué en capa 3 no ocurre lo mismo**: el paquete **IP sí tiene TTL**, que el encaminador **decrementa** en cada salto y descarta al llegar a cero. Un bucle de encaminamiento produce paquetes perdidos y rutas subóptimas, pero **no una multiplicación indefinida**.
  - Conviene señalar que el incidente **no fue una avería del equipo ni un ataque**: fue un error de operación que la arquitectura de red **permitía** que fuese catastrófico. Ese es el fallo de fondo.

- **C3**: (§4.2.1, §6.2.1) Tres medidas de naturaleza distinta:
  1. **Activar STP o, preferiblemente, RSTP** en todos los conmutadores. Es el remedio directo: detecta el camino redundante y **bloquea lógicamente** uno de los enlaces, reactivándolo automáticamente si falla el principal. Se aplica en **los conmutadores**.
  2. **Segmentar en VLAN** toda la red, no solo el último conmutador. No evita el bucle, pero **acota el dominio de difusión** y, con él, el alcance del desastre: la tormenta quedaría confinada a una VLAN en lugar de tumbar la oficina entera. Se aplica en **los conmutadores** y exige encaminamiento entre VLAN.
  3. **Control de tormentas por puerto** (*storm control*), que limita el porcentaje de tráfico de difusión y multidifusión admitido y desactiva el puerto al superarlo. Se aplica en **los conmutadores**, puerto a puerto.
  - Como medidas complementarias de buena práctica: **protección de puerto de acceso** frente a la aparición de tramas de gestión de STP donde no debe haberlas, **desactivar administrativamente los puertos no usados** y etiquetar el patchado.

- **C4**: (§4.2, §5.2)
  - **Topología objetivo: árbol (estrella jerárquica)**, con conmutadores de **acceso** en cada planta que suben a un **conmutador de capa 3** de edificio, y este al **encaminador de frontera**. Es la topología adecuada porque (a) el fallo de un enlace o de un puesto **solo afecta a ese puesto**; (b) el diagnóstico es sencillo, al concentrarse la gestión; y (c) escala añadiendo ramas. Su punto débil conocido es el **nodo superior**, que se mitiga con equipo redundante o al menos con repuesto y configuración guardada. Hacia el CPD conviene mantener el **doble camino** —fibra y radioenlace—, que introduce una **malla parcial mínima** de dos enlaces y responde al riesgo real de corte de fibra por obra en la vía pública.
  - **Qué hacer con el concentrador: retirarlo**, sin matices. Es un equipo de **capa 1** que (a) mantiene ocho equipos en **un único dominio de colisión** compartiendo el ancho de banda, (b) obliga a **semidúplex** y (c) —lo más grave— permite que **cualquier equipo conectado vea el tráfico de todos los demás** poniendo su interfaz en modo promiscuo, lo que es incompatible con la confidencialidad exigible a un sistema municipal. Se sustituye por un conmutador gestionable.
  - **Equipo para cada necesidad**:

| Necesidad | Equipo | Por qué |
|---|---|---|
| **(a)** Separar el tráfico de las cámaras del de los puestos | **Conmutador gestionable con VLAN**, y encaminamiento entre VLAN en el **conmutador de capa 3** | Cada VLAN es un **dominio de difusión** distinto; el aislamiento entre ellas exige pasar por capa 3, donde se aplica la política de acceso |
| **(b)** Llegar al CPD del IAM | **Encaminador de frontera** (capa 3) | Une **redes distintas**, decide la ruta por dirección IP, detiene la difusión y aporta las funciones de frontera (calidad de servicio, listas de acceso, terminación del circuito) |
| **(c)** Integrar el control de accesos con protocolo propietario no IP | **Pasarela (*gateway*)** | Es el único equipo que, operando en **capas superiores**, **traduce entre arquitecturas o protocolos distintos**. Ni un conmutador ni un encaminador pueden hacerlo: no entienden ese protocolo |

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Recuento correcto de los 39 dominios de colisión y los 5 de difusión, con razonamiento | 2 |
| Diagnóstico del bucle y la tormenta, **citando la ausencia de TTL en la trama Ethernet** | 2 |
| Explicación de por qué caen equipos que no se comunicaban (procesamiento de la difusión en la CPU) | 1 |
| Tres remedios de naturaleza distinta, correctamente ubicados en el equipo | 2 |
| Topología en árbol justificada y retirada razonada del concentrador | 1,5 |
| Los tres equipos correctos, especialmente la **pasarela** para el protocolo propietario | 1,5 |

---

## Caso 3 — Despliegue inalámbrico y móvil, seguridad y marco normativo

### Enunciado

El distrito quiere completar la reforma con cuatro actuaciones:

1. **Wi-Fi corporativo** en las tres plantas del edificio, para los puestos móviles, las tabletas de los inspectores y los teléfonos de voz sobre wifi del personal de atención.
2. **Wi-Fi de cortesía para la ciudadanía** en la sala de espera y, en una segunda fase, **en las tres plazas públicas del distrito**.
3. **Sensores** de ocupación de aparcamiento, llenado de contenedores y calidad del aire repartidos por el distrito, incluidos algunos en sótanos y arquetas.
4. Un **radioenlace propio** en banda licenciada entre el edificio de la oficina y un polideportivo municipal cercano.

El sistema de tramitación al que se accede desde esa red está categorizado en el ENS como de **categoría MEDIA**, con confidencialidad MEDIO e integridad y autenticidad ALTO.

### Cuestiones

**Cuestión 1 — Diseño inalámbrico interior (3 puntos).** Proponga el diseño del Wi-Fi del edificio: número y finalidad de los SSID, mecanismo de autenticación y cifrado de cada uno, y segmentación. Justifique cada decisión citando la **medida del ENS** aplicable.

**Cuestión 2 — Medidas ineficaces (1 punto).** El responsable del edificio propone «ocultar el SSID y permitir solo las direcciones MAC de los equipos municipales». Valore la propuesta.

**Cuestión 3 — Tecnología para los sensores (2 puntos).** Elija la tecnología de comunicación para los sensores del distrito y **justifique** la elección, valorando expresamente los sensores situados en sótanos y arquetas. Indique la disyuntiva de fondo que hay que resolver.

**Cuestión 4 — Encaje normativo (4 puntos).** Analice el régimen jurídico de las cuatro actuaciones: (a) el Wi-Fi corporativo, (b) el Wi-Fi de cortesía en la sala de espera y en las plazas públicas, (c) los sensores y (d) el radioenlace en banda licenciada. Cite los preceptos de la **Ley 11/2022** aplicables.

### Solución orientativa

- **C1**: (§7.1, §9.1) Diseño de **tres SSID sobre los mismos puntos de acceso**, cada uno en su propia VLAN:

| SSID | Finalidad | Autenticación y cifrado | Segmentación |
|---|---|---|---|
| **Corporativo** | Puestos móviles, tabletas y teléfonos del personal | **WPA3-Enterprise** con **802.1X / EAP-TLS** contra el directorio municipal | VLAN de usuarios, con acceso a los servicios internos según perfil |
| **Dispositivos** | Impresoras, pantallas de turnos, sensores de edificio | WPA3-Personal con clave larga y rotada, o **certificado de dispositivo** donde sea posible | VLAN propia, **sin acceso** a la red de servicios y con listas de control de acceso estrictas |
| **Cortesía** | Público de la sala de espera | Red abierta con **OWE** (*Wi-Fi Enhanced Open*), portal cautivo y aislamiento entre clientes | VLAN **totalmente aislada**, con **salida directa a internet** y ninguna ruta hacia la red municipal |

  **Justificación normativa**, que es lo que se valora:
  - **`mp.com.4.2`** del anexo II del ENS: *«si se emplean comunicaciones inalámbricas, será en un segmento separado»*. Es el respaldo directo de la decisión de VLAN independiente para todo lo inalámbrico.
  - **`mp.com.4` con refuerzo R1**: al ser el sistema de **categoría MEDIA**, la medida aplica con `+[R1 o R2 o R3]`. El **R1** implementa los segmentos mediante **VLAN**, con un mínimo de tres subredes: **usuarios, servicios y administración**. El diseño propuesto lo cumple y lo supera.
  - **`mp.com.2`** (confidencialidad, nivel **MEDIO** en este sistema): VPN cifrada cuando la comunicación salga del dominio propio, **más el refuerzo R1**, algoritmos y parámetros **autorizados por el CCN**.
  - **`mp.com.3`** (integridad y autenticidad, nivel **ALTO**): exige `+R1+R2+R3+R4`, el nivel de exigencia más alto de las tres medidas en este sistema, precisamente porque la autenticidad del acto administrativo es lo que está en juego.
  - **`mp.com.1`**: perímetro seguro, aplicable en las **tres categorías**; todo el tráfico debe atravesarlo y los flujos deben estar previamente autorizados.
  - **Trazabilidad**: la elección de **802.1X con credencial individual** frente a una clave compartida no es una preferencia técnica, sino un **requisito de imputabilidad**: con clave precompartida no se puede saber quién hizo qué, y además revocar a una persona obliga a cambiar la clave a toda la organización.
  - Se espera además la advertencia final: **el enlace radio es una capa más**. Los servicios municipales deben ir sobre **TLS** de extremo a extremo por encima de él, en aplicación del principio de **defensa en profundidad**.
  - Elementos complementarios que suman: **802.11r** para que la itinerancia no corte las llamadas de voz sobre wifi, **802.11w** para neutralizar los ataques de desautenticación, **desactivar WPS**, planificar canales y potencias —emitir con más potencia de la necesaria amplía la superficie de exposición sin mejorar el servicio— y **detección continua de puntos de acceso no autorizados** desde el controlador.

- **C2**: (§9.1) La propuesta **debe rechazarse**, y no por exceso de celo sino porque **ninguna de las dos medidas aporta seguridad real**:
  - **Ocultar el SSID** no lo oculta: el nombre de la red **viaja en claro** en las tramas de asociación de cualquier cliente que se conecte, de modo que basta con esperar. Y además complica la operación y genera incidencias de conexión.
  - **Filtrar por dirección MAC** no filtra: las direcciones MAC circulan **en claro** en todas las tramas y **se clonan trivialmente**; el atacante solo tiene que copiar una autorizada.
  - Lo relevante es el argumento de fondo: **son medidas cosméticas que dan una falsa sensación de protección**, que es lo peor que puede hacer una medida de seguridad, porque desplaza la atención de lo que sí protege —**cifrado robusto (WPA3) y autenticación por usuario (802.1X)**—. Cabe aceptarlas como complemento cosmético, nunca como sustituto.

- **C3**: (§7.2)
  - **Elección: NB-IoT** (tecnología **3GPP** sobre espectro licenciado del operador) para los sensores en **sótanos y arquetas**, y **LoRaWAN** admisible para los sensores en superficie si se opta por red propia.
  - **Justificación**: los sensores son el caso de uso canónico de **LPWAN** —muy pocos datos, muy de vez en cuando, mucho alcance y años de batería—, y por tanto quedan descartados tanto el **Wi-Fi** (alcance insuficiente y consumo incompatible con años de pila) como una red celular convencional. Entre las LPWAN, el criterio decisivo lo da el enunciado: **los sensores de sótano y arqueta** exigen la **penetración en interiores profundos** que caracteriza a **NB-IoT**, que además se beneficia de la cobertura del operador ya desplegada. En 5G, este tipo de tráfico corresponde a la familia **mMTC** (comunicaciones masivas entre máquinas).
  - **La disyuntiva de fondo que hay que enunciar**: **espectro sin licencia frente a espectro licenciado**. **LoRaWAN** permite al Ayuntamiento **desplegar red propia** sin depender de un operador ni pagar por dispositivo, pero **sin garantía de calidad ni de ausencia de interferencias** y asumiendo la operación de las pasarelas. **NB-IoT** ofrece cobertura y calidad **garantizadas por contrato**, pero el servicio —y la dependencia— son del operador. Una respuesta completa señala que **la decisión no es técnica sino de modelo de servicio**, y que cabe una solución mixta.

- **C4**: (§9.2)

| Actuación | Régimen aplicable |
|---|---|
| **(a) Wi-Fi corporativo** | Banda **ISM de uso común**: basta con respetar las condiciones técnicas y los límites de potencia; **no hace falta título habilitante individual** ni se devenga tasa por reserva. Y como es una **red privada de usuario final** —el Ayuntamiento no la ofrece al público—, **no entra en el art. 13** de la Ley 11/2022 |
| **(b) Wi-Fi de cortesía** | Aquí **sí aparece el art. 13**, porque se estaría prestando un servicio **disponible al público**. Hay que valorar el **principio de inversor privado**, la **separación de cuentas** y los principios de **neutralidad, transparencia, no distorsión de la competencia y no discriminación**, además de la normativa de **ayudas de Estado** (arts. 107 y 108 del TFUE), y en su caso la comunicación al **Registro de operadores**. La respuesta completa distingue los dos supuestos del enunciado: en la **sala de espera** el servicio es claramente **accesorio** a la atención presencial y de escaso riesgo competitivo; en **tres plazas públicas** el análisis es más exigente, y lo prudente es delimitar el servicio (caudal y usos acotados, sin sustituir a la oferta comercial), **documentar esa delimitación** y recabar informe jurídico. Se añaden las obligaciones de **protección de datos** del portal cautivo |
| **(c) Sensores** | Si se opta por **LoRaWAN**, banda de **uso común**: mismo régimen que (a), sin título individual. Si se opta por **NB-IoT**, el Ayuntamiento actúa como **cliente de un operador**, sin obligaciones de espectro propias. En ninguno de los dos casos hay prestación de servicio al público |
| **(d) Radioenlace en banda licenciada** | **Uso privativo del dominio público radioeléctrico**: exige **título habilitante** —autorización individual o concesión, según la banda— otorgado por el **Ministerio** competente, y devenga **tasa por reserva del dominio público radioeléctrico** (título V y título VII de la Ley 11/2022). Fundamento: el art. **85.1** declara que el espectro es **bien de dominio público**, cuya **titularidad y administración corresponden al Estado** |

  Conviene cerrar con la observación transversal: en las cuatro actuaciones el Ayuntamiento sigue siendo **responsable del cumplimiento del ENS** sobre sus sistemas, mientras que las obligaciones de **integridad y seguridad de las redes** del **art. 63** —incluida la notificación de incidentes de impacto significativo— pesan sobre **los operadores** que le prestan servicio. Esa exigencia debe trasladarse **por contrato**.

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Tres SSID con su autenticación, cifrado y segmentación correctos | 1,5 |
| Cita correcta de `mp.com.4.2` y del refuerzo R1 aplicable a categoría MEDIA | 1 |
| Justificación de 802.1X por **trazabilidad**, no por preferencia técnica | 0,5 |
| Rechazo razonado de ocultar el SSID y del filtrado MAC | 1 |
| Elección de LPWAN con justificación de la penetración en sótanos y enunciado de la disyuntiva licenciado/no licenciado | 2 |
| Régimen de uso común frente a uso privativo, con cita del art. 85 y de la tasa | 1,5 |
| Aplicación correcta del **art. 13** al wifi de cortesía, distinguiendo sala de espera y plazas públicas | 2 |
| Observación final sobre el reparto de responsabilidades ENS / art. 63 y su traslado contractual | 0,5 |
