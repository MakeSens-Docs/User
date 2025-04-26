---
description: >-
  Esta herramienta proporciona una interfaz para acceder a los datos de nuestros
  dispositivos y facilita la realización de análisis predefinidos con estos
  datos.
---

# SDK

Este SDK cuenta con librerías desarrolladas en dos de los principales lenguajes de programación utilizados en el análisis de datos: _**Python**_ y _**R**_.&#x20;

## Instalación

Para usar _**APIMakeSens**_ primero necesitas instalarlo.

> **APIMakeSense** es compatible con Python para la versión 3.8 o superior.

{% tabs %}
{% tab title="Python" %}
Instale la última versión usando _pip_

```python
pip install APIMakeSens
```

Si requieres instalar una versión específica  proporcione restricciones al instalar

```python
# Instalar APIMakeSens versión 1.4.7 espeficicamente
pip install APIMakeSens==1.4.7
```
{% endtab %}

{% tab title="R" %}
Instale la última versión desde [GitHub](https://github.com/MakeSens-Data/MakeSensAPI_R).

```r
# Instalación vía GitHub
install.packages('devtools')
library('devtools')
install_github("MakeSens-Data/MakeSensAPI_R", force = TRUE)
```
{% endtab %}
{% endtabs %}

## Usando APIMakeSens

Para utilizar _APIMakeSens_, lo primero es importarlo.

{% tabs %}
{% tab title="Python" %}
```python
from MakeSens import MakeSens
```
{% endtab %}

{% tab title="R" %}
```r
require("MakeSensAPI")
```
{% endtab %}
{% endtabs %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}
