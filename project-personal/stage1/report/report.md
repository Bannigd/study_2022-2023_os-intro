---
## Front matter
title: "Персональный сайт научного работника. Этап 1"
subtitle: "Дисциплина: Операционные системы"
author: "Стариков Данила Андреевич"

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

Разместить на Github pages заготовки для персонального сайта.

# Выполнение лабораторной работы

## Установить необходимое программное обеспечение.

Для создания персонального сайта воспользовались генератором статических сайтов [Hugo](https://github.com/gohugoio/hugo/releases), скачали последнюю версию hugo\_extended\_0.110.0\_Linux-64bit.tar.gz. (Рис. [-@fig:fig01])

![Релизы Hugo.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image01.png){#fig:fig01}

Также для работы с Hugo необходимо установить компилятор языка программирования Go, это можно сделать в консоли по команде `sudo dnf install go` (Рис. [-@fig:fig02]).

![Установка компилятора Go.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image02.png){#fig:fig02}

Скачанный архив Hugo распаковали (Рис. [-@fig:fig03]), исполняемый файл внутри переместили в каталог `/usr/bin/` (Рис. [-@fig:fig04]), что дает возможность вызывать его в консоли по команде `hugo`, без необходимсти указывать полный путь к файлу.

![Распакованный архив Hugo.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image03.png){#fig:fig03}

![Перенос исполняемого файла Hugo в /usr/bin.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image04.png){#fig:fig04}

## Создание репозитория по шаблону сайта

Скопировали репозиторий [шаблона](https://github.com/wowchemy/starter-hugo-academic) персонального сайта (Рис. [-@fig:fig05]), создали каталог `/work/blog` и клонировали созданный репозиторий (Рис. [-@fig:fig06]).

![Создание репозитория по шаблону.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image05.png){#fig:fig05}

![Клонирование созданного репозитория.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image06.png){#fig:fig06}

Перешли в каталог `blog` и запустили команду `hugo server`, который создал сайт на локальном сервере (Рис. [-@fig:fig07]).

![Запуск локального сервера сайта.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image07.png){#fig:fig07}

## Разместить заготовку сайта на Github pages.

Создали новый репозиторий на Github с названием `Bannigd.github.io`, который будет использоваться как персональный сайт. Также клонировали его в каталоге `work`, создали главную ветку командой `git checkout -b main` и добавили пустой файл `README.md` (Рис. [-@fig:fig08])

![Клонирование репозитория Bannigd.github.io и его настройка.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image08.png){#fig:fig08}

Вернулись в каталог `blog` и изменили файл `.gitignore`, закомментировав строку public/, чтобы эта папка загружалась в репозиторий (Рис. [-@fig:fig09]).

![Изменение файла .gitignore.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image09.png){#fig:fig09}


В каталоге `blog` сделали копию репозитория `Bannigd.github.io` с названием `public` (Рис. [-@fig:fig10]), что все изменения между ними будут синхронизироваться. 

![Создание каталога public.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image10.png){#fig:fig10}

Запустили команду `hugo`, чтобы сгенерировать сайт в папке public (Рис. [-@fig:fig11]). Затем коммитим изменения (Рис. [-@fig:fig12]) и проверяем работоспособность сайта (Рис. [-@fig:fig13]).

![Генерация сайта.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image11.png){#fig:fig11}

![Коммит изменений в репозиторий.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image12.png){#fig:fig12}

![Сайт размещен на Github Pages.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/project-personal/stage1/report/image/image13.png){#fig:fig13}

# Выводы

В рамках первого этапа персонального проекта разместили заготовку для персонального сайта на Github Pages с помощью генератора статических сайто `Hugo`.
