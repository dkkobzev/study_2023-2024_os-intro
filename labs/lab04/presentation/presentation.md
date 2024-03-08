---
## Front matter
lang: ru-RU
title: Лабораторная работа №4
subtitle: Архитектура компьютера и операционные системы
author:
  - Кобзев Д. К.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 30 августа 2005

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

## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Кобзев Дмитрий Константинович
  * студент
  * прикладная информатика
  * Российский университет дружбы народов
  * [1132231936@rudn.ru](mailto:1132231936@rudn.ru)

:::
::: {.column width="30%"}

:::
::::::::::::::

# Вводная часть

## Цель работы

Получение навыков правильной работы с репозиториями git.

# Выполнение лабораторной работы

# Установка git-flow

- Устанавливаем git-flow
![](./image/1.png)

# Устанавка Node.js

- Устанавливаем Node.js
![](./image/2.png)

# Установка Node.js

- Устанавливаем apt
![](./image/3.png)

# Выполение source ~/.bashrc

- Выполеняем source ~/.bashrc]
![](./image/4.png)

# Настройка общепринятых коммитов

- Настраиваем общепринятые коммиты
![](./image/5.png)

# Создание репозитория

- Создаем репозиторий git и клонируем его
![](./image/6.png)

![](./image/7.png)

# Первый коммит

- Делаем первый коммит и выкладываем на github 

![](./image/8.png)

![](./image/9.png)

# Конфигурация для пакетов Node.js

- Конфигурируем общепринятые коммиты 
![](./image/10.png)

# Параметры пакета

- Заполняем параметры пакета 
![](./image/11.png)

# Добавление новых файлов

- Добавляем новые файлы
![](./image/12.png)

# Выполнение коммита и отправка файлов на github 

- Выполняем коммит и отправляем на github 
![](./image/13.png)

# Инициализация git-flow

- Инициализируем git-flow
![](./image/14.png)

# Команды git branch и git push

- Проверяем, что мы на ветке develop и загружаем весь репозиторий в хранилище
![](./image/15.png)

# Команды git branch и git flow

- Устанавливаем внешнюю ветку как вышестоящую для этой ветки и создаем релиз в версией 1.0.0
![](./image/16.png)

# Создание журнала изменений, команды git add, git commit и git flow

- Создаем журнал изменений, добавляем журнал изменений в индекс и заливаем релизную ветку в основную ветку 
![](./image/17.png)

# Отправка файлов на github и создание релиза

- Отправляем данные на github и создаем релиз 
![](./image/18.png)

# Команда git flow

- Создаем ветку для новой функциональности и объединяем ветку feature_branch с develop 
![](./image/19.png)

# Файл package.json

- Создаем релиз в версией 1.2.3 и обновляем номер версии в файле package.json 
![](./image/20.png)

# Создание журнала изменений, команды git add, git commit и git flow

- Создаем журнал изменений, добавляем журнал изменений в индекс и заливаем релизную ветку в основную ветку
![](./image/21.png)

# Отправка файлов на github

Отправляем данные на github
![](./image/22.png)
