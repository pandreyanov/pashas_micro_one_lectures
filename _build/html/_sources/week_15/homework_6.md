# Шестое домашнее задание

*В скобках рядом с каждым пунктом указано количество баллов за этот пункт.*

## Задача 1

Рассмотрим экономику обмена с двумя агентами, где полезность $i$-го описывается слудеющей функцией:

$$
u_i(x_i, y_i)=\max \left\{x_i-\frac{1}{y_i}, y_i-\frac{1}{x_i}\right\}.
$$

В этой экономике суммарные запасы благ $x$ и $y$ равны единице:

$$
\omega _x^1+\omega _x^2 = 1, \quad \omega _y^1+\omega _y^2=1.
$$

> (3 балла) Запишите аналитически множество всех Парето-оптимальных распределений и изобразите на графике.

## Задача 2

В реальности не все общественные блага являются "чистыми", то есть найдется агент, потребление общественного блага которым не сокращает потребление этого же общественного блага другим агентом. Например, бесплатные федеральные дороги: если много водителей ими пользуется, то $i)$ их качество со временем ухудшается и $ii)$ большое число водителей на дороге создает пробки.

> * (1 балл) Приведите 2 примера таких общественных благ (если вы укажете больше 2 примеров, засчитаны будут только первые два).

Перейдем к формальной модели.

Пусть в экономике есть $n$ агентов, каждый из которых потребляет общественное благо $g$ и некоторое частное благо $x$. Полезность $i$-го агента представима функцией

$$
u_i(x_i, g) = \sqrt{x_i}+\sqrt{\frac{g}{n}}.
$$

Количества всех благ измеряются в деньгах. Каждый из агентов располагает запасами денежных средств в 2 денежные единицы. Агент $i$ вносит платеж $g_i$ на производство общественного блага, и $\sum _{i=1}^n g_i=g$.

> 1. (2 балла) Найдите равновесие с добровольным финансированием. Как объем производимого общественного блага зависит от количества агентов $n$?
> 2. (2 балла) Пусть государство обязывает каждого агента платить $t_i$ ($i \in \{1, \ldots, n\}$) денежных единиц на производство общественного блага. Найдите общественно-оптимальный объем общественного блага (воспользуйтесь уравнением Самуэльсона) и оптимальные налоговые ставки $t_i$ ($i \in \{1, \ldots, n\}$), если государство не может заставить потребителей платить больше, чем они были готовы в п. 1. Как объем производимого общественного блага зависит от количества агентов $n$?
> 3. (1 балл) Как изменится ваш ответ на пункт 2, если государство может ввести налог только если ставка $t_i\geqslant g_i$?

## Задача 3

В этой задаче вам предлагается рассмотреть следующую экономику.

* Агент $A$, который располагает запасами трудо-часов в размере 16 часов, любит отдыхать и потреблять благо $x$ (запасов этого блага нет). Чтобы получить благо $x$, он может работать. Иными словами, продавать часть запасов трудо-часов по фиксированной ставке $w$ и покупать благо $x$ по цене $p$. Оставшиеся трудо-часы он расходует на отдых $l$. Его полезность описывается функцией:

$$
u^A(x_A, l) = x_Al.
$$

* Агент $B$, который владеет запасами блага $x$ в размере 10 единиц. Также он умеет производить благо $x$ из трудо-часов агента $A$ в соответствии с производственной функцией $x=\sqrt{L}$, где $L$ - количество трудо-часов, купленных у агента $A$. Он может как продавать благо $x$ на монопольном рынке агенту $A$, так и потреблять его самостоятельно. Его полезность описывается функцией:

$$
u^B(x_B, y)=x_B^{\alpha}, \quad \alpha \in (0;1).
$$

Все агенты максимизируют полезность.

> 1. (1 балл) Запишите задачу максимизации полезности агента $A$.
> 2. (1 балл) Запишите задачу максимизации полезности агента $B$.
> 3. (2 балла) Выпишите аналитически множество Парето-оптимальных распределений и изобразите графически. *Подсказка: попробуйте изобразить кривые безразличия в ящике Эджворта*.
> 4. (1 балл) Найдите равновесие Вальраса в этой экономике.
> 5. (1 балл) Как параметры равновесия, найденные в пункте 4 этой задачи, зависят от параметра $\alpha$? Кратко проинтерпретируйте.

## Задача 4

В экономике есть 2 агента. Полезность агента $i$ имеет вид:

$$
U_i(x,z) = i \log x + z,
$$

где $z$ - общественное благо, $x$ - частное благо, и запасы частного блага у каждого агента по единичке. Также есть фирма, производящая общественное благо из частного по технологии 

$$
z = \log(-y),
$$

где $y$ - уровень производства частного блага.

> 1. (2 балла) Найдите равновесие Линдаля, если каждый агент владеет 50% фирмы.
> 2. (2 балла) Найдите равновесие с добровольным финансированием.
> 3. (1 балл) В каком равновесии производство общественного блага больше?