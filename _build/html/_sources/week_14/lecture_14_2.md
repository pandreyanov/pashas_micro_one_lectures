# Четырнадцатая лекция, часть 2

Комментарий - экономики с производством надо **всегда** делать как Эрроу-Дебре.
Общественное благо - специальная версия экстерналий.

## Общественное благо

Предположим, что один из товаров является общественным благом. Это означает, что потребление всех агентов зафиксированы на том же уровне. Я буду обозначать общественное благо как $z$.

Это значит, что у нас значительно меньше переменных, при, грубо говоря, том же количестве уравнений. Для того чтобы сбалансировать эту потерю, мы сделаем не одну, а много цен на общественное благо $z$.

:::{prf:definition} 

Равновесия (Вальраса-)Линдаля это
- уровни потребления частных благ $\vec x_i, \ i \in I$
- уровни производства $\vec y_j, \ j \in J$
- уровни потребления общественных благ $\vec z$

а также цены на частные блага, единые для всех участников рынка, и индивидуальные цены на общественное благо, такие что все агенты ведут себя оптимально при этих ценах. Более того, сумма цен на общественное потребителей равна ценe производителя.

:::

Условие первого порядка гарантируют, что

$$ \sum_{i \in I} \frac{\partial}{\partial z} U_i(...,z) = \frac{\partial}{\partial z}F(z),$$

где F(z) это расходы на производство $z$ единиц общественного блага. Это называется Уравнением Самуэльсона.

:::{dropdown} Выведем уравнение Самуэльсона из Парето оптимальности в квазилинейной экономике.

Если у всех агентов квазилинейные (по одному частному благу) полезности, то из дифференциальной характеристики парето фронта следует, что веса во взвешенной полезности одинаковые. Убедитесь сами.

Соответственно мы решаем следующую задачу

$$\sum_{i \in I} U_i(x,z) - (x - F(z)) \to \max$$

откуда и вытекает уравнение Самуэльсона.
:::

