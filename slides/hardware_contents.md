## Introducción

<aside class="notes">
* Just about any device that can store computer data and read it back can be used as a backup medium.
* The best backup devices are inexpensive, fast, high in capacity, and reliable.
* They don’t usually need to be random-access devices, though. Random-access devices are capable of quickly accessing any piece of data.
* Hard disks, CD-ROMs, and DVDs are all random-access devices.
* These devices contrast with sequential-access devices, which must read through all intervening data before accessing the sought-after component.
* Tapes are the most common sequential-access devices.
* Table 4.9 summarizes critical information about the most common types of backup device. For some such as tape, there are higher-capacity (and more expensive) devices for network backups.
</aside>

* [Dispositivos ópticos](#/5/2)
* [Discos duros](#/5/3)
* [Cintas](#/5/10)
* [Costes](#/5/14)



## Dispositivos ópticos (I)

* Sistemas fiables a corto plazo y con capacidad limitada
* Necesitan de herramientas especiales ([`cdrecord` tools](http://linux.die.net/man/1/cdrecord))

<a class="fancybox" href="img/medios_opticos.png" data-fancybox-group="gallery" title="Medios ópticos">
<img height="250px" src="img/medios_opticos.png" alt="Medios ópticos">
</a>

<aside class="notes">
* Optical Optical media are reliable in the short term, but less reliable in the long term than once believed.
* High-quality media, properly stored, can theoretically last decades; but in practice, failures sometimes occur after only a year or two.
* Some optical media are large enough to back up entire small systems.
* The need to use special tools, such as cdrecord, to write to optical devices can complicate backup plans, but this isn’t an insurmountable hurdle.
</aside>



## Discos duros (I)

* Son medios fiables, relativamente caros y rápidos

<a class="fancybox" href="img/moodle.png" data-fancybox-group="gallery" title="Discos duros">
<img height="450px" src="img/moodle.redimensionado640x480.png" alt="Discos duros">
</a>

<aside class="notes">
* Hard Disks It’s possible to use hard disks for backup purposes.
* Sometimes, computer is equipped with a kit that enables a drive to be quickly removed from a computer,
* You can swap hard disks in and out and move them off-site for storage, if desired.
* Internal hard disks without a removable disk bay, however, are susceptible to theft or damage along with the computer they’re meant to back up.
</aside>



## Discos duros (II)
### NAS (I)

<a class="fancybox" href="img/nas.png" data-fancybox-group="gallery" title="Nas">
<img height="450px" src="img/nas.png" alt="Nas">
</a>

<aside class="notes">
* El NAS (Network-Attached Storage) contiene un solo dispositivo de almacenamiento que está directamente conectado a una LAN
* Ofrece datos compartidos a todos los clientes de la red.
* Un dispositivo NAS es sencillo de instalar y de administrar,  y proporciona una solución de bajo coste.
</aside>



## Discos duros (III)
### NAS (II)

<a class="fancybox" href="img/video.png" data-fancybox-group="gallery" title="Nas">
<img height="450px" src="img/video.redimensionado640x480.png" alt="Nas">
</a>

note:
* Un NAS suele estar formado por un conjunto de discos duros

## Discos duros (IV)
### NAS (III)

<a class="fancybox" href="img/video2.png" data-fancybox-group="gallery" title="Nas">
<img height="250px" src="img/video2.redimensionado640x480.png" alt="Nas">
</a>

<aside class="notes">
* If you decide to use hard disks in removable mounts as a backup medium, you’ll need ordinary internal drives and mounting hardware.
* The hardware comes in two parts: a mounting bay that fits in the computer and a frame in which you mount the hard drive.
* To use the system, you slide the frame with hard drive into the mounting bay.
* You can get by with one of each component, but it’s best to buy one frame for each hard drive, which effectively raises the media cost.
</aside>



## Discos duros (IV)
### SAN (I)

<a class="fancybox" href="img/san.png" data-fancybox-group="gallery" title="SAN">
<img height="450px" src="img/san.redimensionado640x480.png" alt="SAN">
</a>

<aside class="notes">
* Una SAN (Storage Area Network) es una red de alta velocidad diseñada especialmente para el almacenamiento de datos
* Está conectada a uno o más servidores a través de fibra.
* Los usuarios pueden acceder a cualquier de los dispositivos de almacenamiento de la red a través de los servidores,
* El almacenamiento de datos centralizado reduce la administración necesaria y proporciona un tipo de almacenamiento de alto rendimiento y flexible.
</aside>



## Discos duros (V)
### SAN (II)

<a class="fancybox" href="img/san-uhu.png" data-fancybox-group="gallery" title="SAN">
<img height="450px" src="img/san-uhu.redimensionado640x480.png" alt="SAN">
</a>



## Discos duros (VI)

<a class="fancybox" href="img/external_hd.png" data-fancybox-group="gallery" title="External hd">
<img height="550px" src="img/external_hd.redimensionado640x480.png" alt="External hd">
</a>

<aside class="notes">
* Removable hard disk systems work like regular hard disks or other removable disk systems, like USB flash drives.
* Most of these systems use SATA disks, which you’ll access as /dev/sdb, /dev/sdc, or some other SCSI device identifier.
* The disks are likely to be partitioned, and the partitions are likely to hold ordinary Linux filesystems.
* External disks with USB or eSATA interfaces are very common and can make good backup media;
* You’ll need to buy several of them for optimum backup security. Alternatively,
* You can use an external caddy or cable, to which you can easily attach a bare hard disk.
* Buying one caddy and several hard disks enables you to keep multiple backups.
* For optimum speed, get a USB 3.0 or eSATA drive—and be sure your computer supports this high-performance interface!
</aside>



## Cintas (I)

* Son medios fiables, baratos y lentos

<a class="fancybox" href="img/cintas.png" data-fancybox-group="gallery" title="Cintas">
<img height="350px" src="img/cintas.png" alt="Cintas">
</a>

<aside class="notes">
* Tapes Tape drives have historically been the most popular choice for backing up entire computers.
* Their sequential-access nature is a hindrance for some applications, but it isn’t a problem for routine backups.
* The biggest problem with tapes is that they’re less reliable than some backup media, although reliability varies substantially from one type of tape to another, and the best are reasonably reliable.
</aside>



## Cintas (II)

<a class="fancybox" href="img/precios_cintas.png" data-fancybox-group="gallery" title="Precio y tipos">
<img height="550px" src="img/precios_cintas.redimensionado640x480.png" alt="Precio y tipos">
</a>



## Cintas (III)

* Se accede a estos dispositivos mediante
 * `/dev/st0` o `/dev/ht0`, rebobinado automático
 * `/dev/nst0` o `/dev/nht0`, rebobinado manual

<aside class="notes">
* Tape devices are accessed in Linux using the /dev/st0 (SCSI) or /dev/ht0 (PATA) device filenames.
* The /dev/nst0 and /dev/nht0 filenames are non-rewinding variants of these names—when using /dev/st0 or /dev/ht0,
* The tape rewinds automatically after every operation; but when using /dev/nst0 or /dev/nht0, the tape does not rewind.
* If a computer has more than one tape drive of a particular type, the number at the end of the device filename is incremented for each additional drive, as in /dev/st1 for the second SCSI tape drive.
</aside>



## Cintas (IV)
### Robot

<a class="fancybox" href="img/robot-uhu.png" data-fancybox-group="gallery" title="Robot cintas">
<img height="550px" src="img/robot-uhu.redimensionado640x480.png" alt="Robot cintas">
</a>



## Coste (I)

<a class="fancybox" href="img/comparativa_medios.png" data-fancybox-group="gallery" title="Precio medios">
<img height="550px" src="img/comparativa_medios.redimensionado640x480.png" alt="Precio medios">
</a>

<aside class="notes">
* Numbers are approximate as of late 2010.
* Prices on all storage media have historically fallen rapidly, and capacities have risen. Costs are likely to be lower, and capacities higher, in the future.
* In the past, the best backup devices for entire computers and networks have been tapes.
* The low cost and high capacity of tapes made them well suited to performing multiple backups of entire computers.
* In recent years, though, hard disks have plummeted in price, making removable or external hard disks more appealing than tapes for many applications.
</aside>



## Coste (II)

* Se suele usar más de un medio
* Se almacenan en lugares distintos, alejados de la fuente y adecuadamente protegidos
* Se tienen varias copias de lo mismo
* Estrategia 3-2-1: 3 copias de seguridad, en dos medios distintos en 1 lugar distinto

<aside class="notes">
* It’s sometimes desirable to supplement tape or removable hard disk backups with optical backups.
* It’s generally wise to keep multiple backups and to store some of them away from the computers they’re meant to protect.
* Such off-site storage protects your data in case of fire, vandalism, or other major physical traumas.
* Keeping several backups makes it more likely you’ll be able to recover something, even if it’s an older backup, should your most recent backup medium fail.
* Some administrators like to follow the 3-2-1 strategy for backups, which involves keeping three copies of the data on at least two different types of media with at least one copy off-site.
</aside>
