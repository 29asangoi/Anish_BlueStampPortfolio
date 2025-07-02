# Human-Following Robot

What if you could have a robot that follows you around effortlessly without your control? Well, this summer that will be my task to build such a robot. Thus, this would be the general goal for the robot.

| Anish S. | Stratford School | Computer Science | Incoming Freshman |

---

### **Project Image**

**Replace the BlueStamp logo below with an image of yourself and your completed project.**

![Headstone Image](AnishS.HEIC)

---

<!--
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allowfullscreen></iframe>

- What you've accomplished since your previous milestone
- Biggest challenges and triumphs
- Summary of key topics learned
- What you hope to learn next
-->

---

## Second Milestone

<iframe width="640" height="360" src="https://youtu.be/X0dyLCp5_js" frameborder="0" allowfullscreen></iframe>

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

<h2>Detailed Wiring Diagram for Speed Calibration - SunFounder Human Following Robot</h2>

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

h2>Detailed Wiring Diagram for SunFounder Line Following Robot</h2>

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

For this milestone, I assembled the hardware. I had challenges with a broken motor and wheel, but was able to flip the motor around to reuse it. After wiring the L9110 module and Arduino to the breadboard, the robot initially spun in circles due to an unstable obstacle avoidance module.

Eventually, by swapping motor wire positions, both wheels moved correctly and I could successfully control the robot with basic code.

---

### Wiring Schematic

Below is a visual of how different components like the batteries, Arduino, and breadboard connect.

<img src="https://raw.githubusercontent.com/29asangoi/Anish_BlueStampPortfolio/gh-pages/Screen%20Shot%202025-06-25%20at%209.05.49%20AM.png" alt="Schematic">

---
## Code Explanations 


<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>What it Means</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
<pre><code>const int A_1B = 5;
const int B_1B = 9;
const int B_1A = 10;</code></pre>
      </td>
      <td>Initializes every pin that I used throughout the duration of the project. These are pins 5, 6, 9, and 10 and they all appear on the Arduino Uno board.</td>
    </tr>
    <tr>
      <td>
<pre><code>void setup() {
  pinMode(A_1A, OUTPUT);
  pinMode(B_1A, OUTPUT);
  pinMode(A_1B, OUTPUT);
  pinMode(B_1B, OUTPUT);
}</code></pre>
      </td>
      <td>The second set explains how on the L9110 module there are the pins (like A_1B). These pins are in the output for the pins. The input of these pins are located in their respective location in the Arduino Uno board.</td>
    </tr>
    <tr>
      <td>
<pre><code>void moveForward() {
  digitalWrite(A_1A, LOW);
  digitalWrite(B_1A, HIGH);
  digitalWrite(A_1B, LOW);
  digitalWrite(B_1B, LOW);
}</code></pre>
      </td>
      <td>The "LOW" that is shown means that that section will not be activated.
The "HIGH" that is shown represents an activation in the move forward code.</td>
    </tr>
    <tr>
      <td>
        <p>...</p>
      </td>
      <td></td>
    </tr>
    <tr>
      <td>
<pre><code>const int A_1B = 5;
const int A_1A = 6;
const int B_1B = 9;
const int B_1A = 10;
const int lineTrack = 2;</code></pre>
      </td>
      <td>This is the very beginning of the code, which means that all of the pins have to be set up.
The first four lines connect the pins on the Arduino Uno board to the H-Bridge hubs, as explained earlier.
The last line works differently, but it does involve setting up all the pins. But, the basic assembly of the line following section connects the Line Tracking Module with Pin 2.</td>
    </tr>
    <tr>
      <td>
<pre><code>void setup() {
  Serial.begin(9600);
}</code></pre>
      </td>
      <td>This line involves the setup, where everything needs to be defined.
The Serial begin code allows for a smoother connection between the USB and the</td>
    </tr>
    <tr>
      <td>
<pre><code>void moveBackward() {
  digitalWrite(A_1A, HIGH);
  digitalWrite(A_1B, LOW);
  digitalWrite(B_1A, HIGH);
  digitalWrite(B_1B, LOW);
}</code></pre>
      </td>
      <td>The motor will only move a certain direction, in this case it is forward so the A_1A and the B_1A sections on the L9110 module.
For the move backward section, it means that the motor will only move a certain direction, in this case it is backward and the A_1B and the B_1A sections on the L9110 module.</td>
    </tr>
    <tr>
      <td>
<pre><code>void turnRight() {
  digitalWrite(A_1A, HIGH);
  digitalWrite(A_1A, LOW);
  digitalWrite(B_1B, HIGH);
  digitalWrite(B_1A, LOW);
}</code></pre>
      </td>
      <td>The "LOW" that is shown means that that section will not be activated
The "HIGH" that is shown represents an activation in the move forward code.
For the move right section, it means that the motor will only move a certain direction, in this case it is right and the A_1B and the B_1B sections on the L9110 module.</td>
    </tr>
    <tr>
      <td>
<pre><code>void turnLeft() {
  digitalWrite(A_1B, LOW);
  digitalWrite(A_1A, HIGH);
  digitalWrite(B_1A, HIGH);
  digitalWrite(B_1B, LOW);
}</code></pre>
      </td>
      <td>For the move left section, it means that the motor will only move a certain direction, in this case it is left and the A_1A and the B_1A sections on the L9110 module.</td>
    </tr>
    <tr>
      <td>
<pre><code>void stopMove() {
  digitalWrite(A_1A, LOW);
  digitalWrite(A_1A, LOW);
  digitalWrite(B_1B, LOW);
  digitalWrite(B_1B, LOW);
}</code></pre>
      </td>
      <td>This is the most simple piece of code and the most important. This is because in function is to set each pin to LOW, meaning that none of the pins will be activated and this will allow for the robot to stop moving.</td>
    </tr>
  </tbody>
</table>>
</table>

---

## Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/xZFvOUwT63U" frameborder="0" allowfullscreen></iframe>

For my starter project, I chose the **Weevil Eye**. It helped me learn about sensors and improve soldering skills. I initially struggled with LED leg orientation and had to restart, but eventually succeeded. The sensor is more consistent in darker environments.

<img src="Screen%20Shot%202025-06-23%20at%208.42.30%20AM.png" alt="Weevil Eye">

---



# Bill of Materials
Below I list the project materials for the project. Most of the supplies that I used are attached in the kit

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|

| 3 in 1 Starter Kit for Human Following Robot | This contains all the part necessary for the project | $69.99 | <a href="https://www.sunfounder.com/products/sunfounder-3-in-1-iot-smart-car-learning-ultimate-starter-kit"> Link </a> |



# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
