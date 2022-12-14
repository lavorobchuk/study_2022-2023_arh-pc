---
## Front matter
title: "Лабораторная работа №10"
subtitle: "Понятие подпрограммы. Отладчик GDB."
author: "Воробчук Лилия Андреевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение навыков написания программ с использованием подпрограмм. Знакомство с методами отладки при помощи GDB и его основными возможностями.

# Выполнение лабораторной работы

1. Создаю каталог lab10 и файл lab10-1.asm (рис. [-@fig:001])

![создание файла](image/1.png){ #fig:001 width=70% }

2. Ввожу текст листинга (рис. [-@fig:002])

![листинг](image/3.png){ #fig:002 width=70% }

3. Запускаю программу (рис. [-@fig:003])

![создание файла](image/2.png){ #fig:003 width=70% }

4. Меняю текст программы, чтобы она решала выражение f(g(x)). (рис. [-@fig:004])
 
![внесение изменений](image/4.png){ #fig:004 width=70% }

5. Запускаю измененную программу (рис. [-@fig:005])

![запуск](image/5.png){ #fig:005 width=70% }

6. Создаю файл lab10-2.asm и вписываю туда Листинг 10.2(рис. [-@fig:006])

![ввод листинга](image/6.png){ #fig:006 width=70% }

7. Запускаю файл второй программы в отладчик gdb. (рис. [-@fig:007])

![отладчик](image/7.png){ #fig:007 width=70% }

8. Ставлю брекпоинт на метку _start и запускаю программу(рис. [-@fig:008])

![брекпоинт](image/8.png){ #fig:008 width=70% }

9. Просматриваю дисассимплированный код программы, начиная с метки.(рис. [-@fig:009])

![дисассимплированный код](image/9.png){ #fig:009 width=70% }

10. С помощью команды переключаюсь на intel’овское отображение синтаксиса. Отличие заключается в командах, в диссамилированном отображении в командах используют % и $, а в Intel отображение эти символы не используются. (рис. [-@fig:010])

![Intel’овское отображение](image/10.png){ #fig:010 width=70% }

11. Для удобства включаю режим псевдографики. (рис. [-@fig:011])

![режим псевдографики](image/11.png){ #fig:011 width=70% }

12. Посматриваю наличие меток и добавляю еще одну метку на предпоследнюю инструкцию. (рис. [-@fig:012])

![Наличие меток](image/12.png){ #fig:012 width=70% }

13. С помощью команды si посматриваю регистры и изменяю их (рис. [-@fig:013])

![просмотр регистров](image/13.png){ #fig:013 width=70% }

14. Смотрю значение второй переменной msg2. (рис. [-@fig:014])

![Просмотр значения переменной](image/15.png){ #fig:014 width=70% }

15. С помощью команды set меняю значение переменной msg1. (рис. [-@fig:015])

![Изменение значения переменной](image/14.png){ #fig:015 width=70% }

16. Меняю переменную msg2.(рис. [-@fig:016])

![Изменение msg2](image/16.png){ #fig:016 width=70% }

17. Вывожу  значение регистров ecx и eax (рис. [-@fig:017])

![Значение регистров ecx и eax](image/17.png){ #fig:017 width=70% }

18. Меняю значение регистра ebx. Команда выводит два разных значения так как в первый раз мы вносим значение 2, а во второй раз регистр равен двум, поэтому и значения разные. (рис. [-@fig:018])

![Значение регистров ebx](image/18.png){ #fig:018 width=70% }

19. Копирую файл lab9-2.asm и переименовываю его. Запускаю файл в отладчике и указываю аргументы.(рис. [-@fig:019])

![Запуск файла в отладчике](image/19.png){ #fig:019 width=70% }

20. Ставлю метку на _start и запускаю файл.(рис. [-@fig:020])

![Запуск файла lab10-3 через метку](image/20.png){ #fig:020 width=70% }

21. Проверяю адрес вершины стека и убеждаюсь, что там хранится 5 элементов.(рис. [-@fig:021])
 
![Адрес вершины стека](image/21.png){ #fig:021 width=70% }

22. Смотрю все позиции стека. По первому адрему хранится адрес, в остальных адресах хранятся элементы. Элементы расположены с интервалом в 4 единицы, так как стек может хранить до 4 байт, и для того чтобы данные сохранялись нормально и без помех, компьютер использует новый стек для новой информации. (рис. [-@fig:022])

![Все позиции стека](image/22.png){ #fig:022 width=70% }


# Самостоятельная работа

1. Преобразовываю программу из лабораторной работы №9 и реализовываю вычисления как подпрограмму.(рис. [-@fig:023])

![Текст программы](image/23.png){ #fig:023 width=70% }

2. Создаю исполняемый файл и проверяю его работу. (рис. [-@fig:024])

![Запуск программы](image/24.png){ #fig:024 width=70% }

3. Ввожу в файл Листинг 10.3 (рис. [-@fig:025])

![Текст програмы](image/25.png){ #fig:025 width=70% }

4. Запускаю программу и вижу, что результат вычисления неверный(рис. [-@fig:026])

![Запуск программы](image/26.png){ #fig:026 width=70% }

5. После появления ошибки запускаю программу в отладчике (рис. [-@fig:027])

![Запуск программы в отладчике](image/27.png){ #fig:027 width=70% }

6. Открываю регистры и, проанализировав их, понимаю, что некоторые регистры стоят не на своих местах и исправляю это (рис. [-@fig:028])

![Анализ регистров](image/28.png){ #fig:028 width=70% }

7. Изменяю регистры и запускаю программу, программа вывела ответ 25, то есть все работает правильно. (рис. [-@fig:029])

![Повторный запуск программы](image/29.png){ #fig:029 width=70% }


# Выводы

В ходе выполнения данной лабораторной работы я приобрела навыки написания программ с использованием подпрограмм, ознакомилась с методами отладки при помощи GDB и его основными возможностями.


