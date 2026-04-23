# Registro de Testeos y Resultados de Campo

En esta sección se documentan las pruebas de certificación realizadas en los puntos de red del laboratorio, utilizando el estándar **TIA** para categoría **Cat 5e**.

## 1. Tabla de Resultados 
A continuación se detallan los valores obtenidos directamente del equipo certificador **NetChaser TNC950**:

| Punto de Red | Ubicación | Resultado (PASS/FAIL) | Longitud (m) | BERT (Errores) | SNR Promedio |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CABLE009** | PUNTO_21 | **PASS** | 19.2 m | 0 errores | 30.1 dB |
| **CABLE006** | PUNTO_19 | **PASS** | 18.9 m | 0 errores | 29.6 dB |
| **CABLE010** | PUNTO_18 | **FAIL** | 18.8 m | **FAIL** | 29.5 dB |

## 2. Análisis Técnico de Fallas 

### Análisis Detallado del Punto Crítico: CABLE010 (PUNTO_18)

* **Identificación del Problema:** El equipo reporta un fallo en el **hilo 5**, correspondiente al par central (Blanco/Azul) según la norma T568B.
* **Impacto en el Rendimiento:** Bajo el estándar **IEEE 802.3ab (1000Base-T)**, la transmisión Gigabit requiere obligatoriamente el uso de los **4 pares** de cobre de forma simultánea. 
* **Justificación Técnica:** La discontinuidad en el hilo 5 impide la formación del cuarto canal de datos, lo que provoca que el enlace no logre sincronizar a 1 Gbps, degradando la conexión a velocidades inferiores o causando la pérdida total de conectividad lógica (Capa 3), como se evidencia al no obtener IP por DHCP en este punto.
* **Causa Raíz Probable:** Falta de presión en la cuchilla del Jack IDC o un conductor cortado durante el proceso de impacto.


## 3. Verificación de Capa Lógica
En los puntos con resultado **PASS** (PUNTO_21 y PUNTO_19), se utilizó la función de **Prueba de DHCP/Ping** de la certificadora para validar que, tras asegurar la integridad física, la red es capaz de asignar una dirección IP y responder a comandos de eco, garantizando la operatividad total del nodo.
