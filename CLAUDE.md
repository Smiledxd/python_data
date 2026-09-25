# CLAUDE.md — Estudio de Python para análisis de datos

## Contexto
Carpeta de estudio personal de un alumno que aprende Python y análisis de datos desde cero.
El plan completo está en `curricula_data.md` (en esta misma carpeta). Léelo siempre antes de generar una sesión.

## Estructura
```
estudio-python/
├── CLAUDE.md
├── curricula_data.md
└── sesiones/          # un notebook por sesión: S01_python_fundamentos.ipynb, S02_...
```

## Tarea típica
"Genera la sesión N" → crear `sesiones/SNN_tema_corto.ipynb` según:
- la sección **1. Formato de cada notebook** de la currícula, y
- la entrada de la sesión N en la sección **3. Sesiones**.

## Reglas obligatorias
1. **Sin soluciones.** Ningún archivo, celda, comentario ni commit puede contener la respuesta de un ejercicio.
2. **Verificadores que no revelan la respuesta.**
   - Van en una celda de setup al inicio, oculta con `#@title` y vista de formulario de Colab.
   - Validan por propiedades (tipo, forma, longitud, rango) o recalculando el resultado con un método distinto al que se espera que use el alumno. Si hay que comparar contra un valor fijo, se compara contra un hash, nunca contra el valor en texto plano.
   - Mensajes en español: ✅ si está bien, ❌ con el motivo concreto ("se esperaban 5 elementos y hay 3"), sin mostrar la respuesta.
   - Cuando aplique, prueban casos borde: vacíos, negativos, ceros, sin coincidencias.
3. **Idioma y estilo.** Todo en español, Python directo, sin comparaciones con otros lenguajes. Explicaciones cortas y ejemplos que se ejecutan.
4. **Datos.** Generados en el propio notebook con semilla fija (`np.random.default_rng(42)`), sobre ventas de tiendas o movimientos bancarios. Si una sesión requiere descargar datos, usa una URL estable e indica la fuente y la licencia.
5. **Nada de terceros.** No incluir material, código, datos ni enunciados de cursos externos.
6. **Nunca resolver tareas calificadas.** Si una petición parece una tarea o examen de un curso, detente y avisa.
7. **Duración:** unos 60 minutos para un principiante.

## Validación antes de hacer commit
1. Si faltan `jupyter`, `nbconvert`, `numpy`, `pandas` o `matplotlib` en tu entorno, instálalos solo para validar. No agregues archivos de entorno al repo.
2. Crea en `/tmp` (fuera del repo) un notebook de prueba con respuestas de referencia y ejecútalo con `jupyter nbconvert --to notebook --execute` para confirmar que:
   - todos los verificadores dan ✅ con respuestas correctas,
   - dan ❌ con al menos un error típico por ejercicio,
   - no hay celdas que fallen al ejecutarse en orden.
3. Borra el notebook de prueba. No lo commitees.
4. Guarda el notebook final **sin outputs**.
5. Agrega arriba del notebook un enlace "Abrir en Colab" que apunte al archivo en este repo (`https://colab.research.google.com/github/USUARIO/REPO/blob/main/RUTA`).

## Al terminar
- Commit con mensaje `Sesión N: tema` y push a `main`.
- Responde con un resumen de 3 líneas: qué cubre, cuántos ejercicios tiene y si hay bloque de proyecto.
