# Análisis de la Demanda Energética en la Industria Manufacturera de Productos Alimenticios

## Descripción

Este proyecto tiene como objetivo realizar un análisis exhaustivo de la demanda energética en el sector de la industria manufacturera de productos alimenticios. Utilizando datos obtenidos de la API de XM sobre la demanda energética comercial no regulada, se realiza un proceso de agregación, transformación y visualización para identificar patrones y comportamientos clave en la demanda energética a lo largo del tiempo y por código CIIU.

El análisis incluye la exploración de la demanda energética por hora, la distribución porcentual por código CIIU, y el comportamiento mensual y semanal de la demanda. Las visualizaciones generadas permiten una mejor interpretación de los datos y proporcionan información útil para la toma de decisiones estratégicas en el sector energético y productivo.

## Tecnologías Utilizadas

- **Python**: Lenguaje de programación utilizado para el análisis de los datos y la generación de las visualizaciones.
- **Pandas**: Biblioteca para la manipulación de datos y agregación.
- **Matplotlib y Seaborn**: Librerías para la creación de visualizaciones.
- **PyDataXM**: Librería utilizada para la conexión y consulta de datos desde la API de XM.
- **Jupyter Notebook**: Entorno utilizado para desarrollar y documentar el análisis de manera interactiva.

## Descripción del Proceso

El análisis se desarrolló en varias etapas clave:

1. **Conexión a la API de XM**: Se estableció una conexión a la API de XM utilizando la librería `pydataxm` para obtener los datos históricos de la demanda energética en la industria alimentaria.

2. **Selección de los Códigos CIIU Relevantes**: Se filtraron los datos para obtener solo aquellos que corresponden a los códigos CIIU relacionados con la industria manufacturera alimentaria, lo cual se definió previamente en un listado específico.

3. **Transformación y Agregación de los Datos**: Los datos fueron transformados y agrupados por fecha y código CIIU. Se sumaron las demandas horarias para obtener un valor total de demanda diaria y se calcularon métricas adicionales como promedios semanales y porcentajes de distribución por código CIIU.

4. **Cálculo de Métricas**: Se calcularon métricas clave como la demanda promedio por hora, la demanda total por mes y la distribución porcentual de la demanda por cada código CIIU.

5. **Visualización de los Resultados**: Se generaron varias visualizaciones interactivas y estáticas para facilitar la interpretación de los datos:
   - **Comportamiento de la demanda por hora**: Gráfico de líneas que muestra cómo varía la demanda energética durante el día.
   - **Distribución porcentual de la demanda por código CIIU**: Gráfico de barras horizontales que presenta la proporción de demanda correspondiente a cada sector de la industria.
   - **Mapa de calor de la demanda energética por mes**: Visualización de cómo la demanda varía a lo largo de los meses para cada código CIIU.
   - **Demanda mensual y por día de la semana**: Gráfico de barras que muestra la demanda total mensual y los porcentajes correspondientes.
   - **Promedio de demanda energética por día de la semana**: Gráfico de barras que presenta el promedio de la demanda energética para cada día de la semana.

6. **Creación del Diccionario de la Industria Alimentaria**: Se creó un diccionario con los códigos CIIU y sus respectivas descripciones para facilitar la interpretación de los datos.

## Requisitos

Para ejecutar este proyecto, se deben tener instaladas las siguientes dependencias:

- `pandas`
- `matplotlib`
- `seaborn`
- `pydataxm`
- `jupyter`
- `numpy`

## Uso

### Clonar el Repositorio
Para obtener el proyecto, clona este repositorio en tu máquina local:

```bash
git clone https://github.com/S00LEY/Talento-B_-Ing-Data.git
```
### Abrir el Proyecto
Navega a la carpeta del proyecto y abre el archivo Jupyter Notebook:

```bash
cd Talento-B_-Ing-Data
- DemaComeNoReg_CIIU_Alimentos_2024.ipynb
```
### Ejecutar el Análisis
Una vez dentro del notebook, puedes ejecutar las celdas de código para obtener los resultados del análisis, desde la conexión con la API hasta la visualización de los resultados.

 _Nota: Para ejecutar los cuadernos de Jupyter, asegúrate de tener instalado Jupyter en tu entorno. Si no lo tienes, puedes instalarlo ejecutando el siguiente comando:_

```bash
pip install jupyter
```
