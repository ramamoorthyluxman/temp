# Project Title

Ramamoorthy Luxman Imvia repository

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

```
ROS Melodic
Ubuntu 18.04
```

### Installations

Install the following components


#### Installation of EVA SDK - Python

https://pypi.org/project/eva-sdk/
https://automata.tech/docs/v/3.1.0/

http://172.16.16.2/GET/api/v1/

```
pip install evasdk

```

If there is a problem with websockets during the installation :

```
sudo python3 get-pip.py

```

```
sudo pip3 install websockets

```
```
pip install evasdk

```
##### Web interface
```
roslaunch rosbridge_server rosbridge_websocket.launch
```
```
cd ~/ws/src/imvia/webpage_ws
python -m SimpleHTTPServer 7000
```
HTTP requests:

Tutorial: https://www.youtube.com/watch?v=CFzgKfnmG-Q - 
https://www.youtube.com/watch?v=dgvLegLW6ek


```
roslaunch eva_description eva.launch
roslaunch eva_gazebo eva_world.launch
roslaunch eva_control eva_control.launch
rostopic pub /eva/joint23_position_controller/command std_msgs/Float64 "data: -1.2"
```
http://192.168.1.21:7000/

```
rostopic pub /eva/joint23_position_controller/command std_msgs/Float64 "data: -0.9"
```

```
sudo apt-get install ros-melodic-moveit-simple-controller-manager
sudo apt-get install ros-melodic-gazebo-ros-control
rosdep install --from-paths src --ignore-src -r -y
```

To view frames
```
rosrun tf view_frames
```
##### Connecting  EVA 

Set the computer IP to 

```
static IP 172.16.16.1 Subnet mask 255.255.255.0
```

Administrator user ID ramamoorthy_luxman@etu.u-bourgogne.fr password: hackmeeva

##### Running the eva ros driver

```

rosrun eva_driver test.py

IP 172.16.16.2

Token: 2e49551cc7cb55556ee0468e30296755e9f2cf01

```

## Running the tests



## SUMUM demo
```

rosrun eva_driver sumum.py

roslaunch avt_vimba_camera mono_camera.launch

```
```

Open rave installation 
https://roboticslab-uc3m.github.io/installation-guides/install-openrave.html

If you get opengl error 
sudo ln -s /usr/lib/x86_64-linux-gnu/libGL.so.1 /usr/lib/libGL.so

for running the example 
https://scaron.info/teaching/installing-openrave-on-ubuntu-16.04.html


IKFast - Working steps 
note: do not follow the above links. 
https://ros-planning.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html#tweaking-the-creation-process

rosrun moveit_kinematics auto_create_ikfast_moveit_plugin.sh --iktype Transform6D $MYROBOT_NAME.urdf eva base_link link6

```

## OS Tools installations (Optional - for personal use)


#### apt-file

'''
sudo apt-get install apt-file
'''

Usage example

'''
apt-file search Qt5CoreConfig.cmake
    
'''


#### REST and GraphQL API framework builder
'''
https://api-platform.com/
'''




## Authors

* **Ramamoorthy Luxman** 


import error: "rospkg" 
sudo pip3 install rospkg catkin_pkg

https://wiki.ros.org/arm_navigation/Tutorials/Running%20arm%20navigation%20on%20non-PR2%20arm - for robot arm driver development


Eva with Linear actuator

rosrun dobot server /dev/ttyUSB0

rosservice call /DobotServer/SetPTPWithLCmd "{ptpMode: 1, x: 200.0, y: 0.0, z: -30.0, r: 0.0, l: 1000}"

sudo chmod a+rw /dev/ttyUSB0


sudo apt remove cmdtest
sudo apt remove yarn
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install yarn -y


##### For Yuly ####

Press windows key and type terminator

sudo python platform_control.py
192.168.187.1

XY Platform
sudo chmod a+x /dev/ttyACM0
sudo chmod a+rw /dev/ttyACM0
sudo python platform_control.py
cd ~/ws/src/imvia/xy_platform/src


roscore
roslaunch eva_arm_moveit_config live.launch
python3 eva_control_server.py


##### FOR UI #####


For handplus

npm install vue-numeric-input --save
npm i --save @hipsjs/flowy-vue
npm install vue-drag-and-flow -s


https://github.com/vuejs/awesome-vue#video-manipulation
https://htmlpreview.github.io/?https://raw.githubusercontent.com/987153776/vue-picture-cut/master/dist/index.html



*********

npm install --save typeface-roboto
  
  in src/App.vue, add
  
  npm install --save-dev node-sass sass-loader

  <style lang="sass">
    @import '../node_modules/typeface-roboto/index.css'
  </style>

  
  npm install nipplejs --save
  
  npm run serve

  cd vue3-sidebar-master/

  npm install vue
  
  cd /bin
  
   export PATH="~/anaconda3/bin":$PATH
  
  conda create --name anaconda_ws

  
  conda init bash
  
  conda activate anaconda_ws

  
  pip install nodeenv

// eslint-disable-next-line
  
  https://ldwgwffnschmdt.github.io/vue-ros3djs/Ros3dViewer.vue.html
  
  nodeenv env

  
  . env/bin/activate
  
  npm install bootstrap --save
  
  npm install bootstrap-vue --save
  
  npm install @syncfusion/ej2-vue-layouts --save
  
  yarn add @fortawesome/fontawesome-free

/home/ram/anaconda3/envs/anaconda_ws

add router first and then vuetify
npm install vue-round-slider --save
npm install vue-slider-component --save
npm install --save @jzolago/vuetify-number-input
npm install vue-custom-scrollbar --save
npm install vue-scroll-snap --save
npm install vue-horizontal-scroll --save
npm install roslib --save
npm install git://github.com/RobotWebTools/roslibjs#develop --save
npm install --save vue-ros3djs
npm i vue-iframes
npm i -S vue-status-indicator

rosrun tf2_web_republisher tf2_web_republisher
livehttp

post definition in postman
https://www.postman.com/postman/workspace/postman-public-workspace/api/f00b3236-8241-43ce-925f-80f6f73f8ffc?version=26b1363e-2b53-4ec3-85b2-21ae480c86fe&tab=define

to fix the block origin
https://gist.github.com/razor-x/9542707 

killport
https://stackoverflow.com/questions/19071512/socket-error-errno-48-address-already-in-use
add this function in bashrc
function killport {
   kill -9 `lsof -i tcp:"$1" | grep LISTEN | awk '{print $2}'`
}
and use killport 9090


pip install nodeenv
nodeenv env
. env/bin/activate
conda init bash
conda activate anaconda_ws
npm install -g @vue/cli


##### python alternatives

https://www.itsupportwale.com/blog/how-to-upgrade-to-python-3-7-on-ubuntu-18-10/


##### ROS camera parameters #####

config: 
  bools: []
  ints: 
    - 
      name: "exposure_auto_tol"
      value: 5
    - 
      name: "exposure_auto_max"
      value: 50000
    - 
      name: "exposure_auto_min"
      value: 41
    - 
      name: "exposure_auto_outliers"
      value: 0
    - 
      name: "exposure_auto_rate"
      value: 100
    - 
      name: "exposure_auto_target"
      value: 50
    - 
      name: "gain_auto_tol"
      value: 5
    - 
      name: "gain_auto_outliers"
      value: 0
    - 
      name: "gain_auto_rate"
      value: 100
    - 
      name: "gain_auto_target"
      value: 50
    - 
      name: "whitebalance_auto_tol"
      value: 5
    - 
      name: "whitebalance_auto_rate"
      value: 100
    - 
      name: "binning_x"
      value: 1
    - 
      name: "binning_y"
      value: 1
    - 
      name: "decimation_x"
      value: 1
    - 
      name: "decimation_y"
      value: 1
    - 
      name: "width"
      value: 2452
    - 
      name: "height"
      value: 2056
    - 
      name: "roi_width"
      value: 0
    - 
      name: "roi_height"
      value: 0
    - 
      name: "roi_offset_x"
      value: 0
    - 
      name: "roi_offset_y"
      value: 0
    - 
      name: "stream_bytes_per_second"
      value: 45000000
    - 
      name: "iris_auto_target"
      value: 50
    - 
      name: "iris_video_level_min"
      value: 110
    - 
      name: "iris_video_level_max"
      value: 110
  strs: 
    - 
      name: "frame_id"
      value: "left_optical"
    - 
      name: "trig_timestamp_topic"
      value: ''
    - 
      name: "acquisition_mode"
      value: "Continuous"
    - 
      name: "trigger_source"
      value: "FixedRate"
    - 
      name: "trigger_mode"
      value: "On"
    - 
      name: "trigger_selector"
      value: "FrameStart"
    - 
      name: "trigger_activation"
      value: "RisingEdge"
    - 
      name: "exposure_auto"
      value: "Off"
    - 
      name: "exposure_auto_alg"
      value: "FitRange"
    - 
      name: "gain_auto"
      value: "Off"
    - 
      name: "balance_ratio_selector"
      value: "Red"
    - 
      name: "whitebalance_auto"
      value: "Off"
    - 
      name: "pixel_format"
      value: "Mono8"
    - 
      name: "ptp_mode"
      value: "Off"
    - 
      name: "sync_in_selector"
      value: "SyncIn1"
    - 
      name: "sync_out_polarity"
      value: "Normal"
    - 
      name: "sync_out_selector"
      value: "SyncOut1"
    - 
      name: "sync_out_source"
      value: "GPO"
    - 
      name: "iris_mode"
      value: "Continuous"
  doubles: 
    - 
      name: "acquisition_rate"
      value: 8.0
    - 
      name: "trigger_delay"
      value: 0.0
    - 
      name: "exposure"
      value: 500.0
    - 
      name: "gain"
      value: 20.0
    - 
      name: "gain_auto_max"
      value: 32.0
    - 
      name: "gain_auto_min"
      value: 0.0
    - 
      name: "balance_ratio_abs"
      value: 1.0
  groups: 
    - 
      name: "Default"
      state: True
      id: 0
      parent: 0
https://www.hamzamerzic.info/ikfast_generator/






