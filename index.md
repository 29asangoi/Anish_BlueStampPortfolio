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

---

### 🧠 Technical Explanation: Line Detector

This part was the most complex. The line detector connects to:
- **Pin 2** on the Arduino Uno
- **5V and GND** on the breadboard

The detector reads `1` when it detects a black line. I used the serial monitor to verify this behavior. Movement functions are triggered depending on whether the sensor reads a line or not.

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


---

## Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/xZFvOUwT63U" frameborder="0" allowfullscreen></iframe>

For my starter project, I chose the **Weevil Eye**. It helped me learn about sensors and improve soldering skills. I initially struggled with LED leg orientation and had to restart, but eventually succeeded. The sensor is more consistent in darker environments.

<img src="Screen%20Shot%202025-06-23%20at%208.42.30%20AM.png" alt="Weevil Eye">

---

## 💻 Code Explanation Charts
<h2>Code Explanation Table</h2>

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; width: 100%;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th style="text-align: left;">Code</th>
      <th style="text-align: left;">What It Means</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        const int A_1B = 5;<br>
        const int A_1A = 6;<br>
        const int B_1B = 9;<br>
        const int B_1A = 10;<br><br>
        const int lineTrack = 2;
      </td>
      <td>
        These lines define constants that map Arduino digital pins to motor and sensor connections.<br>
        The first four lines are outputs to the H-Bridge motor driver.<br>
        The last line assigns pin 2 to the line tracking sensor input.
      </td>
    </tr>

    <tr>
      <td>
        void setup() {<br>
        &nbsp;&nbsp;Serial.begin(9600);
      </td>
      <td>
        The <code>setup()</code> function runs once at the start.<br>
        <code>Serial.begin(9600)</code> enables serial communication for debugging at 9600 baud.
      </td>
    </tr>

    <tr>
      <td>
        pinMode(A_1B, OUTPUT);<br>
        pinMode(A_1A, OUTPUT);<br>
        pinMode(B_1B, OUTPUT);<br>
        pinMode(B_1A, OUTPUT);<br>
        pinMode(lineTrack, INPUT);
      </td>
      <td>
        These lines define each pin’s mode:<br>
        Motor control pins are set as <code>OUTPUT</code> to send signals.<br>
        The line sensor pin is set as <code>INPUT</code> to receive data.
      </td>
    </tr>

    <tr>
      <td>
        void loop() {<br>
        &nbsp;&nbsp;int speed = 150;
      </td>
      <td>
        The <code>loop()</code> function runs repeatedly.<br>
        <code>speed = 150</code> sets the robot's motor speed (range: 0–255).
      </td>
    </tr>

    <tr>
      <td>
        int lineColor = digitalRead(lineTrack);<br>
        Serial.println(lineColor);
      </td>
      <td>
        Reads the sensor value from <code>lineTrack</code>:<br>
        <code>0</code> = white (no line detected),<br>
        <code>1</code> = black (line detected).<br>
        Prints result to Serial Monitor for debugging.
      </td>
    </tr>

    <tr>
      <td>
        if (lineColor) {<br>
        &nbsp;&nbsp;moveLeft(speed);<br>
        } else {<br>
        &nbsp;&nbsp;moveRight(speed);<br>
        }
      </td>
      <td>
        If a line is detected (<code>lineColor == 1</code>), the robot moves left.<br>
        Otherwise, it moves right.
      </td>
    </tr>

    <tr>
      <td>
        void moveLeft(int speed) {<br>
        &nbsp;&nbsp;analogWrite(A_1B, 0);<br>
        &nbsp;&nbsp;analogWrite(A_1A, speed);<br>
        &nbsp;&nbsp;analogWrite(B_1B, 0);<br>
        &nbsp;&nbsp;analogWrite(B_1A, 0);<br>
        }
      </td>
      <td>
        Moves the robot left by activating Motor A forward and keeping Motor B off.
      </td>
    </tr>

    <tr>
      <td>
        void moveRight(int speed) {<br>
        &nbsp;&nbsp;analogWrite(A_1B, 0);<br>
        &nbsp;&nbsp;analogWrite(A_1A, 0);<br>
        &nbsp;&nbsp;analogWrite(B_1B, speed);<br>
        &nbsp;&nbsp;analogWrite(B_1A, 0);<br>
        }
      </td>
      <td>
        Moves the robot right by activating Motor B forward and keeping Motor A off.
      </td>
    </tr>
  </tbody>
</table>



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
