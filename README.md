# python-geologia

## Contenidos

* [Librerias](#lib)
  * [Carga y manipulación de datos](#carga)
    * [numpy](#numpy) 
    * [pandas](#pandas) 
  * [Visualización de datos](#viz)
    * [Matplotlib](#matplotlib)
    * [Seaborn](#seaborn)
    * [Plotly](#plotly)
    * [Bokeh](#bokeh)
  * [Mapas e información geoespacial](#mapas)
  * [Modelamiento geológico](#modelamiento)

* [Cursos y tutoriales](#lib)

Compilado de librerías y utilidades de Python de código abierto principalmente a la geología.

## <a id="carga">Librerías</a>

### <a id="carga">Carga y manipulación de datos</a>

#### [Numpy](https://numpy.org/) <a id="numpy"></a>
<img src="https://numpy.org/images/logos/numpy.svg" alt="numpy logo" height="200"/>

Numpy permite el trabajo con matrices y vectores y es una parte fundamental de numerosas otras librerías dentro del ecosistema de Python.

#### [pandas](https://pandas.pydata.org/) <a id="pandas"></a> 
<img src="https://pandas.pydata.org/static/img/pandas_white.svg" alt="pandas logo" height="200"/>

Pandas permite la carga, análisis y transformación de información tabular. Con pandas es posible cargar información en forma de CSV, Excel, JSON, GeoJSON entre muchas otros y posee la capacidad de llevar a cabo filtrado, clasificación y ordenamiento de la información.

### <a id="viz">Visualización</a>

Python posee numerosas librerías para la visualización de datos. Y la eleccion de la librería variará según el objetivo de la visualización, algunas de las librerías más populares corresponden a:

##### [Matplotlib](https://matplotlib.org/) <a id="matplotlib"></a>
<img src="https://matplotlib.org/_static/logo2_compressed.svg" alt="matplolib logo" height="200"/>

Matplotlib permite la creación de visualizaciones estáticas (y también interactivas) con una extensa variadad de gráficos disponibles (dispersión, barra, pie, histogramas, entre otros) y con gran capacidad de personalización.

##### [Seaborn](https://seaborn.pydata.org/) <a id="seaborn"></a>
<img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" alt="numpy logo" height="200"/>

Seaborn (basada en Matplotlib) facilita la visualización estadistica mediante gráficos de gran calidad sin la necesidad de extensiva personalización. 

#### [Plotly](https://plotly.com/python/) <a id="plotly"></a>
<img src="https://plotly.com/all_static/images/plotly_graphing_libraries_1.png" alt="plotly logo" height="200"/>

Plotly es una libreria de gráficos interactivos que se destaca por su extensa variedad de gráficos interactivo (más de 40) y la calidad nativa de sus gráficos.

#### <a id="bokeh"></a>[Bokeh](https://bokeh.org/) <a id="bokeh"></a>
<img src="https://static.bokeh.org/logos/logotype.svg" alt="Bokeh logo" height="200"/>

Otra alternativa para la creación de gráficos interactivos en Python.

Plotly se caracteriza por su gran variedad de gráficos disponibles [(más de )]() y el carácter interactivo de estos. 

### <a id="mapas">Mapas e información geoespacial</a>

#### [geopandas](https://pandas.pydata.org/) <a id="geopandas"></a>
![geopandas logo](https://geopandas.org/_static/geopandas_logo_web.svg)
Extiende la funcionalidad de pandas para la manipulación de datos geoespaciales. Permite la carga de formatos GIS comunes (shp, geojson, geopackage, etc.) y la reproyección de sistemas de referencia.

#### [cartopy](https://scitools.org.uk/cartopy/docs/latest/)<a id="cartopy"></a>
Diseñada para el procesamiento de información geoespacial, la creación de mapas y otros análisis.

#### [Plotly](#plotly)
#### [Bokeh](#bokeh)
#### [Folium](https://python-visualization.github.io/folium/)<a id="folium"></a>
Basada en la libería de javascript ```leaflet.js``` para la creación de mapas livianos e interactivos totalmente compatibles con el navegador. Folium posee numerosos mapas base disponibles como OpenStreetMap, Mapbox, and Stamen entre otros y tienen el potencial de crear mapas con series de tiempo e incluso mapas geológicos completos.

### Modelamiento geológico <a id="modelamiento"></a>

#### [gempy](https://www.gempy.org/)<a id="gempy"></a>

![Gempy logo](https://static.wixstatic.com/media/819b61_005a11348d95480981d0a188be0801b2~mv2.png/v1/fill/w_199,h_71,al_c,q_85,usm_0.66_1.00_0.01/GemPy_logo_on_transp.webp)

Gempy permite la modelación 3D de estructuras geologicas complejas (capas, pliegues, fallas, etc.) pudiendo implementar además modelamiento probabilístico.

#### [flopy](https://github.com/modflowpy/flopy)<a id="flopy"></a>
![Flopy logo](https://raw.githubusercontent.com/modflowpy/flopy/master/examples/images/flopy3.png)

Flopy permite la creación, ejecución y post-proceso de modelos basados en MODFLOW.

## Cursos

##
