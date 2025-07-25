# 🤖 RobotStudio Trajectory Simulation: Drawing "A" and "C" on an Inclined Table

> This project was developed as part of a practical robotics module and serves as an academic example of trajectory design, workobject calibration, and robot simulation under imperfect conditions.
> 
## 👩‍💻 Author

- **Maria-Daniela Munteanu**  
  Faculty of Automatic Control and Computer Engineering  
  Technical University "Gheorghe Asachi" of Iași
- **Daniel Drapiciuc**  
  Faculty of Automatic Control and Computer Engineering  
  Technical University "Gheorghe Asachi" of Iași 


## 📌 Project Overview

This project demonstrates a **robotic path planning and simulation** task using **ABB RobotStudio**, where an industrial robot is programmed to draw the letters **"A"** and **"C"** on an **inclined surface**. The project was developed as part of an academic exercise by **Maria-Daniela Munteanu** in collaboration with **Daniel Drapiciuc**.

The challenge showcases trajectory accuracy under physical constraints such as non-horizontal working planes and real-world spatial limitations — essential concepts in applied robotics.

---

## 🎯 Goal of the Project

- 🅰️ Simulate the drawing of **letters "A" and "C"**, which represent the initials of our faculty (*Automatic Control and Computer Engineering*).
- 🧭 Execute these trajectories on a **tilted table**, simulating real-world complexity like gravity bias and tool misalignment.
- 🤖 Use **ABB RobotStudio** and **RAPID** programming to create and test the robotic routine in a 3D virtual environment.

---

## 🧠 Technical Challenges Addressed

| Challenge                              | Approach Taken                                                                 |
|----------------------------------------|---------------------------------------------------------------------------------|
| Inclined surface → Z-axis bias         | Custom workobject and tool alignment using transformation matrices             |
| Physical reachability and collision    | Careful joint orientation planning and TCP positioning in simulation           |
| Trajectory accuracy (curves, sharpness)| Decomposition of letters into fine linear and circular RAPID motion primitives |
| Real-time visualization                | Tested in RobotStudio using virtual execution + recorded demo in `.mp4` format |

---

## 🧰 Tools Used

- **ABB RobotStudio** – Industry-grade simulation and programming tool
- **RAPID** – ABB's high-level programming language for robot control
- **.rspag** File – Contains the full simulation environment (robot cell, table, TCP, path)
- **.mp4** Demo – Video recording showing the drawing execution in simulation

---

## 🖥️ Project Components

| File                            | Description                                                       |
|----------------------------------|-------------------------------------------------------------------|
| `Proiect_Robotica_Drapiciuc_Munteanu.rspag` | RobotStudio project file containing robot cell and code         |
| `demo_AC_drawing.mp4`           | Simulation video showing the robot drawing "A" and "C"            |

> 🛠 *Note: To open `.rspag`, use ABB RobotStudio (downloadable from the official ABB website).*

---

## 🔍 How It Works

1. A virtual workcell is created in **RobotStudio**, including:
   - ABB industrial arm (e.g. IRB 120 or IRB 140)
   - An **inclined table** with a defined *WorkObject* (non-zero rotation)
   - A custom TCP simulating a pen/tool

2. The letters "A" and "C" are defined via:
   - **Linear** (`MoveL`) and **circular** (`MoveC`) instructions
   - Coordinated tool paths with proper Z-depth and approach distances

3. The robot executes these motions in the simulation, maintaining consistent drawing contact despite surface bias.
   
## 🧩 Possible Extensions

- Add more letters or complex shapes
- Replace the stylus with a real end-effector or laser
- Use sensors to adapt the trajectory in real time (closed-loop control)

---

## 🎥 Demo Preview

📽️ mp4 attached.
