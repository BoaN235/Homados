# Homados

**Total Time: 6h**

Homados is a diy bone conduncting headphones.

btw only Tier 2 highway project

## Goals
- design a pair of headphones that work
- use a pcb for controll
- design kind of like the openMoveShokz prob gonna be bulkier tho bc I am stupid 
- decent sound quality
- make it out of 3d printed materials like tpu and petg (bc I have a lot)
- have a mic
- what is inside it ( I am not confident I can even do any of this)
  - Transducer (this is the vibrating thingy)
  - Battery/Battery charging (this holds the power and adds more power)
  - Bluetooth/audo proccesing (this is what connects to your device and procces audio data)
  - control (the stuff that lets you turn it on/off or pause whatever you are listing to)
   

## Parts
2x $9 [Bone Conductor Transducer](https://www.adafruit.com/product/1674)
![image =100x20](https://github.com/user-attachments/assets/da4ee40c-9477-4df4-a603-699cd772bdd5)
# TimeStamps
## 6/1/25
**Time: 2h**

Today I actually get to know what I am doing. for refrence I don't know how headphones work so I should be fineeeeeee. The PCB scares me. Idk how to make bluetooth but I can learn how to make smt for audio proccesing and solder on a bluetooth capable board.

Idea:
- what if I build a custom esp32 board but also build in all the aduio componets so one side is electronics adn the other side is battery and controll

Usefull Recoures:
- [esp32](https://www.instructables.com/Build-Custom-ESP32-Boards-From-Scratch-the-Complet/)

Design rn:

![image](https://github.com/user-attachments/assets/6af40c00-6c52-4318-9141-3cb27f87cc4b)

## 6/2/25
**Time: 4h**



I have found out more things I need on the pcb
- ESP32-S3
- external audio codec (idk wut this is yet) ES8388
- external PMIC (Power Management integrated circut)

| Part                        | Purpose                        | Model Suggestion                |
| --------------------------- | ------------------------------ | ------------------------------- |
| **ESP32-S3**                | Main processor + Bluetooth     | ESP32-S3-WROOM-1                |
| **ES8388 Audio Codec**      | Audio I/O (DAC + ADC)          | ES8388                          |
| **Class-D Amp**             | Drives bone-conduction speaker | TPA2016D2, TPA3110              |
| **Mic**                     | Voice input                    | MAX9814                         |
| **Battery**                 | Power supply                   | 3.7V Li-ion, 500–1000 mAh       |
| **Charger + regulator**     | Power management               |                                 |


Usefull Recoures:
- [firmware maybe](https://github.com/espressif/esp-adf)
- [documentation for the aduio codec](https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8588881966884130816)

## 6/3/25-6/5/25
**Time: 2h**

I was working on getting an esp 32 working however now I was recomend a nrf52840 as a micro chip instead that is better at bluetooth

I found this could be usefull
[chip](https://www.amazon.com/FEASYCOM-QCC3024-Bluetooth-Analogue-certificated/dp/B09P1KBT1R/ref=sr_1_1?crid=YTJ1LJOLZBCK&dib=eyJ2IjoiMSJ9.q5R4eY0b_zg31FoP3KHEoLt_NgIi18yYPdU7yVwxmfM.vy3Ukh211L9wyJHB-zFAVqAV-oZc38_CDR6KyS1hU5k&dib_tag=se&keywords=QCC3040+TWS+Bluetooth+5.2+Audio+Module&qid=1749168789&s=electronics&sprefix=qcc3040+tws+bluetooth+5.2+audio+module%2Celectronics%2C69&sr=1-1-catcorr)

**Update:**
I am **Dumb** so turns out instead of spending hours learning electrical engineering I can just grab audio module with the stats I want and use it YAY

**Update 2:**
I am **Dumb** so turns out I am wrong if I want it to sound good I have to learn electrical enginnering 

**Time to decode this**

![81SGIfq+rrL _AC_SX679_](https://github.com/user-attachments/assets/18dfe54f-f882-417f-8d1f-cd7eb960c520)
