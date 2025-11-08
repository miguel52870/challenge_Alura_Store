# Análisis de Ventas — AluraStore Latam (Challenge 1)

## Descripción
----------
Este repositorio contiene un análisis exploratorio de ventas de cuatro tiendas (Tienda 1 a Tienda 4) realizado con un notebook de Jupyter: `AluraStoreLatam.ipynb`.

El objetivo del análisis es comparar desempeño (ingresos, categorías, calificaciones, productos, costos de envío y métodos de pago) y recomendar cuál tienda podría venderse.

## Datos
-----
Los datos se cargan desde CSV públicos (usados en el notebook):

- Tienda 1: https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_1%20.csv
- Tienda 2: https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_2.csv
- Tienda 3: https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_3.csv
- Tienda 4: https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_4.csv

## Estructura del Notebook
-----------------------
El notebook `AluraStoreLatam.ipynb` realiza las siguientes tareas principales:

1. Importación de datos.
2. Cálculo de ingresos totales por tienda.
3. Ventas por categoría (por tienda).
4. Calificación promedio por tienda.
5. Productos más y menos vendidos por tienda.
6. Costo de envío promedio por tienda.
7. Visualizaciones: barras, líneas, subplots y gráficos comparativos.
8. Análisis final y recomendación.

## Resultados principales (resumen)
--------------------------------
En el análisis incluido se reportan los ingresos totales por tienda (formato COP) y una recomendación estratégica:

| Tienda  | Ingreso Total ($)    |
|---------|---------------------:|
| Tienda 1 | 1,150,880,400 |
| Tienda 2 | 1,116,343,500 |
| Tienda 3 | 1,098,019,600 |
| Tienda 4 | 1,038,375,700 |

Conclusión principal: la **Tienda 4** es la opción recomendada para vender/desinvertir por presentar los menores ingresos y una mezcla de ventas menos favorable en categorías de mayor valor; el notebook incluye el razonamiento y visualizaciones que apoyan esta recomendación.

## Requisitos
----------
- Python 3.8+ (se recomienda 3.9 o superior)
- Recomendado ejecutar en un entorno virtual (venv, conda, etc.)

Dependencias principales (ver `requirements.txt`):
- pandas
- matplotlib
- jupyter
- numpy

## Uso en Google Colab
-------------------
Si vas a ejecutar el notebook en Google Colab, normalmente NO es necesario instalar `pandas` ni `matplotlib`, porque Colab trae estas bibliotecas preinstaladas. Aun así, puede convenir comprobar versiones o instalar una versión específica si necesitas reproducir resultados exactos. Ejemplos para una celda al inicio del notebook:

```python
# comprobar versiones instaladas
import pandas as pd
import matplotlib
print("pandas:", pd.__version__)
print("matplotlib:", matplotlib.__version__)

# si necesitas una versión concreta
%pip install pandas==1.5.3 matplotlib==3.7.1
```

Usa `%pip` en vez de `!pip` para asegurar que la instalación se aplique al mismo kernel del notebook. Algunas instalaciones pueden requerir reiniciar el runtime (Runtime -> Restart runtime) si contienen extensiones compiladas.

## Instalación y ejecución para uso local (Windows / PowerShell)
----------------------------------------------
Abre PowerShell y ejecuta los siguientes pasos desde la carpeta donde está el notebook:

```powershell
# crear y activar un entorno virtual
python -m venv .venv

# en PowerShell, para activar:
.\\.venv\\Scripts\\Activate.ps1

# instalar dependencias
pip install -r requirements.txt

# lanzar Jupyter Notebook en la carpeta actual
jupyter notebook "AluraStoreLatam.ipynb"
```

Alternativamente puedes abrir `AluraStoreLatam.ipynb` directamente en VS Code con la extensión de Jupyter.

## Cómo usar el notebook
---------------------
pasos prácticos y recomendaciones para ejecutar y sacar provecho al notebook `AluraStoreLatam.ipynb`.

1) Ejecutar todo el notebook (flujo recomendado)
	- Abre el notebook en Jupyter Notebook / JupyterLab, google colab o en VS Code (extensión Jupyter).
	- Si trabajas localmente, activa tu entorno virtual y asegúrate de haber instalado las dependencias (ver sección "Instalación y ejecución para uso local").
	- En google colab "Run all, en la interfaz de Jupyter selecciona: Kernel -> Restart & Run All o en VS Code "Run All Cells". Esto ejecuta todas las celdas en orden y genera las tablas y gráficos.

2) Ejecutar solo partes del análisis
	- Si solo necesitas tablas resumen, ejecuta las celdas en las secciones: "1. Análisis de facturación", "2. Ventas por categoría", "3. Calificación promedio".
	- Para regenerar solo gráficos, ejecuta la sección "6. graficos".

3) Ejecutar en Google Colab
	- Sube el notebook a Colab o ábrelo desde GitHub/Drive. Colab incluye `pandas` y `matplotlib` por defecto, por lo que normalmente no necesitas pip instalar nada (ver la sección "Uso en Google Colab").

4) Resultados esperados
	- Tablas: `resultados_ingresos`, `ventas_por_tienda_categoria`, `resultados_df` (calificaciones), tablas de top/bottom products.
	- Gráficos: barras de ingresos por tienda, evolución mensual por tienda (líneas), subplots de categorías por tienda, gráfico scatter costo envío vs calificación, y la gráfica apilada de métodos de pago.
	- Informe final (celda markdown): resumen con la recomendación estratégica (vender Tienda 4).


## Notas sobre reproducibilidad
---------------------------
- Los CSV se cargan directamente desde los enlaces públicos, por lo que necesitarás conexión a internet la primera vez que ejecutes el notebook.
- Si deseas fijar versiones exactas de paquetes en la ejecucion local para reproducir resultados idénticos, modifica `requirements.txt` con versiones específicas.

## Licencia y contacto
-------------------
- Licencia: este documento puede adaptarse libremente para uso personal y educativo.
- Autor/contacto: Miguel Angel Castro Medina / miguel52870@gmail.com

## Archivo principal
-----------------
- `AluraStoreLatam.ipynb` — Notebook con todo el análisis y gráficos.
