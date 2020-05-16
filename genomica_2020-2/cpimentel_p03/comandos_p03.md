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

Paper: < genomica_2020-2/cpimentel_p03/westbury2019.pdf >

En este paper se hizo un ensamble *de novo* usando reads a los que se les hicieron correcciones con un software ensamblador basado en k-meros llamado tadpole de bbtools; también se utilizaron librerías generadas para secuenciación en la plataforma Illumina HiSeq (3 de inserción corta y 3 pareadas) y las librerías pareadas de especies cruzadas (se generaron con el software Cross-Species Scaffolding utilizando genoma de beluga). El ensamble *de novo* se generó utilizando el software SOAPdenovo2. Los gaps fueron cerrados con el software Sealer. La continuidad del ensamble fue estimada con el software quast v4.5 y el contenido génico fue estimado con BUSCO (comparación de ortólogos universales de copia única) v3 y la base de datos de genes de mamíferos BUSCO.

##### Fuentes

-Ríos, E., Mejía-Ruiz, C. and Álvarez-Castañeda, S., 2009. Marcadores Moleculares: Una Revolución en la Zoología. CIENCIA, [en línea] pp.5-13. Disponible en: <http://revistaciencia.amc.edu.mx/images/revista/60_3/PDF/01-496-Marcadores-moleculares.pdf> [Fecha de acceso Mayo 13 2020].

-del Rosario Rodicio, M. and del Carmen Mendoza, M., 2004. Identificación bacteriana mediante secuenciación del ARNr 16S: fundamento, metodología y aplicaciones en microbiología clínica. Enfermedades Infecciosas y Microbiología Clínica, [en línea] 22(4), pp.238-245. Disponible en: <https://www.elsevier.es/es-revista-enfermedades-infecciosas-microbiologia-clinica-28-articulo-identificacion-bacteriana-mediante-secuenciacion-del-13059055>.


-Westbury, M., Petersen, B., Garde, E., Heide-Jørgensen, M. and Lorenzen, E., 2019. Narwhal Genome Reveals Long-Term Low Genetic Diversity despite Current Large Abundance Size. iScience, 15, pp.592-599.
___

## Parte II



___

## Parte III

___

## Parte IV
	