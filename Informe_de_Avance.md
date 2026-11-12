<img width="332" height="116" alt="image" src="https://github.com/user-attachments/assets/4d37edb0-dd1e-4d64-8be6-1043f9219c48" />

# Generador de funciones

**Autores:** Pollero Johann; Rivarola Ignacio; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026

## 1. Definición de Estados de Avance (Código de Colores)

De acuerdo con lo solicitado por la cátedra, se utiliza el siguiente código de colores para reflejar el estado real de implementación de cada requisito del proyecto:

* 🟢 **Verde:** El requisito <ins> se encuentra implementado </ins> en firmware/hardware, integrado y validado mediante pruebas funcionales.
* 🟡 **Amarillo:** El requisito <ins> se encuentra parcialmente desarrollado</ins>, en etapa de prototipado en protoboard/simulación o pendiente de validación/integración.
* 🔴 **Rojo:** El requisito <ins> no será implementado </ins>. 

---

## 2. Estado de Requisitos del Proyecto (WBS)

A continuación se detalla el desglose de requisitos funcionales y de hardware correspondientes a la alternativa seleccionada (*Generador Básico + Pantalla OLED + Bluetooth + Memoria*):

| Grupo | ID | Descripción del Requisito | Estado |
| :--- | :---: | :--- | :---: |
| **1. Generación de Señales** | 1.1 | El sistema deberá generar una señal de forma **senoidal**. | 🔴 Rojo |
| | 1.2 | El sistema deberá generar una señal de forma **cuadrada**. | 🔴 Rojo |
| | 1.3 | El sistema deberá generar una señal de forma **triangular**. | 🔴 Rojo |
| | 1.4 | El sistema deberá contar con una etapa analógica de acondicionamiento y salida de señal. | 🔴 Rojo |
| **2. Control de Parámetros** | 2.1 | El usuario podrá seleccionar el tipo de forma de onda a generar (senoidal, cuadrada, triangular). | 🔴 Rojo |
| | 2.2 | El usuario podrá configurar la **frecuencia** de la señal mediante entradas analógicas/controles físicos. | 🔴 Rojo |
| | 2.3 | El usuario podrá configurar la **amplitud** de la señal mediante entradas analógicas/controles físicos. | 🔴 Rojo |
| | 2.4 | El usuario podrá configurar el **duty-cycle** (ciclo de trabajo) de la señal. | 🔴 Rojo |
| | 2.5 | El usuario podrá configurar el **offset** (nivel de continua) de la señal. | 🔴 Rojo |
| **3. Interfaz Visual (OLED)** | 3.1 | El sistema contará con una pantalla OLED para mostrar los parámetros configurados (forma de onda, frecuencia, amplitud, duty-cycle y offset). | 🔴 Rojo |
| | 3.2 | La pantalla OLED graficará una representación visual de la forma de onda configurada. | 🔴 Rojo |
| **4. Conectividad Bluetooth** | 4.1 | El sistema contará con un módulo Bluetooth para establecer comunicación inalámbrica externa. | 🔴 Rojo |
| | 4.2 | El sistema permitirá recibir comandos de configuración de parámetros de forma remota vía Bluetooth. | 🔴 Rojo |
| | 4.3 | El sistema enviará el estado y los parámetros actuales de la señal al dispositivo conectado por Bluetooth. | 🔴 Rojo |
| **5. Almacenamiento (Memoria)** | 5.1 | El sistema contará con memoria no volátil para almacenar perfiles/configuraciones de usuario. | 🔴 Rojo |
| | 5.2 | El sistema permitirá guardar y recuperar configuraciones previas tras un reinicio o corte de energía. | 🔴 Rojo |

---

## 3. Situación Actual y Propuesta de Ajuste de Alcance

* **Estado general:** Al momento de la presente entrega, el equipo se encuentra en etapa de definición y adquisición de componentes, sin avance implementado en código ni hardware (**100% de los requisitos en estado 🔴 Rojo**).
* **Priorización y posible recorte de alcance:** Dado el cronograma restante de la cursada, en caso de requerir un ajuste de alcance junto con la cátedra, se propone priorizar el núcleo funcional del proyecto (Grupos **1**, **2** y **3.1**: generación de las tres formas de onda, control manual de parámetros y visualización numérica en pantalla OLED) y evaluar la simplificación o eventual recorte de los módulos secundarios (Grupo **4 - Bluetooth**, Grupo **5 - Memoria no volátil** y gráfico dinámico de onda en **3.2**).
