# shutter-check-canon

This guide is written in 2 languages for your convinience: Engligh and Russian.  
Данная статья написана на 2 языках для вашего удобства: на английском и на русском.  
[English version](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/README.md#english-version)  
[Русская версия](https://github.com/fedoroff-aa/shutter-check-canon#%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%B0%D1%8F-%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F)

# English version
Here you can see a tutorial how you can check **shutter count** and **history of happend errors** on Canon cameras. It is useful for people who buy or sell used Canon cameras and want to be patient about them. You can do it quickly (15 minutes) with my guide for free. Another way is to pay capitalists if you have much money and think it's okay to pay to check your camera's state only once or twice (and probably there won't be displayed errors history) ;)

## Prerequisites
Suitable models for check using such a way are all Canon EOS R-series mirrorless cameras (maybe it works for DSLR cameras too, I haven't tried it yet).
Or to be more accurate here is a list:
- Canon EOS R,
- Canon EOS Ra,
- Canon EOS RP,
- Canon EOS R3,
- Canon EOS R5,
- Canon EOS R5C,
- Canon EOS R6,
- Canon EOS R6 Mark II,
- Canon EOS R8,
- Canon EOS R7,
- Canon EOS R10


I have tried this method on my Canon R6.

## Preparing
To read the guide and prepare you need about 10 minutes. You also need a PC with Windows.  
**Algorithm:**  
1. Find or buy ~~or steal~~ SDHC Card (SDXC is not suitable), whose capacity is equal to or lower than 32 GB.
2. Prepare your SD Card using [this article](https://chdk.fandom.com/wiki/EOScard#[_http://pel.hu/down/EOScard.exe_]). For your convinience I downloaded the [EOScard.exe](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/EOScard.exe) tool, so you can do it even if the site goes down.
3. Download [extend.m](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/extend.m) and [script.req](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/script.req) to your PC and copy them to the root of prepared SD Card.

## Check your camera's condition (including shutter count)
For this procedure you need 5 minutes.  
**Algorithm:**  
1. Insert prepared SD Card to your camera (battery also must be in body).
2. Turn on the camera.
3. Press "Play" button (it is usually used to see taken pictures, placed on the right side and looks like triangle in a rectangle) on the camera.
4. Press "SET" button (it is usually used to confirm changes when yo have a dialog window) several times.
5. Turn off the camera, remove the SD Card.

Well done! In the root of the SD Card you can see a new file with the name like "CAM_INFO.XML". This is what you need. You should copy this file to your PC and open it, for example in Chrome browser (it's good because the formatting is pretty good than in Notepad)

## Interpretation of results
As a result you have opened "CAM_INFO.XML" file in browser (I strongly recommend Chrome or Edge) or editor. You can see XML markup with different tags. I think that tags are pretty "obvious" but I don't like when such words are written in articles, that's why I will explain some of the tags.

### Tags (not all but most important, maybe I will add more tags):
- \<TotalShutter\> \- the main number (and the reason why you read this tutorial), which displays shutter count, or in other words how many actuations shutter has made since the release from the conveyor (that's why brand new camera may have 10-100 shots, it's being tested by Canon for quality control)
- \<TotalRunningTime\> \- the number, which displays how many seconds camera have been turned on.
- \<ErrorList\> \- the list of errors which happened to camera.
  Typyical errors (for more info please use google, universal advice) inside \<Kind\>\<ID\> tag:
  - E01 \- problems with lens connection (different reasons, maybe poor connection between lens and body, maybe aperture in lens can't be controlled due to broken ribbon cable inside it)
  - E02 \- problems with SD Card
  - E20 \- problems with shutter or mirror or other mechanisms inside camera (dangerous error, you should pay attention to it if this error occurred more than once, also good practice is to go to the service, where qualified specialists can check camera's health)
  - E70 \- problems with overheating (it's not a dangerous error but keep in mind that going to service while buying an expensive thing is a good practice)

Also you can see the example files: [CAMERA_INFO (good).XML](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/CAM_INFO%20(good).XML) from perfect brand new camera and [CAMERA_INFO (bad).XML](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/CAM_INFO%20(bad).XML) from bad camera with problems (my opinion - it's not recommended to buy it or know the risks and be ready for surprises)

## Epilog


# Русская версия
В данной статье вы можете ознакомиться с материалом о том, как проверить **пробег (количество срабатываний затвора)** и **историю возникновения ошибок** на камерах Canon. Это можно сделать быстро (~15 минут) и бесплатно, хотя есть и другой путь - заплатить капиталистам, если у вас много денег и вы считаете, что отдавать деньги за проверку состояния вашей камеры нормально. Данная инструкция полезна для людей, которые покупают или продают подержанные фотоаппараты Canon.

## Предварительные условия
Для проверки подходят все камеры линейки Canon EOS R (возможно, этот способ работает и для зеркальных камер, я еще не пробовал).
Или, если быть более точным, вот список:
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

Я попробовал данный способ на своей камере Canon R6.

## Подготовка
Для прочтения руководства и подготовки вам понадобится около 10 минут. Вам также нужен компьютер с Windows.  
**Алгоритм:**
1. Найдите или купите ~~или украдите~~ Карту SDHC (SDXC не подходит), емкость которой меньше или равна 32 ГБ.
2. Подготовьте эту SD-карту, используя [эту статью](https://chdk.fandom.com/wiki/EOScard#[_http://pel.hu/down/EOScard.exe_]). Для вашего удобства я скачал [EOScard.exe](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/EOScard.exe), так что вы можете сделать это, даже если указанный сайт упадёт.
3. Скачайте [extend.m](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/extend.m) и [script.req](https://github.com/fedoroff-aa/shutter-check-canon/blob/main/script.req) на ваш компьютер и скопируйте их в корень подготовленной SD-карты.

## Проверьте состояние вашей камеры (включая количество срабатываний затвора)
На эту процедуру вам понадобится 5 минут.  
**Алгоритм:**
1. Вставьте подготовленную SD-карту в камеру (аккумулятор также должен быть в камере).
2. Включите камеру.
3. Нажмите на кнопку "Play" (обычно она используется для просмотра сделанных снимков, расположена с правой стороны и выглядит как треугольник внутри прямоугольника) на фотокамере.
4. Несколько раз нажмите на кнопку "SET" (обычно она используется для подтверждения изменений, когда у вас есть диалоговое окно) несколько раз.
5. Выключите фотокамеру, извлеките SD-карту.

Ура, вы молодцы и справились! В корневом каталоге SD-карты вы можете увидеть новый файл с названием "CAM_INFO.XML". Это то, что вам нужно. Вам необходимо скопировать этот файл на свой компьютер и открыть его, например, в браузере Chrome (т.к. там форматирование довольно приятное и лучше, чем в блокноте).

## Интерпретация результатов
В итоге вы открыли файл "CAM_INFO.XML" в браузере (я настоятельно рекомендую Chrome или Edge) или редакторе. Вы можете увидеть XML-разметку с различными тегами. Я думаю, что теги довольно "очевидны", но мне не нравится, когда такие слова пишут в статьях (особенно когда неочевидно), поэтому я объясню некоторые из тегов.

### Теги (не все, но наиболее важные есть, возможно дополню позже):
- \<TotalShutter\> \- основное число (и причина, по которой вы читаете это руководство), которое отображает пробег затвора, или, другими словами, сколько срабатываний затвора произошло с момента выпуска с конвейера (кстати у совершенно новой камеры может быть 10-100 снимков, она тестируется Canon для контроля качества)
- \<TotalRunningTime\> \- число, которое показывает общее время работы камеры в секундах.
- \<ErrorList\> \- список ошибок, которые произошли с камерой.
Типичные ошибки (для получения дополнительной информации, пожалуйста, используйте Google, универсальный совет) внутри тега \<Kind\>\<ID\>:
  - E01 \- проблемы с подключением объектива (разные причины, возможно, плохое соединение между объективом и байонетом или же диафрагмой в объективе невозможно управлять из-за обрыва шлейфа внутри него)
  - E02 \- проблемы с SD-картой
  - E20 \- проблемы со шторкой, зеркалом или другими механизмами внутри камеры (это опасная ошибка, вам следует обратить внимание, если у проверяемой камеры произошло несколько таких ошибок, также рекомендуется обратиться в сервисный центр, где квалифицированные специалисты могут проверить исправность камеры)
  - E70 \- проблемы с перегревом (это не критичная ошибка, но имейте в виду, что лучше обратиться в сервисный центр при покупке дорогой техники для диагностики)

## Эпилог
