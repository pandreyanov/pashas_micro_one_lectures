# Четвертая лекция, часть 1

## Оптимальное налогообложение

Исторически сложилось так, что государство финансирует свою деятельность, а также производство общественных благ за счет налогообложения. Есть три вида налогов:

- подоходный фиксированный (паушальный, от нем. "Pauschale") налог
- подоходный пропорциональный налог
- товарный налог

В разные периоды времени разные налоги пользовались популярностью. 

Простота **паушального налога** в том, что его можно ввести практически моментально, и его имплементация сводится к знанию своих подданных в лицо. Однако вы не можете установить паушальный налог больше, чем, грубо говоря, минимальный прожиточный минимум. То есть, чтобы собрать большую сумму паушальным налогом, вам придется освободить какую-то часть населения от этих налогов. Как только вы начинаете дискриминировать, то есть говорить кому платить, а кому не платить налог, он становится в какой-то степени пропорциональным.

Обычный **пропорциональный налог** означает, что каждый агент платит пропорционально своему доходу. К примеру, когда король Ричард Львиное Сердце попал в плен, английской короне пришлось платить выкуп за счет временного пропорционального налогообложения размером 25%. Таким образом, удалось в короткие сроки собрать огромную по тем временам сумму, примерно составляющую трехгодовой объем английской казны. 

Геометрически оба подоходных налога можно изобразить как параллельный сдвиг бюджетной линии, см. иллюстрацию.

:::{image} ./podohod_nalog.png
:alt: Подоходный налог
:width: 400px
:align: center
:::

В современной экономике основную роль играет **товарный налог**: VAT в США и НДС в России. Идея этого налога в том, что за каждую единицу проданного товара или оказанную услугу предприниматель платит процент от добавленной стоимости. 

Геометрически товарный налог отвечает за поворот бюджетной линии вокруг вершины, см. иллюстрацию.

:::{image} ./tovarny_nalog.png
:alt: Товарный налог
:width: 400px
:align: center
:::

Товарный налог хорошо адаптируется под быстро меняющуюся экономику. Например, если какой-то город начинает экономически расти, растут требования к окружающей его инфраструктуре: дороги, дома для рабочих, школы и университеты и так далее. Но также растут продажи товаров и услуг и, соответственно, растут налоговые сборы, покрывающие инвестиции в инфраструктуру.

Задача налогообложения может быть сформулирована как либо максимизация чистых налоговых сборов, либо максимизация косвенной полезности при фиксированных налоговых сборах. На выбор, как правило, есть либо подоходный, либо товарный налог.

### Налоги в Коббе-Дугласе

Рассмотрим полезность Кобба-Дугласа

$$U(x,y) = \alpha \log x + \beta \log y, \quad \alpha + \beta = 1$$

и введем налог размера $\tau$. Наш анализ оптимального налогообложения будет сильно зависеть от того, с какой легкостью мы выписываем косвенную полезность.

#### Подоходный налог

Если налог подоходный, то косвенная полезность и налоговые сборы будут равны:

$$ V(p,q,I,\tau) = \log I + \log (1-\tau) - \alpha \log(p) - \beta \log (q), \quad T = \tau I $$

Максимизация чистых налоговых сборов тут не представляет сложности – надо просто выставить $\tau = 1$, то есть отобрать все деньги. Максимизация косвенной полезности при фиксированных налоговых сборах тоже тривиальна: $\tau = T/I$.

<!-- #### Товарный налог

Пусть товарные налоги равны $\tau_x, \tau_y$ соответственно, тогда косвенная полезность и налоговые сборы будут равны:

$$V(p,q,I,\tau) = \log I - \alpha \log(p + \tau_x) - \beta \log (q + \tau_y), \quad T = \alpha I \frac{\tau_x}{p+\tau_x} + \beta I \frac{\tau_y}{q+\tau_y}$$

Максимизация чистых налоговых своров - это задача безусловной оптимизации:

$$T =  I \frac{ \alpha\tau_x}{p+\tau_x} + I \frac{\beta \tau_y}{q+\tau_y}$$

У этой задачи несколько контринтуитивное решение: необходимо назначить бесконечно большой налог на оба товара, тогда удастся собрать, в пределе, точно $I$. Это, конечно, не очень реалистично, но модель есть модель.

Максимизация косвенной полезности при фиксированных налоговых сборах – это задача условной оптимизации. Она уже более интересная:

$$\mathcal{L} = - \alpha \log(p + \tau_x) - \beta \log (q + \tau_y) + \lambda (\alpha I \frac{\tau_x}{p+\tau_x} + \beta I \frac{\tau_y}{q+\tau_y} - T)$$

Условия первого порядка:

$$ - \frac{\alpha}{p + \tau_x} + \lambda I \frac{\alpha}{(p + \tau_x)^2} = 0, \quad - \frac{\beta}{q + \tau_y} + \lambda I \frac{\beta}{(q + \tau_y)^2} = 0$$

Другими словами,

$$1 + \tau_x / p = \lambda I = 1 + \tau_y / q$$

То есть кажется, что **оптимальные налоги должны быть выставлены пропорционально ценам**. Это классный вывод, только нам осталось проверить, что задача выпуклая. Благо, Гессиан - диагональная матрица.

::::{dropdown} Вычислим вторые производные.

Это не бог весть какое сложное упражнение, но вот код в wolframscript, который можно установить бесплатно. 

:::{code}
sub = Solve[D[-a Log[p + x] + l a B x/(p + x), {x, 1}] == 0, l][[1]]
D[-a Log[p + x] + l a B x/(p + x), {x, 2}] /. sub // Simplify

:::

Нам очень повезло, и Гессиан, действительно, отрицательно определен:

$$ \frac{\partial^2 \mathcal{L}}{\partial^2 \tau_x} = \frac{-\alpha}{(p+\tau_x)^2}, \quad \frac{\partial^2 \mathcal{L}}{\partial^2 \tau_y} = \frac{-\beta}{(p+\tau_y)^2}$$

Значит наше внутреннее решение - локальный оптимум.

::::

Подставляя оптимальный налог в спросы, можно вывести, что

$$ p x^{\ast} = \alpha \frac{1}{\lambda}, \quad q y^{\ast} = \beta \frac{1}{\lambda}$$

Это очень похоже на то, что было бы без налогов. Складывается впечатление, что **оптимальные налоги устроены так, что они не меняют доли расходов, потраченные на каждый товар**. Более того, если присмотреться, то этот налог эквивалентен подоходному налогу, ведь он тоже не меняет доли. Другими словами, когда товарные налоги пропорциональны ценам, то бюджетное множество сдвигается параллельно, в точности как у подоходного налога.

Мы только что доказали, хоть и в малой общности, одну из самых глубоких экономических мыслей в теории налогообложения:

:::{prf:property} Оптимальность НДС
Оптимальный налог в Коббе-Дугласе не искажает потребление, это НДС.
:::

По-хорошему надо еще проверить, что потенциальные краевые решения не лучше, чем наш внутренний локальный оптимум, но это упражнение я оставлю читателю.

### Правило Рамсея

Что-то наподобие закона обратной эластичности было выведено для задачи оптимального налогообложения экономистом Фрэнком Рамсеем в начале 20 века. Своей целью он ставил минимизировать ненужные потери общества при потреблении путём введения дифференцированной ставки налогообложения на различные товары. То есть в точности максимизация косвенной полезности при зафиксированных налоговых сборах:

$$
\begin{gather*}
\min_{\lambda} \max_{\tau_x, \tau_y} \mathcal{L}, \quad \mathcal{L} = V(p,q,I) - \mu (\tau_x x(p) + \tau_y y(p) - T)
\end{gather*}
$$

Выпишем условия первого порядка:

$$\frac{\partial V}{\partial p} = \mu \tau_x \frac{\partial x}{\partial p}, \quad \frac{\partial V}{\partial q} = \mu \tau_x \frac{\partial y}{\partial p}$$

Вспомним, что по теореме об Огибающей производная косвенной полезности пропорциональна обычному (Маршаллианскому) спросу. Действительно:

$$ 
\begin{gather*}
V = \min_{\lambda} \max_{x,y} \mathcal{L}, \quad \mathcal{L} = U(x, y) - \lambda (p x + q y - I) \\
\frac{\partial V}{\partial p} = - \lambda x, \quad \frac{\partial V}{\partial q} = - \lambda y
\end{gather*}
$$

Получается, что в оптимуме

$$ \varepsilon_{x,p}\frac{\tau_{x}}{p} = \frac{\tau_x}{x} \frac{\partial x}{\partial p} = - \lambda / \mu = \frac{\tau_y}{y} \frac{\partial y}{\partial q} = \varepsilon_{y,q}\frac{\tau_{y}}{q}$$

Мы только что доказали (немножко игнорируя вопросы выпуклости) один из самых нетривиальных фактов в теории оптимального налогообложения:

:::{prf:property} Правило Рамсея

Оптимальные налоговые ставки пропорциональны обратным эластичностям обычного (Маршаллианского) спроса:

$$ \frac{\tau_x/p}{\tau_y/q} = \frac{1/\varepsilon_{x,p}}{1/\varepsilon_{y,q}},$$

другими словами, менее эластичные товары должны облагаться более сильным налогом, чем более эластичные.

:::

Это правило обобщает результат, который мы вывели в Коббе-Дугласе, поскольку в Коббе-Дугласе все эластичности потребления по цене постоянны, равны друг другу и равны $-1$. -->

## Компенсирующие и эквивалентные вариации

Мы освоили технику оптимального налогообложения. Это очень удобно, но иногда все равно приходится идти на попятную и точечно корректировать доход отдельным людям, возможно, из социально незащищенных слоев населения.

Поставим задачу вычисления денежной компенсации, которая сбалансирует повышение цен, связанное с налогообложением или еще чем-то. Сделать это можно двумя способами: при помощи компенсирующей и эквивалентной вариации.

### Компенсирующая вариация

Предположим, что полезность агентов была изначально на уровне $\bar U_0$ и произошло смещение цен $p \to p'$. Полезность агентов, конечно же, упала. Определим компенсирующую вариацию как изменение дохода, которое вернет их на изначальный уровень $\bar U_0$.

:::{prf:definition}

**Компенсирующая вариация** определяется как изменение в расходах, ассоциированных с первоначальным уровнем полезности

$$CV = E(p',\bar U_0) - E(p,\bar U_0), \quad \bar U_0 = U(x^{\ast}(p), y^{\ast}(p))$$

:::

Другими словами, государство как бы возвращает агентов на их стартовую полезность. Стартовая полезность – это статус-кво.


### Эквивалентная вариация

Предположим, что опять смещение цен $p \to p'$ и что полезность агентов упала до уровня $\bar U_1$. Определим эквивалентную вариацию как изменение дохода, которое было бы эквивалентно этому смещению цен, с точки зрения падения полезности.

:::{prf:definition}

**Эквивалентная вариация** определяется как изменение в расходах, ассоциированных с новым уровнем полезности

$$EV = E(p',\bar U_1) - E(p,\bar U_1), \quad \bar U_1 = U(x^{\ast}(p'), y^{\ast}(p'))$$

:::

Другими словами, государство как бы говорит: "если я верну все назад (и не заплачу вариацию), вы потеряете эквивалентно в полезности". Здесь новая полезность –  это статус-кво.


### Подсчет вариаций через $E$

Если вам комфортнее думать в терминах функции расходов, то все, что вам надо сделать, – это сосчитать уровни полезности до (для CV) и после (для EV) изменения цен и подставить в определение.

К примеру, в Леонтьевской полезности функция расходов выписывается быстро, если вспомнить, что левый и правый аргумент функции минимума обязаны давать одно и то же значение в оптимуме: 

$$h_x = a \bar U, \quad h_y = b \bar U, \quad E = (pa + qb) \bar U$$

Далее, если цены перешли $(p,q) \to (p',q')$, то полезность перешла 

$$ \bar U_0 = \frac{I}{pa + qb} \quad \to \quad \bar U_1 = \frac{I}{p'a + q'b} $$

Получается, что

$$ CV = (p'a + q' b - pa - qb) \frac{I}{pa + qb}, \quad EV = (p'a + q' b - pa - qb) \frac{I}{p' a + q' b}.$$

Вот и все.

### Подсчет вариаций через $V$

Если вам комфортнее думать в терминах косвенной полезности, то CV и EV – это решения достаточно простых нелинейных уравнений:

$$ V(p,q,I) = \bar U_0 = V(p',q',I+CV), \quad V(p,q,I-EV) = \bar U_1 = V(p',q',I)$$

Преимущество этого подхода в том, что сами уровни полезности вам считать необязательно. Можно сэкономить на выкладках.

К примеру, в полезности Кобба-Дугласа косвенную полезность можно запомнить с точностью до константы, которая все равно сократится в правой и левой части уравнения.

Для компенсирующей вариации:

$$
\begin{gather*}
 \log I - \alpha \log p - \beta \log q = \log (I+CV) - \alpha \log p' - \beta \log q'\\
 \log(\frac{I+CV}{I}) = \alpha \log (\frac{p'}{p}) + \beta \log (\frac{q'}{q})
\end{gather*}
$$

:::{dropdown} Для эквивалентной вариации:

$$
\begin{gather*}
 \log (I - EV) - \alpha \log p - \beta \log q = \log I - \alpha \log p' - \beta \log q'\\
 \log(\frac{I}{I - EV}) = \alpha \log (\frac{p'}{p}) + \beta \log (\frac{q'}{q})
\end{gather*}
$$

:::

### Первое приближение

Посмотрим внимательно на компенсирующую вариацию:

$$\log(\frac{I+CV}{I}) = \alpha \log (\frac{p'}{p}) + \beta \log (\frac{q'}{q})$$

Это читается так: **если цена $p$ выросла на $X \%$, а цена $q$ выросла на $Y \%$, то компенсирующая вариация должна увеличить бюджет на $\alpha X + \beta Y$ процентов** в первом приближении.


:::{seealso}
[Прочитайте, если вы не понимаете приближения.](approximations)
:::

Кстати, ни эквивалентная, ни компенсирующая вариации не зависят от нормировки полезности, поэтому вы можете выбирать удобную вам трансформацию. Вот и все.

### Второе приближение

Зафиксируем $q$, и пусть меняется только цена $p$.

Определим $\delta p = p'-p$ как приращение цены. Мы хотим приблизить нелинейное уравнение

$$\log(1 + \frac{CV}{I}) = \alpha \log (1 + \frac{\delta p}{p})$$

подставим все в экспоненту

$$1 + \frac{CV}{I} = (1 + \frac{\delta p}{p})^{\alpha}$$

разложим в ряд Тейлора до второго члена

$$1 + \frac{CV}{I} = 1 + \alpha \frac{\delta p}{p} + \frac{\alpha(\alpha-1)}{2} (\frac{\delta p}{p})^2 + \ldots$$

То есть $CV$ во втором приближении – это

$$CV = \frac{\alpha I}{p} \delta p - \frac{ \alpha \beta I}{p^2} (\delta p)^2.$$

Когда приращения достаточно большие (между 10 и 90 процентов), рекомендуется делать квадратичное, а не линейное приближение. 

Если приращение больше 100 процентов, то никакое приближение не сработает, так как у $\log(1+x)$ радиус сходимости равен единице.

## Чистые субституты и комплементы

Напомню, что первое определение субститутов и комплементов опиралось на перекрестные производные (маршаллианских) спросов по ценам. Несмотря на кажущуюся простоту и интуитивность этого определения, ничего не сдерживало нас от построения таких примеров, где товар $х$ был бы субститутом к $y$, при этом $y$ был комплементом к $x$.

Сейчас мы дадим альтернативное определение субститутов и комплементов. Для экспозиции предположим два товара $х,y$ с ценами $p,q$.

:::{prf:definition}
**Чистыми субститутами** называются пары товаров такие, что 

$$
\frac{\partial h_x}{\partial q} > 0, \quad \frac{\partial h_y}{\partial p} > 0.
$$

::: 

:::{prf:definition}
**Чистыми комплементами** называются пары товаров такие, что 

$$
\frac{\partial h_x}{\partial q} \leqslant 0, \quad \frac{\partial h_y}{\partial p} \leqslant 0.
$$

::: 

На первый взгляд, не совсем понятно, чем помогает замена Маршаллианского спроса на Хиксианский в определении. Однако, поскольку Хиксианский спрос - это градиент функции расходов, градиент Хиксианского спроса – это Гессиан функции расходов. 

А Гессиан, он же матрица Гессa - симметричная матрица.

:::{prf:property}
Пусть $h$ - весь вектор Хиксианского спроса, тогда

$$ \nabla \vec h = \nabla^2 E \quad \Rightarrow \quad \nabla \vec h = (\nabla \vec h)^T.$$

:::

Другими словами, перекрестные производные Хиксианского спроса по ценам - симметричны и нет больше никакого противоречие. Чистая субститутабильность/комплементарность – это свойство пары товаров, неважно как эта пара упорядочена.

### Кобб Дуглас

Напомним, что на предыдущей лекции мы вывели Хиксианские спросы:

$$h_x = \frac{\alpha}{p} E, \quad h_y = \frac{\beta}{q} E, \quad Е = e^{\bar U +C} p^{\alpha} q^{\beta}$$

Тогда перекрестные производные элементарно выводятся 


$$\frac{\partial h_x}{\partial q} = \frac{\alpha}{p} h_y = \frac{\alpha \beta}{p q} E = \frac{\beta}{q} h_x =\frac{\partial h_y}{\partial p}$$

:::{prf:property}
Все товары в Коббе-Дугласе являются чистыми субститутами.
:::

### Леонтьев

Напомним, что на предыдущей лекции мы вывели Хиксианские спросы:

$$h_x = a \bar U, \quad h_y = b \bar U$$

Тогда перекрестные производные равны нулю.

:::{prf:property}
Все товары в Коббе-Дугласе являются чистыми комплементами.
:::

Действительно, при фиксированной кривой безразличия изменение цен просто вращает бюджетную линию вокруг точки касания, а спросы при этом не меняются. 

### Почему ноль – это комплементы?

Конечно, можно было сказать, что ноль – это что-то среднее между субститутами и комплементами, но исторически ноль закреплен именно за комплементами, поскольку полезность "уголки" скорее интерпретируется как "комплементы".

Некоторые авторы предпочитают строгие неравенства во всех определениях, это дело вкуса.







