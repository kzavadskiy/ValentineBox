# ValentineBox
![Foto](https://raw.githubusercontent.com/kzavadskiy/ValentineBox/master/IMG_20200523_154603.jpg)

Даний невеликий проект дозволить вам подарувати гарний настрій та здивує вашу половинку не тільки на день Валентина, але й в інші важливі для вас дати.

Проект створено за ідеєю Vegard Paulsen, посилання [тут](https://vegardpaulsen.wordpress.com/valentineduino/)

Перелік необхіндих компонентів:
* Arduino Nano ~3 usd
* RTC module DS3231 with 2032 battery ~1,4 usd
* 4 digits, 3-segment дисплей ~1,8 usd
* резистори 220 Ом, 6 штук <1 usd
* монтажний провід
* старий USB кабель
* будь яка коробочка
* інструменти

Електричну схему можна зібрати згідно рисунку 1 навісним монтажем чи на монтажній платі. Можна як спаяти провідники, так і використати монтажні провідники, бажано на модулі DS3231 приєднати контакти SCA, SCL через монтажні провідники, з можливістю зручного роз'єднання.
![Scheme](https://raw.githubusercontent.com/kzavadskiy/ValentineBox/master/Schematic_Valentine%20Box.png)
Рисунок 1. Електрична схема ValentineBox

Контакти 5V, GND приєднати до відповідних проводів USB кабелю

## Прошивка
Для коректної роботи модулів у вас мають бути встановлені бібліотеки SevSeg, Wire, DS3231.

Перш за все необхідно налаштувати модуль реального часу. Після збираня схеми, необхідно залити прошивку [Setting time](https://github.com/kzavadskiy/ValentineBox/blob/master/Setting%20time) на Arduino nano з встановленою батарейкою в модулі DS3231.

Після цього можна заливати основну [прошивку](https://github.com/kzavadskiy/ValentineBox/blob/master/box_sketch) з від'єднаними провідниками SCA, SCL.

В змінній dateWeGotTogether необхідно записати вашу пам'ятну дату в форматі unixtime. Для цього використайте конвертер дати https://www.unixtimestamp.com/index.php

Після перевірки роботи можна збирати коробку, при вимкненому живленні модуль реального часу зберігає дату та час і після підключення до блоку живлення через USB кабель дата залишається актуальною.

