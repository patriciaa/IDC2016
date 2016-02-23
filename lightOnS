#include <SoftwareSerial.h>
#define Rx 10 //DOUT to p10
#define Tx 11 // DIN to p11
SoftwareSerial Xbee (Rx, Tx);
void setup() {
  pinMode(13, OUTPUT);
  Serial.begin(9600);
  Xbee.begin(9600);
  delay(500);
}
void loop() {
  if (Serial.available()) {
    char outgoing = Serial.read();
    Xbee.print(outgoing);
  }
  if (Xbee.available()) {
    char incoming = Xbee.read();
    Serial.println(incoming);
    if (incoming == 's') {
    digitalWrite(13, HIGH);
  }
  }
  
  delay(50);
}
