# big-tech-stock-analysis
Análisis de volatilidad de acciones Big Tech para recomendar las más estables a nuevos inversores.


**Proyecto realizado para:** DataLab  
**Autor:** Shirley Sosa  
**Fecha:** 22 de Septiembre de 2025
## Overview
### Objetivo: 
Analizar los precios de las acciones de 14 de las empresas tecnológicas más grandes del mundo para identificar aquellas con la mayor estabilidad de precios. La recomendación final está dirigida a un inversor con un perfil conservador que busca minimizar el riesgo.
### Preguntas a responder:
* ¿De qué período son los datos?
* ¿Puedo integrar datos públicos adicionales para enriquecer el análisis?
* ¿Puedo segmentar las empresas y encontrar aquellas con menor variación en este período?
### Data:
El análisis se basa en dos conjuntos de datos principales:

### Tabla: `Big_tech_stock_prices`
Contiene los precios diarios históricos de las acciones.

| Variable | Descripción |
|---|---|
| `stock_symbol` | Símbolo de las acciones. |
| `date` | Fecha de registro. |
| `open` | El precio en el mercado abierto. |
| `high` | El precio más alto para ese día. |
| `low` | El precio más bajo para ese día. |
| `close` | El precio al cierre del mercado, ajustado por splits. |
| `adj_close` | Precio de cierre ajustado por dividendos y distribuciones. |
| `volume` | El número de acciones negociadas en el día. |

### Tabla: `Big_tech_companies`
Contiene los nombres completos de las empresas.

| Variable | Descripción |
|---|---|
| `stock_symbol` | Símbolo de las acciones utilizado como clave común. |
| `company` | Nombre completo de la empresa. |

### Metodología:

Se analizaron los datos de precios diarios de acciones desde el **4 de enero de 2010 hasta el 12 de septiembre de 2023**. El proceso incluyó las siguientes etapas:

1.  **Limpieza de Datos:** Se trataron valores nulos y se eliminaron registros duplicados para asegurar la calidad de los datos.
2.  **Cálculo de la Métrica Clave:** Para medir la estabilidad, se calculó la **variación porcentual diaria** para cada acción, definida como `(Precio Alto - Precio Bajo) / Precio de Cierre`.
3.  **Agrupación y Segmentación:** Se calculó la media de esta variación para cada empresa y se utilizaron cuantiles para segmentarlas en tres categorías: **Baja, Media y Alta Variación**.



### Resultados:
* Las 3 empresas más estables son: IBM, Oracle y Cisco.

### Conclusiones:
* Los datos muestran que existe una diferencia significativa en la estabilidad de precios entre las diferentes empresas tecnológicas. Compañías más consolidadas como IBM y Oracle tienden a tener una menor fluctuación diaria en comparación con otras. La segmentación nos permite identificar claramente un grupo de acciones que se ajustan al perfil de un inversor que busca bajo riesgo.
* Para un análisis más preciso se recomienda añadir datos externo, como indicadores económicos, índices de volatilidad (VIX) e índices del mercado (S&P 500, NASDAQ Composite).

### Recomendación:
Para un nuevo inversor conservador, se recomienda considerar invertir en las empresas del segmento de **"Baja Variación"**. Estas compañías han demostrado tener la menor volatilidad en sus precios diarios. Las principales empresas recomendadas son:

* **International Business Machines Corporation (IBM)**
* **Oracle Corporation**
* **Cisco Systems, Inc.**
* **Intel Corporation**

Estas acciones representan la opción más estable y predecible dentro del grupo analizado.

### ¿Cómo usar este repositorio?:

* Data: Contiene el archivo final después de limpiar y procesar.
* Notebooks: Contiene el archivo de Google Colab (.ipynb) con el código paso a paso.
* README.md : Contiene el resumen del proyecto
---
