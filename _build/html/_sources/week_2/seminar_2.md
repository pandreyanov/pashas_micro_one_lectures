# Семинар 2
*22 января 2022. Провела Даша*🐼

## Задача 1 Бюджетное ограничение
>
> В одной вымышленной стране живет маленький пёс Винни. Он каждый месяц самостоятельно решает, сколько корма в граммах ($x$) и сколько вкусняшек в граммах ($y$) он будет потреблять в этот месяц. Один грамм корма стоит $p$ денежек, а один грамм вкусняшек — $q$ денежек.  
> *  [Май] Изобразите на графике бюджетное ограничение Винни, если $p=5$, $q=10$ и каждый месяц Винни может потратить 20 000 денежек. Покажите все множество наборов доступных Винни. 
> * [Июнь] Изобразите на *том же* графике бюджетное ограничение Винни, если $p=5$, $q=10$, а доход Винни вырос на $20\%$ в этом месяце. Как изменилось положение Винни? Стало ли ему лучше?
> * [Июль] Изобразите на *том же* графике бюджетное ограничение Винни, если доход Винни остался таким же, как и в предыдущем месяце, а цена на вкусняшки увеличилась на $20\%$. Как изменилось положение Винни? Стало ли ему лучше?
> * [Август] Доход и цены не менялись с предыдущего месяца. Но теперь Винни может потратить 8 000 денежек, чтобы уехать к бабушке в деревню. Вкусняшки в граммах стоят дешевле — 4 денежек соответственно. Как теперь будет выглядеть бюджетное ограничение (подсказка: найдите огибающую)?
> * [Сентябрь*] Для любых цен и любого дохода нарисуйте бюджетное ограничение Винни.
> * [Октябрь*] В город, где живет Винни, завезли пиво для собак в мл. ($z$), которое стоит $r$ денежек. Изобразите бюджетное ограничение Винни для всех трёх товаров.

<details>
    <summary> Тут спрятался пёсик </summary>
 
:::{image} ./dog.png
:alt: Винни
:width: 400px
:align: center
:::

</details>

## Задача 2 Максимизация с применением метода Лагранжа
> [Ноябрь] Найдите, сколько Винни будет потреблять в этот месяц корма в килограммах ($x$), вкусняшек в килограммах ($y$) и сколько пива для собак в л. ($z$), если цены равны $5$ за грамм, $10$ за грамм и $8$ за мл., соответственно. На товары он может потратить 20 000 денежек в месяц. Его полезность имеет вид 
> 
> $$U(x,y,z) = x^\alpha y^\beta z^{1-\alpha-\beta},$$
> 
> где $\alpha, \beta, (\alpha + \beta) \in (0;1)$. 
> 
> <details>
>   <summary> По шагам </summary>
> 
> * Выпишите Лагранжиан
> * Найдите условия первого порядка
> * Найдите оптимальные значения
> * С помощью условия второго порядка покажите, что нашли максимум
> </details>

## Задача 3 Спрос и свойства товаров
> [Декабрь] Найдите спрос Винни в этом месяце на корм в килограммах ($x$), вкусняшки в килограммах ($y$) и пиво для собак в л. ($z$), если цены на товары $p$, $q$, $r$ соответственно, доход $I$. Его полезность имеет вид 
> 
> $$U(x,y,z) = x^\alpha y^\beta z^{1-\alpha-\beta},$$
> 
> где $\alpha, \beta, (\alpha + \beta) \in (0;1)$. 
> 
> * Изобразите на графиках спросы (кривые "цена - потребление")
> * Изобразите на графиках кривые Энгеля (кривые "доход-потребление")
> * Являются эти блага нормальными?
> * Для каждой пары товаров определите являются ли они субститутами или комплементами.
> * Найдите косвенную полезность.


## Задача 4 Графическое рассмотрение полезностей
> Считайте, что в этой вымышленной стране живут другие маленькие пёсики. Они могут потреблять корм в килограммах ($x$) и вкусняшки в килограммах ($y$). Корм стоит 5 денежек за грамм, а вкусняшки 10 денежек за грамм. Каждый пёсик может потратить 20 000 денежек в месяц. Для каждого пёсика изобразите на графике (а) бюджетное ограничение, (б) линии уровня, (в) точку оптимального потребления, а также (г) найдите её координаты и (д) скажите, к какому типу относится функция полезности пёсика. Кроме того, определите (е) являются ли товары нормальными, также (ё) являются ли попарными субститутами/комплементами.
> * [Джоки] $U(x,y,z) = 0.4 \ln (x) + 0.6\ln (y)$.
> * [Винсент] $U(x,y)=\min(x,2y)$
> * [Джесси] $U(x,y)=2x + 3y$
> * [Киса] $U(x,y)=(0.5x^{0.5}+0.5y^{0.5})^{2}$
> * [Ральф] $U(x,y)=x + \ln (y)$


## Задача 5 [Дополнительно]
> Рассмотрите ситуацию, которая сложилась в первой задаче в пункте "Август". 
> 
> <details>
>   <summary> Данные из первой задачи </summary>
> 
> |   | home   | grandma |
> |---|--------|---------|
> | p |    5   |    5    |
> | q |   12   |    4    |
> | I | 24 000 |  16 000 |
>
> </details>
> 
> Найдите для всех пёсиков оптимальную точку потребления на графике и найдите её координаты.
> 
> * [Джоки] $U(x,y,z) = 0.4 \ln (x) + 0.6\ln (y)$.
> * [Винсент] $U(x,y)=\min(x,2y)$
> * [Джесси] $U(x,y)=2x + 3y$
> * [Киса] $U(x,y)=(0.5x^{0.5}+0.5y^{0.5})^{2}$
> * [Ральф] $U(x,y)=x + \ln (y)$