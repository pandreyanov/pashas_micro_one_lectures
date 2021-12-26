# Лекция 3, часть 2

Пусть есть, для простоты, два товара. Как обычно, будем обозначать их (и их спросы) как $x,y$ а соответствующие цены как $p,q$.

## Тождество Роя

Мы хотим связать между собой три объекта: $x^{\ast}(p,q,I), y^{\ast}(p,q,I)$ и  $V(\ast)(p,q,I)$. Для этого мы воспользуемся фундаментальным свойством, что косвенная полезность это полезность, в которую подставили спросы:

$$V(p, q, px + qy) = U(x, y),$$

Убедитесь, что это, действительно, корректная запись.

Что можно сделать с этим тождеством?

- продифференциировать по $p$
- продифференциировать по $q$

Заметим, что цены входят слева дважды, а справа не входят вообще. То есть, с точки зрения дифференциирования по ценам, справа стоит константа, а слева сложная функция. По правилам дифференциирования, полный дифференциал функции $V$ по $p$ равен:

$$ 
\begin{gather*}
\frac{d V}{d p} = \frac{\partial V}{\partial p} + \frac{\partial V}{\partial I} \cdot \frac{\partial I}{\partial p} = 0
\end{gather*}
$$

:::{seealso}
[Прочитайте, если вы не понимаете разницу между частным и полным дифференциалом.](differentials)
:::


````{prf:theorem} Orthogonal-Projection-Theorem
:label: my-theorem

Given $y \in \mathbb R^n$ and linear subspace $S \subset \mathbb R^n$,
there exists a unique solution to the minimization problem

```{math}
\hat y := \argmin_{z \in S} \|y - z\|
```

The minimizer $\hat y$ is the unique vector in $\mathbb R^n$ that satisfies

* $\hat y \in S$

* $y - \hat y \perp S$


The vector $\hat y$ is called the **orthogonal projection** of $y$ onto $S$.
````




## Возвращение к CES