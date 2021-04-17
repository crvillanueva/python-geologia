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

### [NumPy](https://numpy.org/) <a id="numpy"></a>

<img src="https://numpy.org/images/logos/numpy.svg" alt="numpy logo" height="100"/>
NumPy permite el trabajo con matrices y vectores de manera rápida y eficiente. Es una parte clave de numerosas librerías dentro del ecosistema de Python, por ejemplo, encontrándose en el núcleo la librería pandas. 
<br>
<br>

```python
import numpy as np

a = np.arange(15).reshape(3, 5)

a
```
```
array([[ 0,  1,  2,  3,  4],
       [ 5,  6,  7,  8,  9],
       [10, 11, 12, 13, 14]])
```

<hr>

### [pandas](https://pandas.pydata.org/) <a id="pandas"></a> 
<img src="https://pandas.pydata.org/static/img/pandas_white.svg" alt="pandas logo" height="100"/>

Pandas permite la carga, análisis y transformación de información tabular. Con pandas es posible cargar información en forma de CSV, Excel, JSON, GeoJSON entre muchas otros, la que puede ser posteriormente filtrada, clasificada y/o agregada. 
<br>
<br>

##### Ejemplo de carga de [archivo csv](https://raw.githubusercontent.com/crvillanueva/python-geologia/main/data/terremotos.csv)
```python
import pandas as pd 

datos = pd.read_csv('data/terremotos.csv') # Lectura del archivo
datos.head(3) # Mostrar solo las primeras 3 entradas
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
  </tbody>
</table>

<hr>

### <a id="viz">Visualización</a>

Python posee numerosas librerías para la visualización de datos. Algunas de las más populares son:

### [Matplotlib](https://matplotlib.org/) <a id="matplotlib"></a>
<img src="https://matplotlib.org/_static/logo2_compressed.svg" alt="matplolib logo" height="100"/>

Matplotlib permite la creación de visualizaciones estáticas (y también interactivas). Se descataca por una extensa variedad de gráficos disponibles (dispersión, barra, histogramas, entre otros) y una gran capacidad de personalización.
<br>
<br>

```python
import matplolib.pyplot as plt

# Datos
x_silice = [50.2, 54.3, 60.1, 64.9, 66.2, 71.5]
y_magnesio = [7.4, 3.7, 2.8, 1.7, 0.9, 0.5]

# Creación del gráfico
plt.plot(x_silice, y_magnesio, color='orange', linewidth=2)

# Personalización
plt.xlabel('% $SiO_{2}$')
plt.ylabel('% $MgO$')
plt.grid(alpha=0.4)
plt.tight_layout()

plt.show()
```

<img src="https://raw.githubusercontent.com/crvillanueva/python-geologia/main/img/matplob_ex.svg" alt="matplotlib ejemplo" height="400"/>

<hr>

### [Seaborn](https://seaborn.pydata.org/) <a id="seaborn"></a>
<img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" alt="numpy logo" height="100"/>

Seaborn se enfoca en la visualización estadística, permitiendo establecer fácilmente relaciones entre parámetros. Es posible crear con ella gráficos de alta calidad sin necesidad de personalización adicional.
<br>
<br>

```python
import seaborn as sns

# Estilo del gráfico
sns.set_theme(style="darkgrid")

# Datos
tips = sns.load_dataset("tips")

# Gráfico
g = sns.jointplot(x="total_bill", y="tip", data=tips,
                  kind="reg", truncate=False,
                  xlim=(0, 60), ylim=(0, 12),
                  color="m", height=7)
```

<img src="https://seaborn.pydata.org/_images/regression_marginals.png" alt="seaborn ejemplo" height="400"/>

<hr>

### [Plotly](https://plotly.com/python/) <a id="plotly"></a>
<img src="https://plotly.com/all_static/images/plotly_graphing_libraries_1.png" alt="plotly logo" height="100"/>

Plotly es una libreria de gráficos interactivos que se destaca por su extensa variedad de gráficos (más de 40), la calidad nativa de sus visualizaciones, y la compatibilidad con el navedor.

<iframe src="url" title="plotly ejemplo">

<hr>

### <a id="bokeh"></a>[Bokeh](https://bokeh.org/) <a id="bokeh"></a>
<img src="https://static.bokeh.org/logos/logotype.svg" alt="Bokeh logo" height="100"/>

Otra alternativa para la creación de gráficos interactivos en Python.

<hr>

### <a id="mapas">Mapas e información geoespacial</a>

### [geopandas](https://pandas.pydata.org/) <a id="geopandas"></a>
<img src="https://geopandas.org/_static/geopandas_logo_web.svg" alt="geopandas logo" height="100"/>

Extiende la funcionalidad de pandas para permitir la manipulación de datos geoespaciales. Permite la carga de formatos GIS comunes (.shp, .geojson, .gpk, entre otros) y el trabajo y reproyección de sistemas de referencia.

<hr>

### [cartopy](https://scitools.org.uk/cartopy/docs/latest/)<a id="cartopy"></a>
<img src="https://scitools.org.uk/cartopy/docs/latest/_static/cartopy.png" alt="geopandas logo" height="100"/>

Diseñada para el procesamiento de información geoespacial, la creación de mapas y otros análisis.

<hr>

### [Folium](https://python-visualization.github.io/folium/)<a id="folium"></a>
<img src="https://python-visualization.github.io/folium/_images/folium_logo.jpg" alt="geopandas logo" height="100"/>

Basada en la librería de javascript ```leaflet.js``` utilizada en la creación de mapas livianos e interactivos totalmente compatibles con el navegador. Folium posee numerosos mapas base disponibles como OpenStreetMap, Mapbox, and Stamen entre otros y tienen el potencial de crear mapas con series de tiempo e incluso mapas geológicos.

<hr>

### [Plotly](#plotly)

### Modelamiento geológico <a id="modelamiento"></a>

### [gempy](https://www.gempy.org/)<a id="gempy"></a>
<img src="https://static.wixstatic.com/media/819b61_005a11348d95480981d0a188be0801b2~mv2.png/v1/fill/w_199,h_71,al_c,q_85,usm_0.66_1.00_0.01/GemPy_logo_on_transp.webp" alt="gempy logo" height="100"/>

Gempy permite la modelación 3D de estructuras geologicas complejas (capas, pliegues, fallas, etc.) pudiendo implementar además modelamiento probabilístico.

<img src="https://static.wixstatic.com/media/819b61_7bb9c7354c0e4f95b30f6363e049b37f~mv2.png/v1/crop/x_256,y_130,w_1535,h_1406/fill/w_490,h_449,al_c,q_85,usm_0.66_1.00_0.01/sphx_glr_ch1_7_3d_visualization_003.webp" alt="seaborn ejemplo" height="400"/>

<hr>

### [flopy](https://github.com/modflowpy/flopy)<a id="flopy"></a>
<img src="https://raw.githubusercontent.com/modflowpy/flopy/master/examples/images/flopy3.png" alt="flopy logo" height="100"/>

Flopy permite la creación, ejecución y post-proceso de modelos basados en MODFLOW.

## Cursos y tutoriales <a id="cursos"><a/>

* [Nube minera | Introducción a Data Analytics en Geociencias con Python (DAP)](https://nubeminera.cl/course/dap/) Curso gratuito e introductorio donde se enseña a realizar un análisis exploratorio de datos provenientes de muestras de sondajes a través de Python.

## Libros, blogs y canales de Youtube<a id="materiales"></a>
### Libros

📚 [Libros gratuitos generales de Python](https://github.com/pamoroso/free-python-books)

### Blogs y canales de youtube
* [Hatari Labs](https://www.hatarilabs.com/) Página y canal de youtube con blogs y videotutoriales respecto a SIG, modelamiento y otros. Especial enfoque en la hidrogeologia.

## Utilidades <a id="utilidades"></a>

* [Diagrama de Piper con Python | Hatari Labs](https://www.hatarilabs.com/ih-en/how-to-make-a-piper-diagram-in-python-tutorial)
* [Creación de gráficos exportables con Plotly Chart](https://chart-studio.plotly.com/create/)
