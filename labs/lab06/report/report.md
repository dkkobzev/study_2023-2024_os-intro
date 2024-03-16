---
## Front matter
title: "Отчет по лабораторной работе №5"
subtitle: "Архитектура компьютеров и операционные системы"
author: "Дмитрий Константинович Кобзев"

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

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en]

# Выполнение лабораторной работы

Определяем полное имя нашего домашнего каталога (рис. [-@fig:001])
 
![Полное имя домашнего каталога](image/1.png){#fig:001 width=70%}

Переходим в каталог /tmp (рис. [-@fig:002])

![Переход в каталог /tmp](image/2.1.png){#fig:002 width=70%}

Выводим на экран содержимое каталога /tmp. Для  этого используем команду ls с различными опциями (рис. [-@fig:003]), (рис. [-@fig:004])
 
![Cодержимое каталога /tmp](image/2.2.1.png){#fig:003 width=70%}
 
![Cодержимое каталога /tmp](image/2.2.2.png){#fig:004 width=70%}

Определяем, есть ли в каталоге /var/spool подкаталог с именем cron (рис. [-@fig:005])
 
![Содержимое каталога /var/spool](image/2.3.png){#fig:005 width=70%}

Переходим в наш домашний каталог и выводим а экран его содержимое. Определяем, кто является владельцем файлов и подкаталогов (рис. [-@fig:006])
 
![Содержимое домашнего каталога](image/2.4.png){#fig:006 width=70%}

В домашнем каталоге создаем новый каталог с именем newdir (рис. [-@fig:007])
 
![Создание каталога newdir](image/3.1.png){#fig:007 width=70%}

В каталоге ~/newdir создаем новый каталог с именем morefun (рис. [-@fig:008])
 
![Создание каталога morefun](image/3.2.png){#fig:008 width=70%}

В домашнем каталоге создаем одной командой три новых каталога с именами
letters, memos, misk. Затем удаляем эти каталоги одной командой (рис. [-@fig:009])
 
![Создание и удаление новых каталогов](image/3.3.png){#fig:009 width=70%}

Пробуем удалить ранее созданный каталог ~/newdir командой rm (рис. [-@fig:010])

![Удаление каталога /newdir](image/3.4.png){#fig:010 width=70%}

Удаляем каталог ~/newdir/morefun из домашнего каталога (рис. [-@fig:011])
 
![Удаление каталога /morefun](image/3.5.png){#fig:011 width=70%}

С помощью команды man определяем, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него (рис. [-@fig:012])
 
![Опция -R](image/4.png){#fig:012 width=70%}

С помощью команды man определяем набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога
с развёрнутым описанием файлов (рис. [-@fig:013]), (рис. [-@fig:014])
 
![Опция -l](image/5.1.png){#fig:013 width=70%}
 
![Опция -t](image/5.2.png){#fig:014 width=70%}

Используем команду man для просмотра описания следующих команд: cd, pwd, mkdir,
rmdir, rm (рис. [-@fig:015]), (рис. [-@fig:016]), (рис. [-@fig:017]),  (рис. [-@fig:018]),  (рис. [-@fig:019])

![Описание команды cd](image/6.1.png){#fig:015 width=70%}
 
![Описание команды pwd](image/6.2.png){#fig:016 width=70%}

![Описание команды mkdir](image/6.3.png){#fig:017 width=70%}

![Описание команды rmdir](image/6.4.png){#fig:018 width=70%}

![Описание команды rm](image/6.5.png){#fig:019 width=70%}

Используя информацию, полученную при помощи команды history, выполняем модификацию и исполнение нескольких команд из буфера команд (рис. [-@fig:020])

![Модификация и исполнение команд из буфера команд](image/7.png){#fig:020 width=70%}
