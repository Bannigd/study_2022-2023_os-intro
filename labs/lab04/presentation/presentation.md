---
## Front matter
lang: ru-RU
title: "Лабораторная работа №4. Основы интерфейса взаимодействия пользователя с системой Unix на уровне командной строки"
subtitle: "Дисциплина: Операционные системы"
author:
  - Стариков Д. А., cтудент НПИбд-02-22
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 4 марта 2023


## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
 
## Pandoc-crossref customization

figureTitle: ""
 
---

# Вводная часть

## Цели и задачи

- Приобрести практичекие навыки взаимодействия пользователя с системой посредством командной строки

# Выполнение лабораторной работы

## Выполнение лабораторной работы

![Полный путь домашнего каталога.](./image/image01.png){#fig:fig01 width=20%}

![Содержимое каталога tmp с ключом -l.](./image/image02.png){#fig:fig02 width=55%}

![Содержимое каталога tmp с ключом -a.](./image/image03.png){#fig:fig03 width=55%}

## Выполнение лабораторной работы

![Создание и удаление каталогов.](./image/image06.png){#fig:fig06 width=70%}

![Удаление каталогов.](./image/image07.png){#fig:fig07 width=70%}

## Выполнение лабораторной работы

![Фрагмент вывода команды ls -R.](./image/image08.png){#fig:fig08 width=65%}

![Фрагмент вывода команды ls -ctl.](./image/image09.png){#fig:fig09 width=50%}

## Получение справки по командам cd, pwd, mkdir и rmdir

:::::::::::::: {.columns align=center}
::: {.column}

![Справочная информация о команде cd.](./image/image091.png){#fig:fig091 width=110%}

![Справочная информация о команде pwd.](./image/image092.png){#fig:fig092 height=40%}

:::
::: {.column}

![Справочная информация о команде mkdir.](./image/image093.png){#fig:fig093 width=70%}

![Справочная информация о команде rmdir.](./image/image094.png){#fig:fig094 width=70%}

:::
::::::::::::::


## Работа с `history`

:::::::::::::: {.columns align=center}
::: {.column}


![Часть выводы команды history.](./image/image-history.png){#fig:fig-history}

:::
::: {.column}

![Пример №1 модификации команды из буфера обмена.](./image/image10.png){#fig:fig10 width=75%}

:::
::::::::::::::

# Выводы

- Получили практические навыки работы с командной строкой
- Познакомились с командой получения справочной информации `man`
