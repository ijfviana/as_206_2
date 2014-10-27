as_206_2
========

Transparencias de Administración de Servidores. Mantenimiento del Sistema, copias de seguridad.


Instalación
===========

Para instalarlo en Ubuntu 14.04, se siguen los siguientes pasos:

1. Instale nodejs
```
sudo apt-get install nodejs nodejs-legacy
```
2. Instale npm
```
sudo apt-get install npm
```
3. Instale grunt
```
sudo npm install -g grunt-cli
```
4. Instalar bower
```
sudo npm install -g bower
```
5. Clone el repositorio
```
git clone https://github.com/ijfviana/as_206_2.git
```
6. Accedemos al directorio `as_206_2`
```
cd as_206_2
```
7. Instale las dependencias mediante bower
```
bower install
```
7. Instale las dependencias del proyecto
```
npm install
```
8. Ejecute la presentacion
```
grunt server
```
