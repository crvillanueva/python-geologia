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

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>time</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>depth</th>
      <th>mag</th>
      <th>magType</th>
      <th>nst</th>
      <th>gap</th>
      <th>dmin</th>
      <th>rms</th>
      <th>net</th>
      <th>id</th>
      <th>updated</th>
      <th>place</th>
      <th>type</th>
      <th>horizontalError</th>
      <th>depthError</th>
      <th>magError</th>
      <th>magNst</th>
      <th>status</th>
      <th>locationSource</th>
      <th>magSource</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2019-05-26T07:41:15.073Z</td>
      <td>-5.8119</td>
      <td>-75.2697</td>
      <td>122.57</td>
      <td>8.0</td>
      <td>mww</td>
      <td>NaN</td>
      <td>17</td>
      <td>3.180</td>
      <td>0.84</td>
      <td>us</td>
      <td>us60003sc0</td>
      <td>2021-03-05T19:13:06.497Z</td>
      <td>78km SE of Lagunas, Peru</td>
      <td>earthquake</td>
      <td>7.0</td>
      <td>4.0</td>
      <td>0.036</td>
      <td>75.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2019-03-01T08:50:42.591Z</td>
      <td>-14.7131</td>
      <td>-70.1546</td>
      <td>267.00</td>
      <td>7.0</td>
      <td>mww</td>
      <td>NaN</td>
      <td>42</td>
      <td>2.501</td>
      <td>1.13</td>
      <td>us</td>
      <td>us1000j96d</td>
      <td>2021-04-07T02:19:45.001Z</td>
      <td>23km NNE of Azangaro, Peru</td>
      <td>earthquake</td>
      <td>7.6</td>
      <td>1.9</td>
      <td>0.033</td>
      <td>87.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2019-02-22T10:17:23.770Z</td>
      <td>-2.1862</td>
      <td>-77.0505</td>
      <td>145.00</td>
      <td>7.5</td>
      <td>mww</td>
      <td>NaN</td>
      <td>15</td>
      <td>2.045</td>
      <td>1.12</td>
      <td>us</td>
      <td>us2000jlfv</td>
      <td>2020-07-07T22:52:36.277Z</td>
      <td>111km ESE of Palora, Ecuador</td>
      <td>earthquake</td>
      <td>6.2</td>
      <td>1.8</td>
      <td>0.026</td>
      <td>144.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2018-08-24T09:04:08.250Z</td>
      <td>-11.0355</td>
      <td>-70.8284</td>
      <td>630.00</td>
      <td>7.1</td>
      <td>mww</td>
      <td>NaN</td>
      <td>12</td>
      <td>3.770</td>
      <td>0.99</td>
      <td>us</td>
      <td>us1000ggj4</td>
      <td>2018-11-01T17:50:57.040Z</td>
      <td>140km WNW of Iberia, Peru</td>
      <td>earthquake</td>
      <td>9.1</td>
      <td>1.9</td>
      <td>0.055</td>
      <td>32.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2018-08-21T21:31:47.600Z</td>
      <td>10.7731</td>
      <td>-62.9019</td>
      <td>146.82</td>
      <td>7.3</td>
      <td>mww</td>
      <td>NaN</td>
      <td>15</td>
      <td>1.822</td>
      <td>1.10</td>
      <td>us</td>
      <td>us1000gez7</td>
      <td>2020-07-10T15:53:30.330Z</td>
      <td>24km ENE of Rio Caribe, Venezuela</td>
      <td>earthquake</td>
      <td>7.5</td>
      <td>3.4</td>
      <td>0.033</td>
      <td>88.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2018-01-14T09:18:45.540Z</td>
      <td>-15.7675</td>
      <td>-74.7092</td>
      <td>39.00</td>
      <td>7.1</td>
      <td>mww</td>
      <td>NaN</td>
      <td>23</td>
      <td>4.290</td>
      <td>1.20</td>
      <td>us</td>
      <td>us2000cjfy</td>
      <td>2021-02-27T19:54:33.140Z</td>
      <td>38km SSW of Acari, Peru</td>
      <td>earthquake</td>
      <td>7.0</td>
      <td>1.8</td>
      <td>0.032</td>
      <td>95.0</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016-12-25T14:22:27.010Z</td>
      <td>-43.4064</td>
      <td>-73.9413</td>
      <td>38.00</td>
      <td>7.6</td>
      <td>mww</td>
      <td>NaN</td>
      <td>29</td>
      <td>0.355</td>
      <td>0.79</td>
      <td>us</td>
      <td>us10007mn3</td>
      <td>2021-01-29T00:57:34.710Z</td>
      <td>41km SW of Puerto Quellon, Chile</td>
      <td>earthquake</td>
      <td>5.4</td>
      <td>1.9</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2016-08-19T07:32:22.710Z</td>
      <td>-55.2852</td>
      <td>-31.8766</td>
      <td>10.00</td>
      <td>7.4</td>
      <td>mww</td>
      <td>NaN</td>
      <td>18</td>
      <td>2.852</td>
      <td>0.79</td>
      <td>us</td>
      <td>us10006exl</td>
      <td>2018-10-17T21:50:08.416Z</td>
      <td>South Georgia Island region</td>
      <td>earthquake</td>
      <td>8.4</td>
      <td>1.7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2016-04-16T23:58:36.980Z</td>
      <td>0.3819</td>
      <td>-79.9218</td>
      <td>20.59</td>
      <td>7.8</td>
      <td>mww</td>
      <td>NaN</td>
      <td>15</td>
      <td>1.440</td>
      <td>0.94</td>
      <td>us</td>
      <td>us20005j32</td>
      <td>2020-08-15T05:15:07.767Z</td>
      <td>27km SSE of Muisne, Ecuador</td>
      <td>earthquake</td>
      <td>5.7</td>
      <td>3.2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2015-11-24T22:50:54.370Z</td>
      <td>-10.0598</td>
      <td>-71.0184</td>
      <td>620.56</td>
      <td>7.6</td>
      <td>mww</td>
      <td>NaN</td>
      <td>10</td>
      <td>2.852</td>
      <td>1.00</td>
      <td>us</td>
      <td>us100040x6</td>
      <td>2020-07-07T22:44:43.869Z</td>
      <td>211km S of Tarauaca, Brazil</td>
      <td>earthquake</td>
      <td>8.5</td>
      <td>3.1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2015-11-24T22:45:38.880Z</td>
      <td>-10.5372</td>
      <td>-70.9437</td>
      <td>606.21</td>
      <td>7.6</td>
      <td>mww</td>
      <td>NaN</td>
      <td>10</td>
      <td>3.287</td>
      <td>1.36</td>
      <td>us</td>
      <td>us100040ww</td>
      <td>2021-03-02T17:50:34.662Z</td>
      <td>173km WNW of Iberia, Peru</td>
      <td>earthquake</td>
      <td>8.5</td>
      <td>3.2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2015-09-16T23:18:41.850Z</td>
      <td>-31.5622</td>
      <td>-71.4262</td>
      <td>28.41</td>
      <td>7.0</td>
      <td>mww</td>
      <td>NaN</td>
      <td>13</td>
      <td>0.903</td>
      <td>0.93</td>
      <td>us</td>
      <td>us20003k7w</td>
      <td>2021-04-07T02:41:09.403Z</td>
      <td>25km WNW of Illapel, Chile</td>
      <td>earthquake</td>
      <td>4.3</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2015-09-16T22:54:32.860Z</td>
      <td>-31.5729</td>
      <td>-71.6744</td>
      <td>22.44</td>
      <td>8.3</td>
      <td>mww</td>
      <td>NaN</td>
      <td>19</td>
      <td>0.684</td>
      <td>1.02</td>
      <td>us</td>
      <td>us20003k7a</td>
      <td>2021-03-02T17:46:56.822Z</td>
      <td>48km W of Illapel, Chile</td>
      <td>earthquake</td>
      <td>4.7</td>
      <td>3.2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>reviewed</td>
      <td>us</td>
      <td>us</td>
    </tr>
  </tbody>
</table>

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
