# operadores

leer pinao ( analog read-0-1023)(8 bytes)

digitalwrite (du gon abserva en la pigana) es una funcationa que nos pide  un nomebro de pin y el lalor high(O) o low (O)

si el valor es high la placa sumimistirar su en es pin 

si el valor es low ,la placa sumimistirar ov en ese pin 

si hay si,se se actiuaron los circutos si es ov no je activiros 

else (temperature > = baselinetemp+2 &&
temperature < = baselinetemp+4){

Digitalwrite(2,high);

Digitalwrite(3,low);

Digitalwrite(4,low);

}else if (temperature > = baselinetemp+4 &&
temperature < baselinetemp+6){

Digitalwrite(2,high);

Digitalwrite(3Digitalwrite

Digitalwrite(4,low);

}else if(temperature >= baselinetemp+6){

Digitalwrite(2,high);

Digitalwrite(3,high);

Digitalwrite(4,high);

ejercicio
Vamos a conectsr 2 botones y 2 LEDs

Haremos diferentes programas con diferencias comportamientos.

Para poner un boton necesitamos poner una resistencia de 10000 (ohmnios), estas son las que tienen cuerpo beige y una linea naranja.

Pin _____ Pulsasdor __ GND

5V _____ Resistencia 10k ohmnios

Esquema de botón "Por defecto de arriba" o "Pulled - HIGH"

Conectaremos 2 botónes. Uno al pin 2 y otro pin 3. Para poner un LED necesitamos una resistencia de 220 ohmnios las de cuerpo azul.

Hay que tener en cuenta la polaridad del LED. La pata mas corta va hacia el GND (o 0V) y la larga hacia el voltaje.

PIN -->---///---GND

LED 220

Da igual si la resistencia va detras p delante de LED. Contraemos 2 LEDs, uno al pin 4 y otro al pin 5.

Al principio no funcionaba, por que si pones tilde no funciona

![imagen](https://user-images.githubusercontent.com/90753298/140055897-070f5dfd-bc74-4f35-a1bc-83daf181efa8.png)

Este es el código:

https://github.com/ANGEY33/Arduino/blob/main/Operadores1.ino.ino

# Ejercicio 2 

Encender los 2 LEDs si pulsamos cualquiera de los botones si no apagamos

![imagen](https://github.com/ANGEY33/Arduino/blob/main/Captura%20de%20pantalla%20de%202021-11-03%2012-52-32.png)

Este es el código:

https://github.com/ANGEY33/Arduino/blob/main/operadores2.ino.ino

