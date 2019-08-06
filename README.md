# [Geoinformática](https://centrogeo.github.io/curso-geoinformatica-2/)

El objetivo del curso es revisar algunos de los conceptos más importantes relacionados con el Análisis Espacial, utilizando las herramientas proporcionadas por el lenguaje de programación *[Python](https://en.wikipedia.org/wiki/Python_(programming_language))* y sus múltiples librerías.

El curso pretende dar a los estudiantes un entendimiento intuitivo de las posibilidades, limitaciones y capacidades de las herramientas geoinformáticas y su aplicación en el Análisis Espacial, sin detallar extensivamente en el transfondo matemático de los métodos estudiados; como tal, aunque resulta ventajoso haber estudiado los principios básicos de matemáticas, estadística y programación antes de iniciar con el curso, éste se encuentra diseñado de forma que no sea necesario ningún tipo de perfil en específico para poder estudiarlo.

Los temas elegidos fueron escogidos a modo de brindar a los estudiantes de un catálogo extenso, mas no completo, de muchas de las herramientas, tanto tecnológicas como matemáticas, que la Geoinformática aporta al Análisis Espacial, bajo la idea de que, aún si no se conocen todas las técnicas y métodos existentes, los estudiantes adquieran la formación necesaria para entender los conceptos básicos del Análisis Espacial, entender el funcionamiento general de sus procesos y ser capaces de adaptarlos en sus propios proyectos, así como establecer una base sólida para que, en un futuro, los estudiantes investiguen más a profundidad los temas que se relacionen con sus intereses particulares.

## Organización del Curso
El curso se encuentra organizado como un conjunto de prácticas, cada una puntualizando en algún aspecto en particular del Análisis Espacial, así como introduciendo las librerías de *Python* que permiten ejecutar dicho análisis. Cada práctica contiene algo de teoría que explica el tema a desarrollar, las líneas de código que permiten desarrollarla y la explicación detrás de cada uno de los comandos.

Las primeras prácticas pretenden ser simplemente una introducción a la visualización, interpretación y manipulación de los Datos Espaciales:
* [Transformación de los Datos](./01_transformacion/01_transformacion.html)
* [Geovisualización](./02_geovisualizacion/02_geovisualizacion.html)

El siguiente conjunto de prácticas ahonda en conceptos básicos del Análisis Espacial, principalmente relacionados con conceptos estadísticos y la visualización e interpretación de la información espacial obtenida:
* [Pesos Espaciales y Rezago Espacial](./04_pesosespaciales/04_pesosespaciales.html)
* [Autocorrelación Espacial y Análisis Exploratorio de Datos](./05_autocorrelacion/05_autocorrelacion.html)
* [Patrones de Puntos](./07_patrones/07_patrones.html)

Posteriormente, se analizan problemáticas asociadas al Análisis Espacial, especficamente, particularidades a tomar en cuenta al manejar información espacial:
* [Problema de la Unidad de Área Modificable (MUAP)](./practica_extra/practica_extra.html)

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
* `mplleaflet`
* `mapclassify`

Todas pueden ser instaladas al mismo tiempo a través del comando:
```
conda install jupyter-notebook pandas seaborn matplotlib geopandas pysal palettable numpy scikit-learn ipywidgets mplleaflet mapclassify
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
