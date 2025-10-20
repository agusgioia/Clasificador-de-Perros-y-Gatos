# Clasificación de Imágenes: Perros vs Gatos con Redes Neuronales (Densa vs CNN)

Este proyecto tiene como objetivo comparar el rendimiento entre un **modelo denso tradicional (MLP)** y una **red neuronal convolucional (CNN)** 
para la clasificación binaria de imágenes del dataset **Cats vs Dogs** de TensorFlow Datasets.
El trabajo demuestra de forma práctica cómo el uso de arquitecturas adecuadas al tipo de dato impacta directamente en la performance del modelo.

---
##  Descripción del Proyecto

- **Dataset:** [`cats_vs_dogs`](https://www.tensorflow.org/datasets/catalog/cats_vs_dogs) (TensorFlow Datasets)
- **Tamaño de imagen:** 100x100 píxeles, en escala de grises.
- **Etiquetas:**  
  - `0` → Gato  
  - `1` → Perro  

El pipeline completo incluye:
1. **Carga y preprocesamiento de datos** (redimensionamiento, conversión a gris, normalización).
2. **Construcción de dos arquitecturas distintas:**
   - **Modelo Denso (Fully Connected Neural Network)**
   - **Modelo Convolucional (CNN)**
3. **Entrenamiento supervisado** con `binary_crossentropy`, `adam` y **EarlyStopping**.
4. **Evaluación comparativa** de rendimiento entre ambos modelos.

---

##  Tecnologías Utilizadas

- **Python 3.x**
- **TensorFlow / Keras**
- **TensorFlow Datasets**
- **OpenCV**
- **NumPy**
- **Matplotlib**

---

##  Resultados Principales

| Modelo | Accuracy Promedio | Observaciones |
|:--------|:------------------:|:---------------|
| 🔹 Denso (MLP) | ~60% | No logra capturar la estructura espacial de las imágenes. |
| 🔸 CNN | ~85% - 87% | Extrae patrones visuales (bordes, texturas, formas) y generaliza mejor. |

 **Conclusión:**  
Las **redes convolucionales (CNN)** son significativamente más efectivas para tareas de visión por computadora, ya que aprovechan la estructura espacial de los datos de imagen.

---
##  Conclusiones

- El modelo denso alcanza una precisión limitada (~60%), insuficiente para distinguir patrones visuales complejos.
- La CNN, con capas convolucionales y de pooling, obtiene una precisión mucho mayor (~87%) y una pérdida significativamente menor.
- Se utilizó **Early Stopping** para prevenir el sobreajuste y conservar los mejores pesos.

---

##  Autor

**Agustín Gioia**  
 [(https://www.linkedin.com/in/agustin-gioia/)]  
 Proyecto desarrollado con fines educativos y de portfolio personal.  
