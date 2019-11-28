# code-dot
#include <Servo.h>
Servo servoLeft;
Servo servoRight;

void setup() {
tone (4,3000, 1000);
delay(1000);
servoLeft.attach(13);
servoRight.attach(12);

forward(2000);
turnLeft(600);
turnRight(600);
backward(2000);



}

void loop() {
forward(2000);
turnLeft(600);
turnRight(600);
backward(2000);


}
void forward(int time)
{
  servoLeft.writeMicroseconds(1700);
  servoRight.writeMicroseconds(1300);
  delay(time);
}

void turnLeft(int time)
{
  servoLeft.writeMicroseconds(1300);
  servoRight.writeMicroseconds(1300);
  delay(time);
}
void turnRight(int time)
{ servoLeft.writeMicroseconds(1700);
  servoRight.writeMicroseconds(1700);
  delay(time);
}

  void backward (int time)
{ servoLeft.writeMicroseconds(1300);
  servoRight.writeMicroseconds(1700);
  delay(time);
}

void disableServos()
{ servoLeft.detach();
  servoRight.detach();
 
}
