# Human-Following-Robot-Arduino-

A four-wheel robot that detects a person and turns toward them, built for the **Eco Innova challenge at Mekathlon 2024-25** while I was in Class XII.

> **Credit:** This project is based on the human-following robot tutorial by **DIY Builder** ([tutorial link](https://youtu.be/yAV5aZ0unag?si=coUM23Ws61z-ip-E)).

## Demo

- Demo video 1: [LinkedIn post](https://lnkd.in/p/gBsASFh6)
- Demo video 2: [Sensor test](sensor_test.mp4). A hand is placed in front of an infrared sensor, and the wheels turn toward that side.
- Photo:
 ![Robot photo](https://media.licdn.com/dms/image/v2/D562DAQGvdgOVUAmzLw/profile-treasury-image-shrink_480_480/B56aHuYTuGH0AU-/0/1795000712381?e=1795773600&v=beta&t=K5yPX0gXpYd8UV_icXjy5tYlMyQeEcOFk00krstfnOU)

## What it does

The robot senses a person in front of it and moves its wheels toward the side where the person was detected. Two infrared sensors tell it whether someone is on its left or right, and an ultrasonic sensor on a servo-mounted head measures the distance.

## Hardware

| Component | Qty | Purpose |
|---|---|---|
| Arduino Uno | 1 | Main controller |
| Motor driver shield (ADD-MODEL, e.g. L293D) | 1 | Drives the four motors |
| TT gear motors | 4 | Move the robot |
| Wheels | 4 | Attached to the motors |
| Servo motor | 1 | Holds and moves the ultrasonic sensor head |
| Ultrasonic sensor (HC-SR04) | 1 | Measures distance to the person |
| Infrared (IR) sensors | 2 | Detect whether a person is on the left or right |
| Male and female jumper wires | Several | Connections |
| DC power switch | 1 | Turns the robot on and off |
| 9V batteries | 3 | Power supply (ADD-HOW-THEY-WERE-CONNECTED) |

## How it works

1. The ultrasonic sensor measures the distance to the person in front of the robot.
2. The left and right IR sensors each give a signal when something is in front of them.
3. If the left sensor detects a person, the robot turns left. If the right sensor detects a person, it turns right.
4. If the person is within the following range, the robot moves toward them. If nobody is detected, it stops.

## Pin connections

| Part | Connection |
|---|---|
| Ultrasonic sensor, Echo | A0 |
| Ultrasonic sensor, Trig | A1 |
| Right IR sensor, OUT | A2 |
| Left IR sensor, OUT | A3 |
| Ultrasonic and IR sensors, VCC | +5V on the shield's header |
| Ultrasonic and IR sensors, GND | GND on the shield's header |
| Servo motor | Servo header on the motor driver shield (ADD-SER1-OR-SER2) |
| Motors | M1, M2, M3, M4 terminals on the shield |
| Battery pack | +M and GND terminals on the shield, through the power switch |

## My part

- Assembled the chassis, motors, wheels, and sensors
- Wired the Arduino, motor driver shield, servo, and sensors
- Uploaded and tested the code, and troubleshot problems
- Competed with the robot at Mekathlon 2024-25

## Result

The robot reached the final stage of the competition. At the last moment, a battery failure caused a power cut and stopped the run.

## What I learned

- **Power is part of the design.** A good robot with a weak battery is a failed robot.
- **Test the whole system, not just the code.** Everything worked until the one thing I had not stress-tested.
- **Plan for failure.** Carry a backup, check connections, and do not assume it will work on the day.

## Possible improvements

- Replace the 9V batteries with a rechargeable pack, since 9V batteries drain quickly when they drive motors.
- Carry spare batteries and use fresh or fully charged ones before every run.
- Power the Arduino separately from the motors.
- Add a voltage indicator to check battery level.
- Add more sensors for smoother tracking.

## Credits and license

- Original design: DIY Builder tutorial (https://youtu.be/yAV5aZ0unag?si=U98nsG80JnvO0z4J). Check the original's license and follow its terms.
- Documentation, photos, and videos: Saumya Sahu.
- License for this repo: MIT. This applies to my documentation and my own work. The original design and code remain under the DIY Builder tutorial's terms (https://youtu.be/yAV5aZ0unag?si=vWdB-3jS2P7b7KGI).

## Author

Saumya Sahu | [LinkedIn](https://www.linkedin.com/in/saumyasahu-tech/)
