# Arduino
LDR-CAR
int pin=A0;
int data;
//int en=8;
void setup() {
  pinMode(pin,INPUT);
  pinMode(8,OUTPUT);
  pinMode(9,OUTPUT);
  pinMode(10,OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(13,OUTPUT);
  Serial.begin(9600);
  // put your setup code here, to run once:

}

void loop() {
  
//  analogWrite(en,127);
  // put your main code here, to run repeatedly:
  data=analogRead(A0);
  Serial.println(data);
 // delay(100);
  if(data>=100)
/*digitalWrite(13,1);
  else
  digitalWrite(13,0);
*/  {
    digitalWrite(8,1);
    digitalWrite(9,0);
    digitalWrite(10,0);
    digitalWrite(11,1);
  }
  if(data<=100)
  {
    digitalWrite(8,0);
    digitalWrite(9,0);
    digitalWrite(10,0);
    digitalWrite(11,0);
  }


}
