---
## Front matter
title: "Отчет по лабораторной работе №7."
subtitle: "Командная оболочка Midnight Commander"
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

Освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.

# Выполнение лабораторной работы

## Заданиe по mc

1. Изучили информацию о mc, вызвав в командной строке `man mc` (Рис. [-@fig:fig01]).

![Man по команде mc.](image/image01.png){#fig:fig01}

2. Запустили из командной строки `mc`, изучите его структуру и меню (Рис. [-@fig:fig02]).

![Рабочее пространство mc.](image/image02.png){#fig:fig02}

3. Выполнили несколько операций в `mc`, используя управляющие клавиши (операции с панелями; выделение/отмена выделения файлов, копирование/перемещение файлов, получение информации о размере и правах доступа на файлы и/или каталоги и т.п.) (Рис. [-@fig:fig03], [-@fig:fig031]):

![Получение информации о правах доступа к файлу.](image/image03.png){#fig:fig03}

![Выделение нескольких файлов.](image/image031.png){#fig:fig031}

4. Выполнили основные команды меню левой (или правой) панели (Рис. [-@fig:fig32]).

![Команда меню "Левая панель".](image/image32.png){#fig:fig32}

5. Используя возможности подменю ***Файл***, выполнили:

- просмотр содержимого текстового файла (Рис. [-@fig:fig05]);

![Просмотр содержимого файла.](image/image05.png){#fig:fig05}

- редактирование содержимого текстового файла (без сохранения результатов редактирования) (Рис. [-@fig:fig06]);

![Редактирование файла.](image/image06.png){#fig:fig06}

- создание каталога (Рис. [-@fig:fig07]);

![Создание каталога.](image/image07.png){#fig:fig07}

- копирование в файлов в созданный каталог (Рис. [-@fig:fig08]).

![Копирование файла в созданный каталог.](image/image08.png){#fig:fig08}

6. С помощью соответствующих средств подменю ***Команда*** осуществили:

- поиск в файловой системе файла с заданными условиями (имя файла: `*.md`, нутри содержит: `Стариков`) (Рис. [-@fig:fig09] и [-@fig:fig10]);

![Меню "поиск файла".](image/image09.png){#fig:fig09}

![Найденные файлы.](image/image10.png){#fig:fig10}

- выбор и повторение одной из предыдущих команд (Рис. [-@fig:fig11]); 

![Список ранее использованных команд.](image/image11.png){#fig:fig11}

- переход в домашний каталог (Рис. [-@fig:fig12]);

![Дерево каталогов.](image/image12.png){#fig:fig12}

- анализ файла меню и файла расширений (Рис. [-@fig:fig13] и [-@fig:fig14]).

![Файл настройки меню.](image/image13.png){#fig:fig13}

![Файл настройки расширений.](image/image14.png){#fig:fig14}

7. Вызвали подменю ***Настройки*** и освоили операции, определяющие структуру экрана `mc` (Full screen, Double Width, Show Hidden Files и т.д.) (Рис. [-@fig:fig15], [-@fig:fig16], [-@fig:fig17]).

![Подменю настройки.](image/image15.png){#fig:fig15}

![Параметры конфигурации.](image/image16.png){#fig:fig16}

![Настройка панели.](image/image17.png){#fig:fig17}

## Задание по встроенному редактору mc

1. Создали текстовой файл `text.txt` (Рис. [-@fig:fig18]).

2. Открыли этот файл с помощью встроенного в `mc` редактора (Рис. [-@fig:fig18]).

![Новый файл text.txt.](image/image18.png){#fig:fig18}

3. Вставили в открытый файл небольшой фрагмент текста, скопированный из любого другого файла или Интернета (Рис. [-@fig:fig19]).

![В файл вставлен фрагмент текста.](image/image19.png){#fig:fig19}

4. Проделали с текстом следующие манипуляции, используя горячие клавиши:

- Удалили строку текста (Рис. [-@fig:fig20]).

![Удалена одна строка.](image/image20.png){#fig:fig20}

- Выделили фрагмент текста и скопировали его на новую строку (Рис. [-@fig:fig21]).

![Копирование выделенного фрагмента на новую строку.](image/image21.png){#fig:fig21}

- Выделили фрагмент текста и перенесли его на новую строку (Рис. [-@fig:fig211]).

![Перенос выделенного фрагмента на новую строку.](image/image211.png){#fig:fig211}

- Сохранили файл.

- Отменили последнее действие (Рис. [-@fig:fig22]).

![Отмена последнего действия (копирование выделенного фрагмента).](image/image22.png){#fig:fig22}

- Перешли в конец файла и написали некоторый текст (Рис. [-@fig:fig23]).

- Перешли в начало файла (нажав комбинацию клавиш) и напишите некоторый текст (Рис. [-@fig:fig23]).

![Добавление текста в начало и конец файла.](image/image23.png){#fig:fig23}

- Сохранили и закрыли файл.

5. Открыли файл с исходным текстом на языке программирования `asm` (Рис. [-@fig:fig24]).

6. Используя меню редактора, включили подсветку синтаксиса (Рис. [-@fig:fig24]).

![Подсветка синтаксиса в редактора mcedit.](image/image24.png){#fig:fig24}

# Выводы

В рамках лабораторной работы получили практические навыки работы с оболочкой Midnight Commander и его встроенным текстовым редактором.
