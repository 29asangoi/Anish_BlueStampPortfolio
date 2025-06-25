# Human-Following Robot
What if you could have a robot that follows you around effortlessly without your control? Well, this summer that will be my task to build such a robot. Thus, this would be the general goal for the robot. 
You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Anish S. | Stratford School | Computer Science | Incoming Freshman

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](AnishS.HEIC)
  
# Final Milestone

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
- What needs to be completed before your final milestone 

# First Milestone
<h2>📺 Demo Video</h2>

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

## Wiring Diagram: Connect R3 Board and L9110 Motor Driver Module

![Connect R3 board and L9110 module](https://docs.sunfounder.com/projects/3in1-kit-v2/en/latest/_images/1.move_2.png)


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
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Uno | This acts as the "brain" of the robot and controls all operations of the robot | $27.60 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Motor Drive Shield | Controls the electric current that goes into the robot | $Price | https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/ref=sr_1_1?crid=23XVV3LY80E13&dib=eyJ2IjoiMSJ9.MazmhFfn-DF8W5oyX_S-tNl6onbpYQvEhqFzrIDbT0Y6bz8eyqHpr8DjfILgxn8hYtaJNim490vrxGgWKcnxzJIinNjJcdqCj0KPCX9kOK_MylEiIX9Sko0o-EKZWlTZPNIVRgxy7cDFRXvi44SQUjDLCerqk1XcFrQ_KPyxhUpRELlTgSg71N3-5C5Jdcr2dn-4G3z72RCb-JqFKr9RzGk2auFitXbaLpN1cmhx8pg.PR8cvVUwg43cGT3bPA4Y60wCq_g48YaPH5Sh1F5PbTQ&dib_tag=se&keywords=arduino%2Buno&qid=1750434779&sprefix=arduino%2Buno%2Caps%2C151&sr=8-1&th=1 |
| Wheels(4x) | Important for the robot's movement | $59.98 | https://www.amazon.com/AR-PRO-2-Pack-10-Inch-Rubber-Wheels/dp/B08YJJPVMD/ref=sr_1_1_sspa?crid=LODZHK63IV29&dib=eyJ2IjoiMSJ9.aT09hb017B6etBbcTjZ5C2fZhE0bZg1UUf9mm2u-25vdvANCi3FC9mGtbhWRi_KCOCUbZjqIlYxX2HQHAxA1qfy03EIdBmXUjZTMr8hplMBycaq_ynsvYDTEFgk7WcQCItLeYRxd_9Nko1EAouJgkaddOavQVApb7Rg46pyoxW3xH-0lu5QRvnkFaoOZE2J13b1s28krV-8Q7m6JNl1_5pZGspGBwp9DqQuBVJxJkmkdt-VzHCJ5igM5U3BoMmIDUZPjYCZmrJlWHp41Pcbde1tXqJ7VnIgE_ZFXUJ96QEU.95KOSf3_LgiIV7_9bra94fjhR6qx860KXQN31OnoSz4&dib_tag=se&keywords=4x%2Brubber%2Bwheels&qid=1750435363&sprefix=4x%2Brubber%2Bwheel%2Caps%2C165&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1 |
| TT Gear Motor(4x) | Important for the rotational movement of the robot | $14.99 | https://www.amazon.com/Greartisan-Electric-Reduction-Eccentric-Diameter/dp/B072KNG6NT/ref=sr_1_1_sspa?crid=ZOX29D0MCQ7J&dib=eyJ2IjoiMSJ9.yN9DpLCB4WjyV93L1n_PCJR8fmRJMp_94-rTsK9kpzZRzkcTTssz4ZMoIPoapnf7J0PpwMUOfzEDjdX_7BF1sH20CvHL_Uh3EFCJIqPv63HZdu34y0ap-7NjZeWDIc4k59t6y8VpLDeNopwJ9baRbXNjKV7OCSRvQMDM1RzQTDTHuLAAJZK9BFBXIAWRXaOGlxPabjI2D_vttEhl4ANYSzqtHtudsWUgxIt0A_1V9yprNN4COHFPLyT4aSMENV-_jiDvKPBnw-n9Pc0KLXy0ni2yhdx9yhyPw7WRC1pQmS8.rYsV7HbnKn621x1CURhcNw-GJsGUTJUbkoM4hDBWvIM&dib_tag=se&keywords=tt+gear+motor&qid=1750435415&sprefix=tt+gear+moto%2Caps%2C153&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1|
| Servo Motor | Controls the speed of the robot | $Price | https://www.amazon.com/WWZMDiB-SG90-Control-Servos-Arduino/dp/B0BKPL2Y21/ref=sr_1_4_sspa?dib=eyJ2IjoiMSJ9.Z8zXoZs9nMkNwqQN2AI2Fkurdvj8MGFHhgFJWhnJQ_M1ztdB7TvnAheduqMUHY4VzLSUc4hBQ1rbGdg8mn5PkMFhXW0eQSbOIEbbrR2ysQbWy988hFODhMhN |
| Ultrasonic Sensor | Can detect if there is a person near it and uses distance sensors | $2.33 (for one) | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Infared Sensor (2x) | Can detect motion, temperature, and senses objects | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| 18650 Li-on Battery (2x)  | Gives the electrical current to the aprtts that needs it | $11.79 | https://www.amazon.com/CPZZ-1-5V-Battery-Rechargeable-Battery-0720-31/dp/B0CBPK51RP/ref=sr_1_1_sspa?crid=2JFUJ6NFEMZIS&dib=eyJ2IjoiMSJ9.ithtIjs74VeHyxVairm_xDIdPJ2FKrW_YWwIsK2flC2J0gOjKAWQ0dBetjb3MujsTUyB8WAuqWDMp2mMGaGL_ckvLmBg6E9J8Y8G4gjP0RkhRLWCt0mBSU7_WQWzZj0eVHDIGAkS04mHb1BnqiqLL58fsMyoC1jlyyw0C-J_8MZbcVooe2WpXMsjxxaZIbSBEJPOmrAMwMVc3UU76_SoF2_w8-bqTq7cCk5mZsQREc_B_YU1AdLPAFNT1TllzM58G8DgDFKld6y6nPs2eiTHnJoS15t2x0iywDAeLlulhbQ.bJRx-5fvJnG6X7vLaxK4dUf3zpXayKfezp4gtZNyL8Q&dib_tag=se&keywords=18650%2BLi-on%2BBattery%2B(2x)&qid=1750435570&sprefix=18650%2Bli-on%2Bbattery%2B2x%2B%2Caps%2C176&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1 |
| 18650 Battery Holder  | Important for securing the battery | $2.995 (for one) | https://www.amazon.com/LBTODH-Battery-Holder-Storage-Plastic/dp/B092TGQ7PB/ref=sr_1_4?crid=13U8MEQPB3XUB&dib=eyJ2IjoiMSJ9.M6UhWkizRKPmN4Pp70rPkai5ZErEpKHNSeWDJGGouQvO0hAmAKT8V0PBSKNP1Vs-VqaKYUFVhlNTtorzP-hAWUffSkFDRletRBLhvifRgshjV85tCA2xtx1sgzsavAj6cFEpLgF2ZqMuIXOr1Hxg-HQwa29F66yYlY_P5UfHpSRXeGWFfvS4fm7m_UZdap43Zs59yiRd4jZ052YmY-D9kgOp_F5Pd8aluctpzw-nPIU.TeWed0OyPQNtpncWJ-JTivgUVH4qsxWTbgHUoydCFEs&dib_tag=se&keywords=18650+Battery+Holder+1+pack&qid=1750435622&sprefix=18650+battery+holder+1+pack%2Caps%2C154&sr=8-4> |
| Male and Female Jumper wire | Can connect the different holes of the breadboard through electrical current | $3.99 | https://www.amazon.com/California-JOS-Breadboard-Optional-Multicolored/dp/B0BRTHR2RL/ref=sr_1_2?crid=12HDY8COKXU7G&dib=eyJ2IjoiMSJ9.QGbaFF62mgZ1Tf0J7CajkBnivKMOTOpZJUS1O07RvMRENtZVJaMJRebisvoGuONAUbMs4isV3OfmSypDrsemEs6cNRBuQtGINiH6Cov_SZV7HWAa9gcVoDnt8Qi10xl2DZmlKvN3pihDVKyTAwRpmDOA2SVccHwtgbfBWR8CHMIz2E2jgKtDaydoH-vg04ZvVYZkSEPuxa4Pi0h43TTyCCUqPOIyxR4UNFt2T9EhRb0.oUYzEh7imYQWSU9IqG_b9zYbz4iKmTC31SdtSn6x_YQ&dib_tag=se&keywords=male+and+female+jumper+wires&qid=1750435690&sprefix=male+and+female+jumper+wire%2Caps%2C171&sr=8-2|
| DC Motor | Important for the movement of the robot| $4.50 | https://www.amazon.com/MELIFE-Motor-Gearbox-200RPM-Arduino/dp/B096ZZHJW9/ref=sr_1_2_sspa?crid=1F0AAO9104AWG&dib=eyJ2IjoiMSJ9.dLwDHynjItuTGgGIKFMBAlIU7xXmOYDFzqRgQxKR9rUSsGx778rP3casDsBLFsO3uGFxcUcYlT0Pk4seuUs0EOehcXBTo9SmHPmZgJkSKOwSdsFMbOCG28M91HcUKM9aOeJpXEXXjr5rqQqPiVTZ2z3n0k2ocTAQy9vjZZG_pvNUk1SgAxepBUSVwiFibq4_3lUNDD1K9jZgZ1FCHqKQBENh71G8d86YfUIIOfrCLUhZTMocB5XQqPwWxhMebaXXpNhgM8U7-DffnmFzHsvW40eF7NuTkMo7YukVr9WYx8E.iUyFw2SVBWHrN-4aYlxxYcOfX39ocfVYIOQRAe_lECE&dib_tag=se&keywords=DC+5V+TT+motors+2+pack+for+robotics%22+or+%22DC+5V+geared+motors+2+pack&qid=1750435848&sprefix=dc+5v+tt+motors+2+pack+for+robotics+or+dc+5v+geared+motors+2+pack%2Caps%2C193&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1 |
| Breadboard | Important for the connection of wires without soldering| $2.33 each | https://www.amazon.com/ELEGOO-Breadboard-Solderless-Breadboards-Electronics/dp/B0CXF1B6GB/ref=sr_1_1?dib=eyJ2IjoiMSJ9.I97R4jYNHrG8QkfjAbfHenxXhtfgMK0AP7ANAmSG9evSP9skjmtIUZKxtD5_g84siMcvhyjaNP9-rGswComPUSSufGx0vektoD591Ljl21tbITqO0M4d5WpS6ulvMwJwfNV7WvPaL82nHS2VIk17mC5C3pi2HeaQ57JjTDuwLsLRuiL89pRY1BwdJnDxzxluSR3_oW2j6YHElcVQXoz0wmW_rmNbh_e_uGm1IaRRASk.zo0hag_AHNlUOMVIVbu4rdaIXExqOmYuAbQgEYZmx_U&dib_tag=se&keywords=arduino+breadboard&qid=1750435971&sr=8-1|
# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
