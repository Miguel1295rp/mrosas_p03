# Comandos de la Pr�ctica 03
## Miguel �ngel Rosas Paz

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
 1.3 Los marcadores moleculares son son caracter�sticas del ADN que pueden diferenciar a dos o m�s individuos, y son heredables de generaci�n en generaci�n. Son, aquel fragmento de ADN polim�rfico (con variaciones) que nos permita distinguir entre diferentes grupos taxon�micos (hasta nivel de especie o subespecie), poblaciones, familias o individuos (R�os, *et al*., 2009).
 1.4 La importancia de este marcador yace en que se encuentra en todos los organismos conocidos. Su estructura parece mantenerse por largos periodos de tiempo y, como su funci�n no ha cambiado, los cambios en la secuencia probablemente son aleatorios (Valenzuela-Gonz�lez, *et al*., 2015). 
###02. 
|BLAST (tipo de BLAST)|Definici�n                                                                                                                               |Aplicaci�n|
|:...................:|:.......................................................................................................................................:|:........:|
|BLASTP               |Compara secuencias de amino�cidos con una secuencia proteica de la base de datos                                                         |
|BLASTN               |Compara secuencias nucleot�dicas con secuencias de DNA de los bancos de datos                                                            |
|BLASTTX              |Compara una secuencia de nucle�tidos (traducida a prote�nas) respecto a una prote�na                                                     |
|TBLASTN              |Compara una secuencia proteica con una secuencia nucle�tidica de la base de datos traducida a todas sus pautas de lectura                |
|TBLASTX              |Compara los seis marcos de lectura de una secuencia de nucle�tidos respecto  a las seis pautas de lectura de una secuencia de nucle�tidos|
|QBLAST               |Permite a los usuarios seleccionar el tipo de archivo de salida, reduciendo el numero de conexiones a los servidores de NCBI             |  

###03.
En este caso el Software usado fue Bowtie. Lo primero que hicieron fue armar cuatro bibliotecas de DNA gen�mico de *R. toruloides* con tama�os que rondaban desde 200 pb hasta 2 y 6 kb, que fueron construidos con base en las plataformas de secuenciaci�n de Ilumina Gaii. A partir de esto se obtuvieron datos que fueron ensamblados con el software SOAPdenovo para generar andamios del tama�o aproximado de levaduras como *Rhodotorula graminis*. Posteriormente, las lecturas se alineron con el es ensamblaje del genoma utilizando el softaware Bowtie para estimar la profundidad de secuenciaci�n (Zhu, *et al*., 2012). 

## Parte II.

###01.
El problema de los puentes de K�nigsberg nos remonta al siglo XVII cuando la ciudad de
K�nigsberg (hoy en d�a llamada Kaliningrado) se encontraba dividida en cuatro �reas
debido al cruce del r�o Pregel. En ese entonces, siete puentes conectaban las distintas
�reas (Hevia, 1996).
Dado las particularidades del lugar, numerosas personas sol�an pasear y realizar
actividades diversas en las inmediaciones de los puentes. Los m�s �vidos y curiosos
sol�an entretenerse de distintas maneras, aunque al parecer, nada entreten�a m�s que
plantearse la siguiente pregunta: �Es posible recorrer todas las zonas de la ciudad,
atravesando todos los puentes, una y s�lo una vez cada uno de ellos? Diversas
connotaciones surgieron a partir de la planteaci�n de esa pregunta. La mayor�a de ellas
planteaba que no exist�a respuesta alguna. Que m�s bien era imposible responderla. Y de
hecho, as� fue por alg�n tiempo hasta que un comit� de j�venes de la ciudad visit� a
Leonhard Euler, en 1735, para pedirle que resolviera tan conflictivo problema (N��ez, *et
al*., 2004).
El inter�s de Euler pronto se fij� al problema de K�nigsberg y tiempo despu�s
present� los resultados de su trabajo:
Euler logra representar una ruta mediante una sucesi�n de letras. Por ejemplo,
ABDC representa a la ruta que va de A a B, de B a D, y de D a C, atravesando tres
puentes. Si la ruta deseada existe, entonces su representaci�n debe consistir de 8 letras
(ya que cada uno de los siete puentes debe cruzarse exactamente una vez). Euler se dio
cuenta de que esto no era posible dado la incidencia de las letra necesarias para cada
uno de los puentes; A debe aparecer tres veces (por sus 5 puentes); B, C y D debe
aparecer dos veces. Pero entonces, ya tendr�amos nueve letras en la sucesi�n, cuando
para ser la ruta posible �nicamente deber�a haber ocho. Euler dedujo entonces que no se
pod�a realizar la traves�a requerida a trav�s de los siete puentes de K�nigsberg (Hevia,
1996 y N��ez, *et al*., 2004).
Euler no se content� s�lo con solucionar esta situaci�n concreta, sino que se
dedic� por completo al estudio del problema en general, obteniendo una soluci�n que
serv�a tambi�n para cualquier n�mero de puentes:
Para ello, el procedimiento que sigui� Euler consisti� en lo siguiente: en primer
lugar, apunt� en un papel el n�mero de puentes m�s uno (ocho, en el caso de
K�nigsberg).

Despu�s, abajo a la izquierda form� una columna con todas las letras de las
regiones (A, B, C y D, en este caso).

A su derecha, form� una segunda columna con el n�mero de puentes que salen
de cada una de las correspondientes zonas (5, 3, 3 y 3, en este caso), marcando con un
asterisco aquellas letras de las que salen un n�mero par de puentes.

A continuaci�n realiz� las siguientes operaciones con los n�meros de la segunda
columna: si el n�mero de la segunda columna (n�mero de puentes que llegan a una
determinada regi�n) es impar, lo aument� en una unidad y lo dividi� entre dos. Si el
n�mero es par, lo dividi� entre dos. Euler coloc� finalmente a la derecha una tercera
columna con las cuentas anteriormente especificadas (3, 2, 2, 2, en nuestro caso). Euler
dedujo entonces que el problema s�lo tendr�a soluci�n si la suma de los n�meros de la
�ltima columna es menor o igual que el n�mero inicialmente puesto. M�s concretamente,
si esta suma es igual al n�mero inicial (8, en este caso), la ruta comienza en una zona no
marcada con asterisco, y si es menor, en una se�alada. En el caso de K�nigsberg, esta
suma es nueve, no menor o igual que ocho, por lo que no hay soluci�n al problema de los
puentes de K�nigsberg (N��ez, *et al*., 2004).
## Referencias 
Hevia, H. (1996). El Problema de los Siete Puentes de Konigsberg: Leonhard Euler y la Teoria de Grafos. *Educaci�n matem�tica* 8(1)
N��ez Vald�s, J., Alfonso P�rez, M., Bueno Guill�n, S., Di�nez del Valle, M. D. R., y El�as Olivenza, M. D. C. D. (2004). Siete puentes, un camino: K�nigsberg.�*Suma: revista sobre la ense�anza y aprendizaje de las matem�ticas*, 45, 69-78.
R�os, E., Ruiz, H. M., y Casta�eda, S. T. (2009). Marcadores moleculares: una revolucion en la Zoolog�a. Obtenido de http://www. revistaciencia. amc. edu. mx/images/revista/60_3/PDF/01-496-Marcadores-moleculares. pdf.
Valenzuela-Gonz�lez, F., Casillas-Hern�ndez, R., Villalpando, E. y Vargas-Albores, F. (2015). El gen ARNr 16S en el estudio de comunidades microbianas marinas. *Ciencias marinas*, 41(4), 297-313.
Zhu, Z., Zhang, S., Liu, H., Shen, H., Lin, X., Yang, F. y Zhao, Z. K. (2012). A multi-omic map of the lipid-producing yeast *Rhodosporidium toruloides*. *Nature communications*, 3(1), 1-12.