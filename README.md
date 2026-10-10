# Give Me Some Credit — proyecto final de Machine Learning

Entorno reproducible con Python 3.12 y uv.

## Comenzar desde la terminal

```bash
cd /Users/lenytacuri/GiveMeSomeCredit
uv sync --locked
uv run jupyter lab notebooks/01_exploracion.ipynb
```

`uv run` utiliza automáticamente el entorno `.venv`; no necesitas activarlo.
Para añadir dependencias usa `uv add nombre-del-paquete`.
Conserva `pyproject.toml`, `uv.lock` y `.python-version` para reproducir el entorno.

## Archivos de entrada

- `cs-training.csv`: datos etiquetados para desarrollar y validar modelos.
- `cs-test.csv`: datos para predicción; no usarlos como validación si no tienen etiquetas.
- `sampleEntry.csv`: ejemplo del formato de entrega.
- `Data Dictionary.xls`: descripción de variables; se lee con xlrd.

Los datos originales permanecen en esta carpeta. El notebook reconoce la raíz del proyecto tanto si se ejecuta desde la raíz como desde `notebooks/`.

## Bibliotecas

pandas y NumPy para datos, matplotlib y seaborn para gráficos, scikit-learn para modelos, JupyterLab e ipykernel para notebooks, xlrd para el diccionario `.xls`.

## Siguientes pasos del trabajo

1. Revisar el diccionario, la variable objetivo `SeriousDlqin2yrs`, los faltantes y el balance de clases.
2. Separar entrenamiento y validación de forma estratificada antes de ajustar imputaciones o transformaciones.
3. Construir un modelo de referencia con un Pipeline de scikit-learn.
4. Comparar modelos con métricas apropiadas al desbalance y documentar las decisiones según la rúbrica de la materia.

El notebook inicial carga e inspecciona los datos; todavía no entrena modelos.
