# Lab-5-TEC-284

#include <Wire.h>
#include <Adafruit_MotorShield.h>
#include "utility/adafruit_MS_PWMServoDriver.h"

Adafruit_MotorShield AFSM = Adafruit_MotorShield();

Adafruit_DCMotor *rightMotor = AFSM.getMotor(4);
Adafruit_DCMotor *leftMotor = AFSM.getMotor(3);

void setup() 
{
  AFSM.begin();
  

}

void loop() 
{

    

  


directionForward();
directionRight();
directionForward2();
directionLeft();
directionRight2();
directionForward3();

//directionBackwards();


}
void directionForward() {
  rightMotor->setSpeed(200);
  leftMotor->setSpeed(200);


rightMotor->run(FORWARD);
leftMotor->run(FORWARD);

delay(1500); // good
}

void directionForward2() {
  rightMotor->setSpeed(200);
  leftMotor->setSpeed(200);


rightMotor->run(FORWARD);
leftMotor->run(FORWARD);

delay(500); // good
}

void directionForward3() {
  rightMotor->setSpeed(200);
  leftMotor->setSpeed(200);


rightMotor->run(FORWARD);
leftMotor->run(FORWARD);

delay(5000); // good
}
void directionLeft() 
{
rightMotor->setSpeed(100);
leftMotor->setSpeed(100);


rightMotor->run(BACKWARD);
leftMotor->run(FORWARD);

delay(750);
}



void directionRight () 
{
rightMotor->setSpeed(100);
leftMotor->setSpeed(100);
  rightMotor->run(FORWARD);
leftMotor->run(BACKWARD);

delay(750);
}

void directionRight2 () 
{
rightMotor->setSpeed(100);
leftMotor->setSpeed(100);
  rightMotor->run(FORWARD);
leftMotor->run(BACKWARD);

delay(200);
}


/*void directionBackwards () 
{
rightMotor->setSpeed(100);
leftMotor->setSpeed(100);

rightMotor->run(BACKWARD);
leftMotor->run(BACKWARD);

delay(2000);

}
*/




