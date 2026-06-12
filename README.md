# 🌸 Clasificación de Flores con CNN y Segmentación Adaptativa por Umbrales

**Autor:** Cristian Esparza  
**Técnica de Preprocesamiento:** Segmentación Adaptativa por Umbrales  
**Fecha:** Junio 2026

## Descripción

Este proyecto implementa una Red Neuronal Convolucional (CNN) para la clasificación automática de 5 tipos de flores (Margaritas, Dientes de León, Rosas, Girasoles y Tulipanes). Se aplica **segmentación adaptativa por umbrales** como técnica de preprocesamiento para mejorar la detección de bordes y características en las imágenes.

---

##  Requisitos

- Cuenta de **Google** (para usar Google Colab y Google Drive)
- Navegador web
- Espacio disponible en Google Drive (~500 MB recomendado)

---

##  Instrucciones de Instalación y Ejecución

### Paso 1: Clonar o Descargar el Repositorio

1. Ve al repositorio de GitHub
2. Descarga o clona los siguientes archivos:
   - `Segmentación_adaptativo_por_umbrales.ipynb` (Preprocesamiento)
   - `PROYECTO_FINAL_IMÁGENES_RGB.ipynb` (Red Neuronal)
  .  Descarga el archivo en el siguiente enlace **https://drive.google.com/drive/folders/1uRDB5GqLj1Zv5UEmYDH1Dk4qB9CLLrKU?usp=sharing** 
   - Carpeta `archive/` (Dataset original con las imágenes)

### Paso 2: Preparar Google Drive

1. Inicia sesión en tu cuenta de **Google Drive**
2. Crea una carpeta llamada `archive` (si no está incluida en la descarga)
3. Asegúrate de tener suficiente espacio disponible

### Paso 3: Ejecutar el Preprocesamiento en Google Colab

1. Abre **Google Colab**: https://colab.research.google.com/
2. Sube el notebook `Segmentación_adaptativo_por_umbrales.ipynb`
3. Ejecuta la primera celda para **montar Google Drive**:
   ```python
   from google.colab import drive
IMPORTANTE: Modifica la ruta del input en la siguiente variable
 **input_folder = "/content/drive/MyDrive/archive/flowers"**
   

Sigue las instrucciones para autorizar el acceso a tu **Drive**

Ejecuta las celdas restantes del notebook
Resultado: Se creará automáticamente una carpeta llamada output_masks en tu Google Drive con las imágenes preprocesadas
### Paso 4: Configurar y Ejecutar la Red Neuronal
Abre un nuevo notebook en Google Colab
Sube el archivo PROYECTO_FINAL_IMÁGENES_RGB.ipynb
Ejecuta la celda de montaje de Google Drive
IMPORTANTE: Modifica la ruta del dataset en la siguiente variable
**DATASET_DIR = "/content/drive/MyDrive/output_masks"**

Ejecuta todas las celdas del notebook en orden
El modelo se entrenará y mostrará:
Gráficas de accuracy y pérdida
Matriz de confusión
Reporte de clasificación (Precision, Recall, F1-Score)
### Paso 5: Prueba Interactiva (Opcional)###
Al final del notebook principal, encontrarás una celda que te permite:
Subir una imagen de flor desde tu computadora
Obtener una predicción en tiempo real del modelo entrenado
