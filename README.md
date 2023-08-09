# ROS package for TeraRanger modules  
[![Build Status](https://travis-ci.org/Terabee/teraranger.svg?branch=master)](https://travis-ci.org/Terabee/teraranger)

 This package is a collection of nodes for TeraRanger single sensor modules.

 * [TeraRanger Evo Mini](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-mini/)
 * [TeraRanger Evo Thermal 33/90](https://www.terabee.com/sensors-modules/thermal-cameras/)
 * [TeraRanger Evo 64px](https://www.terabee.com/shop/3d-tof-cameras/teraranger-evo-64px/)
 * [TeraRanger Evo 60m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-60m/)
 * [TeraRanger Evo 40m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-40m/)
 * [TeraRanger Evo 15m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-15m/)
 * [TeraRanger Evo 3m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-3m/)
 * [TeraRanger One](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-one/)
 * [TeraRanger Duo](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-duo/)

Link to ROS Wiki package documentation: [Here](http://wiki.ros.org/teraranger)

## Dependencies

This package depends on this [serial](http://wiki.ros.org/serial) library. To get it, execute the following command:

```
sudo apt-get install ros-<your_distro>-serial
```

where <your_distro> is your ROS distribution (e.g. kinetic, lunar, indigo).

If it's not available for your distribution, clone https://github.com/wjwwood/serial into your workspace, then build and source your workspace.


### Building and Running the package from source

 To clone and build the package in your workspace follow these steps:

```
cd ~/stereo_ws/src
git clone https://github.com/up-caelivia/teraranger.git
cd ..
catkin_make
source devel/setup.bash
```

## Running the TeraRanger EVO at right side

After your workspace is built and sourced:
```
roslaunch teraranger teraranger_right.launch
```

## Running the TeraRanger EVO at left side

After your workspace is built and sourced:
```
roslaunch teraranger teraranger_left.launch
```

## Changing Sensor Parameters

You can change the mode of the sensors by running **rqt_reconfigure**:

```
rosrun rqt_reconfigure rqt_reconfigure
```

## Displaying Sensor Information

When the teraranger node is running in a new terminal window execute:

```
rostopic list
```

to see list of available topics. If the teraranger node is running and the sensor is connected to your PC you should see topics starting with /teraranger.

To display the messages arriving on the topic run the following command in a terminal:

```
rostopic echo /teraranger_<sensor_name>
```

where <sensor_name> is the name of your sensor (e.g. one, evo).

## Product pictures and where to get the sensors

### TeraRanger Evo Mini

<img src="https://www.terabee.com/wp-content/uploads/2019/11/TeraRanger-Evo-Mini-image.jpg" width="300"/>

| Information |
| -------------- |
|[Product page](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-mini/)|
|[Specification sheet]()|

### TeraRanger Evo Thermal 33/90

<img src="https://www.terabee.com/wp-content/uploads/2019/04/TR-EVO-T90-USB-3-1024x1024-1.jpg" width="500"/>

| Information |
| -------------- |
| Product pages [Evo Thermal 33](https://www.terabee.com/shop/thermal-cameras/teraranger-evo-thermal-33/) / [Evo Thermal 90](https://www.terabee.com/shop/thermal-cameras/teraranger-evo-thermal-90/)|
|[Specification sheet](https://www.terabee.com/wp-content/uploads/2019/03/TeraRanger-Evo-Thermal-Specification-Sheet-1-2.pdf)|

### TeraRanger Evo 64px

<img src="https://www.terabee.com/wp-content/uploads/2019/04/TR-EVO-64PX-USB-3.jpg " width="300"/>

| Information |
| -------------- |
|[Product page Evo 64px](https://www.terabee.com/shop/3d-tof-cameras/teraranger-evo-64px/)|
|[Specification sheet](https://www.terabee.com/wp-content/uploads/2019/03/TeraRanger-Evo-64px-Specification-sheet-2-1.pdf)|

### TeraRanger Evo 3m

<img src="https://www.terabee.com/wp-content/uploads/2019/03/4-teraranger-evo-3m-short-range-ir-distance-sensor-usb.jpg" width="300"/>

| Information |
| -------------- |
|[Product page Evo 3m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-3m/)|
|[Specification sheet](https://www.terabee.com/wp-content/uploads/2019/03/TeraRanger-Evo-3m-Specification-sheet-1.pdf)|

### TeraRanger Evo 60m/Evo 40m/Evo 15m

<img src="https://www.terabee.com/wp-content/uploads/2019/04/TR-EVO-60M-USB-1.jpg" width="300"/>

| Information |
| -------------- |
|Product pages [Evo 60m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-60m/) / [Evo 40m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-40m/) / [Evo 15m](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-15m/)|
|Specification sheets [Evo 60m](https://terabee.b-cdn.net/wp-content/uploads/2021/02/Specification-Sheet-Evo-60m.pdf) / [Evo 40m](https://terabee.b-cdn.net/wp-content/uploads/2021/02/Specification-Sheet-Evo-40m.pdf) / [Evo 15m](https://terabee.b-cdn.net/wp-content/uploads/2021/02/Specification-Sheet-Evo-15m.pdf)|

### TeraRanger One
<img src="https://www.terabee.com/wp-content/uploads/2019/03/6-teraranger-one-small-tof-sensor.jpg" width="300"/>

| Information |
| -------------- |
|[Product page](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-one/)|
|[Specification sheet](https://www.terabee.com/wp-content/uploads/2019/03/TeraRanger-One-Specification-Sheet1-1.pdf)|

### TeraRanger Duo

<img src="https://www.terabee.com/wp-content/uploads/2019/03/TeraRanger-Duo.png" width="300"/>

| Information |
| -------------- |
|[Product page](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-duo/)|
|[Specification sheet](https://www.terabee.com/wp-content/uploads/2019/03/TeraRangerDuospecificationsheet-1.pdf)|
