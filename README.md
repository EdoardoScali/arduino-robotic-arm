# Arduino Robotic Arm

A 6-DOF robotic arm built around an Arduino Uno, driven by six servos and controlled in real time with three analog joysticks.

![Robotic arm](arm_photo.png)

▶️ **[Watch it in action on YouTube](https://youtu.be/w_Bx6zkQ4wo)**

## How it works

Each joystick controls two joints. Pushing a stick past its dead zone moves the corresponding servo 3° per loop, and releasing it holds the current position, so the arm can be positioned precisely and stays put.

| Joystick | X axis | Y axis |
|---|---|---|
| 1 (farthest from the batteries) | Base rotation | Shoulder |
| 2 (middle) | Elbow | Wrist pitch |
| 3 (closest to the batteries) | Wrist rotation | Gripper |

Every joint is clamped to its own angle limits to protect the mechanics. These limits depend on the physical assembly, so if you build your own, find yours using the Serial Monitor (9600 baud), which prints all servo angles live.

The system runs on four 18650 cells in parallel, stepped up to 5 V with a DC-DC boost converter.

## Wiring

Servos connect to digital pins **D2–D7** (base to gripper), joysticks to analog pins **A0–A5**.

![Circuit diagram](circuit%20diagram.jpg)

## License

[MIT](LICENSE)
