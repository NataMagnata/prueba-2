# Análisis de Recurso Solar y Simulación Fotovoltaica

Este proyecto permite analizar, limpiar y simular datos de recurso solar, así como realizar análisis económico de sensibilidad y visualizar resultados mediante un dashboard interactivo. Está orientado a la evaluación y simulación de proyectos fotovoltaicos en base a datos meteorológicos reales.

---

## Descripción del Proyecto

El objetivo es proporcionar una herramienta integral para el análisis de datos solares, simulación de sistemas fotovoltaicos y evaluación económica, facilitando la toma de decisiones en proyectos de energía solar. El flujo de trabajo abarca desde la revisión y limpieza de datos meteorológicos hasta la visualización interactiva de resultados y análisis de sensibilidad económica.

---

## Cómo ejecutar el código

### 1. Instalar dependencias

Asegúrate de tener Python 3.10+ y pip. Instala todas las dependencias necesarias con:

```bash
pip install -r requirements.txt
```

### 2. Ejecutar los notebooks

Abre Jupyter Notebook en la carpeta del proyecto:

```bash
jupyter notebook
```

Ejecuta los notebooks en el siguiente orden recomendado:
1. `analisis_corruptos.ipynb`  
2. `limpieza.ipynb`  
3. `recurso_solar.ipynb`  
4. `simulacion_pv.ipynb`  
5. `analisis_economia_sensibilidad.ipynb`  
6. `dash.ipynb`  

### 3. Ejecutar el dashboard interactivo (Dash)

Para visualizar el dashboard, puedes ejecutar el notebook `dash.ipynb` o, si tienes un script Dash, ejecutarlo con:

```bash
python dash_app.py
```

Luego abre tu navegador en [http://127.0.0.1:8050](http://127.0.0.1:8050)

---

## Estructura de Carpetas

```
prueba2/
│
├── analisis_corruptos.ipynb
├── limpieza.ipynb
├── recurso_solar.ipynb
├── simulacion_pv.ipynb
├── analisis_economia_sensibilidad.ipynb
├── dash.ipynb
├── requirements.txt
├── calama_corrupted.csv
├── salvador_corrupted.csv
├── Vallenar_corrupted.csv
├── ... (archivos generados: *_clean.csv, *_simulado.csv, imágenes, etc.)
```

---

## Ejemplo de Entrada y Salida

### Entrada
- Archivos CSV de datos meteorológicos horarios, por ejemplo: `calama_corrupted.csv`, `salvador_corrupted.csv`, `Vallenar_corrupted.csv`.

### Salida
- Archivos limpios: `calama_clean.csv`, `salvador_clean.csv`, `Vallenar_clean.csv`
- Archivos simulados: `calama_simulado.csv`, etc. (con columna de producción horaria AC)
- Gráficos de análisis y simulación: PNGs de producción mensual, factor de capacidad, etc.
- Gráfico combinado de producción mensual para los tres sitios: `produccion_mensual_combinada.png`
- Tabla resumen de producción anual: `resumen_produccion_anual.csv` y `resumen_produccion_anual.png`
- **Tablas de resultados económicos:**  
  - `tabla_sensibilidad_lcoe_y_van.csv` (análisis de sensibilidad de LCOE y VAN)  
  - `resumen_lcoe_van.csv` (resumen de LCOE y VAN por sitio)
- Dashboard interactivo accesible vía navegador web

---

## Notebooks incluidos

- **analisis_corruptos.ipynb:** Analiza archivos CSV de recurso solar potencialmente corruptos, revisando valores faltantes, fuera de rango y mostrando estadísticas generales.
- **limpieza.ipynb:** Limpia los datos, reemplazando valores fuera de rango por NaN, interpolando y completando datos faltantes. Genera archivos CSV limpios.
- **recurso_solar.ipynb:** Realiza análisis detallado de los datos limpios, incluyendo visualizaciones y generación de variables útiles para la simulación.
- **simulacion_pv.ipynb:** Simula la producción de energía de un sistema fotovoltaico usando los datos limpios.
- **analisis_economia_sensibilidad.ipynb:** Realiza análisis económico y de sensibilidad, evaluando métricas como LCOE, VAN y periodo de retorno bajo diferentes escenarios.
- **dash.ipynb:** Dashboard interactivo para visualizar datos, resultados de simulación y análisis económico.

---

## Visualizaciones y tablas destacadas

- **produccion_mensual_combinada.png:** Gráfico combinado con la producción mensual de Calama, Salvador y Vallenar en una sola imagen.
- **resumen_produccion_anual.csv / .png:** Tabla resumen con la producción anual de cada sitio.
- **resumen_lcoe_van.csv:** Tabla resumen con LCOE y VAN base por sitio.
- **tabla_sensibilidad_lcoe_y_van.csv:** Tabla de sensibilidad de LCOE y VAN para cada parámetro y sitio.
- Otros gráficos: patrones diarios, comparaciones mensuales, heatmaps horarios, factores de capacidad, etc.
