---
## Front matter
title: "Отчет по лабораторной работе №4"
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

# Цель работы

Получение навыков правильной работы с репозиториями git.

# Задание


Выполнить работу для тестового репозитория.
Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits.


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

Устанавливаем git-flow (рис. [-@fig:001]).

![Установка git-flow](image/1.png){#fig:001 width=70%}

Устанавливаем Node.js (рис. [-@fig:002])

![Установка Node.js](image/2.png){#fig:002 width=70%}

![Установка apt](image/3.png){#fig:003 width=70%}

Выполняем source ~/.bashrc (рис. [-@fig:004])

![Выполение source ~/.bashrc](image/4.png){#fig:004 width=70%}

Настраиваем общепринятые коммиты (рис. [-@fig:005])

![Программа для помощи в форматировании коммитов и создании логов](image/5.png){#fig:005 width=70%}

Создаем репозиторий git и клонируем его (рис. [-@fig:006]),  (рис. [-@fig:007])

![Создание репозитория](image/6.png){#fig:006 width=70%}

![Клонирование репозитория](image/7.png){#fig:007 width=70%}

Делаем первый коммит и выкладываем на github (рис. [-@fig:008]), (рис. [-@fig:009])

![Первый коммит](image/8.png){#fig:008 width=70%}

![Отправка файлов на github](image/9.png){#fig:009 width=70%}

Конфигурируем общепринятые коммиты (рис. [-@fig:010]).

![Конфигурация для пакетов Node.js](image/10.png){#fig:010 width=70%}

Заполняем параметры пакета (рис. [-@fig:011]).

![Файл package.json](image/11.png){#fig:011 width=70%}

Добавляем новые файлы (рис. [-@fig:012])

![Команда git add .](image/12.png){#fig:012 width=70%}

Выполняем коммит и отправляем на github (рис. [-@fig:013])

![Команды git cz и git push](image/13.png){#fig:013 width=70%}

Инициализируем git-flow  (рис. [-@fig:014])

![Инициализация git-flow](image/14.png){#fig:014 width=70%}

Проверяем, что мы на ветке develop и загружаем весь репозиторий в хранилище (рис. [-@fig:015]).

![Команды git branch и git push](image/15.png){#fig:015 width=70%}

Устанавливаем внешнюю ветку как вышестоящую для этой ветки и создаем релиз с версией 1.0.0 (рис. [-@fig:016])

![Команды git branch и git flow](image/16.png){#fig:016 width=70%}

Создаем журнал изменений, добавляем журнал изменений в индекс и заливаем релизную ветку в основную ветку (рис. [-@fig:017])

![Создание журнала изменений, команды git add, git commit и git flow](image/17.png){#fig:017 width=70%}

Отправляем данные на github и создаем релиз (рис. [-@fig:018])

![Отправка файлов на github и создание релиза](image/18.png){#fig:018 width=70%}

Создаем ветку для новой функциональности и объединяем ветку feature_branch с develop (рис. [-@fig:019])

![Команда git flow](image/19.png){#fig:019 width=70%}

Создаем релиз в версией 1.2.3 и обновляем номер версии в файле package.json (рис. [-@fig:020])

![Файл package.json](image/20.png){#fig:020 width=70%}

Создаем журнал изменений, добавляем журнал изменений в индекс и заливаем релизную ветку в основную ветку (рис. [-@fig:021])

![Создание журнала изменений, команды git add, git commit и git flow]](image/21.png){#fig:021 width=70%}

Отправляем данные на github (рис. [-@fig:022])

![Отправка файлов на github](image/22.png){#fig:022 width=70%}

# Вывод

Мною были получены навыки правильной работы с репозиториями git.
