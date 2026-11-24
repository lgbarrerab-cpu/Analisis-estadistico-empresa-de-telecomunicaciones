# Análisis ConnectaTel

## Objetivo del proyecto

Como analista de datos, el objetivo de este proyecto es evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, usando información registrada hasta el año 2024. El análisis busca construir un perfil estadístico de los clientes, detectar comportamientos atípicos, crear segmentos de clientes e identificar patrones de consumo que permitan diseñar estrategias de retención y sugerir mejoras en los planes ofrecidos.

## Datasets utilizados

- **`plans.csv`** — información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
- **`users_latam.csv`** — información de los clientes (edad, ciudad, fecha de registro, plan, churn).
- **`usage.csv`** — detalle del uso real de los servicios (llamadas y mensajes).

Los archivos originales no se incluyen en este repositorio; deben ubicarse en una carpeta `datasets/` en la raíz del proyecto para que el notebook los cargue correctamente (ver sección de reproducción).

## Etapas del análisis

1. **Cargar y explorar** — carga de los tres datasets y revisión inicial de su estructura, columnas y tipos de datos.
2. **Identificación de problemas de calidad de datos** — detección de valores faltantes, valores inválidos/sentinels e inconsistencias en fechas.
3. **Limpieza básica de datos** — corrección de sentinels y fechas imposibles, tratamiento de valores faltantes según su naturaleza y proporción.
4. **Summary statistics de uso por usuario** — resumen estadístico del uso (llamadas y mensajes) por usuario durante 2024.
5. **Visualización de distribuciones y outliers** — histogramas/boxplots del uso y detección de clientes con comportamiento atípico.
6. **Segmentación de clientes** — segmentación por edad y por nivel de uso, con visualización de los segmentos resultantes.
7. **Insight ejecutivo para stakeholders** — resumen ejecutivo con hallazgos clave y recomendaciones de negocio (planes premium para alto uso, retención de bajo uso, segmentación edad-uso, investigación de outliers, campañas de win-back).
8. **Documentación y versionado en GitHub** — carga del notebook y este README al repositorio.

## Cómo ejecutar el notebook

### Opción A: Jupyter local

1. Clona este repositorio.
2. Crea una carpeta `datasets/` en la raíz y coloca ahí `plans.csv`, `users_latam.csv` y `usage.csv`.
3. Instala las dependencias:
   ```bash
   pip install pandas seaborn matplotlib jupyter
   ```
4. Abre el notebook:
   ```bash
   jupyter notebook "S7 Version-Estudiante-Project-ConnectaTel.ipynb"
   ```
5. Ejecuta las celdas en orden (Kernel → Restart & Run All).

### Opción B: Google Colab

1. Sube el notebook a Colab (`Archivo → Abrir notebook → GitHub`, pegando la URL del repositorio) o desde `Archivo → Subir notebook`.
2. Sube los tres archivos CSV a la carpeta `/datasets` del entorno de Colab, o móntalos desde Google Drive ajustando las rutas de carga.
3. Ejecuta todas las celdas en orden.

## Guía de reproducción

- El notebook está diseñado para ejecutarse de principio a fin sin intervención manual, siempre que los tres CSV estén disponibles en `/datasets`.
- Las rutas de carga usadas en el notebook son:
  - `/datasets/plans.csv`
  - `/datasets/users_latam.csv`
  - `/datasets/usage.csv`
- Librerías requeridas: `pandas`, `seaborn`, `matplotlib`.
- No se requiere ningún paso de configuración adicional (credenciales, API keys, etc.).

## Estructura del repositorio

```
.
├── README.md
├── requirements.txt
└── S7 Version-Estudiante-Project-ConnectaTel.ipynb
```

La carpeta `datasets/` (con `plans.csv`, `users_latam.csv` y `usage.csv`) no se incluye en el repositorio; debe crearse localmente como se explica arriba.

## Autor

**Luis Guillermo Barrera Barrios** · Data Analyst  
📧 Lgbarrerab@gmail.com · [LinkedIn](https://www.linkedin.com/in/luis-guillermo-barrera-barrios-64aa5790) · [Portafolio](https://lgbarrerab-cpu.github.io)
