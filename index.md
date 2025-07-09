# Robotic Arm

<!---Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Anirudh K. | Mission San Jose High School | Mechanical Engineering | Incoming Junior |

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

<!---
# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**
<img width="620" alt="image" src="https://github.com/user-attachments/assets/7932a065-1669-4438-b0e5-6967948c5735" /> #This is my 2nd milestone schematic

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
--->
# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/PIYOtmZmPDk?si=pDYBdSPcMP7ViUBq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


**Description**

For my second milestone, I coded servo movements, allowing me to precisely control servo positions. I also added an HCO-5 Bluetooth module to send inputs from my phone to the Arduino. To do this, I made an app on MIT App Inventor with buttons coded to send number inputs to the Arduino. The Arduino then uses the inputs to send commands to the servos, moving the arm. These inputs. I have 1 button to connect to my HCO-5 module, 6 buttons for various arm movements (up, down, left, right, open, close), and 1 button to reset my servos (Figure 7). During this milestone, I improved my battery pack by mounting it to the base of the robotic arm, simplifying my design.  


**How it works**


The HCO-5 Bluetooth module communicates with microcontrollers such as Arduino to recieve commands from my phone through Classic Bluetooth. It acts as a bridge between my phone and the Arduino, receiving  information as bytes, which are then sent to the Arduino. For my robot, when a button was pressed on my phone, it would send a number to the HCO-5 Bluetooth module, which the Arduino then received. The Arduino then uses that input and executes the command. For example, the button that moves the arm down would send an input of 1. The Arduiino will recieve this input and command the servos (2 and 3) to move to bring the arm down.   

On my project, I am using the VCC, Ground, Rx, and Tx pins on my HCO-5 Bluetooth module (Figure 6). The VCC and Ground supply voltage and ground, respectively. The Rx and Tx pins communicate with the Arduino's Tx and Rx pins to receive and transmit information.


**Challenges**


One of my biggest challenges was that when I pressed a button, the servo would keep moving, even when I unpressed the button. This would go on until I pressed another button. My initial solution to work around this problem was to make a button that stops all servos. However, this was not like a joystick, which I wanted to emulate with these buttons. However, I found that I can use the button touch-down and touch-up commands on the MIT App Inventor to give an input that commands the servos to stop moving when the buttons are unpressed. This allows me to have another input after a button unpress, allowing the arm to stop moving after unpressing the button.

While attaching my HCO-5 Bluetooth module, I used a breadboard to connect all of the pins and to make a voltage divider from 5.0V to 3.3V. However, the wires often fell out, so I had to reattach them many times. However, I saw that the working voltage of the HCO-5 Bluetooth module was from 3.3-6.0V, which allowed me to get rid of the voltage divider and the breadboard, making my wiring much simpler and easier to work with. 


**Next Steps**


For my next steps, I plan to add the functionality of the joysticks. This would allow me to use both my phone and the joysticks as input methods for my robotic arm. I also plan on making a different claw iteration, such as a thicker claw to pick up objects better and to decrease the chance of the claw getting stuck. I would also like to add buttons for preset positions, such as one position for picking up an object off the ground. 


**Pictures**


<img width="586" alt="image" src="https://github.com/user-attachments/assets/6a21205d-fbb4-4105-baa7-18da039e251b" />

Figure 5: Schematic for the wiring of the servos, joysticks, battery, and HCO-5 Bluetooth module

![image](https://github.com/user-attachments/assets/79f1f6b2-f6e9-4ee4-bec5-ccb8482f6620)

Figure 6: HCO-5 Bluetooth module

![share_3034429520284810762](https://github.com/user-attachments/assets/550471cf-68ff-47b5-b955-65acf081798d)

Figure 7: Bluetooth App



# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/AHl8VPL7Uiw?si=0OXPjJc_zpjvnt9N" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


**Description**

For my first milestone, I completed the hardware of the robotic arm. I wired the servos, joysticks, and batteries to the Arduino (Figure 1). Using code that resets my servo positions to 90 degrees, I tested my servo movements. I also tested my joysticks by checking their inputs. I soldered a 5-pack battery pack to power my robotic arm. I used zip-ties to prevent tangling while keeping my wires together and more organized (Figure 2).



**How it works**

This servo uses a potentiometer, which calculates resistance changes based on the position to calculate the servo's current angle. This allows the arm to reset to 90 degrees precisely and only move as much as needed. Using the information from the potentiometer, a feedback loop helps maintain the commanded servo position.

Servos use electromagnets that repel a permanent magnet to rotate an axle. The polarity of the electromagnet is constantly flipped by a commutator to continuously repel the permanent magnet, allowing for continuous rotation (Figure 4). The torque of the servo is directly proportional to the current provided to the motor. This is because an increased current increases the magnetic force inside the servo motor, increasing the torque. Similarly, an increase in voltage will increase the RPM. This allows all the servos on the arm to move the arm correctly and efficiently.

Servos use 3 wires to connect to the Arduino. The red wire is for power, the brown for ground, and the yellow for signal. The signal wire receives PWM (Pulse-Width-Modulation) pulses that tell the servo what position to move to (Figure 3).

Similar to servos, joysticks work using potentiometers, which allow them to track the movement of the joystick. The rotation of the joystick on the 2 axes gets calculated in the x-y plane and is given as values that are sent to the Arduino to move servos on the arm. 



**Challenges**

One of my biggest challenges was that my LK Cokoino MG90S servos were not working. I found that while my Tower Pro MG90S Mini Servo for my turret base was working, the LK Cokoinno MG90S servos did not have enough power because my batteries did not provide enough voltage. To solve this, I broke down my battery pack and used its wires along with another battery pack by soldering them together. This new battery pack has space for 5 AA batteries, allowing my robotic arm to have enough voltage for all of my servos. 
Another challenge that I had was with my servo screws. These screws are necessary to attach the servos to the arm's components, but they often got stripped, making them very difficult to attach. To solve this, I had to use pliers to gain enough torque to turn the head of the stripped screws.



**Next Steps**

My next steps are to assign inputs from the joystick to move the servos to various positions instead of a preset position. This would allow me to use the joysticks to precisely control my robotic arm. After completing my movement, I will start using Bluetooth to control my robot with my phone using a Bluetooth module and a Bluetooth Serial Terminal. I also want to add buttons to my controller that bring my arm to preset positions. 



**Pictures** 

<img width="518" alt="image" src="https://github.com/user-attachments/assets/8a145ea6-2797-4459-b633-0523e45cb15b" />

Figure 1: Wiring schematic for the battery, joysticks, and servos connected to the Arduino

![PXL_20250708_183658120](https://github.com/user-attachments/assets/a0bdf4d0-151a-401f-9dfb-f3c459c85553)

Figure 2: All of the parts of the robotic arm are wired and attached

![PXL_20250708_214953169](https://github.com/user-attachments/assets/2ea48c21-509f-4eed-8951-395abc9eaf3b)

Figure 3: Close-up of the servos and wiring of the servos

![image](https://github.com/user-attachments/assets/075510f8-5338-4475-beb7-d9ceade39a69)

Figure 4: Servo schematic


# Starter Project
<iframe width="560" height="315" src="https://www.youtube.com/embed/65kjtID0ET0?si=NultT1yZJ1nP4REx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


**Description**

I chose the retro arcade as my starter project because it allows me to play classic games like Tetris using a simple display and arcade-style buttons. The purpose of this project was to help me master soldering various components, such as a display, buttons, a power switch, and wires. To build it, I first started by soldering the various components of my project on my board and then screwing a case to finish it off. 


**Challenges**


One of the main challenges of building my retro arcade starter project was the very small spaces between the pins I needed to solder, meaning that small mistakes could ruin the whole project and would be very difficult to fix. To solve this project, I practiced with multiple pin strips to make my soldering consistent enough to prevent any mistakes. This alllowed me to have perfect solders for my whole starter project. 


**Next Steps**


My next step is for me to start on my intensive project and to work towards my first milestone.
- Build the hardware of the robotic arm
- Learn how to code the servos
- Code the servos. Assign servo movements to buttons

# Appendix

# First Milestone

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

# Second Milestone
For this milestone, I added the functionality of controlling my robotic arm with my phone through an app I made on MIT App Inventor, and a Bluetooth HCO-5 module. 
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

//Moves the turret to the right when input is 3
if (values == '3'){
  arm.right(10);
}

//Moves the turret to the left when input is 4
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

<!---
# Bill of Materials


Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
-->
<!---
# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
-->
