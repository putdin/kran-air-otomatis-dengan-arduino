#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C lcd(0x27, 16,4);
const int pinTrig = 8;
const int pinEcho = 9;
const int kran = 13;
int jarak;

void setup() {
  // put your setup code here, to run once:
 lcd.init();
 lcd.backlight();
 lcd.setCursor(0,0);
 lcd.setCursor(0,0);
 lcd.print("  KHAMIM-ANGGI");
 lcd.setCursor(0,1);
 lcd.print("FUDIN-KAHFI-ALIF");  

 pinMode(pinTrig, OUTPUT);
 pinMode(pinEcho, INPUT);
 pinMode(kran,OUTPUT);
 digitalWrite(kran,LOW);
 delay (8500);  
 
}
void loop() {
  // put your main code here, to run repeatedly:
 digitalWrite(pinTrig, HIGH);
 delayMicroseconds(10);
 digitalWrite(pinTrig, LOW);
 float durasi = pulseIn(pinEcho, HIGH);
 jarak =(durasi *0.034)/2;
 Serial.println (jarak );

if (jarak < 40) {
  digitalWrite(kran,LOW);
  lcd.setCursor(00,00);
  lcd.print("  TERUS   JAGA    ");
  lcd.setCursor(00,01);
  lcd.print ("   KEBERSIHAN    " );
}
else {
  digitalWrite(kran,HIGH);
  lcd.setCursor(00,00);
  lcd.print("READY , DEKATKAN  ");
  lcd.setCursor(00,01);
  lcd.print ("  TANGAN  ANDA   ");
}
}
