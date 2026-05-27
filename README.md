# Análisis de la estructura del gasto de los hogares españoles mediante la identificación de tipologías de consumo

**Autor:** Hugo Lucendo Romero  
**Tutor:** Inmaculada Gutiérrez García-Pardo  
**Grado:** Estadística Aplicada (Facultad de Estudios Estadísticos), Universidad Complutense de Madrid  
**Fuente de datos:** Encuesta de Presupuestos Familiares 2023, Instituto Nacional de Estadística  

---

## Descripción

Este repositorio recoge el código, los datos de trabajo y las salidas generadas del Trabajo de Fin de Grado.

---

## Estructura del repositorio

La organización del repositorio es la siguiente:

```text
datos_originales/
datos_procesados/
html/
notebook/
pdf/
````

### `datos_originales/`

Contiene los ficheros originales descargados de los microdatos de la EPF 2023 del INE:

```text
EPFgastos_2023.tab
EPFhogar_2023.tab
```

### `datos_procesados/`

Contiene las bases generadas durante el trabajo:

```text
datos_iniciales.csv
datos_con_tipologia_consumo.csv
```

* `datos_iniciales.csv`: base construida después de integrar los ficheros originales de hogares y gastos, con una observación por hogar.
* `datos_con_tipologia_consumo.csv`: base final utilizada en la parte predictiva, incorporando la tipología de consumo obtenida a partir del análisis multivariante y la variable de control que define si la observación pertenece a entrenamiento o a prueba.

### `notebook/`

Contiene los notebooks principales del análisis:

```text
metodologia_datos.ipynb
analisis_multivariante.ipynb
modelos_predictivos.ipynb
```

* `metodologia_datos.ipynb`: carga de los datos originales, limpieza, integración de ficheros, construcción de variables y análisis descriptivo.
* `analisis_multivariante.ipynb`: análisis de componentes principales, selección de dimensiones e identificación de tipologías de consumo mediante cluster.
* `modelos_predictivos.ipynb`: entrenamiento, validación y comparación de modelos predictivos usando como variable objetivo la tipología de consumo.

### `html/`

Contiene una versión HTML de cada notebook.

```text
metodologia_datos.html
analisis_multivariante.html
modelos_predictivos.html
```

### `pdf/`

Contiene una versión PDF de cada notebook.

```text
metodologia_datos.pdf
analisis_multivariante.pdf
modelos_predictivos.pdf
```

---

## Datos

Los datos originales proceden de los microdatos oficiales de la **Encuesta de Presupuestos Familiares 2023**, elaborada por el **Instituto Nacional de Estadística**.

---

## Reproducibilidad

El análisis debe consultarse o ejecutarse en este orden:

```text
1. metodologia_datos.ipynb
2. analisis_multivariante.ipynb
3. modelos_predictivos.ipynb
```

---

## Observaciones

Los microdatos utilizados son datos oficiales anonimizados del INE. Este repositorio tiene una finalidad exclusivamente académica y está asociado al desarrollo del Trabajo de Fin de Grado.

El análisis, las transformaciones y los modelos incluidos en el repositorio deben interpretarse dentro del contexto del trabajo y de sus objetivos: identificar patrones latentes de consumo y estudiar hasta qué punto pueden anticiparse a partir de características del hogar.
