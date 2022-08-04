# ROAR_Embedded
Embedded code running on the ROAR ESP32 chip



# **BLE + SPEED**



**Parts required:**

- Mini/Micro USB Wires supporting Data Transmission

- Jumper wires

- ESP32 Motherboard

- ROAR customized PCB Board

  

## **Procedure:**

Google Doc: https://docs.google.com/document/d/1D5ydaaLVN3bytds7K1XcLaF4Gcsg35xMvoRSOgNlM3k/edit?usp=sharing

1. **STEP1:  Connect all the jumper wires according to the below  config**
2. **STEP2:  Plugin the USB wire into the laptop and the ESP-32-CAM-MB boardOn Platform IO, make sure the code compiles before uploading**
3. **STEP3:  Upload, and when seeing “Connecting…..” in the terminal, press the RST on the ESP32-CAM-MB until the data is being transferred.**
4. **STEP4:  Boom, you’re done!**

*A side note: connect the 5V to the + of throttle/steering is fine, but connecting it to the halleffect sensor +/- may risk frying the chip.*



#### **STEP 1:** 

This code is designed to be used with a custom PCB made for ROAR and intelligent racing. The wiring diagram to flash the PCB is as follows: 

**![img](https://lh3.googleusercontent.com/aU4TQDzP-bojaJTe2CfjARyLG3KweRehD5vFrVFJ7orVl9VL9HCT3HJiBDLcRaB_Diyt_5PEOACz_JJo8E2utp4hUiUggCy6NqVJTcIH252vtcH5woq54lVgdhNA9_WW24DcpcXuCHvhC0-0BIMARpM)**

![img](https://lh4.googleusercontent.com/3XUM5a1xQRVB7GdZLTQaxb3XvHUKfL8oFjTsw2oO_frz2aOBjGtvIBcbhYa-0sCLBsb2t6IqMFptT9bvR5hTGbjtfm490HQ7wgB8zooCRIQ1uzs1X4xr5KM-jqUhItb-Yi7VANNF3h5ZHZ9CdzWh4qY)

![img](https://lh4.googleusercontent.com/xbjtEd9md5aTREAP5z-uRJJXMdOukie_iX5km4-D4KkWtb6obO-NEQwBy0xXRWU8oipFYLT2UDQDHEc-jgjEhtKiKF2TQb_WG2bOzRkfFkRw55uElsic21mfjuxPlRjeYfYblzTZvhycYTc7dxDG8n8)



##### Notes: 

It is *highly recommended* to use **PlatformIO** an IDE and dependency manager along with **Visual Studio Code** to Work on this project and properly manage dependencies. You can follow a Quick Start Installation Guide Here: 

https://docs.platformio.org/en/latest/integration/ide/vscode.html

If you are new to PlatformIO or Arduino programming. For more resources and Tutorials see this helpful youtube tutorial playlist for **ESP32** using **PlatformIO** 

https://youtube.com/playlist?list=PLzvRQMJ9HDiQ3OIuBWCEW6yE0S0LUpWhGU

After opening the project in **Visual Studio Code** with **PlatformIO** 





#### **Step2: BUILD** 

you should see a **SUCCESS** message

![img](https://lh3.googleusercontent.com/PKgQfaZR-yxZYoXrk1KfC5rPwwk9V4rSv-ngRhDM201XC5GSJA7es7_KPJDi835uCXDpj-STdf4qCrzsx-eCcUDcG3J_19XklJdNfsLatb8ayqMwitnvvjVwq32FGMPuU-w0vumQiiy7L96qE980cmQ)



#### **Step3: UPLOAD**

When you see Connecting … in the terminal output

Hold Down the **RST** Button on the **ESP32-CAM-MB**

Post upload you should see **SUCCESS** 

![img](https://lh3.googleusercontent.com/z8YwOJi5jL930u3Jxk7Uk58wpnjFb1fGWcSGzm2h_T_gvZ1ljZgi5hN9MpnejgxcJC_E9LCD2joxw1SpoakCotoE1Zv6IPcjzcLMZT6qskyFyU9qxw3-Lg1-KxF4GnOZYbUPHEvT1lh8Fr2scjHLkuI)







## **APPENDIX**

**Close up of Custom Intelligent Racing Board designed by @BerkeleyCurtis with pin connectors soldered and antenna connected, for the CAD model of this PCB reach out to Adam Curtis**

**![img](https://lh5.googleusercontent.com/_5CbmSSQPpEZKLFRav5T92qPVLagLOwAMwOBYiUagjT51CEtlnuzV4Ts3nJHJGXIHz-fRVB_UfKMB7NYNK84qxA1X8OOqfG1A8FtTtJO9gf-1IFhJs2QqZYod5TNcvEMOcOvd6aCYCLpbYWgO4wG8Os)**







# ROAR (Robotic Open Autonomous Racing) Project Overview

The ROAR Project uses Traxxas RC Cars, in conjunction with this Board and an iPhone iOS application.

This board designed by Adam Curtis @BerkeleyCurtis has onboard PID control and is to be used in conjunction with an iPhone Application developed by Michael Wu @Wuwuxiaohua1011. 

A new ROS2 based ROAR repo (*STAGE1*) is under development between Aman Saraf and Michael Wu. *ROS2 Tutorials: https://docs.ros.org/en/foxy/How-To-Guides.html , https://www.theconstructsim.com/*



## Components Required

1. **STAGE1 > PC:** ROAR Main Repo
2. **STAGE2 > iPhone**: custom iOS app 
3. **STAGE3 > ESP32 board** will perform localized PID control with kp, ki, kd inputs and optional wheel encoder compatibility. 
4. **STAGE4 > Traxas RC Car** ESP32 board plugs into the Traxxas 6519 TQ 2.4 GHz Micro Receiver (3CH), the system is compatible with multiple Traxxas Models

**![img](https://lh3.googleusercontent.com/uVoGiKUsqgr40434Kx9hCbRsBUWZtTNs4ff20S4dILfZvpnMF3arnsN92N4PJXCI09QCsOAtOgo_k2eVviRrh5OHbg3CYQOA3KTev-ZYvF60lele371ZTBpil8ylvzvYctMKG681ZWr0f_y0Ze4ko2c)**



### 1. ROAR MAIN REPO

download the codebase and any prompted dependencies, and choose a python agent to run i.e [runner_ios.py](https://github.com/wuxiaohua1011/ROAR/blob/main/runner_ios.py)

- [**ROAR MAIN**](https://github.com/amansrf/ros_roar_streamer) (ROS2 Based): check with Michael Wu to verify new iOS app compatibility. 

- **[ROAR MAIN](https://github.com/wuxiaohua1011/ROAR)** (Python Based): Stable Version 

- [<u>**ROAR Pinned**</u>](https://github.com/ROAR-FLOW/ROAR) (Python Based): *Older Pinned Stable ROAR Repo Compatible with Pinned Stable Version of iOS App that saves data locally on the iPhone*

  

### 2. ROAR iOS & ROAR_iOS_xcode

- [**ROAR iOS**](https://github.com/wuxiaohua1011/ROAR_iOS) (compatible with python based ROAR MAIN, unsure if compatibility has been updated for ROS2 check with Michael Wu to verify new iOS app compatibility. ): 

- **[ROAR iOS Pinned](https://github.com/ROAR-FLOW/ROAR-iOS)** *Older Pinned Stable Version of iOS App UI depicted below*

  **![img](https://lh4.googleusercontent.com/pRB3PmX_njtSBDUEAakYAQlcfMY38UKIL7Fq0uJtciLQpWhwc8b7EabzW4B1pU0ZiKyupc7JdH4udmb398VjrZhc6zlbNn7nEv3RuXxA6eXh6RYtp5WVCV5OkIXH2Nkobem00JnclPdZO7yzW9V7Wq8)**

  

### 3. ESP32 Repo

- [**ROAR_Embedded**](https://github.com/BerkeleyCurtis/ROAR_Embedded) authored by @BerkeleyCurtis 

- **[ROAR_Embedded_Sum22](https://github.com/redspry/ROAR_Embedded_Sum22)** (forked) recommended check UUID compatibility with app. Current boards are flashed from this Repo.

  The backplane (4x3 female connectors) of the custom ESP32 board plugs into the Traxxas 6519 TQ 2.4 GHz Micro Receiver (3CH), main motor as well as the servo for turning both plug into and are controlled by the ESP32 board which used BLE to communicate with the iOS app. 

  **![img](https://lh3.googleusercontent.com/kbovEJ9-SiMCQkNXlgYFODlLYw6I7oBi0RoBwvtbPxhU78a1kLZAW7s_2waaaPin82Lzy1gGLVYltQNKvLVcarmCaERUiTuys6_5_BXRrJ82bolkO0geeygkiSAiM3CB4C2m-ToUfOf-0yAUsYXnYO8)**



### 4. Traxxas Cars

The cars come in multiple models, they have front facing iPhone mounts, the ROAR system is compatible with multiple Traxxas Models. 



#### Most up to date model: 

**Pros:** offers better vibration damping to solve the [SLAM](https://www.andreasjakl.com/basics-of-ar-slam-simultaneous-localization-and-mapping/) noise issues, **Cons:** There is a plug-in on the ESP32 boards that allows for a Hall Effect sensor to be added, however there is not a good location to mount a hall effect sensor on the car for more precise velocity readings (transaxel inaccesssible), the hope is that the vibration damping will render SLAM through ARKit reliable enough without the need for an additional sensor. 

**![img](https://lh3.googleusercontent.com/nUinFWQly-vrpenJO8dpznNdauX3IsnpQLcr9-BnYkquR4QjG2_CCTK2ElUzD3ckl_QcmJuQKdzb9U9GUSdtNCpONuxH632zxpInXlb6QP1QyUEbCxTaRuD-a7TCW338e0NZtLK0iKhTYUQNctz3C0k)**



#### Prior Model: 

 **Pros:** There is a plug-in on the ESP32 boards that allows for a Hall Effect sensor to be added along the main metal transaxel to measure rotations of this axel and convert this RPM to the car's overall velocity. **Cons:** These Traxxas models have issues with Chassis vibration that causes problems with the iOS app's [SLAM](https://www.andreasjakl.com/basics-of-ar-slam-simultaneous-localization-and-mapping/) capabilities. The Phone vibrates too much and the picture quality is unstable. 

**![img](https://lh3.googleusercontent.com/L2wEyqcjGNGG5SQ0RUvfVG1yEdWqHcdfmoofjrXb1iwdYBJ_MU4MhurQ86zWzP-oOVjuMPyszmeCuHxpU-LN4jQxz_wQ3LULSuITEs36OSsMsT2Cml7MA3K1f5TiyS9fkvC__JaGI6AuIPksPhoU6l0)**