# Python Geología

En este repositorio se realiza un compilado de librerías open-source, utilidades y material de Python gratuito con un enfoque en la geología.

## Contenidos

* [Librerías](#lib)
  * [Carga y manipulación de datos](#carga)
    * [NumPy](#numpy) 
    * [pandas](#pandas) 
  * [Visualización de datos](#viz)
    * [Matplotlib](#matplotlib)
    * [Seaborn](#seaborn)
    * [Plotly](#plotly)
    * [Bokeh](#bokeh)
  * [Mapas e información geoespacial](#mapas)
    * [geopandas](#geopandas)
    * [cartopy](#cartopy)
    * [Folium](#folium)
    * [Plotly](#plotly)
  * [Modelamiento geológico](#modelamiento)
    * [GemPy](#gempy)
    * [Flopy](#flopy)
* [Cursos y tutoriales](#cursos)
* [Libros, blogs y canales de Youtube](#materiales)
* [Utilidades](#utilidades)

## <a id="lib">Librerías</a>
\*El titulo de cada librería lleva a la página oficial correspondiente.

### <a id="carga">Carga y manipulación de datos</a>

#### [NumPy](https://numpy.org/) <a id="numpy"></a>

<img src="https://numpy.org/images/logos/numpy.svg" alt="numpy logo" height="100"/>
NumPy permite el trabajo con matrices y vectores de manera rápida y eficiente. Es una parte clave de numerosas otras librerías dentro del ecosistema de Python, por ejemplo, es el núcleo la librería pandas.
<hr>

#### [pandas](https://pandas.pydata.org/) <a id="pandas"></a> 
<img src="https://pandas.pydata.org/static/img/pandas_white.svg" alt="pandas logo" height="100"/>

Pandas permite la carga, análisis y transformación de información tabular. Con pandas es posible cargar información en forma de CSV, Excel, JSON, GeoJSON entre muchas otros, la que puede ser posteriormente filtrada, clasificada y/o agregada.

```python
import pandas as pd

df = pd.read_csv('https://raw.githubusercontent.com/crvillanueva/python-geologia/main/data/terremotos.csv')
df.head()
```

> 

<hr>

### <a id="viz">Visualización</a>

Python posee numerosas librerías para la visualización de datos. Algunas de las librerías más populares son:

##### [Matplotlib](https://matplotlib.org/) <a id="matplotlib"></a>
<img src="https://matplotlib.org/_static/logo2_compressed.svg" alt="matplolib logo" height="100"/>

Matplotlib permite la creación de visualizaciones estáticas (y también interactivas) con una extensa variadad de gráficos disponibles (dispersión, barra, pie, histogramas, entre otros) y con gran capacidad de personalización.

<img src="https://matplotlib.org/stable/_images/sphx_glr_scatter_demo2_001.png" alt="matplotlib ejemplo" height="400"/>

<hr>

##### [Seaborn](https://seaborn.pydata.org/) <a id="seaborn"></a>
<img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" alt="numpy logo" height="100"/>

Seaborn (basada en Matplotlib) facilita la visualización estadística mediante gráficos de gran calidad sin la necesidad de extensiva personalización. 

<img src="https://seaborn.pydata.org/_images/regression_marginals.png" alt="seaborn ejemplo" height="400"/>

<hr>

#### [Plotly](https://plotly.com/python/) <a id="plotly"></a>
<img src="https://plotly.com/all_static/images/plotly_graphing_libraries_1.png" alt="plotly logo" height="100"/>

Plotly es una libreria de gráficos interactivos que se destaca por su extensa variedad de gráficos (más de 40), la calidad nativa de sus visualizaciones, y la compatibilidad con el navedor.

<iframe src="url" title="plotly ejemplo">

<hr>

#### <a id="bokeh"></a>[Bokeh](https://bokeh.org/) <a id="bokeh"></a>
<img src="https://static.bokeh.org/logos/logotype.svg" alt="Bokeh logo" height="100"/>

Otra alternativa para la creación de gráficos interactivos en Python.

<hr>

### <a id="mapas">Mapas e información geoespacial</a>

#### [geopandas](https://pandas.pydata.org/) <a id="geopandas"></a>
<img src="https://geopandas.org/_static/geopandas_logo_web.svg" alt="geopandas logo" height="100"/>

Extiende la funcionalidad de pandas para permitir la manipulación de datos geoespaciales. Permite la carga de formatos GIS comunes (.shp, .geojson, .gpk, entre otros) y el trabajo y reproyección de sistemas de referencia.

<hr>

#### [cartopy](https://scitools.org.uk/cartopy/docs/latest/)<a id="cartopy"></a>
<img src="https://scitools.org.uk/cartopy/docs/latest/_static/cartopy.png" alt="geopandas logo" height="100"/>

Diseñada para el procesamiento de información geoespacial, la creación de mapas y otros análisis.

<hr>

#### [Folium](https://python-visualization.github.io/folium/)<a id="folium"></a>
<img src="https://python-visualization.github.io/folium/_images/folium_logo.jpg" alt="geopandas logo" height="100"/>

Basada en la librería de javascript ```leaflet.js``` utilizada en la creación de mapas livianos e interactivos totalmente compatibles con el navegador. Folium posee numerosos mapas base disponibles como OpenStreetMap, Mapbox, and Stamen entre otros y tienen el potencial de crear mapas con series de tiempo e incluso mapas geológicos.

<hr>

#### [Plotly](#plotly)

### Modelamiento geológico <a id="modelamiento"></a>

#### [gempy](https://www.gempy.org/)<a id="gempy"></a>
<img src="https://static.wixstatic.com/media/819b61_005a11348d95480981d0a188be0801b2~mv2.png/v1/fill/w_199,h_71,al_c,q_85,usm_0.66_1.00_0.01/GemPy_logo_on_transp.webp" alt="gempy logo" height="100"/>

Gempy permite la modelación 3D de estructuras geologicas complejas (capas, pliegues, fallas, etc.) pudiendo implementar además modelamiento probabilístico.

<hr>

#### [flopy](https://github.com/modflowpy/flopy)<a id="flopy"></a>
<img src="https://raw.githubusercontent.com/modflowpy/flopy/master/examples/images/flopy3.png" alt="flopy logo" height="100"/>

Flopy permite la creación, ejecución y post-proceso de modelos basados en MODFLOW.

## Cursos y tutoriales <a id="cursos"><a/>

* [Nube minera | Introducción a Data Analytics en Geociencias con Python (DAP)](https://nubeminera.cl/course/dap/) Curso gratuito e introductorio donde se enseña a realizar un análisis exploratorio de datos provenientes de muestras de sondajes a través de Python.

## Libros, blogs y canales de Youtube<a id="materiales"></a>
### Libros

![Libros gratuitos generales de Python](https://github.com/pamoroso/free-python-books)

### Blogs y canales de youtube
* [Hatari Labs](https://www.hatarilabs.com/) Página y canal de youtube con blogs y videotutoriales respecto a SIG, modelamiento y otros. Especial enfoque en la hidrogeologia.

## Utilidades <a id="utilidades"></a>

* [Diagrama de Piper con Python | Hatari Labs](https://www.hatarilabs.com/ih-en/how-to-make-a-piper-diagram-in-python-tutorial)
* [Creación de gráficos exportables con Plotly Chart](https://chart-studio.plotly.com/create/)
