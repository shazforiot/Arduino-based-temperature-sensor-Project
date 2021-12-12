int baselineTemp = 0;
int celsius = 0;

void setup()
{
  pinMode(A0, INPUT);
  Serial.begin(9600);

  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
}
void loop()
{
  baselineTemp = 20;
  
  celsius = map(((analogRead(A0) - 20) * 3.04), 0, 1023, -40, 125);
  
  Serial.print(celsius);
  Serial.println(" C, ");
 
  if (celsius < baselineTemp) {
    digitalWrite(2, LOW);
    digitalWrite(3, LOW);
    
  }
  if (celsius >= baselineTemp && celsius < baselineTemp + 20) {
    digitalWrite(2, HIGH);
    digitalWrite(3, LOW);
    
  }
  if (celsius >= baselineTemp + 20 && celsius < baselineTemp + 40) {
    digitalWrite(2, LOW);
    digitalWrite(3, HIGH);
    
  }
  
  if (celsius >= baselineTemp + 40) {
    digitalWrite(2, HIGH);
    digitalWrite(3, HIGH);
    
  }
  delay(1000); 
}
