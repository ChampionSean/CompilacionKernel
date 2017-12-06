# Universidad Nacional Autónoma de México
# Facultad de Ciencias
# Ciencias de la Computación
# Sistemas Operativos

Semestre 2018-1

## Reporte Práctica: Compilación del *kernel* Linux

### Alumno

+ Marco Antonio Estrada Robles

### Requisitos mínimos

+ Debian GNU Linux 8 *jessie*
  * Máquina virtual o instalación física
+ 2 vCPU
+ 2 GB de RAM
+ 20 GB de Disco
+ Conexión a Internet

### Fecha de entrega

Martes, 5 de diciembre de 2017

### Secciones

+ [Preparación del sistema operativo](apt.md)
+ [Instalación de dependencias y compilación del *kernel* Linux](kernel.md)
+ [Creación del paquete `deb` del  *kernel*](deb.md)
+ [Instalación del paquete `deb` del  *kernel*](install.md)

### Lineamientos

+ Cada alumno deberá realizar su propio reporte y subirlo a su repositorio
+ El reporte deberá estar en el archivo `README.md` en formato **Markdown**
+ Subir el archivo `.config` al repositorio
+ Si existen imágenes, deberán ser subidas al repositorio en el directorio `img/`  

  Referenciar las imágenes de acuerdo a la sintaxis de **Markdown**:

    * <https://docs.gitlab.com/ce/user/markdown.html#images>
    * <https://about.gitlab.com/handbook/product/technical-writing/markdown-guide/#images>

  ![Tux](https://assets.gitlab-static.net/uploads/-/system/project/avatar/4644768/Tux.png)

+ Se deberá crear una carpeta llamada `deb/` donde se subirán los paquetes `.deb` generados al ejecutar `make deb-pkg`

    * `linux-firmware-image-3.16.50so-ciencias-unam_3.16.50so-ciencias-unam-2_amd64.deb`
    * `linux-headers-3.16.50so-ciencias-unam_3.16.50so-ciencias-unam-2_amd64.deb`
    * `linux-libc-dev_3.16.50so-ciencias-unam-2_amd64.deb`
    * `linux-image-3.16.50so-ciencias-unam_3.16.50so-ciencias-unam-2_amd64.deb`

+ No subir el siguiente archivo al repositorio porque es de gran tamaño y no es necesario para la práctica

    * `linux-image-3.16.50so-ciencias-unam-dbg_3.16.50so-ciencias-unam-2_amd64.deb`

+ Crear en el repositorio una carpeta llamada `build/` donde se suban los siguientes archivos:

    * `.config.old`
    * `.config`
    * `.version`
    * `System.map`
    * `.vmlinux.cmd`
    * `modules.builtin`
    * `modules.order`
    * `Module.symvers`

+ Explicar que herramientas se utilizaron y si hubo algún problema o dificultad y la manera como se resolvió

### Recursos de ayuda

+ Archivo `sources.list`

  * <https://gist.github.com/tonejito/81b995ddbed62bc3d0f1ab6a36709729>

+ Debian APT first aid

  * <https://gist.github.com/tonejito/540ace6adeb3c01880375689801200f9>

+ Verificación de la firma digital del *kernel* Linux

  * <https://www.kernel.org/signature.html>

+ Script `get-kernel`

  * <https://gist.github.com/tonejito/9460148>

+ Página oficial del *kernel* Linux

  * <https://www.kernel.org/>

+ Árbol de código de la versión 3.16.50 del *kernel* Linux

  * <https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git/tree/?h=v3.16.50>

+ Paquete de código fuente y archivo de firma digital para el *kernel* Linux versión 3.16.50

  * <https://cdn.kernel.org/pub/linux/kernel/v3.x/linux-3.16.50.tar.xz>
  * <https://cdn.kernel.org/pub/linux/kernel/v3.x/linux-3.16.50.tar.sign>

+ Guías de Debian para compilar el *kernel*

  * <https://www.debian.org/releases/stable/amd64/ch08s06.html.en>
  * <http://kernel-handbook.alioth.debian.org/ch-common-tasks.html#s-kernel-org-package>
  * <https://debian-handbook.info/browse/stable/sect.kernel-compilation.html>

+ Guías de Ubuntu para compilar el *kernel*

  * <https://help.ubuntu.com/community/Kernel/Compile>
  * <https://wiki.ubuntu.com/Kernel/BuildYourOwnKernel>

+ Otras guías para compilar el *kernel*

  * <https://www.linux.com/learn/how-compile-linux-kernel>
