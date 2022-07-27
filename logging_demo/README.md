## **What Is This?**

This demo creates and runs 2 individual **ROS2** nodes, **logger_usage_demo** and **logger_config**. 

Through **logger_usage_demo** implementation, working examples are provided for the following **ROS2 Logging** Usage utilities:

- [RCLCPP_INFO_ONCE](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#ac398a2db64fa466508754a6c4dc617c9)
- [RCLCPP_INFO](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#aeb160b6dd1edb7273480560c1027b264)
- [RCLCPP_ERROR](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#ad8f3687eda7312561768319e99cd4ca6)
- [RCLCPP_DEBUG_FUNCTION](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#ab0d5c80bec310a4b333f6af7be97d856)
- [RCLCPP_DEBUG_EXPRESSION](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#ae7f5710b8149302d52349fa013f1e866)
- [RCLCPP_WARN](https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html#a5d1ab3e35c046fd7bf3d5cb36484cea5)

Through **logger_config** implementation, working examples are provided for the following **ROW2 Logging**  Configuration utilities:

- [rcutils_logging_severity_level_from_string](https://docs.ros2.org/latest/api/rcutils/logging_8h.html#a50c51eb73519fb91ebac639555584cde)

![](img/logger_usage_demo_logic_flowchart.png)
![](img/logger_config_logic_flowchart.png)

## **Build**

```bash
cd $HOME
mkdir -p demo_ws/src
cd ~/demo_ws/src
git clone https://github.com/ros2/demos.git
cd ~/demo_ws
source /opt/ros/<DISTRO_NAME>/setup.bash
# source /opt/ros/rolling/setup.bash
colcon build --package-select logging_demo
```

## **Run**

```bash
# Open new terminal
cd ~/demo_ws
source install/setup.bash
```

## **Verify**

### **logger_demo_usage**

The following similar terminal output should be observed when running `ros2 run logging_demo logging_demo_main`:

```bash
[INFO] [1658673666.816515284] [logger_usage_demo]: Timer callback called (this will only log once)
[INFO] [1658673666.816867978] [logger_usage_demo]: Publishing: 'Current count: 0'
[INFO] [1658673667.316514950] [logger_usage_demo]: Publishing: 'Current count: 1'
[INFO] [1658673667.816517051] [logger_usage_demo]: Publishing: 'Current count: 2'
[INFO] [1658673668.316559879] [logger_usage_demo]: Publishing: 'Current count: 3'
[INFO] [1658673668.816574463] [logger_usage_demo]: Publishing: 'Current count: 4'
[INFO] [1658673669.316588825] [logger_usage_demo]: Publishing: 'Current count: 5'
[INFO] [1658673669.816616446] [logger_usage_demo]: Publishing: 'Current count: 6'
[INFO] [1658673670.316635607] [logger_usage_demo]: Publishing: 'Current count: 7'
[INFO] [1658673670.816658652] [logger_usage_demo]: Publishing: 'Current count: 8'
[INFO] [1658673671.316678040] [logger_usage_demo]: Publishing: 'Current count: 9'
[INFO] [1658673671.816694729] [logger_usage_demo]: Publishing: 'Current count: 10'
[INFO] [1658673671.816880187] [logger_usage_demo]: Setting severity threshold to DEBUG
[INFO] [1658673672.316734262] [logger_usage_demo]: Publishing: 'Current count: 11'
[INFO] [1658673672.816742402] [logger_usage_demo]: Publishing: 'Current count: 12'
[DEBUG] [1658673672.816889141] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[DEBUG] [1658673672.816941001] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673673.316767143] [logger_usage_demo]: Publishing: 'Current count: 13'
[INFO] [1658673673.816787196] [logger_usage_demo]: Publishing: 'Current count: 14'
[DEBUG] [1658673673.816933595] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673674.316799420] [logger_usage_demo]: Publishing: 'Current count: 15'
[WARN] [1658673674.316956350] [logger_usage_demo]: Reseting count to 0
[INFO] [1658673674.816826159] [logger_usage_demo]: Publishing: 'Current count: 0'
[ERROR] [1658673674.817002979] [logger_usage_demo]: Modulo divisor cannot be 0
[DEBUG] [1658673674.817095775] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673675.316844789] [logger_usage_demo]: Publishing: 'Current count: 1'
[DEBUG] [1658673675.317010980] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[INFO] [1658673675.816864798] [logger_usage_demo]: Publishing: 'Current count: 2'
[DEBUG] [1658673675.817040023] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[DEBUG] [1658673675.817136254] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673676.316890975] [logger_usage_demo]: Publishing: 'Current count: 3'
[DEBUG] [1658673676.317051644] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[INFO] [1658673676.816919534] [logger_usage_demo]: Publishing: 'Current count: 4'
[DEBUG] [1658673676.817076235] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[DEBUG] [1658673676.817141326] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673677.316932031] [logger_usage_demo]: Publishing: 'Current count: 5'
[INFO] [1658673677.816942424] [logger_usage_demo]: Publishing: 'Current count: 6'
[DEBUG] [1658673677.817098274] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[DEBUG] [1658673677.817152404] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673678.316962692] [logger_usage_demo]: Publishing: 'Current count: 7'
[INFO] [1658673678.816983468] [logger_usage_demo]: Publishing: 'Current count: 8'
[DEBUG] [1658673678.817127648] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673679.317004110] [logger_usage_demo]: Publishing: 'Current count: 9'
[INFO] [1658673679.817031015] [logger_usage_demo]: Publishing: 'Current count: 10'
[DEBUG] [1658673679.817175418] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673680.317044109] [logger_usage_demo]: Publishing: 'Current count: 11'
[INFO] [1658673680.817068948] [logger_usage_demo]: Publishing: 'Current count: 12'
[DEBUG] [1658673680.817273632] [logger_usage_demo]: Count divides into 12 (function evaluated to true)
[DEBUG] [1658673680.817332444] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673681.317090903] [logger_usage_demo]: Publishing: 'Current count: 13'
[INFO] [1658673681.817101197] [logger_usage_demo]: Publishing: 'Current count: 14'
[DEBUG] [1658673681.817238302] [logger_usage_demo]: Count is even (expression evaluated to true)
[INFO] [1658673682.317126985] [logger_usage_demo]: Publishing: 'Current count: 15'
...
```

The following similar terminal output should be observed when running `ros2 run logging_demo logging_demo_main`:

```bash
# Open new terminal.
cd $HOME
cd ~/demo_ws
source /opt/ros/<DISTRO_NAME>/local_setup.bash
source install/local_setup.bash
ros2 service call /logging_demo/ConfigLogger "{logger_name: user, level: DEBUG}"
```

## **FAQ**

`Q`: When I try to build the ROS2 package, I get the following build error:

```bash
--- stderr: logging_demo
CMake Error at CMakeLists.txt:34 (rosidl_get_typesupport_target):
  Unknown CMake command "rosidl_get_typesupport_target".


make: *** [Makefile:1130: cmake_check_build_system] Error 1
---
```

`A`: The issue is potentially due to the differences in **ROS_DISTRO** you are using to compile the package. Compiling with **ROS2 Rolling** or **ROS2 Galactic** should resolve this.

```bash
source /opt/ros/rolling/local_setup.bash
colcon build --packages-select logging_demo
```

`Q`: What is the difference between `rclcpp` and `rcutils` LOGGING MACROS? Is one performing better than the other? 

`A`: The difference between `rclcpp` and `rcutils` LOGGING MACROS are insignificant. `rclcpp` LOGGING MACRO are implmeented by using those of `rcutils`. 

Reference: https://answers.ros.org/question/375900/rcutils-logging-macro-vs-ros_info/?answer=376574#post-id-376574

## **References**
-  `rclcpp` ROS2 C++ Logging Utility API: https://docs.ros2.org/latest/api/rclcpp/logging_8hpp.html 
-  `rcutils` ROS2 Logging Library: https://docs.ros2.org/galactic/api/rcutils/logging_8h.html
