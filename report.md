# Reporte del Proyecto de Análisis Solar y Simulación Fotovoltaica

## Resumen Ejecutivo

Este proyecto es una herramienta integral para el análisis de datos solares, simulación de sistemas fotovoltaicos y evaluación económica. Está diseñado para facilitar la toma de decisiones en proyectos de energía solar mediante el procesamiento y análisis de datos meteorológicos reales.

## Estructura del Proyecto

### Archivos Principales

1. **Notebooks de Análisis y Procesamiento**
   - `analisis_corruptos.ipynb`: Análisis inicial de datos meteorológicos
   - `limpieza.ipynb`: Limpieza y preprocesamiento de datos
   - `recurso_solar.ipynb`: Análisis detallado del recurso solar
   - `simulacion_pv.ipynb`: Simulación de sistemas fotovoltaicos
   - `analisis_economia_sensibilidad.ipynb`: Análisis económico y de sensibilidad
   - `dash.ipynb`: Dashboard interactivo para visualización

2. **Datos de Entrada**
   - `calama_corrupted.csv`: Datos meteorológicos de Calama
   - `salvador_corrupted.csv`: Datos meteorológicos de Salvador
   - `Vallenar_corrupted.csv`: Datos meteorológicos de Vallenar

3. **Archivos de Configuración**
   - `requirements.txt`: Dependencias del proyecto
   - `README.md`: Documentación principal

### Tecnologías Utilizadas

El proyecto utiliza las siguientes tecnologías principales:
- Python 3.10+
- Jupyter Notebooks
- Dash para visualización interactiva
- Bibliotecas científicas:
  - NumPy y Pandas para análisis de datos
  - Matplotlib y Plotly para visualización
  - PVLib para simulación fotovoltaica
  - PySAM para análisis económico

## Flujo de Trabajo

1. **Análisis Inicial**
   - Revisión de datos meteorológicos
   - Identificación de valores corruptos o faltantes
   - Estadísticas descriptivas

2. **Limpieza de Datos**
   - Interpolación de valores faltantes
   - Corrección de valores fuera de rango
   - Generación de datasets limpios

3. **Análisis de Recurso Solar**
   - Caracterización del recurso solar
   - Visualizaciones temporales
   - Análisis de patrones

4. **Simulación Fotovoltaica**
   - Modelado de sistemas PV
   - Cálculo de producción energética
   - Análisis de rendimiento

5. **Análisis Económico**
   - Cálculo de LCOE
   - Análisis de VAN
   - Estudios de sensibilidad

6. **Visualización**
   - Dashboard interactivo
   - Gráficos comparativos
   - Reportes automatizados

## Resultados Generados

### Archivos de Salida
- Datasets limpios (*_clean.csv)
- Resultados de simulación (*_simulado.csv)
- Visualizaciones (PNG)
- Tablas de resumen (CSV)

### Métricas Principales
- Producción energética anual
- Factor de capacidad
- LCOE y VAN
- Análisis de sensibilidad

## Requisitos Técnicos

### Dependencias Principales
```
dash>=2.14.0
Dash-bootstrap-components>=1.5.0
jupyter>=1.0.0
matplotlib>=3.5.0
numpy>=1.21.0
numpy-financial>=1.0.0
pandas>=1.5.0
plotly>=5.18.0
pvlib>=0.9.0
PySAM>=2.2.0
scipy>=1.7.0
seaborn>=0.11.0
windrose>=1.8.0
```

## Instrucciones de Uso

1. **Instalación**
   ```bash
   pip install -r requirements.txt
   ```

2. **Ejecución**
   - Iniciar Jupyter Notebook
   - Ejecutar notebooks en orden secuencial
   - Acceder al dashboard en http://127.0.0.1:8050

## Conclusiones

Este proyecto proporciona una herramienta completa para:
- Análisis de datos meteorológicos
- Simulación de sistemas fotovoltaicos
- Evaluación económica
- Visualización interactiva de resultados

La estructura modular permite una fácil adaptación y extensión para diferentes casos de uso y ubicaciones geográficas. 