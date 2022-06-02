# Двенадцатая лекция, часть 1

В этой части лекции мы поговорим об экономиках с производством.

## Что такое экономика с производством?
Экономика обмена – это
- несколько потребителей (индивидуумов) $I = \{ a,b,c, \ldots\}$,
- несколько производителей $J = \{ \alpha, \beta, \gamma, \ldots\}$,
- несколько товаров $K = \{1, 2, 3, \ldots\}$,
- начальные запасы $\vec w_{a}, \vec w_{b}, \vec w_{c}, \ldots$

$$ \vec w_{a} = \{ w_{a1}, w_{a2}, w_{a3}, \ldots\},$$

- вектора потребления $\vec x_{a}, \vec x_{b}, \vec x_{c}, \ldots$

$$ \vec x_{a} = \{ x_{a1}, x_{a2}, x_{a3}, \ldots\},$$

- вектора производства $\vec y_{\alpha}, \vec y_{\beta}, \vec y_{\gamma}, \ldots$

$$ \vec y_{\alpha} = \{ x_{\alpha 1}, x_{\alpha 2}, x_{\alpha 3}, \ldots\}.$$

Экономика может находиться в одном из многих допустимых состояний

:::{prf:definition}

**Допустимым состоянием** экономики с производством называется набор координат потреблений и производств

$$\vec x = \{\vec x_i\}_{i \in I}, \quad \vec y = \{ \vec y_j\}_{j \in J}$$

такой, что 

- потребления неотрицательные

$$\forall i \in I, k \in K, \quad 0 \leqslant x_{ik},$$

- сумма потреблений (по каждому товару) совпадает с общими запасами (этого товара) и общим производством (этого товара)

$$\forall k \in K, \quad \sum_{i \in I} x_{ik} = \sum_{i \in I} w_{ik} + \sum_{j \in J} y_{jk},$$

- производства принадлежат соответствующим технологическим множествам

$$ \vec y_j \in Y_j.$$

:::

## Совместное технологическое множество

Последнее условие про $ \vec y_j \in Y_j$ можно заменить на то, что суммарное производство принадлежит совместному технологическому множеству $Y$:

$$ \sum_j \vec y_j \in Y $$

:::{prf:definition}

**Совместным технологическим множеством** $Y$ экономики с производством называется сумма всех индивидуальных технологических множеств.

:::

Подсчет $Y$ дословно соответствует тому, что мы делали раньше, когда надо было "объединить два завода". Как правило, $Y$ выглядит примерно так же, как и $Y_i$: он вогнутый, проходит через ноль, не содержит первый ортант.

:::{image} ./tech.png
:alt: Совместное технологическое
:width: 400px
:align: center
:::

## Ящик Эджворта

Как представить себе ящик Эджворта в экономике с производством?

- сначала надо нарисовать суммарные запасы $\{w_k\}_{k \in K}$, другими словами, правый верхний угол ящика Эджворта;
- затем надо построить совместное технологическое множество $Y$, проходящее через $\{w_k\}_{k \in K}$, как если бы это было начало координат;
- затем на границе этого множества выбрать новую точку;
- от нее нарисовать новый ящик Эджворта;
- потом взять другую точку, и так далее...

Пространство допустимых состояний описывается множеством прямоугольников в $\mathbb{R}^2$, по одному на каждый $y \in Y$.

:::{image} ./tech2.png
:alt: Совместное технологическое
:width: 400px
:align: center
:::

Получается, что ящик Эджворта "едет вдоль" границы $Y$. Как только мы зафиксировали производство $y \in Y$, ящик останавливается и дальше анализ соответствует простой экономике обмена.

## Парето-Оптимальность

Парето-оптимальность определяется аналогично тому, как мы это делали в экономике обмена, только поменялась интерпретация допустимого состояния.

:::{prf:definition}

Допустимое (в эк-ке с пр-вом) состояние **сильно ПО**, если не существует другого допустимого состояния, которое делает всем агентам (слабо) лучше, но хотя бы одному агенту сильно.

Допустимое (в эк-ке с пр-вом) состояние **слабо ПО**, если не существует другого допустимого состояния, которое делает всем агентам (сильно) лучше.

:::

## Геометрическая интерпретация ПО

Я могу дать лишь наглядную интерпретацию ПО, когда он является внутренней точкой. 

- нарисуем точку общих запасов,
- нарисуем общую технологическую границу,
- возьмем новую точку на границе и запомним наклон,
- нарисуем ящик Эджворта и как бы Парето-фронт в нем,
- на этом Парето-фронте выберем точку, в которой кривые безразличия касаются с тем же наклоном, что мы запомнили.

:::{image} ./tech3.png
:alt: Совместное технологическое
:width: 400px
:align: center
:::

Другими словами, истинный Парето-фронт состоит из набора точек, по одной на каждом из Парето-фронтах, нарисованных в двигающемся ящике Эджворта. Поскольку наклон Парето-фронта совпадает с наклоном границы технологического множества в соответствующей точке, то их форма приблизительно похожа друг на друга.

## Утилитарная интерпретация ПО

Рассмотрим функцию, задающую границу совместного технологического множества: 

$$\vec y \in \delta Y \quad \Leftrightarrow \quad F(\vec y) = 0.$$

В таком случае, можно интерпретировать ее как полезность дополнительного агента...

$$ U(x, y) = \lambda U_a(x) + \mu U_b(y + w-x) + F(y) \to \max_{x,y}, \quad \alpha, \beta \geqslant 0$$

Максимизируем взвешенную полезность, получаем истинный Парето-фронт. Заметим, что отсюда моментально следует коллинеарность всех трех градиентов: $\nabla U_a, \nabla U_b, \nabla F$ вo внутреннем Парето-оптимуме.

## Равновесие Вальраса с производством

:::{prf:definition}

**Равновесием Вальраса** экономики с производством называется допустимое состояние $\vec x, \vec y$ и вектор цен $\vec p$, такие, что каждый агент достигает максимума полезности по бюджетному ограничению, с бюджетом равным доходу от продажи своих начальных запасов, а производители максимизируют прибыль.

$$ \forall i \in I, \quad \vec x_i \in arg \max U_i(*) \quad s.t. \quad \vec p \cdot * \leqslant \vec p \cdot \vec w_i$$

$$ \forall j \in J, \quad \vec y_j \in arg \max (\vec p \cdot *) \quad s.t. \quad * \in Y_j$$

:::

## Как устроена площадка

Денег изначально у агентов нет, а есть только запасы товаров.

Агенты приходят на абстрактную торговую площадку и начинают менять запасы на деньги по всем известному курсу $\vec p$. Деньги печатаются, по мере необходимости, а товары остаются на центральном складе.

Далее приходят фирмы и начинают производить новые товары из тех, что лежат на складе. Покупая и продавая товары на площадке, они получают прибыль в деньгах, а число товаров на складе меняется.

Далее, агент начинает тратить свои деньги на товары. Причем, агент не видит товары и откуда они появляются, он просто "запрашивает" определенное количество. В некотором смысле он покупает "обещание" получить товар после окончания торгов.

Когда торги закончатся, организатор обязуется выполнить обещания в точности, причем, не должно остаться лишних товаров на складе (товарное равенство). Однако, уже не выполняется денежное равенство, поскольку часть денег останется на руках у производителей.

Задача организатора - выбрать цены $\vec p$ так, чтобы все получилось.

## РВ как система уравнений

Поиск Равновесия Вальраса можно представить себе как несколько групп уравнений.

- товарные равенства, $K$ штук: что сумма товаров в каждой категории равны соответствующим общим запасам, т.е. допустимое состояние экономики,
- условия оптимальности агентов, $K \cdot I$ штук: что каждый агент выбирает потребление оптимально, т.е. условия первого порядка,
- условия оптимальности фирм, $K \cdot J$ штук: также условия первого, порядка
- законы вальраса, $I$ штук,

неизвестные тоже можно разбить на группы

- цены, их $K$ штук,
- собственно потребления, их $K \cdot I$ штук,
- производства, их $K \cdot J$ штук,
- множители Лагранжа, их $I$ штук.

Как и в прошлый раз, у нас система из $(I +J)\cdot K + K + I$ уравнений и столько же неизвестных, но система снова линейно зависима. 

Как и в экономике обмена, если выполнены законы Вальраса для всех кроме одного агента, то последний закон Вальраса выполняется автоматически. 

То есть линейно независимых уравнений, на самом деле $(I+J)\cdot K + K + I - 1$. И столько же переменных, поскольку одну из цен можно нормировать к единице.

## Теоремы благосостояния

:::{prf:theorem} Первая теорема благосостояния
:class: remark
Пусть $(\vec x, \vec y, \vec p)$ - общее равновесие в экономике с производством, где все полезности локально ненасыщаемы, тогда $(\vec x, \vec y)$ - Парето-оптимум в сильном смысле.
:::

:::{dropdown} Доказательство

От обратного, предположим, что есть слабое Парето-улучшение, несмотря на то, что а) агенты максимизируют полезности б) фирмы максимизируют прибыль.

Назовем $(\tilde x, \tilde y)$ - кандидат на Парето-улучшение. 

**Точка зрения агентов**

Из локальной ненасыщаемости следует, что $\tilde x$ должна лежать вне бюджетного ограничения для того агента, который строго предпочитает $\tilde x$ к $\vec x$, в противном случае он бы никогда не купил $\vec x$ в равновесии,

$$ \exists i \in I \quad \vec p \cdot \tilde x_i > \vec p \cdot \vec x_i$$

А для всех остальных агентов либо вне либо в точности на бюджетной гиперплоскости,

$$ \forall i \in I \quad \vec p \cdot \tilde x_i \geqslant \vec p \cdot \vec x_i.$$

Тогда

$$ \vec p \cdot \sum \tilde x_i > \vec p \cdot \sum \vec x_i.$$

**Точка зрения фирм**

Поскольку все фирмы максимизируют прибыль,

$$ \forall j \in J \quad \vec p \cdot \tilde y_j \leqslant \vec p \cdot \vec y_j$$

а значит

$$ \vec p \cdot \sum \tilde y_j \leqslant \vec p \cdot \sum \vec y_j.$$

**Допустимое состояние**

$$ \forall k \in K: \quad \sum_{i \in I} \tilde x_{ik} = \sum_{i \in I} w_{ik} + \sum_{j \in J} \tilde y_{jk}$$

а значит

$$ \vec p \cdot \sum_{i \in I} \tilde x_{ik} = \vec p \cdot (\sum_{i \in I} w_{ik} + \sum_{j \in J} \tilde y_{jk})$$

**Построим цепочку**

$$

\vec p \cdot \sum \tilde x_i > \vec p \cdot \sum \vec x_i = \\
= \vec p \cdot (\sum \vec w_i + \sum \vec y_i) \geqslant \\
\geqslant \vec p \cdot (\sum \vec w_i + \sum \tilde y_i)

$$

Противоречие.

:::

:::{prf:theorem} Вторая теорема благосостояния
:class: remark
Пусть $(\vec x, \vec y)$ - внутренний сильный Парето-оптимум в экономике с производством, где все выпукло, непрерывно и локально ненасыщаемо, тогда существуют вектор цен и трансферты, такие, что $(\vec x, \vec y, \vec p)$ - равновесие вальраса с трансфертами.
:::

:::{dropdown} Идея доказательства

см. Теорема 4.7 в учебнике БЖЦ, опирается на теорему о разделяющей гиперплоскости.

:::

## Экономика Эрроу-Дебре

:::{prf:definition}

**Равновесием** экономики Эрроу-Дебре называется допустимое состояние $\vec x, \vec y$ и вектор цен $\vec p$, такие, что каждый агент достигает максимума полезности по бюджетному ограничению, с бюджетом равным доходу от продажи своих начальных запасов, а также какой-то доли прибыли фирм:

$$ \forall i \in I, \quad \vec x_i \in arg \max U_i(*) \quad s.t. \quad \vec p \cdot * \leqslant \vec p \cdot \vec w_i + \sum_{j \in J} s_{ij} \pi_j, \quad \pi_j = \vec p \cdot \vec y_j,$$

а производители максимизируют прибыль:

$$ \forall j \in J, \quad \vec y_j \in arg \max (\vec p \cdot *) \quad s.t. \quad * \in Y_j.$$

Ну и, конечно, доли должны суммироваться в единицу:

$$\forall j \in J, \quad \sum_{i \in I} s_{ij} = 1.$$

:::