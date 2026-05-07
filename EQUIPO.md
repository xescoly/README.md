# Especificaciones y Operación del Equipo Certificador
Para la ejecución de las pruebas de campo, se utilizó el certificador **Platinum Tools NetChaser**, equipado con el módulo **TMA050-NC**. Este equipo permite validar la capacidad de transporte de datos y la integridad física del cableado estructurado.
## conozcamos al equipo desde 0 
<img width="397" height="559" alt="image" src="https://github.com/user-attachments/assets/5f519b67-3409-4938-8c1e-8181485bcc07" />


# 1. Resumen de Conectores (Interfaz del Equipo)
El equipo cuenta con varios puntos de conexión clave para las distintas tareas:

Conector RJ45 (Superior): Es el conector principal para las pruebas de cables de red Ethernet y pruebas de red activa. 

Conector F (Superior): Situado junto al RJ45, se utiliza para las pruebas en cables coaxiales. 

Puerto Micro USB: Ubicado en el lateral, sirve para conectar el equipo a la PC y transferir archivos o actualizar el firmware. 

Ranura para tarjeta SD: Justo debajo del USB, para guardar los reportes de las pruebas.

Cargador de CC: Enchufe para conectar la fuente de alimentación y cargar la batería.

# funciones de cada conector 

2. Tipos de Prueba que puedes realizar
   El Net Chaser es bien completo y te permite hacer tres grupos grandes de pruebas: 

A. Pruebas de Cable (Certificación y Continuidad)

•	Certificación de Velocidad: Certifica cables de cobre hasta 1 Gb/s. 

•	Prueba de Tasa de Error de Bits (BERT): Envía paquetes de datos a velocidades definidas para detectar errores al máximo rendimiento.

•	Relación Señal/Ruido (SNR): Mide la calidad de la señal para asegurar que aguante altas velocidades. 

•	Asimetría (Skew): Informa sobre el retardo de tiempo entre pares. 

•	Continuidad y Mapa de Cableado: Detecta si el cable está abierto, en corto, con hilos cruzados, pares divididos o invertidos. 

•	Distancia a la Falla (TDR): Mide con precisión el largo del cable y te dice a qué distancia está el drama (falla).


## Configuración de la Prueba
Antes de iniciar las mediciones, se procedió con la configuración de los parámetros en el equipo:
* **Módulo de Prueba:** TMA050-NC.
* **Tipo de Cable:** Par trenzado sin blindaje (UTP).
* **Categoría:** Cat 5e.
* **Estándar de Red:** IEEE 802.3ab (1000Base-T) para certificar transmisiones Gigabit.
<img width="341" height="496" alt="image" src="https://github.com/user-attachments/assets/e17f2fcc-49e2-45e5-a823-0726859f7aff" />

# 1. Cable Test (Prueba de Cable)
Esta función está diseñada para realizar el diagnóstico físico y la certificación de la infraestructura de cableado de cobre.

Certificación de Velocidad: Determina si el cable es capaz de soportar transmisiones de hasta 1 Gb/s mediante la medición de parámetros como la relación señal-ruido (SNR) y el retraso de propagación (Skew).

Mapa de Cableado: Identifica la continuidad de los hilos, detectando errores de terminación como pares divididos, cruzados o en cortocircuito.

Localización de Fallas (TDR): Utiliza reflectometría de dominio de tiempo para medir la longitud del cable y precisar la distancia exacta a una discontinuidad o falla.

# 2. Link Test (Prueba de Enlace)
Esta sección permite verificar la capacidad de comunicación entre el equipo de medición y los dispositivos activos de la red (switches o routers).

Negociación de Enlace: Identifica la velocidad de conexión (10/100/1000 Mbps) y el modo de transmisión (Half o Full Dúplex).

Verificación de PoE: Analiza la presencia de alimentación a través de Ethernet, identificando el estándar (802.3 af/at/bt), el voltaje y la carga disponible en los pares correspondientes.

Identificación de Puerto: Incluye la función de parpadeo de LED (Link Light) para localizar físicamente la conexión en un panel de parcheo o switch.

# 3. Network Test (Prueba de Red)
Conjunto de herramientas para validar la conectividad lógica y la configuración de los servicios de red una vez establecido el enlace físico.

Protocolos de Diagnóstico: Realiza pruebas de Ping para verificar la latencia y pérdida de paquetes, y Traceroute para identificar la ruta hacia un host.

Gestión de Direccionamiento: Comprueba la disponibilidad y respuesta de servidores DHCP para la asignación de direcciones IP.

Descubrimiento de Red: Identifica parámetros críticos como la VLAN configurada en el puerto y reconoce dispositivos mediante protocolos CDP o LLDP.

# 4. System Settings (Configuración del Sistema)
Módulo dedicado a la gestión interna del dispositivo y la personalización de sus parámetros de operación.

Parámetros Operativos: Permite configurar la dirección IP del equipo, el idioma de la interfaz, la fecha/hora y la gestión de energía (tiempos de espera).

Mantenimiento: Proporciona información sobre la versión de firmware instalada y permite realizar actualizaciones para asegurar la compatibilidad con nuevos estándares.

# 5. File Manager (Administrador de Archivos)
Herramienta de gestión de datos para la organización y almacenamiento de los resultados obtenidos durante las pruebas.

Almacenamiento de Reportes: Permite visualizar, organizar o eliminar los registros de certificación guardados en la memoria interna o tarjeta SD.

Documentación: Facilita la exportación de resultados para la generación de informes técnicos que validen la conformidad de la instalación ante el cliente final.

 ## 2. Funciones Avanzadas Utilizadas
De acuerdo con los requerimientos solicitados, se emplearon las siguientes herramientas del equipo:
* **Calibración a Cero (Set Reference):** Antes de iniciar la jornada de pruebas, se realiza una calibración del equipo utilizando los latiguillos de referencia. Esto permite descontar la resistencia y atenuación de los propios cables de prueba, garantizando que los resultados reflejen únicamente el estado del enlace permanente.
* **TDR (Time Domain Reflectometer):** Se utilizó para determinar la longitud exacta de cada par de hilos y localizar la distancia precisa de cualquier anomalía física o discontinuidad.
* **Prueba de BERT (Bit Error Rate Test):** Se realizó una prueba de tasa de error de bits para certificar la calidad del enlace, asegurando que el cableado soporte el tráfico real a 1 Gbps sin pérdida de información.
* **Verificación de SNR (Signal-to-Noise Ratio):** Se midió la relación señal-ruido en cada par para garantizar que las interferencias externas no afecten la estabilidad de la red.

[Net_Chaser_Manual-12_8_15 (2).pdf] (https://github.com/user-attachments/files/27239622/Net_Chaser_Manual-12_8_15.2.pdf)

 [Net_Chaser_Manual-12_8_15.2 conv.docx](https://github.com/user-attachments/files/27239976/Net_Chaser_Manual-12_8_15.2.conv.docx)
