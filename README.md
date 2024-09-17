# AtlasVPM - Análisis de variaciones en cirugías frecuentes en el SNS
## Procedimientos quirírugicos incluídos en decretos de garantía de tiempos de espera
Este repositorio contiene el código de análisis de los indicadores de cirugías frecuentes en el SNS - procedimientos incluídos en decretos de garantía de tiempos de espera. 
Este código se basa en un script de [QUARTO](https://quarto.org/) (.qmd) programado en R. 

### Introducción

Este informe del Atlas de Variaciones de la Práctica Médica describe la variación en la utilización de un conjunto de procedimientos quirúrgicos programados (cirugía electiva) en las 212 áreas sanitarias de residencia, que corresponden a la organizacion territorial del Sistema Nacional de Salud (SNS) exceptuando las ciudades autónomas de Ceuta y Melilla (INGESA).
En los resultados se presenta la evolución de la variación por área sanitaria a lo largo del tiempo a nivel del SNS y la CCAA; y la variación geográfica a nivel de área sanitaria para cada uno de los procedimientos seleccionados.
El objetivo de este AtlasVPM es explorar la evolución temporal de las variaciones geográficas en la indicación y realización de un conjunto seleccionado de procedimientos quirúrgicos electivos a nivel de área sanitaria para el conjunto de las comunidades autónomas (CCAA) participantes.
Estos procedimientos quirúrgicos electivos se han seleccionado a partir de aquellas cirugías consideradas de especial interés para su información y monitorización por los sistemas de información de listas de espera quirúrgica del SNS.


### Notas metodológicas

Los procedimientos seleccionados para estudio se corresponden con los procesos incluidos en el Anexo IV del Real Decreto 605/2003, de 23 de mayo, por el que se establecen medidas para el tratamiento homogéneo de la información sobre las listas de espera en el Sistema Nacional de Salud [RD 605/2003](https://www.boe.es/eli/es/rd/2003/05/23/605/con) para todos los indicadores excepto prótesis de rodilla y histerectomía que aparecen en [RD 1039/2011](https://www.boe.es/eli/es/rd/2011/07/15/1039).


#### Fuente de datos

Los episodios correspondientes a los procedimientos de cirugía programada se extrajeron del Conjunto Mínimo Básico de Datos al Alta Hospitalaria (CMBD-AH) de las Comunidades Autónomas (CCAA) participantes en el Proyecto Atlas VPM durante el período 2003-2022. Los datos los CMBDs de Andalucía en toda la serie, Galicia en los años 2016 a 2022, Castilla-León en los años 2019 a 2022, y Cataluña en los años 2021 y 2022 no han estado disponibles para la ejecución de este análisis.


#### Sobre el numerador

Para el cálculo de los indicadores por proceso quirúrgico se contabilizaron todas las altas en hospitales del Sistema Nacional de Salud más las altas financiadas públicamente en los centros de titularidad privada - allá donde esta información estuviera disponible. Respecto a estas últimas (actividad bajo concierto), hay que tener en consideración que la información sobre las mismas se recoge de forma irregular entre Comunidades Autónomas. Este hecho puede influir en que los indicadores de utilización presenten tasas relativamente más altas en las áreas sanitarias donde el uso de proveedores privados financiados públicamente sea mayor o la notificación de este tipo de actividad sea más detallada, o por el contrario, generar tasas menores en áreas con menor contribución del sector privado o sub-notificación de casos. 
En el año 2016 entró en vigor a nivel nacional la nueva clasificación de diagnósticos y procedimientos CIE-10-MC-ES, reemplazando la CIE-9-MC-ES utilizada previamente. La transición entre ambos tipos de codificación no ha sido homogénea en todas las comunidades autónomas, ni en los hospitales dentro de cada comunidad, lo que ha originado que en los primeros años de utilización de CIE-10, no se haya alcanzado el 100% de cobertura en la codificación de episodios en algunos hospitales. Este hecho puede influir en la modificación de la tendencia observada en la utilización de algunos procedimientos quirúrgicos a partir de 2016. 
Por otra parte, el cambio en la codificación ha obligado a traducir los indicadores previamente definidos con códigos CIE-9, a códigos CIE-10. La nueva clasificación supone un cambio cualitativo (_i.e., mayor especificidad_) y cuantitativo (_i.e., disminución relativa de la codificación de diagnósticos secundarios y procedimientos_) en la codificación, por lo que la traducción se ha realizado para conseguir la equivalencia semántica entre las dos clasificaciones. En cualquier caso, la observación de la evolución de las tasas parece descartar en la mayoría de los procesos estudiados que la traducción esté afectando a los resultados de este Atlas.

#### Sobre el denominador

Los episodios se asignan al área de residencia del paciente y se computan con independencia del hospital, área o comunidad autónoma en la que se produce la hospitalización. De esta manera, el análisis realizado compara la exposición de las poblaciones a la asistencia sanitaria según su lugar de residencia, antes que las pautas de ingreso de los hospitales (i.e., propensión a hospitalización), aunque unas y otras están asociadas.
La población utilizada en la estandarización y cálculo de los denominadores de los indicadores procede de la actualización anual de los padrones municipales publicados por el Instituto Nacional de Estadística (INE) entre los años 2003 a 2022.

#### Sobre la unidad de análisis

La unidad de análisis en este informe son las áreas sanitarias de referencia según residencia de los pacientes intervenidos. 

#### Sobre los resultados analizados

Este informe se centra en el cálculo de las tasas estandarizadas para cada proceso tomando como referencia la población española (por sexo y grupo de quinquenal de edad) para cada año en el periodo de estudio.