# Generador de funciones

**Autores:** Pollero Johann; Rivarola Ignacio; Villegas Wanda

**Padrón:** 108752; 112199; 113805

**Fecha:** 2do cuatrimestre 2026


## 1. Selección del proyecto a implementar

### 1.1 Objetivo del proyecto y resultados esperados
El objetivo de este proyecto es implementar un generador de funciones. Se busca que el prototipo permita seleccionar el tipo de forma las cuáles serán tres tipos: senoidal, cuadrada y triangulares. Se busca que el usuario pueda configurar los parámetros de la señal: frecuencia, amplitud, duty-cycle y off-set, a través entradas analógicas. Además tendrá una intefaz visual que permitirá mostrar la forma de la señal configurada.
Se espera que el prototipo permita generar señales de prueba para analizar la respuesta de un circuito ante señales alternas.

### 1.2 Proyectos similares
En base al objetivo se proponen estas posibles alternativas de implementación del generador de funciones, que se diferencian principalmente en sus capacidades. Para seleccionar la alternativa más adecuada, se ponderan los aspectos de criterio de cada alternativa.

1. **Generador Básico:** Control mediante entradas analógicas con capacidad de comunicación Bluetooth (HM-10) para visualización/control desde una App en dispositivo, y uso de memoria (E2PROM/Flash) para almacenar el SET_UP del usuario.
2. **Generador Básico + Pantalla LCD + Bluetooth + Memoria:** Sistema de generación de señales con control manual (encoders/potenciómetros) que incluye una pantalla LCD para visualizar la configuración aplicada a la onda, pero sin conectividad externa ni guardado en memoria no volátil.
3. **Generador Básico + Pantalla OLED + Bluetooth + Memoria:** Sistema de generación de señales con control manual (encoders/potenciómetros) que incluye una pantalla OLED para visualizar la onda configurada con sus parámetros, pero sin conectividad externa ni guardado en memoria no volátil.


Para comparar estas alternativas, se tienen en cuenta cinco aspectos característicos, los cuales se ponderan del 1 al 10:
1.  **Disponibilidad del hardware (9):** Se evalúa si el proyecto puede implementarse utilizando hardware fácilmente adquirible en el mercado local.
2.  **Impacto en el proyecto (8):** Se pondera cuánto aporta a la funcionalidad moderna y al cumplimiento de la consigna de la materia.
3.  **Costo (8):** Se evalúa el costo total del hardware requerido para cada opción.
4.  **Viabilidad (10):** Se contempla el tiempo requerido y la complejidad de implementación (firmware y hardware).
5.  **Interés personal del equipo (7):** Se pondera la motivación e interés del equipo en implementar cada alternativa.

La siguiente tabla (Tabla 1) muestra los valores ponderados asignados a cada proyecto considerado:

<table>
    <thead>
        <tr>
            <th rowspan="2">Criterio</th>
            <th colspan="2">1. Analógico Básico</th>
            <th colspan="2">2. Básico + Pantalla LCD</th>
            <th colspan="2">3. Bluetooth + Memoria</th>
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
[ pendiente ]

## 2. Elicitación de requisitos y casos de uso
[ pendiente ]
