---
## Front matter
title: "ОТЧЕТ
ПО ЛАБОРАТОРНОЙ РАБОТЕ №3"
subtitle: «Система контроля версий Git»
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

изучить идеологию и применение средств контроля версий.
Приобрести практические навыки по работе с системой git.

# Выполнение лаборатнорной работы

1. Настройка Github. Создаю учётную запись на сайте https://github.com/ и
заполняю основные данные.
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 13-59-07.png
2. Базовая настройка git. Делаю предварительную конфигурацию git. Ввожу в
терминале команды, указав имя и email владельца репозитория. Настраиваю
utf-8 в выводе сообщений. Задаю имя начальной ветки. 
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-16-10.png
3. Создание SSH-ключа. Генерирую пару ключей (приватный и открытый).
Далее загружаю сгенерированный открытый ключ. Для этого захожу на сайт
http://github.org/ под своей учётной записью и перехожу в меню Setting .
После этого выбираю в боковом меню SSH and GPG keys и нажимаю кнопку
New SSH key. Скопировав из локальной консоли ключ в буфер обмена,
вставляю его в появившееся на сайте поле и указываю для ключа имя (Title).
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-37-27.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-37-59.png
4. Создание рабочего пространства и репозитория курса на основе
шаблона. Открываю терминал и создаю каталог для предмета «Архитектура
компьютера»
5. Создание репозитория курса на основе шаблона. Перехожу на станицу репозитория с шаблоном курса
https://github.com/yam adharma/course-directory-student-template. Далее
выбираю Use this template.
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-40-15.png
6. В открывшемся окне задаю имя репозитория (Repository name) study_2022–
2023_arh-pc и создаю репозиторий https://github.com/lavorobchuk/study_2022-
2023_arh-pc.git
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-42-26.png
7. Открываю терминал, перехожу в каталог курса: cd ~/work/study/2022-
2023/"Архитектура компьютера" и клонирую созданный репозиторий
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 14-47-26.png
8. Ссылку для клонирования копирую на странице созданного репозитория Code
-> SSH
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-03-23.png
9. Настройка каталога курса. Перехожу в каталог курса, удаляю лишние файлы,
создаю необходимые каталоги, отправляю файлы на сервер
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-02-59.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-02-47.png
Проверяю правильность создания иерархии рабочего пространства в локальном
репозитории и на странице github.
# Cамостоятельная работа
1. Этот отчёт помещаю в соответствующий каталог рабочего пространства
(labs>lab03>report)
2. Копирую отчеты по выполнению предыдущих лабораторных работ в
соответствующие каталоги созданного рабочего пространства и загружаю файлы
на github.
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-06-16.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-06-32.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-10-29.png
/afs/.dk.sci.pfu.edu.ru/home/l/a/lavorobchuk/work/study/2022-2023/Архитектура компьютера/arch-pc/labs/lab03/report/image/Снимок экрана от 2022-10-14 15-10-45.png
# Вывод 
В ходе выполнения данной лабораторной работы я научилась работать с
системой Git, изучила идеологию и применение средств контроля версий.
