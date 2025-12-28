# KidneyDiseaseAnalysis

Ejercicio Bloque 7 – Clasificación y Reconocimiento
Asignatura: Técnicas Avanzadas de Análisis y Reconocimiento de Imágenes Biomédicas
Máster en Ingeniería Biomédica y Salud Digital.

Cuaderno en Jupyter Notebook para entrenar y evaluar una red neuronal convolucional (CNN) que clasifica imágenes de TC renal en cuatro categorías: Cyst, Normal, Stone y Tumor, utilizando el dataset público CT KIDNEY DATASET (Normal-Cyst-Tumor-Stone).

El objetivo del ejercicio es aplicar técnicas de deep learning para clasificación de imágenes biomédicas, evaluando el rendimiento del modelo mediante métricas cuantitativas y análisis cualitativo de las predicciones.

--------------------------------------------------

REQUISITOS

Entorno probado con las siguientes versiones (o compatibles):

- Python 3.6.13
- Windows 10 (AMD64, CPU; sin CUDA)
- PyTorch 1.10.2
- Torchvision 0.11.3
- NumPy 1.19.2
- Matplotlib 3.3.4
- scikit-learn 0.24.2
- Pillow 6.2.1
- Pandas 1.1.5
- Jupyter Notebook / JupyterLab
- tqdm

El entrenamiento está diseñado para ejecutarse en CPU, con un número reducido de épocas (3), por lo que el tiempo de ejecución es moderado y adecuado para un portátil sin GPU.

Instalación recomendada de dependencias (alternativamente se puede usar requirements.txt):

pip install torch==1.10.2 torchvision==0.11.3
pip install numpy==1.19.2 matplotlib==3.3.4
pip install scikit-learn==0.24.2 pillow==6.2.1
pip install pandas==1.1.5 tqdm

--------------------------------------------------

DATASET

El dataset utilizado es CT KIDNEY DATASET (Normal-Cyst-Tumor-Stone), disponible públicamente en Kaggle:

https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone

El dataset no se incluye en este repositorio por motivos de tamaño y licencia, y debe descargarse manualmente.

Una vez descargado, descomprimir manteniendo la siguiente estructura de carpetas:

kidney-dataset/
 - Cyst/
 - Normal/
 - Stone/
 - Tumor/

En el notebook debe actualizarse la variable dataset_path para que apunte a la carpeta local donde se haya descomprimido el dataset.

--------------------------------------------------

USO

1. Clonar el repositorio:

git clone https://github.com/fraaanci28/KidneyDiseaseAnalysis.git
cd KidneyDiseaseAnalysis

2. (Opcional) Crear y activar un entorno virtual e instalar las dependencias indicadas.

3. Abrir Jupyter Notebook (por ejemplo, desde Anaconda Prompt):

jupyter notebook

4. En el navegador, abrir el fichero ct-kidney-dataset.ipynb.

5. Ejecutar las celdas en orden. El notebook incluye:

- Carga y exploración del dataset
- Visualización inicial de ejemplos
- Preprocesamiento y creación de DataLoader
- Definición del modelo KidneyCNN
- Entrenamiento del modelo (3 épocas) en CPU
- Evaluación del modelo:
  - Curvas de pérdida y accuracy
  - Matriz de confusión
  - Ejemplos cualitativos de predicciones

Para mejorar la reproducibilidad de los resultados, se fijan semillas aleatorias en NumPy y PyTorch dentro del notebook.

--------------------------------------------------

RESULTADOS

El modelo CNN alcanza una accuracy razonable para un entrenamiento corto en CPU.
Los resultados completos, junto con el análisis y conclusiones, se incluyen tanto en el propio notebook como en el informe PDF generado como parte del ejercicio académico.
