# CS147Lab-Tue-ZiCong-Stanley
Code for CS147's Labs
Our Team: ZiCong Yu (Leader), Quang Dinh Tue Tran, Stanley Jian

Lab 1 — Build the Kit
People: Lab 1 — Build the Kit
GroupPointsDue
Group
Labs	Points
10	Due
Fri 09 Oct
Grading (rubric below, 10 pts): Demo — TA checkoff 5 · Serial log 3 · Photo 2. Graded as a team. Not attending the Fri Oct 16 checkoff = 0. Late: 20% per day (syllabus), waived if a teammate submitted on time. Built during the week on your own kit; demonstrated in Friday lab. One member is picked at random to explain the code.

Build instructions: Lab 1 – Build Your Kit in Stages

Wiring diagrams, parts list per stage, and the kit-check sketch. In Lab 1 you solder every header and wire Stage 1 (what Lab 2 needs). Stage 2 (I²C sensors) is due by Wed Oct 14, Stage 3 (servo rail) by Wed Oct 21, Stage 4 (LoRa) by Wed Nov 4.

This one is built in the room
Three jobs run in parallel. Rotate at the ten-minute mark so everyone holds the iron.

Solder headers onto the OLED, the MPU-6050 and the BMP280.
Cut, strip and bundle jumper leads to length for the fixed rail wiring.
Build the breadboard baseline and stage the acceptance test.
The baseline circuit
ESP32, SPI OLED, potentiometer on the ADC, button, LED and buzzer, wired to match the pin map the CS147Pins library assumes — so every later activity drops onto the same board with no rewiring.

The acceptance test is the deliverable
A provided sketch with four TODOs walks every pin, scans the I²C bus expecting three addresses, drives the display, reads the pot and the button, and prints a PASS / FAIL table.

Submit: the serial log of a full run and a photo of the assembled board. The log is your kit's permanent record.

Read Lab Safety: Soldering before you arrive.

-----------------------------------------------------------------------------------------------------------------

Lab 2 — Traffic Controller
📄 Lab handout: Lab 2 – Traffic Controller (Google Doc)

People: Lab 2 — Traffic Controller
GroupPointsDue
Group
Labs	Points
10	Due
Fri 23 Oct
Demo 5 · Code 3 · Project Analysis 2. Built during the week on your own kit; demonstrated in Friday lab. One member is picked at random to explain the code.

A simplified traffic-light controller as a state machine: three LEDs, a buzzer and a pedestrian button.

Red 10 s. Yellow and red-yellow 2 s each. Green holds until the pedestrian button is pressed, then at least 5 s more. Buzzer 500 ms on / 1500 ms off in green, 250 / 250 in red.

Project Analysis: why does green stay until asked? What is the safest initial state on power-up, and why? What would you add for a pedestrian with a visual or auditory impairment?