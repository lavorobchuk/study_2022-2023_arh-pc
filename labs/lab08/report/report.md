---
## Front matter
title: "Лабораторная работа No8"
subtitle: "Команды
безусловного и условного переходов в
Nasm. Программирование ветвлений"
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

Изучение команд условного и безусловного переходов. Приобретение навыков написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга.

# Выполнение лабораторной работы

1. Создаю каталог ‘lab08’ с помощью команды mkdir, перехожу в него с помощью команды cd и создаем в нем файл ‘lab8-1.asm’ с помощью команды
touch (рис. [-@fig:001])

![Создание каталогов и файлов](image/1.png){ #fig:001 width=70% }

2. Открываю файл ‘lab8-1.asm’ и ввожу листинг 8.1 (рис. [-@fig:002])

![Ввод листинга 8.1](image/2.png){ #fig:002 width=70% }

Создаем исполняемый файл и запускаем его (рис. 2.3). Программа выводит правильный результат, значит, она написана корректно. (рис. [-@fig:003])

![Запуск программы из файла](image/3.png){ #fig:003 width=70% }

Снова открываю файл ‘lab8-1.asm’ и редактирую его так, чтобы она выводила сначала ‘Сообщение No2’, а потом ‘Сообщение No1 (рис. [-@fig:004])

![Ввод изменений в программу из файла](image/4.png){ #fig:004 width=70% }

Создаю исполняемый файл и запускаю его. Программа выводит правильный результат, значит, она написана корректно (рис. [-@fig:005])

![Запуск измененной программы из файла](image/5.png){ #fig:005 width=70% }

Далее редактирую файл ‘lab8-1.asm’ так, чтобы сообщения выводились в обратной последовательности: ‘Сообщение No3’, ‘Сообщение No2’, ‘Сообщение No1 (рис. [-@fig:006])

![Повторный ввод изменений в программу из файла](image/6.png){ #fig:006 width=70% }

Создаю исполняемый файл и запускаю его (рис. [-@fig:007])

![Запуск повторно измененной программы из файла](image/7.png){ #fig:007 width=70% }

3. Создаю файл ‘lab8-2.asm’ с помощью команды
Создаю исполняемый файл и запускаю его. (рис. [-@fig:008])

![Ввод листинга 8.3](image/8.png){ #fig:008 width=70% }

Проверяю работу программы, вводя несколько чисел - программа выводит правильный результат,значит, она написана корректно (рис. [-@fig:009])

![Запуск программы из файла ‘lab8-2.asm](image/9.png){ #fig:009 width=70% }

4. Открываем файл листинга с помощью редактора mcedit (рис. [-@fig:010])

![Листинг программы из файла ‘lab8-2.asm’](image/10.png){ #fig:010 width=70% }

5. Открываю файл ‘lab8-2.asm’ и убираю у команды ‘cmp’ второй операнд (рис. [-@fig:011])

![изменение файла](image/11.png){ #fig:011 width=70% }

Выполняю трансляцию с получением файла листинга . Программа выводит ошибку, при этом файл листинга создается. Если открыть его, мы увидим,
что в файле листинга также обозначена ошибка отсутствия одного операнда (рис. [-@fig:012])

![ошибка](image/12.png){ #fig:012 width=70% }

# Cамостоятельная работа

1. Значения a, b и с для первого задания, согласно таблице, 45, 67 и 15. Значит, программа должна выводить число 15 (рис. [-@fig:013])
Создаю файл ‘proper.asm’ и пишу в нем программу для вывода наименьшего числа (рис. [-@fig:014])

![Создание файла](image/13.png){ #fig:013 width=70% }

![Ввод программы в файл proper.asm](image/14.png){ #fig:014 width=70% }

Создаю исполняемый файл и запускаю его. Программа выводит правильный результат, значит, она написана корректно. (рис. [-@fig:015])

![Запуск программы из файла](image/15.png){ #fig:015 width=70% }

2. Создаю файл ‘boo.asm’ и ввожу в него программу. Проверяю его работу (рис. [-@fig:016])

![Запуск программы из файла boo.asm](image/16.png){ #fig:016 width=70% }

# Выводы

В ходе выполнения данной лабораторной работы я изучила команды условного и безусловного переходов, приобрела навы-
ки написания программ с использованием переходов, ознакомилась с назначе-
нием и структурой файла листинга.
