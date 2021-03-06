# Четырнадцатая лекция, часть 1

В этой части лекции мы поговорим об экстерналиях и корректирующих налогах.

## Что такое экстерналии?

Одной из двух важнейших предпосылок в анализе общего равновесия является **отсутствие экстерналий**, то есть, потребление одного  агента (производство фирмы) не меняет полезность других агентов (технологии других фирм). Формально, первая теорема благосостояния, доказанная на прошлых лекциях опирались на это предположение. 

Посмотрим, что получится, если добавить экстерналии. 

Я рассмотрю три класса экстерналии, которые я различаю по следующему принципу:

- экстерналии, получающиеся смешиванием полезностей
- сепарабельные экстерналии
- не сепарабельные экстерналии

### Первый класс: смешивание полезностей

Предположим, что полезности агентов $a,b$ равны:

$$ U_a(x_a,y_a|x_b,y_b) = u(x_a,y_a) + \varepsilon u(x_b,y_b), \quad U_b(x_b,y_b|x_a,y_a) = u(x_b,y_b) + \delta u(x_a,y_a)$$

Можно считать, что агенты "заботятся друг о друге", поэтому добавляют полезность противника себе с небольшими весами $\varepsilon, \delta$. Проанализируем, как изменится Парето фронт.

Поскольку взвешенная полезность равна 

$$U_a + \lambda U_b = (1+\lambda \delta)u(x_a, y_a) + (\lambda + \varepsilon)u(x_b, y_b)$$

то парето фронт будет абсолютно таким же, как если бы экстерналий не было:

$$ \tilde U_a(x_a,y_a) = u(x_a,y_a), \quad \tilde U_b(x_b,y_b) = u(x_b,y_b)$$

потому, что изменилась лишь параметризация парето фронта, но не сам он. Действительно, в обоих случаях используется условие сонаправленности градиентов: $\nabla u(x_a,y_a)$ и $\nabla u(x_b,y_b)$. А как насчет равновесия Вальраса?

Заметим, что полезность оптимизируется только по координатам собственного потребления, то есть, у оптимизационных задач:

$$ U_a(x_a,y_a|x_b,y_b) \to \max_{x_a,y_a},  \quad \tilde U(x_a,y_a) \to \max_{x_a,y_a}$$

одинаковые условия первого порядка. Действительно, возмущение связанное с добавлением чужой полезности, превратится в ноль при первом же дифференциировании.

Таким образом, для экстерналий, имеющих вид смешанных полезностей - обе теоремы благосостояния выполнены, поскольку экстерналии не меняют ни парето фронт, ни равновесие.

### Второй класс: сепарабельные экстерналии

Рассмотрим чуть более общий пример:

$$ U_a(x_a,y_a|x_b,y_b) = \tilde U_a(x_a,y_a) + f(x_b,y_b)\\
U_b(x_b,y_b|x_a,y_a) = \tilde U_b(x_b,y_b) + g(x_a,y_a)$$

где $f,g$ это функции, существенно отличные от $\tilde U_a$, $\tilde U_b$.

Заметим, что наличие функций $f,g$, опять не меняют равновесие Вальраса. Однако, они скорее всего меняют положение Парето фронта.

Например, пусть $f(x_b,y_b) = -x_b$, а $g(x_a, y_a) = 0$. Тогда, при максимизации взвешенной полезности, все кроме одного условия первого порядка:
$$
\frac{\partial}{\partial x_b} \tilde U_a(x_a,y_a) - 1 = \lambda  \frac{\partial}{\partial x_b} U_b(w_x-x_b,w_y - y_b)$$
остаются неизменными, а значит система не может иметь то же самое решение, что и без экстерналий.

Таким образом, для сепарабельных экстерналий - Парето фронт сдвигается, но равновесие Вальраса стоит на месте. Это значит, что теорема благосостояния, скорее всего, нарушается.

Сепарабельность не обязательно должна быть аддитивной. Если мы будет, например, умножать полезности, то добьемся похожего эффекта.

### Третий класс: несепарабельные экстерналии

В общем случае, например

$$U_a(x_a,y_a|x_b,y_b)=x_b \log x_a + \log y_a, \quad U_b(x_b,y_b|x_a,y_a) = \log x_b + x_a\log y_b$$

Парето фронт и равновесие Вальраса меняются одновременно и, скорее всего, первая теорема благосотояния не выполняется. Однако, наверняка сказать нельзя, поскольку равновесие может "чисто случайно" попасть на парето фронт.

## Что такое корректирующие налоги?

Предположим, что в силу экстерналий, или каких то других причин, равновесие Вальраса не является парето оптимальным. Тогда, государство может вмешаться и "подвинуть" равновесие ближе к Парето фронту, при помощи **корректирующих налогов**. Примерами таких налогов являются
- налоги и акцизы на табак и алкоголь
- штрафы за загрязнение окружающей среды

Налоги могут быть товарные, аушальные, а также общие и индивидуальные.

### Пример корректирующих налогов

Рассмотрим положительные экстерналии на потребление в экономике обмена:

$$U_a(x_a,y_a|x_b)= \log x_a + \log y_a + \log x_b, \quad U_b(x_b,y_b) = \log x_b + \log y_b$$

запасы пусть равняются $(1,1)$. 

Запишем условия первого порядка для поиска Парето фронта:

$$ \frac{1}{x_a} = \frac{\lambda + 1}{1-x_a}, \quad \frac{1}{y_a} = \frac{\lambda}{1-y_b}\\

$$

что приведет к

$$ x_a = \frac{1}{2+\lambda}, \quad y_a = \frac{1}{1+\lambda}.$$

:::{dropdown} Попробуем сначала попасть на парето фронт, при помощи **общего налога** $\tau$ на товар $x$, то есть, налога, который платят все агенты.

Запишем условия первого порядка для поиска равновесия Вальраса (положим цену товара $y$ равной 1):

$$ \frac{1}{x_a}/\frac{1}{y_a}  = p + \tau = \frac{1}{1-x_a}/\frac{1}{1-y_a}\\
(p + \tau) x_a + y_a = (p + \tau) + 1
$$

Легко видеть, что на Парето фронте 

$$\frac{1}{x_a}/\frac{1}{y_a}  = \frac{1}{1-x_a}/\frac{1}{1-y_a}$$ 

тогда и только тогда, когда $\lambda = \lambda + 1$, то есть никогда. Получается, что невозможно изменить цены для всех так, чтобы равновесие оказалось Парето оптимальным.

:::

:::{dropdown} Попробуем теперь попасть на парето фронт, при помощи **индивидуального налога** $\tau$ на товар $x$, который будет платить первый агент.

Запишем условия первого порядка для поиска равновесия Вальраса (положим цену товара $y$ равной 1):

$$ \frac{1}{x_a}/\frac{1}{y_a}  = p + \tau, \quad \frac{1}{1-x_a}/\frac{1}{1-y_a} = p\\
(p + \tau) x_a + y_a = (p + \tau) + 1
$$

получается система из 5 уравнений (2 от парето фронта, 3 от равновесия) и 5 неизвестных: $x_a, y_a, p, \tau, \lambda$; большая часть из которых линейна. Можно упростить до трех:

$$ p + \tau = \frac{1}{x_a}/\frac{1}{y_a} = \frac{2+\lambda}{1+\lambda}  \quad \Rightarrow \quad (\frac{2+\lambda}{1+\lambda} )(\frac{1}{2+\lambda}) + \frac{1}{1+\lambda} = (\frac{2+\lambda}{1+\lambda}) + 1$$
получается

$$ 2 = 3 + 2\lambda \quad \Rightarrow \quad \lambda = -1/2.$$

Остальные координаты легко найти.

:::

### Пример с производством

Предположим, что у нас экономика с одним потребителем

$$ U(x,y) = \log x + 2\log y$$

и одним производителем с технологией

$$ F(x,y) = (1-x) +  \log (1-y) \geqslant 0$$

причем, в экономике изначально всего 1 товара $x$ и 0 товара $y$. Будем считать, что производство товара $y$ из $x$ сопряжено с отрицательными экстерналиями (например, загрязнение воздуха), которые равны $H(y) = \log y$ в терминах полезости агента.

:::{dropdown} Вычислим Парето фронт:

$$ U(x,y) - H(y) + \lambda F(x,y) \to \max$$

$$ \log x + 2\log y - \log y + \lambda (1-x + \log (1-y)) \to \max$$

$$ \frac{1}{x} = \lambda, \quad \frac{1}{y} = \frac{\lambda}{1-y}$$

$$ x = \frac{1}{\lambda}, \quad y = \frac{1}{1+\lambda}, \quad \Rightarrow \quad x = \frac{y}{y-1}$$

:::