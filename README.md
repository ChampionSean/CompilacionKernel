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

### Preparacion del sistema operativo

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
