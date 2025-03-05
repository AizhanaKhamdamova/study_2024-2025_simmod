---
## Front matter
title: "Упражнение на работу с xcos"
subtitle: "Построение фигур Лиссажу"
author: "Хамдамова Айжана"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Выполнить упражнение по ознакомлению с программой *xcos*.

# Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) $A = B = 1, a = 2, b = 2, \, \delta = 0; \, \pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$

2) $A = B = 1, a = 2, b = 4, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi;$

3) $A = B = 1, a = 2, b = 6, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3π/4; \, π;$

4) $A = B = 1, a = 2, b = 3, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi.$

# Выполнение лабораторной работы

Математическое выражение для кривой Лиссажу:
$$
\begin{cases}
  x(t) = A sin(at + \delta),\\
  y(t) = B sin(bt),
\end{cases}
$$
где $A, B$ -- амплитуды колебаний, $a, b$ -- частоты, $\delta$ -- сдвиг фаз.
В модели, изображённой на рис. [-@fig:001], использованы следующие блоки xcos:
- CLOCK_c -- запуск часов модельного времени;
- GENSIN_f -- блок генератора синусоидального сигнала;
- CSOPXY -- анимированное регистрирующее устройство для построения графика
типа y = f(x);
- TEXT_f -- задаёт текст примечаний.

Построим самый первый пример фигуры Лиссажу как на картинке (рис. [-@fig:001])

![Модель для построения фигуры Лиссажу в xcos](image_ex/1.png){#fig:001 width=70%}

Щелкнув правой кнопкой мышки по генератору синусоидальный колебаний, откроем вкладку параметры на редактирование и внесем нужные данные.

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 2, \delta = 0$ (рис. [-@fig:004]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:005]-[-@fig:008]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 0$](image_ex/2.png){#fig:004 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /4$](image_ex/3.png){#fig:005 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /2$](image_ex/4.png){#fig:006 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 3\pi /4$](image_ex/5.png){#fig:007 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi$](image_ex/6.png){#fig:008 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4, \delta = 0$ (рис. [-@fig:010]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:011]-[-@fig:014]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 0$](image_ex/6.png){#fig:010 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /4$](image_ex/7.png){#fig:011 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /2$](image_ex/8.png){#fig:012 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 3\pi /4$](image_ex/9.png){#fig:013 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi$](image_ex/10.png){#fig:014 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 6, \delta = 0$ (рис. [-@fig:016]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:017]-[-@fig:020]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 0$](image_ex/11.png){#fig:016 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /4$](image_ex/12.png){#fig:017 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /2$](image_ex/13.png){#fig:018 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 3\pi /4$](image_ex/14.png){#fig:019 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi$](image_ex/15.png){#fig:020 width=70%}



Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4, \delta = 0$ (рис. [-@fig:022]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:023]-[-@fig:026]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 0$](image_ex/16.png){#fig:022 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /4$](image_ex/17.png){#fig:023 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /2$](image_ex/18.png){#fig:024 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 3\pi /4$](image_ex/19.png){#fig:025 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi$](image_ex/20.png){#fig:026 width=70%}

# Выводы

В результате выполнения данной лабораторной работы я выполнила упражнение по ознакомлению с программой *xcos*.
