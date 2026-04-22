# Registro de Testeos y Resultados de Campo

En esta sección se documentan las pruebas de certificación realizadas en los puntos de red del laboratorio, utilizando el estándar **TIA** para categoría **Cat 5e**.

## 1. Tabla de Resultados (Paso 2 de la Práctica)
A continuación se detallan los valores obtenidos directamente del equipo certificador **NetChaser TNC950**:

| Punto de Red | Ubicación | Resultado (PASS/FAIL) | Longitud (m) | BERT (Errores) | SNR Promedio |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CABLE009** | PUNTO_21 | **PASS** | 19.2 m | 0 errores | 30.1 dB |
| **CABLE006** | PUNTO_19 | **PASS** | 18.9 m | 0 errores | 29.6 dB |
| **CABLE010** | PUNTO_18 | **FAIL** | 18.8 m | **FAIL** | 29.5 dB |

## 2. Análisis Técnico de Fallas (Paso 3)

* **Punto afectado:** CABLE010 (PUNTO_18).
* **Falla detectada:** El equipo arroja un fallo en la prueba de **BERT (Bit Error Rate Test)** y muestra una anomalía en el mapa de cableado.
* **Detalle del Wiremap:** Se observa una falta de continuidad física (circuito abierto) específicamente en el **hilo 5**.
* **Causa técnica probable:** La falla en el hilo 5 impide la correcta transmisión de la ráfaga de datos, lo que genera errores de bits. Esto suele ocurrir por un mal contacto en las cuchillas del Jack IDC o un conductor cortado durante el proceso de impacto.
* **Solución propuesta:** Se recomienda sanear el extremo del cable y re-conectorizar bajo la norma **T568B** para restablecer la continuidad del hilo 5.

## 3. Verificación de Capa Lógica
En los puntos con resultado **PASS** (PUNTO_21 y PUNTO_19), se utilizó la función de **Prueba de DHCP/Ping** de la certificadora para validar que, tras asegurar la integridad física, la red es capaz de asignar una dirección IP y responder a comandos de eco, garantizando la operatividad total del nodo.
