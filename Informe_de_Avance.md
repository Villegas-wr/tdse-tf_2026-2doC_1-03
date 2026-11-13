<img width="332" height="116" alt="image" src="https://github.com/user-attachments/assets/4d37edb0-dd1e-4d64-8be6-1043f9219c48" />

# Generador de funciones

**Autores:** Pollero Johann; Rivarola Ignacio; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026

## 1. Definición de Estados de Avance (Código de Colores)

De acuerdo con lo solicitado por la cátedra, se utiliza el siguiente código de colores para reflejar el estado real de implementación de cada requisito del proyecto:

* 🟢 **Verde (Completado):** El requisito se encuentra implementado en firmware/hardware, integrado y validado mediante pruebas funcionales.
* 🟡 **Amarillo (En Progreso):** El requisito se encuentra parcialmente desarrollado, en etapa de prototipado en protoboard/simulación o pendiente de validación/integración.
* 🔴 **Rojo (No Iniciado):** El requisito aún no ha comenzado a desarrollarse.

## 2. Estado de Requisitos del Proyecto (WBS)

A continuación se detalla el desglose de requisitos funcionales y de hardware correspondientes a la alternativa seleccionada (*Generador Básico + Pantalla OLED + Bluetooth + Memoria*):

### 1. Generación de Señales

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 1.1 | El sistema deberá generar las señales básicas | 🔴 |
| 1.1.1 | Señal de forma senoidal. | 🔴 |
| 1.1.2 | Señal de forma cuadrada. | 🔴 |
| 1.1.3 | Señal de forma triangular. | 🔴 |
| 1.2 | El sistema deberá generar las señales especiales | 🔴 |
| 1.2.1 | Señal de forma exponencial periódica | 🔴 |
| 1.2.2 | Señal de forma pulsos | 🔴 |
| 1.2.3 | Señal de forma sumatoria de senoidales | 🔴 |
| 1.2.4 | Señal de forma ruido gaussiano | 🔴 |
| 1.2.5 | Señal de forma senoidal rectificada de media onda | 🔴 |
| 1.2.6 | Señal de forma senoidal rectificada de onda completa | 🔴 |

### 2. Tratamiento de la señal

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 2.1 | Configuración del DAC | 🔴 |
| 2.2 | Acondicionamiento de la señal | 🔴 |
| 2.2.1 | Filtrado | 🔴 |
| 2.2.2 | Offset default | 🔴 |
| 2.2.3 | Amplificación / Atenuación default | 🔴 |

### 3. Interfaz de Usuario y Controles

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 3.1 | Selección del tipo de forma de onda a generar | 🔴 |
| 3.2 | Configuración de frecuencia | 🔴 |
| 3.3 | Configuración de amplitud | 🔴 |
| 3.4 | Configuración de duty-cycle | 🔴 |
| 3.5 | Configuración de offset | 🔴 |

### 4. Interfaz Visual (OLED)

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 4.1 | Visualización de parámetros configurados (forma de onda, frecuencia, amplitud, duty-cycle y offset). | 🔴 |
| 4.2 | Visualización de señal configurada medida | 🔴 |

### 5. Conectividad Bluetooth

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 5.1 | Comunicación inalámbrica externa | 🔴 |
| 5.2 | Recibir comandos de configuración de parámetros | 🔴 |
| 5.3 | Visualización remota de la señal medida y parámetros | 🔴 |

### 6. Almacenamiento (Memoria externa)

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 6.1 | Guardado de señales customizadas/especiales | 🔴 |

### 7. Indicadores y alarmas

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 7.1 | Led indicador | 🔴 |
| 7.2 | Buzzer de alarma | 🔴 |

### 8. Botones

| Req ID | Descripción | Estado |
| :---: | :--- | :---: |
| 8.1 | Botón on/off | 🔴 |

---

## 3. Situación Actual y Propuesta de Ajuste de Alcance

* **Estado general:** Al momento de la presente entrega, el equipo se encuentra en etapa de definición y adquisición de componentes, sin avance implementado en código ni hardware (**100% de los requisitos en estado 🔴 Rojo**).
* **Priorización y posible recorte de alcance:** Dado el cronograma restante de la cursada, en caso de requerir un ajuste de alcance junto con la cátedra, se propone priorizar el núcleo funcional del proyecto (Grupos **1**, **2** y **3.1**: generación de las tres formas de onda, control manual de parámetros y visualización numérica en pantalla OLED) y evaluar la simplificación o eventual recorte de los módulos secundarios (Grupo **4 - Bluetooth**, Grupo **5 - Memoria no volátil** y gráfico dinámico de onda en **3.2**).
