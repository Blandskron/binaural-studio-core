# Binaural Studio Core 🧠🎧

### High-Fidelity Audio Synthesis for Cognitive Optimization

**Binaural Studio Core** es un motor de síntesis de audio basado en el navegador que utiliza la **Web Audio API** para generar pulsos binaurales precisos. Este proyecto está diseñado con un enfoque de **Accesibilidad Cognitiva (UX)**, optimizado para usuarios neurodivergentes (TDAH, TEA) que buscan mejorar el enfoque, la relajación o la inducción al sueño mediante el arrastre de ondas cerebrales (*Brainwave Entrainment*).

-----

## 🔬 Fundamentos Científicos y Técnicos

### El Fenómeno Binaural

El pulso binaural es una ilusión auditiva percibida cuando se presentan dos tonos de frecuencias ligeramente diferentes de forma dicótica (un tono distinto en cada oído). El cerebro, específicamente el **núcleo olivar superior**, procesa esta diferencia y genera un tercer tono interno equivalente a la resta aritmética de ambas frecuencias.

$$f_{binaural} = |f_{right} - f_{left}|$$

### Brainwave Entrainment (Arrastre Cerebral)

Este proyecto se basa en la hipótesis de que el cerebro tiende a sincronizar sus ondas electroencefalográficas (EEG) con la frecuencia del estímulo externo. Al seleccionar un preset, el usuario está "entrenando" su estado cognitivo:

| Onda | Rango (Hz) | Estado Asociado | Aplicación Técnica |
| :--- | :--- | :--- | :--- |
| **Delta** | 0.5 – 4 | Sueño Profundo | Regeneración de tejidos, reducción de cortisol. |
| **Theta** | 4 – 8 | Meditación | Acceso a memoria profunda y estados hipnagógicos. |
| **Alpha** | 8 – 14 | Flujo (Flow) | Reducción de la "red neuronal por defecto" (rumiación). |
| **Beta** | 14 – 30 | Concentración | Procesamiento lineal, atención externa y lógica. |
| **Gamma** | 30 – 100 | Hiper-foco | Síntesis de información compleja y alta cognición. |

-----

## 🛠 Arquitectura del Software

El motor utiliza un gráfico de audio modular para garantizar latencia cero y una pureza de onda senoidal absoluta:

1.  **Oscillators (L/R):** Dos nodos `OscillatorNode` generan ondas senoidales puras.
2.  **Channel Merger:** Un `ChannelMergerNode` de 2 canales asegura que las frecuencias no se mezclen en el aire (mono), sino que lleguen de forma independiente a cada auricular (estéreo real).
3.  **WAV Synthesis:** Para la descarga, se implementó un codificador manual de encabezados **RIFF/WAVE**, transformando los datos de punto flotante en enteros de 16 bits (PCM) a una frecuencia de muestreo de **44,100 Hz**.

-----

## 🎨 Diseño para la Neurodivergencia

Siguiendo principios de **Diseño Universal**, la interfaz evita la sobrecarga sensorial mediante:

  * **Contraste de Proporción Áurea:** Uso de fondos oscuros (`#0f172a`) para reducir la fatiga visual.
  * **Affordance Intuitivo:** Botonera con codificación de colores basada en semántica de seguridad (Start/Stop).
  * **Información On-Demand:** La documentación técnica está encapsulada en un modal para no abrumar al usuario durante la tarea principal (evitar la parálisis por análisis).

-----

## 🚀 Instalación y Uso

1.  Clona el repositorio:
    ```bash
    git clone https://github.com/Blandskron/binaural-studio-core.git
    ```
2.  Abre `index.html` en cualquier navegador moderno.
3.  **Requisito Crítico:** Se deben utilizar **auriculares estéreo** para que el efecto binaural sea efectivo.

-----

## 📄 Licencia

Distribuido bajo la Licencia MIT. Ver `LICENSE` para más información.
