---
## Front matter
title: "ОТЧЕТ 
ПО ЛАБОРАТОРНОЙ РАБОТЕ №4"
subtitle: "дисциплина: Архитектура компьютера"
author: "Шурыгин Илья Максимович"

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

Научиться оформлять отчеты с помощью легковесного языка разметки Markdown.

# Задание

Необходимо разобраться с синтаксисом языка Markdown и оформить отчеты 3-ей и 4-ой лабораторных работ с помощью него.

# Выполнение лабораторной работы

1. Установим Tex Live. (рис. [-@fig:001])(рис. [-@fig:002])

![Установка Tex Live](image/img-1.jpg){ #fig:001 width=70% }

![Завершение установки](image/img-2.jpg){ #fig:002 width=70% }

2. Установка Pandoc и pandoc-crossref.(установил версию 2.19)(рис. [-@fig:003])

![Файлы лежат в нужном каталоге](image/img-3.jpg){ #fig:003 width=70% }

3.	Обновим локальный репозиторий с помощью команды git pull, затем проведем компиляцию шаблона с использованием Makefile при помощи команды make. Проверим сгенерированные файлы report.pdf и
report.docx.(рис. [-@fig:004])

![Генерируем файлы repotr.pdf и report.docx](image/img-4.jpg){ #fig:004 width=70% }

4. Откроем файл report.md c помощью текстового редактора gedit.(рис. [-@fig:005])

![Отчет в текстовом редакторе gedit](image/img-5.jpg){ #fig:005 width=70% }

5. Загрузим файлы с отчетами в трех форматах на Github.(рис. [-@fig:006])

![Загружаем файлы на Github](image/img-6.jpg){ #fig:006 width=70% }

# Задание для самостоятельной работы:

1. Создадим отчеты для 3-ей лабораторной работы в форматах pdf и docx при помощи команды make уже в каталоге labs/lab03. Загрузим их на Github(рис. [-@fig:007])

![](image/img-7.jpg){ #fig:007 width=70% }

2.	Проверим, что все файлы лежат в нужном каталоге на сайте.(рис. [-@fig:008])

![](image/img-8.png){ #fig:008 width=70% }

# Выводы

В данной лабораторной работе я научился оформлять отчеты с помощью языка разметки Markdown. Теперь все отчеты будут храниться сразу в 3-х форматах(md, pdf, docx).