# Estadística inferencial

# Estadística inferencial vs. descriptiva

## Descriptiva:

Parte de la estadística que arregla los datos de forma que puedan ser analizados e interpretados.

Nos ayuda a determinar:

- La **Tendencia** central de una variable.
- La **variabilidad** de una variable.
- La distribución de una variable.
    - Unimodal, bimodal, multimodal

## Inferencial:

Parte de la estadística que busca predecir o deducir caracerísticas o resultados esperados de una población, basados en los datos obtenidos de una muestra de esa población.

Nos ayuda a determinar:

- Muestreo
    - Sobre la muestra nos haremos preguntas con técnicas de muestreo.
- Intervalos de confianza
- Validación de hipótesis
- Evitar sesgos

### Inferencia estadística

- Conclusiones que se obtienen sobre los parámetros de la población de datos.
- Estudio del grado de fiabilidad de los resultados extraídos del estudio.

## Uso en data science y machine learning

Tanto en un análisis como en un modelo predictivo, la estadística inferencial servirá para:

- Entender la **distribución** de nuestros datos.
- Crear y validar hipótesis.
- Hacer **experimentos.**
- Elegir los **modelos predictivos** adecuados según los datos.

# Estadísticos principales

## Experimentos

Procedimiento que peude repetirse infinitamente y tiene un conjunto bien definido de resultados posibles, conocido como espacio muestral.

- Aleatorio
    - Si tiene más de un resultado posible
- Determinista
    - Si solo tiene un resutado posible

## Población y muestra

**Muestra:** subconjunto de datos perteneciente a una población. 

Condiciones:

- **Número** suficiente de registros para ser estadísticamente significativo.
- Representación **no sesgada** de la información total.

![population-sample.png](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/population-sample.png)

## Eventos

Cada uno de los posibles resultados de un experimento. 

## Variables

Es una característica que puede obtener diferentes valores.

Tipos:

- Cualitativo: atributos (no medibles)
- Cuantitativos: números (medibles)
    - Discretas
    - Continuas

## Probabilidad

Mide **qué tan posible** es que ocurra un evento determinado.

El análisis de los eventos probabilísticos se denomina **estadística.**

### Probabilidad condicional

Posibilidades de que ocurra un evento como consecuencia de que **otros evento** haya sucedido

$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled.png)

Estas son probabilidades conjuntas que están ocurriendo una a consecuencia de la otra.

# Poblaciones normales

La población más normal, más habitual. La mayoría de los factores se rigen de una población normal que siguen una distribución normal.

## Distribución normal

- Distribución normal = Distribución de Gauss
- Su moda = su media = su mediana.
- Es simétrica.
- Tiene forma de campana, por eso es llamada en ocasiones la campana de Gauss.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%201.png)

### Ejemplos de población normal

- Calorías ingeridas y peso
- Presión sanguínea
- Tamaño de los coches producidos por una máquina

# Introducción al muestreo y teorema central del límite

## Muestreo

La muestras es una estracción a la población. Es un contenido que sacamos sobre una población general y esta debe cumplir dos requisitos: que sean suficientemente grande para sacar una conclusión (estadísticamente significativo) y que esté no sesgada, que cumpla ciertos atributos.

- Técnica para la selección de una muestra.
- Se obtiene a partir de una población estadística.
- La selección tiene que ser aleatoria y se espera que sus propiedades sean extrapolables a la población.

### Tipos de muestreo

**Aleatorio simple**

Método de seleción de ciertas unidades sacadas de una población de manera que cada una de las muestras tiene la misma probabildiad de ser elegida. Ejempo: La lotería. Todos los numeros tienen la posibilidad de ser los ganadores.

**Sistemático**

Método de selección de ciertas unidades al azar y a continuación, se eligen el resto siguiendo intervalos regulares. Ejemplo: dar un premio a cada cien personas que hagan una inscripción hasta llegar a un total de mil inscritos.

**Estratificado**

Método de selección de ciertas unidades por segmentos exclusivos y homogéneos y a continuación se elige una muestra aleatoria simple de cada segmento. Ejemplo: división por edades.

## Teorema del límite central

Teoría estadística que establece que, dada una muestra aleatoria suficientemente grande de la población, la distribución de las medias seguirá una distribución normal. 

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%202.png)

Cuando repetimos multiples veces un experimentos, la mayoría de los casos van a estar siempre siguiendo esta distribución.

El teorema de límite central demuestra que las medias o promedios de diferentes muestras obtenidas de una misma distribución (ya sea una distribución normal, exponencial o gamma) van a darnos una distribución normal. 

Es decir, si de una población, tomamos varias muestras y de cada una de esas muestras calculamos la media, el conjunto de esas medias va a describir una distribución normal. Mientras más muestras más evidente es la distribución normal. Lo importante aqui’es entender que no importa el tipo de distribución de esa población, las medias de esas muestras siempre me darán una distribución normal. Eso demuestra el teorema,

# Media muestral

## Media

Suma de los datos dividida entre la cantidad de datos. La media ayuda a calcular el promedio.

## Moda

El dato que más se repite.

## Mediana

Es el dato que están en el centro de todos.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%203.png)

## Media muestral (media aritmética)

- Media aritmética = promedio = media
- Valor que se obtiene de sumar un conjunto de valores cuantitativos y dividirlo por el numero total de sumandos.
- Se simboliza con $\overline{X}$ y es diferente a la media poblacional $\mu$
- ejemplo: estimación puntual de la edad promedio de una población.

### Calculo de la varianza y desviación estandar

**Muestral**

**Poblacional**

$$
s=\sqrt{s^2}=\sqrt{\frac{\sum_{=1}^n(x_i-\bar{x})^2}{n-1}}
$$

$$
\sigma=\sqrt{\sigma^2}=\sqrt{\frac{\sum_{=1}^n(x_i-\mu)^2}{N}}
$$

- indica qué tan dispersos están los datos respecto a la media.
- **La desviación estándar es la raíz cuadrada de la varianza.**
- Ejemplo: edades de la población.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%204.png)

Desviación estándar de una clase donde los estudiantes tienen las siguientes edades: 28, 24, 25, 23, 38, 52. Sabemos que la edad promedio es 31.7

Varianza muestral = 43.8 y desviación estandar muestral = 6.62

# Intervalos de confianza

- un par o varios pares de números entre los cuales se estima que estará cierto valor desconocido, respecto de un parámetro poblacional con un determinado nivel de confianza.
- son simétricos respecto a la media

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%205.png)

Son un par o varios pares de números en los cuales se estima que estará cierto valor desconocido respecto  de un parámetro poblacional con un determinado valor de confianza, es decir que tendremos intervalos con nivel superior e inferior, y estos indicarán los valores dentro de estos parámetros cuales serán las poblaciones (la concentración de números).

## Nivel de significación

- El nivel de significación o alfa es el nivel límite para juzgar si un resultado es o no es estadísticamente significativo.
- Si el valor de significación es menor que el nivel de significación, el resultado es estadísticamente significativo.

El nivel de significación esta indicando cual es el alpha para encontrar si un límite es o no es estadísticamente significativo.  Cuando el valor es menor al valor de significación, no es significativo.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%206.png)

## Cálculo de intervalos de confianza

### Cuando no conocemos a la población

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%207.png)

La concentración tiene el 95% y el 5% estará distribuido en los máximos y mínimos. Para encontrar los límites se utiliza la tabla de z.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%208.png)

### Cuando se tiene conocimiento de la población

La duración en días de un cepillo de dientes se ajusta a la distribución normal (28,4) ¿Cuál es el intervalo de confianza al 80%?

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%209.png)

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2010.png)

[grafico intervalos deconfianza.webp](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/grafico_intervalos_deconfianza.webp)

¿Cuál es el valor a buscar en la tabla Z? Confianza + alpha/2  

# Prueba de hipótesis

La prueba de hipótesis o prueba de significación ayuda a juzgar si existe una diferencia significativa entre el tamaño de la muestra y el parámetro general.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2011.png)

1. Establecer una hipótesis nula (H0) y una hipótesis alternativa (H1)
2. Seleccionar el nivel de significancia.
3. Seleccionar el estadístico de prueba.
4. Formular la regla de decisión.
5. Interpretar los resultados y tomar una decisión.

## Significancia estadística

Cuando hacemos una prueba de hipótesis, buscamos significancia estadística para aceptar o rechazar.

Un resultado tiene significancia estadística cuando este tiene poca probabilidad de haber ocurrido dada la hipótesis nula. Para esto usamos el *p-value*.

### P-value

Es la probabilidad de obtener un valor que sea al menos tan extremo como el observado, considerando que la hipótesis nula sea verdadera.

Para que exista significancia, el p-value debe ser menor que 0.05, o en otros casos, menor que 0.01.

# Tipos de pruebas de hipótesis

![1_2hGMrCjLtVKtOKD_QnyuWA.png](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/1_2hGMrCjLtVKtOKD_QnyuWA.png)

## Distribución t de Student

Se usa para estimar una media de población normalmente distribuida a partir de una muestra pequeña que sigue una distribución normal y de la que desconocemos la desviación estandar.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2012.png)

## Coeficiento de Pearson

Se usa para medir la dependencia lineal (correlación) entre dos variables aleatorias cuantitativas.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2013.png)

Sucede cuando tenemos variables cuantitativas y vemos correlaciones. Si sube el valor de una variable que pasa con el resto, si subo una variable y sube la otra significa que estan correlacionadas positivamente y en efecto contrario es correlación negativa. 

![maxresdefault (10)-a3e58bc5-276f-4c8a-8751-d0645179415a.jpg](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/maxresdefault_(10)-a3e58bc5-276f-4c8a-8751-d0645179415a.jpg)

## Análisis de la varianza (ANOVA)

Se usa para comparar las varianzas entre las medias (o el promedio) de diferentes grupos.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2014.png)

![anlisis-de-la-varianza-2-320-a63afbc2-33ad-49d3-923a-4d1986389872.jpg](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/anlisis-de-la-varianza-2-320-a63afbc2-33ad-49d3-923a-4d1986389872.jpg)

# Tipos de errores

Las conclusiones a las que llegamos se basan en una muestra, por lo que podemos equivocarnos

**Decisones correctas**

**Decisiones incorrectas**

- Rechazar H0 cuando es falsa

- Rechazar H0 cuando es verdadera

- No rechazar H0 cuando es verdadera

- No rechazar H0 cuando es falsa

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2015.png)

**SABIENDO CUALES SON LAS CARACTERÍSTICAS QUE MÁS SE RELACIONAN CON LA VARIABLE OBJETIVO PODEMOS VER SI LAS PODEMOS DESCARTAR O NO AL CREAR NUESTRO MODELO DE MACHINE LEARNING O NUESTRA RED NEURONAL.** 

**PARA EL EJEMPLO DE IRIS LA VARIABLE OBJETIVO ES LA COLUMNA SPECIES, ENTONCES AL REALIZAR UN ANÁLISIS DE EXTRACCIÓN DE CARACTERÍSTICAS EL COEFICIENTO DE PEARSON NOS PERMITE SABER CUÁL ES LA RELACIÓN ENTRE ESTAS Y LA VARIABLE OBJETIVO.**

# Bootstrapping

- Método de remuestreo de datos dentro de una muestra aleatoria. Se usa para hallar una aproximación a la distribución de la variable analizada.
- Muy útil en muestras pequeñas o en distribuciones muy sesgadas.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2016.png)

Bootstrapping es un método de remuestreo con reemplazo ¿y qué es un remuestro con reemplazo? dado que partimos de una muestra, de esta muestra volvemos a obtener una muestra. Es decir, una muestra de la muestra. Y decimos con reemplazo porque la muestra original, siempre mantiene todos sus elementos. 

A los bootstraps los podemos obtener **n** veces. Por eso es un método que viene a ser muy versátil si usamos computadoras.

![1_SgeDm_wb2QNSF0CSYVmhuw.jpg](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/1_SgeDm_wb2QNSF0CSYVmhuw.jpg)

## ¿Por qué usar bootscrapping?

Porque es un método muy versátil y tenemos acceso al poder del computo necesario para hacerlo. 

Los métodos *t student* y de *pearson* asumen criterios de la población. Pero esto no siempre es así. No siempre podremos asumir ciertos parámetros y es aquí que bootscrapping se vuelve muy útil porque hace simulaciones de las muestras. Además, hoy en día es muy accesible la capacidad de cómputo para hacerlo (a menos que sea big data)

> Para realizar bootscrapping se debe tener al menos 25 registros y realizar mínimo 1000 simulaciones.
> 

# Validación cruazada

Técnica utilizada al final del análisis, sirve para evaluar los resultados de un análisis estadístico y garantizar que son independientes de la partición entre datos de entrenamiento y prueba. 

Sirven para demostrar que los datos de prueba son independientes de los datos de entrenamiento. 

Cuando estamos hablando de problemas o combinaciones dentro de IA vamos a crear dos grupos , con el fin que uno ajuste mejor que el otro. Uno no le aplicaremos ningún modelo estadístico y el otro será el que estemos modificando.  El objetivo final será validar y a partir de esa predicción, vamos ajustando más al modelo de origen.

## Procedimiento

- División de los datos de forma aleatoria en **k** grupos de un tamaño similar.
- Se usan k-1 grupos para entrenar el modelo y uno de ellos se usa para validarlo.
- El procedimiento se repite **k** veces usando un grupo distinto como validación en cada iteración.

![Untitled](Estadi%CC%81stica%20inferencial%20e7d8f227fd134540952baee6f4a07e72/Untitled%2017.png)

La idea de este modelo es tener una validación cruzada para poder comparar validaciones. Se repetirá k veces hasta llegar al resultado ideal donde la población de entrenamiento y de prueba se ajusten lo mejor posible.

De una seleción de la población estamos sacando una prueba, una pequeña muestra y de aquí vamos de iteración de la 1 hacia k, con el fin de evaluar y validar nuestro modelo final.

La validación cruzada es muy potente cuando usamos hiperparámetros en nuestros modelos, ya que aumenta la precisión considerablemente. Sin embargo es buena práctica balancear los datos, ya que en la vida real pasa siempre que tenemos una clase mayoritaria.

La evalución con una matriz de decisión es sumamente importante para detetectar falsos positivos y faltos negativos en nuestro modelo.