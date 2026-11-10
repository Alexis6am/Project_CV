# Computer Vision – Retail Product Recognition

## Descripción

Este proyecto desarrolla un sistema de **Computer Vision** orientado al reconocimiento de productos de retail mediante modelos de aprendizaje automático.

El repositorio contiene el proceso de preparación de datos, procesamiento de imágenes, entrenamiento de modelos y desarrollo de un backend para exponer las funcionalidades mediante una API.

## Estructura del proyecto

```text
proyecto/
│
├── data/
│   └── raw/
│       ├── producto_antoni/
│       ├── producto_cafe/
│       ├── producto_03/
│       ├── producto_04/
│       ├── ...
│       └── producto_10/
│
├── notebooks/
│   └── ...
│
├── backend/
│   └── ...
│
└── README.md
```

El dataset contiene un mínimo de 10 categorías de productos, organizadas en carpetas independientes dentro de `data/raw/`. Cada carpeta almacena las fotografías correspondientes a un producto específico.

## Instalación y ejecución

### 1. Preparación del dataset

Descargar el dataset y colocarlo dentro de la carpeta `data/raw/`.

Las imágenes deben organizarse en carpetas independientes según el producto al que pertenecen.

Ejemplo:

```text
data/raw/
├── producto_antoni/
├── producto_cafe/
└── ...
```

### 2. Ejecución de notebooks

Ejecutar los scripts y notebooks disponibles en la carpeta `notebooks/`, respetando el orden de procesamiento y entrenamiento establecido en cada uno.

## Procesamiento y experimentos

### Segmentación Colgate

Se desarrolló un proceso de segmentación por color utilizando el espacio de color **HSV**.

El procedimiento consiste en:

1. Convertir las imágenes al espacio de color HSV.
2. Generar histogramas para analizar la distribución de los valores de color.
3. Identificar las concentraciones más altas de píxeles correspondientes al color de interés.
4. Seleccionar manualmente los umbrales de segmentación a partir de la interpretación de los histogramas.
5. Aplicar los umbrales seleccionados para obtener la máscara de segmentación.

### U1 – Construcción del dataset

Creación y organización del dataset a partir de las fotografías recopiladas.

**Consideraciones para añadir nuevas imágenes:**

- Mantener la nomenclatura utilizada en el dataset.
- Verificar cuál es el último número asignado a las imágenes existentes.
- Continuar la numeración de manera consecutiva al añadir nuevas fotografías.

Por ejemplo, si la última imagen tiene el número `10`, la siguiente deberá continuar con el número `11`.

### U2 – [Nombre del experimento]

Descripción del proceso, técnicas utilizadas y resultados obtenidos.

## Backend – FastAPI

Se implementa un backend utilizando **FastAPI**, encargado de exponer las funcionalidades del proyecto mediante endpoints HTTP.

Aquí se integrarán los modelos y procesos necesarios para realizar las tareas de reconocimiento de productos.

## Tecnologías utilizadas

- Python
- Computer Vision
- OpenCV
- NumPy
- Matplotlib
- FastAPI
- [Framework de entrenamiento utilizado]

## Estado del proyecto

En desarrollo.