# ESPhome Craft LVGL 800

**Dashboard for waveshare ESP32 S3 N8R8 LCD 7 and Guition ESP32 8048S070**

![image](https://github.com/user-attachments/assets/a9315adf-f3ac-48d0-a87d-aa4b253453d7)

![image](https://github.com/user-attachments/assets/54d7f8a8-cc59-44cc-ab97-02e12d13f987)

![image](https://github.com/user-attachments/assets/68d18ae2-5453-4abe-a373-b7e0da132d47)

![image](https://github.com/user-attachments/assets/ea657fff-211a-4112-9979-1a964433d5d1)

![image](https://github.com/user-attachments/assets/34740547-f88d-4b9b-9b19-857ff3caa894)


This is not for everyone, it's optimized for personal use, but a source I share to refer to.

I don't know any programming languages, and I made this as a hobby.

If someone asks why I have two, it's because I got frustrated with the touch issue on the Waveshare 7' product.

# waveshare ESP32 S3 N8R8 LCD 7 LCD Brightness Wire

it is necessary to adjust the backlight brightness, you can be adjusted by connecting the pin below and the remaining GPIO pin(ex:GPIO6) of ESP32 module.

![image](https://github.com/user-attachments/assets/2d22f57b-f7c4-4f2f-8bdc-42b48757c781)

I'm connecting this using GPIO6

# Sample Video

[https://www.youtube.com/shorts/WfNRwrhKC6Q?feature=share](https://www.youtube.com/shorts/sdezhiXci4w)

it's just sample. This is optimized for my home, and the public version is a bit simpler.

The code used for the device in this video is personalized and cannot be used by other users. The cool weather page and other menus are components that are only available in Korea and my Homea Assistant. If you want to use this, you need to be able to understand and modify ESPhome LVGL. If you can't, no matter how much you receive the yaml file, you can't use it.

If that is possible, you can modify the yaml file I released below to suit your country and your home assistant.

# Custom Entities

This YAML configuration needs key devices like climate, media player, blinds, energy meter, air quality sensors, illuminance, and presence sensor.

```
substitutions:
# Device setting  
  board: esp32-s3-devkitc-1
  name: "esphome-craft-800"
  comment: ESPhome Craft 800
  type: esp-idf  
  latitude: "37"    
  longitude: "126"   
  font: gfonts://Roboto
  mdi: fonts/materialdesignicons-webfont.ttf 
  # http://materialdesignicons.com/cdn/7.4.47/ 

# Device entities:
  climate: your_device_entity
  media_player: your_device_entity
  blind: your_device_entity
# indoor sensors
  temperature: your_sensor_entity
  humidity: your_sensor_entity
  pm2_5: your_sensor_entity
  tvoc: your_sensor_entity
  co2: your_sensor_entity
  illuminance: your_sensor_entity
  presence: your_sensor_entity
# energy entities:
  energy_meter: your_sensor_entity
  daily_meter: your_sensor_entity
  monthly: your_sensor_entity
  prev_monthly: your_sensor_entity

#font setting
  characters: " !#%'()+,-./0123456789:;<>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[]_abcdefghijklmnopqrstuvwxyz{|}°²³µ"

 #Radio channel, For Korea User, If you want to edit channel names. you can change the yaml
  kbscool: "http://yourip:3005/radio?keys=kbs_cool&token=homeassistant&atype=1"
  itv: "http://yourip:305/radio?keys=ifm&token=homeassistant&atype=1"
  mbcfm4u: "http://yourip:3005/radio?keys=mbc_fm4u&token=homeassistant&atype=1"
  KBSClassic: "http://yourip:3005/radio?keys=kbs_1radio&token=homeassistant&atype=1"
  CBSMusic: "http://yourip:3005/radio?keys=cbs_fm&token=homeassistant&atype=1"
  YTN: "http://yourip:3005/radio?keys=ytn&token=homeassistant&atype=1"
  TBS: "http://yourip:3005/radio?keys=tbsfm&token=homeassistant&atype=1"
  MBCFM: "http://yourip:3005/radio?keys=mbc_fm&token=homeassistant&atype=1"
  KBS1FM: "http://yourip:3005/radio?keys=kbs_1radio&token=homeassistant&atype=1"
  CBSFM: "http://yourip:3005/radio?keys=cbs_fm&token=homeassistant&atype=1"
  TBN: "http://yourip:3005/radio?keys=tbnfm&token=homeassistant&atype=1"
  SBSLoveFM: "http://yourip:3005/radio?keys=mbc_fm&token=homeassistant&atype=1"
  EBSFM: "http://yourip:3005/radio?keys=ebsfm&token=homeassistant&atype=1"
  KBS3FM: "http://yourip:3005/radio?keys=kbs_3radio&token=homeassistant&atype=1"
  KBSHappyFM: "http://yourip:3005/radio?keys=kbs_happy&token=homeassistant&atype=1"
  SBSPowerFM: "http://yourip:3005/radio?keys=sbs_power&token=homeassistant&atype=1"
```

## 후원
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/plplaaa2)
