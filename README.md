# responsibleAI-dmiDetained

Repositorio del Proyecto del Curso *IA Responsable*

Integrantes:

- Silvana Baez
- Gabriel Cisneros
- Lenin Falconí
- Mario Moreno
- Jorge Pazmiño
- Jonathan Zea

## Acerca de los datos
Conjunto de datos del Ministerio del Interior sobre Personas detenidas/aprehendidas. Consta de 489.847 casos entre los años 2019 y 2024. Disponible en [datosabiertos.gob.ec](https://datosabiertos.gob.ec/sk/dataset/personas-detenidas-aprehendidas/resource/83c9b4d2-3d43-4404-97e3-5bdecbe03915)

## Atributos Sensibles
Estado civil, Género, Edad, Autoidentificación Étnica

## Análisis y Procedimiento de Limpieza de Datos

1. Se observó que el 91% de observaciones (446.543) no tienen registro de fecha.  

2. Los datos de los años 2020–2023 aportan registros menos del 1% en conjunto.  Por ello, se toman datos del año 2024 (41.510 casos, registros en bruto).  
3. Se limitó los datos únicamente a nacionalidad ecuatoriana.  
4. Se descartó los datos en de edad “SIN DATO” (534 registros).  
5. La variable de género fue tratada tal que para los casos **NO APLICA** se considera el dato disponible en **SEXO**.  
6. Se excluyó 39 registros asignados a la provincia **Mar territorial** y 17 registros con estado civil **Se desconoce**.  
7. De las 35 columnas, 28 fueron retiradas por ser información redundante o códigos.  

La base depurada quedó con 38.820 observaciones válidas, sobre las cuales se continuaron los análisis.  El procedimiento seguido para depurar la base está descrito en [mdi_aprendidos_analisis.ipynb](https://github.com/LeninGF/responsibleAI-dmiDetained/blob/main/mdi_aprendidos_analisis.ipynb)

## 



1. se descarta la las variables:
    - codigo_iccs: tiene relación con el código ICCS pero no guarda relación lineal con presunta_infraccion
    - fecha
    - presunta_infraccion
    - estatus_migratorio
    - sexo
    - autoidentificacion_etnica
    - nivel_instruccion
    - condicion
    - tipo de arma
    - arma
2. Definimos la variable target:
    - tipo
    - presunta_infraccion
    - nacionalidad se elimina por que todos son ecuatorianos
3. Se conserva los datos del año 2024 para el model
4. la variable edad se descarta los sin dato
5. la variable genero los no aplica se renombran como masculino o femenino segun el sexo
6. la nacionalidad queda en ecuatorianos
7. se concserva tipo de lugar pero solo las 3 primeras y las demas se van a otros
8. para comparar usar nombre provincia pero en valores per capita es mejor la comparacion
9. se usan 8 variables

