# Week 7 -10/9 - Motors and Microcontrollers! #

This week, we got started on out projects and figuring out what all the different components are. 
Some of the work we've done so far includes:

October 4, 2023, Wednesday
- Testing 1/8” wire with the DI Wire machine in the makerspace 
- Has the capability to bend wire left/right

October 9, 2023, Monday
- Tested 1/16”  wire in stainless steel and aluminum.
- Used a chisel as a bending plate to test possibilities by changing angles, pitch yaw and roll.
- Stainless steel works well since it can hold its shape and is stiffer. Aluminum was too malleable and ended up kinking in the machine.
- Wire didn't follow the exact path we expected, but we realized its because the wire was rolling while being fed.
- Was able to get a twisted wire after many attempts, shown below.

[![Wire Bending](Images/Wire_Test_1.png)](https://vimeo.com/873771388?share=copy)
[![Wire Bending 2](Images/Wire_Test_2.png)]

In addition, we were able to get our motors working with and without an accelerometer by following the intro tutorials on Github!

Servo Motor without Acceleromater: 

```
SYSTEM_THREAD(ENABLED);
Servo serv;

int servoPin = D1;
int pos = 0;

void setup() {
  Serial.begin(9600);
  Serial.println("Started");
  serv.attach(servoPin);
}

void loop() {
  serv.write(120);
  delay(2500);
  serv.write(90);
  delay(2500);
  Serial.println("test");
  Serial.println(serv.read());
}
```

