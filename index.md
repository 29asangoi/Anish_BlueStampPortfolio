# Human-Following Robot
What if you could have a robot that follows you around effortlessly without your control? Well, this summer that will be my task to build such a robot. Thus, this would be the general goal for the robot. 
You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```


| Anish S. | Stratford School | Computer Science | Incoming Freshman

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](AnishS.HEIC)
  
<!---# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone--->

# Second Milestone

Below is a video when I tested my robot after moving it by using the code. The robot will move forward for a bit, before moving in left, right, and backwards in order to form a complete circle. The formation of the complete circle is important for the other pieces of code, which use this motion. The robot does not move in a completely straight line, however, and there would need to be a speed calibration tool installed in order to make this work.

  <iframe width="640" height="360" 
          src="https://youtu.be/X0dyLCp5_js" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>

Below is a video when I tested my robot with the "speed up" code. For one half of the video, the robot will start at a "base speed", which is its lowest speed. Then, the robot will gradually increase speed, but as it does so, it actually waits for about 0.5 seconds before each increase in speed. This small wait period is harder to notice and makes it seem like the robot is always moving. For the other half of the video, the robot's base speed is its highest possible speed. Then, it will climb down to its lowest possible speed, and will slow down until it is not in motion at all. The delay period described earlier applies for all changes in speed of the robot. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/_To6-qzbhQQ" frameborder="0" allowfullscreen></iframe>



# First Milestone


<div align="center">
  <iframe width="560" height="315"
    src="https://www.youtube.com/embed/zruteu_Ingk"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>



When beginning working toward my first milestone, I attached every component on. Some challenges with this was that one of the pieces of the motor broke off, and I thought that I had to get a new motor. This then also made me think I had to get some new wheels because one of the wheels had a piece of the motor inside.  To solve this problem, I just flipped the motor around so that it could still be used, and I was able to use two identical wheels instead. Then, I had to begin attaching some of the wires. First, I started by attaching the motor’s wires to the L9110 module. This would ensure that the wheels would rotate in the correct direction. Next, I attached the Ground and 5 Volt sections from the Arduino Uno board into the breadboard. This was an important step because it would ensure that the other components were connected to the Ground and the battery. Then, I took the same module the motors were attached to and attached all of the parts to the breadboard. Some of the parts were attached on one side (which was all connected to the Ground), and then some of the parts were connected to the other side, which was connected to the 5 volt connector. The next step of the process was testing and debugging the overall code. When testing it, the robot would first just start to spin around in some circles. The reason this was occurring was because the obstacle avoidance module was not secure, and it was instead spinning that module around, which caused this issue. However, even after securing this module, the robot behaved similarly. So, I then changed some of the wiring on the motors, after which I saw the right wheel moved forward, and the left wheel moved backward. So, I switched the position of the left motor’s wires. Then, after that, both wheels started moving backward. Finally, the robot started behaving as expected and I had finished moving it by code. For my next milestone, I hope to be able to move the robot by using code. Specifically, I would use the Arduino app and would attach my robot to this app in order to allow it move. 

Below is a schematic which explains how the different components connect to each other when using a wire to connect such components. The component include batteries, breadboard, arduino board, and more. 

<img src="https://raw.githubusercontent.com/29asangoi/Anish_BlueStampPortfolio/gh-pages/Screen%20Shot%202025-06-25%20at%209.05.49%20AM.png" alt="Screenshot">

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Starter Project
<iframe width="560" height="315" src="https://www.youtube.com/embed/xZFvOUwT63U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


For my starter project, I chose the Weevil Eye project. This was because it would allow me to develop a deeper understanding of sensors and how they work. Additionally, this allowed me to become better at soldering because I was tasked throuhgout this project to do a lot of soldering with the different components that was required. However, I soon learned that another alternative to soldering was using a breadboard to connect the different components together. 
There were some challenges in attaching the LED components because I was not sure about the placement of the legs (both short and long). So, I had to restart the project, but I worked quickly and was able to get it to work. The sensor does not quite work consistently, but if it is dark, then it will work more consistently. 

<img src="Screen%20Shot%202025-06-23%20at%208.42.30%20AM.png" alt="Screenshot">

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

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
