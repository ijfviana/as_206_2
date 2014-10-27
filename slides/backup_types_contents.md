## Tipos de copias

* [Completa](#/3/1)
* [Diferencial](#/3/2)
* [Incremental](#/3/3)



### Completa

<a class="fancybox" href="img/completa.png" data-fancybox-group="gallery" title="Copias completas">
<img height="550px" src="img/completa.redimensionado75.png" alt="Copias completas">
</a>

note:

* En un backup completo de todos los archivos seleccionados en el plan de copias.
* Cada vez que se realiza una copia completa, el sistema operativo pone el bit de copia del archivo salvaguardado (también llamado bit de modificación) a 0,
* Este bit volverá a 1 en el momento en que el archivo sea modificado.
* Ventajas:
 * Todos los archivos de las carpetas y unidades seleccionadas están respaldados hasta un conjunto de copia de seguridad.
 * En caso de que necesite restaurar archivos, restaurar fácilmente desde un único conjunto de copia de seguridad.
* Desventajas:
  * Una copia de seguridad completa consume más tiempo que otras opciones de copia de seguridad.
  * Copias de seguridad completas requieren más espacio de la unidad de red, cinta o disco.



### Diferencial

<a class="fancybox" href="img/diferencial.png" data-fancybox-group="gallery" title="Copias diferenciales">
<img height="550px" src="img/diferencial.redimensionado75.png" alt="Copias diferenciales">
</a>

note:
* Se salvaguardan solamente los datos que han sido modificados desde la última copia de seguridad completa que se realizó.
* Ventajas:
 * Ocupan menos espacio y tiempo
* Desventajas:
 * Tardan más al restaurarse al necesitar la copia completa




### Incremental

<a class="fancybox" href="img/incremental.png" data-fancybox-group="gallery" title="Copias incrementales">
<img height="550px" src="img/incremental.redimensionado75.png" alt="Copias incrementales">
</a>

note:
* Solo almacenará la información que haya sido modificada desde la última copia de seguridad realizada, ya sea completa, diferencial o incremental, da lo mismo.
* Ventajas:
 * Es la que menos espacio y tiempo ocupa
* Desventajas
 * Hay que restaurar antes las copias completas, diferenciales e incrementales.
