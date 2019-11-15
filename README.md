# Chip_Resetter
Chip Resetter for Ricoh, Samsung and Xerox

Представляю на ваше обозрение обнулятор чипов сделаный на Arduino UNO для картриджей Ricoh, Samsung и Xerox которые основанные на чипе (AT24CXX и его аналога 5ME3).

Цель была простая, получить обнулятор не дорогой и быстро собираемый.

Состоит он из:

1.	Arduino UNO
2.	LCD (1602) Keypad DFrobot
3.	2 резистора на 10 кОм
4.	4 зажима (крокодила)
5.	Лист бумаги формата а4 для создания кейса в котором он будет лежать (по желанию)

Сборка:

1.	Соединяем Arduino UNO и LCD (1602) Keypad DFrobot
2.	Припаиваем провода и резисторы согласно схеме (фото схемы в папке Scheme)
3.  Прошиваем его скетчем (скетч в папке Sketch)
4.	По желанию можете распечатать кейс если надо (шаблон открыть через LibreOffice Draw)

Прошивка/обновление обнулятора:

1.	Устанавливаем Arduino IDE 
2.	Устанавливаем библиотеки в Arduino IDE (инструкция в папке Library)
3.	Открываем sketch и заливаем его в Arduino UNO

Как пользоваться обнулятором:

0.  Подключаем чип.
1.	Выбираем нужный чип кнопками влево (LEFT) или вправо (RIGHT).
2.	Нажать кнопку вверх (UP), пойдет процесс обнуления чипа.
3.	Дождаться окончания процесса, обычно около 2х секунд в зависимости от прошиваемого чипа.
4.  Чип обнулился!

Дополнительные возможности:

1. Кнопка вниз (DOWN) показывает построчно по 16 байт из подключенного чипа, нужна для самопроверки обнуленного чипа.
2. Программная защита от короткого замыкания, питание на чип подается только при обнуление чипа.
3. В правом верхнем углу показывается распиновка чипа G (ground), V (vcc), D (data), C (clock)
4. По копке SELECT запускаются подпрограммы:
* Показывает сколько отпечатал страниц картридж Richo SP 100, 111, 150
* Прошивка чипа с отсчетом времени. Это удобно когда нужно держать картридж и чип обеими руками.
* Чтение дампа (128 байт) с чипа и вывод его на монитор порта (ctrl + shift + M) arduino ide. 
   Нужно для снятие новых (и не только) дампов с чипа. Чтобы не использовать другие программаторы (ол инклюзив)   
* Чтение дампа (256 байт) 
* Чтение дампа (512 байт) 


Инструкция по кнопке SELECT:
1) Нажимаем на кнопку SELECT и выбираем подпрограмму.
2) Как выбрали подпрограмму (точнее остановились на ней), надо подождать 3 секунды и повторно нажать на кнопку SELECT.
3) Все, подпрограмма выполнилась. Сразу может не получится, надо немного попрактиковаться.

Какие чипы поддерживает обнулятор?
- Ricoh SP 100 (SP 101E) (407059)
- Ricoh SP 111 (SP 110E)
- Ricoh SP 150 (408010)
- Ricoh SP 200HL 2.6K (407262) for Ricoh SP SP200/202/203/210/212 
- Ricoh SP 201HE 2.6K (111135) for Ricoh SP201/204/211/213/220
- Ricoh Aficio SP С220 С221 С222 С240 (406144, 406145, 406146, 406147)
- Ricoh Aficio SP C250/C260 (407543/407544/407545/407546) for Ricoh SP C250/C260
- Ricoh Aficio SP C252 (407716,407717,407718,407719)
- Ricoh SP 277 на 2.6K (408160) for Ricoh SP 277
- Ricoh SP 300 1.5K (406956) for Ricoh SP 300DN
- Ricoh SP С310 6K (406482, 122728, 406479, 122700) 
- Ricoh SP 311HE 3.5K (407246) for Ricoh SP 311/325  
- Ricoh SP 311UXE 6.4K (821242) for Ricoh SP 311/325 
- Ricoh SP 330N 7k (408283) for Ricoh SP 330SN
- Ricoh SP 400/450 5k (408061)
- Ricoh SP 3400HE 5K (406522) for Ricoh SP3400/3410/3500/3510
- Ricoh SP 3500XE 6.4K (406990) для Ricoh SP3500/3510  
- Ricoh SP 4500HE 12K (407318) for Ricoh SP3600/3610/4510  
- Samsung SCX 4200 (автоматическая смена номера CRUM)
- Xerox PE 220 (автоматическая смена номера CRUM)
- Xerox WC 3119 (автоматическая смена номера CRUM)
- Xerox WC 4118 (автоматическая смена номера CRUM)

Новые дампы будут появляться по мере появления у меня их. 
Дампы чипов (желательно новые) для Ricoh можно отправлять мне на email GalavarezMan@yandex.ru

Фото обнулятора:

<img src="https://github.com/Galavarez/Chip_Resetter/blob/master/Photos%20of%20the%20device/IMG_20171012_154550.jpg" width="400" height="300"/>
