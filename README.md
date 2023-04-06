# agile_autonomy_flightmare

Modified flightmare for the paper Learning to Fly in the Wild

## installation
### 1. 功能包准备
下载flights_autonomy_flightmare和assimp_catkin
```
mkdir flights_autonomy_flightmare_ws
cd flights_autonomy_flightmare_ws
mkdir src
cd src
git clone https://github.com/antonilo/flightmare_agile_autonomy.git
git clone https://github.com/uzh-rpg/assimp_catkin.git
```
把原本的flightmare下的catkin_simple、eigen_catkin、mav_comm拷贝过来
### 2. 依赖安装
```
git clone https://github.com/glfw/glfw.git
cd glfw
mkdir build
cmake ..
make -j4
sudo make install
```
### 2. 修改
在rpgq_simulator/CMakeLists.txt里面第18行后面添加
```
include_directories(${CMAKE_BINARY_DIR}/rpgq_simulator/configuration)
```
### 3. 编译
```
cd flights_autonomy_flightmare_ws
catkin build assimp_catkin
catkin build
```


