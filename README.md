# M8 · Herramientas y Data Science

Repositorio docente del **Módulo 8** del *Máster en Hidrogeología y Modelación* de la Universitat de Barcelona (curso 2026–2027). Contiene los notebooks de las sesiones de programación, análisis de datos y automatización, los datos del curso y las soluciones de los ejercicios de clase.

**No se necesitan conocimientos previos de programación.**

## Cómo empezar (Google Colab)

1. Pulsa el botón **Abrir en Colab** de la sesión del día (tabla inferior). Necesitas una cuenta de Google.
2. En Colab, guarda tu copia: **Archivo → Guardar una copia en Drive**. Si no lo haces, perderás los cambios al cerrar la pestaña.
3. Ejecuta la **primera celda de código** (*Preparación del entorno*). Descarga este repositorio con los datos dentro de la sesión de Colab.
4. Ejecuta las celdas **en orden**, de arriba abajo.

> Colab es un entorno **temporal**: al cerrar la sesión se borran los archivos generados (tablas, figuras…). Descarga lo que quieras conservar.

## Sesiones

| Sesiones | Contenido | Notebook | Soluciones |
|---|---|---|---|
| M8_8.19–21 | Programación científica · entornos y reproducibilidad · Git · fundamentos de Python | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8_data_science_module/blob/main/M8_8.19_21_ashkan_python_basics/M8_8.19_21_Programacion_cientifica_y_Python.ipynb) | [soluciones](soluciones/M8_8.19_21_soluciones.ipynb) |
| M8_8.22–24 | NumPy · pandas · Matplotlib · caso: ensayo de bombeo (Cooper–Jacob) | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8_data_science_module/blob/main/M8_8.22_24_ashkan_numpy_pandas_matplotlib/M8_8.22_24_NumPy_pandas_Matplotlib.ipynb) | [soluciones](soluciones/M8_8.22_24_soluciones.ipynb) |
| M8_8.25–27 | Bases de datos y SQL · estadística descriptiva · calidad de datos · correlación y retardos | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8_data_science_module/blob/main/M8_8.25_27_ashkan_dbs_statistics/M8_8.25_27_Gestion_datos_estadistica_calidad.ipynb) | [soluciones](soluciones/M8_8.25_27_soluciones.ipynb) |
| M8_8.31–33 | Funciones y módulos · automatización · taller: proyecto reproducible con datos nuevos | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8_data_science_module/blob/main/M8_8.31_33_ashkan_python_advanced/M8_8.31_33_Funciones_automatizacion_reproducibilidad.ipynb) | [soluciones](soluciones/M8_8.31_33_soluciones.ipynb) |

Las soluciones de cada sesión se publican después de la clase.

### Recorrido completo del módulo

| Bloque | Profesorado | Herramientas |
|---|---|---|
| M8_8.1 · Presentación del módulo | Ashkan Hassanzadeh | — |
| M8_8.2–9 · Sistemas de información geográfica | Nieves Lantada | QGIS |
| M8_8.10–15 · Modelización geológica 3D | Gemma Mitjanas | Leapfrog |
| M8_8.16–18 · Automatización de geoprocesos | Ashkan Hassanzadeh | QGIS Graphical Modeler |
| **M8_8.19–27 · Python, datos, estadística y calidad** | **Ashkan Hassanzadeh** | **Python (este repositorio)** |
| M8_8.28–30 · Análisis exploratorio, interpolación y balance hídrico | Víctor Pinilla | Python, WaterpyBal |
| **M8_8.31–33 · Funciones, automatización y reproducibilidad** | **Ashkan Hassanzadeh** | **Python (este repositorio)** |
| M8_8.34–36 · Análisis hidrogeológico con Python y modelos numéricos | Teresa Palma y Marc Diviu | Python |
| M8_8.37–42 · Machine learning aplicado a la hidrogeología | Aitor Iraola | Python |
| M8_8.43 · Introducción a los modelos de lenguaje | Ashkan Hassanzadeh | — |

## Datos del curso

`data/input/` contiene un conjunto de datos **sintético**: 12 pozos en 3 acuíferos, 2 estaciones meteorológicas, medidas mensuales de 2021 a 2025, análisis químicos, un ensayo de bombeo y una campaña de campo de 2026. Como los datos reales, **contiene errores** que aprenderás a detectar y tratar. Consulta [data/input/README.md](data/input/README.md) y `data/input/diccionario_datos.csv`.

La misma información está en `data/database/hidrogeologia.sqlite` (base de datos SQLite) y en `data/input/datos_hidrogeologicos.xlsx`.

## Estructura del repositorio

```text
m8_data_science_module/
├── README.md
├── LICENSE
├── environment.yml                    entorno Conda (para trabajar en tu ordenador)
├── requirements.txt
├── Guia_instalacion_*.docx            guías de instalación (Anaconda, SQLite y DB Browser)
├── data/
│   ├── input/                         datos originales (no se modifican nunca)
│   ├── database/                      base de datos SQLite
│   └── output/                        resultados generados por los notebooks
├── M8_8.19_21_ashkan_python_basics/
├── M8_8.22_24_ashkan_numpy_pandas_matplotlib/
├── M8_8.25_27_ashkan_dbs_statistics/
├── M8_8.31_33_ashkan_python_advanced/
└── soluciones/
```

## Trabajar en tu propio ordenador (opcional)

Colab es suficiente para todas las sesiones. Si prefieres trabajar en local:

```bash
git clone https://github.com/Ashkanhszd/m8_data_science_module.git
cd m8_data_science_module
conda env create --file environment.yml
conda activate modulo8
jupyter lab
```

Las guías de instalación del repositorio explican estos pasos con detalle para Windows.

## Uso de asistentes de IA

Se permite usar asistentes de IA (por ejemplo, Gemini en Colab) para **entender** código y mensajes de error. En los ejercicios de clase, inténtalo primero por tu cuenta. Debes poder explicar cada línea de cualquier código que entregues, y comprobar siempre lo que te dice el asistente con la documentación oficial.

## Licencia

Material docente bajo licencia [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es); código bajo licencia MIT. Ver [LICENSE](LICENSE).

Contacto: Ashkan Hassanzadeh · a.hassanzadeh@csic.es
