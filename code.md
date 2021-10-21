//Arduino Piano




#define T_C 262
#define T_D 294
#define T_E 330
#define T_F 349
#define T_G 392
#define T_A 440
#define T_B 493


const int E = 10;
const int F = 9;
const int G = 8;
const int D = 5;
const int C = 6;

const int Buzz = 11;
const int LED = 13;

void setup()
{
  pinMode(LED, OUTPUT);
  pinMode(C, INPUT);
  digitalWrite(C,HIGH);
  
  pinMode(D, INPUT);
  digitalWrite(D,HIGH);
  
  pinMode(E, INPUT);
  digitalWrite(E,HIGH);
  
  pinMode(F, INPUT);
  digitalWrite(F,HIGH);
  
  pinMode(G, INPUT);
  digitalWrite(G,HIGH);
  
 

   digitalWrite(LED,LOW);
}

void loop()
{
  while(digitalRead(C) == LOW)
  {
    tone(Buzz,T_C);
    digitalWrite(LED,HIGH);
  }

  while(digitalRead(D) == LOW)
  {
    tone(Buzz,T_D);
    digitalWrite(LED,HIGH);
  }

  while(digitalRead(E) == LOW)
  {
    tone(Buzz,T_E);
    digitalWrite(LED,HIGH);
  }

  while(digitalRead(F) == LOW)
  {
    tone(Buzz,T_F);
    digitalWrite(LED,HIGH);
  }

  while(digitalRead(G) == LOW)
  {
    tone(Buzz,T_G);
    digitalWrite(LED,HIGH);
  }

  
  

  
  

  noTone(Buzz);
  digitalWrite(LED,LOW);

}
