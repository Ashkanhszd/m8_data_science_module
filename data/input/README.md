# Datos de entrada del Módulo 8

Datos **sintéticos** creados para la docencia. Representan una zona ficticia cercana a Barcelona con tres acuíferos, doce pozos y dos estaciones meteorológicas, con datos mensuales de 2021 a 2025. En ese periodo hay una sequía (2022–2024) y una recuperación en 2025.

Son datos pensados para aprender. Se comportan de forma parecida a los reales y, **como los datos reales, contienen errores e incidencias**. Parte del trabajo del módulo consiste en encontrarlos, decidir qué hacer con ellos y documentar la decisión.

> Los archivos de esta carpeta son los **datos originales**: no se modifican nunca. Cualquier versión corregida se guarda en `data/output/`.

## Archivos

| Archivo | Qué contiene | Una fila representa |
|---|---|---|
| `pozos.csv` | Localización, acuífero, cota, profundidad y uso de cada pozo | un pozo |
| `estaciones.csv` | Estaciones meteorológicas | una estación |
| `precipitacion.csv` | Precipitación mensual por estación | una estación en un mes |
| `mediciones.csv` | Profundidad del nivel y conductividad eléctrica | un pozo en un mes |
| `hidroquimica.csv` | Iones mayoritarios (campañas de primavera y otoño 2024–2025) | un análisis |
| `ensayo_bombeo_P02.csv` | Descensos durante un ensayo de bombeo en P02 | un instante del ensayo |
| `diccionario_datos.csv` | Significado, unidad y tipo de cada columna | una columna |
| `datos_hidrogeologicos.xlsx` | Las mismas tablas en un libro Excel (una hoja por tabla) | — |

La base de datos `data/database/hidrogeologia.sqlite` contiene las mismas tablas en formato SQLite.

## Relaciones entre tablas

```text
estaciones 1 ──── N pozos           (pozos.id_estacion)
estaciones 1 ──── N precipitacion   (precipitacion.id_estacion)
pozos      1 ──── N mediciones      (mediciones.id_pozo)
pozos      1 ──── N hidroquimica    (hidroquimica.id_pozo)
```

## Información mínima (metadatos)

- **Sistema de referencia:** ETRS89 / UTM zona 31N (**EPSG:25831**).
- **Profundidad del nivel:** se mide desde la superficie del terreno, en metros. Un valor mayor significa un nivel **más bajo**.
- **Cota piezométrica:** no se entrega. Se calcula como `cota_terreno_m − profundidad_nivel_m`.
- **Conductividad eléctrica:** se da en µS/cm a 25 °C.
- **Fechas:** siguen el formato ISO `AAAA-MM-DD`. Los datos mensuales se fechan el día 1 de cada mes.
- **Hidroquímica:** se da en mg/L. Los valores por debajo del límite de detección aparecen como texto, por ejemplo `<0.5`.
- **Ensayo de bombeo:** caudal constante Q = 12 L/s en P02, con descensos medidos en un piezómetro situado a r = 25 m.

El detalle de cada columna está en `diccionario_datos.csv`.
