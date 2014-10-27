## Software

* [tar](#/6/1)
* [cpio](#/6/7)
* [dd](#/6/13)
* [rsync](#/6/16)
* [mt](#/6/18)



## `tar` (I)

* El comando [`tar` (tape archiver)](http://linux.die.net/man/1/tar) permite "empaquetar" ficheros bajo un nombre único
* Se puede usar en unión con [`bzip`](http://linux.die.net/man/1/bzip2) o [`gzip`](http://linux.die.net/man/1/gzip) para comprimirlos
* Nos permite dividir el fichero en volúmenes.
* Es un programa complejo con muchas opciones.

note:
* The tar program’s name stands for “tape archiver.”
* Despite this, you can use tar to archive data to other media.
* In fact, tarballs (archive files created by tar and typically compressed with gzip or bzip2) are often used for transferring multiple files between computers in one step, such as when distributing source code.
* The tar program is a complex package with many options



## `tar` (II)
### Comandos

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th>Comando</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--create`, `-c`</td>
<td>Crea un nuevo archivo</td>
</tr>
<tr>
<td>`--concatenate`, `-A`</td>
<td>Añade fichero tar a un archivo</td>
</tr>
<tr>
<td>`--append`, `-r`</td>
<td>Añade ficheros no-tar a un archivo</td>
</tr>
<tr>
<td>`--update`, `-u`</td>
<td>Actualiza los ficheros contenidos en el archivo</td>
</tr>
</tbody>
</table>
</div>

note:
| Command       | Abbreviation | Description |
|---------------|--------------|-------------|
| --create      | c            | Creates an archive |
| --concatenate | A | Appends tar files to an archive |
| --append      | r | Appends non- tar files to an archive
| --update      | u  |Appends files that are newer than those in an archive
| --diff or --compare | d | Compares an archive to files on disk
| --list        | t | Lists an archive’s contents
| --extract or --get | x  | Extracts files from an archive



## `tar` (III)
### Comandos (II)
<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th>Comando</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
  <tr>
<td>`--diff`, `--compare`, `-d`</td>
<td>Compara un archivo con los ficheros en disco</td>
</tr>
<tr>
<td>`--list`, `-t`</td>
<td>Muestra los contenidos de un archivo</td>
</tr>
<tr>
<td>`--extract`, `--get`, `-x`</td>
<td>Extrae los ficheros de un archivo</td>
</tr>
</tbody>
</table>
</div>

note:
| Command       | Abbreviation | Description |
|---------------|--------------|-------------|
| --create      | c            | Creates an archive |
| --concatenate | A | Appends tar files to an archive |
| --append      | r | Appends non- tar files to an archive
| --update      | u  |Appends files that are newer than those in an archive
| --diff or --compare | d | Compares an archive to files on disk
| --list        | t | Lists an archive’s contents
| --extract or --get | x  | Extracts files from an archive



## `tar` (IV)
### Calificadores (I)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="550em">Calificador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--directory dir`, <br>`-C`</td>
<td>Cambia al directorio `dir` antes de hacer la operación</td>
</tr>
<tr>
<td>`--file [ host :] file`, <br> `-f`</td>
<td>Usa el fichero  `file` para guardar los datos</td>
</tr>
</tbody>
</table>
</div>

note:
| Qualifier                 | Abbreviation | Description
|---------------------------|--------------|------------
|--directory dir            | C            | Changes to directory dir before performing operations
| --file [ host :] file     | f            | Uses the file called file on the computer called host as the archive file
| --listed-incremental file | g            | Performs an incremental backup or restore, using file as a list of previously archived files
| --one-file-system         | l (on older versions of tar ) | Backs up or restores only one filesystem (partition)



## `tar` (V)
### Calificadores (II)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="550em">Qualificadores</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--listed-incremental file`, <br> `-g`</td>
<td>Realiza copia incremental, usado el fichero `file` como listado de ficheros ya guardados</td>
</tr>

<tr>
<td>`--one-file-system`, `-l`</td>
<td>Hace una copia de seguridad o restaura un único sistema de ficheros</td>
</tr>

</tbody>
</table>
</div>

note:
| Qualifier                 | Abbreviation | Description
|---------------------------|--------------|------------
|--directory dir            | C            | Changes to directory dir before performing operations
| --file [ host :] file     | f            | Uses the file called file on the computer called host as the archive file
| --listed-incremental file | g            | Performs an incremental backup or restore, using file as a list of previously archived files
| --one-file-system         | l (on older versions of tar ) | Backs up or restores only one filesystem (partition)



## `tar` (VI)
### Calificadores (III)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="400em">Calificador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--multi-volume`, `M`</td>
<td>Crea/extrae archivos multi volumen</td>
</tr>
<tr>
<td>`--tape-length N`, `L`</td>
<td>Cambia la cinta después de `N` kilobytes</td>
</tr>
<tr>
<td>`--same-permissions`, `p`</td>
<td>Preserva toda la información de protección</td>
</tr>
<tr>
<td>`--absolute-paths`, `P`</td>
<td>Guarda todo con caminos absolutos</td>
</tr>
<tr>
<td>`--verbose`, `v`</td>
<td>Muestra información adicional</td>
</tr>
</tbody>
</table>
</div>
note:
| Qualifier                 | Abbreviation | Description
|---------------------------|--------------|------------
| --multi-volume            | M | Creates or extracts a multi-tape archive
| --tape-length N           | L | Changes tapes after N kilobytes
| --same-permissions        | p | Preserves all protection information
| --absolute-paths          | P | Retains the leading / on filenames
| --verbose                 | v | Lists all files read or extracted when used with --list ; displays file sizes, ownership, and time stamps



## `tar` (VII)
### Calificadores (IV)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="400em">Calificador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--verify`, `W`</td>
<td>Verifica el fichero después de crearlo</td>
</tr>
<tr>
<td>`--exclude file`</td>
<td>Excluye `file` del archivo</td>
</tr>
<tr>
<td>`--exclude-from file`, `X`</td>
<td>Excluye ficheros listados en el fichero `file` del archivo</td>
</tr>
<tr>
<td>`--gzip` `--ungzip`, `z`</td>
<td>Aplica compresión zip</td>
</tr>
<tr>
<td>`--bzip2`, `j` </td>
<td>Aplica compresión bzip2</td>
</tr>
</tbody>
</table>
</div>
note:
| Qualifier                 | Abbreviation | Description
|---------------------------|--------------|------------
| --verify                  | W | Verifies the archive after writing it
| --exclude file            | (none) | Excludes file from the archive
| --exclude-from file       | X | Excludes files listed in file from the archive
| --gzip or --ungzip        | z | Processes an archive through gzip
| --bzip2                   | j (some older versions used I or y ) | Processes an archive through bzip2



## `tar` (VIII)
### Ejemplos

* Crea copia de seguridad de una serie de directorios
```bash
# tar cvpf /dev/st0 --one-file-system /home / /boot /var
```
* Crea copias de seguridad incrementales
```bash
# tar --create \
           --file=archive.1.tar \
           --listed-incremental=/var/log/usr.snar \
           /usr
# tar --create \
           --file=archive.2.tar \
           --listed-incremental=/var/log/usr.snar \
           /usr
```
* [Más información](https://www.gnu.org/software/tar/manual/html_chapter/tar_5.html)



## `cpio` (I)

* Es comando [`cpio`](http://linux.die.net/man/1/cpio) es similar al comando [`tar` (tape archiver)](http://linux.die.net/man/1/tar)
* No requiere de almacenamiento intermedio
* Hay que indicarle por la entrada estándar los directorios a copiar

note:
* The cpio program is similar to tar in that it creates an archive file.
* That file can be stored on disk, or it can be directed straight to your tape device.
* This can be a convenient way to back up the computer, because it requires no intermediate storage.
* To restore data, you use cpio to read directly from the tape device file.



## `cpio` (II)
### Modos

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="190em">Nombre</th>
<th width="370em">Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>Copy-out</td>
<td>`-o`, `--create`</td>
<td>Crea un archivo y copia ficheros en él</td>
</tr>
<tr>
<td>Copy-in</td>
<td>`-i`, -extract</td>
<td>Extrae datos de un fichero</td>
</tr>
<tr>
<td>Copy-pass</td>
<td>`-p`, `--pas--through`</td>
<td>Permite copiar una estructura de directorios de un sitio a otro</td>
</tr>
</tbody>
</table>
</div>

note:
* Copy-Out Mode This mode, activated by use of the -o or --create option, creates an archive and copies files into it.
* Copy-In Mode You activate copy-in mode by using the -i or --extract option. This mode extracts data from an existing archive. If you provide a filename or a pattern to match, cpio will extract only the files whose names match the pattern you provide.
* Copy-Pass Mode This mode is activated by the -p or --pass-through option. It combines the copy-out and copy- in modes, enabling you to copy a directory tree from one location to another.



## `cpio` (III)
### Opciones (I)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="530em">Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--reset-access-time`, <br> `-a`</td>
<td>Resetea el tiempo de acceso después de leer el fichero</td>
</tr>
<tr>
<td>`--append`, `-A`</td>
<td>Añade datos a un archivo existente</td>
</tr>
<tr>
<td>`--pattern-file=filename`, <br>`-E filename`</td>
<td>Usa el contenido de `filename` como lista de ficheros a extraer en modo copy-in</td>
</tr>
</tbody>
</table>
</div>

note:
| Option                   | Abbreviation | Description |
|--------------------------|--------------|-------------|
| --reset-access-time      | -a           | Resets the access time after reading a file so that it doesn’t appear to have been read.
| --append                 | -A           | Appends data to an existing archive.
| --pattern-file= filename | -E filename  | Uses the contents of filename as a list of files to be extracted in copy-in mode.
| --file= filename         | -F filename  | Uses filename as the cpio archive file; if this parameter is omitted, cpio uses standard input or output.



## [`cpio`](http://linux.die.net/man/1/cpio) (IV)
### Opciones (II)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`--file= filename`, `-F filename`</td>
<td>Usa `filename` como el archivo cpio; si se omite se usa la salida/entrada estándar</td>
</tr>
<tr>
<td>`--format= format`, `-H format`</td>
<td>Usa un formato específico de fichero. (bin, crc, tar).</td>
</tr>
<tr>
<td>`-I filename`</td>
<td>Usa `filename` como fichero de entrada</td>
</tr>
</tbody>
</table>
</div>

note:
| Option                   | Abbreviation | Description |
|--------------------------|--------------|-------------|
| --format= format         |-H format     | Uses a specified format for the archive file. (bin, crc, tar).
| N/A                      | -I filename  | Uses the specified input filename.
| --no-absolute-filenames  | N/A          | In copy-in mode, extracts files relative to the current directory, even if filenames in the archive contain full directory paths.
| N/A                      | -O  filename | Uses the specified output filename.



## [`cpio`](http://linux.die.net/man/1/cpio) (V)
### Opciones (III)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="400em">Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
  <tr>
<td>`--no-absolute-filenames`</td>
<td>En modo copy-in, extrae los ficheros en el directorio actual, aunque se guardaran con camino absoluto</td>
</tr>
<tr>
<td>`-O filename`</td>
<td>Usa `filename` como fichero de salida</td>
</tr>
<tr>
<td>`--list`, `-t`</td>
<td>Muestra los contenidos</td>
</tr>
</tbody>
</table>
</div>

note:
| Option                   | Abbreviation | Description |
|--------------------------|--------------|-------------|
| --list                   | -t           | Displays a table of contents for the input.
| --unconditional          | -u           | Replaces all files, without first asking for verification.
| --verbose                | -v           | Displays filenames as they’re added to or extracted from the archive. When used with -t , displays additional listing information (similar to ls -l ).



## [`cpio`](http://linux.die.net/man/1/cpio) (VI)
### Opciones (IV)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="400em">Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>

<tr>
<td>`--unconditional, -u`</td>
<td>Reemplaza todos los ficheros, no solicita confirmación</td>
</tr>
<tr>
<td>`--verbose, -v`</td>
<td>Muestra información adicional del proceso</td>
</tr>
</tbody>
</table>
</div>

note:
| Option                   | Abbreviation | Description |
|--------------------------|--------------|-------------|
| --list                   | -t           | Displays a table of contents for the input.
| --unconditional          | -u           | Replaces all files, without first asking for verification.
| --verbose                | -v           | Displays filenames as they’re added to or extracted from the archive. When used with -t , displays additional listing information (similar to ls -l ).



## [`cpio`](http://linux.die.net/man/1/cpio) (VII)
### Ejemplos

* Copia de seguridad de un sistema de ficheros:
``` bash
# find / | cpio -oF /dev/st0
```
* Copia de seguridad de ciertos directorios
``` bash
# find /home / /boot /var -xdev | cpio -oF /dev/st0
```
* Copia de seguridad incremental
```bash
$ find . -type f -a -newer /etc/local/lastinc -print | cpio -oacvQ /dev/rmt0
$ touch /etc/local/lastinc
```



## [`dd`](http://linux.die.net/man/1/dd) (I)

* Realiza copias a bajo nivel (sector a sector)
* Es independiente del sistema de ficheros
* Las copias son exactas, copia incluso sectores no usados
* Las copias de seguridad son grandes en tamaño y tardan en realizarse y restaurarse.

<aside class="notes">
The dd utility is a low-level file copying tool, with the ability to apply certain transformations at the same time. As a
backup tool, dd is useful for backing up an entire raw filesystem—even one that Linux doesn’t support or one
that’s been badly damaged. Table 4.13 summarizes the dd options you’re most likely to use when backing up a
filesystem using this tool. Consult the program’s man page for additional options.
</aside>



## [`dd`](http://linux.die.net/man/1/dd) (II)
### Operaciones

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered"><thead>
<tr>
<th width="290em">Operación</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`bs= size`</td>
<td>Trabajo con bloques de tamaño `size`</td>
</tr>
<tr>
<td>`count=blocks`</td>
<td>Copia `blocks` bloques</td>
</tr>
<tr>
<td>`if=file`</td>
<td>Usa `file` como fichero de entrada</td>
</tr>
<tr>
<td>`of=file`</td>
<td>Usa `file` como fichero de salida</td>
</tr>
<tr>
<td>`skip=blocks`</td>
<td>Pasa por alto `blocks` bloques de entrada</td>
</tr>
<tr>
<td>`seek=blocks`</td>
<td>Empieza a escribir desde el bloque `blocks`</td>
</tr>
<tr>
<td>`conv=conver`</td>
<td>Aplica reglas de conversión</td>
</tr>
</tbody>
</table>
</div>

note:
| Operand | Description |
|---------|-------------|
|bs= size | Operates on chunks (blocks) of size bytes at a time.
|count= blocks | Copies the specified number of blocks.
|if= file | Uses file as the source (input) file.
|of= file |Writes output to the specified file.
|skip= blocks |Skips the specified number of blocks on input.
|seek= blocks | Starts writing the specified number of blocks into the output file.
|conv= conversions | Applies conversion rules from a list. `noerror', the program continues if it encounters an input/output error.



## [`dd`](http://linux.die.net/man/1/dd) (II)
### Ejemplos

* Crea copia de seguridad
```bash
$ dd if=/dev/sda2 of=/media/backups/sda2-back.img
```
* Crea copia seguridad de una partición comprimidaa
```bash
$ dd if=/dev/sda2 | gzip -9 > /media/backups/sda2-back.img.gz
```



## [`rsync`](http://linux.die.net/man/1/rsync)

* Se usa para haccer copias de seguridad remotas
* Está diseñado para sincronizar los contenidos de dos localizaciones, una local y otra remota
* Sólo se transfiere lo que se ha modificado
* No transfiere las copias de seguridad a un dispositivo de backup, a no ser que esté montado

<aside class="notes">
* For small network backup tasks, rsync may be all you need.
* This program is designed to copy data from one computer to another on a network, keeping two network directories synchronized.
* The program supports a large number of options and variant machine specifications; however, a general use looks something like this:
* Although rsync doesn’t transfer data directly to a backup medium unless it’s a hard disk that’s mounted, it can be useful for network data transfers.
* Users can copy their files to a central backup server, or the backup server can use rsync to grab files from backup client computers.
* In either case, the backup server computer can then back the files up to tape or some other storage medium.
</aside>



## [`rsync`](http://linux.die.net/man/1/rsync)
### Ejemplos

* Copia el directorio local a uno remoto
``` bash
$ rsync -av ./ user@remote:~/backups/
```
* Realiza una copia de seguridad completa de todo el sistema
```bash
$ rsync -aAXv /* /path/to/backup/folder \
        --exclude={/dev/*,/proc/*,/sys/*,/tmp/*,/run/*,/mnt/*,/media/*,/lost+found}
```
* Copia de seguridad incremental
``` bash
$ rsync -a --backup origen/ destino/
```



## `mt` (I)

* Usamos `cpio` y `tar` para hacer copias de seguridad es un fichero
* Estos ficheros se suelen almacenar en cintas.
* El comando [`mt`](http://linux.die.net/man/1/mt) sirve para mover la cabeza de lectura/escritura de la cinta

<a class="fancybox" href="img/mt.png" data-fancybox-group="gallery" title="Volumenes físicos">
<img height="250px" src="img/mt.png" alt="Volumenes físicos">
</a>

<aside class="notes">
* In cpio and tar terminology, each backup is a file.
* This file is likely to contain many files from the original system,
* Sometimes an archive file is far smaller than the tape on which it’s placed.
* If you want to store more than one archive file on a tape, you can do so by using the nonrewinding tape device filename.
</aside>



## `mt` (II)
### Comandos (I)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="350em">Comando</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`fsf`</td>
<td>Moves forward count files.</td>
</tr>
<tr>
<td>`bsf`</td>
<td>Moves backward count files.</td>
</tr>
<tr>
<td>`eod`,  `seod`</td>
<td>Moves to the end of data on the tape.</td>
</tr>
<tr>
<td>`rewind`</td>
<td>Rewinds the tape.</td>
</tr>
<tr>
<td>`offline`, `rewoffl`</td>
<td>Rewinds and unloads the tape.</td>
</tr>
</tbody>
</table>
</div>

note:
| Operation | Description
|-----------| ------------
| fsf       | Moves forward count files.
| bsf       | Moves backward count files.
| eod or seod | Moves to the end of data on the tape.
| rewind      | Rewinds the tape.
| offline or rewoffl | Rewinds and unloads the tape. (Unloading is meaningless on some drives but ejects the tape on others.)



## [`mt`](http://linux.die.net/man/1/mt)
### Comandos (II)

<div class="table-responsive">
<table class="table table-hover table-condensed table-bordered">
<thead>
<tr>
<th width="330em">Comando</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>`retension`</td>
<td>Rebobina dos veces</td>
</tr>
<tr>
<td>`erase`</td>
<td>Marca la cinta como vacía</td>
</tr>
<tr>
<td>`status`</td>
<td>Muestra información sobre la unidad de cinta</td>
</tr>
<tr>
<td>`load`</td>
<td>Carga la cinta en el driver</td>
</tr>
<tr>
<td>`compression`</td>
<td>Activa o desactiva la compresión</td>
</tr>
<tr>
<td>`datcompression`</td>
<td>También activa/desactiva la compresión</td>
</tr>
</tbody>
</table>
</div>

note:
| Operation | Description
|-----------| ------------
| retension | Rewinds the tape, winds it to the end, and then rewinds it again.
| erase | Erases the tape. (This command usually doesn’t actually erase the data; it just marks the tape as being empty.)
| status | Displays information on the tape drive.
| load | Loads a tape into the drive. Unnecessary with many drives.
| compression | Enables or disables compression by passing an argument of 1 or 0 , respectively.
| datcompression | Also enables and disables compression.



## [`mt`](http://linux.die.net/man/1/mt)
### Ejemplos

* Posicionarse al principio de la cinta
```bash
$ mt -f /dev/nst0 rewind
```
* Posicionarse en el fichero siguiente
```bash
# mt -f /dev/nst0 fsf 1
```
* Hacemos copia de seguridad en la posición actual
``` bash
# tar cvlpf /dev/nst0/directory/to/back/up
```
* Rebobinamos y descargamos la cinta
```bash
# mt -f /dev/nst0 offline
```
