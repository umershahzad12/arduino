# THEREMIN ÓPTICO

## primer projecto 

## Explain 

In the first project me and hanzla we did a circuit in which if we put hand on the sensor it stop 

and if we take away hand from the sensor it starts working.

### IMAGEN

Aqui esta imagen de primer projecto

![](https://github.com/Hanzla55/Arduino/blob/main/therminal%202(1).jpg?raw=true)

### CODIGO
``` C++
int sensorValue;

int sensorLow = 500;

int sensorHigh = 0;

const int ledPin = 13;

void setup(){

 
    
     pinMode(ledPin, OUTPUT);

     digitalWrite(ledPin, HIGH);

while (millis() < 5000) {

      sensorValue = analogRead(A0);

          if (sensorValue > sensorHigh) {

                    sensorHigh = sensorValue;

          }

          if (sensorValue < sensorLow) {

                    sensorLow = sensorValue;

          }

 }//Fin del bucle while.

     digitalWrite(ledPin, LOW);

 Serial.begin(9600);

} //Fin de la funcion setup.

void loop() {

 

        sensorValue = analogRead(A0);
        Serial.println(sensorValue);

int pitch = map(sensorValue, sensorLow, sensorHigh, 50, 4000);

     tone(8,pitch,20);

         delay(10);

 

}
```




## SEGUNDO PROJECTO

In the second project 

### IMAGEN

![](https://github.com/Hanzla55/Arduino/blob/main/therminal%202.jpg?raw=true)

### CODIGO




## TERCER PROJECTO

### IMAGEN
![](https://github.com/Hanzla55/Arduino/blob/main/therminal%203.jpg?raw=true)


### CODIGO

``` C++
int sensorValue;

int sensorLow = 500;

int sensorHigh = 0;

const int ledPin = 13;

void setup(){

 
     pinMode(2,INPUT);
     pinMode(ledPin, OUTPUT);

     digitalWrite(ledPin, HIGH);

while (millis() < 5000) {

      sensorValue = analogRead(A0);

          if (sensorValue > sensorHigh) {

                    sensorHigh = sensorValue;

          }

          if (sensorValue < sensorLow) {

                    sensorLow = sensorValue;

          }

 }//Fin del bucle while.

     digitalWrite(ledPin, LOW);

 Serial.begin(9600);

} //Fin de la funcion setup.

void tocarTheremin() {

 

        sensorValue = analogRead(A0);
        Serial.println(sensorValue);

int pitch = map(sensorValue, sensorLow, sensorHigh, 50, 4000);

     tone(8,pitch,20);

         delay(10);
}

 void loop() {
  
 int estadoBoton = digitalRead(2);
     if (estadoBoton == HIGH){
        tocarTheremin();
     }
     else{
       noTone(8);
       delay(10);
     } //llave else
 }//llave loop
 ```

## QUARTO PROJECTO

### CODIGO
``` C++
int sensorValue;

int sensorLow = 500;

int sensorHigh = 0;

const int ledPin = 13;

int switchState = 0;
bool isTheButtonBeingPressed = false;
bool play = false;

int buttonPin = 2;

void setup(){

 
     pinMode(buttonPin, INPUT);
     pinMode(ledPin, OUTPUT);

     digitalWrite(ledPin, HIGH);

while (millis() < 5000) {

      sensorValue = analogRead(A0);

          if (sensorValue > sensorHigh) {

                    sensorHigh = sensorValue;

          }

          if (sensorValue < sensorLow) {

                    sensorLow = sensorValue;

          }

 }//Fin del bucle while.

     digitalWrite(ledPin, LOW);

 Serial.begin(9600);

} //Fin de la funcion setup.

void tocarTheremin() {

 

        sensorValue = analogRead(A0);
        Serial.println(sensorValue);

int pitch = map(sensorValue, sensorLow, sensorHigh, 50, 4000);

     tone(8,pitch,20);

         delay(10);
}

 void loop() {
   checkButton();
  if (play) {
        tocarTheremin();
     }
     else{
       noTone(8);
       delay(10);
     } //llave else
 }//llave loop


 void checkButton(){
  switchState = digitalRead(buttonPin);
  if (switchState == HIGH && !isTheButtonBeingPressed){
    play = !play;
    isTheButtonBeingPressed = true;
  }
  
  if (switchState == LOW)
  {
  isTheButtonBeingPressed = false;
  }

}
```
 
