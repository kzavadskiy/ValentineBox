# ValentineBox
![Foto](https://lh3.googleusercontent.com/zsYO3oxreWbP0d8SufO2Wx7JvZOUeQSrICO7VNHVK3ys23LzPO-s1nXEhfPwgTgUEKrC0hyDTvxF-3sO7x4S691Ke4ylLM8sJr7Ne8aTJthsNc81nhdhf8s9GH9rGcMVUOiH3igOYbIzAw1fMrclcBwpNpQAblWZy3Pp3jSs_9DnBToHs1uo6fTz-AIRNu-RrJ0nZb0NPnOqqqM-jXApjLhGEe18rzNunjHX6rvrM716FCsjxgBd4wcOL-Q82-O2g551veDFHm2N5KnhMLesH9CYmf3Go1i8E3bzgY2C5IHdmumoO8b9YkOHT9US40BuKZbfNBFHyoc_ABPfHa2PqIHeCEgAUCnvThzJMrvcUVZymOkQ-wWGErG-WP66DnMGEeP5VIo0GXGXrYURLxGIZrFjkpGQwE8Nk8LzJYodQQEAzhR-DjLhvaolCp1HrztInszEYt0PBR52vZqhm6_2Bb5j1jNeTCPn-3WNWQwpf6b_xLfs42UliupfYjhPnJa9Q07ZrGpWQNWL8pqaxsAZiSYlMiSF4OmLW75r7MiRpJXZ78p0B2JRz8QZisCTSEYGZ8XqpAa69RcpPW_h9TXsvvmcvKtj-532DkzIrtIsLrX8AZba5SPQK8UfmIIXff3KJdMVq_Y2MjGIK7QzQl-eqOLZ6wSyHIpOxjMHekZvQl2rCAVRvoCGbjc3eJ9Y=w872-h654-no?authuser=0)

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
![Scheme](https://lh3.googleusercontent.com/C0eLP7MX9KyfVlWX35nVtFYSX55kJ22HcbiFyaYtI_rm8lAYkZcHnOkICZqad9HaUam8NfuwUAVjqO48W2DQj-pkv85jCPJvbpT7W6Qg7Tj8MSITcDHqRMryfY_eHac_YRIv-Oy2UQv7rWjDXUFiM2pz8owH3e5oUUHp43EFb9-rELdk0tUR5aUznW0FO6bk3Xf4zUbzvm6gz80FCR12D0iVVPZ9S0mLQWtqY-D7Rz6Jxdm_LJy-2X6DviY7h5zg7Ufg8VRsVBOf_RlrexeZ6CFodxbMEzfj3QHVB4Rd-JNQ0cNW8a6XPzg0Dzr9UXp4R4bLBzEI-or1UqK8Rfq00BRjKGWUr_F7Yv-cfARKgg-XfyJKodtBulrP_lng5N75rfd8PbF-XtHnvnIMbgkUh89tv78EtcRSo6A7w95w8sRs3pzlGHRdhIx60CF-0-8MBc1OARfK5GAa-nYwPc3Rh8_B_C-xkWGB8VMnPo3i3xfx0bUVaDRgTgSVPiXdALVXd0I_0_zvux0mIzDrGZg_mGnNjLCrmoyazkCnWaCzFjWjLBKS_u5P82TwE08QRg_qxIxuh1XaXOHJ_Oqk7WLCv4SorvL8ehwAgsGT_eDmSOqH0GpRP8I-xoaN0UCuTeBbyLtudAOUqkLv035ukw6jBNUV--kX1a0o2svUg4Ipn940jdMf9fFWFQ05Np-z=w857-h436-no?authuser=0)
Рисунок 1. Електрична схема ValentineBox

Контакти 5V, GND приєднати до відповідних проводів USB кабелю

## Прошивка
Для коректної роботи модулів у вас мають бути встановлені бібліотеки SevSeg, Wire, DS3231.

Перш за все необхідно налаштувати модуль реального часу. Після збираня схеми, необхідно залити прошивку [Setting time](https://github.com/kzavadskiy/ValentineBox/blob/master/Setting%20time) на Arduino nano з встановленою батарейкою в модулі DS3231.

Після цього можна заливати основну [прошивку](https://github.com/kzavadskiy/ValentineBox/blob/master/box_sketch) з від'єднаними провідниками SCA, SCL.

В змінній dateWeGotTogether необхідно записати вашу пам'ятну дату в форматі unixtime. Для цього використайте конвертер дати https://www.unixtimestamp.com/index.php

Після перевірки роботи можна збирати коробку, при вимкненому живленні модуль реального часу зберігає дату та час і після підключення до блоку живлення через USB кабель дата залишається актуальною.
ц
