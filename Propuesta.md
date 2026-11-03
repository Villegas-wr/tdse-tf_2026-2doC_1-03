# Generador de funciones

**Autores:** Pollero Johann; Rivarola Nacho; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026


## 1. Selección del proyecto a implementar

### 1.1 Objetivo del proyecto y resultados esperados
El objetivo de este proyecto es implementar un generador de funciones.
Con el prototipo se busca que permita seleccionar tres tipo de funciones disponibles: senoidal, cuadrada y triangulares, configurar la frecuencia de la señal, iniciar o detener la señal desde entradas analógicas. Además se utilizará un modo de guardado de configuración y señal en un dispositivo como computadora o celular mediante conexión a Bluetooth.  

### 1.2 Proyectos similares
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
