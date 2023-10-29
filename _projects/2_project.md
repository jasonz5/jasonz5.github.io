---
layout: page
title: ROBOCON Competition
description: 2021 The 20th CURC ROBOCON Robot Competition
img: assets/img/projects/robocon/logo.jpg
importance: 1
category: SUSTech
---

## ROBOCON and ARES

In my second year at SUSTech, I joined ARES, the SUSTech Robotics team that participates in ROBOCON. ROBOCON is a well-known robotics competition in China and is known for its highly competitive environment and comprehensive engineering training. Here is a brief introduction to the competition:

ROBOCON, is an annual international robotics competition that's organized by Asia-Pacific Broadcasting Union (ABU). The teams are tasked with designing and manufacturing their own robots that will compete in a game-based contest. The theme and rules of the competition change every year, promoting creativity and innovation among the participants. It provides an excellent platform for students to showcase their technical skills, creativity, and ability to work as a team.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/robocon/rules.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The rules of the 20th China University Robot Competition-ROBOCON and the engineering vehicles we build.
</div>

I joined the SUSTech robot team due to my passion for working and playing with practical robots. I participated in the 20th China University Robot Competition-ROBOCON and accumulated intensive embedded control experience, strengthening my engineering skills and problem-solving ability. This competition took me seven months with seven partners to design and manufacture two robots from scratch. One was the Throwing Robot (TR), used to shoot arrows into competitors’ pots, and another was the Defensive Robot (DR), preventing rival arrows into our pots. Without any embedded knowledge, I spent one-month self-studying C programming language and STM32 development board. Later, I was designated to direct the movement control of the TR’s chassis.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/robocon/spi.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The spi interaction between two stm32 board.
</div>

Of course, this feat didn’t go smoothly. One development board didn’t have enough Controller Area Network (CAN) ports to control all motors due to the new mechanical structure with the need for more actuators. I added an extended board as slave board with complementary CAN ports and used Serial Peripheral Interface (SPI) as inter-board communication. The set-up of SPI was off-the-shelf, but I still met one intractable problem with data loss, which only occurred when the baud rate was higher than 500 KBits/s. Although the problem could be easily avoided using a lower baud rate, I was curious about the root cause. After meticulously checking the set-up process and program, I tried to observe the output signal of master board with the oscilloscope. I found that the SPI Chip Select (CS) pin delayed about 60us during the pull-down process compared with another two data transmission pins. Meanwhile, I consulted a senior member with the oscillograph and circuit element diagram and learned how the decoupling capacitor caused the pull-down delay in the corresponding circuit. This inherent hardware problem of the board could be solved by programming to compensate for this delay, and after a series of trials, the ultimate effective transmission rate can reach 930 KBits/s. This experience deeply inspired me to keep the good habit of keep asking and thinking. Luckily, we won the merit of national 3rd prize in the final competition.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/robocon/group.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
