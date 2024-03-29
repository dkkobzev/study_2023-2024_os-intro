---
## Front matter
title: "Отчет по лабораторной работе №1"
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

## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, нЦелью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов..

# Задание

Получите следующую информацию.

    Версия ядра Linux (Linux version).
    Частота процессора (Detected Mhz processor).
    Модель процессора (CPU0).
    Объём доступной оперативной памяти (Memory available).
    Тип обнаруженного гипервизора (Hypervisor detected).
    Тип файловой системы корневого раздела.
    Последовательность монтирования файловых систем.


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

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Устанавливаем систему на диск (рис. [-@fig:001]).

![Установленная система на диске](image/1.png){#fig:001 width=70%}

Устанавливаем операционную систему (рис. [-@fig:002]).

![Установленная операционная система](image/2.png){#fig:002 width=70%}

Переключаемся на роль супер-пользователя (рис. [-@fig:003]).

![Роль супер-пользователя](image/3.png){#fig:003 width=70%}

Обновляем все пакеты (рис. [-@fig:004]).

![Обновление всех пакетов](image/4.png){#fig:004 width=70%}

Устанавливаем программы для удобства работы в консоли (рис. [-@fig:005]).

![Установка программы для удобства работы в консоли](image/5.png){#fig:005 width=70%}

Устанавливаем программное обеспечение для автоматического обновления (рис. [-@fig:006]).

![Установка программного обеспечения для автоматического обновления](image/6.png){#fig:006 width=70%}

Запускаем таймер (рис. [-@fig:007]).

![Запуск таймера](image/7.png){#fig:007 width=70%}

Отключаем SELinux, заменив значение в файле /etc/selinux/config (рис. [-@fig:008]).

![Отключение SELinux](image/8.png){#fig:008 width=70%}

Запускаем терминальный мультиплескор tmux  и переключаемся на роль супер-пользователя (рис. [-@fig:009]).

![Роль супер-пользователя](image/9.png){#fig:009 width=70%}

Устанавливаем средства разработки (рис. [-@fig:010]).

![Установка средств разработки](image/10.png){#fig:010 width=70%}

Устанавливаем пакет DKMS (рис. [-@fig:011]).

![Установка пакета DKMS](image/11.png){#fig:011 width=70%}

В меню виртуальной машины подключаем образ диска дополнений гостевой ОС (рис. [-@fig:012]).

![Подключение образа диска дополнений гостевой ОС](image/12.png){#fig:012 width=70%}

Подмонтируем диск (рис. [-@fig:013]).

![Подмонтаж диска](image/13.png){#fig:013 width=70%}

Устанавливаем драйвер (рис. [-@fig:014]).

![Установка драйверов](image/14.png){#fig:014 width=70%}


Создаем конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf (рис. [-@fig:015]).

![Создание конфигурационного файла](image/15.png){#fig:015 width=70%}

Отредактируем конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf (рис. [-@fig:016).

![Редактирование конфигурационного файла](image/16.png){#fig:016 width=70%}

Отредактируем конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf (рис. [-@fig:017]).

![Редактирование конфигурационного файла](image/17.png){#fig:017 width=70%}

Создаем пользователя, задаем пароль, устанавливаем имя хоста и проверяем, что имя хоста установлено верно (рис.	[-@fig:018]).

![Создание пользователя](image/18.png){#fig:018 width=70%}

Внутри виртуальной машины добавляем своего пользователя в группу vboxsf (рис.	[-@fig:019]).

![Добавление своего пользователя в группу vboxsf](image/19.png){#fig:019 width=70%}

В хостовой системе подключаем разделяемую папку (рис.  [-@fig:020]).

![Подключение разделяемой папки](image/20.png){#fig:020 width=70%}

Устанавливаем pandoc для работы с языком разметки Markdown (рис.  [-@fig:021]).

![Установка pandoc](image/21.png){#fig:021 width=70%}

Устанавливаем pandoc-crossref для работы с перекрестными ссылками и распаковываем в каталог /usr/local/bin (рис.  [-@fig:022]), (рис.  [-@fig:023]).

![Распаковка pandoc-crossref](image/22.png){#fig:022 width=70%}
![Перемещение в каталог /usr/local/bin](image/23.png){#fig:023 width=70%}

Устанавливаем дистрибутив TexLive (рис.  [-@fig:024]).

![Установка TexLive](image/24.png){#fig:024 width=70%}

Домашнее задание (рис.	[-@fig:025]).

![Использование команды dmesg](image/25.png){#fig:025 width=70%}

Контрольные вопросы

1. Имя пользователя, название хоста.
2. man - для получения справки по команде.
cd - для перемещения по файловой системе.
ls - для просмотра содержимого каталога.
du - для определения объёма каталога.
mkdir/rm  - для создания / удаления каталогов / файлов.
chmod - для задания определённых прав на файл / каталог.
history - для просмотра истории команд.
3. Файловая система — это структура, используемая операционной системой для организации и управления файлами на устройстве хранения, например на жестком диске, твердотельном накопителе (SSD) или USB-накопителе.
4. С помощью команды findmnt.
5. С помощью команд kill и killall.

# Выводы

Мною были приобретены практические навыки устанковки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

::: {#refs}
:::
