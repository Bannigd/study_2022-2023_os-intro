---
## Front matter
title: "Отчет по лабораторной работе №3"
subtitle: "Markdown"
author: "Данила Андреевич Стариков"

## Generic options
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

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.

# Задание

Сделать отчет по лабораторной работе №2 в формате Markdown, предоставить в отчет в 3 форматах: `pdf`, `docx`, `md`.

# Выполнение лабораторной работы

Для преобразования файла формата `md` необходимо скачать ПО: утилиту `pandoc` и подходящую ей версию `pandoc-crossref`, дистрибутив `TeX Live` (Рисунок [-@fig:fig01]).

![Установленные версии pandoc, pandoc-crossref и TeX Live.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab03/report/image/image01.png){#fig:fig01}

Редактирование отчета по лабораторной работе №2 проводили в программе `gedit` (Рисунок [-@fig:fig02]). 

![Рабочее окно редактора gedit.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab03/report/image/image02.png){#fig:fig02}

Для конвертации файла формата `md` в `pdf` и `docx`, в каталоге курса `/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab03/report/` хранится файл `Makefile` ([Листинг 1](#lst1)). Введя в консоли команду `make` из файла `report.md` генерируются  файлы `report.pdf` и `report.docx` (Рисунок [-@fig:fig03]).

![Использование команды make.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab03/report/image/image03.png){#fig:fig03}

[Листинг 1. Программа Makefile.]{#lst1}
```{.makefile .numberLines }
FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

FILTERS =
OPTIONS =
PDF_ENGINE =
PDF_OPTIONS =
FORMAT_OPTIONS =

### Cross references
## Use pandoc-xnos (https://github.com/tomduck/pandoc-xnos)
## Local pandoc-xnos
FILTERS += --filter pandoc/filters/pandoc_fignos.py \
	--filter pandoc/filters/pandoc_eqnos.py \
	--filter pandoc/filters/pandoc_tablenos.py \
	--filter pandoc/filters/pandoc_secnos.py
## System-wide pandoc-xnos
# FILTERS += --filter pandoc-fignos --filter pandoc-eqnos \
	--filter pandoc-tablenos --filter pandoc-secnos
## Use pandoc-crossref (https://github.com/lierdakil/pandoc-crossref)
# FILTERS += --filter pandoc-crossref
###
PDF_ENGINE += --pdf-engine=lualatex --pdf-engine-opt=--shell-escape
OPTIONS += --number-sections
BIB_OPTIONS = --citeproc


%.docx: %.md
	-pandoc "$<" $(FILTERS) $(OPTIONS) $(BIB_OPTIONS) -o "$@"

%.pdf: %.md
	-pandoc "$<" $(FILTERS) $(PDF_ENGINE) $(PDF_OPTIONS) \
	$(BIB_OPTIONS) $(FORMAT_OPTIONS) $(OPTIONS) -o "$@"

all: $(FILES)


clean:
	-rm $(FILES) *~

cleanall: clean
```

Все изображения, использованные в отчете, хранятся в отдельном каталоге `/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab02/report/image`.

По выполнении работы, все изменения загружены на Github.

# Выводы

В рамках лабораторной работы познакомились с языком разметки Markdown, научились конвертировать файлы `md` в `pdf` и `docx`, пользуясь утилитами `pandoc`, `pandoc-crossref` и дистрибутивом `TeX Live`.
