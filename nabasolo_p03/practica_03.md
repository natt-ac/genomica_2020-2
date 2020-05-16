#Comandos de la Práctica 03. Genómica Computacional
#Natalia Abasolo Cortés

##01. `mkdir nabasolo_p03`
##02. `touch practica_03.md`

#Parte I.
##01. 
1.1 ¿A qué organismo pertenece? A *Mycoplasma genitalium*
1.2 ¿Es un gen o una región genómica de importancia? Es una gen de importancia
1.3 ¿Qué es un marcador molecular? Es un gen o segmento de ADN con una ubicación 
identificada y que se conserva a través de las especies y su descendencia.
1.4 ¿Cuál es la importancia de este tipo de marcador en particular? Que se encuentra
en una gran cantidad de especies de seres vivos.
##02. Tipos de BLAST
| BLAST   | Definición                                                                                                                                                            | Aplicación                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| BLASTP  | Compara secuencias de aminoácidos<br>con una secuencia proteica de la base de datos.                                                                                  | Buscar posibles individuos<br>relacionados entre sí.             |
| BLASTX  | Compara una secuencia de nucleótidos(traducida<br>a proteínas, con todas sus posibles pautas de <br>lectura) respecto a una proteína de la base de<br>datos.          | Establecer posibles proteínas<br>similares entre individuos.<br> |
| TBLASTN | Compara una secuencia proteica con una secuencia<br>nucleotidica de la base de datos traducida a <br>todas sus pautas de lectura.                                     | Encontrar relaciones cuando<br>tienes información más general.   |
| TBLASTX | Compara los seis marcos de lectura de una <br>secuencia de nucleótidos respecto las seis<br>pautas de lectura de una secuencia de nucleótidos<br>de la base de datos. | Encontrar una relación con un<br>nivel de certeza más confiable. |

##03. ["Clonal genome evolution and rapid invasive spread of the marbled crayfish"](https://doi.org/10.1038/s41559-018-0467-9)
Metodología
Los datos de secuenciación de todos los individuos (cangrejos de río marmolados, _P. fallax_ y _P. alleni_) se mapearon en el genoma de referencia de cangrejos de río marmolados utilizando Bowtie2 (2.2.6). 
Posteriormente, se extrajo un subconjunto de secuencias de más de 10 kb. La llamada variante se realizó usando Freebayes (0.9.21-g7dd41db). Se realizó asignación y eliminación para filtrar posibles sitios de error de mapeo. 

Las mutaciones genéticas de la población se cuantificaron mediante el mapeo de datos leídos al genoma de referencia, como se describió anteriormente. Se requirió que cada sitio tuviera un genotipo válido (según lo determinado por Freebayes) en todas las muestras. Los árboles filogenéticos se generaron en base a información de polimorfismo en parejas entre diferentes especies de Procambarus y entre diferentes animales cangrejos de río marmolados.

Gutekunst, J., Andriantsoa, R., Falckenhayn, C. et al. _Clonal genome evolution and rapid invasive spread of the marbled crayfish._ Nat Ecol Evol 2, 567–573 (2018). 

#Parte II.
##01. 
¿En que consiste el problema de los puentes de la ciudad de Königsberg? Se basa en encontrar un camino o ruta
que permita cruzar los 7 puestes que hay en la ciudad pero sin cruzar uno de ellos mas que una vez.
¿Por qué no tiene solución? No tiene solución ya que debido a que, para cumplir la condición, cada puente solo puede ser considerado como entrada o salida, lo que hace que no sean suficientes y alguno tenga que ser cruzado dos veces en algún momento.

##02. Tres problemáticas comunes en la aplicación de las gráficas de Bruijin a genomas
   1. Los genomas en el proceso de ser secuenciados generan una gran cantidad de lecturas y por ende, datos que para analizar con este tipo de algoritmo, es muy difícil y tardado de procesar.
   2. Aún no existe un algoritmo que genere una respuesta óptima al problema que se intenta resolver al hacer alineamientos.
   3. Existen problemas computacionales, como encontrar un ciclo de Hamilton, que pertenece a una clase de problemas que se denominan colectivamente NP-Complete, pero actualmente no han encontrado solucion a alguno de estos problemas pero a su vez no se ha podido demostrar que son imposibles de resolver.

##03. Estadísticas N50 y L50
¿Qué son? Son estadísticas de un conjunto de longitudes de contig o andamio. 
¿En qué consisten? N50 considera que el  50% de todo el conjunto está en contigs o scaffolds igual o mas largos.
L50 se define como el menor número de contigs, dado que el largo de sus sumas es igual a N50. Los valores solo son significativos cuando, comparado con el tamaño del genoma base es iggual en todos los casos.
¿Para qué se usan? Para exponer la "integridad" de un conjunto de genoma, pero esencialmente se utilizan para describir la frecuencia de la longitud de los contigs.