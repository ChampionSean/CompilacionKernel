# Universidad Nacional Autónoma de México
# Facultad de Ciencias
# Ciencias de la Computación
# Sistemas Operativos

Semestre 2018-1

## Reporte Práctica: Compilación del *kernel* Linux

### Alumno

+ Marco Antonio Estrada Robles

### Requisitos mínimos


### Fecha de entrega

### Secciones

+ [Preparación del sistema operativo](apt.md)
+ [Instalación de dependencias y compilación del *kernel* Linux](kernel.md)
+ [Creación del paquete `deb` del  *kernel*](deb.md)
+ [Instalación del paquete `deb` del  *kernel*](install.md)

### Lineamientos
+ Imagenes: 

  ![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(25).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(26).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(27).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(28).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(29).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(30).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(31).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(32).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(33).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(34).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(35).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(36).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(37).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(38).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(39).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(40).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(41).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(42).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(43).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(44).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(45).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(46).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(47).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(48).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(49).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(50).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(51).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(52).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(53).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(54).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(55).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(56).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(57).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(58).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(59).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(60).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(61).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(62).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(63).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(64).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(65).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(66).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(67).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(68).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(69).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(70).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(71).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(72).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(73).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(74).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(75).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(76).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(77).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(78).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(79).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(80).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(81).png)
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
