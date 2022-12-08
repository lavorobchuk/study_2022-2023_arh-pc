---
## Front matter
title: "Лабораторная работа №9"
subtitle: "Программирование цикла. Обработка
аргументов командной строки."
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

Приобретение навыков написания программ с использованием циклов и
обработкой аргументов командной строки.

# Выполнение лабораторной работы

1. Создаю каталог для программам лабораторной работы №9, перехожу в него и создаю файл lab9-1.asm (рис. [-@fig:001])

![создание файла](image/1.png){ #fig:001 width=70% }

2.  Ввожу в файл lab9-1.asm текст программы из листинга 9.1. (рис. [-@fig:002])

![ввод листинга](image/2.png){ #fig:002 width=70% }

3. Создаю исполняемый файл и проверяю его работу. (рис. [-@fig:003])

![запуск](image/3.png){ #fig:003 width=70% }

4. Меняю текст программы lab9-1, добавив изменение значение регистра ecx в цикле. В данном случае число проходов цикла соответстует значению N введенному с клавиатуры
 (рис. [-@fig:004])

![изменненая программа](image/4.png){ #fig:004 width=70% }

5. Создаю исполняемый файл и проверяю его работу. (рис. [-@fig:005])

![запуск](image/5.png){ #fig:005 width=70% }

6. Вношу изменения в текст программы, добавив команды push и pop для сохранения значения счетчика цикла loop. В данном случае число проходов цикла не соответстует значению N введенному с клавиатуры (рис. [-@fig:006])

![внесение изменений](image/7.png){ #fig:006 width=70% }

7. Создаю исполняемый файл и запускаю его (рис. [-@fig:007])

![исполнение файла](image/6.png){ #fig:007 width=70% }

8. Создаю файл lab9-2.asm в каталоге и ввожу в него текст программы из листинга 9.2.(рис. [-@fig:008])

![создание файла](image/8.png){ #fig:008 width=70% }

9. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:009])

![запуск](image/9.png){ #fig:009 width=70% }
 
10. Создаю файл lab9-3.asm и ввожу в него текст программы из листинга 9.3 (рис. [-@fig:010])

![ввод листинга](image/10.png){ #fig:010 width=70% }

11. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:011])

![исполнение](image/11.png){ #fig:011 width=70% }

12. Изменяю текст программы из листинга 9.3 для вычисления произведения аргументов командной строки (рис. [-@fig:012])

![измененный текст программы](image/12.png){ #fig:012 width=70% }

13. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:013]) 

![запуск](image/13.png){ #fig:013 width=70% }


# Самостоятельная работа

1. Пишу программу, которая находит сумму значений функции f(x)= 4x+3 (рис. [-@fig:014])

![программа для функции](image/14.png){ #fig:014 width=70% }

2. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:015])

![запуск](image/15.png){ #fig:015 width=70% }

# Выводы

В ходе выполнения данной лабораторной работы я приобрела навыки написания программ с использованием циклов и
обработкой аргументов командной строки.

