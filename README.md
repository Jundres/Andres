# Andres
Codigo facil para pantalla OLED y Arduino V1.0

//Hecho para nimo2.blospot
//Por ANR Estudiante de ingenieria en sistemas electronicos industriales
//17/11/2018
//"Homo sum, humani nihil a me alienum puto"
//"Nada humano me es ajeno"

#include <Wire.h>//Comunicacion I2C
#include <Adafruit_GFX.h>//Libreria GFX
#include <Adafruit_SSD1306.h>//Libreria SSD1306

#define OLED_RESET 4
Adafruit_SSD1306 display(OLED_RESET);

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  display.begin(SSD1306_SWITCHCAPVCC, 0x3C); //Direccion hexadecimal del OLED
  display.clearDisplay(); //Limpia el buffer del display
}

void loop() {
  // put your main code here, to run repeatedly:
  display.clearDisplay();//Limpiamos el buffer de nuevo
  display.setTextColor(WHITE);//Color del texto
  display.setCursor(0,0);//Posicion del texto
  display.setTextSize(1);//Tamaño del texto
  display.println("Hola, me llamo Andres"); //Texto en pantalla
  display.println(3.141516);//Texto en pantalla
  display.display();//Actualizar informacion en el display
  delay(1000);//Delay de un segundo
}

//Hecho para nimo2.blospot
//Por ANR Estudiante de ingenieria en sistemas electronicos industriales
//17/11/2018
//"Homo sum, humani nihil a me alienum puto"
//"Nada humano me es ajeno"
