# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure


Step1: Initiate the MobileRobot.

Step2: Connect your PC with the MobileRobot.

Step3: Open Python program.

Step4: Program the movements of the robot using python code.

Step5: Execute the python program.

## Program
```python
# Developed by : Karthikeyan R
Register no    : 212222240045

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=2.9, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=100,b=255,)
    
    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,)
    
    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=139,g=0,b=0,)
    
    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=165,g=42,b=42,)


    ep_chassis.move(x=0, y=0, z=75, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=124,g=252,b=0,)

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,)

    ep_chassis.move(x=0, y=0, z=-50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,)

    ep_chassis.move(x=1.3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,)

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=255,g=255,b=255,)


    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=230,g=230,b=250,)

    ep_chassis.move(x=0, y=0, z=35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=139,g=0,b=139,)

    ep_chassis.move(x=0.2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=255,g=204,b=204,)

    ep_chassis.move(x=0, y=0, z=65, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=255,g=255,b=0,)

    ep_chassis.move(x=2.2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=204,g=0,b=102,)


    ep_chassis.move(x=0, y=0, z=90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=204,g=0,b=204,)

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all", r=204,g=0,b=102,)




    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here

![image](https://github.com/karthikeyan-R16/mobilerobot-openloopcontrol/assets/119421232/81af0720-ecb6-49a3-9456-8d3e6536b4fd)


![image](https://github.com/karthikeyan-R16/mobilerobot-openloopcontrol/assets/119421232/051bab9d-13fe-4030-b8a3-1df1e8e936f8)


![image](https://github.com/karthikeyan-R16/mobilerobot-openloopcontrol/assets/119421232/026f70d8-95ef-4696-ad1f-88f29f24821d)

<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here
https://youtu.be/kxpzwlBn9SE


<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
