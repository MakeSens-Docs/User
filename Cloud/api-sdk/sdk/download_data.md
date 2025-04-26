# download\_data

{% code fullWidth="false" %}
```
download_data(id_device, start_date, end_date, sample_rate, logs = False,
                    data_type = 'RAW',  file_format = None, fields = None)
```
{% endcode %}

Acceda o descargue datos de los dispositivos: _EVA Classic, EVA Lite, ERIS_ y _CaMI Sensors_

## _Parameters:_

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>id_device : </strong><em><strong>str</strong></em><br>Id del dispositivo desde el cual se descargan los datos</p>                                                                                                                                                                                                                                                                                                                                                                      |
| <p><strong>start_date : </strong><em><strong>str</strong></em><br>Fecha y hora de inicio en formato <code>'YYYY-MM-DD HH:MM:SS'</code></p>                                                                                                                                                                                                                                                                                                                                                        |
| <p><strong>end_date : </strong><em><strong>str</strong></em><br>Fecha y hora de fin en formato <code>'YYYY-MM-DD HH:MM:SS'</code></p>                                                                                                                                                                                                                                                                                                                                                             |
| <p><strong>sample_rate : </strong><em><strong>str</strong></em></p><p>Especifica el intervalo para la extracción de datos. Valores aceptables incluyen <code>'1T'</code> para              datos por minuto, <code>'1H'</code> por hora, <code>'1D'</code> por día, y <code>'1W'</code> por semana. Adicionalmente, se pueden definir frecuencias personalizadas utilizando la notación de pandas; por ejemplo, <code>'5H'</code> para cada cinco horas o <code>'2D'</code>para cada dos días</p> |
| <p><strong>logs : </strong><em><strong>bool, default False</strong></em><br>Indica si se quiere descargar los logs, datos del funcionamiento del dispositivo. Por defecto False (descarga data)</p>                                                                                                                                                                                                                                                                                               |
| <p><strong>data_type : </strong><em><strong>str, default 'RAW'</strong></em><br>Indica el tipo de dato que se va a descargar: <code>RAW</code> o <code>PROCESSED</code>.</p>                                                                                                                                                                                                                                                                                                                      |
| <p><strong>file_format : </strong><em><strong>str, default None</strong></em><br>Formato para guardar los datos descargados (<code>'csv'</code> o <code>'xlsx'</code>). </p>                                                                                                                                                                                                                                                                                                                      |
| <p><strong>fields : </strong><em><strong>str, default None</strong></em><br>Lista de campos específicos a descargar. Por defecto None (todos los campos)</p>                                                                                                                                                                                                                                                                                                                                      |

## Returns

|                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>pd.DataFrame (Python) / data.frame (R)</strong></p><p>Devuelve un conjunto de datos con la información descargada. En Python, <code>pd.DataFrame</code> de Pandas, mientras que en R se retorna un <code>data.frame</code>, ambos estructurados para facilitar el análisis de los datos.</p> |

## Examples

{% tabs %}
{% tab title="Python" %}
```python
from MakeSens import MakeSens
data = MakeSens.download_data('device123', '2023-01-01 00:00:00', 
                     '2023-01-02 00:00:00', '1H')
```
{% endtab %}

{% tab title="R" %}
```r
data <- download_data('device123', '2023-01-01 00:00:00', 
                     '2023-01-02 00:00:00', '1H')
```
{% endtab %}
{% endtabs %}
