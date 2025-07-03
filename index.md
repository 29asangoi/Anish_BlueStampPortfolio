# Human-Following Robot

What if you could have a robot that follows you around effortlessly without your control? Well, this summer that will be my task to build such a robot. Thus, this would be the general goal for the robot.
Imagine the greater possiblities of being able to use your robot as a pet, only that it only requires some battery power! I hope to update this project as well in order to expand these possiblites.


| Anish S.      | Stratford School | Computer Science | Incoming Freshman

---



![AnishS_(2).jpg](https://github.com/29asangoi/Anish_BlueStampPortfolio/blob/gh-pages/AnishS_(2).jpg?raw=true)

---

<!--
# Final Milestone

<iframe width="200" height="200" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allowfullscreen></iframe>

- What you've accomplished since your previous milestone
- Biggest challenges and triumphs
- Summary of key topics learned
- What you hope to learn next
-->

---

## Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/nu14NIBjSes?si=qb4GKF6pG0DR5GHE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/X0dyLCp5_js?si=Ynit8LUnFUbSQC8Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In this milestone, I tested the robot's movement. It first moves forward, then in all directions to form a full circle — which is critical for later code functions.

<iframe width="560" height="315" src="https://www.youtube.com/embed/_To6-qzbhQQ" frameborder="0" allowfullscreen></iframe>

In this video, the robot starts at a base speed and increases speed with a short delay between changes. It also demonstrates the opposite: starting fast and gradually slowing to a stop. The robot simulates acceleration and deceleration smoothly.

---

###  Technical Explanation: Movement by Code

The robot's movement uses C++ functions to go forward, backward, left, and right. Motor A controls left-side movement and Motor B controls the right. The H-Bridge controls current flow. To stop the robot, all H-Bridge outputs are set to `LOW`.

---

###  Technical Explanation: Speed Calibration

Using a `for` loop, the robot increases speed from 0 to 255 in increments of 5. This change is controlled using an integer variable `i`, and is important when rotating the robot to adjust turning responsiveness. 

Here is a wiring diagram for the speed calibration

<h6>Detailed Wiring Diagram for Speed Calibration - SunFounder Human Following Robot</h6>

<img src="https://raw.githubusercontent.com/29asangoi/Anish_BlueStampPortfolio/gh-pages/Screen%20Shot%202025-06-25%20at%209.05.49%20AM.png" 
     alt="SunFounder Human Following Robot Wiring Diagram" 
     width="800" 
     style="max-width:100%; height:auto; display:block; margin: 0 auto;">

---

### Technical Explanation: Line Detector

This part was the most complex. The line detector connects to:
- **Pin 2** on the Arduino Uno
- **5V and GND** on the breadboard

The detector reads `1` when it detects a black line. I used the serial monitor to verify this behavior. Movement functions are triggered depending on whether the sensor reads a line or not.

Here you can see a more visual representation of the line detector code.

<h6>Detailed Wiring Diagram for SunFounder Line Following Robot</h6>

<img src="https://docs.sunfounder.com/projects/picar-s/en/latest/_images/linefollow_2_wiring.png" 
     alt="Detailed Wiring Diagram for SunFounder Line Following Robot" 
     width="800" 
     style="max-width:100%; height:auto; display:block; margin: 0 auto;">

---

### Challenges Faced

At first, I assumed the motors weren’t working, but after testing, I discovered the issue was a logic error in the `turnRight` function. I corrected the motor wiring logic by switching values for Motor B’s control pins, which fixed directional movement.


---

## First Milestone

<div align="center">
  <iframe width="560" height="315"
    src="https://www.youtube.com/embed/zruteu_Ingk"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

###  Technical Explanation: Assembly
First, I began by attaching every component on. Some challenges with this was that one of the pieces of the motor broke off, and I thought that I had to get a new motor. This then also made me think I had to get some new wheels because one of the wheels had a piece of the motor inside.  To solve this problem, I just flipped the motor around so that it could still be used, and I was able to use two identical wheels instead. Then, I had to begin attaching some of the wires. First, I started by attaching the motor’s wires to the L9110 module. 

This would ensure that the wheels would rotate in the correct direction. Next, I attached the Ground and 5 Volt sections from the Arduino Uno board into the breadboard. This was an important step because it would ensure that the other components were connected to the Ground and the battery. Then, I took the same module the motors were attached to and attached all of the parts to the breadboard. Some of the parts were attached on one side (which was all connected to the Ground), and then some of the parts were connected to the other side, which was connected to the 5 volt connector. 

###  Technical Explanation: Debugging the Code
The next step of the process was testing and debugging the overall code. When testing it, the robot would first just start to spin around in some circles. The reason this was occurring was because the obstacle avoidance module was not secure, and it was instead spinning that module around, which caused this issue. However, even after securing this module, the robot behaved similarly. So, I then changed some of the wiring on the motors, after which I saw the right wheel moved forward, and the left wheel moved backward. So, I switched the position of the left motor’s wires. Then, after that, both wheels started moving backward. Finally, the robot started behaving as expected and I had finished moving it by code. 

###  Next Steps
Next, I hope to be able to move the robot by using Arduino code, which would use the programming language C. I also hope to be able to increase the several applications that my robot might be able to do in the future. 

---

### Wiring Schematic

Below is a visual of how different components like the batteries, Arduino, and breadboard connect.

<img src="https://raw.githubusercontent.com/29asangoi/Anish_BlueStampPortfolio/gh-pages/Screen%20Shot%202025-06-25%20at%209.05.49%20AM.png" alt="Schematic">


---

## Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/xZFvOUwT63U" frameborder="0" allowfullscreen></iframe>

For my starter project, I chose the **Weevil Eye**. It helped me learn about sensors and improve soldering skills. I initially struggled with LED leg orientation and had to restart. When I restarted, the process was a lot more simple because I understood what components were inccoled and what their specific roles were. While I have done projects that are battery powered, this project also introduced me to the idea of how to use a battery coin. For me, this was a lot more challenging because it was hard to take out the battery coin after it had been inserted. One issue that I did when I resarted is the placement of the sensor, which was not soldered in fully. The next time that I solder, I will ensure that all the components are soldered in fully without actually breaking thd compoennts.

Below is a schematic, which explains the wiring of the overall assmebly and wirings of the Weevil Eyes. 

<img src="Screen%20Shot%202025-06-23%20at%208.42.30%20AM.png" alt="Weevil Eye">

---


---
# Bill of Materials
Below I list the project materials for the project. Most of the supplies that I used are attached in the kit

<table>
  <thead>
    <tr>
      <th>Product</th>
      <th>Description</th>
      <th>Price</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3 in 1 Starter Kit for Human Following Robot</td>
      <td>This contains all the part necessary for the project</td>
      <td>$69.99</td>
      <td><a href="https://www.sunfounder.com/products/sunfounder-3-in-1-iot-smart-car-learning-ultimate-starter-kit">Link</a></td>
    </tr>
  </tbody>
</table>

---

# Code Explanantions

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arduino Project Documentation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }
        h1, h2 {
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
            margin-top: 40px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 40px; /* Increased space between tables */
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: left;
            vertical-align: top;
        }
        th {
            background-color: #e9ecef; /* Lighter header background */
            font-weight: bold;
        }
        pre {
            background-color: #f8f9fa; /* Very light gray for code blocks */
            padding: 10px;
            border-radius: 4px;
            overflow-x: auto;
            white-space: pre-wrap;
            word-wrap: break-word;
            font-family: 'Courier New', Courier, monospace;
            font-size: 0.9em; /* Slightly smaller font for code */
            color: #333;
        }
        ul {
            list-style-type: decimal; /* For numbered lists */
            margin-left: 20px;
            padding-left: 0;
        }
        ul li {
            margin-bottom: 5px;
        }
        strong {
            font-weight: bold;
            color: #2980b9; /* A blue color for emphasis */
        }
    </style>
</head>
<body>

   

    <h2>1. Arduino Code and Explanations</h2>
    <table>
        <thead>
            <tr>
                <th>Code/Functions</th>
                <th>Explanation</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><pre>const int A_1B = 5;
const int A_1A = 6;
const int B_1A = 9;
const int B_1B = 10;</pre></td>
                <td>Initializes every pin that I used throughout the project on the Arduino board through pins 5, 6, 9 and 10 and they all appear on the Arduino Uno board.</td>
            </tr>
            <tr>
                <td><pre>void setup() {
  pinMode(A_1B, OUTPUT);
  pinMode(A_1A, OUTPUT);
  pinMode(B_1A, OUTPUT);
  pinMode(B_1B, OUTPUT);
}</pre></td>
                <td>The second set explains how on the L9110 module there are pins (like A_1A, B) that act as the output for the pins. The input of all the pins are then in their respective location in the Arduino Uno board.</td>
            </tr>
            <tr>
                <td><pre>void moveForward() {
  digitalWrite(A_1A, HIGH);
  digitalWrite(A_1B, LOW);
  digitalWrite(B_1A, HIGH);
  digitalWrite(B_1B, LOW);
}</pre></td>
                <td>The "LOW" that is shown means that that section will not be activated. The "HIGH" that is shown represents an activation in the move forward code.</td>
            </tr>
            <tr>
                <td><pre>void moveBackward() {
  digitalWrite(A_1A, LOW);
  digitalWrite(A_1B, HIGH);
  digitalWrite(B_1A, LOW);
  digitalWrite(B_1B, HIGH);
}</pre></td>
                <td>For the move forward section, it means that the motor will only move a certain direction, in this case it is forward and the A_1A and the B_1B sections on the L9110 module. For the move backward section, it means that the motor will only move a certain direction, in this case it is backward and the A_1B and the B_1A sections on the L9110 module.</td>
            </tr>
            <tr>
                <td><pre>void turnRight() {
  digitalWrite(A_1A, HIGH);
  digitalWrite(A_1B, LOW);
  digitalWrite(B_1A, LOW);
  digitalWrite(B_1B, HIGH);
}</pre></td>
                <td>In this case it is backward and the A_1B and the B_1A sections on the L9110 module.</td>
            </tr>
            <tr>
                <td><pre>void turnLeft() {
  digitalWrite(A_1A, LOW);
  digitalWrite(A_1B, HIGH);
  digitalWrite(B_1A, HIGH);
  digitalWrite(B_1B, LOW);
}</pre></td>
                <td>The "LOW" that is shown means that that section will not be activated. The "HIGH" that is shown represents an activation in the move forward code. For the move right section, it means that the motor will only move a certain direction, in this case it is right and the A_1B and the B_1B sections on the L9110 module. For the move left section, it means that the motor will only move a certain direction, in this case it is left and the A_1A and the B_1A sections on the L9110 module.</td>
            </tr>
            <tr>
                <td><pre>void stopMove() {
  digitalWrite(A_1A, LOW);
  digitalWrite(A_1B, LOW);
  digitalWrite(B_1A, LOW);
  digitalWrite(B_1B, LOW);
}</pre></td>
                <td>This is the most simple piece of code and the most important. This is because its function is to set each pin to LOW, meaning that none of the pins will be activated and this will allow for the robot to stop moving. This is added at the end of the code upon completion of the movements for forward, backward, left, and right.</td>
            </tr>
            <tr>
                <td><pre>void loop() {
  moveForward();
  delay(2000);
  stopMove();
  delay(500);

  moveBackward();
  delay(2000);
  stopMove();
  delay(500);

  turnLeft();
  delay(2000);
  stopMove();
  delay(500);

  turnRight();
}</pre></td>
                <td>The robot goes forward for 2 seconds, stops for 0.5 seconds, then goes backward for 2 seconds, stops for 0.5 seconds, and repeats this cycle forever. Then, it repeats this same process, but for moving left and right. The delays are the same here. Delays are represented in milliseconds delay (2000) = 2 second delay delay (500) = 0.5 second delay The void loop must be declared in order for this process to be repeated. The move forward and the move backward must be defined in order for this to occur, and these codes are added in earlier sections.</td>
            </tr>
            <tr>
                <td><pre>delay(2000);
stopMove();
delay(500);</pre></td>
                <td>The same is required for moving left and right.</td>
            </tr>
        </tbody>
    </table>



</body>
</html>



