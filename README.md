# MowBot: A Smart Robotic Solution for Automated Lawn Mowing

## Project Purpose
The primary purpose of **MowBot** is to automate the task of lawn mowing to reduce the physical labor, time consumption, and health risks associated with traditional lawn maintenance.

***Safety & Health:** It aims to mitigate risks such as dehydration, heatstroke, and exhaustion caused by prolonged exposure to the sun and extreme heat during manual mowing.
***Efficiency:** The robot is designed to operate autonomously, cutting grass evenly while maneuvering through the lawn with minimal human intervention.
  **Sustainability:** Unlike gas-powered mowers that release harmful emissions, MowBot utilizes a rechargeable battery system, offering a cleaner and more energy-efficient solution.

## Technologies Used
The development of MowBot integrates various hardware and software components to achieve autonomous operation:

**Mobile Platform:** A four-wheeled chassis selected for stability and maneuverability on flat grass surfaces.
**Power System:** A rechargeable battery system designed to provide sustainable energy for operations.
**Mowing Mechanism:** A DC motor equipped with rotating blades, mounted on the front of the chassis for quiet and smooth cutting.
**Sensor Array:** Object detection sensors used to identify obstructions (trees, furniture, walls) and trigger obstacle avoidance logic.
**Control System:** Programmable algorithms that manage movement, blade operation, and obstacle avoidance.

## Proponents
**Department of Computer Applications**
**Mindanao State University – Iligan Institute of Technology**

**Karl Michael T. Bulos**

**Floyd Joshua T. Luna**

**Reymart K. Respecia**

**Rafael Pogenio**

## Block Diagram
The following diagram illustrates the operational flow of the MowBot system, from power distribution to sensor input and actuator output.


    %% graph TD
    %% Power System
    Power[Rechargeable Battery Source] -->|Supplies Power| Micro[Microcontroller/Main Unit]
    Power -->|Supplies Power| Motors

    %% Input Section
    subgraph Inputs
    Sensors[Obstacle Detection Sensors] -->|Data Signal| Micro
    end

    %% Processing Section
    subgraph Processing
    Micro -->|Executes| Algo[Navigation & Avoidance Algorithm]
    Algo -->|Decision Making| Micro
    end

    %% Output Section
    subgraph Outputs
    Micro -->|Control Signal| WheelMotor[Wheel Motors (Navigation)]
    Micro -->|Control Signal| BladeMotor[Cutter Motor (Mowing)]
    end

    %% Physical Interaction
    WheelMotor -->|Action| Move[Robot Moves/Turns]
    BladeMotor -->|Action| Cut[Blades Rotate]
    Sensors -.->|Detects| Obstacle[Obstacles in Path]
    Move -.->|Encounters| Obstacle
