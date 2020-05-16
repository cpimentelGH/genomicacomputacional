# Comandos de la Práctica 03
## Carlos Pimentel Ruíz

___

## Parte I

1. Secuencia x para copiar y pegar en BLAST.

~~~
>sequence_x
AGAGTTTGATCCTGGCTCAGGATTAACGCTGGCGGCATGCCTAATACATGCAAGTCGAT
CGGAAGTAGCAATACTTTAGAGGCGAACGGGTGAGTAACACGTATCCAATCTACCTTAT
AATGGGGGATAACTAGTTGAAAAACTAGCTAATACCGCATAAGAACTTTAGTTCGCATG
AATTAAAGTTGAAAGGACCTGCAAGGGTTCGTTATTTGATGAGGGTGCGCCATATCAGC
TAGTTGGTAGGGTAATGGCCTACCAAGGCAATGACGTGTAGCTATGCTGAGAAGTAGAA
TAGCCACAATGGGACTGAGACACGGCCCATACTCCTACGGGAGGCAGCAGTAGGGAATT
TTTCACAATGAGCGAAAGCTTGATGGAGCAATGCCGCGTGAACGATGAAGGTCTTTTTG
ATTGTAAAGTTCTTTTATTTGGGAAGAATGACTCTAGCAGGCAATGGCTGGAGTTTGAC
TGTACCACTTTGAATAAGTGACGACTAACTATGTGCCAGCAGTCGCGGTAATACATAGG
TCGCAAGCGTTATCCGGATTTATTGGGCGTAAAGCAAGCGCAGGCGGATTGAAAAGTCT
GGTGTTAAAGGCAGCTGCTTAACAGTTGTATGCATTGGAAACTATCAGTCTAGAGTGTG
GTAGGGAGTTTTGGAATTTCATGTGGAGCGGTGAAATGCGTAGATATATGAAGGAACAC
CAGTGGCGAAGGCGAAAACTTAGGCCATTACTGACGCTTAGGCTTGAAAGTGTGGGGAG
CAAATAGGATTAGATACCCTAGTAGTCCACACCGTAAACGATAGATACTAGCTGTCGGA
GCGATCCCTTCGGTAGTGAAGTTAACACATTAAGTATCTCGCCTGGGTAGTACATTCGC
AAGAATGAAACTCAAACGGAATTGACGGGGACCCGCACAAGTGGTGGAGCATGTTGCTT
AATTCGACGGTACACGAAAAACCTTACCTAGACTTGACATCCTTGGCAAAGTTATGGAA
ACATAATGGAGGTTAACCGAGTGACAGGTGGTGCATGGTTGTCGTCAGCTCGTGTCGTG
AGATGTTGGGTTAAGTCCCGCAACGAGCGCAACCCTTATCGTTAGTTACATTGTTTAAC
GAGACTGCTAATGTAAATTGGAGGAAGGAAGGGATGACGTCAAATCATCATGCCCCTTA
TGTCTAGGGCTGCAAACGTGCTACAATGGCCAATACAAACAGTAGCCAACTTGTAAAAG
TGAGCAAATCTGAAAAGTTGGTCTCAGTTCGGATTGAGGGCTGCAATTCGTCCTCATGA
AGCTGGAATCACTAGTAATCGCGAATCAGCTATGTCGCGGTGAATACGTTCTCGGGTCT
TGTACACACCGCCCGTCAAACTATGAAAGCTGGTAATATTTAAAAACGTGTTGCTAACC
TTTATTGGAAGCGCATGTCAAGGATAGCACCGGTGATTGGAGTTAAGTCGTAACAAGGT
ACCCCTACGAGAACG
~~~

1.1 ¿A qué organismo pertenece?

 *Mycoplasma genitalium*

1.2 ¿Es un gen o una región genómica de importancia?

 Gen ARNr 16S

1.3 ¿Qué es un marcador molecular?

 Es un fragmento de DNA polimórfico (con variaciones) que permite distinguir entre diferentes grupos taxonómicos, poblaciones o individuos. Estos marcadores muchas veces son utilizados como estimadores de la historia evolutiva de los organismos ya que se evalúan relaciones filogenéticas en distintos niveles de organización.

1.4. ¿Cuál es la importancia de este tipo de marcador en particular?

 El ARN ribosómico 16S (ARNr 16S) es utilizado en estudios de filogenia y taxonomía de bacterias ya que se encuentra altamente conservado, presentado regiones comunes en todos los organismos pero con variaciones en zonas específicas. 

2. Tabla comparativa programas BLAST


| BLAST 	| Definición 	| Aplicación 	|
|:-------:	|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:	|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:	|
| blastn 	| Nucleotide Blast. Requiere de un query de nucleótidos para buscarlo en una base de datos de nucleótido mediante un alineamiento de nucleótidos. 	| -Identificación de secuencias de nucleótidos.<br><br>-Comparación intraespecífica de secuencias.<br><br>-Comparación interespecífica de secuencias.<br><br>-Búsqueda de pequeños queries en una comparación interespecífica. 	|
| blastp 	| Protein Blast. Requiere un query de aminoácidos para buscarlo en una base de datos de proteínas (secuencia de aminoácidos) mediante un alineamiento de aminoácidos. 	| -Identificación de la secuencia general y búsqueda de similitudes. 	|
| blastx 	| Requiere de un query de nucleótidos que es traducido en una secuencia de aminoácidos y se busca en una base de datos de proteínas (secuencia de aminoácidos) mediante un alineamiento de aminoácidos. 	| -Identificar potenciales productos proteicos codificados por un<br>query de nucleótidos. 	|
| tblastn 	| Necesita un query de aminoácidos para buscarlo en bases de datos generadas por secuencias de nucleótidos traducidas. Esto es mediante un alineamiento de secuencias de aminoácidos. 	| -Identificar secuencias de bases de datos que codifican para proteínas similares a la del query. 	|
| tblastx 	| Se necesita de un query de nucleótidos que se traduce en una secuencia de aminoácidos y se busca en una base de datos generada por secuencias de nucleótidos traducidas en secuencias de aminoácidos mediante un alineamiento de secuencias de aminoácidos. 	| -Identificar secuencias de nucleótidos similares al query basándose en su potencial de codificación. 	|


3. Metodología de Mapeo.

[Narwhal Genome Reveals Long-Term Low Genetic Diversity despite Current Large Abundance Size][Artículo]

[Artículo]: https://www.sciencedirect.com/science/article/pii/S2589004219300896

En este paper se hizo un ensamble *de novo* usando reads a los que se les hicieron correcciones con un software ensamblador basado en k-meros llamado tadpole de bbtools; también se utilizaron librerías generadas para secuenciación en la plataforma Illumina HiSeq (3 de inserción corta y 3 mate paired) y las librerías mate paired de especies cruzadas (se generaron con el software Cross-Species Scaffolding utilizando genoma de beluga). El ensamble *de novo* se generó utilizando el software SOAPdenovo2. Los gaps fueron cerrados con el software Sealer. La continuidad del ensamble fue estimada con el software quast v4.5 y el contenido génico fue estimado con BUSCO (comparación de ortólogos universales de copia única) v3 y la base de datos de genes de mamíferos BUSCO.

##### Fuentes

- Ríos, E., Mejía-Ruiz, C. and Álvarez-Castañeda, S., 2009. Marcadores Moleculares: Una Revolución en la Zoología. CIENCIA, [en línea] pp.5-13. Disponible en: <http://revistaciencia.amc.edu.mx/images/revista/60_3/PDF/01-496-Marcadores-moleculares.pdf> [Fecha de acceso Mayo 13 2020].

- del Rosario Rodicio, M. and del Carmen Mendoza, M., 2004. Identificación bacteriana mediante secuenciación del ARNr 16S: fundamento, metodología y aplicaciones en microbiología clínica. Enfermedades Infecciosas y Microbiología Clínica, [en línea] 22(4), pp.238-245. Disponible en: <https://www.elsevier.es/es-revista-enfermedades-infecciosas-microbiologia-clinica-28-articulo-identificacion-bacteriana-mediante-secuenciacion-del-13059055>.


- Westbury, M., Petersen, B., Garde, E., Heide-Jørgensen, M. and Lorenzen, E., 2019. Narwhal Genome Reveals Long-Term Low Genetic Diversity despite Current Large Abundance Size. iScience, 15, pp.592-599.
___

## Parte II

1. Puentes de la Ciudad de Königsberg

1.1 ¿En qué consiste el problema de los puentes de la ciudad de Königsberg?

 La ciudad de Königsberg se encontraba distribuida en cuatro superficies terrestres conectadas por 7 puentes. El problema consiste en encontrar la ruta que le permita a una persona cruzar los siete puentes sin pasar por ellos más de una vez.

1.2 ¿Por qué no tiene solución?

 De acuerdo con lo propuesto por Euler, llamado en ese momento geometría de la posición y ahora recibe el nombre de teoría de grafos. Este razonamiento permite visualizar la Ciudad de Königsberg en **nodos** (las 4 masas terrestres) y **vértices** (los 7 puentes) además de un término que es el **grado** de los nodos (el número de puentes que tienen contacto con esa masa de tierra). 

 La ruta que recorre los nodos pasando por los ejes recibe el nombre de **Camino Euleriano** y según la teoría propuesta, un camino, podrá pasar sólo una vez por todos los ejes siempre y cuando exista alguna de de estas dos situaciones:

 - Hay dos nodos de grado impar, indicando que los restantes tienen un grado par. Por lo tanto, el nodo de inicio es uno de los nodos de grado impar y el nodo de término es el otro nodo de grado impar.

 - Se forma un **Circuito Euleriano**; esto quiere decir que todos los nodos tienen un grado par y el nodo de inicio será el mismo que el nodo de término.

**Conclusión:** Este problema no tiene solución porque tenemos cuatro nodos con grado 3, 5, 3 y 3 respectivamente, por lo que no es posible pasar por todos los puentes sin repetir alguno. La solución es destruir cualquiera de los puentes lo que nos dejaría al menos 2 nodos con grado impar y la solución se daría por la situación 1.

2.Problemáticas comunes en la aplicación de las gráficas de Bruijin a genomas.

3.Estadísticas N50 y L50.

3.1 N50
 - ¿Qué es?
 - ¿En qué consiste?

3.2 L50
 - ¿Qué es?
 - ¿En qué consiste?
___

## Parte III

___

## Parte IV
	