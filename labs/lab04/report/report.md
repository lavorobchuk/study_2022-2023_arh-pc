---
## Front matter
title: "ОТЧЕТ
ПО ЛАБОРАТОРНОЙ РАБОТЕ №4"
subtitle: "Язык разметки
Markdown"
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

освоение процедуры оформления отчетов с помощью
легковесного языка разметки Markdown.

# Задание

Изучить синтаксис markdown, освоить основные команды

# Теоретическое введение

Чтобы создать заголовок, используйте знак #, например:
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
Чтобы задать для текста полужирное начертание, заключите его в двойные
звездочки:
This text is **bold**.
Чтобы задать для текста курсивное начертание, заключите его в одинарные
звездочки:
This text is *italic*.
Чтобы задать для текста полужирное и курсивное начертание, заключите его
в тройные звездочки:
This is text is both ***bold and italic***.
Блоки цитирования создаются с помощью символа >:
> The drought had lasted now for ten million years, and the reign of
the terrible lizards had long since ended. Here on the Equator,
in the continent which would one day be known as Africa, the
battle for existence had reached a new climax of ferocity, and
the victor was not yet in sight. In this barren and desiccated
land, only the small or the swift or the fierce could flourish,
or even hope to survive.
↪
↪
↪/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-24-02.png
↪
↪
↪
Упорядоченный список можно отформатировать с помощью соответствующих цифр:
1. First instruction
1. Sub-instruction
1. Sub-instruction
1. Second instruction
Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка:
1. First instruction
1. Second instruction
1. Third instruction
Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире:
* List item 1
* List item 2
* List item 3

Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка:
- List item 1
- List item A
- List item B
- List item 2

# Выполнение лаборатнорной работы

1. Открываю терминал, перехожу в каталог курса, сформированный при выполнении лабораторной работы №3 и обновляю локальный репозиторий, скачав изменения из удаленного репозитория с помощью команды git pull
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-21-13.png
2. Перехожу в каталог с шаблоном отчета по лабораторной работе № 4,провожу компиляцию шаблона с использованием Makefile. Для этого ввожу команду make и генерирую файлы report.pdf и
report.docx. Открываю и проверяю корректность полученных файлов.
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-20-45.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-20-22.png
3. Удаляю полученный файлы с использованием Makefile.Для этого ввожу команду make clean
Проверяю, что после этой команды файлы report.pdf и report.docx были удалены.
file:///afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/%D0%90%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%B0/arch-pc/labs/lab04/report/image/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-10-20%2011-23-37.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-24-02.png
4. Открываю файл report.md c помощью любого текстового редактора gedit. Внимательно изучаю структуру этого файла.
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab04/report/image/Снимок экрана от 2022-10-20 11-25-19.png
5. Заполняю отчет и компилирую отчет с использованием Makefile. Проверяю корректность полученных файлов.
6. Загружаю файлы на Github.
# Вывод 
В ходе выполнения данной лабораторной мной был изучен синтаксис markdown, освоены процедуры оформления отчетов с помощью
легковесного языка разметки Markdown.Изучить синтаксис markdown.😊️
