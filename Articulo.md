Introducción

Objetivo General

Objetivos Especificos

Jistificacion

1. Obtener informacion para ingresos y para seguridad
1.1 Seleccion de varianbles ingresos
    Para la contruccion de esta tabla vea (anexo 1) con el fin de observar que variables intervienen en esta base de datos.
    La base de datos contiene información relacionada con el trabajo, los ingresos y la coposicion del hogar, así como algunas carac
    teristicas de las personas encuestadas. Por ejemplo su edad y sexo biologico.

    Las variables seleccionadas se encuentran en el (anexo 1). Las variables relacionadas con honorarios, primas, comisiones y cualquier otro valor  relacionado con ingresos se suman en funciones mensuales, por ejemplo las primas de servicio se divide en 12 con la finalidad de obtener un valor mensual. 

    Las variable de respuesta es interpretada en unidades por millon para mayor preacticidad y entendimiento. En el grafico se observa como se distribuyen los ingresos de los habitantes de cundinamarca, se puede observar que hay varios espacios vacios, dado que no tienen medicion de esta variable.

    En el histograma se puede observar que la variable se aumula hacia valores entre 0 y cinco unidades por millon, tambien que existe una pequeña poblacion que se encuentra entre los 10 y 15 unidades por millon. En la tabla se puede observar la descripción de algunas estadísticas de interes. 

    '\\begin{tabular}{lr}\n\\toprule\n & Total_ingresos \\\\\n\\midrule\ncount & 6436.000000 \\\\\nmean & 1.721322 \\\\\nstd & 1.944517 \\\\\nmin & 0.000000 \\\\\n25% & 0.650000 \\\\\n50% & 1.170000 \\\\\n75% & 2.000000 \\\\\nmax & 15.000008 \\\\\n\\bottomrule\n\\end{tabular}\n'

    De manera normal se intentaria reazlizar un modelo lineal generalizado, como el que se ve a continuación.

    '\\begin{tabular}{lrrr}\n\\toprule\n & \\multicolumn{3}{r}{Total_ingresos} \\\\\n & mean & std & count \\\\\nNOMB_MUN &  &  &  \\\\\n\\midrule\nANOLAIMA & 1.131487 & 1.706069 & 65 \\\\\nARBELÁEZ & 1.091940 & 1.436529 & 61 \\\\\nBITUIMA & 0.555879 & 0.590026 & 63 \\\\\nBOGOTÁ, D.C. & 2.089606 & 2.328083 & 2805 \\\\\nCAJICÁ & 3.500226 & 3.120746 & 93 \\\\\nCHOCONTÁ & 0.758479 & 0.789663 & 72 \\\\\nCHÍA & 1.891970 & 1.773540 & 135 \\\\\nCOGUA & 1.464145 & 0.988231 & 71 \\\\\nCOTA & 1.102257 & 1.232482 & 59 \\\\\nFACATATIVÁ & 1.580316 & 1.706879 & 159 \\\\\nFUNZA & 1.961152 & 1.941373 & 135 \\\\\nFUSAGASUGÁ & 1.601347 & 1.237374 & 163 \\\\\nGACHANCIPÁ & 1.549287 & 1.196325 & 107 \\\\\nGIRARDOT & 1.193273 & 1.033879 & 129 \\\\\nGUACHETÁ & 0.811132 & 0.854030 & 72 \\\\\nGUADUAS & 0.943850 & 0.614453 & 58 \\\\\nGUASCA & 1.585069 & 1.178731 & 60 \\\\\nGUTIÉRREZ & 1.064884 & 0.953990 & 72 \\\\\nLA CALERA & 1.750233 & 1.707966 & 70 \\\\\nLA MESA & 1.248744 & 0.840252 & 69 \\\\\nMADRID & 2.114693 & 1.693391 & 133 \\\\\nMANTA & 0.595376 & 0.640428 & 72 \\\\\nMEDINA & 0.691466 & 0.659192 & 44 \\\\\nMOSQUERA & 1.899657 & 1.614763 & 160 \\\\\nNILO & 1.015787 & 0.773099 & 47 \\\\\nPACHO & 0.973189 & 0.768317 & 100 \\\\\nRICAURTE & 1.059285 & 0.732542 & 64 \\\\\nSAN FRANCISCO & 2.199885 & 2.986257 & 40 \\\\\nSIBATÉ & 1.419120 & 1.057029 & 36 \\\\\nSOACHA & 1.315572 & 1.095866 & 513 \\\\\nSOPÓ & 1.218767 & 0.715284 & 62 \\\\\nSUBACHOQUE & 1.932205 & 1.183029 & 48 \\\\\nTENA & 1.291324 & 0.657721 & 68 \\\\\nTENJO & 1.636798 & 1.838635 & 42 \\\\\nTIBACUY & 1.027986 & 0.675837 & 72 \\\\\nUNE & 1.004289 & 1.244988 & 61 \\\\\nVERGARA & 0.729442 & 0.738980 & 62 \\\\\nVILLAPINZÓN & 0.577874 & 0.731627 & 112 \\\\\nVILLETA & 1.486037 & 1.315931 & 41 \\\\\nZIPAQUIRÁ & 2.345312 & 2.631738 & 141 \\\\\n\\bottomrule\n\\end{tabular}\n'

    1.1 MODELO LINEAL GENERALIZADO SIN CONTEPLAR LA DIMENSIÓN ESPACIAL

    Se plantean dos modelos normales, uno con funcion de enlace identidad y otra con funcion de enlace inversa, de los dos modelos el que mejor explica la variable de respuesta es el que contiene la inversa con un r² = 41%, sin embargo, con una fuerte afectacion en el deviance. la comparación de los criterios bayesianos BIC modelo 1 -38580.8 vs BIC modelo 2 -18789.5  indican que a pesar de la diferencia de Deviance se elige el modelo 2 en caso de pertenecer esto a un modelo bayesiano.

    Una vez que se plantea el modelo, para este caso un modelo normal, entonces se evaluan los supuestos de los residuales, para el primer supuesto de normalidad da como resultado "Se rechaza la hipótesis nula, con un valor p de 0.00". Antes de aplicar tecnicas mas complejas ṕara intentar investigar la dependecnai espacial de los individuos (para este caso regiones), el modelo generalizado lineal asume independeniente a los individuos. 

    1.2 DEPENDENCIA ESPACIAL

    Principalmente se realizara una consulta del indice de morgan, que es en pocas palabras el  nivel en que estan relacionadas las regiones, entre mas cercano a 1 es una estrecha relacion directa mientras un indice de 0 indica que los individuos son independientes, 
    por lo tanto sepodria tratar como un modelo lineal generalizado comumnente. Lo principal es calcular la matriz de distancia para esto usaremos el metodo de distancias euclidianas con forma de Reina. 

    En la imagen se observa como se toman las distancias entre municipios para crear la matriz de conectividad espacial, usandondo la funcion ps.weights.Queen.from_dataframe(df_) se calcula dicha matriz, ademas se tiene el siguiente sistema de hipotesis

    $H_0: I  = 0$
    $H_a: I != 0$

    El indice de Morgan General es de : 0.35, el valor p para el sistema de hipótesis es de 0.009 por lo tanto se rechaza la hiótesis nula, entonces la prueba indica que existe dependencia espacial, por lo tanto, no se puede tratar como un modelo lineal generalizado, por lo tanto debe averiguarse es necesario averiguar cuales son las areas donde existe mayor dependencia, para ello se realiza un indice de morgan localizado. Los resultados se consignan a continuacion:

    En el grafico se observa como existe grados de dependecia entre varios lugares, entonces se debe considerar la dependencia espacial.
    BIC modelo 1 -18789.5 vs BIC modelo 2 -18607.3





1.2 Seleccion de variables seguridad

    Las variables iniciales de segurida
2. Evaluar indice de moran local y  general
2.1 Realizar graficos LISA (Graficos para seguridad e ingresos medios)

3. Realizar modelo de regresion lineal generalziado 
3.1.1 Modelo lineal Generalizado (Normal) para Media ingreos
3.1.1.1 Evaluacion de supuestos
    a. Normalidad
    b. Homocedasticidad
3.1.2 Incorporar datos localizacion para el modelo
3.1.2.1 Evaluacion de supuestos
    a. Normalidad
    b. Homocedasticidad
3.1.3 Comparacion de modelos
3.1.4 Modelo sklear metricas

3.2 Modelo Lineal Generalizado Bernoulli (Datos seguridad)
3.2.1.1 Evaluacion de supuestos
    a. Normalidad
    b. Homocedasticidad
3.2.2 Incorporar datos localizacion para el modelo
3.2.2.1 Evaluacion de supuestos
    a. Normalidad
    b. Homocedasticidad

3.2.3 Comparacion de modelos

4. Redes Neuronales para ingresos promedio 
4.1 Modelo sklearn 

5. Modelo de clasificacion bosques aleatorios
5.1 Metricas sklearn

6. 