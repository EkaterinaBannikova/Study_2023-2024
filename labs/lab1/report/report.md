---
## Front matter
title: "Лабораторная работа №1"
subtitle: "Информационная безопасность"
author: "Банникова Екатерина Алексеевна"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

1. Приобретение практических навыков установки операционной системы на виртуальную машину.
2. Настройка минимально необходимых для дальнейшей работы сервисов.



# Выполнение лабораторной работы

Для установки на виртуальную машину VirtualBox операцинной системы Linux(дистрибутив CenOS) в нашем случае использовалась внешняя операционная система Windows.
В VirtualBox нажимаем "Машина" - "Создать" и задаем имя для нашей будущей операционной системы. Тип - LInux, версия - Red Hat(64-bit)

![Имя и тип ОС](image/1.png){ #fig:1 width=70% }

Задаем объем оперативной памяти 1024МБ.


![Объем памяти](image/2.png){ #fig:2 width=70% }

Создадим новый динамический виртуальный жесткий диск, укажем тип VDI, выделим 25ГБ


![Создание вертуального жесткого диска](image/3.png){ #fig:3 width=70% }

![Тип виртуального жесткого диска](image/4.png){ #fig:4 width=70% }

![Формат хранения](image/5.png){ #fig:5 width=70% }

![Размера виртуального жесткого диска](image/6.png){ #fig:06 width=70% }

Первоначальные основные настройки виртуальной машины заданы, теперь запускаем нашу операцинноую систему, выбирая образ дистрибутива CentOS.
Теперь стали доступны варианты установки дистрибутива и продолжение загрузки в тестовом режиме без установки. 

![Установка CentOS](image/7.png){ #fig:7 width=70% }

Отобразился обзор установки, где мы можем задать настройки уже нашей операционной системы: задать язык, пароль для суперпользователя, выбрать часовой пояс и тд.

![Выбор языка](image/8.png){ #fig:8 width=70% }

![Обзор установки с настройками ОС](image/9.png){ #fig:9 width=70% }

Нажимаем начать установку

![Установка](image/10.png){ #fig:10 width=70% }

После установки необходимо принять лизенцию.

![Лицензия](image/11.png){ #fig:11 width=70% }

Теперь можно завершать установку и переходить в CentOS.

Теперь нужно установитб дополнения гостевой ОС. Для это в виртуальной машине нажимаем "Устройства", "Подключить образ диска Дополнений гостевой ОС". После этого запускается установка в терминале.

![Установка дополнений гостевой ОС](image/12.png){ #fig:12 width=70% }

В итоге получили готовую к использованию операционную систему Linux с установленными дополнениями гостевой ОС, что позволяет менять разрешение экрана, использовать двухнаправленный буфер обмена с внешней ОС и др.

# Выводы

1. Я приобрела практические навыки установки операционной системы на виртуальную машину.
2. Настроила минимально необходимые для дальнейшей работы сервисы.


# Контрольные вопросы{.unnumbered}

1. Учетная запись пользователя содержит:
имя пользователя (логин) и пароль.
2. Команда для получения справки по команде - man ваша_команда
Команда для перемещения по файловой системе – cd
Команда для просмотра содержимого каталога - ls
Команда для определения объёма папки – du имя_папки
Команда для создания каталога – mkdir
Команда для создания файла – touch
Команда для удаления каталогов - rm
Команда для удаления файлов - rm -f
Команда для задания определённых прав - chmod права_доступа
имя_файла_или_имя_директории, где вместо «прав доступа» пишутся специальные знаки, обозначающие эти права доступа (u, g, o, a; +, -, =; r, w, x)
Команда для просмотра истории команд – history
3. Файловая система – это набор правил, устанавливающий способ хранения данных на определенном носителе информации.
Ext2, Ext3, Ext4 или Extended Filesystem - это стандартная файловая система для Linux, самая стабильная, содержит больше всего функций. JFS или Journaled File System была разработана в IBM для AIX UNIX и использовалась в качестве альтернативы для файловых систем ext. Сейчас она используется там, где необходима высокая стабильность и минимальное потребление ресурсов. ReiserFS - была разработана намного позже, в качестве альтернативы ext3 с улучшенной производительностью и расширенными возможностями. XFS - это высокопроизводительная файловая система, разработанная в Silicon Graphics для собственной операционной системы, для больших файлов и поддерживала диски до 2 терабайт. Btrfs или B-Tree File System - это совершенно новая файловая система, которая сосредоточена на отказоустойчивости, легкости администрирования и восстановления данных. Другие файловые системы, такие как NTFS, FAT, HFS могут использоваться в Linux, но корневая файловая система linux на них не устанавливается, поскольку они для этого не предназначены.
4. Чтобы посмотреть, какие файловые системы продемонстрированы в ОС, используется команда findmtn –all
5. Команды kill, xkill, pkill, killall cлужат для завершения процессов. Но они принимают различные параметры для идентификации процессов. Kill нужен PID процесса, xkill - достаточно кликнуть по окну, чтобы закрыть его, killall и pkill принимают имя процесса.

::: {#refs}
:::