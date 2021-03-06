This file is part of Ardufocuser.

Ardufocuser is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Foobar is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with Foobar.  If not, see <http://www.gnu.org/licenses/>.

---

## Servidor INDI

En el siguiente enlace puede encontrar el enlace de descarga y un mini tutorial del funcionamiento del Servidor INDI sobre el que vamos ejecutamos el Driver INDI Ardufocuser.

[Enlace documetación servidor INDI](http://indilib.org/develop/indiforjava/i4j-server-manual.html)

## Dependencias


RXTX for Java:
```
sudo apt-get install librxtx-java
```
## Runing Script

Script para lanzar el servidor INDI junto con el Driver Ardufocuser.

```
#!/bin/bash

java  -Djava.library.path=/usr/lib/jni -Djava.library.path=/usr/lib/rxtx \
      -jar ./I4JServer/dist/I4JServer.jar  \
      -add=./I4JArdufocuserDriver/dist/I4JArdufocuserDriver.jar
```

### Añadir al Run VM options del proyecto Netbeans:

  ```bash
  -Djava.library.path=/usr/lib/rxtx
  cd /dev
  sudo ln -s ttyACM0 ttyUSB0
  ```
## Instalación en Raspberry PI.

Contamos con Raspbindi una imagen personalizada de Raspbian, con todas las herramientas y servicios INDI instalado.
Puede descargarla en el [enlace](https://drive.google.com/file/d/0Bz7iXJ4BvZ9SbnJPZWkweVhUVjQ/view?usp=sharing)

## Web del proyecto:

[http://ardufocuser.info/](http://ardufocuser.info/)

## Más información

Documentación oficial INDI2Java [enlace](http://indilib.org/develop/indiforjava/i4j-indi-driver.html)

