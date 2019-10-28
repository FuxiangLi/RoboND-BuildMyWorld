# RoboND-BuildMyWorld
This is the code for my Udacity Robotics Software Engineer Nanodegree  - Build My World. It creates a simulation world with Gazebo.

### Directory Structure
```
    .RoboND-BuildMyWorld               # main folder 
    ├── images                         # Code output image
    │   ├── output.png
    ├── model                          # Model files of the two-wheeled robot
    │   ├── Building
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── MobileRobot
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script
    │   ├── welcome_message.cpp
    ├── world                          # Gazebo main World containing models
    │   ├── MyHome.world
    ├── CMakeLists.txt                 # Link libraries 
    └── README.md
```

### Steps to launch the simulation

#### Clone the project folder in /home/workspace/
```sh
$ cd /home/workspace/
$ git clone https://github.com/nancyreschka/RoboND-BuildMyWorld.git
```

#### Compile the code
```sh
$ cd /home/workspace/RoboND-BuildMyWorld/
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/RoboND-BuildMyWorld/build
```

#### Run the Gazebo World file  
```sh
$ cd /home/workspace/RoboND-BuildMyWorld/world/
$ gazebo MyHome.world
```

### Output
A welcome message is printed and the Building, MobileRobots are displayed inside a Gazebo World. It should launch as follow:
![alt text](images/output.png)
