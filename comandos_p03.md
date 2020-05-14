# Comandos de la Práctica 03
## Miguel Ángel Rosas Paz

## Parte I. 
mkdir mrosas_p03
cd mrosas_p03
touch comandos_p03.md
mkdir data && mkdir filtered && mkdir raw_data && mkdir meta && mkdir scripts && mkdir figures && mkdir archive
mv filtered /home/genomica_2020-2/mrosas_p03/data 
mv raw_data /home/genomica_2020-2/mrosas_p03/data 
###01. 
 1.1 *Mycoplasma genitalum*
 1.2 Es el gen 16s de RNA ribosomal
 1.3 Los marcadores moleculares son son características del ADN que pueden diferenciar a dos o más individuos, y son heredables de generación en generación. Son, aquel fragmento de ADN polimórfico (con variaciones) que nos permita distinguir entre diferentes grupos taxonómicos (hasta nivel de especie o subespecie), poblaciones, familias o individuos (Ríos, *et al*., 2009).
 1.4 La importancia de este marcador yace en que se encuentra en todos los organismos conocidos. Su estructura parece mantenerse por largos periodos de tiempo y, como su función no ha cambiado, los cambios en la secuencia probablemente son aleatorios (Valenzuela-González, *et al*., 2015). 
###02. 
|BLAST (tipo de BLAST)|Definición                                                                                                                               |Aplicación|
|:...................:|:.......................................................................................................................................:|:........:|
|BLASTP               |Compara secuencias de aminoácidos con una secuencia proteica de la base de datos                                                         |
|BLASTN               |Compara secuencias nucleotídicas con secuencias de DNA de los bancos de datos                                                            |
|BLASTTX              |Compara una secuencia de nucleótidos (traducida a proteínas) respecto a una proteína                                                     |
|TBLASTN              |Compara una secuencia proteica con una secuencia nucleótidica de la base de datos traducida a todas sus pautas de lectura                |
|TBLASTX              |Compara los seis marcos de lectura de una secuencia de nucleótidos respecto  a las seis pautas de lectura de una secuencia de nucleótidos|
|QBLAST               |Permite a los usuarios seleccionar el tipo de archivo de salida, reduciendo el numero de conexiones a los servidores de NCBI             |  

###03.
En este caso el Software usado fue Bowtie. Lo primero que hicieron fue armar cuatro bibliotecas de DNA genómico de *R. toruloides* con tamaños que rondaban desde 200 pb hasta 2 y 6 kb, que fueron construidos con base en las plataformas de secuenciación de Ilumina Gaii. A partir de esto se obtuvieron datos que fueron ensamblados con el software SOAPdenovo para generar andamios del tamaño aproximado de levaduras como *Rhodotorula graminis*. Posteriormente, las lecturas se alineron con el es ensamblaje del genoma utilizando el softaware Bowtie para estimar la profundidad de secuenciación (Zhu, *et al*., 2012). 

## Parte II.

###01.
El problema de los puentes de Königsberg nos remonta al siglo XVII cuando la ciudad de
Königsberg (hoy en día llamada Kaliningrado) se encontraba dividida en cuatro áreas
debido al cruce del río Pregel. En ese entonces, siete puentes conectaban las distintas
áreas (Hevia, 1996).
Dado las particularidades del lugar, numerosas personas solían pasear y realizar
actividades diversas en las inmediaciones de los puentes. Los más ávidos y curiosos
solían entretenerse de distintas maneras, aunque al parecer, nada entretenía más que
plantearse la siguiente pregunta: ¿Es posible recorrer todas las zonas de la ciudad,
atravesando todos los puentes, una y sólo una vez cada uno de ellos? Diversas
connotaciones surgieron a partir de la planteación de esa pregunta. La mayoría de ellas
planteaba que no existía respuesta alguna. Que más bien era imposible responderla. Y de
hecho, así fue por algún tiempo hasta que un comité de jóvenes de la ciudad visitó a
Leonhard Euler, en 1735, para pedirle que resolviera tan conflictivo problema (Núñez, *et
al*., 2004).
El interés de Euler pronto se fijó al problema de Königsberg y tiempo después
presentó los resultados de su trabajo:
Euler logra representar una ruta mediante una sucesión de letras. Por ejemplo,
ABDC representa a la ruta que va de A a B, de B a D, y de D a C, atravesando tres
puentes. Si la ruta deseada existe, entonces su representación debe consistir de 8 letras
(ya que cada uno de los siete puentes debe cruzarse exactamente una vez). Euler se dio
cuenta de que esto no era posible dado la incidencia de las letra necesarias para cada
uno de los puentes; A debe aparecer tres veces (por sus 5 puentes); B, C y D debe
aparecer dos veces. Pero entonces, ya tendríamos nueve letras en la sucesión, cuando
para ser la ruta posible únicamente debería haber ocho. Euler dedujo entonces que no se
podía realizar la travesía requerida a través de los siete puentes de Königsberg (Hevia,
1996 y Núñez, *et al*., 2004).
Euler no se contentó sólo con solucionar esta situación concreta, sino que se
dedicó por completo al estudio del problema en general, obteniendo una solución que
servía también para cualquier número de puentes:
Para ello, el procedimiento que siguió Euler consistió en lo siguiente: en primer
lugar, apuntó en un papel el número de puentes más uno (ocho, en el caso de
Königsberg).

Después, abajo a la izquierda formó una columna con todas las letras de las
regiones (A, B, C y D, en este caso).

A su derecha, formó una segunda columna con el número de puentes que salen
de cada una de las correspondientes zonas (5, 3, 3 y 3, en este caso), marcando con un
asterisco aquellas letras de las que salen un número par de puentes.

A continuación realizó las siguientes operaciones con los números de la segunda
columna: si el número de la segunda columna (número de puentes que llegan a una
determinada región) es impar, lo aumentó en una unidad y lo dividió entre dos. Si el
número es par, lo dividió entre dos. Euler colocó finalmente a la derecha una tercera
columna con las cuentas anteriormente especificadas (3, 2, 2, 2, en nuestro caso). Euler
dedujo entonces que el problema sólo tendría solución si la suma de los números de la
última columna es menor o igual que el número inicialmente puesto. Más concretamente,
si esta suma es igual al número inicial (8, en este caso), la ruta comienza en una zona no
marcada con asterisco, y si es menor, en una señalada. En el caso de Königsberg, esta
suma es nueve, no menor o igual que ocho, por lo que no hay solución al problema de los
puentes de Königsberg (Núñez, *et al*., 2004).
## Referencias 
Hevia, H. (1996). El Problema de los Siete Puentes de Konigsberg: Leonhard Euler y la Teoria de Grafos. *Educación matemática* 8(1)
Núñez Valdés, J., Alfonso Pérez, M., Bueno Guillén, S., Diánez del Valle, M. D. R., y Elías Olivenza, M. D. C. D. (2004). Siete puentes, un camino: Königsberg. *Suma: revista sobre la enseñanza y aprendizaje de las matemáticas*, 45, 69-78.
Ríos, E., Ruiz, H. M., y Castañeda, S. T. (2009). Marcadores moleculares: una revolucion en la Zoología. Obtenido de http://www. revistaciencia. amc. edu. mx/images/revista/60_3/PDF/01-496-Marcadores-moleculares. pdf.
Valenzuela-González, F., Casillas-Hernández, R., Villalpando, E. y Vargas-Albores, F. (2015). El gen ARNr 16S en el estudio de comunidades microbianas marinas. *Ciencias marinas*, 41(4), 297-313.
Zhu, Z., Zhang, S., Liu, H., Shen, H., Lin, X., Yang, F. y Zhao, Z. K. (2012). A multi-omic map of the lipid-producing yeast *Rhodosporidium toruloides*. *Nature communications*, 3(1), 1-12.