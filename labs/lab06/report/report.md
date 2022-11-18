---
## Front matter
title: ". Лабораторная работа №6"
subtitle: "Основы работы с
Midnight Commander (mc). Структура
программы на языке ассемблера NASM.
Системные вызовы в ОС GNU Linux"
author: "Воробчук лилия Андреевна"

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

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.

# Выполнение лабораторной работы

1. Открываю Midnight Commander (рис. [-@fig:001]) 

![mc](image/1.png){ #fig:001 width=70% }

2. Перехожу в каталог ~/work/arch-pc, созданный при выполнении лабораторной работы №5 (рис. [-@fig:002]) 

![переход в каталог](image/2.png){ #fig:002 width=70% }

3. Нажимаю клавишу f7 и создаю каталог с именем lab06

4. C помощью команды touch создаю в этом каталоге файл lab6-1.asm (рис. [-@fig:003]) 

 ![создание файла](image/3.png){ #fig:003 width=70% }
 
5. Клавишей f4 открываю созданный файл

6. Ввожу текст программы из листинга, сохраняю изменения и закрываю файл. (рис. [-@fig:004]) 

![Ввод листинга программы](image/4.png){ #fig:004 width=70% }

7. С помощью клавиши F3 открываю файл lab6-1.asm и убеждаюсь, что файл содержит текст программы

8. Транслирую текст программы lab6-1.asm в объектный файл. Выполняю компоновку объектного файла и запускаю получившийся исполняемый
файл. На запрос программы ввожу мои ФИО. (рис. [-@fig:005]) 

![исполнение программы](image/5.png){ #fig:005 width=70% }

9. Скачиваю файл in_out.asm со страницы курса в ТУИС. 

10. Копирую файл in_out.asm в каталог с файлом lab6-1.asm
с помощью клавиши F5 ( (рис. [-@fig:006]) 

![копирование файла](image/6.png){ #fig:006 width=70% }

11. . С помощью функциональной клавиши F6 создаю копию файла lab6-
1.asm с именем lab6-2.asm. (рис. [-@fig:007]) 

![создание копии файла](image/7.png){ #fig:007 width=70% }

12. Исправляю текст программы в файле lab6-2.asm в соответствии с листингом (рис. [-@fig:008]) 

![новый текст](image/8.png){ #fig:008 width=70% }

 Создаю исполняемый файл и проверяю его работу (рис. [-@fig:009]) 
 
 ![исполнение программы](image/9.png){ #fig:009 width=70% }

13. В файле lab6-2.asm заменяю подпрограмму sprintLF на sprint. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:010]) 

![изменение подпрограммы](image/10.png){ #fig:010 width=70% }

sprint выводит сообщение на экран, а sprintLF добавляет к этому переход на новую строку.


# Самостоятельная работа

1. Создаю копию файла lab6-1.asm. Вношу изменения в программу (рис. [-@fig:011]) 

![копирование lab6-1.asm с именем lab6-3.asm](image/11.png){ #fig:011 width=70% }

Вношу изменения в программу (рис. [-@fig:012]) 

![измененная программа](image/12.png){ #fig:012 width=70% }

2. Получаю исполняемый файл и проверяю его работу. На приглашение
ввести строку ввожу свои ФИО. (рис. [-@fig:013]) 

![исполнение программы](image/13.png){ #fig:013 width=70% }

3. Создаю копию файла lab6-2.asm с именем lab6-4.asm (рис. [-@fig:014]) 

![копирование файла](image/14.png){ #fig:014 width=70% }

В тексте программы перед командой завершения вводжу mov eax, buf1 call sprint

Исполнение программы (рис. [-@fig:015]) 

![исполнение](image/15.png){ #fig:015 width=70% } 

# Выводы

В ходе выполнения данной лабораторной работы мной были приобретены практические навыки работы в Midnight Commander, а также освоены инструкции языка ассемблера mov и int.

