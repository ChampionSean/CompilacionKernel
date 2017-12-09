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

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(25).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(26).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(27).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(28).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(29).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(30).png)

### Preparacion del sistema operativo

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(31).png)

+ Verificar el archivo sources.list

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(32).png)

+ Verificar que el sistema esté actualizado


+ Ejecutar aptitude update para actualizar la información de los repositorios de paquetes y verificar que no existan actualizaciones pendientes

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(33).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(34).png)

+ Descargar e instalar actualizaciones


+ En caso de existir actualizaciones pendientes, descargarlas e instalarlas

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(35).png)

### Instalacion de dependencias y compilacion del kernel linux

+ Instalación de dependencias

+ 
Instalar las dependencias básicas para compilar un kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(36).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(37).png)

+ Descargar el código fuente del kernel Linux



+ Descargar tarball del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(38).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(39).png)

+ Descargar la firma GPG
+ Listar para revisar el tamaño de los archivos descargados

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(40).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(41).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(42).png)

+ Descomprimir el tarball
+ Intentar verificar la firma digital con gpg
+ Descargar el bloque de llaves públicas GPG de los desarrolladores del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(43).png)

+ Verificar la firma digital con gpg



+ Ejecutar gpg --verify por segunda vez para que verifique la firma digital

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(44).png)

+ Desempaquetar el tarball del kernel



+ Es necesario desempaquetar el archivo tar para acceder al árbol de código fuente del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(45).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(46).png)

+ Copiar la configuración del kernel actual


+ Se hace una copia de la configuración kernel actual para tomarla como base para el nuevo kernel que vamos a compilar:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(47).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(48).png)

+ Configurar las opciones del kernel



+ Ejecutar make menuconfig para acceder al menú de configuración de las opciones del kernel

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(49).png)

+ Configurar opciones del kernel


Seleccionar la opción General setup:
+ Después seleccionar Local version:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(50).png)

+ Guardar cambios en el archivo .config


Seleccionar la opción < Save > para guardar los cambios hechos a la configuración del kernel


+ Aceptar el nombre predeterminado (.config) en los cuadros de diálogo

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(51).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(52).png)

+Ejecutamos make help para ver las opciones disponibles

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(53).png)

+ Ejecutar make all para compilar el kernel y los módulos


+ Una vez leídas las opciones, ejecutamos make all para compilar el kernel, los módulos y hacer una imágen comprimida con bzip (bzImage)

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(54).png)
![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(55).png)

+ Se puede comprobar que make no generó error al revisar el código de salida:

![Tux](https://github.com/ChampionSean/CompilacionKernel/blob/master/img/Captura%20de%20pantalla%20(56).png)

### Creación del paquete `deb` del kernel

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

### Instalación del paquete `deb` del  *kernel*

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
### Herramientas
+ Virtual Box
+ nano
+ gedit
+ git

### Dificultadas
+ La única dificultad que tuve en la práctica fue a la hora de instalar los paquetes con dpkg -i \ en el paquete linux-image..., para arreglar el error solo cambie el nombre por que no encontraba el linux-image...
