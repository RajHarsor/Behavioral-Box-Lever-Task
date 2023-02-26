# Behavioral-Box-Lever-Task

## Task Description
The basis of the this task is that the mouse is to learn to do an equal ration of pushes and pulls. By maintaining an equal ration, the mouse will maximize the amount of water that it will recieve. 

## Task Layout
The basic layout of the task can be described by the flow chart below. To start the task, the mouse will have to hold the joystick at position (0,0) or in the neutral resting position of the joystick. Following holding this neutral position for 50 ms, the task will start. A sound will be played which is 3khz in frequency for 100 ms. The sound is meant to cue the mouse to either push or pull the joystick. A push will result in "reward 1" and a pull will result in "reward 2." The rewards are different amounts of water and the amounts are dependant on the ratio of push to pull. If the mouse does not push or pull the joystick and exceeds the timeout limit specified in the code, the mouse will receive an air puff as a punishment. An ISI delay will follow in between each trial.

((Insert Picture here))

## Building the Behavioral Box
Most of the behavioral box is built using ThorLabs parts and some additional supplies from Amazon and Adafuit. This list contains the structural components of the box as well as the electronics components.

## The Circuit and Code for Prototyping
The circuit is built using a Teensy 4.1 instead of an Arduino board. The reason this is the case is because a Teensy board allows for multithreading while Arduino boards don't. Despite this, an Arduino board can work for prototyping the system and making changes on it if you don't have a Teensy board available (Please see "Using the Arduino Board to Prototype Section). A diagram of the Arduino board is shown below as well as the Teensy board circuit. 

The final build should be made using a Teensy board microcontroller since you will need to be able to run two programs simultaneously. Also, the Teensy board is much stronger than the Arduino board and will likely run into less problems due to the power it has. 

### The Code 
The code can be divided in two different programs. The first program will run to just acquire the joystick position at all times. The second program will run to actually run the behavioral task. Annotations have been made in the code. If not making big changes to the code, it likely will be best practice to just modulate times/variables in the first part of the code.

 ### Using the Arduino Board for Prototype
 Despite is being preferable to use the Teensy board, the Arduino board can be used for prototyping, testings, and making changes to the second porgram in the code. Wire up the Arduino board as in the diagram above 

## Recording Joystick Data
The code will run and print the joystick positon as well as other information regarding the task to the Serial monitor (most likely baud 9600). 


