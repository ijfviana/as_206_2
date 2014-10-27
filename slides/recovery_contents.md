## Introducción

* Cuando el sistema falla es necesario restaurar el sistema:
 * [Restauración parcial](#/7/1)
 * [Recuperaciones de emergencia](#/7/3)

note:
* Además de hacer copias de seguridad, debemos ser capaces de restaurarlas en caso de "desastre"
* Esta tarea implica dos aspectos: restauraciones parciales y recuperaciones de emergencia



## Restauración parcial (I)

<div class="alert alert-info">
  Sólo restauramos parte del sistema
</div>
&nbsp;
<div class="row">
  <div class="col-xs-6 col-sm-6 col-md-6 col-lg-6">
      <p> Usando el comando `tar` </p>
        <pre><code class="hljs bash" data-trim bash>
$ cd /
$ tar xvpf /dev/st0 home/username/filename
$ tar --extract \
               --listed-incremental=/dev/null \
               --file archive.1.tar
        </code></pre>
  </div>
  <div class="col-xs-6 col-sm-6 col-md-6 col-lg-6">
    <p>Usamos el comando `cpio`</p>
        <pre><code class="hljs bash" data-trim bash>
$ cd /
$ cpio -ivF /dev/st0 home/username/filename
        </code></pre>
  </div>
  </div>
</div>

note:
* Involve recovering just a few noncritical files.
* For instance, users might come to you and ask you to restore files from their home directories.
* You can do so fairly easily by using the --extract (x) tar command, as in:
# cd /
# tar xvpf /dev/st0 home/username/filename
When you’re using cpio, the procedure is similar, but you use the --extract (-i) option, along with other options
to feed the name of the archive, and perhaps do other things:
# cd /
# cpio -ivF /dev/st0 home/username/filename



## Restauración parcial (II)

* Podemos restaurar parte de una copia de seguridad si conocemos el nombre de los ficheros

``` bash
$ cd /
$ tar -tvf /dev/st0
$ tar xvpf /dev/st0 mifchero -C /tmp
```

note:
* Whether you’re using tar or cpio, you’ll need to know the exact name of the file or directory you want to restore in order to do this.
* If you don’t know the exact filename, you may need to use the --list (t) command to cpio or tar to examine the entire contents of the tape
* If you use incremental backups, you can use the incremental file list to locate the filename you want to restore.



## Restauración de emergencia

* Hay que restaurar por completo el sistema
* Un disco duro se ha roto
* El sistema se ha visto comprometido

note:
* A much more serious problem is that of recovering a system that’s badly damaged.
* If your hard disk has crashed or your system has been invaded by crackers, you must restore the entire system from scratch, without the benefit of your normal installation.



## Restauración de emergencia (II)
### Opciones

* Usar los discos de instalación de la distribución
* Usar CD de recuperación
* Usar sistemas de emergencia
* Usar partición de emergencia
* Instalación parcial



## Restauración de emergencia (III)
### Discos de Instalación

* Usamos los propios disco de instalación de la distribución
* Suelen tener distintas opciones de emergencia
* Estas opciones nos ofrecen acceso al sistema  y a una shell básica

note:
 Distribution’s Installation Disk Most Linux distributions’ installation disks have some sort of emergency
recovery system. These systems are typically small but functional Linux installations with a handful of vital tools,
such as fdisk, mkfs, Vi, and tar. Check your distribution’s documentation or boot its boot media and study its
options to learn more.



## Restauración de emergencia (IV)
### Instalaciónes autoarrancables

* Arrancamos la máquina usando distribuciones como
 * [Knoppix](http://www.knoppix.com),
 * [SystemRescueCd](http://www.sysresccd.org),
 * [PartedMagic](http://partedmagic.com)

note:
CD-Based Linux System Several Linux systems are now available that boot from CD-ROM or DVD. Examples
include Knoppix (http://www.knoppix.com), SystemRescueCd (http://www.sysresccd.org), and PartedMagic
(http://partedmagic.com). All of these systems can be used to help recover or restore a corrupted Linux
installation.



## Restauración de emergencia (V)
### Sistemas de emergencia

* Hacemos una copia del sistema arrancable
* Esta copia se ha almacenado en algún medio de almacenamiento removible
* Restauramos esta copia

note:
Emergency System on Removable Disk You can create your own emergency system on a removable disk, such
as a USB flash drive. A 16 GiB flash drive is sufficient to hold a fairly comfortable Linux installation, although it
won’t perform as quickly as an installation on a PATA, SATA, or SCSI hard disk.



## Restauración de emergencia (VI)
### Recuperación de particiones

* Cuando se instala el sistema por primera vez se reserva una partición
* En esa partición se hace la instalación de otro sistema operativo
* Se usa este sistema operativo para intentar la restauración

note:
Emergency Recovery Partition If you plan ahead, you might create a small emergency installation of your
preferred distribution alongside the regular installation. You should not mount this system in /etc/fstab. This
system can be useful for recovering from some problems, such as software filesystem corruption, but it’s not
useful for others, such as a total hard disk failure.



## Restauración de emergencia (VII)
### Reinstalación parcial

* Se hace una instalación mínima del sistema
* A partir de esta instalación mínima intentamos recuperar el sistema

note:
* You can reinstall a minimal Linux system and then use it to recover your original installation.
* This approach is much like the emergency recovery partition approach, but it takes more time at disaster recovery.
* On the other hand, it will work even if your hard disk is completely destroyed.
* Whatever approach you choose to use, you should test it before you need it.
* Learn at least the basics of the tools available in any system you plan to use.
* Ideally, you should boot the tools, restore a system, and test that the system works. This may be possible if you have spare hardware on which to experiment, but if you lack this luxury, you may have to make do with performing a test restore of a few files and testing an emergency boot procedure—say, using Super GRUB Disk (http://www.supergrubdisk.org). Note that a freshly restored system will not be bootable; you’ll need a tool such as Super GRUB
