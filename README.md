# RoBotO.1

<h3>Mobile Controlled Robot Components</h3><ul><li>Arduino Uno with cable: 1</li><li>IR Sensor:&nbsp; 2</li><li>L293D Module: 1</li><li>Jumper Wires: 20pcs</li><li>Chassis: 1</li><li>BO Motor: 2</li><li>Caster wheel: 1</li><li>Breadboard: 1</li><li>Wheels: 2</li><li>Screws set – 1</li><li>Clamps – 2</li><li>9v Battery – 2</li><li>Battery Snap – 2</li></ul>
<h3>Components:</h3>
<p align="left">
  <img src="components.jpg" width="650" title="Components">
</p>
<h3>Circuit Diagram:</h3>
<p align="left">
  <img src="circuit-diagram.jpg" width="650" title="Components">
</p>
<h3>Code:</h3>

```c++
// code away!
/*------ Arduino Code----- */ 
/*-------definning Inputs------*/ 
#define LS 2      // left sensor 
#define RS 3      // right sensor 
 
/*-------definning Outputs------*/ 
#define LM1 4       // left motor 
#define LM2 5       // left motor 
#define RM1 6       // right motor 
#define RM2 7       // right motor
void setup () { 
    pinMode(LS, INPUT);
    pinMode(RS, INPUT);   
    pinMode(LM1, OUTPUT);   
    pinMode(LM2, OUTPUT);   
    pinMode(RM1, OUTPUT);   
    pinMode(RM2, OUTPUT);
} 
void loop() { 
  if(digitalRead(LS) && digitalRead(RS))     // Move Forward 
  { 
    digitalWrite(LM1, HIGH);     
    digitalWrite(LM2, LOW);     
    digitalWrite(RM1, HIGH);     
    digitalWrite(RM2, LOW); 
  } 
   
  if(!(digitalRead(LS)) && digitalRead(RS))     // Turn right 
  { 
    digitalWrite(LM1, LOW);     
    digitalWrite(LM2, LOW);     
    digitalWrite(RM1, HIGH);     
    digitalWrite(RM2, LOW); 
  } 
   
  if(digitalRead(LS) && !(digitalRead(RS)))     // turn left 
  { 
    digitalWrite(LM1, HIGH);     
    digitalWrite(LM2, LOW);     
    digitalWrite(RM1, LOW);     
    digitalWrite(RM2, LOW); 
  } 
   
  if(!(digitalRead(LS)) && !(digitalRead(RS)))     // stop 
  { 
    digitalWrite(LM1, LOW);     
    digitalWrite(LM2, LOW);     
    digitalWrite(RM1, LOW);     
    digitalWrite(RM2, LOW); 
  } 
} 
```

