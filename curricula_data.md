# Currícula: de cero a analista de datos

> Plan de estudio personal de Python para análisis de datos, con un proyecto de portafolio que crece sesión a sesión.
> Cada sesión es un notebook de Google Colab en `sesiones/`.

---

## 0. Reglas del plan

**Meta:** dominar Python para análisis de datos (NumPy, pandas, Matplotlib, Machine Learning, SQL) y publicar un proyecto propio de portafolio.

**Ritmo:** ~1 hora diaria. Si un día hay más tiempo, se avanza a la siguiente sesión; si se pierde uno, se recupera el fin de semana.

**Reglas**
- Los notebooks no incluyen soluciones: el alumno escribe todo su código.
- Solo datasets propios, generados en el notebook o públicos con licencia abierta; nunca material de cursos de terceros.

---

## 1. Formato de cada notebook (instrucciones para generarlo)

- Google Colab, todo en español, Python directo (sin comparaciones con otros lenguajes).
- Duración objetivo: 60 min. Un notebook por sesión: `S01_python_fundamentos.ipynb`, `S02_...`.
- Sin soluciones en ningún archivo.

**Estructura fija**

1. **Encabezado:** título, objetivos (3–5), duración estimada y qué debes saber antes.
2. **Celda de setup:** imports y funciones verificadoras (`check_ejercicio_X`). Van al inicio, con un aviso de "ejecuta y no la edites".
3. **Bloques repetidos por cada concepto:**
   - 📘 **Concepto:** explicación corta con un ejemplo que se ejecuta.
   - ✍️ **Tu turno:** celda con `# Tu código aquí` e instrucción precisa.
   - ✅ **Verificar:** llama al verificador. Muestra ✅ o ❌ con el motivo ("el resultado tiene 3 elementos, se esperaban 5"), sin revelar la respuesta. Prueba también casos borde (listas o arrays vacíos, negativos, ceros).
   - 💡 **Pista:** celda Markdown con `<details>` plegable; una o dos pistas graduales.
4. 🏋️ **Reto final de la sesión:** combina todo lo visto, con verificador.
5. 🚀 **Nivel pro** (opcional): uno o dos extras para quien va sobrado.
6. 🧱 **Avance del proyecto** (cuando aplique): qué agregar al proyecto, por qué lo haría un analista y cómo debe verse el resultado. Sin código.
7. **Cierre:** checklist de autoevaluación ("puedo explicar la diferencia entre...").

**Datos de práctica:** ventas de tiendas (conceptos), movimientos bancarios (aplicación) y los datasets del proyecto. Datos pequeños y generados en el propio notebook con semilla fija, salvo cuando se practica cargar archivos.

---

## 2. Mapa general

| Módulo | Sesiones | Fechas objetivo | Hito del proyecto |
|---|---|---|---|
| 1. Python | S01–S03 | 25/9 – 27/9 | — |
| 2. NumPy | S04–S08 | 28/9 – 3/10 | P0 y P1 |
| 3. Pandas | S09–S13 | 4/10 – 9/10 | P2 (parte 1) |
| 4. Matplotlib | S14–S16 | 10/10 – 12/10 | P2 completo → **Post 1** |
| 5. Machine Learning | S17–S22 | 13/10 – ~28/10 | P3 → **Post 2** |
| 6. Negocio y extras | S23–S27 | noviembre | P4 → **Post 3 + GitHub** |

---

## 3. Sesiones

### Módulo 1: Python

**S01 · Fundamentos (vie 25/9)**
- Colab: celdas de código y de texto, ejecutar, comentarios y cómo leer un error.
- `print`, variables, asignación y reasignación.
- Tipos `int`, `float`, `str`, `bool`; `type()`; conversión entre tipos.
- Operadores `+ - * / // % **`, precedencia, y `//` y `%` con números negativos.
- Strings: índices, slicing, `len`, `.upper()`, `.lower()`, `.strip()`, `.split()`, `.replace()` y f-strings.

**S02 · Colecciones y control de flujo (sáb 26/9)**
- Listas: índices, slicing, `append`, `remove`, `pop`, `in`, `len`, `sum`, `max`, `min`, `sorted` y listas 2D.
- Tuplas y unpacking.
- Diccionarios: acceso, `.get()`, agregar, `del`, `.keys()`, `.values()` e `.items()`.
- `if`/`elif`/`else`, comparadores y `and`/`or`/`not`.
- `for` con `range`, sobre listas, `enumerate` y `zip`; `while`, `break` y `continue`.

**S03 · Funciones y Python moderno (dom 27/9)**
- `def` y `return`; parámetros posicionales, por nombre y por defecto; varios valores de retorno; alcance de variables.
- Escribir funciones que resistan casos borde: entradas vacías, negativas o sin coincidencias.
- `import`, alias, `from ... import` y el módulo `math`.
- List comprehension, incluida la versión con filtro; expresión condicional; `lambda`; `sorted(key=...)`; `map` y `filter`.
- `try`/`except` básico.

### Módulo 2: NumPy

**S04 · El ndarray (lun 28/9)**
- Diferencias entre lista y ndarray; `np.array`; `shape`, `ndim`, `size`, `dtype`; `.tolist()`.
- Crear arrays: `zeros`, `ones`, `arange`, `linspace`.
- Ufuncs aritméticas y matemáticas (`sqrt`, `exp`, `log`, `log1p`, `round`); división por cero, `inf` y `nan`.
- Comparaciones elemento a elemento; broadcasting con escalares; `concatenate`.
- Agregación: `sum`, `mean`, `median`, `min`, `max`, `std`, `argmin`, `argmax`.

**S05 · Indexing y filtrado en 1D (mar 29/9)**
- Índices positivos y negativos; lista de índices; slicing `start:end:step`; invertir un array.
- Indexing booleano; combinar condiciones con `&`, `|`, `~` y la importancia de los paréntesis.
- Contar con `np.sum(mascara)`; `np.any`, `np.all`, `np.where`.
- Casos borde: resultado vacío, negativos con `%`, tipo del resultado.

**S06 · Arrays 2D y `axis` (mié 30/9)**
- Crear arrays 2D, `reshape` (con `-1`), transpuesta.
- Operaciones y broadcasting 2D: fila contra matriz, columna `(n, 1)` contra matriz.
- `axis=0` y `axis=1` en agregaciones; `keepdims`.
- Estandarización (z-score) por columna.

**S07 · Indexing 2D y datos reales (vie 2/10)**
- `a[i, j]`, filas, columnas, slicing 2D, fancy indexing, `np.ix_`.
- Filtrar filas según la condición de una columna.
- Datos sucios: valores centinela, conversión a `nan`, `np.isnan`, `nanmean` y demás funciones `nan*`.
- Cargar archivos con `np.loadtxt` y `np.genfromtxt`.
- `np.unique` (con conteos), `sort`, `argsort`.
- 🧱 **P0 y P1** (ver sección 4).

**S08 · Aleatorios, álgebra lineal y jefe final (sáb 3/10)**
- `np.random`: `default_rng`, semillas, `rand`/`random`, `normal`, `integers`, muestreo.
- Producto punto, `@`, norma, `np.linalg` básico.
- Vectorización frente a bucles, midiendo con `%timeit`.
- Reto integrador: analizar de principio a fin un dataset simulado de ventas usando solo NumPy.

### Módulo 3: Pandas

**S09 · Series y DataFrame (dom 4/10)**
- `Series` y `DataFrame`; `read_csv` (con `sep`); `head`, `info`, `describe`, `shape`, `dtypes`.
- Seleccionar columnas; `loc` e `iloc`; filtros booleanos; `query`.
- 🧱 P2: cargar el dataset del proyecto con pandas.

**S10 · Limpieza (lun 5/10)**
- Nulos: `isna`, `fillna`, `dropna`; valores tipo "unknown" y valores centinela.
- Duplicados; `astype`; métodos `.str`; renombrar columnas.
- Crear columnas; `map`, `apply`, `np.where`; `pd.cut` y `pd.qcut` para rangos.

**S11 · Agrupar y resumir (mar 6/10)**
- `groupby` con `agg`; `value_counts(normalize=True)`; `crosstab`; `pivot_table`.
- Tasas de conversión por segmento; `sort_values`, `nlargest`.

**S12 · Combinar y fechas (mié 7/10)**
- `merge`, `concat`, tipos de join.
- `to_datetime`, accessor `.dt`, `resample` básico.
- Method chaining (encadenar operaciones de forma legible).

**S13 · Integrador pandas (vie 9/10)**
- Mini-caso de principio a fin con datos bancarios de práctica.
- 🧱 P2: limpieza y tablas de análisis del proyecto.

### Módulo 4: Matplotlib

**S14 · Anatomía de un gráfico (sáb 10/10)**
- `fig` y `ax`; `plot`, `bar`, `barh`, `hist`, `scatter`, `boxplot`.
- Títulos, ejes, formato de números y porcentajes.

**S15 · Gráficos que comunican (dom 11/10)**
- `subplots`; graficar desde pandas; anotaciones; color con intención.
- Un gráfico, una conclusión; errores comunes.
- `savefig` con buena resolución. Seaborn como extra.

**S16 · Cierre del EDA (lun 12/10)**
- 🧱 P2 completo: 4–6 gráficos con conclusiones de negocio.
- 📣 **Post 1.**

### Módulo 5: Machine Learning (1–2 días por sesión)

**S17 · Fundamentos de ML**
- Qué es aprendizaje supervisado; `train_test_split`; la API de scikit-learn (`fit`, `predict`); regresión lineal; baseline.

**S18 · Clasificación**
- Regresión logística, árbol de decisión, KNN; probabilidades y umbral.

**S19 · Evaluación**
- Accuracy y por qué engaña con clases desbalanceadas; matriz de confusión; precision, recall, F1; ROC-AUC; validación cruzada.

**S20 · Modelos más fuertes**
- Overfitting; hiperparámetros; `GridSearchCV`; Random Forest; gradient boosting (LightGBM).

**S21 · Feature engineering**
- One-hot y codificación de categorías; escalado; variables nuevas; **data leakage**.
- `Pipeline` y `ColumnTransformer`.

**S22 · Flujo de competencia**
- Validación honesta; leaderboard público vs. privado; archivo de envío; registro de experimentos.
- 🧱 **P3** → 📣 **Post 2.**

### Módulo 6: Negocio y extras (noviembre)

**S23 · Marketing analytics**
- Embudo, conversión, lift, segmentación RFM, ROI de campaña y supuestos explícitos.

**S24 · Aprendizaje no supervisado**
- K-means, escalado, cómo elegir k (codo, silueta), PCA, interpretar segmentos.

**S25 · SQL desde Python**
- `sqlite3` + `pd.read_sql`; `JOIN`, `GROUP BY`, `HAVING`, CTEs, funciones de ventana.

**S26 · Series de tiempo**
- Índice temporal, `resample`, `rolling`, estacionalidad, descomposición y pronóstico básico.

**S27 · Comunicar resultados**
- Estructura de una propuesta de negocio, slides para decisores, notebook limpio y referencias.
- Prepara la presentación final del proyecto.
- 🧱 **P4** (incluye dashboard en Power BI) → 📣 **Post 3 + repositorio final.**

---

## 4. Proyecto: el sistema financiero peruano visto por sus consumidores

> Título provisional. Proyecto principal con **datos abiertos peruanos del sector financiero**, varias fuentes cruzadas y cierre con **dashboard en Power BI**.

**Por qué este enfoque**
- Diferencia frente a los datasets de siempre (Titanic, Bank Marketing, Iris).
- Habla el idioma de los empleadores objetivo: bancos, retail y consumo masivo en Perú.
- Demuestra el trabajo real de un analista: datos sucios, varios archivos, unificar, cruzar fuentes y convertirlo en recomendaciones.

### Fuentes candidatas (se evalúan en P0)

| Candidato | Fuente | Rol en el proyecto | Qué verificar |
|---|---|---|---|
| Denuncias de consumidores en materia financiera, de seguros y pensiones (INDECOPI) | PNDA, un xlsx por año, licencia Open Data Commons Attribution | Núcleo: entidades, productos, motivos y regiones | Años disponibles, columnas, consistencia entre años |
| Expedientes resueltos de protección al consumidor (INDECOPI) | PNDA | Variable a predecir (resultado del caso) para ML | Si incluye el resultado y el sector |
| Series del BCRP (crédito, tasas, tipo de cambio) | BCRPData | Contexto macro y módulo de series de tiempo | Frecuencia y periodo |
| Estadísticas de la SBS (clientes y créditos por entidad) | SBS | Normalizar denuncias por tamaño de la entidad | Formato y periodos |

**Criterios para elegir en P0:** años recientes, columnas suficientes, una llave para cruzar fuentes (entidad, año, región), licencia que permita reutilizar y tamaño manejable en Colab.

**Datos personales:** si algún archivo trae información que identifique a personas, se elimina en la limpieza y nunca se publica.

### Preguntas de negocio (borrador, se ajustan tras P0)
1. ¿Qué entidades y productos (tarjetas, préstamos, seguros) concentran más denuncias, y cómo evolucionan en el tiempo?
2. **Ajustado por tamaño** (clientes o créditos), ¿qué entidades tienen más denuncias relativas? La cifra bruta engaña: la entidad más grande siempre tiene más denuncias. Normalizar demuestra criterio.
3. ¿Qué motivos se repiten más y en qué regiones?
4. ¿El crecimiento de las denuncias acompaña al crecimiento del crédito?
5. ¿Qué factores anticipan que un caso se resuelva a favor del consumidor? (ML, si el dato existe)
6. Si fueras analista de un banco: ¿dónde atacar primero para reducir reclamos y con qué impacto estimado, bajo supuestos explícitos?

### Hitos

| Hito | Sesión | Qué se construye | Pregunta |
|---|---|---|---|
| P0 | S07 (2/10) | Evaluar 2–3 candidatos y elegir; repo en GitHub; README borrador; instrucciones de descarga; diccionario de datos | — |
| P1 | S07–S08 | Primer vistazo con NumPy: rangos, conteos, faltantes y valores centinela en columnas numéricas | — |
| P2 | S09–S16 | Unificar archivos por año, normalizar nombres de entidades, cruzar con BCRP/SBS, tablas y 4–6 gráficos con conclusiones → 📣 Post 1 | 1–4 |
| P3 | S17–S22 | Modelo con variable del proyecto (o respaldo, ver abajo), evaluación correcta y sin leakage → 📣 Post 2 | 5 |
| P4 | S23–S27 | Base SQL con las tablas limpias; segmentación; dashboard en Power BI; recomendaciones → 📣 Post 3 + repo final | 6 |

### Estructura del repositorio (nombre provisional)
```
peru-reclamos-financieros/
├── README.md              # problema, hallazgos, cómo reproducir, fuentes y licencias
├── data/                  # instrucciones de descarga (no subir archivos pesados)
├── notebooks/
│   ├── 01_evaluacion_fuentes.ipynb
│   ├── 02_limpieza_unificacion.ipynb
│   ├── 03_eda_visualizacion.ipynb
│   ├── 04_modelo.ipynb
│   └── 05_sql.ipynb
├── dashboard/             # archivo .pbix y capturas
└── reports/figures/       # gráficos para posts y README
```

### Respaldo para el módulo de ML: Bank Marketing
Solo si ningún dataset peruano tiene una buena variable a predecir.
- UCI Machine Learning Repository (id 222), `bank-additional-full.csv` (41 188 filas, separador `;`). Objetivo: predecir si el cliente contrata un depósito a plazo (`y`).
- Clases desbalanceadas (~11% "yes"). La variable `duration` es **leakage** (solo se conoce después de la llamada) y se excluye.
- Cita: Moro, S., Rita, P., & Cortez, P. (2014). *Bank Marketing* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5K306

### Publicaciones
- Post 1 (~13/10): hallazgos del análisis exploratorio, con 2–3 gráficos.
- Post 2 (~fin de octubre): el modelo, cómo se evaluó y qué aporta al negocio.
- Post 3 + repo (~mediados de noviembre): dashboard y recomendaciones.
- Todo el contenido es propio, con fuentes citadas y sin material de terceros.

---

## 5. Progreso

| Sesión | Fecha objetivo | Hecha | Notas |
|---|---|---|---|
| S01 | 25/9 | ☐ | |
| S02 | 26/9 | ☐ | |
| S03 | 27/9 | ☐ | |
| S04 | 28/9 | ☐ | |
| S05 | 29/9 | ☐ | |
| S06 | 30/9 | ☐ | |
| S07 | 2/10 | ☐ | P0 (elegir dataset), P1 |
| S08 | 3/10 | ☐ | |
| S09 | 4/10 | ☐ | |
| S10 | 5/10 | ☐ | |
| S11 | 6/10 | ☐ | |
| S12 | 7/10 | ☐ | |
| S13 | 9/10 | ☐ | |
| S14 | 10/10 | ☐ | |
| S15 | 11/10 | ☐ | |
| S16 | 12/10 | ☐ | Post 1 |
| S17–S22 | 13/10 – 28/10 | ☐ | Post 2 |
| S23–S27 | noviembre | ☐ | Post 3 |
