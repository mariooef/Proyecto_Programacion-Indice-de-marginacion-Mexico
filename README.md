# Proyecto Programacion - Indice de marginalización en Mexico

**Analista:** Ing. Mario Estrada Ferreira

**Docente evaluador:** Dr. Julio Waissman Vilanova

## Descripción del trabajo

Este repositorio cuenta con un proyecto final para el curso de programación pertenecientes como requisito para la maestría en ciencia de datos.

El proyecto realizado consta del análisis de datos de ciertos puntos respecto al índice de marginalización en México el cual su base de datos fue extraída de https://www.gob.mx/conapo/documentos/indices-de-marginacion-2020-284372 (página oficial del gobierno) y en el que nos muestra una base de datos que contienen los indicadores socioeconómicos que sirvieron para la construcción de los índices de marginación 2020 en los diferentes niveles de desagregación geográfica censal posible, y por primera ocasión, una estimación a nivel de colonias. En cada caso, se ofrece la publicación que contiene el apartado conceptual de la marginación, los capítulos de análisis de resultados, así como los anexos estadísticos, cartográficos y metodológicos; o bien, pueden consultarse las notas técnico-metodológicas que ofrecen una explicación sobre la construcción de los indicadores socioeconómicos que conformaron cada índice de marginación, así como una descripción de los métodos utilizados para su obtención, su estratificación —que determina los cinco grados de marginación—, su normalización y los principales resultados.

#### Herramientas tecnicas

El análisis se realizó con Código Python hecho en un entorno de desarrollo jupyter notebook

Librerias utilizadas:
* numpy
* pandas
* matplotlib.pyplot

#### El analisis

El análisis consta de lo siguiente:

* análisis de los datos estadísticos generales de la base de datos
* Grafica que permite ver el porcentaje de municipios por estado con índices de marginación "muy bajo", "bajo", "medio", "alto" y "muy alto".
* Grafica que permite ver el porcentaje de la población con respecto a la población de cada estado con índices de marginación "muy bajo", "bajo", "medio", "alto" y "muy alto".
* análisis comparativo de las dos graficas anteriores.
* Grafica del porcentaje de alfabetismo respecto al porcentaje de poblaciones con localidades de menos de 5000 habitantes.
* análisis de la grafica
* Desarrollo de un nuevo DataFrame, basado en el DataFrame original del estudio, en donde se plantea nuevos indicadores que pudieran ser de importancia a la hora de definir políticas públicas.

    * **VIPE.2KM** (Porcentaje de vivienda que cuenta con a alguna institución publica educativa a menos de 2 km de distancia) = Este indicador es importante para saber que tan disponible, sin ningún otro factor, alguna escuela o institución publica educativa independientemente del nivel. Por qué elegí 2 kilómetros, me parece una distancia razonable en donde el factor de trasporte no debe influir y tampoco estaría lo demasiado cerca para afectar alguna zona habitacional provocando otros problemas viales o civiles. Este indicador puede ayudar a en caso de que el porcentaje en una localidad sea bajo, puede dar la pauta de construir escuelas más cercanas o bien optar por un sistema de transporte especial para estudiantes y así permitan a cada familia quitar ese factor para la educación, el transporte cuesta y esto puede ser causa de deserción escolar.

    * **OVAI** (Porcentaje de ocupantes en viviendas particulares con acceso a internet) = Este indicador, aunque pueda parecer incongruente con los índices de marginalidad, puesto que el acceso a internet se puede seguir interpretando como no básico, si se me ha hecho interesante preguntarme realmente la población con índices de marginalidad altos o medios que tanto acceso a internet tienen (vía celular, vía telefónica, etc) y si a pesar de índices altos el internet al final responde la pregunta que se ha convertido en parte importante para la población. Este indicador también puede dar la pauta para poder determinar de qué manera se educa o bien se informa o se mantiene en contacto con la población marginada, si existe un medio de comunicación es más fácil llegar a ellos y ayudarlos.

    * **COMDIA** (Porcentaje de la población que tiene disponibilidad de no más 2 comidas al día.) = Este indicador podría ser de mucha ayuda para generar programas adecuados para otorgar acceso a una mejor alimentación, ya sea para comedores comunitarios o bien para acceso a vales de despesa por ley (que puedan ser cambiados por ciertas tiendas y con reglas para su uso formal). Todo ser humano o bien toda persona que forme parte de una población debe tener acceso al menos a 3 comidas diarias, este indicador lógicamente no estaría contando a personas que por decisión deciden hacer una o dos o ninguna comida, es porcentaje de cuantas comidas al día se tiene acceso.

    * **EMNA** (Porcentaje de muertes no accidentales con edad menor de 65 años.) = Este indicador indica el porcentaje de muertes en personas menores de 65 años que no tenga que estar relacionado con accidentes. Muertes naturales, enfermedad, delincuencia. es importante conocer este indicador para saber que tanto es la esperanza de vida y si la marginalidad influye en ella. esto se podría tomar para mejorar el sistema de salud y los servicios médicos en general en localidad que así lo requiera en donde la marginalidad y la esperanza de vida estén de la mano.

    * **OME.2** (Porcentaje de ocupantes menores de edad en viviendas particulares que superan la cantidad de 2) = La justificación para este indicador es que es importante conocer que tanto está relacionado el porcentaje de personas menores edad que superan los 2 habitantes por vivienda con el índice de marginalidad y si hay una relación entre más índice de marginalidad. esto ayudara para crear programas más eficientes para el control de natalidad o bien crear leyes que puedan controlar el número de nacimientos permitidos (esto es algo extremista, pero entre más personas que no tengan acceso a recursos suficientes o trabajos formales que le permitan tener una calidad de vida adecuada, el índice de marginalidad seguirá en ascenso).

#### Archivos en este repositorio

* **Indice-marginacion-Mexico.ipynb** : Este archivo del proyecto de tipo jupyter
* **grafica_marginacion.png** : Archivo de imagen obtenida a partir de desarrollar la actividad "c" de lo solicitado.
* **grafica_poblacion.jpg** : Archivo de imagen obtenida a partir de desarrollar la actividad "d" de lo solicitado.
* **Nuevos_Indicadores_Dataframe_IMM_2020.parquet** : Archivo donde está contenido el nuevo DataFrame que se creó con indicadores nuevos a partir de desarrollar la actividad "h" de lo solicitado.
