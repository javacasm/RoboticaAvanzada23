[v1 los botones encienden 
leds](https://makecode.microbit.org/_XoChXwfF12HJ)


[v2 funciones sin extensión 
maqueen](https://makecode.microbit.org/_PvpeE5gtCRfu)

Vemos cómo retirar extensiones/paquetes que no usamos

* Javascript -> Explorador

Similar al linkado

[V3 autoapagado](https://makecode.microbit.org/_hcuAMWasM12a)


## Movimientos maqueen

Definimos las funciones de movimiento:

* Adelante
* Atrás
* Derecha
* Izquierda 
* Parar

Calibramos tiempos para giros de 90 grados y movimientos de 50 cm

## Led de maqueen con botones

![](./images/luces_bonotes_maqueen.png)

## Eliminar extensiones o componentes no utilizados

1. Cambiamos a código Javascript

![](./images/luces_bonotes_maqueen_quitar_extension1.png)

2. Pulsamos en explorar

![](./images/luces_bonotes_maqueen_quitar_extension2.png)

3. Podemos eliminar las que tienen el icono de la papelera

![](./images/luces_bonotes_maqueen_quitar_extension3.png)

4. Se elimina la extensión

![](./images/luces_bonotes_maqueen_quitar_extension4.png)

## Pines micro:bit

![](./images/pins-v1-v2.png)

[Detalles sobre los pines](https://makecode.microbit.org/device/pins)

[Más detalles sobre los pines](https://tech.microbit.org/hardware/edgeconnector/)

Hay pines digitales, analógicos, PWM, comunicaciones...

### Encender led de maqueen (P8) con pulsador A (P5)
 
Con eventos:
 
![](./images/Pulsador+leds1.png)

Polling

![](./images/Pulsador+leds2.png)

Uno con polling otro con eventos

![](./images/Pulsador+leds3.png)

![](./images/luces_bonotes_maqueen_sin_extension.png)

## Apagamos los leds pasados 5 segundos

![](./images/luces_bonotes_maqueen_quitar_extension_apagamos.png)

Usamos una variable

## Ejemplos

* Radio: rover, coreografía
* Funciones: control maqueen, "librerias"
* Variables: medida de sensores. Dado con imágenes
* Termostato: intervalos, ventilador
* Ultrasonido: sigueme, personalidades


## Sesión 2

* Maqueen funciones
* Dado en grupo usando radio
* Control de maqueen por radio

## Sesión 3

### Kit avanzado

[Kit avanzado](https://tienda.bricogeek.com/microbit/1686-starter-kit-sensores-37-en-1-para-microbit.html)

![](./images/starter-kit-sensores-37-en-1-para-microbit.jpeg)

[Wiki del kit](https://wiki.keyestudio.com/KS0361(KS0365)_keyestudio_37_in_1_Starter_Kit_for_BBC_micro:bit)


[Extensor](https://tienda.bricogeek.com/microbit/1706-keyestudio-shield-para-sensores-v2-para-microbit.html)

Conexión de componentes: 

* pulsador
* lcd
* servo
* sensor de temperatura

![](./images/EjemploSensoresLCD.png)

[Ejemplo con LCD y sensores](https://makecode.microbit.org/_D0wECTdkHMK5)

![](./images/MontajeLCDSensores.jpeg)

## Proyecto: Rover marciano

Se trata de crear un rover marciano que podemos controlar remotamente, que nos envía datos y que ademas es capaz de reaccionar ante obstáculos. 

Necesitamos 2 micro:bit, una para el mando y otra con maqueen.

Haremos 3 versiones:

0. Funciones de control de maqueen. Vamos a definir una serie de funciones para facilitar el uso de maqueen:

![](./images/rover_funciones_movimiento.png)

1. Control remoto de maqueen vía radio. Usaremos los botones y el logo para enviar órdenes usando caracteres/cadenas

![](./images/rover_receptor_v1.png)

![](./images/rover_receptor_v1.png)

2. Añadimos el extensor y conectamos un pulsador en P1 para ampliar el mando

![](./images/rover_mando_v2.png)

Conectamos un servo en el S1 de maqueen. El servo hará un barrido entre 0 y 180

![](./images/rover_receptor_v2.png)

3. El rover enviará datos que el receptor mostrará.

El rover envía la temperatura vía radio cada segundo como número. 

![](./images/rover_receptor_v3.png)

[Proyecto rover v3](https://makecode.microbit.org/_bxcEpVUyTXCv)

El receptor mostrará los datos en un LCD que hemos conectado vía I2C (pines 20-SDA y 19 SCL)

Añadimos la configuración del LCD (Address 0x27=69)

Añadimos una tarea cada segundo que mostrará en la fila 0 del LCD la temperatura del mando

Cuando recibamos datos numéricos del rover los mostramos en la fila 1

![](./images/rover_mando_v3.png)

[Proyecto mando v3](https://makecode.microbit.org/_EADA3w304YCR)


## Uso de Pines

Lectura analógica + PWM

## Riego

Humedad suelo + LCD + Relé

## Iluminación automática

LCD + LDR + LED PWM

## Meteo

LM35 o DHT11 + LCD




