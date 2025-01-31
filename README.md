# Cubo-8x8x8_effect

# Cubo LED 8x8x8 con ATmega8
Descripción
Este proyecto consiste en la construcción de un cubo LED 8x8x8 controlado por un microcontrolador ATmega8. Utilicé registros de desplazamiento 74HC595 y transistores ULN2803 para controlar los cátodos de cada piso. A continuación, se describe el proceso de construcción, los materiales utilizados y cómo replicar el proyecto.

<img src="https://github.com/BrandonRv/Cubo-8x8x8_effect/blob/main/fotos/cubo_imagen.jpeg" alt="PROJECT_PHOTO" width="500"/>

## Materiales

- 1x ATmega8
- 9x Registros de desplazamiento 74HC595
- 1x Transistores ULN2803
- 512x LEDs (preferiblemente del mismo color o combinaciones de colores)
- 68x Resistencias de 220Ω (para limitar la corriente de los LEDs)
- xPCB Baquela universal perforada 90cm x 15cm
- 9x socket de 16pines para cada Compuerta 74hc595
- Cables de conexión (Bastantes jejej..)
- 1x Fuente de alimentación de 5V (Puede ser de Celular est no superara los 2 amperios de cosumo)
- 1x Rollo Alambre Galvanizado
- 2x Pines Header Hembra 
- 2x Pines Header Macho
- 1x Cristal 16mhz
- 2x Capitores 22pf
- 2x Resistencias 10kohm
- 3x Pulsadores sencillo (o de acuerdo a la nececidad)
- 1x Capacitor 470uf x 10v
- 1x socket 28pines para el microcontrolador
- 1x socket de 18pines para el array de transistores
- 1x Led Rojo
- 1x Led Verde

## CODIGO ARDUINO 

- Lo encuentras en la carpeta <Cub0_INO>

Esquema del Circuito

![PROJECT_PHOTO](https://github.com/BrandonRv/Cubo-8x8x8_effect/blob/main/Esquematico_CUBO.png)

El cubo utiliza un esquema multiplexado. Los 74HC595 se encargan de controlar las filas de LEDs, mientras que los transistores ULN2803 se utilizan para controlar los cátodos de cada piso del cubo.

Construcción
1. Montaje de la Estructura del Cubo
Preparar los LEDs: Organizar los LEDs en 8 capas de 8x8.
Soldadura: Soldar los ánodos de cada fila juntos y conectar los cátodos de cada columna de LEDs en cada piso.
Cableado de los cátodos: Cada capa (piso) debe conectarse a un transistor ULN2803 para ser controlada.
2. Conexión del Circuito
Conectar los registros de desplazamiento 74HC595: Estos controlarán las columnas de LEDs a través de las resistencias limitadoras.
Conectar el ULN2803: Los cátodos de cada piso están controlados por los transistores ULN2803, que son activados por las salidas del ATmega8.
3. Programación del Microcontrolador
El código fuente para controlar el cubo se encuentra en el archivo Cub0_INO.ino Este código incluye secuencias animadas de encendido y apagado de los LEDs que pueden ser modificadas a voluntad.

Para compilar y cargar el código al ATmega8, sigue estos pasos:

Conecta el ATmega8 a tu computadora utilizando una placa arduino Uno.
Abre el archivo .ino en el IDE de Arduino.

Configura el IDE para usar el microcontrolador ATmega8 seleccionándolo en el menú "Herramientas".

![PROJECT_PHOTO](https://github.com/BrandonRv/Cubo-8x8x8_effect/blob/main/screenshot/cap.jpeg)

Carga el código en el ATmega8.

NOTA: Si no te aparencen las Placas Minicore Utiliza este Json reinicia tu IDE y ya deberia actualizar las librerias
- https://mcudude.github.io/MiniCore/package_MCUdude_MiniCore_index.json

4. Alimentación
El cubo se alimenta con una fuente de 5V. Asegúrate de que la fuente pueda entregar la corriente suficiente para alimentar todos los LEDs.
el consumo total teniento todos lo led encendidos es de aprox de 1amp a 1.5amp no mas de hay todo varia depende del led que uses

## Demo

https://github.com/user-attachments/assets/f515fe18-2103-49e3-8c22-d274ce426c20

## Youtube 

Sera Subido Pronto!!!

