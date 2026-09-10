# M8 · Herramientas y Data Science

Repositorio docente para las sesiones de programación, gestión y análisis de datos del **Módulo 8: Herramientas y Data Science** del Máster de Formación Permanente en Hidrogeología y Modelación.

## Cómo utilizar los notebooks

Los notebooks están alojados en GitHub y pueden abrirse directamente en Google Colab, sin necesidad de instalar Python en el ordenador.

1. Selecciona el notebook correspondiente a la sesión.
2. Haz clic en el botón **Open in Colab**.
3. En Google Colab, selecciona **Archivo → Guardar una copia en Drive** antes de empezar a modificarlo.
4. Ejecuta las celdas en orden.
5. Descarga o guarda los resultados que quieras conservar, ya que el almacenamiento temporal de Colab se elimina al finalizar la sesión.

> [!IMPORTANT]
> Antes de publicar el repositorio, sustituye `Ashkanhszd` en los enlaces siguientes por el nombre del usuario o de la organización de GitHub donde se aloje el repositorio.

## Notebooks del módulo

### M8_8.19–M8_8.21 · Programación científica, entornos y control de versiones

Conceptos de programación científica, fundamentos de Python, entornos virtuales, Conda, contenedores, Docker, Git, GitHub y uso de Google Colab.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8-herramientas-data-science/blob/main/M8_8.19_21/M8_8.19_21_Programacion_entornos_git.ipynb)

[Ver el notebook en GitHub](M8_8.19_21/M8_8.19_21_Programacion_entornos_git.ipynb)

### M8_8.22–M8_8.24 · NumPy, pandas y Matplotlib

Introducción a arrays y operaciones numéricas, importación de datos desde CSV y Excel, consulta de la misma información desde SQLite, manipulación de datos con pandas y visualización científica con Matplotlib.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8-herramientas-data-science/blob/main/M8_8.22_24/M8_8.22_24_NumPy_pandas_Matplotlib.ipynb)

[Ver el notebook en GitHub](M8_8.22_24/M8_8.22_24_NumPy_pandas_Matplotlib.ipynb)

### M8_8.25–M8_8.27 · Gestión de datos, estadística descriptiva y calidad

Organización de datos, bases de datos relacionales y NoSQL, creación y consulta de SQLite, estadística descriptiva, control de calidad, comparación entre grupos, correlación y dependencia espacial y temporal.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8-herramientas-data-science/blob/main/M8_8.25_27/M8_8.25_27_Datos_estadistica_calidad.ipynb)

[Ver el notebook en GitHub](M8_8.25_27/M8_8.25_27_Datos_estadistica_calidad.ipynb)

### M8_8.31–M8_8.33 · Funciones, automatización y reproducibilidad

Conversión de operaciones conocidas en funciones reutilizables, validación de entradas, automatización por pozo o escenario, configuración, rutas portables, gestión de errores y generación reproducible de tablas, figuras y registros.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ashkanhszd/m8-herramientas-data-science/blob/main/M8_8.31_33/M8_8.31_33_Funciones_automatizacion_reproducibilidad.ipynb)

[Ver el notebook en GitHub](M8_8.31_33/M8_8.31_33_Funciones_automatizacion_reproducibilidad.ipynb)

## Estructura del repositorio

```text
m8-herramientas-data-science/
├── README.md
├── environment.yml
├── requirements.txt
├── data/
│   ├── input/
│   │   ├── pozos.csv
│   │   ├── mediciones.csv
│   │   └── datos_hidrogeologicos.xlsx
│   ├── database/
│   │   └── hidrogeologia.sqlite
│   └── output/
│       ├── tables/
│       ├── figures/
│       └── logs/
├── M8_8.1/
├── M8_8.16_18/
├── M8_8.19_21/
├── M8_8.22_24/
├── M8_8.25_27/
├── M8_8.28_30_victor/
├── M8_8.31_33/
├── M8_8.34_36_marc_tere/
├── docs/
└── src/
```

## Datos docentes

Los archivos siguientes contienen las mismas dos tablas lógicas en formatos diferentes:

- `data/input/pozos.csv`
- `data/input/mediciones.csv`
- `data/input/datos_hidrogeologicos.xlsx`
- `data/database/hidrogeologia.sqlite`

Las tablas representan:

- **pozos**: información relativamente estable de cada punto de control;
- **mediciones**: observaciones mensuales asociadas a los pozos.

Los datos son sintéticos y se han creado exclusivamente con fines docentes. La tabla de mediciones contiene algunos problemas introducidos de forma deliberada para practicar control de calidad: un valor ausente, una precipitación negativa, una conductividad inusualmente alta y una fila duplicada.

## Organización de entradas y resultados

- Los datos originales se conservan en `data/input` y no deben sobrescribirse.
- La base de datos docente se encuentra en `data/database`.
- Las tablas generadas se guardan en `data/output/tables`.
- Las figuras generadas se guardan en `data/output/figures`.
- Los parámetros y registros de ejecución se guardan en `data/output/logs`.

## Trabajo en Google Colab

Cuando un notebook se abre desde GitHub, Google Colab ejecuta una copia editable. Los cambios no modifican automáticamente el notebook original del repositorio.

Para conservar el trabajo:

- utiliza **Archivo → Guardar una copia en Drive**;
- o descarga el notebook mediante **Archivo → Descargar → Descargar .ipynb**;
- descarga también cualquier tabla o figura generada que quieras conservar.

Los notebooks incluyen una celda para localizar el repositorio y acceder de forma coherente a los datos de entrada, la base SQLite y las carpetas de resultados.

## Condiciones de uso

- No publiques contraseñas, tokens, claves de acceso ni datos sensibles.
- No sobrescribas los archivos originales de `data/input`.
- Documenta las unidades, supuestos y decisiones de tratamiento.
- Comprueba e interpreta los resultados antes de utilizarlos en un informe.
