# Python para análisis de datos · de cero a analista

Mi ruta de estudio de Python aplicada al análisis de datos: 27 sesiones prácticas en Google Colab, desde variables y listas hasta Machine Learning, SQL y series de tiempo. Todo en español.

Cada sesión dura alrededor de una hora y se resuelve escribiendo el código desde cero. **Los notebooks no traen soluciones**: traen ejercicios y verificadores que dicen si la respuesta está bien o mal, y por qué, sin revelarla.

## Cómo está armada cada sesión

Cada notebook abre en Colab con el botón de su primera celda y sigue la misma estructura:

1. **Objetivos** y lo que hay que saber antes.
2. **Celda de setup** con imports y funciones verificadoras (se ejecuta, no se edita).
3. Por cada concepto:
   - 📘 **Concepto**: explicación corta con un ejemplo que se ejecuta.
   - ✍️ **Tu turno**: ejercicio con `# Tu código aquí`.
   - ✅ **Verificar**: ✅ o ❌ con el motivo concreto ("se esperaban 5 elementos y hay 3"), probando también casos borde como listas vacías, negativos o ceros.
   - 💡 **Pista**: plegable, por si me quedo atascado.
4. 🏋️ **Reto final** que combina todo lo de la sesión.
5. 🚀 **Nivel pro** opcional.
6. **Checklist de autoevaluación** para cerrar.

Los datos de práctica son pequeños y se generan dentro de cada notebook con semilla fija: ventas de tiendas y movimientos bancarios.

## Temario

### Módulo 1 · Python
| Sesión | Temas |
|---|---|
| [S01 · Fundamentos](sesiones/S01_python_fundamentos.ipynb) | Colab, variables, tipos, operadores, strings y f-strings |
| [S02 · Colecciones y control de flujo](sesiones/S02_colecciones_control_flujo.ipynb) | Listas, tuplas, diccionarios, `if`, `for`, `while` |
| [S03 · Funciones y Python moderno](sesiones/S03_funciones_python_moderno.ipynb) | Funciones, casos borde, comprehensions, `lambda`, `try/except` |

### Módulo 2 · NumPy
| Sesión | Temas |
|---|---|
| [S04 · El ndarray](sesiones/S04_numpy_ndarray.ipynb) | Arrays, ufuncs, `nan` e `inf`, agregaciones |
| [S05 · Indexing y filtrado 1D](sesiones/S05_numpy_indexing_filtrado.ipynb) | Slicing, máscaras booleanas, `np.where` |
| [S06 · Arrays 2D y `axis`](sesiones/S06_numpy_2d_axis.ipynb) | `reshape`, broadcasting 2D, `axis`, z-score |
| [S07 · Indexing 2D y datos reales](sesiones/S07_numpy_indexing_2d_datos_reales.ipynb) | Datos sucios, valores centinela, funciones `nan*`, cargar archivos |
| [S08 · Aleatorios y álgebra lineal](sesiones/S08_numpy_aleatorios_algebra.ipynb) | `default_rng`, producto punto, vectorización vs. bucles |

### Módulo 3 · pandas
| Sesión | Temas |
|---|---|
| [S09 · Series y DataFrame](sesiones/S09_pandas_series_dataframe.ipynb) | `read_csv`, `loc`, `iloc`, filtros, `query` |
| [S10 · Limpieza](sesiones/S10_pandas_limpieza.ipynb) | Nulos, duplicados, `.str`, `apply`, `pd.cut` |
| [S11 · Agrupar y resumir](sesiones/S11_pandas_agrupar_resumir.ipynb) | `groupby`, `pivot_table`, `crosstab`, tasas por segmento |
| [S12 · Combinar y fechas](sesiones/S12_pandas_combinar_fechas.ipynb) | `merge`, `concat`, `.dt`, `resample`, method chaining |
| [S13 · Integrador](sesiones/S13_pandas_integrador.ipynb) | Caso bancario de principio a fin |

### Módulo 4 · Matplotlib
| Sesión | Temas |
|---|---|
| [S14 · Anatomía de un gráfico](sesiones/S14_matplotlib_anatomia.ipynb) | `fig` y `ax`, barras, histogramas, dispersión, formato de ejes |
| [S15 · Gráficos que comunican](sesiones/S15_matplotlib_graficos_que_comunican.ipynb) | Subplots, anotaciones, color con intención, `savefig` |
| [S16 · Cierre del EDA](sesiones/S16_cierre_eda.ipynb) | Análisis exploratorio con conclusiones de negocio |

### Módulo 5 · Machine Learning
| Sesión | Temas |
|---|---|
| [S17 · Fundamentos de ML](sesiones/S17_ml_fundamentos.ipynb) | `train_test_split`, API de scikit-learn, regresión lineal, baseline |
| [S18 · Clasificación](sesiones/S18_ml_clasificacion.ipynb) | Regresión logística, árboles, KNN, umbral |
| [S19 · Evaluación](sesiones/S19_ml_evaluacion.ipynb) | Matriz de confusión, precision, recall, F1, ROC-AUC, validación cruzada |
| [S20 · Modelos más fuertes](sesiones/S20_ml_modelos_fuertes.ipynb) | Overfitting, `GridSearchCV`, Random Forest, LightGBM |
| [S21 · Feature engineering](sesiones/S21_feature_engineering.ipynb) | Codificación, escalado, data leakage, `Pipeline` |
| [S22 · Flujo de competencia](sesiones/S22_flujo_competencia.ipynb) | Validación honesta, leaderboard, registro de experimentos |

### Módulo 6 · Negocio y extras
| Sesión | Temas |
|---|---|
| [S23 · Marketing analytics](sesiones/S23_marketing_analytics.ipynb) | Embudo, conversión, lift, segmentación RFM, ROI |
| [S24 · No supervisado](sesiones/S24_no_supervisado.ipynb) | K-means, codo y silueta, PCA |
| [S25 · SQL desde Python](sesiones/S25_sql_desde_python.ipynb) | `sqlite3`, `pd.read_sql`, CTEs, funciones de ventana |
| [S26 · Series de tiempo](sesiones/S26_series_de_tiempo.ipynb) | `resample`, `rolling`, estacionalidad, pronóstico básico |
| [S27 · Comunicar resultados](sesiones/S27_comunicar_resultados.ipynb) | Propuesta de negocio, slides para decisores, notebook limpio |

## Proyecto de portafolio (en curso)

Lo aprendido aquí se aplica en un proyecto aparte con **datos abiertos del sistema financiero peruano**: denuncias de consumidores ante INDECOPI, cruzadas con estadísticas de la SBS y series del BCRP, para responder qué entidades y productos generan más reclamos ajustando por su tamaño. Cierra con un dashboard en Power BI.

El plan completo, con sesiones, hitos y fuentes, está en [`curricula_data.md`](curricula_data.md).

## Herramientas

Python · NumPy · pandas · Matplotlib · scikit-learn · LightGBM · SQLite · Google Colab

## Cómo usarlo

Abre cualquier notebook de [`sesiones/`](sesiones/) y pulsa **Abrir en Colab** en su primera celda. No hace falta instalar nada. Ejecuta primero la celda de setup y luego resuelve cada ejercicio antes de verificarlo.
