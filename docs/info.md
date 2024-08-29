<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

The traffic light control system cycles through three states—RED, GREEN, and YELLOW—based on a clock signal and vehicle detection from a sensor input. The system starts in the RED state and transitions to GREEN after a set time. If the sensor detects no vehicles, it may switch from GREEN to YELLOW early; otherwise, it transitions when the GREEN timer expires. 

A countdown timer is used for each state, and when it reaches zero, the system moves to the next state. This ensures a smooth and orderly flow of traffic. The reset input allows the system to restart from the RED state if necessary.

## How to test

1. *Normal Operation*:
   - *Red Light*: On for 60 seconds.
   - *Green Light*: On for 60 seconds.
   - *Yellow Light*: On for 5 seconds.
   - After the yellow light, the cycle repeats back to red.

2. *Vehicle Detection with Magnetic Sensor*:
   - When the *light is green* and the *magnetic sensor* detects *no vehicles*, the light changes:
     - *From Green to Yellow* immediately, reducing the green light duration.
     - Then, *from Yellow to Red*, allowing other vehicles on different roads at the intersection to proceed earlier than they would under normal timing.

### Key Points of the System:

- *Adaptive Traffic Control*: The system adapts to real-time traffic conditions, enhancing efficiency at intersections.
- *Priority to Active Roads*: By reducing the green light duration when no vehicles are present, it reduces wait times for vehicles on other roads.
- *Energy Efficiency and Reduced Idle Time*: Reducing unnecessary green light time helps save energy and reduces idle time for vehicles waiting at red lights, improving fuel efficiency and reducing emissions.


## External hardware

LEDs: To visually represent the RED, GREEN, and YELLOW lights.
Inductive Loop Sensor: embedding a loop of wire in the road surface. The sensor detects changes in the inductance caused by the presence of a vehicle over the loop.
