---
title: history-of-computation-and-rendering-(a-guide-on-what-is-what)
date: 2025-05-29 15:53:00 +0800
categories: [Computer Science]
tags: []
author: parsa
math: true
image:
  path: assets/headers/2025-05-29-history-of-computation-and-rendering-(a-guide-on-what-is-what)y.png
  alt: Computer Science
---

so have you heard about gtk and wayland and then openGL and just getting confused about their role and what problem each of these softwares are solving ? but more profound qouestion is about rendering, how is it done? is this flow is for only os-based computation and not bare metal ? so in this article we gonna have a deep dive in this and see what is what.

so first lets see how modern embeded systems are displaying and what is going on, and then we gonna go to more complex peices of software which is implemented on operating systems and also will take a look at its history and timline too.


so first I am gonna go with cortext series M ARM embeded systems which basically are microcontrollers and can run only a very small binary made by compiling a c code and not a full fleged Operating system.
so basically 3 thins matter in any approach heavilly, first you core processor, then your protocl, last your display device.

## STM32 + LCD 1602 Display and I2C 16x2

so in this paradigme fistly there is very basic discplay which is small LCD cells 
so they have though of data pinns and by connecting 7 pins on data 

and the framework is a very small c SDK that can manage these small LCD cells and you can show alphabets and numbers and even like emojis


## STM32 + STM32 + OLED

## STM32 + LCD Display (FMC) or lcd TFT

so now we can create different stuff both the code base and the method matte, we can not get into messy appraoches, becuase these are actaully foundation and infrastructrue for others to use in their program and create user interfaces

## STM32 + ToughGFX or QT


## X86 corei7 + VGA/HDMI/Display port/ board + any convential monitor







# Sources
- https://controllerstech.com/interface-lcd-16x2-with-stm32-without-i2c/
- https://diyusthad.com/2019/06/two-ways-of-interfacing-lcd-module-with.html
