# MicroMouse Robot

## Overview

The **MicroMouse Robot** is an autonomous robotic vehicle designed to navigate and solve a maze. Using **Arduino Nano**, the robot is equipped with various **infrared (IR) distance measurement sensors** to detect the walls of the maze and make decisions to find the shortest path from the starting point to the center. The robot uses a **stepper motor** for movement, and a **stepper motor driver** for precise control of its position.

The robot follows a maze-solving algorithm, specifically the **left-hand algorithm**, which keeps the left-hand side of the maze as a guide, always turning left at intersections until reaching the center.

### Key Features

- **Microcontroller**: Uses **Arduino Nano** as the brain of the robot to control sensors, motors, and algorithms.
- **Sensors**: 
  - **IR-based Distance Sensors**: Two sensors at the front and one on the left and right sides to measure distance from walls and detect obstacles.
- **Movement**: The robot moves based on commands derived from the sensor data and is controlled by **stepper motors** and **stepper motor drivers** for precise motion.
- **Maze Solving**: Implements the **left-hand algorithm** to navigate the maze.
- **Autonomous Navigation**: The robot is fully autonomous, with no manual control required once it starts the maze.

## System Components

- **Microcontroller**: **Arduino Nano**
- **Motors**: **Stepper Motors** for movement
- **Motor Driver**: **Stepper Motor Driver** for controlling the stepper motors
- **Sensors**: 
  - **2 IR Distance Sensors** on the front for measuring the distance to walls.
  - **Left and Right IR Sensors** to detect obstacles on the respective sides.
- **Power Supply**: The robot runs on a rechargeable battery to power the Arduino Nano, motors, and sensors.

## Features in Detail

### 1. **Distance Sensors**
The robot uses a combination of **IR distance sensors** to map its environment and make decisions about where to move. The **front sensors** measure the distance to the wall in front, while the **left and right sensors** detect obstacles on the respective sides. These sensors feed real-time data to the Arduino Nano, which makes decisions on whether to move forward, backward, or turn left/right.

### 2. **Left-Hand Algorithm for Maze Solving**
The **left-hand algorithm** is a simple yet effective strategy for maze navigation. The robot:
- Keeps its **left hand** on the wall, ensuring it never gets lost in the maze.
- At every intersection or decision point, it turns left if possible, ensuring that it will eventually reach the center of the maze.

This algorithm is simple but reliable, and it's commonly used in the **MicroMouse competition**.

### 3. **Movement and Control**
The robot uses **stepper motors** for precise movement. The **stepper motor driver** ensures that the robot can move accurately through the maze by controlling the direction and steps of the motors.

The movement is controlled as follows:
- **Move Forward**: The robot moves straight ahead if there is no obstacle in front.
- **Turn Left/Right**: Based on sensor data, the robot turns left or right as needed.
- **Move Backward**: If it encounters a dead-end, the robot will backtrack to explore other possible paths.

### 4. **Arduino Nano and Programming**
The robot is programmed using **C++** in the **Arduino IDE**. The code reads data from the sensors and makes decisions based on the left-hand algorithm to navigate the maze. The Arduino Nano processes the sensor inputs and outputs commands to the motors in real-time to ensure smooth navigation.

### 5. **Testing and Optimization**
Once the robot is programmed, it can be tested in a maze to evaluate its performance. Adjustments to the sensors, motors, and algorithms can be made to improve the robot's speed and accuracy in solving the maze. Fine-tuning the code and hardware setup will help the robot perform better in different maze environments.

---

## Circuit Diagram

The circuit diagram illustrates:
- **Arduino Nano** connections to the **IR sensors** (front, left, right).
- **Stepper motor connections** to the **stepper motor driver**.
- **Power supply connections** for both the microcontroller and motors.

---

## Hardware Components List

1. **Arduino Nano** (Microcontroller)
2. **IR Distance Sensors** (2 front sensors, 1 left sensor, 1 right sensor)
3. **Stepper Motors** (For movement)
4. **Stepper Motor Driver** (To control the stepper motors)
5. **Rechargeable Battery** (For powering the robot)
6. **Wires and Connectors** (For connections)
7. **Chassis** (For holding all components together)

---

## Software and Development Environment

- **Arduino IDE**: Used for writing, compiling, and uploading code to the **Arduino Nano**.
- **Programming Language**: **C++** (Arduino programming language).

---

## System Workflow

1. **Startup**: The Arduino Nano initializes the sensors and motor drivers.
2. **Sensor Readings**: The IR sensors detect the proximity of walls in front, left, and right.
3. **Decision Making**: Based on the sensor data, the robot decides to:
   - Move forward if no obstacle is detected.
   - Turn left if there's an intersection or dead-end.
   - Turn right or move backward if necessary.
4. **Left-Hand Algorithm**: The robot keeps its left-hand side on the wall and turns left at intersections, ensuring it finds its way to the center.
5. **Completion**: Once the robot reaches the center of the maze, it has solved the maze autonomously.

---

## Contributing

Feel free to fork the repository, report bugs, and submit pull requests. Contributions to improve the functionality and stability of the project are welcome.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Thanks to the **Arduino IDE** and **C++** for their tools and language that made this project possible.
- Special thanks to the open-source community for their resources and support.

