# M8 · Herramientas y Data Science

Repositorio docente para las sesiones de Python y análisis de datos del Módulo 8.

## Uso en Google Colab

1. Publicar este repositorio en GitHub con el nombre `m8-herramientas-data-science`.
2. En los notebooks, sustituir `REPLACE_WITH_YOUR_GITHUB_USERNAME` por el usuario u organización de GitHub.
3. Abrir un notebook con una URL de este tipo:

```text
https://colab.research.google.com/github/USUARIO/m8-herramientas-data-science/blob/main/M8_8.19_21/M8_8.19_21_Programacion_entornos_git.ipynb
```

La primera celda de preparación localiza el repositorio. En Colab, clona una copia temporal. Los estudiantes deben guardar una copia en Drive o descargar su notebook para conservar cambios.

## Notebooks

- `M8_8.19_21`: programación científica, entornos, Conda, contenedores, Git/GitHub y Python.
- `M8_8.22_24`: NumPy, pandas y Matplotlib con CSV, Excel y SQLite.
- `M8_8.25_27`: SQL, estadística descriptiva, calidad, grupos, correlación y dependencia.
- `M8_8.31_33`: funciones, automatización y reproducibilidad.

## Datos

`data/input` contiene CSV y Excel. `data/database` contiene la misma información en SQLite. No sobrescribir los originales. Los resultados regenerables van en `data/output`.

## Entorno local

```bash
conda env create -f environment.yml
conda activate modulo8
jupyter lab
```

## Flujo Git recomendado para el profesorado

```bash
git status
git add .
git commit -m "Actualiza materiales del modulo"
git push
```

## Flujo para estudiantes

Abrir desde Colab, trabajar sobre una copia y seguir las instrucciones de entrega. No publicar credenciales, tokens ni datos sensibles.
