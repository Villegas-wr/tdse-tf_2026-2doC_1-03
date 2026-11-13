<img width="332" height="116" alt="image" src="https://github.com/user-attachments/assets/4d37edb0-dd1e-4d64-8be6-1043f9219c48" />

# Generador de funciones

**Autores:** Pollero Johann; Rivarola Ignacio; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026


## 1. Selección del proyecto a implementar

### 1.1 Objetivo del proyecto y resultados esperados
El objetivo de este proyecto es implementar un generador de funciones. Se busca que el prototipo permita seleccionar el tipo de forma las cuáles serán las típicas (senoidal, cuadrada y triangulares) y otras de carácter mas customizado (entre ellas, exponencial periódica, pulsos, sumatoria de senoidales, ruido gaussiano, senoidales rectificadas y senoidales rectificadas total). Se busca que el usuario pueda configurar los parámetros de la señal: frecuencia, amplitud, duty-cycle y off-set, a través entradas analógicas. Además tendrá una interfaz visual que permitirá mostrar la forma de la señal configurada.
Se espera que el prototipo permita generar señales de prueba para analizar la respuesta de un circuito ante señales alternas.

### 1.2 Proyectos similares
En base al objetivo se proponen estas posibles alternativas de implementación del generador de funciones, que se diferencian principalmente en sus capacidades. Para seleccionar la alternativa más adecuada, se ponderan los aspectos de criterio de cada alternativa.

1. **Generador Básico:** Generador de señales controlado exclusivamente mediante potenciómetros analógicos, sin capacidad de almacenamiento ni conectividad.
2. **Generador Básico + Pantalla LCD + Bluetooth + Memoria:** Sistema de generación de señales con control manual (encoders/potenciómetros) que incluye una pantalla LCD para visualizar la configuración aplicada a la onda, con conectividad externa y guardado en memoria no volátil.
3. **Generador Básico + Pantalla OLED + Bluetooth + Memoria:** Sistema de generación de señales con control manual (encoders/potenciómetros) que incluye una pantalla OLED para visualizar la onda medida y con sus parámetros, con conectividad externa y guardado en memoria no volátil.


Para comparar estas alternativas, se tienen en cuenta cinco aspectos característicos, los cuales se ponderan del 1 al 10:
1.  **Disponibilidad del hardware (9):** Se evalúa si el proyecto puede implementarse utilizando hardware fácilmente adquirible en el mercado local.
2.  **Impacto en el proyecto (8):** Se pondera cuánto aporta a la funcionalidad moderna y al cumplimiento de la consigna de la materia.
3.  **Costo (8):** Se evalúa el costo total del hardware requerido para cada opción.
4.  **Viabilidad (10):** Se contempla el tiempo requerido y la complejidad de implementación (firmware y hardware).
5.  **Interés personal del equipo (7):** Se pondera la motivación e interés del equipo en implementar cada alternativa.

La siguiente tabla (Tabla 1) muestra los valores ponderados asignados a cada proyecto considerado.

<table>
    <thead>
        <tr>
            <th rowspan="2">Criterio</th>
            <th colspan="2">Generador Básico</th>
            <th colspan="2">Generador Básico + Pantalla LCD + Bluetooth + Memoria</th>
            <th colspan="2">Generador Básico + Pantalla OLED + Bluetooth + Memoria</th>
        </tr>
        <tr>
            <th>Puntaje</th>
            <th>Puntaje Ponderado</th>
            <th>Puntaje</th>
            <th>Puntaje Ponderado</th>
            <th>Puntaje</th>
            <th>Puntaje Ponderado</th>
        </tr>
    </thead>
    <tbody>
        <tr class="header-row">
            <td align="center">Disponibilidad de Hardware <br>(peso: 9)</td>
            <td>10</td>
            <td>90</td>
            <td>9</td>
            <td>81</td>
            <td>10</td>
            <td>90</td>
        </tr>
        <tr>
            <td align="center">Impacto en el proyecto <br>(peso: 8)</td>
            <td>4</td>
            <td>32</td>
            <td>6</td>
            <td>48</td>
            <td>10</td>
            <td>80</td>
        </tr>
        <tr class="header-row">
            <td align="center">Costo (peso: 8)</td>
            <td>10</td>
            <td>80</td>
            <td>7</td>
            <td>56</td>
            <td>8</td>
            <td>64</td>
        </tr>
        <tr>
            <td align="center">Dificultad técnica / Viabilidad <br>(peso: 10)</td>
            <td>10</td>
            <td>100</td>
            <td>8</td>
            <td>80</td>
            <td>8</td>
            <td>80</td>
        </tr>
        <tr class="header-row">
            <td align="center">Interés personal <br>(peso: 7)</td>
            <td>4</td>
            <td>28</td>
            <td>6</td>
            <td>42</td>
            <td>9</td>
            <td>63</td>
        </tr>
        <tr class="highlight-green">
            <td><strong>Puntaje Total</strong></td>
            <td>-</td>
            <td>330</td>
            <td>-</td>
            <td>307</td>
            <td>-</td>
            <td class="highlight-red"><strong>377</strong></td>
        </tr>
    </tbody>
</table>
<p align="center"><em>Tabla 1: Comparación de alternativas de proyecto</em></p>

  
### 1.3 Selección de proyecto
A partir del análisis realizado en la sección 1.2, se selecciona la 3ra Alternativa (Generador Básico + Pantalla OLED + Bluetooth + Memoria), la cual obtuvo la calificación ponderada más alta.

Esta elección se justifica debido las siguientes razones:
  * Mayor Impacto y Experiencia de Usuario: La pantalla OLED permite representar de forma gráfica y nítida la forma de onda sintética generada, sus parámetros numéricos exactos y la navegación de menús intuitivos, mejorando drásticamente el valor didáctico y funcional del prototipo respecto a pantallas numéricas o alfanuméricas tradicionales.
  * Conectividad y Almacenamiento: El módulo Bluetooth HM-10 posibilita el control remoto y la telemetría desde dispositivos móviles (App), mientras que la memoria no volátil (E2PROM/Flash) garantiza la persistencia de las configuraciones de onda (SET_UP) tras un reinicio del sistema.
  * Factibilidad y Disponibilidad (90/90 pts en HW, 80/80 en Viabilidad): Los componentes requeridos (pantalla OLED I2C/SPI, módulo HM-10, potenciómetros y memoria) son de alta disponibilidad local y su integración dentro de la arquitectura Event-Triggered es técnicamente viable en el plazo del cuatrimestre.

En la figura 1.3.1, se presenta el diagrama en bloques, planteando de forma gráfico las características del prototipo del generador de funciones en relación con el microcontrolador. 

<img width="900" height="508" alt="image" src="https://github.com/user-attachments/assets/6731b34b-8d30-4484-aa2d-e5c0c033136c" />
<p align="center"><em>Figura 1.3.1: Diagrama en bloques del sistema</em></p>

A continuación se detallan los módulos del diagrama:

1. **Núcleo de Procesamiento (Microcontrolador)**
   * **Función:** Actúa como el elemento central del prototipo. Ejecuta la arquitectura de firmware no bloqueante (Event-Triggered / Ejecutor Cíclico) supervisada por el SysTick ($1\text{ ms}$). Gestiona los estados del sistema (ej. NORMAL, SET_UP, FALLA), la máquina de estados finitos (FSM) y coordina el tráfico entre todos los periféricos mediante interrupciones, polling eficiente o DMA.
2. **Subsistema de Entradas**
   * **Potenciómetros (ADC):** Conectados a canales del conversor analógico-digital del microcontrolador. Permiten digitalizar valores analógicos continuos para modificar variables del sistema en tiempo real.
   * **Botones (GPIO):** Entradas digitales discretas configuradas con resistencia de pull-up/pull-down interna o externa. Se emplean para la navegación en el menú interactivo, la selección de opciones y el cambio manual de estados.
3. **Subsistema de Señalización y Salidas Discretas**
   * **LED (GPIO):** Salida digital que proporciona señalización visual inmediata respecto al estado lógico interno del sistema.
   * **Buzzer (GPIO):** Transductor piezoeléctrico accionado por salida digital (o señal PWM) para generar tonos de notificación, confirmación de eventos o alarmas sonoras.
4. **Subsistema de Interfaz Gráfica y Salida Analógica**
   * **Pantalla OLED (SPI / I²C):** Periférico de salida de alta resolución para la representación visual del menú interactivo, estado de conexión Bluetooth y lecturas de sensores. La elección del bus SPI o I²C depende del compromiso entre velocidad de refresco y consumo de pines GPIO.
   * **DAC Externo (SPI):** Convertidor Digital-Analógico dedicado fuera del chip del microcontrolador. Comunicado por un bus SPI de alta velocidad, se encarga de reconstruir waveforms o señales analógicas a partir de los datos procesados digitalmente por el MCU.
5. **Subsistema de Almacenamiento y Comunicaciones**
   * **Memoria Externa (SPI / I²C):** Módulo EEPROM o Flash no volátil externa. Permite guardar las señales customizadas, garantizando que la configuración persista tras un reinicio o corte de energía.
   * **Módulo de Bluetooth (UART):** Módulo de transmisión inalámbrica (ej. HM-10 / BLE) conectado a la interfaz UART del microcontrolador (pines TX/RX). Facilita el intercambio bidireccional de tramas de datos entre la aplicación móvil de control y el firmware.

## 2. Elicitación de requisitos y casos de uso
### 2.1 Requisitos del sistema
En la tabla 2 se detallan los requisitos del sistema clasificándolos en las categorías de "Hardware" y "Software"
<table>
  <thead>
    <tr>
      <th>Categoría</th>
      <th>Descripción del Requisito</th>
      <th>Estado / Detalle</th>
      <th>Tipo de Requisito</th>
    </tr>
  </thead>
  <tbody>
    <!-- HARDWARE -->
    <tr>
      <td rowspan="7"><b>Hardware</b></td>
      <td>Entradas analógicas</td>
      <td>Potenciómetros conectados a canales ADC para ajustar Frecuencia, Amplitud, Duty-Cycle y Offset.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Botones / Dip-Switches</td>
      <td>Pulsadores para selección de forma de onda, navegación por menú y switches de selección de modo.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Módulo Bluetooth HM-10</td>
      <td>Enlace serie UART inalámbrico para interacción con aplicación móvil externa.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Memoria No Volátil</td>
      <td>Almacenamiento permanente de configuraciones (SET_UP) mediante E2PROM externa (I2C/SPI) o Flash interna del STM32.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Indicadores locales</td>
      <td>LEDs de estado operativo y Buzzer para alertas sonoras del sistema.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Interconexión / Placa Base</td>
      <td><b>Sin protoboard ni cables Dupont.</b> Montaje definitivo sobre placa base soldada (PCB o placa experimental con conexiones soldadas).</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Pantalla OLED</td>
      <td>Display OLED (I2C o SPI) para visualización en tiempo real de la forma de onda, valores numéricos y menú interactivo.</td>
      <td>Adicional</td>
    </tr>
    <!-- Software -->
    <tr>
      <td rowspan="12"><b>Software</b></td>
      <td>Arquitectura Bare Metal</td>
      <td>Programación sin Sistema Operativo (RTOS) basada en arquitectura <i>Event-Triggered System</i>.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Estructura Modular</td>
      <td>Organización del firmware bajo el esquema <b>Escrutar / Procesar / Actuar</b>, evitando código desestructurado.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Ejecutor Cíclico (Super-Loop)</td>
      <td>Ciclo principal no bloqueante con tiempo por vuelta garantizado de $T_{\text{loop}} < 1\text{ ms}$.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Temporizador de Sistema (SysTick)</td>
      <td>Base de tiempo mediante <b>SysTick</b> de $1\text{ ms}$ asociando rutinas de interrupción (Callbacks).</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Tareas No Bloqueantes</td>
      <td>Prohibido el uso de retardos bloqueantes (<code>HAL_Delay</code> o bucles <code>while</code> de espera). Uso de temporización por conteo de Ticks.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Máquinas de Estado</td>
      <td>Modelado y diseño de comportamientos del sistema mediante <b>Itemis CREATE</b> e implementación modular en C.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Menú Interactivo</td>
      <td>Interfaz de navegación para configuración de parámetros y modos de uso.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Modos de Operación</td>
      <td>Al menos dos modos claramente definidos: <b>Modo NORMAL</b> (generación continua) y <b>Modo SET_UP</b> (configuración de parámetros), más modo <b>FALLA</b>.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Comunicación Periférica</td>
      <td>Uso de buses I2C, SPI y UART con gestión por Polling no bloqueante, Interrupciones o DMA.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Gestión de Bajo Consumo</td>
      <td>Implementación de modos de bajo consumo del MCU STM32 cuando el sistema permanezca inactivo.</td>
      <td>Obligatorio</td>
    </tr>
    <tr>
      <td>Síntesis Digital de Señales</td>
      <td>Algoritmo de generación de ondas Senoidal, Cuadrada y Triangular mediante tablas de consulta (LUT) y salida por DAC/PWM.</td>
      <td>Adicional</td>
    </tr>
    <tr>
      <td>Protocolo de Comandos BT</td>
      <td>Parser no bloqueante de tramas UART para procesar comandos recibidos desde la App Bluetooth.</td>
      <td>Adicional</td>
    </tr>
  </tbody>
</table>
<p align="center"><em>Tabla 2: Requisitos del sistema</em></p>

### 2.2 Casos de uso
A continuación se detallan los casos de uso principales que describen la interacción del usuario y la respuesta del sistema.

#### Caso 1: Configuración Manual y Generación de Onda
* **Nombre:** Configuración manual de forma de onda y parámetros analógicos.
* **Actor:** Usuario (Operador / Estudiante).
* **Precondiciones:** El generador de funciones se encuentra encendido en Modo NORMAL.
* **Flujo Principal:**
    1. El usuario presiona el botón de selección para alternar el tipo de onda (Senoidal, Cuadrada o Triangular).
    2. El sistema detecta la pulsación (filtrando rebotes en forma no bloqueante) y actualiza la tabla de búsqueda correspondiente.
    3. El usuario gira los potenciómetros analógicos para modificar la Frecuencia, Amplitud, Duty-Cycle u Offset.
    4. El canal ADC escruta en forma periódica los valores de tensión analógicos y los convierte en variables numéricas de configuración.
    5. El módulo de procesamiento recalcula el periodo del Timer / DMA o DAC para actualizar la señal de salida.
    6. La etapa de salida entrega la nueva forma de onda física en los bornes del prototipo.
* **Flujo Alternativo / Excepción:**
    * Si un parámetro configurado excede los límites seguros (x ej. frecuencia fuera de rango soportado), el sistema acota el valor al límite máximo permitido y activa una alerta breve en el Buzzer.
* **Postcondiciones:** El generador emite la señal configurada en tiempo real sin interrumpir la ejecución del Super-Loop.

#### Caso 2: Navegación de Menú y Visualización en Pantalla OLED
* **Nombre:** Visualización gráfica de la señal y menú interactivo en Pantalla OLED.
* **Actor:** Usuario.
* **Precondiciones:** La pantalla OLED está inicializada vía bus I2C/SPI y el sistema está activo.
* **Flujo Principal:**
    1. El usuario ingresa al Modo SET_UP mediante la combinación o pulsación prolongada del botón de menú.
    2. La pantalla OLED despliega el menú interactivo con las opciones: Tipo de Onda, Frecuencia, Amplitud, Duty-Cycle, Offset y Guardar Configuración.
    3. El usuario navega por las opciones utilizando los botones de incremento/decremento o un encoder rotativo.
    4. La pantalla refresca de forma no bloqueante (x ej. cadenciada cada 50ms) dibujando la vista previa del perfil de la onda sintética junto con los valores numéricos de los parámetros.
    5. El usuario confirma los valores y regresa al Modo NORMAL.
* **Postcondiciones:** La pantalla OLED muestra la representación gráfica actualizada de la señal que se está generando.

#### Caso 3: Control Remoto y Telemetría vía Bluetooth HM-10
* **Nombre:** Transmisión de parámetros y control mediante App Bluetooth.
* **Actor:** Usuario a través de Smartphone / Tablet.
* **Precondiciones:** El módulo HM-10 está emparejado inalámbricamente con la App en el dispositivo móvil.
* **Flujo Principal:**
    1. El usuario envía una trama de comandos desde la App (ejemplo: SET:WAVE=SINE,FREQ=1000).
    2. El periférico USART recibe los caracteres en buffer mediante interrupciones o DMA.
    3. La tarea no bloqueante de parseo procesa la trama completa, valida la suma de chequeo/sintaxis y extrae los nuevos parámetros.
    4. El sistema actualiza los registros de generación de señal sin detener el Super-Loop.
    5. El sistema responde transmitiendo por Bluetooth una trama de confirmación con la configuración insertada (siguiendo el ej. ACK:WAVE=SINE,FREQ=1000).
* **Flujo Alternativo / Excepción:**
    * Si la trama recibida está corrupta o incompleta, el sistema responde ERR:INVALID_COMMAND y mantiene los parámetros anteriores.
* **Postcondiciones:** La señal generada se actualiza remotamente y los nuevos parámetros se reflejan sincronizadamente en la pantalla OLED.

#### Caso 4: Almacenamiento y Recuperación de la Configuración en Memoria No Volátil
* **Nombre:** Guardado y restauración del perfil de usuario (SET_UP) en E2PROM / Flash.
* **Actor:** Usuario / Sistema.
* **Precondiciones:** El sistema cuenta con parámetros modificados en el Modo SET_UP.
* **Flujo Principal:**
    1. El usuario selecciona la opción "Guardar SET_UP" en el menú o el sistema ejecuta un único guardado automático tras 10 segundos de inactividad de ajustes.
    2. El firmware empaqueta la estructura de configuración (tipo de onda, frecuencia, amplitud, duty-cycle, offset) en un arreglo de bytes.
    3. Se inicia una escritura no bloqueante vía I2C/SPI en la memoria E2PROM externa (o por páginas en la Flash interna).
    4. El sistema confirma la escritura exitosa emitiendo un tono corto en el Buzzer y mostrando un mensaje en la pantalla OLED.
    5. Al reiniciar o encender el prototipo en el futuro, la rutina de Startup lee los bytes de la memoria y restaura automáticamente el último perfil guardado.
* **Postcondiciones:** Las configuraciones seleccionadas por el usuario permanecen guardadas entre ciclos de encendido del dispositivo.
