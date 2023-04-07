# agile_autonomy_flightmare

Modified flightmare for the paper Learning to Fly in the Wild

## installation
### 1. package preparation
download flights_autonomy_flightmare and assimp_catkin.
```
mkdir flights_autonomy_flightmare_ws
cd flights_autonomy_flightmare_ws
mkdir src
cd src
git clone https://github.com/antonilo/flightmare_agile_autonomy.git
git clone https://github.com/uzh-rpg/assimp_catkin.git
```
copy catkin_simple, eigen_catkin & mav_comm from flightmare_ws to current directory.
### 2. dependencies installation
install glfw.
```
git clone https://github.com/glfw/glfw.git
cd glfw
mkdir build
cmake ..
make -j4
sudo make install
```
install glm.
```
sudo apt-get update
sudo apt-get install -y libglm-dev
```
### 3. source code modification
add following line after line 18 at rpgq_simulator/CMakeLists.txt.
```
include_directories(${CMAKE_BINARY_DIR}/rpgq_simulator/configuration)
```
### 4. flightrender download
download unity standalone.tar from here[https://zenodo.org/record/5517791/files/standalone.tar?download=1] & unzip into flightrender directory.
### 5. build
```
cd flights_autonomy_flightmare_ws
catkin build assimp_catkin
catkin build
```


