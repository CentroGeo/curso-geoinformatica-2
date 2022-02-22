# [Geoinformática](https://centrogeo.github.io/curso-geoinformatica-2/)

Este curso es una introducción a las principales herramientas de Python para en Análisis Espacial, está pensado como una primera aproximación y se centra en el uso de las herramientas más que en los conceptos de análisis.

El curso busca dar a los estudiantes un entendimiento intuitivo de las posibilidades, limitaciones y capacidades de las herramientas geoinformáticas y su aplicación en el Análisis Espacial, sin detallar extensivamente en el transfondo matemático de los métodos estudiados. En este sentido, el curso asume que los estudiantes cuentan con nociones básicas de programación y estadística y, preferentemente, de Análisis Espacial.co para poder estudiarlo.

Los temas elegidos fueron escogidos para brindar a los estudiantes de un panorama  amplio, mas no completo, de las herramientas, tanto tecnológicas como matemáticas de la geoinformática. La idea es que, aún si no se conocen todas las técnicas y métodos existentes, los estudiantes adquieran la formación necesaria para entender los conceptos básicos, el funcionamiento general de las herramientas computacionales y sean capaces de adaptarlos a sus propios proyectos. De esta forma el curso busca establecer una base para que, en un futuro, los estudiantes investiguen más a profundidad los temas que se relacionen con sus intereses particulares.

## Organización del Curso
El curso se encuentra organizado como un conjunto de talleres. En cada taller se revisarán algunas ideas detrás del análisis de datos geoespaciales con énfasis en las herramientas y técnicas computacionales. Cada taller es un Notebook de Jupyter que contiene todo el código necesario y las explicaciones básicas. El curso está pensado para funcionar de forma presencial y síncrona, sin embargo también es posible seguir el material de forma autónoma. Además de talleres con ejemplos generales del uso de las herramientas, también hay talleres dedicados a desarrollar ejemplos específicos de análisis para entender problemas reales, estos talleres toman como ejemplo la epidemia de COVID-19 en México.

### Parte 1. Introducción al manejo de datos en Python
Las primeras prácticas pretenden ser simplemente una introducción a la visualización, interpretación y manipulación de los Datos Espaciales:
* [Transformación de Datos](./01_transformacion/01_transformacion_original.html). Introducción al manejo de Pandas para transformar datos
* [Manejando los datos abiertos de COVID-19](./01_transformacion/01_transformacion.html). Descripción de la base de datos y su uso básico
* [Automatizando la transformación de datos](./01_transformacion/02_transformacion.html). Definiendo funciones para automatizar las transformaciones
* [Curvas epidémicas](./02_geovisualizacion/02_visualizacion.html). Visualizando la evolución de la epidemia
* [Ejemplo de COVID por grupos de edad](./02_geovisualizacion/03_Covid_grupos-de-edad.html). Analizando el impacto para diferentes grupos de edad
* [Introducción a GeoPandas](./02_geovisualizacion/02_geovisualizacion.html). Elementos básicos para usar objetos geográficos en Python
* [Mapas de COVID](./02_geovisualizacion/mapas.html)

### Parte 2. Elementos de Ánálisis Espacial
El siguiente conjunto de prácticas ahonda en conceptos básicos del Análisis Espacial, principalmente relacionados con conceptos estadísticos y la visualización e interpretación de la información espacial obtenida:
* [Pesos Espaciales y Rezago Espacial](./04_pesosespaciales/04_pesosespaciales.html)
* [Autocorrelación y Análisis Exploratorio de Datos Espaciales (ESDA)](./05_autocorrelacion/05_autocorrelacion.html)
* [Caso de Estudio: Análisis Espacial del COVID](./05_autocorrelacion/Asociacion_local.html)
* [Agrupamiento y Regionalizacíon](./06_regionalizacion/06_intro.html)
* [Patrones de Puntos](./07_patrones/07_patrones.html)

Posteriormente, se analizan problemáticas asociadas al Análisis Espacial, especficamente, particularidades a tomar en cuenta al manejar información espacial:
* [Problema de la Unidad de Área Modificable (MUAP)](./08_muap/08_muap.html)

También se estudian modelos propuestos por diversos especialistas en la materia, y su implementación a través de Python, que resultan de utilidad al momento de abarcar problemáticas en las que se encuentra involucrada la componente espacial:
* [Difusión Espacial - Modelo de Hägerstrand](./09_difusionespacial/09_intro.html)

## Preparación para el Curso
En primer lugar, es necesario tener una computadora actualizada con la versión más reciente de Python. Para el caso de Windows y MacOS, puede ser descargada a través de la [página oficial de *Python*](https://www.python.org/downloads/); en el caso de Linux, basta con correr en la terminal el siguiente comando:
```
sudo apt-get update && sudo apt-get upgrade
```
Una vez instalado Python, resulta útil instalar un complemento llamado *Conda*, el cual permitirá instalar, actualizar y manejar las librerías existentes para Python de forma más rápida y sencilla; especficamente, la versión de este complemento llamada *Miniconda*. La información para descargar este complemento se encuentra en la [documentación oficial de *Conda*](https://docs.conda.io/en/latest/miniconda.html).

Asimismo, resulta útil crear lo que dentro de *Python* se conoce como [*Virtual Environment*](https://www.geeksforgeeks.org/python-virtual-environment/), esto es, un espacio dentro de la computadora diseñado específicamente para trabajar sobre un proyecto en específico. Esto se puede realizar rápidamente [utilizando *Conda*](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html); una vez instalado, basta con correr el siguiente comando, sustituyendo `nombre` por el nombre con el que uno desee trabajar:
```
conda create --name nombre
```
Y, para utilizar este espacio, debe de ejecutarse el comando:
```
conda activate nombre
```
Una vez activado el espacio a utilizar, deben de instalarse todas las librerías de Python a utilizar durante el curso. A continuación, se listan las librerías pertinentes:
* `jupyter`
* `pandas`
* `seaborn`
* `matplotlib`
* `geopandas`
* `pysal`
* `palettable`
* `numpy`
* `scikit-learn`
* `ipywidgets`
* `mapclassify`
* `scikit-image`
* `future`
* `jsanimation`
* `mplleaflet`

Todas pueden ser instaladas al mismo tiempo a través de los comandos:
```
conda install jupyter pandas seaborn matplotlib geopandas pysal palettable numpy scikit-learn ipywidgets mapclassify scikit-image future
conda install -c conda-forge jsanimation
conda install -c ioos mplleaflet
```
O, si es necesario instalar sólo una de ellas, puede ejecutarse el siguiente comando, sustituyendo `libreria` por el nombre de la librería que se pretende instalar:
```
conda install libreria
```
Finalmente, todas las prácticas pueden ser visualizadas en web gracias al archivo `.html` presente en el repositorio; sin embargo, en éste también puede ser encontrado archivos del tipo `.ipynb`, los cuales permiten ejecutar los comandos de la práctica activamente; éstos son visualizados utilizando el complemento `jupyter-notebook` instalado anteriormente, y el cual puede ser activado simplemente ejecutando el comando:
```
jupyter-notebook
```

## Referencias
* Algunas prácticas fueron adaptadas del curso impartido por el [Dr. Dani Arribas](http://darribas.org/), docente de la Universidad de Liverpool, durante la segunda mitad del 2016, el cual puede ser encontrado [en su página oficial](http://darribas.org/gds16/).
* El libro *Python for Data Analysis: Data Wrangling with Pandas, NumPy and IPython* del autor William McKinney es una excelente introducción al manejo de datos en Python, ofreciendo múltiples ejemplos y comandos útiles ([Información](http://shop.oreilly.com/product/0636920023784.do))
