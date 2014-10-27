## Introducción (I)

<a class="fancybox" href="img/scheduler.png" data-fancybox-group="gallery" title="Volumenes físicos">
<img height="550px" src="img/scheduler.redimensionado640x480.png" alt="Volumenes físicos">
</a>

<aside class="notes">
* Regular computer backup is important, but precisely how regularly is a matter that varies from one system to another.
* You’ll have to decide for yourself just how frequently your systems require backup.
* El número de medios para hacer esas copias es limitado, cómo los reutilizamos para tener copias de seguridad lo más "útiles posibles".
</aside>



## Introduccíon (II)

* Para realizar una buena política de copías de seguridad hay que tener en cuenta una serie de [Factores](#/4/3)
* Dependiende de las características propias de mi sistema problemos aplicar polícas tipo:
 * [FIFO](#/4/4)
 * [Grandfather-father-son](#/4/5)
 * [Torres de Hanoi](#/4/6)



## Factores

* Antes de optar por una política de copias de seguridad u otra hay que responder a las siguientes preguntas:

<ul>
<li class="fragment fade-in">
¿Cambian muchos los datos?
</li>
<li class="fragment fade-in">
¿Cuánto tarda en hacerse la copia?
</li>

<li class="fragment fade-in">
¿Cuánto tarda en recuperarse la copia?
</li>
</ul>

note:

* Take into consideration factors such as
 * how often the data change, the importance of the data,
 * the cost of recovering the data without a current backup,
 * the cost of making a backup. Costs may be measured in money,
* Cost = money, time, productivity. sales..




## First In, First Out

<a class="fancybox" href="img/fifo.png" data-fancybox-group="gallery" title="Política FIFO">
<img height="550px" src="img/fifo.png" alt="Política FIFO">
</a>

note:
* Saves new or modified files onto the "oldest" media in the set
* Performing a daily backup onto a set of 14 media, the backup depth would be 14 days.
* Each day, the oldest media would be inserted when performing the backup.
* This is the simplest rotation scheme, and is usually the first to come to mind.



## Grandfather-father-son

<a class="fancybox" href="img/gfs.png" data-fancybox-group="gallery" title="Política GFS">
<img height="550px" src="img/gfs.redimensionado640x480.png" alt="Política GFS">
</a>

<aside class="notes">
* In this scheme there are three or more backup cycles, such as daily, weekly and monthly.
* The daily backups are rotated on a daily basis using a FIFO system as above.
* The weekly backups are similarly rotated on a weekly basis, and the monthly backup on a monthly basis.
* In addition, quarterly, half-yearly, and/or annual backups could also be separately retained.
* Often some of these backups are removed from the site for safekeeping and disaster recovery purposes.
</aside>



## Torres de Hanoi

Para tres medios de almacenamiento

|    Día  | 01  | 02 | 03 | 04 | 05 | 06 | 07 | 08 |
|---------|-----|----|----|----|----|----|----|----|
|         | A   |    | A  |    | A  |    | A  |    |
|Conjunto |     | B  |    |    |    | B  |    |    |
|         |     |    |    | C  |    |    |    |  C |

Para cuatro medios de almacenamiento

|    Día  | 01  | 02 | 03 | 04 | 05 | 06 | 07 | 08 | 09 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|---------|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|         | A   |    | A  |    | A  |    | A  |    | A  |    | A  |    |  A |    | A  |    |
|Conjunto |     | B  |    |    |    | B  |    |    |    | B  |    |    |    | B  |    |    |
|         |     |    |    | C  |    |    |    |    |    |    |    | C  |    |    |    |    |
|         |     |    |    |    |    |    |    |  D |    |    |    |    |    |    |    | D  |

note:
* A set of n tapes (or other media) will allow backups for 2 n-1 days before the last set is recycled. So, three tapes will give four days' worth of backups and on the fifth day Set C will be overwritten; four tapes will give eight days, and Set D is overwritten on the ninth day; five tapes will give 16 days, etc. Files can be restored from 1, 2, 4, 8, 16, ..., 2 n - 1 days ago.



## Ejemplo

<a class="fancybox" href="img/ejemplo_scheduler.png" data-fancybox-group="gallery" title="Ejemplo planificación">
<img height="550px" src="img/ejemplo_scheduler.redimensionado640x480.png" alt="Ejemplo planificación">
</a>
