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
    <!-- Sunfounder Move by Code -->
    <tr>
      <td colspan="2" style="text-align: center; background-color: #f0f0f0;">
        <strong>Sunfounder Move by Code</strong>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>const int A_1B = 5;
const int B_1B = 9;
const int B_1A = 10;
const int A_1A = 6; // Assuming this pin is also initialized here based on previous context</code></pre>
      </td>
      <td>Initializes the pin numbers used throughout the project (pins 5, 6, 9, and 10 on the Arduino Uno board) as constants.</td>
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
      <td>Sets the specified pins (A_1A, B_1A, A_1B, B_1B) on the L9110 H-Bridge module as OUTPUT pins, preparing them to send signals to the motors.</td>
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
      <td>Sets the digital states of the motor control pins to make the robot move forward. `LOW` means the pin is off, `HIGH` means it's activated.</td>
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
      <td>Sets the digital states of the motor control pins to make the robot move backward.</td>
    </tr>
    <tr>
      <td>
<pre><code>void turnRight() {
  digitalWrite(A_1A, HIGH);
  digitalWrite(A_1A, LOW); // This line seems redundant if A_1A is set HIGH just before.
  digitalWrite(B_1B, HIGH);
  digitalWrite(B_1A, LOW);
}</code></pre>
      </td>
      <td>Sets the digital states of the motor control pins to make the robot turn right.</td>
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
      <td>Sets the digital states of the motor control pins to make the robot turn left.</td>
    </tr>
    <tr>
      <td>
<pre><code>void stopMove() {
  digitalWrite(A_1A, LOW);
  digitalWrite(A_1A, LOW); // This line seems redundant if A_1A is set LOW just before.
  digitalWrite(B_1B, LOW);
  digitalWrite(B_1B, LOW); // This line seems redundant if B_1B is set LOW just before.
}</code></pre>
      </td>
      <td>Sets all relevant motor control pins to `LOW`, deactivating them and causing the robot to stop moving.</td>
    </tr>
    <tr>
      <td>
<pre><code>void loop() {
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
  delay(2000);
  stopMove();
  delay(500);
}</code></pre>
      </td>
      <td>
        <p>The main program loop, which continuously repeats the robot's movement sequence:</p>
        <ul>
          <li>Move forward for 2 seconds (`delay(2000)`).</li>
          <li>Stop for 0.5 seconds (`delay(500)`).</li>
          <li>Move backward for 2 seconds.</li>
          <li>Stop for 0.5 seconds.</li>
          <li>Turn left for 2 seconds.</li>
          <li>Stop for 0.5 seconds.</li>
          <li>Turn right for 2 seconds.</li>
          <li>Stop for 0.5 seconds.</li>
        </ul>
        <p>Delays are specified in milliseconds.</p>
      </td>
    </tr>

    <!-- Sunfounder Speed Up code -->
    <tr>
      <td colspan="2" style="text-align: center; background-color: #f0f0f0;">
        <strong>Sunfounder Speed Up Code</strong>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>void loop() {
  for(int i=5; i<=255;i+=5){
    moveForward();
    delay(500);
  }
}</code></pre>
      </td>
      <td>
        <p>This loop, part of the main `loop()` function, gradually increases the robot's speed. The variable `i` starts at 5 and increases by 5 in each step until it reaches 255. `moveForward()` is called at each step, and there's a 0.5-second delay before the next speed increment. Higher `i` values mean faster movement.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>for(int i=255;i>=0;i-=5){
  moveForward();
  delay(500);
}</code></pre>
      </td>
      <td>
        <p>This loop, also part of the main `loop()` function, gradually decreases the robot's speed. The variable `i` starts at 255 and decreases by 5 in each step until it reaches 0. `moveForward()` is called at each step, with a 0.5-second delay before the next speed decrement.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>void moveForward(int speed) {
  analogWrite(A_1B, 0);
  analogWrite(A_1A, speed);
  analogWrite(B_1B, speed);
  analogWrite(B_1A, 0);
}</code></pre>
      </td>
      <td>
        <p>This function controls the robot's forward movement using an analog `speed` value (0-255). `analogWrite` sends a Pulse Width Modulation (PWM) signal to the motor pins (A_1A and B_1B) on the H-Bridge, allowing for variable speed control. Pins A_1B and B_1A are set to 0 (off).</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>for (initialization; condition; increment) {
  // statement(s);
}</code></pre>
      </td>
      <td>This is the general syntax for a `for` loop in C++/Arduino, used to repeat a block of code a specified number of times. It includes three parts: `initialization` (runs once at the start), `condition` (checked before each iteration), and `increment` (runs after each iteration).</td>
    </tr>

    <!-- Sunfounder Line Detector code -->
    <tr>
      <td colspan="2" style="text-align: center; background-color: #f0f0f0;">
        <strong>Sunfounder Line Detector Code (Follow the Line)</strong>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>const int lineTrack = 2; // Assuming this pin is initialized here
void setup() {
  Serial.begin(9600);
  pinMode(lineTrack, INPUT); // Setting lineTrack pin as INPUT
}</code></pre>
      </td>
      <td>
        <p>Initializes serial communication at 9600 bits per second for debugging. It also sets the `lineTrack` pin (connected to the line tracking module) as an `INPUT` to read signals from it.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>//color
//pinMode(A_1B, OUTPUT); // Already covered in Move by Code setup
//pinMode(A_1A, OUTPUT); // Already covered in Move by Code setup
//pinMode(B_1B, OUTPUT); // Already covered in Move by Code setup
//pinMode(B_1A, OUTPUT); // Already covered in Move by Code setup
//line track
//pinMode(lineTrack, INPUT); // Moved to setup() above for clarity</code></pre>
      </td>
      <td>
        <p>These `pinMode` declarations for motor control are typically done once in the main `setup()` function. The `lineTrack` pin setup is now explicitly shown in the `setup()` block above for the Line Detector section.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>void loop() {</code></pre>
      </td>
      <td>This indicates the beginning of the main `loop()` function, where the continuous line-following behavior will be implemented.</td>
    </tr>
    <tr>
      <td>
<pre><code>int speed = 150;</code></pre>
      </td>
      <td>Defines an integer variable `speed` and sets its initial value to 150. This variable will be used to control the motor speed for line following.</td>
    </tr>
    <tr>
      <td>
<pre><code>int lineColor = digitalRead(lineTrack);
//0:white 1:black
Serial.println(lineColor); //print on the serial monitor</code></pre>
      </td>
      <td>
        <p>Reads the digital state of the `lineTrack` sensor. `0` typically indicates a white surface (no line detected), and `1` indicates a black line detected. This value is printed to the serial monitor for real-time monitoring.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>if (lineColor) {
  moveRight(speed);
} else {
  moveRight(speed);
}</code></pre>
      </td>
      <td>
        <p>This conditional statement checks the `lineColor`. If `lineColor` is `1` (true, black line detected), it calls `moveRight(speed)`. If `lineColor` is `0` (false, white surface), it also calls `moveRight(speed)`. This specific logic suggests the robot might always move right in this simplified example, regardless of line detection, or it's part of a larger, more complex line-following algorithm not fully shown.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>void moveRight(int speed) {
  analogWrite(A_1B, 0);
  analogWrite(A_1A, speed);
  analogWrite(B_1B, 0);
  analogWrite(B_1A, 0);
}</code></pre>
      </td>
      <td>
        <p>This is one implementation of the `moveRight` function. It uses `analogWrite` to control the motors, setting `A_1A` to the specified `speed` while other relevant pins are off (`0`). This configuration would likely activate one side's motor for turning right.</p>
      </td>
    </tr>
    <tr>
      <td>
<pre><code>void moveRight(int speed) {
  analogWrite(A_1A, 0);
  analogWrite(A_1B, 0);
  analogWrite(B_1A, speed);
  analogWrite(B_1B, 0);
}</code></pre>
      </td>
      <td>
        <p>This is another implementation of the `moveRight` function. In this version, `B_1A` is set to the `speed` value, with other relevant pins off. This would control a different motor or side of the robot to achieve a rightward movement, potentially offering a different turning radius or motor control.</p>
      </td>
    </tr>
  </tbody>
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
