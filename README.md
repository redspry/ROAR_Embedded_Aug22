# ROAR_Embedded
Embedded code running on the ROAR ESP32 chip



# **BLE+ SPEED**



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

**![img](https://lh5.googleusercontent.com/dcrItysA1vCB6Iapmp6_PBJhu6NvvBAXSvNjNpGJssOE8nlkeJqoGUzb9J-H1B12KUlEaa6eNVd659nKJt3QlCjM7mfoNhfW7uORjk9QfNa0EOeBMfYUritU-SZuXs6gznB4-OUdo-R7sAyQpZQMnJ8)**

![img](https://lh6.googleusercontent.com/njinFGkUZ2gwNYP3cuehx0bRftz-hjR6sz2ISShLw0CAqdu-L8EysXXKZDxesquedApwhP9_kJv5qYvhK6vCs8egicrhNo0bZGJZ4WEQJzMyHEIz97ECLfaS28RzrAKS78nSkxiZyTPtcvf-nqZmO3g)

![img](https://lh4.googleusercontent.com/HA22wGCiAjM_qIMw_REF8ghlSEZF7CGKrmHgqx6XwFEz9oLuA7dTX8RJTKDouO7J5RwS_Rw5gKQfQJynggVnIwaALP376alYo5vo6d2YBqjykvgjNeCsGv23VNWUIiY_bNagYFxZA8Dl8ArRNvjIpVU)



##### Notes: 

It is *highly recommended* to use **PlatformIO** an IDE and dependency manager along with **Visual Studio Code** to Work on this project and properly manage dependencies. You can follow a Quick Start Installation Guide Here: 

https://docs.platformio.org/en/latest/integration/ide/vscode.html

If you are new to PlatformIO or Arduino programming. For more resources and Tutorials see this helpful youtube tutorial playlist for **ESP32** using **PlatformIO** 

https://youtube.com/playlist?list=PLzvRQMJ9HDiQ3OIuBWCEW6yE0S0LUpWhGU

After opening the project in **Visual Studio Code** with **PlatformIO** 





#### **Step2: BUILD** 

you should see a **SUCCESS** message

![img](https://lh3.googleusercontent.com/dpNPNo2XW5Wsh1Jsj71V33ftfUXOBfgr2g_8gbWZA5mSceZQFjtGHgFC-kq_GLuEgwHrjkPBgpNoB6_57uo_hjd5EEMGELZHU7nNPkEeHCudwNTE1_Le0w1wruHBQGxFeJhH_crXYf400EvBkTcKHG8)



#### **Step3: UPLOAD**

When you see Connecting … in the terminal output

Hold Down the **RST** Button on the **ESP32-CAM-MB**

Post upload you should see **SUCCESS** 

![img](https://lh3.googleusercontent.com/xiaFQpvozDrDD9NB8HvBt_gh9e73hPXZz7cUCpWQeHWgnTwJ0szl-Lxam_ekuSTbUky_WYouPT42-vFpSard0wZDFpJhCB7Q_sArxVMIPG-t8QBICVZ6aAV7O8i31vFMfKjG_26wa8kkcw4r-GTddPA)







## **APPENDIX**

**Close up of Custom Intelligent Racing Board designed by @BerkeleyCurtis with pin connectors soldered and antenna connected, for the CAD model of this PCB reach out to Adam Curtis**

**![img](https://lh5.googleusercontent.com/4VaHHM4LpXi8djfWLC6MyRubIU_zFWfTSYiFNbiQGY65l_MRYnFKqkCJpFJSFFlkMLTNkZa7JBxJVZqwtfdyB18km08pVYeA_CpWGPCvAPzPXRPxBA-Tg1iD1fkWCMOjBPH25RwVR5975E8Ot5SdMUc)**





