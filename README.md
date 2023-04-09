# Analisis del precio de las viviendas en el oriente antioqueño

Este proyecto tiene le fin de analizar el comportamiento de los precios de las viviendas en el oriente antioqueño en el año 2021 y posteriormente a esto realizar un modelado estadisticos para buscar patrones ocultos y realizar prodecciones del precio de las viviendas

**Todavia de esta trabajando en el proyecto, por lo tanto esta sujeto a cambios**

## Limpieza de los datos

Se realizan los siguientes pasos:

Se realiza una primera limpieza en este [script](https://github.com/juanguzman2/Precio-de-viviendas-en-colmbia/blob/master/Script/limpieza/primera_limpieza.ipynb) en donde se siguen estos pasos:

1. Se observa la calidad de los datos las variables.
2. Se observa gran canitdad de columnas que contienen mas de un 70% de datos faltantes
3. Se tratan las columnas mencionadas en el paso 2
4. Se realiza un cruce de informacion con el objetivo de crear una sola tabla que contenga las caracteristicas de las viviendas y su ubicacion
5. Se organzian ciertos aspectos de nombres de las variables y datos 

A continuacion se hace una segunda limpieza de los datos mas profunda en este [script](https://github.com/juanguzman2/Precio-de-viviendas-en-colmbia/blob/master/Script/limpieza/limpieza_final.ipynb) en donde se realizan las siguientes acciones:

1. Limpieza y transformacion de los valores faltantes para todas las variables del dataset
2. Se examina variable por variable con el fin de determinar las transformaciones necesaras
3. Renombramiento de columnas
4. Deteccion de valores atipicos: En este paso se realizan pasos adicionales como:
    1. Se hacen unos filtros iniciales para la variable precio y area
    2. Deteccion de valores atipicos mediante analisis graficos 
    3. Deteccion de valores atipicos mediante metodos de aprendizaje automatico no supervisado usando el algoritmo OneClassSVM
5. Tratamiento de los valores atipicos

## Analisis exploratorio de la variable precios

Se realiza un analisis sobre la variable precios en el siguiente [script](https://github.com/juanguzman2/Precio-de-viviendas-en-colmbia/blob/master/Script/Analisis%20exploratorio/Analisis_precio.ipynb) en el cual se busca su comportamiento y distribucion. Tambien su relacion bivariado con otras variables contestando preguntas como:
* Relacion entre el precio y el area de las viviendas
* Precio promedio de la vivienda por estrato
* Precio promedio de la vivienda por municipio
* Precio promedio de la vivienda por antiguedad
* Boxplot de precios de la vivienda por estrato
* Distribución precios de la vivienda por tipo de vivienda
* Distribución precios de la vivienda por ubicación

Por ultimo su comportamiento multivariado en el cual se resuelven preguntas como:
* precio promedio de las viviendas por estrato en cada municipio.
* precio promedio de las vieindas por tipo de propiedad en cada municipio.
* Correlacion general de todas las variables con todas las variables

## Prediccion del precio de las viviendas mediante metodos estadisticos

Debido a que es una base de datos que contiene una variable dependeinte y muchas independientes se usaran los siguientes modelos con el fin de solucionar el problema:
1. Regresion lineal multiple
2. Arboles de decision
3. Bosque aleatorios
4. Redes neuronales
5. Maquina de vectores de soporte(SVM)
6. Gradient boosting Machine (GBM)

### Seleccion del modelo

Se usaran metodos de evaluacion del modelo como:
1. MAPE: Error porcentual absoluto medio
2. Coeficiente de determinacion (R2)


