#include <LiquidCrystal.h>
const int rs = 12, en = 11, d4 = 10, d5 = 9, d6 = 8, d7 = 7;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

int v1 = A0;
int v2 = A1;
int v3 = A2;
int v4 = A3;
int v5 = A4;

int light1 = 2;
int light2 = 3;
int light3 = 4;
int light4 = 5;
int light5 = 6;

int a, b, c, d, e;

int buzzer = A5;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  lcd.begin(16, 2);

  pinMode(v1, INPUT);
  pinMode(v2, INPUT);
  pinMode(v3, INPUT);
  pinMode(v4, INPUT);
  pinMode(v5, INPUT);

  pinMode(light1, OUTPUT);
  pinMode(light2, OUTPUT);
  pinMode(light3, OUTPUT);
  pinMode(light4, OUTPUT);
  pinMode(light5, OUTPUT);
  pinMode(buzzer, OUTPUT);

  digitalWrite(light1, LOW);
  digitalWrite(light2, LOW);
  digitalWrite(light3, LOW);
  digitalWrite(light4, LOW);
  digitalWrite(light5, LOW);
  digitalWrite(buzzer, LOW);
}

void loop() {
  // put your main code here, to run repeatedly:
  a = analogRead(v1);
  b = analogRead(v2);
  c = analogRead(v3);
  d = analogRead(v4);
  e = analogRead(v5);

  Serial.print("v1 : ");
  Serial.println(a);

  Serial.print("v2 : ");
  Serial.println(b);

  Serial.print("v3 : ");
  Serial.println(c);

  Serial.print("v4 : ");
  Serial.println(d);

  Serial.print("v5 : ");
  Serial.println(e);

  if (a > 10) {
    digitalWrite(light1, HIGH);
    lcd.setCursor(0, 0);
    lcd.print("V1");
    lcd.setCursor(1, 1);
    lcd.print("1");
    buz();
    delay(2000);
  } else {
    digitalWrite(light1, LOW);
    lcd.setCursor(0, 0);
    lcd.print("V1");
    lcd.setCursor(1, 1);
    lcd.print("0");
  }

  if (b > 10) {
    digitalWrite(light2, HIGH);
    lcd.setCursor(3, 0);
    lcd.print("V2");
    lcd.setCursor(4, 1);
    lcd.print("1");
    buz();
    delay(2000);
  } else {
    digitalWrite(light2, LOW);
    lcd.setCursor(3, 0);
    lcd.print("V2");
    lcd.setCursor(4, 1);
    lcd.print("0");
  }

  if (c > 10) {
    digitalWrite(light3, HIGH);
    lcd.setCursor(7, 0);
    lcd.print("V3");
    lcd.setCursor(8, 1);
    lcd.print("1");
    buz();
    delay(2000);
  } else {
    digitalWrite(light3, LOW);
    lcd.setCursor(7, 0);
    lcd.print("V3");
    lcd.setCursor(8, 1);
    lcd.print("0");
  }

  if (d > 20) {
    digitalWrite(light4, HIGH);
    lcd.setCursor(10, 0);
    lcd.print("V4");
    lcd.setCursor(11, 1);
    lcd.print("1");
    buz();
    delay(2000);
  } else {
    digitalWrite(light4, LOW);
    lcd.setCursor(10, 0);
    lcd.print("V4");
    lcd.setCursor(11, 1);
    lcd.print("0");
  }

  if (e > 10) {
    digitalWrite(light5, HIGH);
    lcd.setCursor(13, 0);
    lcd.print("V5");
    lcd.setCursor(14, 1);
    lcd.print("1");
    buz();
    delay(2000);
  } else {
    digitalWrite(light5, LOW);
    lcd.setCursor(13, 0);
    lcd.print("V5");
    lcd.setCursor(14, 1);
    lcd.print("0");
  }
  delay(200);
}
void buz() {
  digitalWrite(buzzer, HIGH);
  delay(500);
  digitalWrite(buzzer, LOW);
}
