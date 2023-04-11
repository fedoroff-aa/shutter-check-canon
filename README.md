# shutter-check-canon

This guide is written in 2 languages for your convinience: Engligh and Russian.

# English version
Here you can see a tutorial how you can check **shutter count** and **history of happend errors** on Canon cameras. You can do it quickly (15 minutes) with my guide for free or pay capitalists if you have much money and think it's okay to pay to check your camera's state. It's useful for people who buy or sell used Canon cameras.

## Prerequisites
Suitable models for check using such a way are all Canon EOS R-series mirrorless cameras (maybe it works for DSLR cameras too, I haven't tried it yet).
Or to be more accurate here is a list:
- Canon EOS R,
- Canon EOS Ra,
- Canon EOS RP,
- Canon EOS R3,
- Canon EOS R5,
- Canon EOS R5 C,
- Canon EOS R6,
- Canon EOS R6 Mark II,
- Canon EOS R8,
- Canon EOS R7,
- Canon EOS R10

## Preparing
To read the guide and prepare you need about 10 minutes. You also need a PC with Windows.
Algorithm:
1. Find or buy ~~or steal~~ SDHC Card (SDXC is not suitable), whose capacity is equal to or lower than 32 GB.
2. Prepare your SD Card using [this article](https://chdk.fandom.com/wiki/EOScard#[_http://pel.hu/down/EOScard.exe_]). For your convinience I downloaded the [EOScard.exe](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/EOScard.exe) tool, so you can do this even if the site goes down.
3. Download [extend.m](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/extend.m) and [script.req](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/script.req) to your PC and copy them to the root of prepared SD Card.

## Check your camera's condition (including shutter count)
For this procedure you need 5 minutes.
Algorithm:
1. Insert prepared SD Card to your camera (battery also must be in body).
2. Turn on the camera.
3. Press "Play" button (it is usually used to see taken pictures, placed on the right side and looks like triangle in a rectangle) on the camera.
4. Press "SET" button (it is usually used to confirm changes when yo have a dialog window) several times.
5. Turn off the camera, remove the SD Card.

In the root of the SD Card you can see a new file with the name like "CAM_INFO.XML". This is what you need. You should copy this file to your PC and open it, for example in Chrome browser (it's good because the formatting is pretty good than in Notepad)

## Interpretation of results
As a result you have opened "CAM_INFO.XML" file in browser (I strongly recommend Chrome or Edge) or editor. You can see XML markup with different tags. I think that tags are pretty "obvious" but I don't like when such words are written in articles, that's why I will explain some of the tags.

### Tags:
- \<TotalShutter\> \- the main number (and the reason why you read this tutorial), which displays shutter count, or in other words how many actuations shutter has made since the release from the conveyor (that's why brand new camera may have 10-100 shots, it's being tested by Canon for quality control)
- \<TotalRunningTime\> \- the number, which displays how many milliseconds camera have been turned on.
- \<ErrorList\> \- the list of errors which happened to camera.
  Typyical errors (for more info please use google, universal advice) inside \<Kind\>\<ID\> tag:
  - E01 \- problems with lens connection (different reasons, maybe poor connection between lens and body, maybe aperture in lens can't be controlled due to broken ribbon cable inside it)
  - E02 \- problems with SD Card
  - E20 \- problems with shutter or mirror or other mechanisms inside camera (dangerous error, you should pay attention if used camera have such type of erorr and more than one case, also good practice is to go to the service, where qualified specialists can check camera's health)
  - E70 \- problems with overheating (it's not a dangerous error but keep in mind that going to service while buying an expensive thing is a good practice)

## Epilog


# Русская версия
To be continued...
