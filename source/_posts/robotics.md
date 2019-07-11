---
title: Robotics
categories:
  - trivia
toc: true
date: 2015-10-19 15:46:34
tags:
  - science
---

[Documentation - ROS Wiki](http://wiki.ros.org/)

[Robots4Us Student Contest | DRC Finals](http://www.theroboticschallenge.org/Robots4Us)
[The Robots4Us Challenge - TechStuff (podcast)](https://player.fm/series/techstuff/the-robots4us-challenge)
[A Compilation of Robots Falling Down at the DARPA Robotics Challenge - YouTube](https://www.youtube.com/watch?v=g0TaYhjpOfo)

[VEX IQ Super Kit - Do you want to build a robot? - YouTube](https://www.youtube.com/watch?v=sohekAXc8UY)

[Robot Quickstart! - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/robot-quickstart) TB6612FNG

[The Complete History And Future of Robots | WIRED](https://www.wired.com/story/wired-guide-to-robots/)
[How I Became a Robot in London—From 5,000 Miles Away | WIRED](https://www.wired.com/story/how-i-became-a-robot-in-london/)

[How to Control a Servo Motor From a Webpage | Arduino | Maker Pro](https://maker.pro/arduino/tutorial/how-to-control-a-servo-motor-from-a-webpage)
[Raspberry PI L298N Dual H Bridge DC Motor: 5 Steps](https://www.instructables.com/id/Raspberry-PI-L298N-Dual-H-Bridge-DC-Motor/)
[Arduino Robot - Motor Control - DarkBlueBit.com](https://darkbluebit.com/arduino/robot-motor-control/)

[PythonRobotics | Python sample codes for robotics algorithms.](https://atsushisakai.github.io/PythonRobotics/)
[AtsushiSakai/PythonRobotics: Python sample codes for robotics algorithms.](https://github.com/AtsushiSakai/PythonRobotics)

[ESP32 LED PWM Controller Example and Sample Code](http://iot-bits.com/esp32/esp32-led-pwm-controller-example-sample-code/)
[ESP32 with DC Motor - Control Speed and Direction | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-dc-motor-l298n-motor-driver-control-speed-direction/)
[How to Control a Servo Motor From a Webpage With the ESP32 | Everything ESP | Maker Pro](https://maker.pro/everything-esp/tutorial/how-to-control-a-servo-motor-from-a-webpage-with-the-esp32)

[Arduino and Servos: How to Make a Laser Turret with XOD - YouTube](https://www.youtube.com/watch?v=iH9_xtulyws)

## Robotic Hands/Arms

[A Clever and Simple Robot Hand | WIRED](https://www.wired.com/story/a-clever-and-simple-robot-hand/) SoftHand 2 has only 2 motors

[This Robot Hand Taught Itself How to Grab Stuff Like a Human | WIRED](https://www.wired.com/story/this-robot-hand-taught-itself-how-to-grab-stuff-like-a-human/) reinforcement learning in virtual world, lots of parameter randomization

[This One-Armed Robot Is Super Manipulative (in a Good Way) | WIRED](https://www.wired.com/story/this-one-armed-robot-is-super-manipulative-in-a-good-way/) deformable finger, soft robotics

## Bio-inspired Robots

[This Supple, Squishy Robo-Jellyfish Can Explore Ocean Reefs | WIRED](https://www.wired.com/story/supple-squishy-robot-jellyfish-can-explore-ocean-reefs/) soft robotics

[C-Turtle](https://sites.google.com/view/c-turtle/)

## Soft robotics

[Giada Gerboni: The incredible potential of flexible, soft robots | TED Talk](https://www.ted.com/talks/giada_gerboni_the_incredible_potential_of_flexible_soft_robots?language=en)

## Motor

[Electric motor - Wikiwand](http://www.wikiwand.com/en/Electric_motor) Electronic speed controllers (ESC)
[Types of Motors | Adafruit Motor Selection Guide | Adafruit Learning System](https://learn.adafruit.com/adafruit-motor-selection-guide)
[Motors and Selecting the Right One - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/motors-and-selecting-the-right-one)
[Which Motor Type is the Best Generator? || DC, BLDC or Stepper? (Experiment) - YouTube](https://www.youtube.com/watch?v=cJ_vDA7xsGs)

[The Electric Motor - Edison Tech Center](http://www.edisontechcenter.org/electricmotors.html)
[Induction Motors](http://www.edisontechcenter.org/inductionMotors.html)
[Electric Motor: Model S, Tesla Motors - YouTube](https://www.youtube.com/watch?v=NaV7V07tEMQ)
[Electric motor basics](https://www.st.com/content/ccc/resource/sales_and_marketing/presentation/application_presentation/group0/23/a1/94/a3/39/cf/4c/37/introduction_to_electric_motors_pres.pdf)
[How to make the simplest electric motor | Evil Mad Scientist Laboratories](https://www.evilmadscientist.com/2006/how-to-make-the-simplest-electric-motor/)

[Arduino Blog » This self-balancing mech is piloted by an insect](https://blog.arduino.cc/2019/06/14/this-self-balancing-mech-is-piloted-by-an-insect/)
[Augmented Arthropod - Self-Balancing Mech: 11 Steps (with Pictures)](https://www.instructables.com/id/Augmented-Arthropod-Self-Balancing-Mech/)

[Electrical Machines - YouTube](https://www.youtube.com/playlist?list=PLuUdFsbOK_8qVROrfl2M2WSV2xAz-ABVU)

### Motor Control

To drive a motor with reverse motion, a circuit with 5 transistors, so called H Bridge. The H-bridge module om market usually support 2 outputs. The logical voltage is usually 3.3V/5V.

When using PWM to drive DC motor, do a high pass (of say 8 out of 255 with 8 bit resolution) on the duty cycle as the motor does not handle low voltage well and will squeak.

> Do use a suppression diode to cross the load to protect the transistor from voltage spike.
> [How to protect circuits from reversed voltage polarity! - YouTube](https://www.youtube.com/watch?v=IrB-FPcv1Dc)

[Motor Control Simulation - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08q6N0vjurZxdOaFdbsjuQq2)

[Pololu - DRV8833 Dual Motor Driver Carrier](https://www.pololu.com/product/2130) 10V 1.5A, used by LEGO IR receiver v2
[Pololu - DRV8835 Dual Motor Driver Carrier](https://www.pololu.com/product/2135)
[Pololu - TB6612FNG Dual Motor Driver Carrier](https://www.pololu.com/product/713) 15V 1.2A
[STM L293D](https://www.st.com/content/st_com/en/products/motor-drivers/brushed-dc-motor-drivers/l293d.html) 0.6A, with diode
[STM L298](https://www.st.com/en/motor-drivers/l298.html) 12V 2A, not efficient

[LB1938](http://www.onsemi.com/pub/Collateral/ENA2041-D.PDF) 2.2-10V, 800mA

[L9110_2_CHANNEL_MOTOR_DRIVER.pdf](http://me.web2.ncut.edu.tw/ezfiles/39/1039/img/617/L9110_2_CHANNEL_MOTOR_DRIVER.pdf)
[L9110.doc](https://www.elecrow.com/download/datasheet-l9110.pdf)
[How to use the HG7881 (L9110) Dual Channel Motor Driver Module](https://www.bananarobotics.com/shop/How-to-use-the-HG7881-(L9110%29-Dual-Channel-Motor-Driver-Module)
[L9110 Motor Driver Primer](https://www.electroschematics.com/13797/l9110-motor-driver-primer/)

[Adafruit Motor/Stepper/Servo Shield for Arduino v2 Kit [v2.3] ID: 1438 - \$19.95 : Adafruit Industries, Unique & fun DIY electronics and kits](https://www.adafruit.com/product/1438) TB6612
[Using the pololu tb6612fng dual motor driver with an Arduino to control two low powered DC motors - Let's Make Robots / Tutorials - RobotShop Community](https://www.robotshop.com/community/forum/t/using-the-pololu-tb6612fng-dual-motor-driver-with-an-arduino-to-control-two-low-powered-dc-motors/13158)

[Ardumoto Shield Hookup Guide - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/ardumoto-shield-hookup-guide) L298P
[Mired in RC: The Fundumoto motor shield](http://rc.mired.org/2017/09/the-fundumoto-motor-shield.html)
[Arduino Motor Shield 智能小车电机驱动板 支持 PS2 手柄无线遥控-淘宝网](https://item.taobao.com/item.htm?id=546984627565) ¥98 奇果派

- 4 DC, 4 servo
- wireless PS2 controller
- i2c interface

[ODrive](https://odriverobotics.com/)
[Overview | Adafruit Motor Shield | Adafruit Learning System](https://learn.adafruit.com/adafruit-motor-shield)
[Overview | Adafruit Motor Shield V2 for Arduino | Adafruit Learning System](https://learn.adafruit.com/adafruit-motor-shield-v2-for-arduino)

[Arduino - Servo](https://www.arduino.cc/en/Reference/Servo)
[Arduino - Stepper](https://www.arduino.cc/en/Reference/Stepper)

[Make your own ESC || BLDC Motor Driver (Part 1) - YouTube](https://www.youtube.com/watch?v=W9IHEqlGG1s)
[Make your own ESC || BLDC Motor Driver (Part 2) - YouTube](https://www.youtube.com/watch?v=NXkLydhRvS0)

### DC brushed/brushless motor

[摩打 - Wikiwand](https://www.wikiwand.com/zh-hk/电动机)
[DC motor - Wikiwand](http://www.wikiwand.com/en/DC_motor)

Deceleration Motor
[减速机\_百度百科](https://baike.baidu.com/item/减速机)
[减速电机\_百度百科](https://baike.baidu.com/item/减速电机)

[DC Motors in Drones](http://www.edisontechcenter.org/Drones.html)

[Make your own ESC || BLDC Motor Driver (Part 1) - YouTube](https://www.youtube.com/watch?v=W9IHEqlGG1s)
[Make your own ESC || BLDC Motor Driver (Part 2) - YouTube](https://www.youtube.com/watch?v=NXkLydhRvS0)

[Brushed DC Motors | AddOhms #20 - YouTube](https://www.youtube.com/watch?v=iKqruCYuc1Q)
[Brushless DC Motors (BLDCs) Introduction | AO #21 - YouTube](https://www.youtube.com/watch?v=ZqEHXEuq2rc)
[Electronic Basics #18: DC & Brushless DC Motor + ESC - YouTube](https://www.youtube.com/watch?v=UteZJ_7C4Mg)

GPIO pin does not provide enough current to drive the motor, use transistor to draw current from main input.
[DC Motor - Microbit - Google Docs](https://docs.google.com/document/d/1lPu3yNbNnEjcNbhkx-jtpx01nyoOD-lB66QQqUEqaMs/edit)
[Overview | Arduino Lesson 13. DC Motors | Adafruit Learning System](https://learn.adafruit.com/adafruit-arduino-lesson-13-dc-motors?view=all)

[ESP32 with DC Motor - Control Speed and Direction | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-dc-motor-l298n-motor-driver-control-speed-direction/) L298N, can be powered by 6V-12V, have 5V output in this mode
[All You Need to Know About L293D | Custom | Maker Pro](https://maker.pro/custom/projects/all-you-need-to-know-about-l293d)

[Arduino DC Motor Control Tutorial - L298N | H-Bridge | PWM | Robot Car - YouTube](https://www.youtube.com/watch?v=I7IFsQ4tQU8)
[Controlling DC Motors with the L298N H Bridge and Arduino - YouTube](https://www.youtube.com/watch?v=dyjo_ggEtVU)

[Control a DC Motor with the L9110S and a Rotary Encoder – Brainy-Bits](https://www.brainy-bits.com/l9110s/)

[电机马达-卡卡模型商城-淘宝网](https://kaka-model.taobao.com/category-702173154.htm)
130, 280, 380 motor
电机规格：15 _ 20 _ 25 MM
输出轴： 2.0 MM
输出轴长度：7.5-11.0 MM

Secure rack with M4 screws

日本中速 FA-130RD

红色后盖微型 130 马达，扭矩不大
额定电压：3V
3V：16500 转 空载电流约 0.7A，堵转电流 1.3A

白色后盖
电压：3V
电流：60ma
转速：10000 转左右
电压：6V
电流：120ma
转速：18000 转左右

淡金色后盖
转速：4V 20000 转左右
转速：4V 20000 转左右

TT 减速马达
with box and gears, usually yellow or blue

N20 减速电机
small, usually naked

### Servo Motors

[Servomotor - Wikiwand](https://www.wikiwand.com/en/Servomotor)
[伺服馬達 - Wikiwand](https://www.wikiwand.com/zh-hk/伺服馬達)
[How Servo Motors Work | Servo Motor Controllers](https://www.jameco.com/jameco/workshop/howitworks/how-servo-motors-work.html)
[Technical animation: How a servo motor works - YouTube](https://www.youtube.com/watch?v=hg3TIFIxWCo&vl=en)
[How RC Servos Works](http://pcbheaven.com/wikipages/How_RC_Servos_Works/)
[Electronic Basics #25: Servos and how to use them - YouTube](https://www.youtube.com/watch?v=J8atdmEqZsc)
PWM freq: 50Hz (period: 20ms)
Duty cycle: 5-10% (1-2ms)
1ms: -90°; 1.5ms: 0°; 2ms: 90°

### Stepper motor

[Stepper motor - Wikiwand](https://www.wikiwand.com/en/Stepper_motor)
[步進馬達 - Wikiwand](https://www.wikiwand.com/zh-hk/步進馬達)

[What is a Stepper Motor? | All About Stepper Motors | Adafruit Learning System](https://learn.adafruit.com/all-about-stepper-motors?view=all)
[Arduino Stepper Motor Driver](https://www.electroschematics.com/12353/arduino-stepper-motor-driver/)

[Electronic Basics #24: Stepper Motors and how to use them - YouTube](https://www.youtube.com/watch?v=bkqoKWP4Oy4)
[Stepper Motors with Arduino - Controlling Bipolar & Unipolar stepper motors - YouTube](https://www.youtube.com/watch?v=0qwrnUeSpYQ)
[04-步進馬達 - 阿玉 maker 研究區](https://sites.google.com/site/wenyumaker/04-bu-jin-ma-da)

[Electronic Miter box! Control a Stepper Motor with a Keypad – Brainy-Bits](https://www.brainy-bits.com/diy-stepper-miter-box/)
[Control a Stepper motor using an Arduino and Potentiometer – Brainy-Bits](https://www.brainy-bits.com/control-a-stepper-motor-using-a-potentiometer/)
[Arduino NEMA stepper control with Joystick and Limit Switches – Brainy-Bits](https://www.brainy-bits.com/stepper-motor-with-joystick-and-limit-switches/)
[Control a Stepper Motor with an Arduino and IR Remote – Brainy-Bits](https://www.brainy-bits.com/control-stepper-motor-with-arduino/)

[Control a Stepper Motor using an Arduino and a Rotary Encoder – Brainy-Bits](https://www.brainy-bits.com/stepper-motor-rotary-encoder-p1/)
[NEMA Stepper Motor control with Arduino and Rotary Encoder – Brainy-Bits](https://www.brainy-bits.com/nema-motor-with-rotary-encoder-part-2/)
[NEMA Stepper speed control with Arduino and Easy Driver – Brainy-Bits](https://www.brainy-bits.com/nema-motor-with-rotary-encoder-part-3/)
[Set IN and OUT Stepper travel points using tact switches – Brainy-Bits](https://www.brainy-bits.com/nema-motor-with-rotary-encoder-part-4/)

### Rotary Encoders

[A simple method to measure rotation speed](http://www.whatimade.today/counting-speed-of-rotation-with-an-arduino-an-led-and-an-ldr-light-dependent-resistor/)

[Adventures in Science: How to Use Rotary Encoders - YouTube](https://www.youtube.com/watch?v=oLBYHbLO8W0)
[HACKED!: Using an HDD Motor as a Rotary Encoder?! - YouTube](https://www.youtube.com/watch?v=tjCJ3MlFt7g)

## Control Systems

[Understanding Control Systems - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08q8CE0pbZ-cSrMm_WYJfVGd)
[Control Systems in Practice - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08pFBqgd_6Bi7msgkWFKL33b)
[Understanding Model Predictive Control - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08ozoeoXgxPSBKLyd4YEHww8)

[Power Conversion Control - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08oXmudIFr2KDVzeCn2fMbl8)

### PID Control

Proportional, Derivative, Integral

[PID controller - Wikiwand](https://www.wikiwand.com/en/PID_controller)
[Understanding PID Control - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08pQBgjxYFXSsODEF3Jqmm-y)
[PID Tutorials for Line Following | RobotShop Community](https://www.robotshop.com/community/blog/show/pid-tutorials-for-line-following)

[Arduino Playground - PIDLibrary](https://playground.arduino.cc/Code/PIDLibrary/)
[Arduino Playground - PIDAutotuneLibrary](https://playground.arduino.cc/Code/PIDAutotuneLibrary/)
[PID « Project Blog](http://brettbeauregard.com/blog/category/pid/)

[Line Follower Robot - PID Control - Android Setup: 12 Steps (with Pictures)](https://www.instructables.com/id/Line-Follower-Robot-PID-Control-Android-Setup/#step8)
[PID Tutorials for Line Following - Let's Make Robots / Tutorials - RobotShop Community](https://www.robotshop.com/community/forum/t/pid-tutorials-for-line-following/13164)

[How to program hand following mBot with XOD PID-controller](https://medium.com/xodlang/how-to-program-mbot-with-xod-pid-controller-c3e310f8eceb)
[XOD powered line follower mBot – XODlang – Medium](https://medium.com/xodlang/xod-powered-line-follower-mbot-2ae4a4862a9e)

[PID Line Follower for EV3 - The Ultimate Line Follower! - YouTube](https://www.youtube.com/watch?v=AMBWV_HGYj4)
[What is the Best EV3 Line Follower For You? - YouTube](https://www.youtube.com/watch?v=P50CE0xwhvo)

- boolean/zigzag
- two sensor
- proportional
- two sensor proportional
- PID

### Kalman Filter

[Kalman filter - Wikiwand](https://www.wikiwand.com/en/Kalman_filter)
[Understanding Kalman Filters - YouTube](https://www.youtube.com/playlist?list=PLn8PRpmsu08pzi6EMiYnR-076Mh-q3tWr)

## Mecanum wheel/Omni wheel

[Mecanum wheel - Wikiwand](https://www.wikiwand.com/en/Meclanum_wheel)
[Omni wheel - Wikiwand](https://www.wikiwand.com/en/Omni_wheel)

[麥克納姆輪全向移動原理 - IT 閱讀](https://www.itread01.com/content/1549544428.html)
[机器人中的全向轮是什么 - 知乎](https://zhuanlan.zhihu.com/p/20892139)

X O
AB BA
BA AB

[【萝卜君 025】全方位移动神器 麦克纳姆轮 - YouTube](https://www.youtube.com/watch?v=sZlCp41VRao)
