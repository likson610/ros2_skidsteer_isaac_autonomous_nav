# 🤖 Skid-steer Autonomous Vehicle Simulation (ROS 2 Jazzy + Isaac Sim + Nav2)

This project contains configuration and launch files for autonomous vehicle simulations within the NVIDIA Isaac Sim environment. It integrates the ZED SDK for sensing and Nav2 for autonomous navigation.

## 📋 Requirements

To run this simulation correctly, ensure you have the following software installed:

* **ROS 2:** Jazzy Jalisco
* **Isaac Sim:** (Version 5.1.0 recommended)
* **RViz2:** For visualization
* **Nav2:** Navigation Stack
* **ZED Wrapper & ZED SDK:** For camera integration and spatial sensing

## 📂 Directory Structure

The repository must be cloned into the `src` folder of your ROS 2 workspace. Build and launch commands must be executed from the **workspace root**, not from within the `src` folder.

The correct structure should look like this:
```text
your_workspace/
├── build/
├── install/
├── log/
└── src/
    └── skidsteer_simulation/  <-- (this repository)
        ├── config/
        ├── launch/
        ├── urdf/
        └── CMakeLists.txt
```
## 🚀 Installation and Building
1. Source the Global Environment:
Navigate to the root directory of your workspace. Ensure the global ROS 2 Jazzy environment is sourced:
```text
source /opt/ros/jazzy/setup.bash
```
**💡 Pro Tip: To avoid running this command in every new terminal, add it to your .bashrc:**
```text
echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
2. Build the Project:
From the root of your workspace, run:
```text
colcon build --symlink-install
```
3. Launch the Simulation:
After a successful build, source your local workspace and launch the simulation:
```text
source install/setup.bash
ros2 launch skidsteer_simulation full.launch.xml
```
## 🛠️ Recommended Tools
For the best development experience, we recommend using Visual Studio Code with the following extension:

Robot Developer Extensions for ROS 2 (by Ranch Hand Robotics LLC): Provides essential syntax highlighting, code snippets, and autocompletion for ROS 2 development.
