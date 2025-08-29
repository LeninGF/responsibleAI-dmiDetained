# responsibleAI-dmiDetained

Repositorio del Proyecto del Curso *IA Responsable*

Integrantes:

- Silvana Baez
- Gabriel Cisneros
- Lenin Falconí
- Mario Moreno
- Jorge Pazmiño
- Jonathan Zea

## Acerca de los datos:



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

