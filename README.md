
## Tabla de contenidos

- [Descripcion](#descripcion)

- [Hardware](#hardware)
- [Ensamblaje](#ensamblaje)
- [Instalacion](#instalacion)
- [Configuracion](#configuracion)
- [Errores frecuentes](#errores)

## Descripcion
[Brewpiless](https://github.com/vitotai/BrewPiLess) es un port de brewpi desarrollado por [vitotai](https://github.com/vitotai). Utiliza un esp8266 para reemplazar a una Raspberry pi y Arduino.

> Ejecutando BrewPi sin Pi, por lo tanto, BrewPi-Less.
<img src="./img/brewpiless.jpg" height="480">

## Hardware

- 1 esp8266 nodemcu
<img src="./img/esp8266.jpg" height="280">

- 1 display Lcd 2004 Backlight Azul 20x4 + Serie I2c Arduino (es importante comprar el que trae adaptador Serie l2c). El display es opcional, pero es cómodo.
<img src="./img/lcd.jpg" height="280">
- 2 sensores digitales temperatura Ds18b20 Cable Sumergible 2 Metros ( comprar el de 2 metros, el de 1 metro queda muy corto)
<img src="./img/sensor.jpg" height="280">
- 1 Modulo Relay Rele De 2 Canales 5v 10a Arduino Pic Avr
<img src="./img/relay.jpg" height="280">
- 1 bornera doble de al menos 5 bocas (se suele conseguir en cualquier casa de electronica)
<img src="./img/bornera.jpg" height="280">
- 20 cables dupont hembra-hembra. 
<img src="./img/Dupont-hembra.png" height="280">
- 1 toma doble (se consigue en ferreterías)
<img src="./img/toma-doble.jpg" height="280">

- 1 resistencia de 4,7k oms (se suele conseguir en cualquier casa de electronica)
- 1 caja para el proyecto ( yo use una caja ciega)
- 1 cargador de celular con cable micro usb (cualquiera que sobre en casa)

## Ensamblaje
El ensamblaje es mas sencillo de lo que parece, solo hay que usar los cables hembra-hembra para conectar cada dispositivo al esp8266.
Este es el diagrama de las conexiones, debajo del mismo dejo algunas notas.  
<img src="./img/BPL_simple.jpg" height="720">

- El 5v power supply seria nuestro cargador de celular, este se conecta directo al nodemcu.
- Entre el cable de data y el de 5v de los sensores Ds18b20 tiene que ir la resistencia.
- La forma mas facil de cablear el esp8266 a bornera es agarrar un cable dupont, sacarle la punta plastica y pelar el cable.  


```
NOTA
Los sensores Ds18b20 pueden venir con 3 configuraciones de colores en los cables.
```

* El tipo 1 donde:
  * Cable rojo: VDD
  * Cable negro: GND
  * Cable amarillo: DQ (data)

  <img src="./img/sonda1.jpg" height="280">
  
 * El tipo 2 donde:
   * Cable rojo: VDD
   * Cable verde: GND
   * Cable amarillo: DQ (data)

  <img src="./img/sonda-2.jpg" height="280">
  
 * El tipo 3 donde:
   * Cable rojo: VDD 
   * Cable verde: DQ
   * Cable amarillo: GND (data)

  <img src="./img/sonda3.jpg" height="280">
  
## Instalacion

Para instalar el software tenemos que descargar algunas herramientas y el codigo

1. Descargar e instalar visual studio code: https://code.visualstudio.com
2. Instalar PlatformIO para visual studio code http://platformio.org/get-started/ide?install=vscode
3. Descargar el codigo de brewpiless https://github.com/vitotai/BrewPiLess/archive/master.zip
4. Una vez descargado el codigo (tarda unos minutos) lo descomprimimos en alguna carpeta y abrimos el visual studio code.

## Configuracion

## Errores frequentes

* Mi lcd prende pero no muestra nada de info
  * Para que el lcd muestre info tenemos que ajustar el potenciometro que trae atras con un destorllinador (cuidado de no tocar las soldaduras) asi establecemos el contraste, solo con girarlo un poco alcanza
 <img src="./img/potenciometro.png" height="280">
