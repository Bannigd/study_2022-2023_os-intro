---
## Front matter
title: "Отчет по Персональному проекту. Этап 3"
subtitle: "Добавление достижений"
author: "Данила Андреевич Стариков"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: false # List of figures
lot: false # List of tables
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

Добавить к сайту данные о себе.

- Список добавляемых данных:

* Список достижений
   * Добавить информацию о навыках (Skills).
   * Добавить информацию об опыте (Experience).
* Сделать пост по прошедшей неделе.
* Добавить пост на тему по выбору: языки разметки. LaTeX.

# Выполнение лабораторной работы

1. Добавили информацию о навыках (Skills) (Рис. [-@fig:fig01])

![Скриншот информации о навыках](image/image01.png){#fig:fig01}

2. Добавить информацию об опыте (Experience). (Рис. [-@fig:fig02])

![Скриншот информации об опыте](image/image02.png){#fig:fig02}

3. Сделать пост по прошедшей неделе. (Рис. [-@fig:fig03])

![Скриншот поста о прошедей неделе.](image/image03.png){#fig:fig03}

4. Добавить пост на тему по выбору: языки разметки. LaTeX. (Рис. [-@fig:fig04])

![Скриншот поста на тему по выбору.](image/image04.png){#fig:fig04}

# Выводы

В рамках третьего этапа персонального проекта на сайт добавлены информация о навыках, опыте, и написаны 2 поста.

