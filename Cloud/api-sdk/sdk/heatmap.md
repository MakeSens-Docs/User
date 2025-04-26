# heatmap

Visualización de las series temporales de material particulado PM10 y PM2.5 en un mapa de calor de los valores promedio de  de la serie agrupados por día y hora. Con gradiente de color de acuerdo a las [recomendaciones](http://www.ideam.gov.co/documents/51310/527391/2.+Resoluci%C3%B3n+2254+de+2017+-+Niveles+Calidad+del+Aire..pdf/c22a285e-058e-42b6-aa88-2745fafad39f) del Ministerio de Ambiente y Desarrollo Sostenible del Gobierno de Colombia.

## Parameters

|                                                                                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p><strong>data : </strong><em><strong>pd.Series (python) / data.frame (R)</strong></em><br>Contiene los datos a visualizar. En Python, debe ser una <code>pd.Series</code> con el índice de tipo <code>datetime</code>. En R,  En R, debe ser un data.frame, donde la primera columna corresponde a la estampa temporal, <code>ts</code> y la segunda a la variable de interés.</p> |
| <p><strong>variable : </strong><em><strong>str</strong></em><br>Especifica la variable de interés para la visualización, influenciando los rangos de colores normalizados y las unidades del eje Y. Opciones actuales incluyen 'PM10' y 'PM2.5'</p>                                                                                                                                  |

## Example

#### Mapa de calor para el PM10

{% tabs %}
{% tab title="Python" %}
```python
from MakeSens import MakeSens
data = MakeSens.download_data('device123','2023-10-08 05:00:00','2023-11-08 00:00:00',
                             '1H', data_type = 'PROCESSED')
MakeSens.heatmap(data.pm10,'PM10')
```

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="R" %}
```r
id_device <- 'mE1_00004'
start_date <- '2023-10-08 05:00:00'
end_date <- '2023-11-08 00:00:00'
sample_rate <- '1H'
logs <- FALSE
data_type <- 'PROCESSED'
data <- download_data(id_device,start_date,end_date,sample_rate,logs,data_type)

heatmap(data[c('ts','pm10')],'PM10')
```

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
