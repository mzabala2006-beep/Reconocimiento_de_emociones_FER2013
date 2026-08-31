# Reconocimiento_de_emociones_FER2013
Descripción

Este proyecto implementa un sistema de clasificación de emociones faciales utilizando TensorFlow/Keras y el dataset FER2013. El modelo está basado en una CNN profunda (Modelo 3) y permite realizar predicciones en tiempo real usando la cámara web.

Requisitos

•	Python 3.8+
•	TensorFlow 2.x
•	Keras (incluido en TensorFlow)
•	OpenCV
•	Streamlit (opcional, para interfaz web)

Instalar dependencias:

bash
pip install -r requirements.txt
Ejemplo de requirements.txt:

Código

tensorflow==2.12.0
opencv-python
streamlit
numpy
scikit-learn
matplotlib

Estructura del repositorio

Código
├── dataset/              # FER2013 (train/test)
├── notebook_entrenamiento.ipynb  # Notebook de entrenamiento
├── modelo_final.keras       # Modelo entrenado
├── prediccion_realtime.py # Código para predicciones en tiempo real con OpenCV
├── app.py                # Interfaz web con Streamlit
├── requirements.txt
└── README.md

Entrenamiento del modelo

Ejecuta el notebook:

bash
notebook notebook_entrenamiento.ipynb

El modelo se guarda como:
python
model.save("modelo_final.keras") Predicciones en tiempo real

Ejecuta el script de cámara:
bash
python prediccion_realtime.py

•	Se abrirá la cámara web.
•	El sistema mostrará la emoción detectada en tiempo real.
•	Presiona q para salir.

Interfaz visual (Streamlit)

Ejecuta:

bash
streamlit run app.py

Esto abrirá una aplicación web local donde podrás ver las predicciones de forma clara e inmediata.

Resultados

•	Accuracy en prueba: ~60%
•	Matriz de confusión: incluida en el notebook.
•	Mejor desempeño: emociones “Happy” y “Surprise”.
•	Mayor confusión: entre “Sad” y “Fear”.
Decisiones de diseño

•	Uso de data augmentation para mejorar generalización.
•	Arquitectura CNN más profunda (Modelo 3).
•	Dropout y Batch Normalization para reducir sobreajuste.
•	Optimizador Adam con tasa de aprendizaje reducida.
•	Entrenamiento extendido (40–50 épocas).
