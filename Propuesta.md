# Generador de funciones

**Autores:** Pollero Johann; Rivarola Ignacio; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026


## 1. Selección del proyecto a implementar

### 1.1 Objetivo del proyecto y resultados esperados
El objetivo de este proyecto es implementar un generador de funciones. Se busca que el prototipo permita seleccionar el tipo de forma las cuáles serán tres tipos: senoidal, cuadrada y triangulares. Se busca que el usuario pueda configurar los parámetros de la señal: frecuencia, amplitud, duty-cycle y off-set, a través entradas analógicas. Además tendrá una intefaz visual que permitirá mostrar la forma de la señal configurada.
Se espera que el prototipo permita generar señales de prueba para analizar la respuesta de un circuito ante señales alternas.

### 1.2 Proyectos similares
En base al objetivo se proponen posibles alternativas de implementación y se ponderan los aspectos a tener en cuenta para seleccionar el más adecuado.

### 1.3 Selección de proyecto
[ pendiente ]

## 2. Elicitación de requisitos y casos de uso
[ pendiente ]


- Hardware obligatorio:
  -  Dip Switchs, Buttons, Leds, Buzzer, módulo HM-10 (para usar App vía Bluetooth).
  -  Memoria E2PROM externa o Flash interna (almacenamiento del SET_UP)
  -  Sensores analógicos (temperatura, joystick, etc.)
  -  Para la interconexión de placas/módulos/conectores/componentes/etc.:
      -  No usar protoboard ni cables Dupont
      -  Usar una placa base, opciones:
          - Circuito impreso diseñado y fabricado al efecto
          -  Placa experimental con componentes y conectores soldados e interconexión de componentes/conectores mediante cables soldados (alambres telefónico o wire wrap soldado)


- Hardware adicional:
  - A consensuar con los docentes responsables en función de las necesidad de cada trabajo


- Programación obligatorio:
  -  Bare Metal (sin Sistema Operativo), del tipo Event-Triggered System
  -  Estructurada/Modular (Escrutar/Procesar/Actuar), nada de código Spaguetti
  -  Patrones de software:
      -  Ejecutor cíclico, Super-Loop (polling & interrupts) => 1 vuelta < 1mS
      -  Tick = 1mS (Systick => Callback)
      -  Tareas de código no bloqueante, ya sea temporizada o no temporizada
      -  Modelos - Diagramas de Estado - c/Interfaces (colas, estructuras, array de estructuras)
      -  Menú Interactivo
      -  Bajo Consumo
      -  Al menos dos modos de operación (NORMAL, SET_UP, FALLA, ...)
      -  Periféricos con comunicación SPI y/o I2C
      -  Periféricos gestionados por Polling (siempre que no sea código bloqueante), Interrupts o DMA (=> Callbacks), por ejemplo acelerómetro, gps, humedad, temperatura, presión, ...


- Programación adicional:
  - A consensuar con los docentes responsables en función de las necesidad de cada trabajo
