# Universidad Nacional Autónoma de México
# Facultad de Ciencias
# Ciencias de la Computación
# Sistemas Operativos

Semestre 2018-1

## Reporte Práctica: Compilación del *kernel* Linux

### Alumno

+ Marco Antonio Estrada Robles

### Secciones

+ Preparación del sistema operativo
+ Instalación de dependencias y compilación del *kernel* Linux
+ Creación del paquete `deb` del  *kernel*
+ Instalación del paquete `deb` del  *kernel*

### Reporte, imagenes en orden, secuencia de comandos
+ Imagenes: 

### Intalacion del sistema operativo

+ En estas imagenes se muestra la instalación que hice del sistema operativo debian-jessie usando una máquina virtual con virtualbox.
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(25).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(26).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(27).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(28).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(29).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(30).png)

### Preparacion del sistema operativo

+ Después de haber instalado el sistema operativo continuo con el proceso de compilación del kernel.

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(31).png)

+ Primero verifico el archivo sources.list, que venga tal y como se muestra en la práctica, en mi caso remplace el archivo por el que venía descrito en la práctica

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(32).png)

+ Verificar que el sistema esté actualizado


+ Ejecuté aptitude update para actualizar la información de los repositorios de paquetes y verificar que no existan actualizaciones pendientes

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(33).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(34).png)



+ En caso de existir actualizaciones pendientes, descargarlas e instalarlas
+ Pero a mi no me salieron actualizaciones pendientes por lo que todo se quedó como estaba.

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(35).png)

### Instalacion de dependencias y compilacion del kernel linux

+ Instalación de dependencias

+ 
Instalé las dependencias básicas para compilar el kernel, usando los comandos descritos en la práctica
+ Adjunto el resultado en las imágenes:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(36).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(37).png)

+ Después descargué el código fuente del kernel linux y el tarball del kernel, usando los comandos descritos en la práctica

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(38).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(39).png)

+ Lo siguiente fué descargar la firma GPG
+ Y istar para revisar el tamaño de los archivos descargados

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(40).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(41).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(42).png)

+ Lo siguiente fué descomprimir el tarball
+ E intentar verificar la firma digital con gpg
+ También descargar el bloque de llaves públicas GPG de los desarrolladores del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(43).png)

+ Volví a verificar la firma digital con gpg



+ Ejecuté gpg --verify por segunda vez para que verifique la firma digital

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(44).png)

+ Después procedí a desempaquetar el tarball del kernel



+ Fué necesario desempaquetar el archivo tar para acceder al árbol de código fuente del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(45).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(46).png)

+ Hice una copia de la configuración del kernel actual

, tal y como lo indica la práctica
+ E hice una copia de la configuración kernel actual para tomarla como base para el nuevo kernel que vamos a compilar, tal y como lo indica la práctica:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(47).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(48).png)



+ Después Ejecuté make menuconfig para acceder al menú de configuración de las opciones del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(49).png)

+ Después configuré las opciones del kernel tal y como lo indica la práctica, y quedó tal y como se muestra en la siguiente imágen.

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(50).png)

+ Guardé cambios en el archivo .config


Seleccionar la opción < Save > para guardar los cambios hechos a la configuración del kernel


+ Aceptar el nombre predeterminado (.config) en los cuadros de diálogo

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(51).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(52).png)

+Después ejecuté make help para ver las opciones disponibles del comando

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(53).png)

+ Para finalizar esta sección hice make all para compilar el kernel y los módulos
+ En esta parte se tardó en terminar de compilar

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(54).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(55).png)

+ Se puede comprobar que make no generó error al revisar el código de salida:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(56).png)

### Creación del paquete `deb` del kernel

+ Ejecuté make deb-pkg para generar los paquetes necesarios para instalar este kernel en un equipo con sistema operativo de tipo debian

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(57).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(58).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(59).png)

+ Listé los paquetes generados y tomar nota del tamaño, especialmente para el paquete linux-image-*-dbg_*.deb

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(60).png)

+ Obtener la información de control sobre cada paquete



+ libc-dev
+ Aquí listé los paquetes libc-dev 
	
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(61).png)

+ Obtener la información de control sobre cada paquete



+ linux-firmware
+ Aquí listé los paquetes linux-firmware

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(62).png)

+ Obtener la información de control sobre cada paquete



+ linux-headers
+ Aquí listé los paquetes linux-headers

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(63).png)

+ Obtener la información de control sobre cada paquete



+ linux-image
+ Aquí listé los paquetes linux-image

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(64).png)

+ Obtener la información de control sobre cada paquete



+ linux-image, símbolos de depuración
+ Aquí listé los paquetes linux-image

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(65).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(66).png)

### Instalación del paquete `deb` del  *kernel*

+ Aquí instalé los paquetes con dpkg

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(67).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(68).png)

+ Listé los paquetes instalados,

 lo hice utilizando aptitude:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(69).png)

+ Aquí verifiqué el contenido del directorio /boot


Dentro del directorio /boot deben existir los siguientes archivos para cada kernel que se tenga instalado:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(70).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(71).png)

+ Aquí verifiqué la configuración del cargador de inicio grub


Debe donde la configuración de grub que hace referencia al kernel que se compiló e instaló desde paquetes:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(72).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(73).png)

+ Después reinicie el sistema y Verifiqué la versión de kernel en el cargador de inicio

 al reiniciar la máquina virtual se muestra la pantalla de grub

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(74).png)

+ Verifiqué utilizando las herramientas del sistema operativo la versión del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(78).png)

+ Verifiqué utilizando la información de algún módulo para ver la ruta y la versión del kernel para la que fue compilado
+ Intenté cargar el módulo y ver si se integra la funcionalidad que contiene

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(79).png)

+ Por último listé la ruta de los módulos y cabeceras para el kernel compilado

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(80).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(81).png)
### Herramientas
+ Virtual Box
+ nano
+ gedit
+ git

### Dificultadas
+ La única dificultad que tuve en la práctica fue a la hora de instalar los paquetes con dpkg -i \ en el paquete linux-image..., para arreglar el error solo cambie el nombre por que no encontraba el linux-image...
