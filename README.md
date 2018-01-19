# Curso-RNAseq-UNAM-2014
Este es material creado para el curso de RNAseq de Cuernavaca, México, de la UNAM, 2014

Sería conveniente comenzar a leer el LEEME, en el cual se explica de forma basica como crear nuestro directorio de trabajo, y algunas otras tareas que nos preparan para seguir el tutorial. Una vez hecho esto, ya se puede comenzar con los ficheros HOWTO en orden numerico.

En el HOWTO_0 se obtienen los datos con los que se trabaja el resto del curso, y se echa un primer vistazo al aspecto de un ficheros con reads de secuenciacion. Ademas, se cuenta el numero de reads y se comprueba que cada read cuenta con su pareja.

En el HOWTO_1 se realiza la comprobacion de calidad de los reads, asi como un preprocesamiento de los datos para eliminar aquellos reads de peor calidad. Para ello se utilizan las herramientas FastQC y Trimmomatic. A continuacion, se realiza un paso opcional para tratar de corregir errores de secuenciacion, mediante la herramienta Musket.

En el HOWTO_2 se lleva a cabo un ensamblaje de novo de los reads de secuenciacion, con el programa Trinity. A continuacion, se realinean los reads al ensamblaje para comprobar la calidad de este por visualizacion de algunos mapeos mediante la herramienta IGV.

En el HOWTO_3 se utiliza GMAP para alinear los contigs obtenidos en el ensamblaje de novo, para compararlos con ua referencia de calidad que tengamos, y así comprobar la calidad del ensamblaje. Posteriormente, se aprovecha el alineamiento para realizar una anotacion estructural de nuestros ensamblajes, y se visualizan los resultados con IGB y GenomeViewer. Finalmente, se utiliza Transdecoder, para llevar a cabo una identificacion de ORFs de novo, que podemos utilizar con aquellos transcritos que no alineen bien a nuestra referencia.

En el HOWTO_4 se cambia de estrategia: en lugar de realizar un ensamblaje de novo, se analizan los reads por medio de alineamientos a un genoma de referencia. Para ello mapeamos los reads con TopHat2, y a continuacion se utiliza Cufflinks para obtener un ensamblaje. A continuacion, se utiliza Cuffcompare para comparar anotaciones previas y las nuevas obtenidas con nuestros datos, y con Cuffmerge se crea una nueva anotacion.

En el HOWTO_5 se utilizan los mapeos que hemos obtenido para tratar de identificar polimorfismos (SNPs e indels) en nuestras muestras. Primero se eliminan duplicados de nuestros mapeos, y luego se utilizan samtools y bcftools para identificar las variantes. Por ultimo se explica integrar las variantes en el visualizador IGV.

En el HOWTO_6 se realizan análisis de expresión de los datos de RNAseq. Por un lado, se analiza la expresion con nuestros datos basados en genoma de referencia. Para ello utilizamos Cuffdiff, y aprovechamos cummeRbund para visualizar algunos resultados. Por otro lado, partimos de los datos basados en el ensamblaje de novo. En este caso utilizamos RSEM para obtener conteos y edgeR para el analisis de expresion diferencial.

Y eso es todo.
Carlos P Cantalapiedra
