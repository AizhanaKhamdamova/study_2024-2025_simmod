---
## Front matter
lang: ru-RU
title: Лабораторная работа № 8 
subtitle: Модель TCP/AQM
author:
  - Хамдамова Айжана
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 29 марта 2025

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
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Хамдамова Айжана 
  * студент факультета Физико-математических и естественных наук
  * Российский университет дружбы народов
  * [1032225989@pfur.ru](mailto:1032225989@pfur.ru)
  * <https://github.com/AizhanaKhamdamova/study_2024-2025_simmod>

:::
::: {.column width="30%"}

![](./image/my_photo.jpg)

:::
::::::::::::::


## Цели и задачи

- Построить модель TCP/AQM в xcos;
- Построить графики динамики изменения размера TCP окна $W(t)$ и размера очереди $Q(t)$;
- Построить модель TCP/AQM в OpenModelica;

## Выполнение лабораторной работы

![Установка контекста](image/1.png)

## Ход работы в xsoc

![Модель TCP/AQM в xcos](image/4.png){#fig:002 width=70%}

## Ход работы в xsoc

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t)](image/3.png)


## Ход работы в xsoc

![Фазовый портрет (W, Q)](image/2.png){#fig:004 width=70%}

## Ход работы в xsoc

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t) при С = 0.9](image/6.png)

## Ход работы в xsoc

![Фазовый портрет (W, Q) при С = 0.9](image/5.png)

## Реализация модели в OpenModelica

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t). OpenModelica](image/8.png)

## Реализация модели в OpenModelica

![Фазовый портрет (W, Q). OpenModelica](image/9.png)


## Выводы

В процессе выполнения данной лабораторной работы я реализовала модель TCP/AQM в xcos и OpenModelica.

## Список литературы{.unnumbered}

Братусь А. С., Новожилов Артем Сергеевич abd Платонов А. П. Динамические системы и модели биологии. — М. : ФИЗМАТЛИТ, 2010. — 400 с.

OM overall User’s Guide. — 2020. — URL: https://www.openmodelica.org/useresresources/userdocumentation.

Modelica Language. — URL: https : / / www . modelica . org /
modelicalanguage.

OpenModelica. — URL: https://www.openmodelica.org/.

Xcos. — URL: https://www.scilab.org/software/xcos.
