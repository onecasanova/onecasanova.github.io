---
layout: post
title: "Unattended Laster Therapy Automation"
date: 2025-04-17 -0500
permalink: /projects/Unattended_Laser_Therapy
categories: projects
---

<!-- inputing an image-->
<!-- with centering of image -->
<figure style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/Unattended/screenshot_lab.jpg" alt="Image" width="650" style="display: block; margin: 0 auto;">
    <figcaption style="font-style: italic; color: #aaa;">Prototype of unattended laser therapy concept.</figcaption>
</figure>


## What
This was my senior design project at University of Delaware. At the time of doing this project, Envois Recovery Sciences’ laser therapy device required a practitioner to move a handpiece with the laser light at a proper speed based on haptic feedback. To expand the availability of this non-invasive, drug-free therapy while mitigating the time costs experienced by healthcare providers, our sponsor had requested the development of an unattended device that can deliver a controlled dosage of the laser therapy at a speed set by the user. 

The goal of this project was to develop a device that allows laser therapy to be performed unattended by a practitioner. This includes eliminating the human efforts and automating the process while maintaining the current effectiveness of the treatment.

## How 
We initally did some benchmarking and came up with many preliminary concepts. The one chosen is shown below. We were inspired by the functionality of a CNC machine and so we thought this was the best bet to have a working prototype given the constraints of our project.

<figure style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/Unattended/CNC_concept.png" alt="Image" width="650" style="display: block; margin: 0 auto;">
    <figcaption style="font-style: italic; color: #aaa;">Concept drawing of "CNC machine" inspired design.</figcaption>
</figure>

The main idea is a grid-like motion on a 2D plane within an enclosed area above the patient. This motion is done by two stepper motors and controlled with feedback from distance sensors. The laser would be mvoing with a constant speed horizontally across the the patient and the surface of the patient would read a certain distance. When the distance increased dramatically, indicating the laser reaching the edge of the patient, it would move slightly upward and the go back horizontally in the opposite direction, hence the grid-like motion. The device had a temperature sensor, but it wasn't used in the feedback, it just was a proof-of-concept of how it could be potentially used to detect changes in the surface temperature of a live patient's skin. An arduino was used to control the stepper motors and sensors and it was all programmed in Arduino IDE in C++ language.


## Results

<!-- <div style="display: flex; justify-content: center; gap: 20px;">
    <div style="display: flex; justify-content: center; gap: 20px;">
        <img src="{{ site.baseurl }}/assets/Unattended/IMG_3113.jpeg" alt="Image 1" width="300">
        <img src="{{ site.baseurl }}/assets/Unattended/IMG_3111.jpeg" alt="Image 2" width="300">
    </div>
    <figcaption style="font-style: italic; color: #aaa; margin-top: 10px;">
        Unattended laser therapy (prototype) device at the UD design showcase.
    </figcaption>
</div> -->

<!-- Wrap everything in a <div> to control layout, then center the caption outside the flexbox: -->
<div style="text-align: center;">
  <div style="display: flex; justify-content: center; gap: 20px;">
    <img src="{{ site.baseurl }}/assets/Unattended/IMG_3113.jpeg" alt="Image 1" width="300">
    <img src="{{ site.baseurl }}/assets/Unattended/IMG_3111.jpeg" alt="Image 2" width="300">
  </div>
  <div style="font-style: italic; color: #aaa; margin-top: 5px;">
    Unattended laser therapy (prototype) device at the UD design showcase.
  </div>
</div>

In the end a functioning prototype was developed that we could demo to our sponsors. The prototype was fully integrated with the already existing laser therapy device. It had an adjustable height controlled by a linear actuator with a press of a button. Since we couldn't have th eactual laser on or a patient underneath we just simulated the grid-like motion of the laser in the gripper moving at a constant speed as it would when fully functional.


## Challenges
My main contribution to this project was the programming and controlling of the motors, making sure they functioned how they were supposed to. It was difficult communicating with two motors, trying to have them move together based on sensor data. I even tried using an arduino library but it got too convoluted. I ended up consulting my advisor and recommended I just start from scratch and write out base functionality code and build off that, a bottom-up approach. So that's what I did and I eventually managed to get the motors to move as intended. 

