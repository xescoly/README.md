# Especificaciones y Operación del Equipo Certificador

Para la ejecución de las pruebas de campo, se utilizó el certificador **Platinum Tools NetChaser**, equipado con el módulo **TMA050-NC**. Este equipo permite validar la capacidad de transporte de datos y la integridad física del cableado estructurado.

## 1. Configuración de la Prueba
Antes de iniciar las mediciones, se procedió con la configuración de los parámetros en el equipo:
* **Módulo de Prueba:** TMA050-NC.
* **Tipo de Cable:** Par trenzado sin blindaje (UTP).
* **Categoría:** Cat 5e.
* **Estándar de Red:** IEEE 802.3ab (1000Base-T) para certificar transmisiones Gigabit.
 ## 2. Funciones Avanzadas Utilizadas
De acuerdo con los requerimientos solicitados, se emplearon las siguientes herramientas del equipo:

* **Calibración a Cero (Set Reference):** Antes de iniciar la jornada de pruebas, se realiza una calibración del equipo utilizando los latiguillos de referencia. Esto permite descontar la resistencia y atenuación de los propios cables de prueba, garantizando que los resultados reflejen únicamente el estado del enlace permanente.
* **TDR (Time Domain Reflectometer):** Se utilizó para determinar la longitud exacta de cada par de hilos y localizar la distancia precisa de cualquier anomalía física o discontinuidad.
* **Prueba de BERT (Bit Error Rate Test):** Se realizó una prueba de tasa de error de bits para certificar la calidad del enlace, asegurando que el cableado soporte el tráfico real a 1 Gbps sin pérdida de información.
* **Verificación de SNR (Signal-to-Noise Ratio):** Se midió la relación señal-ruido en cada par para garantizar que las interferencias externas no afecten la estabilidad de la red.
