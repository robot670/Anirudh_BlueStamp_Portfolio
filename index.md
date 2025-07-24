# Robotic Arm
<!---


Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!
--->

My project this summer at Bluestamp was a phone-controlled robotic arm and car project. When I press a button on my phone, it sends inputs to my robot, which then moves the servos and motors of my robot. This allows me to control my robotic arm precisely. I also added pick-up and drop-off positions, which allowed my robotic arm to function like a human arm to pick up and move objects. For my modification, to increase the range of my robotic arm's ability to pick up objects, I added a car with four DC motors underneath, allowing me to pick up objects from anywhere. 

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Anirudh K. | Mission San Jose High School | Mechanical Engineering | Incoming Junior |

![PXL_20250724_154950807](https://github.com/user-attachments/assets/64098335-6aa5-4b05-9e02-9a43c5972e2a)


<!--- 
**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
--->




# Modification Milestone

## Description

For my modification milestone, I improved my phone-controlled robotic arm by attaching it to a 4WD chassis (Refer to Figure 11 for wiring schematic). This allows me to pick up objects from anywhere using my robot. To move the chassis, I used an H-Bridge to allow my wheels to switch directions, allowing for all directions of movement: forward, backward, left, and right. To turn left and right, I move one side of the chassis forward and the other backward. To add these new features to my robot, I added many new buttons to the app I made on MIT App Inventor to move the car in all directions (Figure 1). I used the button touchdown and touchup commands in MIT App Inventor for these movements, because they were not set positions (Figure 2). In addition to the chassis, I also added many 3D printed components, such as clamps to keep my robotic arm's base down to the chassis, walls for structural rigidity, and a power button switch box at the back of the robot to turn the external battery pack powering my DC motors on and off. 


<img width="400" height="800" alt="share_5599700110188042459323423" src="https://github.com/user-attachments/assets/464791e7-acd8-4fb7-b3ed-db60713c9fde" />
<img width="400" height="800" alt="image" src="https://github.com/user-attachments/assets/b638ed03-402d-45b5-8941-11c6f1b2f889" />

Figure 1: Robotic Arm and Car buttons
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Figure 2: Robotic Arm and Car button input code

## How it works

DC motors can change direction based on the direction of their current. An L298N H-Bridge can connect to 2 motors to drive them and change their direction (Figure 3). Although it can only connect to 2 motors, the left and right side pairs of motors always move at the same time and direction, so only 2 connections are needed. By changing the direction of either side of the car's motors, the car can move in any direction, left, right, forward, or backward. 

<img width="383" height="199" alt="image" src="https://github.com/user-attachments/assets/001502f7-a8bc-41cb-8475-e51b666137b4" />

Figure 3: How an H-Bridge works


## Challenges

One of my biggest challenges during this milestone was with my H-Bridge. I connected the batteries to my H-Bridge to power it and the DC motors, but the wheels did not turn, even though the Arduino pins were connected. I found that the H-Bridge needed 5V of regulated power in its VCC port, and would not work properly otherwise. I saw that I should use the Arduino to power the H-Bridge using the VCC port and power the DC motors using the batteries on the power port (Figure 4). When I connected it, I found that the H-Bridge operated correctly and moved the motors based on the inputs. One problem with this is that I had only one 5V output from my Arduino, and I needed it for both the H-Bridge and the HC-05 Bluetooth module. To solve this problem, I used a breadboard to create a parallel circuit to power both devices (Figure 5).

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/db913237-d182-4f6d-b2ca-b3e975594506" />

Figure 4: H-Bridge connection ports

<img width="543" height="579" alt="image" src="https://github.com/user-attachments/assets/db65744f-c754-4b18-9eac-1fda89c7fd35" />

Figure 5: Parallel Connection

I also found that the battery pack powering my DC motors ran out of charge quickly because it was always powering the H-Bridge. To prevent this, I had to remove one battery each time I wanted to turn off power to the H-Bridge and DC motors. To make this a lot more seamless, I added a power button that allowed me to turn the power on and off for the H-Bridge and DC motors. This power button was mounted at the back of the robot using the power button switch push-fit box.


## 3D printed components

In my modification milestone, I added numerous 3D-printed components that I designed using Fusion 360 to my robot. I 3D printed the clamps that hold down my robotic arm to the top plate of my chassis (Figure 6). These surround the bottom plate of the robotic arm to provide a secure fit, both horizontally and vertically. These clamps have slits that allow me to use holes on the top chassis plate, which are at various distances away from the base of the robotic arm. 

<img width="796" height="427" alt="image" src="https://github.com/user-attachments/assets/91a2d3f5-fa0f-4309-8109-d0b1995ceb11" />

Figure 6: Robotic arm base clamp


I also added a power button box that holds the power button for my motor (Figure 7). Since my motors require a separate battery pack from my Arduino, they did not have a power switch, and would always be on. To prevent this, I added a power button switch and a 3D printed holder for it. This holder is a push-fit box, so I did not need any complex locking mechanisms. It is screwed into the top chassis plate, similar to the clamps for my robotic arm.

<img width="695" height="506" alt="image" src="https://github.com/user-attachments/assets/97185c3c-b971-477c-84cc-e20fad0ce303" />

Figure 7: Power button switch box


To make my robot look more appealing and similar to a car, I added many 3D-printed wall components to the top and bottom of the chassis. I used 4 components screwed onto the top chassis plate that go above the wheels (Figure 8). Screws thread into these components and hold them in place. The bottom components between the top and bottom chassis plates cover the inner components and wiring of the robot and add to the walls on top of the chassis. The front and back components cover the corners of the chassis (Figure 10), while the middle components go between the wheels of the robot. (Figure 9) In total, this gives the robot a much more finished look. This also greatly improves the structural integrity of my robot.


<img width="699" height="460" alt="image" src="https://github.com/user-attachments/assets/0f69c938-ce9f-45c9-839d-f4c8a119c8ed" />

Figure 8: Car side top component

<img width="692" height="433" alt="image" src="https://github.com/user-attachments/assets/63445e42-8d5d-4275-b83d-58d9ab1a4573" />

Figure 9: Middle car wall component

<img width="722" height="418" alt="image" src="https://github.com/user-attachments/assets/3dbe54cd-0657-4c7b-90ba-0a4f6a5f0e80" />

Figure 10: Back/Front car wall component


## Pictures

<img width="630" height="524" alt="image" src="https://github.com/user-attachments/assets/c10a0fd6-47d1-409b-a2db-cae0aa7d5fb0" />

Figure 11: Wiring schematic for all components (Arduino, batteries, servos, HC-05 Bluetooth module, H-bridge, DC motors, power switch)

## Modification Milestone Code
<details>
  <summary> Click to see code </summary>

```c++

// Uses the Software Serial and the Bluetooth Serial for the Bluetooth functionality
#include <SoftwareSerial.h>
SoftwareSerial Phone (A0,A1);

// Uses the library for the servo/arm that moves, reads, and sets the position of the servos.
#include "src/CokoinoArm.h"
CokoinoArm arm;                                                   //Declares object 'arm' in class 'CokoinoArm'
                                                                  //Object arm is used for all arm commands
// Declares the inputs that are read in the Bluetooth serial
char values;


// Declares the inputs from the joysticks
int xL,yL,xR,yR;


int motor1pin1 = 2;
int motor1pin2 = 3;

int motor2pin1 = 4;
int motor2pin2 = 5;



//Servo and bluetooth setup
void setup() {
  arm.ServoAttach(6,7,10,11);                                     // arm of servo motor connection pins
  Serial.begin(38400);                                            // Serial baud rate
    Phone.begin(9600);                                            // Bluetooth serial baud rate

  pinMode(motor1pin1, OUTPUT);
  pinMode(motor1pin2, OUTPUT);
  pinMode(motor2pin1, OUTPUT);
  pinMode(motor2pin2, OUTPUT);

}

// Runs repeatedly
void loop() {

// Looks for inputs in the Bluetooth serial
if (Phone.available()>0){
  values = Phone.read();                                          // Reads the values from the Bluetooth serial and saves them as the variable "values" 
    Serial.print(values);
}


// Bluetooth


// If the buttons are unpressed, the input will be '0', which makes the servos stop moving
if (values == '0'){ 
  arm.down(0);
  arm.up(0);
  arm.right(0);
  arm.left(0);
  arm.open(0);
  arm.close(0);
}


// Moves the arm down when input is 'a'
if (values == 'a'){
  arm.down(45);                                                   // Function to move arm down
}                                                                 // (#) = Speed of the servo movement

// Moves the arm up when input is 'b'
if (values == 'b'){
  arm.up(45);                                                     // Function to move arm up
}

// Moves the rotating base to the right when input is 'c'
if (values == 'c'){
  arm.right(10);                                                  // Function to move arm to the right
}

// Moves the rotating bases to the left when input is 'd'
if (values == 'd'){
  arm.left(10);                                                   // Function to move arm to the left
}

// Opens the claw when input is 'e'
if (values == 'e'){
  arm.open(5);                                                    // Function to open claw
}

// Closes the claw when input is 'f'
if (values == 'f'){
  arm.close(5);                                                   // Function to close claw
}


// Resets all servos when input is 'g'
if (values == 'g'){
  arm.servo1.write(82);                                           // Function to set servo at a certain angle
  arm.servo2.write(90);                                           // Reset position servo angles
  arm.servo3.write(100);
  arm.servo4.write(90);
}

// Goes to pickup position when input is 'h'
if (values == 'h'){
  arm.servo1.write(82);                                           // Pickup position servo angles
  arm.servo2.write(180);
  arm.servo3.write(0);
  arm.servo4.write(35);
}

// Goes to dropoff position when input is 'i'
if (values == 'i'){
  arm.servo4.write(0);                                            // Dropoff position servo angles
  arm.servo1.write(180);
  arm.servo2.write(90);
  arm.servo3.write(0);
  arm.servo4.write(0);

}


// Opens the claw when input is 'k'
if (values == 'j'){
  arm.servo4.write(30);                                           // Sets claw servo to 30 degrees (opens claw)
}

// Closes the claw when input is 'l'
if (values == 'k'){
  arm.servo4.write(0);                                            // Sets claw servo to 0 degrees (closes claw)
} 

//Moves the arm to inside the robot to store object in robot when input is 'j'
if (values == 'l'){
  arm.servo1.write(82);
  arm.servo2.write(45);                                           // Storage position servo angles
  arm.servo3.write(135);
  arm.servo4.write(0);
}

// If the buttons are unpressed, the input will be '1', which makes the motors stop moving
if (values == '1'){
  digitalWrite(motor1pin1, LOW);
  digitalWrite(motor1pin2, LOW);
  digitalWrite(motor2pin1, LOW);
  digitalWrite(motor2pin2, LOW);
}

// Moves the robot forward
if (values == 'm'){
  digitalWrite(motor1pin1, LOW);
  digitalWrite(motor1pin2, HIGH);

  digitalWrite(motor2pin1, HIGH);
  digitalWrite(motor2pin2, LOW);
}

//Moves the robot backward
if (values == 'n'){
  digitalWrite(motor1pin1, HIGH);
  digitalWrite(motor1pin2, LOW);

  digitalWrite(motor2pin1, LOW);
  digitalWrite(motor2pin2, HIGH);
}

// Rotates the robot to the left
if (values == 'o'){
  digitalWrite(motor1pin1, LOW);
  digitalWrite(motor1pin2, HIGH);

  digitalWrite(motor2pin1, LOW);
  digitalWrite(motor2pin2, HIGH);
}

//Rotates the robot to the right
if (values == 'p'){
  digitalWrite(motor1pin1, HIGH);
  digitalWrite(motor1pin2, LOW);

  digitalWrite(motor2pin1, HIGH);
  digitalWrite(motor2pin2, LOW);
}


delayMicroseconds(20);                                            // Delays for 20 microseconds to prevent too many inputs at once

}
```
</details>


# Third Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZH-uhBaCyNU?si=-JbVSa9VHABHDd5z" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>




## Description

For my third milestone, I added wire sleeves, rubber bands for my claw, a box for my HC-05, and buttons coded to preset positions. The wire sleeves significantly made my wiring more manageable and less visible, while still allowing a full range of motion for my servos and arm movements. Rubber bands on my claw improved my grip, allowing me to pick up objects from the ground. The box for my HC-05 allowed me to mount the HC-05 onto my robotic arm while allowing me to wire it and check its pairing light. I added buttons to my app on MIT App Inventor that are coded to preset positions, allowing me to, at the press of a button, hover my claw over an object in front of the arm to pick it up (Figure 12). With another button, I close the claw on the object. Finally, another button moves that object to another preset position for drop-off. 

<img width="500" height="646" alt="share_4075640570769880466424253545243" src="https://github.com/user-attachments/assets/b039986f-bc43-401b-8257-019ce75cadf1" />

Figure 12: New buttons for preset positions


## Challenges

One of my small challenges was my wiring. Since I have a rotating base, the wiring can get stuck when the rotating base moves. To solve this, I used wire sleeves and zip ties to keep wires close to the arm and away from the rotating base, allowing for a full range of motion for my robotic arm. Without wiring in the way, my wire sleeves gave my arm a much cleaner and sleeker look.

I used Fusion 360 to design my HC-05 Bluetooth module box, which I made using a 3D printer (Figure 13). I had to go through multiple iterations because it was difficult to get the hole spacing correct, as measuring by hand is inconsistent, even with calipers. In these iterations, I also had to modify the dimensions of the HC-05 box until it fit the HC-05 Bluetooth module perfectly. I decided on using a push-fit lid for my box because it is simple to print and doesn't require me to modify the box (Figure 14).



<img width="823" height="527" alt="image" src="https://github.com/user-attachments/assets/efe8b9d0-9c7a-4a49-ad69-bdc8f2414d17" />

Figure 13: Drawing and picture of the HC-05 Bluetooth module box 

<img width="784" height="316" alt="image" src="https://github.com/user-attachments/assets/57fdba30-df8a-4f1e-82ee-6275534c465f" />

Figure 14: Drawing and picture of the HC-05 Bluetooth module box push-fit lid



One of the biggest things that I wanted to do for this milestone was to be able to pick up objects with my claw. This would allow my robotic arm to pick up objects with its degrees of freedom, like a human arm. I found that the perfect angle to pick up objects was perpendicular to the ground. However, since the robotic arm was not mounted high, it would cause the claw to dig into the ground. To move my claw to the best angle possible, I decreased the angle of servo 2 and increased the angle of servo 3. This was my pickup preset, which sets my arm on the ground and opens the claw to 35 degrees to be at the right position to pick up objects. 

I found that my current claw, made of acrylic, did not have enough grip to hold the object while moving it to the drop-off position. The objects kept falling out of the claw. To solve this problem, I added rubber bands to my claw to increase its grip strength (Figure 15). This allows me to pick up objects at any position and drop them off in the drop-off position. 


![PXL_20250710_170534942~2](https://github.com/user-attachments/assets/dc52142a-b383-40f5-86be-baf399cc779d)

Figure 15: Rubber band claw grip


I also found another issue that caused my transfer between pickup and dropoff to fail. When my arm was moving between those positions, my claw opened for a moment, causing the object I was picking up to fall out. I first attempted to fix this by tightening all of my screws. However, this did not work. Then, I realized that the moment between pickup and dropoff was when all 4 servos were being used at the same time. This caused the 4th servo (claw) to lose power for a moment, dropping the object. To solve this, I replaced the battery, and it worked correctly. 

## Third Milestone Code
<details>  
  <summary> Click to see code </summary>

```c++

// Uses the Software Serial and the Bluetooth Serial for the Bluetooth functionality
#include <SoftwareSerial.h>
SoftwareSerial Phone (A0,A1);

// Uses the library for the servo/arm that moves, reads, and sets the position of the servos.
#include "src/CokoinoArm.h"
CokoinoArm arm;                                                   //Declares object 'arm' in class 'CokoinoArm'
                                                                  //Object arm is used for all arm commands
// Declares the inputs that are read in the Bluetooth serial
char values;


// Declares the inputs from the joysticks
int xL,yL,xR,yR;



//Servo and bluetooth setup
void setup() {
  arm.ServoAttach(6,7,10,11);                                       // arm of servo motor connection pins
  Serial.begin(38400);                                            // Serial baud rate
    Phone.begin(9600);                                            // Bluetooth serial baud rate
  arm.JoyStickAttach(A2,A3,A0,A1);                                // Initializes the Joysticks
}

// Runs repeatedly
void loop() {

// Looks for inputs in the Bluetooth serial
if (Phone.available()>0){
  values = Phone.read();                                          // Reads the values from the Bluetooth serial and saves them as the variable "values" 
    Serial.print(values);
}

// Bluetooth


// If the buttons are unpressed, the input will be '0', which makes the servos stop moving
if (values == '0'){ 
  arm.down(0);
  arm.up(0);
  arm.right(0);
  arm.left(0);
  arm.open(0);
  arm.close(0);
}


// Moves the arm down when input is 'a'
if (values == 'a'){
  arm.down(45);                                                   // Function to move arm down
}                                                                 // (#) = Speed of the servo movement

// Moves the arm up when input is 'b'
if (values == 'b'){
  arm.up(45);                                                     // Function to move arm up
}

// Moves the rotating base to the right when input is 'c'
if (values == 'c'){
  arm.right(10);                                                  // Function to move arm to the right
}

// Moves the rotating base to the left when input is 'd'
if (values == 'd'){
  arm.left(10);                                                   // Function to move arm to the left
}

// Opens the claw when input is 'e'
if (values == 'e'){
  arm.open(5);                                                    // Function to open claw
}

// Closes the claw when input is 'f'
if (values == 'f'){
  arm.close(5);                                                   // Function to close claw
}


// Resets all servos when input is 'g'
if (values == 'g'){
  arm.servo1.write(82);                                           // Function to set servo at a certain angle
  arm.servo2.write(90);                                           // Reset position servo angles
  arm.servo3.write(100);
  arm.servo4.write(90);
}

// Goes to pickup position when input is 'h'
if (values == 'h'){
  arm.servo1.write(82);                                           // Pickup position servo angles
  arm.servo2.write(150);
  arm.servo3.write(0);
  arm.servo4.write(35);
}

// Goes to dropoff position when input is 'i'
if (values == 'i'){
  arm.servo4.write(0);                                            // Dropoff position servo angles
  arm.servo1.write(180);
  arm.servo2.write(90);
  arm.servo3.write(0);
  arm.servo4.write(0);

}

//Goes to pickup from current base position when input is 'j'
if (values == 'j'){
  arm.servo2.write(150);                                          // Pickup position servo angles without base movement
  arm.servo3.write(0);
  arm.servo4.write(35);
}

// Opens the claw when input is 'k'
if (values == 'k'){
  arm.servo4.write(30);                                           // Sets claw servo to 30 degrees (opens claw)
}

// Closes the claw when input is 'l'
if (values == 'l'){
  arm.servo4.write(0);                                            // Sets claw servo to 0 degrees (closes claw)
} 




delayMicroseconds(20);                                            // Delays for 20 microseconds to prevent too many inputs at once




//Joysticks


//Sets variables for the inputs from the joysticks
  xL = arm.JoyStickL.read_x();                                    // Uses function that reads the joystick position
  yL = arm.JoyStickL.read_y();
  xR = arm.JoyStickR.read_x();
  yR = arm.JoyStickR.read_y();
  date_processing(&xL,&yL);                                       // Function for only allowing one direction of the joystick input to be used on the left joystick
  date_processing(&xR,&yR);                                       // Function for only allowing one direction of the joystick input to be used on the right joystick
  turnUD();                                                       // Function for moving up and down based on joystick inputs
  turnLR();                                                       // Funciton for moving left and right based on joystick inputs
  turnCO();                                                       // Function for opening and closing the claw based on joystick inputs
}


// Function for only allowing one direction of the joystick input to be used on the right joystick
void date_processing(int *x,int *y){                              // It will make it so that only the x or y can be processed as an input at a time
  if(abs(512-*x)>abs(512-*y))                       
    {*y = 512;}                                                   // If x is the greater vector then y will be given a value of 512 (invalidates it later)
  else
    {*x = 512;}                                                   // If y is the greater vector then x will be given a value of 512 (invalidates it later)
}

// Arm movements based on joystick
void turnUD(void){
  if(xL!=512){                                                    // Allows this part of the code to only run if the x value is greater than the y value (value not equal to 512)
    if(0<=xL && xL<=100){arm.up(10);return;}                      // Moves the arm up and down based on the joystick inputs
    if(900<xL && xL<=1024){arm.down(10)0;return;} 
    if(100<xL && xL<=200){arm.up(20);return;}
    if(800<xL && xL<=900){arm.down(20);return;}
    if(200<xL && xL<=300){arm.up(25);return;}
    if(700<xL && xL<=800){arm.down(25);return;}
    if(300<xL && xL<=400){arm.up(30);return;}
    if(600<xL && xL<=700){arm.down(30);return;}
    if(400<xL && xL<=480){arm.up(35);return;}
    if(540<xL && xL<=600){arm.down(35);return;} 
    }
}

void turnLR(void){
  if(yL!=512){
    if(0<=yL && yL<=100){arm.right(0);return;}                    // Allows this part of the code to only run if the y value is greater than the x value (value not equal to 512)
    if(900<yL && yL<=1024){arm.left(0);return;}                   // Moves the arm left and right based on the joystick inputs
    if(100<yL && yL<=200){arm.right(5);return;}
    if(800<yL && yL<=900){arm.left(5);return;}
    if(200<yL && yL<=300){arm.right(10);return;}
    if(700<yL && yL<=800){arm.left(10);return;}
    if(300<yL && yL<=400){arm.right(15);return;}
    if(600<yL && yL<=700){arm.left(15);return;}
    if(400<yL && yL<=480){arm.right(20);return;}
    if(540<yL && yL<=600){arm.left(20);return;}
  }
}

void turnCO(void){
  if(xR!=512){
    if(0<=xR && xR<=100){arm.close(0);return;}                    // Allows this part of the code to only run if the y value is greater than the x value (value not equal to 512)
    if(900<xR && xR<=1024){arm.open(0);return;}                   // Opens and closes the claw based on the joystick inputs
    if(100<xR && xR<=200){arm.close(5);return;}
    if(800<xR && xR<=900){arm.open(5);return;}
    if(200<xR && xR<=300){arm.close(10);return;}
    if(700<xR && xR<=800){arm.open(10);return;}
    if(300<xR && xR<=400){arm.close(15);return;}
    if(600<xR && xR<=700){arm.open(15);return;}
    if(400<xR && xR<=480){arm.close(20);return;}
    if(540<xR && xR<=600){arm.open(20);return;} 
    }
}
```
</details>  


# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/PIYOtmZmPDk?si=pDYBdSPcMP7ViUBq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Description

For my second milestone, I coded servo movements, allowing me to precisely control servo positions. I also added an HC-05 Bluetooth module to send inputs from my phone to the Arduino. To do this, I made an app on MIT App Inventor with buttons coded to send number inputs to the Arduino. The Arduino then uses those inputs to send commands to the servos, moving the arm. I have 1 button to connect to my HC-05 module and 1 button to reset my servos (Figure 16). The other six main buttons are coded to various arm movements (up, down, left, right, open, close). The up and down movements are driven by both servos 2 and 3, while opening and closing the claw is driven by servo 4, and the rotating base is moved by servo 1 (Figure 17). During this milestone, I also improved my battery pack by mounting it to the base of the robotic arm, simplifying my design. Refer to (Figure 19) for the milestone 2 wiring schematic.

![share_303442952028481076235](https://github.com/user-attachments/assets/9ad0e360-f225-4ed8-b226-6398d57b69b8) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img width="425" alt="image" src="https://github.com/user-attachments/assets/2af536f3-51e4-4599-a59f-e9a53e773a9a" />


Figure 16: Bluetooth App &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Figure 17: Initializing Bluetooth/assigning buttons to number inputs
 

## How it works

Bluetooth enables low-power, wireless communication between 2 devices using radio waves within the 2.4 GHz frequency band. One device acts as the master, while the other device acts as the slave. The master device will initiate and maintain the communication with the slave device, while the slave device listens and responds to the master. In this example, my phone is the master device, and the HC-05 Bluetooth module is the slave device. 

The HC-05 Bluetooth module communicates with microcontrollers such as Arduino to recieve commands from my phone through Classic Bluetooth. It acts as a bridge between my phone and the Arduino, receiving  information as bytes, which are then sent to the Arduino. For my robot, when a button was pressed on my phone, it would send a number to the HC-05 Bluetooth module, which the Arduino then received. The Arduino then uses that input and executes the command. For example, the button that moves the arm down would send an input of 1. The Arduino will recieve this input and command the servos (Figures 2 and 3) to move to bring the arm down. 


On my project, I am using the VCC, Ground, Rx, and Tx pins on my HC-05 Bluetooth module (Figure 18). The VCC and Ground supply voltage and ground, respectively. The Rx and Tx pins stand for the receiver and transmitter pins that communicate with the Arduino's Tx and Rx pins to receive and transmit information. Using the Rx and Tx pins, the HC-05 Bluetooth module and Arduino communicate at the set baud rates of 9600 and 38400, respectively. The baud rate is the number of symbols or signal changes per second, relating to the speed of data transmission. The transmitter takes parallel data and converts it into a stream of bits, which are sent over the wire to the receiver on the other end. The receiver then converts that serial stream of bits back into parallel data. Both the HC-05 Bluetooth module and the Arduino have Rx and Tx pins, enabling continuous 2-way communication between the devices. 

![image](https://github.com/user-attachments/assets/79f1f6b2-f6e9-4ee4-bec5-ccb8482f6620)

Figure 18: HC-05 Bluetooth module


## Challenges


One of my biggest challenges was that when I pressed a button, the servo would keep moving, even when I unpressed the button. This would go on until I pressed another button. My initial solution to work around this problem was to make a button that stops all servos. However, this was not like a joystick, which I wanted to emulate with these buttons. However, I found that I can use the button touch-down and touch-up commands on the MIT App Inventor to give an input that commands the servos to stop moving when the buttons are unpressed. This allows me to have another input after a button is unpressed, allowing the arm to stop moving after unpressing the button.

While attaching my HC-05 Bluetooth module, I used a breadboard to connect all of the pins and to make a voltage divider from 5.0V to 3.3V. However, the wires often fell out, so I had to reattach them many times. However, I saw that the working voltage of the HC-05 Bluetooth module was from 3.3-6.0V, which allowed me to get rid of the voltage divider and the breadboard, making my wiring much simpler and easier to work with. 

Another challenge I had during this milestone was adding a limit to my claw movement so it could not close on itself. While this was not part of my milestone, I wanted to make this improvement to prevent my claw from breaking by continuously closing on itself. To solve this, I want to stop the claw when it goes 20 degrees by reading the angle from the servo and stopping it when it moves to a position of under 20 degrees. However, although I was able to print values for when the angle was under 20 degrees, the claw continued to move under 20 degrees. Since this was not part of this milestone, I will continue on it in the next milestone.


## Next Steps


For my next steps, I plan to add the functionality of the joysticks. This would allow me to use both my phone and the joysticks as input methods for my robotic arm. I also plan on making a different claw iteration, such as a thicker claw to pick up objects better and to decrease the chance of the claw getting stuck. I would also like to add buttons for preset positions, such as one position for picking up an object off the ground. I will also add a limit to my claw movement so that it cannot move under 20 degrees, preventing it from closing on itself. 


## Pictures


<img width="586" alt="image" src="https://github.com/user-attachments/assets/6a21205d-fbb4-4105-baa7-18da039e251b" />

Figure 19: Schematic for the wiring of the servos, joysticks, battery, and HC-05 Bluetooth module

## Second Milestone Code
<details>  
  <summary> Click to see code </summary>


```c++

//Uses the Software Serial and the Bluetooth Serial for the Bluetooth functionality
#include <SoftwareSerial.h>
SoftwareSerial Phone (2,3);

//Uses the library for the servo/arm that moves, reads, and sets the position of the servos.
#include "src/CokoinoArm.h"
CokoinoArm arm;

//Declares the inputs that are read in the Bluetooth serial
char values;

//Servo and bluetooth setup
void setup() {
  arm.ServoAttach(4,5,6,7);                   //arm of servo motor connection pins
  Serial.begin(38400);
    Phone.begin(9600);
}

//Runs repeatedly
void loop() {

//Looks for inputs in the Bluetooth serial
if (Phone.available()>0){
  values = Phone.read();                      // Reads the values from the Bluetooth serial and saves them as the variable "values" 
    Serial.print(values);
}

//Moves the arm down when input is 1
if (values == '1'){
  arm.down(45);                               //(#) is the speed of the servo movement
}

//Moves the arm up when input is 2
if (values == '2'){
  arm.up(45);
}

//Moves the rotating base to the right when input is 3
if (values == '3'){
  arm.right(10);
}

//Moves the rotating base to the left when input is 4
if (values == '4'){
  arm.left(10);
}

//Opens the claw when input is 5
if (values == '5'){
  arm.open(10);
}

//Closes the claw when input is 6
if (values == '6'){
  arm.close(10);
  }

}

//If the buttons are unpressed, the input will be 8, which makes the servos stop moving
if (values == '8'){ 
  arm.down(0);
  arm.up(0);
  arm.right(0);
  arm.left(0);
  arm.open(0);
  arm.close(0);
}

//Resets all servos
if (values == '7'){
  arm.servo1.write(90);                      //Servo set to 90 degrees
  arm.servo2.write(90);
  arm.servo3.write(90);
  arm.servo4.write(90);
}


delayMicroseconds(10);                       // Delays for 10 microseconds to prevent too many inputs at once
}
```

</details>  


# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/AHl8VPL7Uiw?si=0OXPjJc_zpjvnt9N" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Description

For my first milestone, I completed the hardware of the robotic arm. I wired the servos, joysticks, and batteries to the Arduino (Figure 23). Using code that resets my servo positions to 90 degrees, I tested my servo movements. I also tested my joysticks by checking their inputs. I soldered a 5-pack battery pack to power my robotic arm. I used zip-ties to prevent tangling while keeping my wires together and more organized (Figure 20).


![PXL_20250708_183658120](https://github.com/user-attachments/assets/a0bdf4d0-151a-401f-9dfb-f3c459c85553)

Figure 20: All of the parts of the robotic arm are wired and attached


## How it works

This servo uses a potentiometer, which calculates resistance changes based on the position to calculate the servo's current angle. This allows the arm to reset to 90 degrees precisely and only move as much as needed. Using the information from the potentiometer, a feedback loop helps maintain the commanded servo position.

Servos use electromagnets that repel a permanent magnet to rotate an axle. The polarity of the electromagnet is constantly flipped by a commutator to continuously repel the permanent magnet, allowing for continuous rotation (Figure 21). The torque of the servo is directly proportional to the current provided to the motor. This is because an increased current increases the magnetic force inside the servo motor, increasing the torque. Similarly, an increase in voltage will increase the RPM. This allows all the servos on the arm to move the arm correctly and efficiently.

![image](https://github.com/user-attachments/assets/075510f8-5338-4475-beb7-d9ceade39a69)

Figure 21: Servo schematic


Servos use 3 wires to connect to the Arduino. The red wire is for power, the brown for ground, and the yellow for signal. The signal wire receives PWM (Pulse-Width-Modulation) pulses that tell the servo what position to move to (Figure 22).


![PXL_20250708_214953169](https://github.com/user-attachments/assets/2ea48c21-509f-4eed-8951-395abc9eaf3b)

Figure 22: Close-up of the servos and wiring of the servos


Similar to servos, joysticks work using potentiometers, which allow them to track the movement of the joystick. The rotation of the joystick on the 2 axes gets calculated in the x-y plane and is given as values that are sent to the Arduino to move servos on the arm. 



## Challenges

One of my biggest challenges was that my LK Cokoino MG90S servos were not working. I found that while my Tower Pro MG90S Mini Servo for my rotating base was working, the LK Cokoinno MG90S servos did not have enough power because my batteries did not provide enough voltage. To solve this, I broke down my battery pack and used its wires along with another battery pack by soldering them together. This new battery pack has space for 5 AA batteries, allowing my robotic arm to have enough voltage for all of my servos. 
Another challenge that I had was with my servo screws. These screws are necessary to attach the servos to the arm's components, but they often got stripped, making them very difficult to attach. To solve this, I had to use pliers to gain enough torque to turn the head of the stripped screws.



## Next Steps

My next steps are to assign inputs from the joystick to move the servos to various positions instead of a preset position. This would allow me to use the joysticks to precisely control my robotic arm. After completing my movement, I will start using Bluetooth to control my robot with my phone using a Bluetooth module and a Bluetooth Serial Terminal. I also want to add buttons to my controller that bring my arm to preset positions. 



## Pictures

<img width="518" alt="image" src="https://github.com/user-attachments/assets/8a145ea6-2797-4459-b633-0523e45cb15b" />

Figure 23: Wiring schematic for the battery, joysticks, and servos connected to the Arduino


## First Milestone Code
<details>  
  <summary> Click to see code </summary>

```c++
#include<Servo.h>
Servo myservo1;  // Create a servo class
Servo myservo2;  // Create a servo class
Servo myservo3;  // Create a servo class
Servo myservo4;  // Create a servo class

void setup() {  
myservo1.attach(4);  //Set the servo control pin as D4
myservo2.attach(5);  //Set the servo control pin as D5
myservo3.attach(6);  //Set the servo control pin as D6
myservo4.attach(7);  //Set the servo control pin as D7
delay(100);          //delay 100ms 
}
/////////////////////////////////////////////////////////
void loop() {
 myservo1.write(90);  //The servo is 90 degrees
 myservo2.write(90);  //The servo is 90 degrees
 myservo3.write(90);  //The servo is 90 degrees
 myservo4.write(90);  //The servo is 90 degrees
 delay(1000);
 }
```
</details>  


# Starter Project
<iframe width="560" height="315" src="https://www.youtube.com/embed/65kjtID0ET0?si=NultT1yZJ1nP4REx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Description

I chose the retro arcade as my starter project because it allows me to play classic games like Tetris using a simple display and arcade-style buttons. The purpose of this project was to help me master soldering various components, such as a display, buttons, a power switch, and wires. To build it, I first started by soldering the various components of my project onto my board and then screwing a case to finish it off. 


## Challenges


One of the main challenges of building my retro arcade starter project was the very small spaces between the pins I needed to solder, meaning that small mistakes could ruin the whole project and would be very difficult to fix. To solve this project, I practiced with multiple pin strips to make my soldering consistent enough to prevent any mistakes. This alllowed me to have perfect solders for my whole starter project. 


## Next Steps


My next step is for me to start on my intensive project and to work towards my first milestone. This includes build the hardware of the robotic arm, learning how to code the servos, coding the servos, and assigning inputs from my joysticks to servo movements.



# Bill of Materials


| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Robotic Arm Kit | Kit for the robotic arm | $49.99 | <a href="https://www.amazon.com/LK-COKOINO-Compliment-Engineering-Technology/dp/B081FG1JQ1/ref=asc_df_B081FG1JQ1?mcid=9da4c6c9864a305ca1ea713827f50833&hvocijid=2083331172026415723-B081FG1JQ1-&hvexpln=73&tag=hyprod-20&linkCode=df0&hvadid=721245378154&hvpos=&hvnetw=g&hvrand=2083331172026415723&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032171&hvtargid=pla-2281435178138&psc=1"> Link </a> |
| HC-05 Bluetooth Module | Used for wireless connection from my phone to my robot | $10.39 | <a href="https://www.amazon.com/HiLetgo-Wireless-Bluetooth-Transceiver-Arduino/dp/B071YJG8DR"> Link </a> |
| Robot drivetrain kit | 4 DC Motors and base for movement | $41.99 | <a href="https://www.amazon.com/Robot-Smart-Chassis-Speed-Encoder/dp/B0DFH13LBJ?gQT=1"> Link </a> |
| L298N H-Bridge | Changes the direction of the motors | $7.99 | <a href="https://www.amazon.com/Qunqi-Controller-Module-Stepper-Arduino/dp/B014KMHSW6"> Link </a> |
| Jumper Wires | Wiring to connect all components | $7.49 | <a href="https://www.amazon.com/EDGELEC-Breadboard-Optional-Assorted-Multicolored/dp/B07GD25V8D/ref=sr_1_2_sspa?dib=eyJ2IjoiMSJ9.I3nSspk5onl8Jong0G-0Eej0s1agLXJoNbNWfIFXRRAEOMuK7c7b9DmCgh8gnhKUOTq503QX8IIwpA7yXyJDHyE27e6vwXn-gkjXyhuBXzIR48hGgOEkilolw7PmeiIcgFcb5S4wzl-UkVWskUiHdUZJM15E7_IyUAeFj7qvU6jCIItRL0VPqUg7yGQ-HYDXzM5vfZecJLZcH5E23KheZvLm-6vdPkEScrxE5a7py2s.dMev98kQUFQeiokRO7DejXrUzpfHPZOnVdCD1dq3x1o&dib_tag=se&keywords=jumper%2Bwires&qid=1753376220&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| AA Batteries | Powers the ArduinoNano and the DC motors  | $9.99 | <a href="https://www.amazon.com/AmazonBasics-Performance-Alkaline-Batteries-20-Pack/dp/B00NTCH52W/ref=sr_1_1_ffob_sspa?crid=AL01JPQ69B66&dib=eyJ2IjoiMSJ9.riz1Te5yzJxEwLNmR013N98XpNfPyoNQr-Y5nntdCXbUofnaZV-3fRoGR04Lf7ZJo9WTc8yhidieYeVHT8h50VN778ggLV8OPWL4FsQpHrPTFewWWiaPlnjJCkHAB-8N9f2ANPn9JptiwyYetKZtwcZV4E4P5JY2AHeaJOwumiTeKqEI2iwhfKKDMV6-cSFpTCASU7C0TLSFuuO3lJMw_mbfK0oPAieq-s4teS58VqmCRzFozFx0fnyXTRn7k0s0Z_ikgJ4j8BGY6jLS92rzgfIplbo3RkqZcddlkrpWhbM.FgD-QWWTdvzbOTWC_GHIXH-eg1QxLJ-B3X07TQ-vVVs&dib_tag=se&keywords=AA%2Bbatteries&qid=1753376321&rdc=1&sprefix=aa%2Bbatterie%2Caps%2C198&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| 5 AA Battery Holder | Holds the batteries to power the Arduino Nano and the DC motors | $7.99 | <a href="https://www.amazon.com/LampVPath-Battery-Holder-Leads-Wires/dp/B07WRQ44YK/ref=sr_1_1_sspa?dib=eyJ2IjoiMSJ9.iDeEIOEvnhCRTxPFr0HPSnakx6TL2rJdtwGNw7cbQ4sSNdC897I45ym8K0nc5YI5Ju937vYRCKzfxKJ-ywWb_0Hbi6-Ii1RF5cntou400kI5ifU-HD0bbijz7cxLbCAcf4AI4mwPMaTH1krZc2GifdBa-yaenE4WmQHTjPYz0knli_x3VIxzJr3MKcuB4Hix61Dct6aRhjpuyF_p9aZ33OT3hqr9SqUjP_JbHzWkonI.uAezwsj6ZPHZln4e_J2GG7xfZGBb8cMgzXCCYrO0XoY&dib_tag=se&keywords=5+AA+battery+holder&qid=1752183577&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |
| Small Breadboard | Parallel connection from the Arduino Nano's 5V pin to the HC-05 and H-Bridge | $6.66 | <a href="https://www.amazon.com/Breadborad-Solderless-Breadboards-Distribution-Connecting/dp/B082VYXDF1/ref=sr_1_2_sspa?crid=18E20Y0ZZ3Z7H&dib=eyJ2IjoiMSJ9.EQvCK09g_r0CejNbKABqFY0gRfQNtZKfRgXvRy06gRhEz3g_IRgyi5UMa6jSz15PY3AGFV-DUMzOvXD_04TpwcXX3wtZS80XtkMSoirtn_8pi5lyxFMDEprXfzO2dEOVneQesvDPJddYI19W_WC0xI1HZcfGolCZZXfJNeezNSzPUk2oRUocbM1zHSYcVX5G325VYDCBLZhkZV2jDa2XmaFh5iNhNJmXsk6e6klCj_g.AoN-P0h_wrmNtrgk_pEwe-AMbFcwHC0clqn5bO2pYMo&dib_tag=se&keywords=breadboard+small&qid=1753377542&sprefix=breadboard+smal%2Caps%2C136&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |














