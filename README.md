# AluraStoreLatam — Análisis de ventas (Challenge 1)

Este repositorio contiene un notebook (`AluraStoreLatam.ipynb`) con un análisis exploratorio y visual de ventas para cuatro tiendas del challenge de Alura (LATAM).

## Propósito del análisis

El objetivo principal es extraer insights operativos y comerciales a partir de los datos de ventas de las cuatro tiendas. Concretamente:
- Detectar o calcular la columna de facturación (revenue) por tienda y comparar los totales.
- Analizar ventas por categoría y productos más/menos vendidos.
- Calcular métricas de calidad como calificación promedio (rating) y analizar envío promedio por tienda.
- Proveer visualizaciones que faciliten la interpretación y la toma de decisiones (gráficos de barras, series agregadas y tablas resumen).

## Estructura del proyecto

- `AluraStoreLatam.ipynb` — Notebook principal con todos los análisis y visualizaciones.
- `base-de-datos-challenge1-latam/` — Carpeta con los CSV de las tiendas:
  - `tienda_1 .csv`
  - `tienda_2.csv`
  - `tienda_3.csv`
  - `tienda_4.csv`
- `README.md` — Este archivo (documentación y pasos para ejecutar).
- `requirements.txt` — Dependencias mínimas para reproducir el entorno y ejecutar el notebook.

## Ejemplos de gráficos e insights obtenidos

El notebook incluye varias visualizaciones y resultados; aquí tienes ejemplos de lo que puedes esperar y por qué son útiles:

- Gráfico: Facturación por tienda (bar chart)
  - Qué muestra: suma total de la columna de facturación detectada por tienda.
  - Insight: permite identificar qué tienda tiene mayor/menor facturación y detectar discrepancias entre tiendas.

- Gráfico: Ventas por categoría (bar/treemap)
  - Qué muestra: ventas agregadas (por monto o unidades) por categoría de producto.
  - Insight: ayuda a priorizar categorías con mayor contribución a los ingresos.

- Tabla: Productos más y menos vendidos
  - Qué muestra: top N y bottom N según unidades vendidas o ingresos por producto.
  - Insight: detecta productos estrella y productos con baja rotación que podrían analizarse para promociones o discontinuación.

- Métrica: Calificación promedio por tienda
  - Qué muestra: promedio de las reseñas o ratings si existen en los datos.
  - Insight: correlacionar satisfacción con ventas y priorizar mejoras operativas.

- Métrica: Envío promedio por tienda
  - Qué muestra: costo de envío promedio por pedido.
  - Insight: comparar estructuras de costo entre tiendas y estimar impacto en margen.

> Nota: las gráficas son generadas con matplotlib/pandas. El notebook incluye código que intenta detectar automáticamente la columna de facturación (por nombres comunes como `total`, `monto`, `price`, etc.) y, si es necesario, calcula la facturación como `cantidad * precio`.

## Instrucciones para ejecutar el notebook

Requisitos previos
- Python 3.8 o superior (recomendado).
- Pip (gestor de paquetes).

Instalación de dependencias (PowerShell)
```powershell
python -m pip install -r requirements.txt
```

Abrir y ejecutar el notebook
- Opción 1 — Visual Studio Code:
  1. Abre la carpeta del proyecto en VS Code.
  2. Instala la extensión "Jupyter" si no la tienes.
  3. Abre `AluraStoreLatam.ipynb` y ejecuta las celdas con la interfaz de Jupyter integrada.

- Opción 2 — Jupyter Notebook / JupyterLab:
  1. Abre una terminal en la raíz del proyecto.
  2. Ejecuta `jupyter notebook` o `jupyter lab`.
  3. En la interfaz web, abre `AluraStoreLatam.ipynb` y ejecuta las celdas.

Recomendaciones prácticas
- Si trabajas con datos locales (archivos CSV en `base-de-datos-challenge1-latam/`) el notebook los cargará directamente. Si prefieres usar las URLs remotas incluidas en el código, asegúrate de tener conexión a Internet.
- Si ves resultados inesperados (por ejemplo facturación 0 o NaN), revisa las columnas de tus CSV: puede haber símbolos de moneda, separadores de miles o texto no numérico que requieren limpieza previa.
- Para evitar que el notebook mutile los DataFrames originales al crear columnas temporales (p. ej. `__revenue_calc`), modifica las celdas para usar `df = df.copy()` antes de las transformaciones.

## Ejecución rápida (comandos útiles)

Instalar dependencias:
```powershell
python -m pip install -r requirements.txt
```

Abrir Jupyter Lab:
```powershell
jupyter lab
```

Abrir Jupyter Notebook:
```powershell
jupyter notebook
```


Licencia: MIT (ajusta según prefieras)

