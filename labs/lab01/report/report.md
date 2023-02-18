---
## Front matter
title: "Лабораторная работа №1"
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

Целью  данной  работы  является  приобретение  практических  навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов. 

# Задание

1. Установка и настройка VirtualBox
2. Создание виртуальной машины
3. Установка операционной системы Linux Fedora
4. Установка программного обеспечения для создания документации
5. Домашнее задание

# Выполнение лабораторной работы

## Установка и настройка VirtualBox

1. Проверка  местоположения  каталога  для  виртуальных  машина  в  свойствах VirtualBox.

В верхней панели нажали «Файл» $\rightarrow$ «Настройки», вкладка «Общие». В поле «Папка для машин по умолчанию» указали папку на диске, куда будут происходить установка виртуальной машины (Рис. [-@fig:fig01]). 

![Вкладка «Общие» в найстроках VirtualBox.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image1.jpeg){#fig:fig01}

2. Смена комбинацию для хост-клавиши, которая используется для освобождения курсора мыши, который может захватить виртуальная машина. 

В  верхней  панели  нажали  «Файл»  $\rightarrow$  «Настройки»,  вкладка  «Ввод»  $\rightarrow$ «Виртуальная машина». Выдели поле «Хост-комбинация» и нажали одновременно клавиши «Ctrl» + «Alt», затем «Enter» для сохранения изменений (Рис. [-@fig:fig02]). 

![Вкладка «Ввод» в найстроках VirtualBox.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image2.jpeg){#fig:fig02}

## Создание виртуальной машины. 

При  создании  виртуальной  машины  в  качестве  операционной  системы выбрана Linux Fedora (64-bit). Дальнейшие шаги установки: 

- Выбрать объем оперативной памяти для виртуальной машины– 3000 Мб (Рис. [-@fig:fig03]), впоследствии объем оперативной памяти увеличен до 8192 Мб; 

![Меню выбора выделяемого объема оперативной памяти.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image3.png){#fig:fig03}

- Подключить виртуальный жесткий диск (Рис. [-@fig:fig04]). 

Выбранный диск «dastarikov.dvi» имеет следующие параметры (Рис. [-@fig:fig05]): тип – VDI (VirtualBox Disk Image), динамический формат хранения, размер диска – 16 Гб. Размер диска компьютера составляет всего 256 Гб, поэтому для виртуального выбран  размер  меньше  рекомендованного  заданием  (не  менее  80  Гб),  однако  в случае  нехватки  места  VirtualBox  поддерживает  увеличение  объема  уже  после создания виртуального диска.  

![Меню выбора виртуального жесткого диска для использования виртуальной машиной.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image4.png){#fig:fig04}

![Параметры виртуального диска «dastarikov.vdi».](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image5.jpeg){#fig:fig05}
 
После  установки  увеличили  доступный  объем  видеопамяти  до  128  Мб, перейдя в настройки виртуальной машины, «Дисплей» $\rightarrow$ «Экран» (Рис. [-@fig:fig06]). 

![Настройки выбора объема выделяемой выдеопамяти. ](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image6.jpeg){#fig:fig06}

Далее во вкладке «Носители» добавили новый привод оптических дисков и выбрали  образ  Linux  Fedora,  скачанный  с  официального  сайта  (URL: [(https://getfedora.org/ru/workstation/download/)](https://getfedora.org/ru/workstation/download/) (Рис. [-@fig:fig07]). 

![Вкладка «Носители» с выбранным образом ОС.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image7.jpeg){#fig:fig07}

## Установка операционной системы Linux Fedora

Для запуска виртуальной машины в верхнем меню выбираем «Машина» $\rightarrow$ «Запустить». После загрузки образа с оптического диска появляется окно с двумя вариантами (Рис. [-@fig:fig08]): 

- Try  Fedora  —  запустить  систему  без  установки  —  этот  вариант выбирать не надо; 
- Install  to  Hard  Drive  —  установить  систему  на  жесткий  диск  — выбираем этот вариант. 

![Окно выбора при первичной загрузки виртуальной машины с монтированным образом ОС.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image8.jpeg){#fig:fig08}

Далее настроили клавиатуру и часовой пояс, а также выбрали место установки системы и нажали «Начать установку» (Рис. [-@fig:fig09] и [-@fig:fig010]). 

![Начальное меню установщка ОС. ](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image9.jpeg){#fig:fig09}

![Меню «Место установки». ](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image10.jpeg){#fig:fig010}

3. Завершение установки. 

После  завершения  установки  выключаем  систему,  извлекаем  образ  из дисковода, так как мы установили систему прямо на виртуальный диск (Рис. [-@fig:fig011]). 

![Вкладка «Носители» с пустым дисководом.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image11.jpeg){#fig:fig011}

При первой загрузке ОС настроили некоторые функции, в том числе логин и пароль для входа (Рис. [-@fig:fig012] --- [-@fig:fig016]). 

![Окно настройки ОС при первом запуске.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image12.jpeg){#fig:fig012}

![Меню «Конфиденциальность».](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image13.jpeg){#fig:fig013}

![Меню «Сторонние репозитории». ](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image14.jpeg){#fig:fig014}

![Меню «О вас» с установкой логина.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image15.jpeg){#fig:fig015}

![ Меню «О вас» с установкой пароля.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image16.jpeg){#fig:fig016}

## Установка программного обеспечения для создания документации

### Установка Git

Git – система управления версиями. Команда для установки Git через терминал: sudo dnf install -y git. При выполнении команды обнаружили, что актуальная версия Git уже установлена (Рис. [-@fig:fig022]). 

![Ввод команды установки Git и результат ее выполнения.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image22.png){#fig:fig022}

### Установка TeX Live
С официального сайта TeX Live
<https://www.tug.org/texlive/acquire-netinstall.html> скачали архив install-tl-unx.tar.gz (Рисунок [-@fig:fig101])) и распаковали (Рисунок [-@fig:fig102])).

![Загрузка установочного архива TeX Live.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image101.png){ #fig:fig101}

![Распаковка установочного архива TeX Live.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image102.png){#fig:fig102}

Перешли в распакованную папку и запустили скрипт install-tl с root правами (Рис. [-@fig:fig103]-[-@fig:fig104]).

![Запуск скрипта для установки TeX-Live.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image103.png){#fig:fig103}

![Окончание установки TeX Live.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image104.png){#fig:fig104}

Добавили /usr/local/texlive/2022/bin/x86_64-linux в PATH для текущей и будущих сессий (Рисунок [-@fig:fig105]).

![Добавление /usr/local/texlive/2022/bin/x86_64-linux в PATH.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image105.png){#fig:fig105}

### Установка Pandoc 2.19.2 и Pandoc-crossref v0.3.13.0b

Для корректной работы устанавливаем версию Pancdoc-crossref v0.3.13.0b, совместимую с Pandoc 2.19.2 (последняя версия).

Скачиваем архив pandoc (<https://github.com/jgm/pandoc/releases>:) и
архив pandoc-crossref (<https://github.com/lierdakil/pandoccrossref/releases>:) (Рисунок [-@fig:fig106]).

![Скачанные архивы pandoc и pandoc-crossref.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image106.png){#fig:fig106}

Распаковываем оба архива ((Рисунок [-@fig:fig107]).

![Команды для распаковки архивов.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image107.png){#fig:fig107}

Копируем файлы pandoc и pandoc-crossref в каталог /usr/local/bin/ (Рисунок [-@fig:fig108]):

![Перенос архивов в каталог /usr/local/bin/.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image108.png){#fig:fig108}

## Домашнее задание

С помощью команды `dmesg` проанализировали последовательность загрузки системы (Рисунок [-@fig:fig109]).

![Фрагмент вывода команды dmesg.](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image109.png){#fig:fig109}

Для поиска конкретной информации воспользовались командой `dmesg | grep -i "запрос"`:

* Версия ядра Linux (Рисунок [-@fig:fig110])

![Версия ядра Linux](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image110.png){#fig:fig110}

* Частота процессора (Рисунок [-@fig:fig111])

![Частота процессора](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image111.png){#fig:fig111}

* Модель процессора (Рисунок [-@fig:fig112])

![Модель процессора](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image112.png){#fig:fig112}

* Объем доступной оперативной памяти (Рисунок [-@fig:fig113])

![Объем доступной оперативной памяти](/home/dastarikov/work/study/2022-2023/Операционные\ системы/os-intro/labs/lab01/report/image/image113.png){#fig:fig113}

* Тип обнаруженного гипервизора (Рисунок [-@fig:fig114])

![Тип обнаруженного гипервизора](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image114.png){#fig:fig114}

* Тип файловой системы (Рисунок [-@fig:fig115])

![Тип файловой системы](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image115.png){#fig:fig115}

* Последовательность монтирования файловых систем (Рисунок [-@fig:fig116])

![Последовательность монтирования файловых систем](/home/dastarikov/work/study/2022-2023/Операционные системы/os-intro/labs/lab01/report/image/image116.png){#fig:fig116}

# Выводы

ри выполнении лабораторной работы были приобретены навыки установки операционной системы на виртуальной машину, в частности Linux Fedora, а также установки необходимых для работы в ОС сервисов, таких как TeX Live, pandoc, Git.
