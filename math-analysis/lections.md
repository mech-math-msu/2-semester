---
title: Математический анализ
---

# Неопределенный интеграл


:::: {#definition-0}

**Определение:**  Пусть $f(x)$ определена на $(a, b)$. Пусть $F(x)$, такова что $F’(x) = f(x) \,\,\,\, \forall x \in (a, b)$. Тогда $F(x)$ *первообразная* $f(x)$ на $(a, b)$.

::::

:::: {#definition-1}

**Определение:**  *Неопределенный интеграл* $f(x)$ на $(a, b)$ -- это множество всех первообразных $f(x)$ на $(a, b)$. Обозначается $\displaystyle \int f(x)dx$.

::::

Замечание: $f(x)dx = F’(x)dx = dF(x)$. То есть интеграл -- это множество всех функций, дифференциал которых равен некоторой заданной функции $f(x)$.

:::: {#theorem-0}

**Теорема:**  Пусть $F(x)$ первообразная $f(x)$ на $(a, b)$. Тогда 
$$\displaystyle \int f(x)dx = \{F(x) + g(x), \,\,\,\, g(x) = C, \,\,\,\, C \in \mathbb{R}\}$$

*Доказательство:* Докажем, что $F(x) + C$ -- это первообразная $f(x)$ на $(a, b)$. $(F(x) + C)’ = F’(x) + C’ = f(x)$.

Докажем, что любая первообразная представима в виде $F(x) + g(x), \,\,\,\, g(x) = C \,\,\,\, C \in \mathbb{R}$. Пусть $G(x)$ первообразная $f(x)$ на $(a, b)$. Рассмотрим $F(x) - G(x)$. $(F(x) - G(x))’ = F’(x) - G’(x) = f(x) - f(x) = 0$. Следовательно по следствию из теоремы Лагранжа $F(x) - G(x) = const \Rightarrow G(x) = F(x) + C \,\,\,\,\blacksquare$

Далее пишем $\displaystyle \int f(x) dx = F(x) + C$, подразумевая множество всех первообразных.

::::

## Свойства неопределенного интеграла


:::: {#statement-0}

**Утверждение:**  (*Свойства неопределенного интеграла*)

1. $\displaystyle \int k \cdot f(x) dx = k \cdot \displaystyle \int f(x) dx$ (Множество умножить на число -- это каждый элемент множества умножить на число)

2. $\displaystyle \int (f(x) + g(x)) dx = \displaystyle \int f(x) dx + \displaystyle \int g(x) dx$

3. $\displaystyle \int f(\varphi(x)) \varphi’(x) dx = F(\varphi(x)) + C$, если $F(x)$ первообразная $f(x)$.

4. $\displaystyle \int f’(x) g(x) dx = f(x)g(x) - \displaystyle \int f(x) g’(x) dx$

*Доказательство:*

1. -- 3. очев $\,\,\,\,\blacksquare$
4. Проинтегрировать производную суммы функций $\,\,\,\,\blacksquare$

::::

## Таблица неопределенных интегралов


Смэрть

## Интегрирование рациональных функций


Хотим интегрировать функции вида: $\frac{P(x)}{Q(x)}$, где $P(x), Q(x) \in \mathbb{R}[x]$, то есть многочлены от одной пременной над полем $\mathbb{R}$.

Из алгебры любая такая дробь представима в виде:

$$\frac{P(x)}{Q(x)} = S(x) + \displaystyle \sum_{i = 0}^{n} \frac{A_i}{(x - a_i)^{\alpha_i}} + \displaystyle \sum_{j = 0}^{m}\frac{B_j + C_jx}{(x^2 + p_jx + q_j)^{\beta_j}},$$ где $x^2 + p_jx + q_j = 0$ не имеет действительных корней, а $S(x)$ многочлен.

То есть нужно уметь искать интегралы трех видов:

1. $S(x) = a_0 + a_1x + a_2x^2 + \ldots + a_nx^n$
2. $\frac{A}{(x - a)^{\alpha}}$
3. $\frac{B + Cx}{(x^2 + px + q)^{\beta}}$

Найдем эти интегралы:

1. $\displaystyle \int S(x)dx = \displaystyle \int (a_0 + a_1x + a_2x^2 + \ldots + a_nx^n)dx=$ 
$= \displaystyle \int a_0 dx + \displaystyle \int a_1x dx + \ldots + \displaystyle \int a_nx^n dx= a_0 x + a_1 \frac{x^2}{2} + \ldots + a_n \frac{x^{n + 1}}{n + 1}$

2. $\frac{A}{(x - a)^{\alpha}}$ Пусть $\alpha \ne 1$. Тогда 
$$\displaystyle \int \frac{A}{(x - a)^{\alpha}}dx = \displaystyle \int A(x - a)^{-\alpha}dx = A\frac{(x - a)^{-\alpha + 1}}{-\alpha + 1} + C.$$
Пусть $\alpha = 1$. Тогда
$$\displaystyle \int \frac{A}{(x - a)}dx = \displaystyle \int \frac{A}{(x - a)}d(x - a) = A\ln|x - a| + C.$$

3. $$\frac{B + Cx}{(x^2 + px + q)^{\beta}} = 
\frac{C(x + \frac{p}{2}) + s}{((x + \frac{p}{2})^2 + e^2)^{\beta}} = \frac{C t}{(t^2 + e^2)^{\beta}} + \frac{s}{(t^2 + e^2)^{\beta}}$$
То есть $\displaystyle\int \frac{B + Cx}{(x^2 + px + q)^{\beta}} dx = \displaystyle\int \frac{C t}{(t^2 + e^2)^{\beta}} dt + \displaystyle\int \frac{s}{(t^2 + e^2)^{\beta}} dt$

a. $$\displaystyle\int \frac{C t}{(t^2 + e^2)^{\beta}} dt = \frac{C}{2}\displaystyle\int \frac{d(t^2 + e^2)}{(t^2 + e^2)^{\beta}} = \ldots$$

b. $$I_{\beta} = \displaystyle\int \frac{dt}{(t^2 + e^2)^{\beta}} = \frac{t}{(t^2 + e^2)^{\beta}} + \displaystyle\int \frac{2t^2\beta}{(t^2 + e^2)^{\beta + 1}} dt =$$
$$= \frac{t}{(t^2 + e^2)^{\beta}} + 2\beta\displaystyle\int \frac{(t^2 + e^2) - e^2}{(t^2 + e^2)^{\beta + 1}} dt = \frac{t}{(t^2 + e^2)^{\beta}} + 2\beta I_{\beta} - 2\beta e^2 I_{\beta + 1}$$
Получили рекуррентную формулу для вычисления интеграла:
$$I_{\beta + 1} = \frac{t}{2\beta e^2 (t^2 + e^2)^{\beta}} + \frac{2\beta - 1}{2\beta e^2}I_{\beta}$$

При $\beta = 1$ имеем $$\displaystyle\int \frac{dt}{t^2 + e^2} = \frac{1}{e}\displaystyle\int \frac{d(\frac{t}{e})}{(\frac{t}{e})^2 + 1} = \frac{1}{e}\tan^{-1}\frac{t}{e} + C$$

## Метод Остроградского


![](img/blah-blah.png)

# Определенный интеграл Римана

## Определения

:::: {#definition-2}

**Определение:**  *Положительное разбиение* отрезка $[a, b]$ -- это множество точек $\{x_i\}_{i = 0}^{n}$, таких что $a = x_0 < x_1 < \ldots < x_{n - 1} < x_n = b$. 

Обозначается: $\mathcal{T}_{[a, b]}^{+}$.

::::


:::: {#definition-3}

**Определение:**  *Отрицательное разбиение* отрезка $[a, b]$ -- это множество точек $\{x_i\}_{i = 0}^{n}$, таких что $b = x_0 > x_1 > \ldots > x_{n - 1} > x_n = a$. 

Обозначается: $\mathcal{T}_{[a, b]}^{-}$.

::::

:::: {#definition-4}

**Определение:**  Пусть дано разбиение $\mathcal{T}_{[a, b]} = \{x_i\}_{i = 0}^{n}$ отрезка $[a, b]$.

$i$-й *отрезок разбиения* $\mathcal{T}_{[a, b]}$ -- это $\Delta_i = [x_{i - 1}, x_i] \,\,\,\, \forall i \in \{1, \ldots, n\}$.<br>

*длина* $\Delta_i$ равна $|\Delta_i| = |x_{i} - x_{i - 1}|$.<br>

*диаметр разбиения* $d(\mathcal{T}_{[a, b]})$ -- это $\displaystyle \max_{i \in \{1, \ldots, n\}}{|\Delta_i|}$.

::::

:::: {#definition-5}

**Определение:**  Пусть дано разбиение $\mathcal{T}_{[a, b]} = \{x_i\}_{i = 0}^{n}$ отрезка $[a, b]$.

*Разметка* $\mathcal{T}_{[a, b]}$ -- это множество точек $\xi = \{\xi_1, \xi_2, \ldots, \xi_n\}$, таких что $\xi_i \in \Delta_i$.
Разбиение с заданной разметкой обозначается $\mathcal{T}(\xi)_{[a, b]} = \{\mathcal{T}, \xi\}$.

::::

:::: {#definition-6}

**Определение:**  *Интегральная сумма* -- это $\sigma_{f}(\mathcal{T}(\xi)) = \displaystyle \sum_{i = 1}^{n}f(\xi_i)\cdot(x_i - x_{i - 1})$.

::::

:::: {#definition-7}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$. Если $\exists I \in \mathbb{R}$, такое что 

$$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall \mathcal{T}_{[a, b]}^{+}(\xi) \left(d(\mathcal{T}_{[a, b]}^{+}) < \delta\right) \,\,\,\, |\sigma_{f}(\mathcal{T}(\xi)) - I| < \varepsilon,$$
то функция $f(x)$ *интегрируема по Риману* на отрезке $[a, b]$, а число $I$ -- *интеграл* $f(x)$ на отрезке $[a, b]$. Обозначается $I = \displaystyle \int\limits_a^b f(x)dx$.

::::

:::: {#definition-8}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$. Если $\exists I \in \mathbb{R}$, такое что 

$$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall \mathcal{T}_{[a, b]}^{-}(\xi) \left(d(\mathcal{T}_{[a, b]}^{-}) < \delta\right) \,\,\,\, |\sigma_{f}(\mathcal{T}(\xi)) - I| < \varepsilon,$$
то функция $f(x)$ *интегрируема по Риману* на отрезке $[a, b]$, а число $I$ -- *интеграл* $f(x)$ на отрезке $[a, b]$. Обозначается $I = \displaystyle \int\limits_b^a f(x)dx$.

::::

:::: {#statement-1}

**Утверждение:**  $$\displaystyle \int\limits_a^b f(x)dx = -\displaystyle \int\limits_{b}^{a} f(x)dx$$

*Доказательство:* нуу, очев $\,\,\,\,\blacksquare$

::::

:::: {#definition-9}

**Определение:**  Множество всех функций интегрируемых по Риману на отрезке $[a, b]$ обозначается $\mathcal{R}[a, b]$.

::::

:::: {#theorem-1}

**Теорема:**  Если функция $f(x) \in \mathcal{R}[a, b]$, то $f(x)$ ограничена на $[a, b]$.

*Доказательство:* (от противного) Пусть $f(x)$ неограничена на $[a, b]$, то есть $\forall x \in \mathbb{R} \,\,\,\, \exists \xi \in [a, b]: \,\,\,\, f(\xi) > x$.
$\exists \displaystyle\int\limits_a^b f(x)dx = I$. Возьмем $\varepsilon = 1$, имеем
$$\exists \delta > 0: \,\,\,\, \forall \mathcal{T}_{[a, b]}^{+}(\xi) \left(d(\mathcal{T}_{[a, b]}^{+}) < \delta\right) \,\,\,\, |\sigma_{f}(\mathcal{T}(\xi)) - I| < 1$$

$$I - 1 < \displaystyle \sum_{i = 1}^{n}f(\xi_i)\cdot(x_i - x_{i - 1}) < I + 1$$

Зафиксируем разметку $\xi$. $f(x)$ неограничена на одном из $\Delta_i$. Будем менять $\xi_i \in \Delta_i$. $|f(\xi_i)|$ принимает сколь угодно большое значение, а значит сумма не будет ограничена $\,\,\,\,\blacksquare$


::::

## Суммы Дарбу


:::: {#definition-10}

**Определение:**

Пусть $f(x)$ ограничена на отрезке $[a, b]$. $\mathcal{T}_{[a, b]}^{+}$ -- некоторое разбиение отрезка $[a, b]$.
Пусть 
$m_i = \displaystyle \inf_{x\in \Delta_i}f(x)$ (точная нижняя грань $f(x)$ на $i$-ом отрезке разбиения $\mathcal{T}_{[a, b]}^{+}$), $M_i = \displaystyle \sup_{x\in \Delta_i}f(x)$.

$s(\mathcal{T}) = \displaystyle \sum_{i = 1}^{n} m_i\cdot (x_{i} - x_{i - 1})$ -- это *нижняя сумма Дарбу* функции $f(x)$ по разбиению $\mathcal{T}_{[a, b]}^{+}$.

$S(\mathcal{T}) = \displaystyle \sum_{i = 1}^{n} M_i\cdot (x_{i} - x_{i - 1})$ -- это *верхняя сумма Дарбу* функции $f(x)$ по разбиению $\mathcal{T}_{[a, b]}^{+}$.

::::

## Свойства сумм Дарбу


:::: {#lemma-0}

**Лемма:**  Пусть $\{X_i: \,\,\,\, X_i \subset \mathbb{R}\}_{i = 1}^n$, $X_i$ -- ограничено $\forall i \in \{1, \ldots, n\}$. $\{a_i: \,\,\,\, a_i \ge 0\}_{i = 1}^n$. Тогда 
$$\displaystyle\sup_{x_i \in X_i}\left\{\sum_{i = 1}^{n}a_ix_i\right\} = \displaystyle \sum_{i = 1}^{n}a_i \displaystyle\sup\left(X_i\right)$$
$$\displaystyle\inf_{x_i \in X_i}\left\{\sum_{i = 1}^{n}a_ix_i\right\} = \displaystyle \sum_{i = 1}^{n}a_i \displaystyle\inf\left(X_i\right)$$

Точная верхняя грань сумм -- это точная верхняя грань множества всех сумм вида $\displaystyle \sum_{i = 1}^{n}a_ix_i$, где $x_i \in X_i$.

*Доказательство:* $$\forall \varepsilon \,\,\,\, \forall i \,\,\,\, \exists x_i \in X_i:\,\,\,\, x_i > \sup X_i - \varepsilon$$

Домножая каждую сумму неравенства на $a_i$ и суммируя по $i$, получаем:

$$\forall \varepsilon > 0 \,\,\,\, \exists \{x_i \in X_i\}_{i = 1}^n:\,\,\,\,\displaystyle \sum_{i = 1}^{n}a_ix_i > \displaystyle \sum_{i = 1}^{n}a_i\sup X_i - \varepsilon \displaystyle \sum_{i = 1}^{n}a_i$$

Так как утверждение верно для любого $\varepsilon > 0$, то домножение $\varepsilon$ на положительную константу ничего не меняет, то есть:  
$$\forall \varepsilon > 0 \,\,\,\, \exists \{x_i \in X_i\}_{i = 1}^n:\,\,\,\,\displaystyle \sum_{i = 1}^{n}a_ix_i > \displaystyle \sum_{i = 1}^{n}a_i\sup X_i - \varepsilon$$

Значит $$\displaystyle\sup_{x_i \in X_i}\left\{\sum_{i = 1}^{n}a_ix_i\right\} = \displaystyle \sum_{i = 1}^{n}a_i \displaystyle\sup\left(X_i\right) \,\,\,\,\blacksquare$$

::::

:::: {#theorem-2}

**Теорема:**  (*Свойства сумм Дарбу*)

1. Пусть разбиение $\mathcal{T}_2$ измельчение $\mathcal{T}_1$. Тогда $S(\mathcal{T}_1) > S(\mathcal{T}_2)$ и $s(\mathcal{T}_1) < s(\mathcal{T}_2)$.

2. Пусть $\mathcal{T}_2$ и $\mathcal{T}_1$ некоторые разбиения $[a, b]$. Тогда $s(\mathcal{T}_1) < S(\mathcal{T}_2)$

3. $$S(\mathcal{T}) = \displaystyle\sup_{\xi}\left\{\sigma_f(\mathcal{T}(\xi))\right\}$$
$$s(\mathcal{T}) = \displaystyle\inf_{\xi}\left\{\sigma_f(\mathcal{T}(\xi))\right\}$$

*Доказательство:*

1. Пусть $\mathcal{T}_2 = \mathcal{T}_1 \cup \{t\}, \,\,\,\, t \in [x_{j - 1}, x_j]$. Тогда 
$$S(\mathcal{T}_2) - S(\mathcal{T}_1) = \displaystyle\sup_{[x_{j - 1}, t]}(f(x))\cdot (t - x_{j - 1}) + \displaystyle\sup_{[t, x_j]}(f(x))\cdot (x_j - t) - \displaystyle\sup_{[x_{j - 1}, x_j]}(f(x))\cdot (x_j - x_{j - 1})=$$
$$=\displaystyle\sup_{[x_{j - 1}, t]}(f(x))\cdot (t - x_{j - 1}) + \displaystyle\sup_{[t, x_j]}(f(x))\cdot (x_j - t) - \displaystyle\sup_{[x_{j - 1}, x_j]}(f(x))\cdot ((t - x_{j - 1}) + (x_j - t))\le 0 \,\,\,\,\blacksquare$$

2. Пусть $\mathcal{T} = \mathcal{T}_1 \cup \mathcal{T}_2$. Тогда по свойству $1$: 
$$s(\mathcal{T}_1) < s(\mathcal{T}) < S(\mathcal{T}) < S(\mathcal{T}_2) \,\,\,\,\blacksquare$$

3. По лемме $$\displaystyle\sup_{\xi}\left\{\sigma_f(\mathcal{T}(\xi))\right\} = \displaystyle\sup_{\xi}\left\{\displaystyle \sum_{i = 1}^{n}f(\xi_i)\cdot (x_{i} - x_{i - 1})\right\} = \displaystyle \sum_{i = 1}^{n}\displaystyle\sup_{\Delta x_i}\left(f(x)\right)\cdot(x_i - x_{i-1})$$Множеством $X_i$ здесь будет отрезок $\Delta x_i = [x_i, x_{i - 1}]$, так как точная верхняя грань ищется по множеству всех разметок и, следовательно, $\xi_i$ пробегает весь отрезок $\Delta x_i \,\,\,\,\blacksquare$

::::

## Критерий интегрируемости функции по Риману


:::: {#definition-11}

**Определение:**  

$I^{*} = \displaystyle\inf_{\mathcal{T}}S(\mathcal{T})$ -- *верхний интеграл Дарбу*.

$I_{*} = \displaystyle\sup_{\mathcal{T}}s(\mathcal{T})$ -- *нижний интеграл Дарбу*.

Замечание: определение верхнего и нижнего интеграла Дарбу корректно, так как выполняется свойство 2.

::::

:::: {#theorem-3}

**Теорема:**  (*критерий интегрируемости*)

$$f(x) \in R[a, b] \Leftrightarrow \forall \varepsilon > 0 \,\,\,\, \exists \delta: \,\,\,\, \forall \mathcal{T}(\xi) \left(d(\mathcal{T}) < \delta\right) \,\,\,\, S(\mathcal{T}) - s(\mathcal{T}) < \varepsilon$$

*Доказательство:* $$\Rightarrow$$

$f(x) \in R[a, b]$, то есть $\exists I \in \mathbb{R}:\,\,\,\,\forall \varepsilon > 0 \,\,\,\, \exists \delta >0: \,\,\,\, \forall \mathcal{T}(\xi) \left(d(\mathcal{T}) < \delta\right) \,\,\,\, |\sigma_f(\mathcal{T}(\xi)) - I| <\varepsilon$. Следовательно
$$I - \varepsilon < \sigma_f(\mathcal{T}(\xi)) < I + \varepsilon$$
$$\Downarrow$$(переходим к верхней и нижней граням и используем свойства $2$ и $3$)
$$I - \varepsilon \le s(\mathcal{T}) < S(\mathcal{T}) \le I + \varepsilon \,\,\,\,\blacksquare$$

$$\Leftarrow$$

Из определения верхнего и нижнего интегралов Дарбу следует, что $s(\mathcal{T}) \le I_{*} \le I^{*} \le S(\mathcal{T}) \Rightarrow I_{*} = I^{*} = I$. 

Имеем $$\begin{cases}
s(\mathcal{T}) \le I \le S(\mathcal{T})\\
S(\mathcal{T}) - s(\mathcal{T}) < \varepsilon\\
s(\mathcal{T}) \le \sigma_f(\mathcal{T}(\xi)) \le S(\mathcal{T})
\end{cases} \Rightarrow |\sigma_f(\mathcal{T}(\xi)) - I| <\varepsilon \,\,\,\,\blacksquare$$

::::


## Интегрируемость непрерывных и монотонных функций


:::: {#theorem-4}

**Теорема:**  Пусть $f(x) \in C[a, b]$, тогда $f(x) \in R[a, b]$.

*Доказательство:* $\forall \varepsilon > 0$ возьмем $\delta = \varepsilon$, тогда $\forall \mathcal{T}(\xi) (d(\mathcal{T}) < \delta = \varepsilon) \,\,\,\, S(\mathcal{T}) - s(\mathcal{T}) = \displaystyle \sum_{i = 1}^{n}(\sup_{\Delta x_i}(f(x)) - \inf_{\Delta x_i}(f(x)))(x_{i} - x_{i - 1})$
$$= \displaystyle \sum_{i = 1}^{n}(\max_{\Delta x_i}(f(x)) - \min_{\Delta x_i}(f(x)))(x_{i} - x_{i - 1})$$
$$= \displaystyle \sum_{i = 1}^{n}(f(x_{max_i}) - f(x_{min_i}))(x_{i} - x_{i - 1}) \le \displaystyle \sum_{i = 1}^{n}\varepsilon (x_{i} - x_{i - 1}) = \varepsilon (b - a) < \varepsilon \,\,\,\,\blacksquare$$

::::

:::: {#theorem-5}

**Теорема:**  Пусть $f(x)$ монотонна на $[a, b]$, тогда $f(x) \in R[a, b]$.

*Доказательство:* Пусть $f(x)$ монотонно возрастает. $\forall \varepsilon > 0$ возьмем $\delta = \varepsilon$, тогда $\forall \mathcal{T}(\xi) (d(\mathcal{T}) < \delta = \varepsilon) \,\,\,\, S(\mathcal{T}) - s(\mathcal{T}) = \displaystyle \sum_{i = 1}^{n}(\sup_{\Delta x_i}(f(x)) - \inf_{\Delta x_i}(f(x)))(x_{i} - x_{i - 1}) =$
$$=\displaystyle \sum_{i = 1}^{n}(f(x_i) - f(x_{i - 1}))(x_{i} - x_{i - 1})\le$$
$$\le \displaystyle \sum_{i = 1}^{n}(f(x_i) - f(x_{i - 1}))\varepsilon = \varepsilon (f(b) - f(a)) < \varepsilon\,\,\,\,\blacksquare$$

::::

:::: {#definition-12}

**Определение:**  Множество $A \subset \mathbb{R}$ *имеет лебегову меру* $0$, если $\forall \varepsilon \,\,\,\, \exists \{(a_i, b_i)\}_i: \,\,\,\, A \subset \displaystyle\cup_i (a_i, b_i) \,\,\,\, \displaystyle\sup_{N < \infty}\displaystyle \sum_{i = 1}^{N}|b_i - a_i| < \varepsilon$.

::::

:::: {#theorem-6}

**Теорема:**  $f(x) \in R[a, b] \Leftrightarrow$ множество предельных точек $f(x)$ на $[a, b]$ имеет лебегову меру $0$.

*Доказательство:* $\,\,\,\,\blacksquare$

::::

## Основные свойства интегрируемых по Риману функций


### Интегрируемость на подотрезках

:::: {#statement-2}

**Утверждение:**  Пусть $f(x) \in R[a, b]$, тогда $f(x) \in R[a^{*}, b^{*}]$, если $[a^{*}, b^{*}] \subset [a, b]$.

*Доказательство:* Пусть $\mathcal{T}_{[a, b]}$ некоторое разбиение $[a, b]$, $\mathcal{T}_{[a, b]}^{*} = \mathcal{T}_{[a, b]} \cup \{a^{*}, b^{*}\}$. 

Тогда $\varepsilon > S(\mathcal{T}_{[a, b]}) - s(\mathcal{T}_{[a, b]}) \ge S(\mathcal{T}_{[a, b]}^{*}) - s(\mathcal{T}_{[a, b]}^{*})=$
$$= S(\mathcal{T}_{[a, a^{*}]}^{*}) + S(\mathcal{T}_{[a^{*}, b^{*}]}^{*}) + S(\mathcal{T}_{[b^{*}, b]}^{*}) - s(\mathcal{T}_{[a, a^{*}]}^{*}) - s(\mathcal{T}_{[a^{*}, b^{*}]}^{*}) - s(\mathcal{T}_{[b^{*}, b]}^{*})\ge$$
$$\ge S(\mathcal{T}_{[a^{*}, b^{*}]}^{*}) - s(\mathcal{T}_{[a^{*}, b^{*}]}^{*}) \,\,\,\,\blacksquare$$

::::

### Аддитивность

:::: {#statement-3}

**Утверждение:**  Пусть $f(x) \in R[a, b]$ и $f(x) \in R[b, c]$, тогда $f(x) \in R[a, c]$ и $$\displaystyle\int\limits_a^c f(x)dx = \displaystyle\int\limits_a^b f(x)dx + \displaystyle\int\limits_b^c f(x)dx$$

*Доказательство:* Пусть  $b \in \Delta x_j = [x_{j - 1}, x_j]$.
$$S(\mathcal{T}_{[a, c]}) - s(\mathcal{T}_{[a, c]}) = S(\mathcal{T}_{[a, c]} \cup \{b\}) - s(\mathcal{T}_{[a, c]} \cup \{b\})+$$
$$+ \displaystyle\sup_{\Delta_j}f(x)(x_j - x_{j - 1}) - \displaystyle\inf_{\Delta_j}f(x)(x_j - x_{j - 1}) - \displaystyle\sup_{[x_{j - 1}, b]}f(x)(b - x_{j - 1}) - \displaystyle\sup_{[b, x_j]}f(x)(x_j - b)+$$
$$+ \displaystyle\inf_{[x_{j - 1}, b]}f(x)(b - x_{j - 1}) + \displaystyle\inf_{[b, x_j]}f(x)(x_j - b) < 7 \varepsilon \,\,\,\,\blacksquare$$

::::

### Линейность

:::: {#statement-4}

**Утверждение:**  Пусть $f(x), g(x) \in R[a, b], \,\,\,\, \lambda, \mu \in \mathbb{R}$, тогда $$\lambda f(x) + \mu g(x) \in R[a, b]$$

*Доказательство:* $$S_{\lambda f(x) + \mu g(x)}(\mathcal{T}) - s_{\lambda f(x) + \mu g(x)}(\mathcal{T})=$$
$$=\lambda S_{f(x)}(\mathcal{T}) + \mu S_{g(x)}(\mathcal{T}) - \lambda s_{f(x)}(\mathcal{T}) - \mu s_{g(x)}(\mathcal{T})=$$
$$= \lambda (S_{f(x)}(\mathcal{T}) - s_{f(x)}(\mathcal{T})) + \mu (S_{g(x)}(\mathcal{T}) - s_{g(x)}(\mathcal{T})) < (\lambda + \mu) \varepsilon \,\,\,\,\blacksquare$$

::::

### Мега-свойство

:::: {#statement-5}

**Утверждение:**  Пусть $f(x) \in R[a, b]$. Тогда $$\displaystyle\int\limits_a^b f(x)dx \le \displaystyle\sup_{[a, b]} |f(x)| |b - a|$$

*Доказательство:* $$\forall \mathcal{T}(\xi) \,\,\,\, |\sigma_f(\mathcal{T}(\xi))| = \left|\displaystyle \sum_{i = 1}^{n}f(\xi_i)(x_{i} - x_{i - 1})\right| \le \left|\displaystyle \sum_{i = 1}^{n}\sup_{[a, b]} |f(x)| (x_{i} - x_{i - 1})\right| = \displaystyle\sup_{[a, b]} |f(x)| |b - a| \,\,\,\,\blacksquare$$

::::

### Интегрируемость модуля

:::: {#statement-6}

**Утверждение:**  Пусть $f(x) \in R[a, b]$. Тогда $|f(x)| \in R[a, b]$ и $$\left|\displaystyle\int\limits_a^b f(x)dx\right| \le \displaystyle\int\limits_a^b |f(x)|dx$$

*Доказательство:* $$||f(x_2)| - |f(x_1)|| \le |f(x_2) - f(x_1)|$$
Перейдем к супремуму:
$$\displaystyle \sup_{[a, b]}||f(x_2)| - |f(x_1)|| \le \displaystyle\sup_{[a, b]}|f(x_2) - f(x_1)|$$
Так как $\displaystyle\sup_{x, x’ \in [a, b]}|f(x) - f(x’)| = \displaystyle\sup_{[a, b]}f(x) - \displaystyle\inf_{[a, b]}f(x)$, получаем:
$$\displaystyle \sup_{[a, b]}|f(x_2)| - \displaystyle\inf_{[a, b]}|f(x_1)| \le \displaystyle \sup_{[a, b]}f(x_2) - \displaystyle\inf_{[a, b]}f(x_1)$$
$$\Downarrow$$
$$S_{|f|}(\mathcal{T}) - s_{|f|}(\mathcal{T}) \le S_f(\mathcal{T}) - s_f(\mathcal{T}) < \varepsilon  \,\,\,\,\blacksquare$$

::::

### Положительность интеграла от положительной

:::: {#statement-7}

**Утверждение:**  $$f(x) \ge 0 \Rightarrow \displaystyle\int\limits_a^b f(x)dx \ge 0$$

*Доказательство:* $$\forall \mathcal{T}(\xi) \,\,\,\, \sigma_f(\mathcal{T}(\xi)) \ge 0 \,\,\,\,\blacksquare$$

::::

### Более сильная положительность

:::: {#statement-8}

**Утверждение:**  Пусть $f(x) \in R[a, b], \,\,\,\, f(x) \ge 0 \,\,\,\, \forall x \in [a, b], \,\,\,\, \exists c \in [a, b]: \,\,\,\, f(c) > 0$ и $f(x)$ непрерывна в точке $c$. Тогда $$\displaystyle\int\limits_a^b f(x)dx > 0$$

*Доказательство:* $$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x: 0 < |x - c| < \delta \,\,\,\, |f(x) - f(c)| < \varepsilon$$

Пусть $\varepsilon = \frac{f(c)}{2} \Rightarrow \forall x \in (c - \delta, c + \delta) \,\,\,\, f(x) > \frac{f(c)}{2} \Rightarrow \displaystyle\int\limits_{c - \delta}^{c + \delta} f(x)dx > \frac{f(c)}{2} > 0 \Rightarrow \displaystyle\int\limits_a^b f(x)dx > 0 \,\,\,\,\blacksquare$

::::

### Интегрируемость произведения

:::: {#statement-9}

**Утверждение:**  $$f(x), g(x) \in R[a, b] \Rightarrow f(x)g(x) \in R[a, b]$$

*Доказательство:* $|f(x_2)g(x_2) - f(x_1)g(x_1)| = |f(x_2)||g(x_2) - g(x_1)| + |g(x_1)||f(x_2) - f(x_1)| \,\,\,\,\blacksquare$

::::

### Интегрируемость частного

:::: {#statement-10}

**Утверждение:**  Пусть $f(x) \in R[a, b]$ и $\exists \delta > 0: \,\,\,\, \forall x \in [a, b] \,\,\,\, f(x) > \delta$. Тогда $\frac{1}{f(x)} \in R[a, b]$.

*Доказательство:* $$\frac{1}{f(x)} \le \frac{1}{\delta}$$
$$\left|\frac{1}{f(x_2)} - \frac{1}{f(x_1)}\right| \le \frac{1}{\delta^2}|f(x_2) - f(x_1)| \,\,\,\,\blacksquare$$

::::


## Первая теорема о среднем


:::: {#theorem-7}

**Теорема:**  Пусть $f(x), g(x) \in R[a, b], \,\,\,\, g(x) \ge 0, \,\,\,\, m = \displaystyle\inf_{[a, b]} f(x), \,\,\,\, M = \displaystyle\sup_{[a, b]} f(x)$. Тогда $$\exists \mu \in [m, M]: \,\,\,\, \displaystyle\int\limits_a^b f(x)g(x)dx = \mu\displaystyle\int\limits_a^b g(x)dx$$

*Доказательство:* $$m g(x) \le g(x)f(x) \le M g(x) \Rightarrow$$

$$m \displaystyle\int\limits_a^b g(x)dx \le \displaystyle\int\limits_a^b f(x)g(x)dx \le M\displaystyle\int\limits_a^b g(x)dx$$
Если $\displaystyle\int\limits_a^b g(x)dx \ne 0$, то возьмем в качестве $\mu = \,\,\,\, \frac{\displaystyle\int\limits_a^b f(x)g(x)dx}{\displaystyle\int\limits_a^b g(x)dx}$.

Иначе, любое $\mu$ подходит $\,\,\,\,\blacksquare$

::::

# Интеграл с переменным верхним пределом

:::: {#theorem-8}

**Теорема:**  Пусть $f(x) \in R[a, b]$. Тогда $F(x) = \displaystyle\int\limits_a^x f(t)dt$ непрерывна на отрезке $[a, b]$.

*Доказательство:* $f(x) \in R[a, b] \Rightarrow \exists c > 0: \,\,\,\, |f(x)| < c \,\,\,\, \forall x \in [a, b]$.
$|F(x + \Delta x) - F(x)| = \left|\displaystyle\int\limits_a^{x + \Delta x} f(t)dt - \displaystyle\int\limits_a^{x} f(t)dt\right|=$
$= \left|\displaystyle\int\limits_{x}^{x + \Delta x} f(t)dt\right| \le \left|\displaystyle\int\limits_{x}^{x + \Delta x} |f(t)|dt \right| \le |\Delta x|c \,\,\,\,\blacksquare$

::::

:::: {#theorem-9}

**Теорема:**  Пусть $f(x) \in R[a, b]$, $f(x)$ непрерывна в точке $x_0 \in [a, b]$. Тогда $F(x) = \displaystyle\int\limits_a^x f(t)dt$ дифференцируема в точке $x_0$ и $F’(x_0) = f(x_0)$.

*Доказательство:* $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall t: 0 < |t - x_0| < \delta \,\,\,\, |f(t) - f(x_0)| < \varepsilon$.
$\left|\frac{1}{\Delta x}(F(x + \Delta x) - F(x)) - f(x_0)\right| = \left|\frac{1}{\Delta x}\left(\displaystyle\int\limits_a^{x + \Delta x} f(t)dt - \displaystyle\int\limits_a^{x} f(t)dt\right) - f(x_0)\right|=$

$= \left|\frac{1}{\Delta x}\displaystyle\int\limits_x^{x + \Delta x} f(t)dt - \frac{1}{\Delta x}\displaystyle\int\limits_x^{x + \Delta x} f(x_0)dt\right| = \left|\frac{1}{\Delta x}\displaystyle\int\limits_x^{x + \Delta x} (f(t) - f(x_0))dt\right|\le$

$\le \left|\frac{1}{\Delta x}\right|\left|\displaystyle\int\limits_x^{x + \Delta x} |f(t) - f(x_0)|dt\right| \le \varepsilon \left|\frac{1}{\Delta x}\right|\left|\Delta x\right| = \varepsilon \,\,\,\,\blacksquare$

::::

:::: {#corollary-0}

**Следствие:**  Пусть $f(x) \in R[a, b]$ и $f(x) \in C(a, b)$. Тогда $F(x) = \displaystyle\int\limits_a^x f(t)dt$ -- первообразная $f(x)$ на $(a, b)$ и $F(x) \in C[a, b]$.

*Доказательство:*

::::

## Формула Ньютона-Лейбница

:::: {#theorem-10}

**Теорема:** (формула Ньютона-Лейбница) Пусть $f(x) \in R[a, b]$, $\Phi(x)$ -- первообразная $f(x)$ на $(a, b)$. Тогда $$\displaystyle\int\limits_a^b f(x)dx = \Phi(b) - \Phi(a)$$

*Доказательство:* $\displaystyle\int\limits_a^x f(t)dt = \Phi(x) + C$, так как один и два. Подставим $x = a \Rightarrow C = -\Phi(a) \Rightarrow \displaystyle\int\limits_a^x f(t)dt = \Phi(x) - \Phi(a)$, подставляя $x = b$, получаем требуемое равенство $\,\,\,\,\blacksquare$

::::

:::: {#theorem-11}

**Теорема:**  (обобщение формулы Ньютона-Лейбница) Пусть $f(x) \in R[a, b]$ и $f(x) \in C([a, b] \setminus \{x_i\}_{i = 1}^n)$, $\Phi(x) \in C^([a, b])$, $\Phi’(x) = f(x) \,\,\,\, \forall x \in [a, b] \setminus \{x_i\}_{i = 1}^n$. Тогда $$\displaystyle\int\limits_a^b f(x)dx = \Phi(b) - \Phi(a)$$

*Доказательство:* Пусть $x_0 = a, \,\,\,\, x_{n + 1} = b$. Тогда $\displaystyle\int\limits_a^b f(x)dx = \displaystyle \sum_{i = 0}^{n}\displaystyle\int\limits_{x_i}^{x_{i + 1}} f(x)dx = \displaystyle \sum_{i = 0}^{n} \Phi(x_{i + 1}) - \Phi(x_{i}) = \Phi(b) - \Phi(a) \,\,\,\,\blacksquare$

::::

## Интегрирование по частям и замена переменной для определенного интеграла


:::: {#theorem-12}

**Теорема:**  (замена переменной при интегрировании определенного интеграла) Пусть $f(x) \in R[a, b], \,\,\,\, \varphi(t) \in C^{1}[\alpha, \beta]$($\varphi(x)$ непрерывна, и ее производная непрерывна), $\varphi([\alpha, \beta]) \subset [a, b], \,\,\,\,\varphi(\alpha) = a, \,\,\,\, \varphi(\beta) = b$. Тогда 
$$\displaystyle\int\limits_a^b f(x)dx = \displaystyle\int\limits_{\alpha}^{\beta} f(\varphi(t))\varphi’(t)dt$$

*Доказательство:* Пусть $\Phi(x)$ -- первообразная $f(x)$ на $(a, b) \Rightarrow \Phi(\varphi(t))$ -- первообразная для $f(\varphi(t))\varphi’(t)$.
$$\displaystyle\int\limits_{\alpha}^{\beta} f(\varphi(t))\varphi’(t)dt = \Phi(\varphi(\beta)) - \Phi(\varphi(\alpha)) = \displaystyle\int\limits_a^b f(x)dx \,\,\,\,\blacksquare$$

::::

:::: {#theorem-13}

**Теорема:**  (интегрирование по частям определенного интеграла) Пусть $f(x), g(x) \in R[a, b]$. Тогда $$\displaystyle\int\limits_a^b f(x)g’(x)dx = \left.f(x)g(x)\right\rvert_{a}^{b} - \displaystyle\int\limits_a^b f’(x)g(x)dx$$

*Доказательство:* $$\left.f(x)g(x)\right\rvert_{a}^{b} = \displaystyle\int\limits_a^b \left(f(x)g(x)\right)’dx \,\,\,\,\blacksquare$$

::::

## Вторая теорема о средних


:::: {#theorem-14}

**Теорема:**  Пусть $f(x) \in C[a, b], \,\,\,\, g(x) \in C^1[a, b], \,\,\,\, g(x)$ -- монотонно возрастает. Тогда $\exists c \in [a, b]$:

$$\displaystyle\int\limits_a^b f(x)g(x)dx = g(a)\displaystyle\int\limits_a^c f(x)dx + g(b)\displaystyle\int\limits_c^b f(x)dx$$

*Доказательство:* $F(x) = \displaystyle\int\limits_x^b f(t)dt$
$$\displaystyle\int\limits_a^b f(x)g(x)dx = -\displaystyle\int\limits_a^b g(x)dF(x) = -\left.g(x)F(x)\right|_{a}^{b} + \displaystyle\int\limits_a^b F(x)g’(x)dx=$$
$$= g(a) \displaystyle\int\limits_a^b f(x)dx + F(c) \displaystyle\int\limits_a^b g’(x)dx=$$
$$= g(a) \displaystyle\int\limits_a^b f(x)dx + \displaystyle\int\limits_c^b f(x)dx (g(b) - g(a))=$$
$$= g(a)\displaystyle\int\limits_a^c f(x)dx + g(b)\displaystyle\int\limits_c^b f(x)dx \,\,\,\,\blacksquare$$

::::

# Кривые


:::: {#statement-11}

**Утверждение:**   Отображение $\gamma: [a, b] \to \mathbb{R}^n, \,\,\,\, \gamma(t): t \in [a, b] \mapsto (x_1(t), \ldots, x_n(t))$ -- непрерывно на $[a, b]$, тогда и только тогда, когда $x_i(t)$ -- непрерывно на $[a, b] \,\,\,\, \forall i \in \{1, \ldots, n\}$.

*Доказательство:*

::::

:::: {#definition-13}

**Определение:**  Непрерывное отображение $\gamma: [a, b] \to \mathbb{R}^n$ -- это *(непрерывная) кривая*.

$t \in [a, b] \,\,\,\, \gamma(t) = (x_1(t), \ldots, x_n(t))$, где $x_1(t)$ -- *первая координата*...

$\forall t \in [a, b] \,\,\,\, M = \gamma(t)$ -- *точка* кривой $\gamma$.

Если $\exists t_1 \ne t_2 (t_1, t_2 \in [a, b]): \,\,\,\, M = \gamma(t_1) = \gamma(t_2)$, то $M$ *точка самопересечения* кривой $\gamma$.

$\operatorname{card}\{t: \,\,\,\, M = \gamma(t), \,\,\,\, t \in [a, b]\}$ -- *кратность* точки $M$.

Если точек самопересечения нет, то кривая $\gamma$ -- *простая*.

Если существует единственная точка самопересечения и ее кратность равна $2$, то кривая $\gamma$ -- *простая замкнутая*.

::::

:::: {#definition-14}

**Определение:**  Пусть $\mathcal{T} = \{t_i\}_{i = 0}^k$ разбиение $[a, b]$, $\gamma$ -- кривая.

$|l_{\gamma}(\mathcal{T})| = \displaystyle \sum_{i = 1}^{k}|\gamma(t_i) - \gamma(t_{i - 1})|$ -- *длина ломаной*, отвечающей разметке $\mathcal{T}$.

::::

:::: {#lemma-1}

**Лемма:** Если $\mathcal{T}_1 \subset \mathcal{T}_2$, то 
$$|l_{\gamma}(\mathcal{T}_1)| \le |l_{\gamma}(\mathcal{T}_2)|$$

*Доказательство:* $\mathcal{T}_2 \setminus \mathcal{T}_1 = \{t^{*}\}, \,\,\,\, t_{j - 1} < t^{*} < t_j$. <br>$|l_{\gamma}(\mathcal{T}_2)| - |l_{\gamma}(\mathcal{T}_1)| \ge 0$ -- неравенство треугольника в плоскости $\{\gamma(t_{j - 1}), \gamma(t^{*}), \gamma(t_{j})\} \,\,\,\,\blacksquare$

::::

:::: {#definition-15}

**Определение:**  Пусть $\gamma$ -- кривая. Если множество $\{|l_{\gamma}(\mathcal{T})|\}_{\mathcal{T}}$ ограничено сверху, то $\gamma$ *спрямляемая* и $\sup \{|l_{\gamma}(\mathcal{T})|\}_{\mathcal{T}} = |\gamma|$ -- *длина кривой* $\gamma$.

::::

:::: {#theorem-15}

**Теорема:**  Пусть $\gamma(t) \in C^1[a, b]$. Тогда $\gamma$ -- спрямляемая и
$$|\gamma| = \displaystyle\int\limits_a^b \sqrt{\displaystyle \sum_{i = 1}^{n} x_i’^2(t)} dt$$

*Доказательство:* Докажем, что $\gamma$ спрямляемая, то есть $\{|l_{\gamma}(\mathcal{T})|\}_{\mathcal{T}}$ ограничено сверху.
$$|l_{\gamma}(t)| = \displaystyle \sum_{j = 1}^{m} \sqrt{\displaystyle \sum_{i = 1}^{n}(x_i(t_j) - x_i(t_{j - 1}))^2} =$$
$$=\displaystyle \sum_{j = 1}^{m} \sqrt{\displaystyle \sum_{i = 1}^{n}x_i’^2(\xi_{ij}) (t_j - t_{j - 1})^2} = \displaystyle \sum_{j = 1}^{m} \sqrt{\displaystyle \sum_{i = 1}^{n}x_i’^2(\xi_{ij})} |t_j - t_{j - 1}|\le$$
$$\le M \sqrt{n} (b - a)$$
Следовательно, $\gamma$ спрямляемая.

::::

:::: {#lemma-2}

**Лемма:**  $$\sqrt{\displaystyle \sum_{i = 1}^{n}x_i^2} - \sqrt{\displaystyle \sum_{i = 1}^{n}y_i^2} \le \displaystyle \sum_{i = 1}^{n}|x_i - y_i|$$

*Доказательство:* домножить на сопряженное и поколдовать $\,\,\,\,\blacksquare$

::::

$f(t) = \sqrt{\displaystyle \sum_{i = 1}^{n} x_i’^2(t)}$ -- композиция суммы непрерывных функций непрерывна, а следовательно $$\exists \displaystyle\int\limits_a^b \sqrt{\displaystyle \sum_{i = 1}^{n} x_i’^2(t)} dt = I$$

1. $$\forall \varepsilon > 0 \,\,\,\, \exists \delta_1 > 0: \,\,\,\, \forall \mathcal{T} (d(\mathcal{T}) < \delta_1) \,\,\,\, |\sigma_f(\mathcal{T}) - I| < \varepsilon$$
2. $$||l_{\gamma}(\mathcal{T})| - \sigma_f(\mathcal{T})| = \left|\displaystyle \sum_{j = 1}^{m} \sqrt{\displaystyle \sum_{i = 1}^{n}x_i’^2(\xi_{ij})} |t_j - t_{j - 1}| - \sigma_f(\mathcal{T})\right|=$$
$$=\left|\displaystyle \sum_{j = 1}^{m} \sqrt{\displaystyle \sum_{i = 1}^{n}x_i’^2(\xi_{ij})} |t_j - t_{j - 1}| - \displaystyle \sum_{j = 1}^{m}\sqrt{\displaystyle \sum_{i = 1}^{n} x_i’^2(\xi_j)}|t_j - t_{j - 1}|\right| \le$$
$$\le \left|\displaystyle \sum_{j = 1}^{m} \displaystyle \sum_{i = 1}^{n}|x_i’(\xi_{ij}) - x_i’(\xi_j)| |t_j - t_{j - 1}|\right|$$ 
$$\forall \varepsilon > 0 \,\,\,\, \exists \delta_2 > 0: \,\,\,\, \forall \xi_{ij}, \xi_j: \,\,\,\, |\xi_{ij} - \xi_j| < \delta \,\,\,\, |x_i’(\xi_{ij}) - x_i’(\xi_j)| < \varepsilon \Rightarrow$$
$$\forall \frac{\varepsilon}{n(b - a)} \,\,\,\, ||l_{\gamma}(t)| - \sigma_f(\mathcal{T})| < \varepsilon$$
3. $$|\gamma| = \sup_{\mathcal{T}}\{|l_{\gamma}(\mathcal{T})|\} \Rightarrow |\gamma| - |l_{\gamma}(\mathcal{T})| < \varepsilon$$

$$\Downarrow$$

$$|\gamma| - I < \varepsilon \Rightarrow I = |\gamma| \,\,\,\,\blacksquare$$


# Фигуры и площади


:::: {#definition-16}

**Определение:**  $A \subset \mathbb{R}^2$ -- *плоская фигура*.

$(x, y) \in A$ -- *точка* фигуры.

$B_{\varepsilon}(x_0, y_0) = \{(x, y) \in A: \,\,\,\, (x - x_0)^2 + (y - y_0)^2 < \varepsilon^2\}$ - $\varepsilon$-*окрестность* точки $(x_0, y_0) \in A$.

::::

:::: {#definition-17}

**Определение:**  Пусть $\{A_{\alpha}\}_{\alpha}$ -- множество плоских фигур.

Отображение $\mu: \,\,\,\, \{A_{\alpha}\}_{\alpha} \to \mathbb{R}$ -- *площадь* фигуры, если:

1. $\forall A \,\,\,\, \mu(A_{\alpha}) \ge 0$.
2. $\forall A_1, A_2: \,\,\,\, A_1 \cap A_2 = \varnothing \,\,\,\, \mu(A_1) + \mu(A_2) = \mu(A_1 \cup A_2)$.
3. $\forall A_1, A_2: \,\,\,\, A_1 \subset A_2 \,\,\,\, \mu(A_1) \le \mu(A_2)$.
4. Площадь фигур, которые можно совместить движением, одинакова.
5. Площадь прямоугольника со сторонами $a \ge 0$ и $b \ge 0$ равна $a\cdot b$.

::::

:::: {#statement-12}

**Утверждение:**  Площадь открытого и замкнутого прямоугольников равны.

*Доказательство:* очев $\,\,\,\,\blacksquare$

::::

:::: {#statement-13}

**Утверждение:**  Площадь прямоугольного треугольника с катетами $a$ и $b$ равна $\frac{1}{2}ab$.

*Доказательство:* половина прямоугольника $\,\,\,\,\blacksquare$

::::

:::: {#statement-14}

**Утверждение:**  Площадь треугольника с основанием $a$ и высотой $h$ равна $\frac12 ah$.

*Доказательство:* сумма двух прямоугольных треугольников $\,\,\,\,\blacksquare$

::::

:::: {#definition-18}

**Определение:**  Плоская фигура, состоящая из непересекающихся треугольников -- *многоугольная фигура*. Пустое множество является многоугольной фигурой по определению.

::::

:::: {#statement-15}

**Утверждение:**  Площадь многоугольной фигуры равна сумме площадей составляющих ее треугольников и не зависит от разбиения на треугольники.

*Доказательство:* определение площади $\,\,\,\,\blacksquare$

::::

## Верхняя и нижняя площади


:::: {#definition-19}

**Определение:**  Пусть $A \subset \mathbb{R}^2$ -- плоская фигура.

Любое замкнутое множество $P$, такое что $A \subset P$ -- *описанная* около $A$ фигура.

Любое открытое множество $Q$, такое что $Q \subset A$ -- *вписанная* в $A$ фигура.

::::

:::: {#statement-16}

**Утверждение:**  Пусть $A$ -- ограниченная плоская фигура. Тогда множество площадей описанных около нее фигур ограничено снизу, а множество площадей вписанных в нее фигур ограничено сверху.

*Доказательство:* очев $\,\,\,\,\blacksquare$

::::

:::: {#definition-20}

**Определение:**  Пусть $A$ -- ограниченная плоская фигура, $\{P\}$ -- множество всех описанных около нее фигур, $\{Q\}$ -- множество всех вписанных в нее фигур.

$\mu^{*}(A) = \displaystyle\inf_{P}\mu(P)$ -- *верхняя площадь* фигуры $A$.

$\mu_{*}(A) = \displaystyle\sup_{Q}\mu(Q)$ -- *нижняя площадь* фигуры $A$.

Если $\mu(A) = \mu^{*}(A) = \mu_{*}(A)$, то $A$ -- *квадрируема* (имеет площадь по-русски).

::::

## Равенство определенного интеграла площади под графиком функции


:::: {#statement-17}

**Утверждение:**  (первый критерий квадрируемости) Пусть $A$ -- ограниченная плоская фигура. Тогда $A$ -- квадрируема $\Leftrightarrow \,\,\,\, \forall \varepsilon > 0 \,\,\,\, \exists P, Q: \,\,\,\, \mu(P) - \mu(Q) < \varepsilon$.

*Доказательство:* $$\Rightarrow$$
$A$ -квадрируема, следовательно $\mu^{*}(A) = \mu_{*}(A)$.
$$\left.\begin{array}{c}
\forall \varepsilon > 0 \,\,\,\, \exists P: \,\,\,\, \mu(P) - \mu^{*}(A) < \frac{\varepsilon}{2}\\
\forall \varepsilon > 0 \,\,\,\, \exists Q: \,\,\,\, \mu_{*}(A) - \mu(Q) < \frac{\varepsilon}{2}
\end{array}\right\} \Rightarrow \mu(P) - \mu(Q) < \varepsilon$$
$$\Leftarrow$$
$$\forall \varepsilon > 0 \,\,\,\, \exists P, Q: \,\,\,\, \mu^{*}(A) - \mu_{*}(A) \le \mu(P) - \mu(Q) < \varepsilon \Rightarrow \mu^{*}(A) = \mu_{*}(A) \,\,\,\,\blacksquare$$

::::

:::: {#statement-18}

**Утверждение:**  (геометричекий смысл интеграла Римана) Пусть $f(x) \in R[a, b], \,\,\,\, f(x) \ge 0 \,\,\,\, \forall x \in [a, b]$. 

Тогда фигура $A = \{(x, y): \,\,\,\, a \le x \le b, 0 \le y \le f(x)\}$ -- квадрируема и ее площадь равна $\displaystyle\int\limits_a^b f(x)dx$.

*Доказательство:* $f(x)$ -- интегрируема на $[a, b]$, следовательно $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall \mathcal{T} (d(\mathcal{T}) < \delta) \,\,\,\, S(\mathcal{T}) - s(\mathcal{T}) < \varepsilon$. Для любой разметки $S(\mathcal{T})$ -- это площадь описанной около $A$ фигуры, а $s(\mathcal{T})$ -- площадь вписанной в $A$ фигуры $\,\,\,\,\blacksquare$

::::

:::: {#theorem-16}

**Теорема:**  (второй критерий квадрируемости) Плоская фигура $A$ квадрируема $\Leftrightarrow \,\,\,\, \mu^{*}(\partial A) = 0$.
($\partial A$ -- множество граничных точек $A$)

*Доказательство:* запомните, что нужно получить $32 \varepsilon$ и вперед $\,\,\,\,\blacksquare$

::::


# Несобственные интегралы


:::: {#definition-21}

**Определение:**  Пусть функция $f(t)$ определена на полуинтервале $[a, b)$ и $f(t) \in R[a, x]\,\,\,\, \forall x \in [a, b)$. $\displaystyle\lim_{x \to b-0}\displaystyle\int\limits_a^x f(t)dt$ -- *несобственный интеграл I рода* функции $f(t)$ на $[a, b)$.

Если $\displaystyle\lim_{x \to b-0}\displaystyle\int\limits_a^x f(t)dt$ существует, то несобственный интеграл I рода -- *сходящийся*.

Если $\displaystyle\lim_{x \to b-0}\displaystyle\int\limits_a^x f(t)dt$ не существует, то несобственный интеграл I рода -- *расходящийся*.

Обозначается: $\displaystyle\int\limits_a^b f(t)dt$.

::::

:::: {#definition-22}

**Определение:**  Пусть функция $f(t)$ определена на $[a, +\infty)$ и $f(t) \in R[a, x]\,\,\,\, \forall x \in [a, +\infty)$. $\displaystyle\lim_{x \to +\infty}\displaystyle\int\limits_a^x f(t)dt$ -- *несобственный интеграл II рода* функции $f(t)$ на $[a, +\infty)$.

Если $\displaystyle\lim_{x \to +\infty}\displaystyle\int\limits_a^x f(t)dt$ существует, то несобственный интеграл II рода -- *сходящийся*.

Если $\displaystyle\lim_{x \to +\infty}\displaystyle\int\limits_a^x f(t)dt$ не существует, то несобственный интеграл II рода -- *расходящийся*.

Обозначается: $\displaystyle\int\limits_a^{+\infty} f(t)dt$.

::::

:::: {#theorem-17}

**Теорема:**  (*критерий Коши существования несобственного интеграла*) 
$$\exists \displaystyle\int\limits_a^{+\infty} f(x)dx \Leftrightarrow \forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x_1, x_2 > \delta \,\,\,\, \left|\displaystyle\int\limits_{x_1}^{x_2} f(x)dx\right| < \varepsilon$$

*Доказательство:* критерий Коши для функции $\,\,\,\,\blacksquare$

::::

## Свойства несобственного интеграла


:::: {#statement-19}

**Утверждение:**  

1. (линейность) Пусть $\exists \displaystyle\int\limits_a^w f(x)dx$ и $\exists \displaystyle\int\limits_a^w g(x)dx$. Тогда $\forall \alpha, \beta \in \mathbb{R} \,\,\,\, \exists \alpha \displaystyle\int\limits_a^w f(x)dx + \beta \displaystyle\int\limits_a^w g(x)dx$.

*Доказательство:* пределы $\,\,\,\,\blacksquare$

2. (интегрирование по частям) Пусть существует два из трех: $\displaystyle\int\limits_a^w f’(x)g(x)dx$, $\displaystyle\int\limits_a^w f(x)g’(x)dx$, $\displaystyle\lim_{x \to w}f(x)g(x)$. Тогда существует третье и выполнено:
$$\displaystyle\int\limits_a^w f’(x)g(x)dx = \displaystyle\lim_{x \to w}f(x)g(x) - \displaystyle\int\limits_a^w f(x)g’(x)dx$$

*Доказательство:* $\,\,\,\,\blacksquare$

3. (замена переменной) Пусть $\exists \displaystyle\int\limits_a^w f(x)dx$, $\varphi(t) \in C^1[\alpha, w_1)$, $\varphi(\alpha) = a$, $0 \le \varphi(t) < w_1$, $\displaystyle\lim_{t \to w_1}f(t) = w$. Тогда $$\displaystyle\int\limits_a^w f(x)dx = \displaystyle\int\limits_{\alpha}^{w_1} f(\varphi(t)) \varphi’(t) dt$$

*Доказательство:* 

4. (интегрирование неравенств) Пусть $\exists \displaystyle\int\limits_a^w f(x)dx$ и $\exists \displaystyle\int\limits_a^w g(x)dx$. Пусть $f(x) \le g(x) \,\,\,\, \forall x \in [a, w)$. Тогда $$\displaystyle\int\limits_a^w f(x)dx \le \displaystyle\int\limits_a^w g(x)dx$$

*Доказательство:* пределы $\,\,\,\,\blacksquare$

5. (модуль) Если $\exists \displaystyle\int\limits_a^w |f(x)|dx$, то $\exists \displaystyle\int\limits_a^w f(x)dx$ и $$\left|\displaystyle\int\limits_a^w f(x)dx\right| \le \left|\displaystyle\int\limits_a^w |f(x)|dx\right|$$

*Доказательство:* $$\left|\displaystyle\int\limits_{x_1}^{x_2} f(x)dx\right| \le \left|\displaystyle\int\limits_{x_1}^{x_2} |f(x)|dx\right| < \varepsilon \,\,\,\,\blacksquare$$

::::

:::: {#definition-23}

**Определение:**  

Если $\exists \displaystyle\int\limits_a^w |f(x)|dx$, то $\displaystyle\int\limits_a^w f(x)dx$ -- *абсолютно сходящийся*.

Если $\exists \displaystyle\int\limits_a^w f(x)dx$ и $\not\exists \displaystyle\int\limits_a^w |f(x)|dx$, то $\displaystyle\int\limits_a^w f(x)dx$ -- *условно сходящийся*.

::::

## Признаки сходимости несобственного интеграла


:::: {#theorem-18}

**Теорема:**  Пусть $0 \le f(x) \le g(x)$.

Если $\exists \displaystyle\int\limits_a^w g(x)dx$, то $\exists \displaystyle\int\limits_a^w f(x)dx$.

Если $\not\exists \displaystyle\int\limits_a^w f(x)dx$, то $\not\exists \displaystyle\int\limits_a^w g(x)dx$.

*Доказательство:* $\forall b \in [a, w) \,\,\,\, 0 \le \displaystyle\int\limits_a^b f(x)dx \le \displaystyle\int\limits_a^b g(x)dx$. Далее переходим к пределам, если $\exists \displaystyle\int\limits_a^w g(x)dx$, то $F(b) = \displaystyle\int\limits_a^b f(x)dx$ ограничена, также $F(b)$ монотонна(по аддитивности интеграла), а следовательно $\exists\displaystyle\int\limits_a^w f(x)dx$(почему?) $\,\,\,\,\blacksquare$

::::

:::: {#theorem-19}

**Теорема:**  Если $\displaystyle\lim_{x \to w}\frac{f(x)}{g(x)} = 1$ и $f(x), g(x) > 0$, то интегралы $\displaystyle\int\limits_a^w g(x)dx$ и $\displaystyle\int\limits_a^w f(x)dx$ сходятся или расходятся одновременно.

*Доказательство:* Взять $\varepsilon = 1$ для предела и по предыдущей теореме.

::::

:::: {#theorem-20}

**Теорема:**  (признак Дирихле $(\mathcal{D})$ и Абеля $(\mathcal{A})$)

Пусть $f(x)$ и $g(x)$ ограничены на $[a, w)$, $g(x)$ монотонна на $[a, w)$, $\forall b \in [a, w) \,\,\,\, \displaystyle\int\limits_a^b f(x)dx$ и $\displaystyle\int\limits_a^b g(x)dx$ и выполнены условия второй теоремы о средних.

1. $(\mathcal{A})$ Если $\exists \displaystyle\int\limits_a^w f(x)dx$, то $\exists \displaystyle\int\limits_a^w f(x)g(x)dx$.
2. $(\mathcal{D})$ Если $\displaystyle\lim_{x\to w}g(x) = 0$ и $\exists M > 0: \,\,\,\, \forall x_1, x_2 \in [a, w) \,\,\,\, \left|\displaystyle\int\limits_{x_1}^{x_2} f(x)dx\right| < M$, то $\exists \displaystyle\int\limits_a^w f(x)g(x)dx$.

*Доказательство:* 

$$\left|\displaystyle\int\limits_{x_1}^{x_2} f(x)g(x)dx\right| = \left|g(x_1)\displaystyle\int\limits_{x_1}^{\xi} f(x)dx + g(x_2)\displaystyle\int\limits_{\xi}^{x_2} f(x)dx\right|\le$$
$$\le |g(x_1)|\left|\displaystyle\int\limits_{x_1}^{\xi} f(x)dx\right| + |g(x_2)|\left|\displaystyle\int\limits_{\xi}^{x_2} f(x)dx\right| \le \begin{cases}
(\mathcal{A}) \sup|g(x)|\cdot 2 \varepsilon\\
(\mathcal{D}) M \cdot 2 \varepsilon    
\end{cases} \,\,\,\,\blacksquare$$

::::

## Главное значение интеграла в смысле Коши


:::: {#definition-24}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$ и не ограничена в точке $c \in (a, b)$. Если $\exists \displaystyle\lim_{\varepsilon \to 0+0}\left(\displaystyle\int\limits_a^{c - \varepsilon} f(x)dx + \displaystyle\int\limits_{c + \varepsilon}^b f(x)dx \right)$, то он обозначается $v.p.\displaystyle\int\limits_a^b f(x)dx$ и называется *главное значение интеграла* $\displaystyle\int\limits_a^b f(x)dx$ *в смысле Коши*.

::::

:::: {#definition-25}

**Определение:**  Пусть $f(x)$ определена на $\mathbb{R}$ и не ограничена. Если $\exists \displaystyle\lim_{a \to +\infty}\displaystyle\int\limits_{-a}^{a} f(x)dx$, то он обозначается $v.p.\displaystyle\int\limits_{-\infty}^{+\infty} f(x)dx$ и называется *главное значение интеграла* $\displaystyle\int\limits_{-\infty}^{+\infty} f(x)dx$ *в смысле Коши*.

::::

:::: {#statement-20}

**Утверждение:**  $$\exists v.p.\displaystyle\int\limits_{-\infty}^{+\infty} f(x)dx \Leftrightarrow \exists \displaystyle\int\limits_0^{+\infty} (f(x) - f(-x))dx$$

*Доказательство:* $f(x) = \frac{f(x) - f(-x)}{2} + \frac{f(x) + f(-x)}{2}$, где одна из дробей четная функция, а другая нечетная, интеграл от нечетной -- ноль $\,\,\,\,\blacksquare$

::::

# Функции ограниченной вариации


:::: {#definition-26}

**Определение:**  Пусть $\mathcal{T} = \{x_i\}_{i = 0}^n$ разбиение отрезка $[a, b]$. $f(x)$ определена на $[a, b]$.

Величина $\operatorname{V}(f, \mathcal{T}) = \displaystyle \sum_{i = 1}^{n}|f(x_i) - f(x_{i - 1})|$ -- *вариация функции* $f(x)$ *на разбиении* $\mathcal{T}$.

::::

:::: {#definition-27}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$.

Если множество вариаций функции $f(x)$ по всем разбиениям ограничено, то $f(x)$ -- *функция ограниченной вариации*.

Величина $\operatorname{V}_a^b f(x) = \displaystyle\sup_{\mathcal{T}_{[a,b]}}\operatorname{V}(f, \mathcal{T}_{[a,b]})$ -- *(полная) вариация функции* $f(x)$ на $[a, b]$.

$\operatorname{V}[a, b]$ -- множество всех функций ограниченной вариации на $[a, b]$.

::::

## Свойства функций ограниченной вариации


:::: {#statement-21}

**Утверждение:**  

1. Пусть $f(x) \in \operatorname{V}[a, b]$. Тогда $f(x)$ ограничена на $[a, b]$.

2. Пусть $\mathcal{T}_{[a, b]}^{*}$ измельчение $\mathcal{T}_{[a, b]}$. Тогда $\operatorname{V}(f, \mathcal{T}) \le \operatorname{V}(f, \mathcal{T}^{*})$.

3. Пусть $f(x) \in \operatorname{V}[a, b]$. Если $c \in (a, b)$, то $f(x) \in \operatorname{V}[a, c]$, $f(x) \in \operatorname{V}[c, d]$ и $\operatorname{V}_a^b f(x) = \operatorname{V}_a^c f(x) + \operatorname{V}_c^d f(x)$.

4. Пусть $f(x), g(x) \in \operatorname{V}[a, b]$. Тогда 

a. $\forall \alpha, \beta \in \mathbb{R} \,\,\,\, \alpha f(x) + \beta g(x) \in \operatorname{V}[a, b]$.
b. $f(x) \circ g(x) \in \operatorname{V}[a, b]$.

5. Если $f(x)$ монотонна на $[a, b]$, то $f(x) \in V[a, b]$.

*Доказательство:* 

::::

## Представление функции ограниченной вариации в виде разности монотонных


:::: {#theorem-21}

**Теорема:**  Пусть $f(x) \in \operatorname{V}[a, b]$. Тогда существуют монотонные на $[a, b]$ функции $v(x)$ и $w(x)$, такие что $f(x) = v(x) - w(x)$.

*Доказательство:* Пусть $v(x) = \operatorname{V}_a^x f(x)$ -- монотонно возрастает, так как аддитивна.

Рассмотрим $w(x) = v(x) - f(x)$. Докажем, что $w(x)$ монотонно возрастает. Пусть $x_2 > x_1$. $w(x_2) - w(x_1) = v(x_2) - v(x_1) - (f(x_2) - f(x_1)) =$
$= \operatorname{V}_{x_2}^{x_1}f(x) - (f(x_2) - f(x_1)) \ge 0$, так как $\operatorname{V}_{x_2}^{x_1}f(x) \ge |f(x_2) - f(x_1)|\,\,\,\,\blacksquare$

::::

:::: {#theorem-22}

**Теорема:**  Если $f(x) \in C^{1}[a, b]$, то $f(x) \in \operatorname{V}[a, b]$ и 
$$\operatorname{V}_a^b f(x) = \displaystyle\int\limits_a^b |f’(x)|dx$$

*Доказательство:* $$V(f, \mathcal{T}) = \displaystyle \sum_{i = 1}^{n}|f(x_i) - f(x_{i - 1})| = \displaystyle \sum_{i = 1}^{n}|f’(\xi_i)|(x_i - x_{i - 1}) \le M\cdot(b - a)$$

$$M = \displaystyle\max_{[a, b]}|f’(x)| \Rightarrow f(x) \in V[a, b]$$

$$I = \displaystyle\int\limits_a^b |f’(x)|dx$$

$$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \forall \mathcal{T} (d(\mathcal{T}) < \delta) \,\,\,\, |\operatorname{V}(f, \mathcal{T}) - I| = \left|\displaystyle \sum_{i = 1}^{n}|f(x_i) - f(x_{i - 1})| - I\right|=$$
$$= \left|\displaystyle \sum_{i = 1}^{n}|f’(\xi_i)(x_i - x_{i - 1})| - I\right| = \left|\sigma_{|f’|}(\mathcal{T}(\{\xi_i\}))\right| < \varepsilon$$

Достаточно доказать для конкретной разметки, получающейся при применении формулы Лагранжа, потому что интеграл уже существует(функция непрерывна), то есть нужно доказать равенство.

$$\forall \varepsilon > 0 \,\,\,\, \exists \mathcal{T}_{\varepsilon}^{*}: \,\,\,\, |\operatorname{V}_a^b f(x) - \operatorname{V}(f, \mathcal{T}_{\varepsilon}^{*})| < \varepsilon$$

Измельчаем $\mathcal{T}^{*}$ до $\mathcal{T}^{**}$, так чтобы $d(\mathcal{T}^{**}) < \delta$.

$$\begin{cases}
|\operatorname{V}_a^b f(x) - \operatorname{V}(f, \mathcal{T}_{\varepsilon}^{**})| < \varepsilon\\
|\operatorname{V}(f, \mathcal{T}_{\varepsilon}^{**}) - I| < \varepsilon    
\end{cases} \Rightarrow |\operatorname{V}_a^b f(x) - I| < 2 \varepsilon \Rightarrow \operatorname{V}_a^b f(x) = I \,\,\,\,\blacksquare$$

::::

# Интеграл Римана-Стилтьеса


:::: {#definition-28}

**Определение:**  Пусть $f(x)$ и $g(x)$ определена на $[a, b]$. Для $\mathcal{T}_{[a, b]}(\xi)$ сумма:

 $$\sigma_f(g, \mathcal{T}(\xi)) = \displaystyle \sum_{i  = 1}^{n}f(\xi_i)(g(x_i) - g(x_{i - 1}))$$
 *интегральная сумма Стилтьеса* для $f(x)$ по $g(x)$ на $[a, b]$.

::::

:::: {#definition-29}

**Определение:**  Если $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall \mathcal{T}(\xi) (d(\mathcal{T}(\xi)) < \delta)$

$|\sigma_f(g, \mathcal{T}(\xi)) - I| < \varepsilon$, то $f(x)$ *интегрируема по* $g(x)$ на $[a, b]$.

Обозначается: $\displaystyle\int\limits_a^b f(x)dg(x)$

::::

## Свойства интеграла Стилтьеса

:::: {#statement-22}

**Утверждение:**  

1. Если $\exists \displaystyle\int\limits_a^b f_1(x)dg(x)$ и $\exists \displaystyle\int\limits_a^b f_2(x)dg(x)$, то
$\exists \displaystyle\int\limits_a^b (\alpha f_1(x) + \beta f_2(x))dg(x) = \alpha \displaystyle\int\limits_a^b f_1(x)dg(x) + \beta \displaystyle\int\limits_a^b f_2(x)dg(x)$.
*Доказательство:* очев $\,\,\,\,\blacksquare$

2. Если $\exists \displaystyle\int\limits_a^b f(x)dg_1(x)$ и $\exists \displaystyle\int\limits_a^b f(x)dg_2(x)$, то
$\exists \displaystyle\int\limits_a^b f(x)d(\alpha g_1(x) + \beta g_2(x)) = \alpha \displaystyle\int\limits_a^b f(x)dg_1(x) + \beta \displaystyle\int\limits_a^b f(x)dg_2(x)$.

*Доказательство:* очев $\,\,\,\,\blacksquare$

3. Если $\exists \displaystyle\int\limits_a^b f(x)dg(x)$, $\exists \displaystyle\int\limits_a^c f(x)dg(x)$ и $\exists \displaystyle\int\limits_c^b f(x)dg(x)$ для $c \in (a, b)$, то $$\displaystyle\int\limits_a^b f(x)dg(x) = \exists \displaystyle\int\limits_a^c f(x)dg(x) + \exists \displaystyle\int\limits_c^b f(x)dg(x)$$

*Доказательство:* записать определение $\,\,\,\,\blacksquare$

::::

:::: {#statement-23}

**Утверждение:**  Если $\exists \displaystyle\int\limits_a^b f(x)dg(x)$, то $\forall c \in (a, b) \,\,\,\, \exists \displaystyle\int\limits_a^c f(x)dg(x)$ и $\exists \displaystyle\int\limits_c^b f(x)dg(x)$.

*Доказательство:* без доказательства $\,\,\,\,\blacksquare$

::::

## Обязательный пример, показывающий, что интеграл Римана-Стилтьеса не аддитивен


:::: {#theorem-23}

**Теорема:**  Если $\exists \displaystyle\int\limits_a^b f(x)dg(x)$, то $\exists \displaystyle\int\limits_a^b g(x)df(x)$ и 
$$\displaystyle\int\limits_a^b f(x)dg(x) = f(x)g(x){|^b_a} - \displaystyle\int\limits_a^b g(x)df(x)$$

*Доказательство:* $$\sigma_f(g, \mathcal{T}(\xi)) = \displaystyle \sum_{i = 1}^{n}g(\xi_i)(f(x_i) - f(x_{i - 1}))=$$
$$= g(\xi_1)(f(x_1) - f(a)) + g(\xi_2)(f(x_2) - f(x_1)) + \ldots + g(\xi_{n - 1})(f(x_{n - 1}) - f(x_{n - 2})) + g(\xi_n)(f(b) - f(x_{n - 1}))=$$
$$=-g(\xi_1)f(a) - f(x_1)(g(\xi_2) - g(\xi_1)) - \ldots - f(x_{n - 1})(g(\xi_n) - g(\xi_{n - 1})) + g(\xi_n)f(b) + f(a)g(a) + f(b)g(b) - f(a)g(a) - f(b)g(b)=$$
$$=-f(a)(g(\xi_1) - g(a)) - f(x_1)(g(\xi_2) - g(\xi_1)) - \ldots - f(x_{n - 1})(g(\xi_n) - g(\xi_{n - 1})) - f(b)(g(b) - g(\xi_n)) + f(x)g(x){|^b_a}\Rightarrow$$
$$\Rightarrow \sigma_g(f, \mathcal{T}) = -\sigma_f(g, \mathcal{T}) + f(x)g(x){|^b_a} \,\,\,\,\blacksquare$$
::::

:::: {#theorem-24}

**Теорема:**  Если $f(x) \in C[a, b], \,\,\,\, g(x) \in \operatorname{V}[a, b]$, то $\exists \displaystyle\int\limits_a^b f(x)dg(x)$

*Доказательство:* Достаточно доказать для $g(x)$ возрастающей.
$$\mathcal{T}_{[a, b]}(\xi) \,\,\,\, m_i = \displaystyle\min_{\Delta x_i}f(x) \,\,\,\, M_i = \displaystyle\max_{\Delta x_i}f(x)$$

Пусть $$s(\mathcal{T}) = \displaystyle \sum_{i = 1}^{n}m_i(g(x_i) - g(x_{i - 1})) \le \sigma_f(g, \mathcal{T}(\xi)) \le$$
$$\le \displaystyle \sum_{i = 1}^{n} M_i(g(x_i) - g(x_{i - 1})) = S(\mathcal{T})$$

Так как $f(x) \in C[a, b]$, то $f(x)$ равномерно непрерывно на $[a, b]$, то есть
$$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x_1, x_2 (|x_1 - x_2| < \delta) \,\,\,\, |f(x_1) - f(x_2)| < \varepsilon \Rightarrow$$
$\Rightarrow$ если $d(\mathcal{T}) < \delta$, то $\forall i \,\,\,\, M_i - m_i < \varepsilon$, т.к. максимум и минимум -- это значения $f(x)$.

При $d(\mathcal{T}) < \delta \,\,\,\, S - s < \varepsilon (g(b) - g(a))$, берем разность и все $M_i - m_i < \varepsilon$, выносим $\varepsilon$ за знак суммы, далее всё сокращается, кроме $g(b) - g(a) \Rightarrow$
$\Rightarrow \displaystyle\sup_{\mathcal{T}}s = \displaystyle\inf_{\mathcal{T}}S = I \Rightarrow |\sigma_f(g, \mathcal{T}) - I| < \varepsilon(g(b) - g(a)) \,\,\,\,\blacksquare$

::::


## Липшицевы и Гёльдеровы функции


:::: {#definition-30}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$. Если $\exists M > 0$, такое что $\forall x, y \in [a, b] \,\,\,\, |f(x) - f(y)| < M \cdot |x - y|$, то $f(x)$ -- *липшицева* функция.

Множество всех липшицевых функций на отрезке $[a, b]$ обозначается: $\operatorname{Lip}[a, b]$.

::::

:::: {#definition-31}

**Определение:**  Пусть $f(x)$ определена на $[a, b]$. Если $\exists M > 0$ и $\exists \alpha \in (0, 1)$, такие что $\forall x, y \in [a, b] \,\,\,\, |f(x) - f(y)| < M \cdot |x - y|^{\alpha}$, то $f(x)$ -- *гёльдерова* функция.

Множество всех гёльдеровых функций на отрезке $[a, b]$ с заданной $\alpha$ обозначается: $\operatorname{Gel}^{\alpha}[a, b]$.

::::

### Липшицева функция является функцией ограниченной вариации


:::: {#statement-24}

**Утверждение:**  Пусть $f(x) \in \operatorname{Lip}[a, b]$. Тогда $f(x) \in \operatorname{V}[a, b]$.

*Доказательство:* $f(x) \in \operatorname{Lip}[a, b] \Rightarrow \exists M: \,\,\,\,  \forall \mathcal{T}_{[a, b]} \,\,\,\, \displaystyle \sum_{i = 1}^{n}(f(x_i) - f(x_{i - 1})) \le \displaystyle \sum_{i = 1}^{n} M \cdot |x_i - x_{i - 1}| \le M |b - a| \,\,\,\,\blacksquare$

::::

:::: {#statement-25}

**Утверждение:**  Пусть $f(x) \in \mathcal{D}[a, b]$ и $\exists M > 0: \,\,\,\, |f’(x)| < M \,\,\,\, \forall x \in [a, b]$. Тогда $f(x) \in \operatorname{Lip}[a, b]$.

*Доказательство:* $\forall x, y \in [a, b] \,\,\,\, |f(x) - f(y)| = |f’(\xi) \cdot (x_i - x_{i - 1})| \le M \cdot |x - y|\,\,\,\,\blacksquare$

::::

## Связь интеграла Стилтьеса и интеграла Римана


:::: {#theorem-25}

**Теорема:**  Пусть $f(x) \in C[a, b], \,\,\,\, g(x) \in \mathcal{D}[a, b], \,\,\,\, g’(x) \in R[a, b]$. Тогда существует интеграл Стилтьеса $\displaystyle\int\limits_a^b f(x)dg(x)$, 
существует интеграл Римана $\displaystyle\int\limits_a^b f(x)g’(x)dx$ и $$\displaystyle\int\limits_a^b f(x)dg(x) = \displaystyle\int\limits_a^b f(x)g’(x)dx$$

*Доказательство:*

1. Существование $\,\,\,\,\blacksquare$
2. Так как эти интегралы существуют, достаточно доказать равенство интегральных сумм Римана и Ститьеса для конкретной разметки. $\forall \mathcal{T}\,\,\,\, \exists \{\xi_i\}: \,\,\,\, g(x_i) - g(x_{i - 1}) = g’(\xi_i)(x_i - x_{i - 1})$ по теореме Лагранжа. Возьмем в качестве разметки $\xi = \{\xi_i\}_{i = 1}^{n - 1}$. Имеем $\sigma_f(g, \mathcal{T}(\xi)) = f(\xi_i)(g(x_i) - g(x_{i - 1})) = f(\xi_i)g’(\xi_i)(x_i - x_{i - 1}) = \sigma_{f\cdot g’}(\mathcal{T}(\xi)) \,\,\,\,\blacksquare$

::::

## Первая и вторая теоремы о средних для интеграла Стилтьеса


:::: {#theorem-26}

**Теорема:**  (первая теорема о среднем) Пусть $g(x)$ монотонно возрастает на $[a, b]$, $f(x) \in C[a, b]$. Тогда $\exists c \in [a, b]: \,\,\,\, \displaystyle\int\limits_a^b f(x)dg(x) = f(c)(g(b) - g(a))$.

*Доказательство:* $m = \displaystyle\min_{[a, b]}f(x) \,\,\,\, M = \displaystyle\max_{[a, b]}f(x)$ 

Существуют по теоремам Вейерштрасса.

$g(x)$ -- монотонно возрастает на $[a, b]$, следовательно $g(x)$ - функция ограниченной вариации на $[a, b]$. А значит по теореме интеграл $\displaystyle\int\limits_a^b f(x)dg(x)$ существует.

$$m \cdot(g(b) - g(a)) \le \sigma_f(g, \mathcal{T}) \le M \cdot (g(b) - g(a))$$

Если $g(b) - g(a) \ne 0$, то $\frac{\displaystyle\int\limits_a^b f(x)dg(x)}{g(b) - g(a)}$ -- это значение $f(x)$ в некоторой точке $c \in [a, b]$ по теореме.

Если $f(a) = f(b) = 0$, то возьмем в качестве $c$ любую точку из $[a, b] \,\,\,\,\blacksquare$

::::

:::: {#theorem-27}

**Теорема:**  (вторая теорема о средних) Пусть $g(x)$ монотонно возрастает на $[a, b]$, $f(x) \in C[a, b]$. Тогда $\exists c \in [a, b]: \,\,\,\, \displaystyle\int\limits_a^b f(x)dg(x) = g(a)(f(c) - f(a)) + g(b)(f(b) - f(c))$.

*Доказательство:* $\displaystyle\int\limits_a^b f(x)dg(x) = f(x)g(x)|^b_a - \displaystyle\int\limits_a^b f(x)dg(x) =$ по первой теореме о среднем

$= f(b)g(b) - f(a)g(a) - f(c)(g(b) - g(a)) = g(a)(f(c) - f(a)) + g(b)(f(b) - f(c)) \,\,\,\,\blacksquare$

::::

## Вторая теорема о среднем для интеграла Римана (усиленная версия)

:::: {#theorem-28}

**Теорема:**  Пусть $g(x)$ монотонно возрастает на $[a, b]$, $f(x) \in C[a, b]$. Тогда $\exists c \in [a, b]: \,\,\,\, \displaystyle\int\limits_a^b f(x)g(x)dx = g(a)\displaystyle\int\limits_a^c f(x)dx + g(b) \displaystyle\int\limits_c^b f(x)dx$.

*Доказательство:* $g(x) \in R[a, b]$ по теореме, следовательно по свойству интеграла интеграл $\displaystyle\int\limits_a^b f(x)g(x)dx$ существует.

$F(x) = \displaystyle\int\limits_a^x f(t)dt \in \operatorname{Lip}[a, b]$, так как $|F(x) - F(y)| = \left|\displaystyle\int\limits_y^x f(t)dt\right| \le \left|M\cdot \displaystyle\int\limits_y^x 1 dx\right| = M \cdot |x - y|$.

Значит $F(x) \in \operatorname{V}[a, b]$.

$$\displaystyle\int\limits_a^b f(x)g(x)dx = \displaystyle\int\limits_a^b g(x)dF(x)=$$ рассмотрим этот интеграл, как интеграл Стилтьеса (можем, так как теорема) и применим вторую теорему о среднем
$$=g(a)(F(c) - F(a)) + g(b)(F(b) - F(c))= g(a)\displaystyle\int\limits_a^c f(x)dx + g(b)\displaystyle\int\limits_c^b f(x)dx \,\,\,\,\blacksquare$$ 

::::


# Норма, метрика


:::: {#definition-32}

**Определение:**  Функция $f: \mathbb{R}^n \to \mathbb{R}$ -- *норма*, если:

1. $\forall x \in \mathbb{R}^n \,\,\,\, f(x) \ge 0$
2. $f(x) = 0 \Leftrightarrow x = 0$
3. $\forall x \in \mathbb{R}^n, \,\,\,\, \lambda \in \mathbb{R} \,\,\,\, |\lambda|\cdot f(x) = f(\lambda x)$
4. $\forall x, y \in \mathbb{R}^n \,\,\,\, f(x + y) \le f(x) + f(y)$

$f(x)$ обозначается $||x||$

Скалярное произведение на $\mathbb{R}^n$ -- это попарное произведение координат векторов (точек). (нет)

Скалярное произведение векторов (точек) $x \in \mathbb{R}^n$ и $y \in \mathbb{R}^n$ обозначается $(x, y)$.

::::

:::: {#definition-33}

**Определение:**  Норма на $\mathbb{R}^n$ задается так: $||x|| = \sqrt{(x, x)}$.

**Замечание:** Норм много, и это не единственный способ задать норму.

::::

:::: {#definition-34}

**Определение:**  Функция $\rho: \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ -- *метрика (функция расстояния)*, если:

1. $\forall x, y \in \mathbb{R}^n \,\,\,\, \rho(x, y) \ge 0$
2. $\rho(x, y) = 0 \Leftrightarrow x = y$
3. $\forall x, y \in \mathbb{R}^n \,\,\,\, \rho(x, y) = \rho(y, x)$
4. $\forall x, y, z \in \mathbb{R}^n \,\,\,\, \rho(x, y) \le \rho(x, z) + \rho(y, z)$

На $\mathbb{R}^n$ зададим функцию расстояния так: $\rho(x, y) = ||x - y||$.

**Замечание:** Если хотите строгости, то посмотрите линал и топологию.

::::

## Пределы

:::: {#definition-35}

**Определение:**  Последовательность $\{x\}_{k = 1}^{\infty}$ -- *сходящаяся (имеет предел)* равный $a \in \mathbb{R}^n$, если $\forall \varepsilon > 0 \,\,\,\, \exists K \in N: \,\,\,\, \forall k > K \,\,\,\, \rho(x_k, a) < \varepsilon$.

::::

:::: {#statement-26}

**Утверждение:**  $\exists \displaystyle\lim_{k \to \infty}\{x_k\} = a \Leftrightarrow \forall i \in \{1, \ldots, n\} \,\,\,\,\exists \displaystyle\lim_{k \to \infty}\{x_{k_i}\} = a_i$.

*Доказательство:* $$\Rightarrow$$
$\forall \varepsilon > 0 \,\,\,\, \exists K \in \mathbb{N}: \,\,\,\, \forall k > K \,\,\,\, \sqrt{\displaystyle \sum_{i = 1}^{n}(x_{k_i} - a_i)^2} < \varepsilon \Rightarrow \forall \in \{1, \ldots, n\} \,\,\,\, |x_{k_i} - a_i| < \varepsilon$
$$\Leftarrow$$
$\forall \in \{1, \ldots, n\} \,\,\,\, |x_{k_i} - a_i| < \varepsilon \Rightarrow \sqrt{\displaystyle \sum_{i = 1}^{n}(x_{k_i} - a_i)^2} < \sqrt{n}\varepsilon \,\,\,\,\blacksquare$

::::

:::: {#definition-36}

**Определение:**  Множество $A \subset \mathbb{R}^n$ -- *ограничено*, если содержится в некотором открытом шаре.

::::

### Теорема Больцано-Вейерштрасса


:::: {#theorem-29}

**Теорема:**  (Больцано-Вейерштрасса) Пусть последовательность $\{x_k\}_{k = 1}^{\infty}$ -- ограниченное множество. Тогда у $\{x_k\}$ существует сходящаяся подпоследовательность $\{x_{k_m}\}_{m = 1}^{\infty}$.

*Доказательство:* $\{x_k\}_{k = 1}^{\infty}$ -- ограничена, а значит каждая из "последовательностей-координат" $\{x_{ik}\}_{k = 1}^{\infty}$ ($i \in \{1, \ldots, n\}$ -- индекс координаты, $k$ -- номер элемента последовательности) ограничена, а значит из $\{x_{1k}\}_{k = 1}^{\infty}$ можно выделить сходящуюся подпоследовательность $\{x_{1k_m}\}_{m = 1}^{\infty}$. Далее возьмем в последовательности $\{x_{2k}\}_{k = 1}^{\infty}$ элементы с индексами $k_m$ и выберем в полученной последовательности сходящуюся подпоследовательность $\{x_{2{k_m}_l}\}_{l = 1}^{\infty}$ (существует, т.к. каждая "последовательность-координата" ограничена). Подпоследовательность $\{x_{1k}\}_{k = 1}^{\infty}$ c индексами ${k_m}_l$ также сходится. Продолжая выбирать сходящиеся подпоследовательности, получим ответ $\,\,\,\,\blacksquare$

::::

## "Прицип полноты Кантора"


:::: {#definition-37}

**Определение:**  Множество $\Pi_{[a, b]} = \{x \in \mathbb{R}^n: \,\,\,\, a_i \le x_i \le b_i\}$ -- *параллелепипед*.

::::

:::: {#theorem-30}

**Теорема:**  Пусть $\{a_k\}$ и $\{b_k\}$, таковы, что $\Pi_{[a_{k+1}, b_{k+1}]} \subset \Pi_{[a_k, b_k]}$ и $\forall i \in \{1, \ldots, n\} \,\,\,\, |a_{k_i} - b_{k_i}| \to 0, \,\,\,\, k \to \infty$. Тогда $\exists ! \xi: \,\,\,\, \xi \in \Pi_{[a_k, b_k]} \,\,\,\, \forall k$.

*Доказательство:* $\forall i \in \{1, \ldots, n\} \,\,\,\, [a_{k+1}, b_{k +1}] \subset [a_k, b_k]$ и $|b_{k_i} - a_{k_i}| \to 0, \,\,\,\, k \to \infty$, значит по принципу поноты Кантора $\exists ! \xi_i: \,\,\,\, \xi_i \in [a_{k_i}, b_{k_i}] \forall k$. Рассмотрим $\xi = (\xi_1, \ldots, \xi_n)$, удовлетворяющий условиям теоремы $\,\,\,\,\blacksquare$

::::

## Расстояние между подмножествами


:::: {#definition-38}

**Определение:**  Пусть $A, B \subset \mathbb{R}^n$. Тогда $\rho(A, B) = \displaystyle\inf_{a \in A, b \in B}\rho(a, b)$ -- *расстояние между множествами* $A$ и $B$.

::::

:::: {#theorem-31}

**Теорема:**  Пусть $A, B \subset \mathbb{R}^n$ -- замкнутые, $A$ -- ограничено. Если $A \cap B = \varnothing$, то $\rho(A, B) > 0$.

*Доказательство:* (от противного) Пусть $\displaystyle\inf_{x \in A, y \in B}\rho(x, y) = 0$. Тогда $\forall k \in \mathbb{N} \,\,\,\, \exists x_k \in A, y_k \in B: \,\,\,\, \rho(x_k, y_k) < \frac{1}{k} \Rightarrow \{x_k\}_{k = 1}^{\infty}$ -- ограничена, а значит существует сходящаяся подпоследовательность $\{x_{k_m}\}_{m = 1}^{\infty}$ и $\displaystyle \lim_{m\to \infty} x_{k_m} = x_0 \in A$, но $\rho(x_0, y_{k_m}) \le \rho(x_0, x_{k_m}) + \rho(x_{k_m}, y_{k_m}) < \varepsilon + \frac{1}{k} \Rightarrow \exists \displaystyle \lim_{m\to \infty}y_{k_m} = x_0 \in B$ противоречие $\,\,\,\,\blacksquare$

::::

:::: {#theorem-32}

**Теорема:**  $A \subset \mathbb{R}^n$ -- замкнуто, $x \not\in A$. Тогда $\exists y \in A: \,\,\,\, \rho(x, y) = \rho(x, A)$.

*Доказательство:* $\forall k \in \mathbb{N} \,\,\,\, \exists y_k \in A: \,\,\,\, \rho(x, y_k) < \rho(x, A) + \frac{1}{k}$.
$\forall k \in \mathbb{N} \,\,\,\, \rho(x, y_k) \le \rho(x, A) + 1 \Rightarrow \{y_k\}$ -- ограничена, а значит существует сходящаяся подпоследовательность $\{y_{k_m}\}$ и $\displaystyle \lim_{m\to \infty}\{y_{k_m}\} = y_0 \in A$, т.к. $A$ -- замкнуто.

$$\rho(x, y_{k_m}) < \rho(x, A) + \frac{1}{k}$$
$$\Downarrow$$
$$\rho(x, y_0) \le \rho(x, A)$$
и, так как $\rho(x, A)$ точная нижняя грань, $\rho(x, y_0) \ge \rho(x, A) \Rightarrow \exists y = y_0\,\,\,\,\blacksquare$

::::

$\DeclareMathOperator*{\bigtimes}{\text{\Large $\times$}}$

## Компактность


:::: {#definition-39}

**Определение:**  $A \subset \mathbb{R}^n$ -- *компакт*, если из любого откытого покрытия $A$ можно выделить конечное подпокрытие.

::::

:::: {#definition-40}

**Определение:**  $A \subset \mathbb{R}^n$ -- *секвенциальный компакт*, если у любой последовательности из $A$ существует сходящаяся подпоследовательность.

::::

:::: {#theorem-33}

**Теорема:**  $A$ - секвенциальный компакт $\Leftrightarrow$ $A$ -- замкнуто и ограничено.

*Доказательство:* $$\Rightarrow$$

(от противного) Пусть $A$ -- секвенциальный компакт и $A$ неограничено. Тогда $\forall k \in \mathbb{N} \,\,\,\, \exists x_k \in A: \,\,\,\, ||x_k|| > k \Rightarrow$ получили последовательность, у которой нет сходящейся подпоследовательности. Противоречие. У любой последовательности $\{x_k\}$ существует сходящаяся подпоследовательность $\{x_{k_m}\}: \,\,\,\, \displaystyle \lim_{m\to \infty}x_{k_m} = x_0$ -- предельная точка $A$. 

$$\Leftarrow$$
$\,\,\,\,\blacksquare$

::::

:::: {#theorem-34}

**Теорема:**  $A \subset \mathbb{R}^n$ -- секвенциальный компакт $\Leftrightarrow$ $A$ -- компакт.

*Доказательство:* $$\Rightarrow$$

(от противного) Пусть существует открытое покрытие $A \,\,\,\, \displaystyle\cup_{\alpha}\{U_{\alpha}\}:$ не существует конечного подпокрытия. Рассмотрим куб (существует, так как $A$ ограничено) $\displaystyle\bigtimes_{i = 1}^m[a_i, a_i + d]$ делим куб на $2^n$ частей, выбираем ту, для которой нельзя выделить конечное подпокрытие из $U_{\alpha}$, и продолжаем делить. Получаем последовательность вложенных кубов, а значит по теореме $\exists ! \xi: \,\,\,\, \xi$ принадлежит каждому кубу. А значит $\exists U_{\alpha^{*}}: \,\,\,\, \xi \in U_{\alpha^{*}}$. $U_{\alpha^{*}}$ -- открытое, следовательно $\exists O_{\varepsilon}(\xi): \,\,\,\, \xi \in O_{\varepsilon}(\xi) \subset U_{\alpha^{*}}$. В этой окрестности содержится один из кубов, построенной последовательности, а значит существует покрытие этого куба, состоящее из $U_{\alpha^{*}}$. Противоречие.

$$\Leftarrow$$
Пусть $A$ -- компакт, но существует ограниченная $\{x_k: x_k \in A\}_{k = 1}^{\infty}$, такая, что $A$ не содержит предельных точек $\{x_k: x_k \in A\}_{k = 1}^{\infty}$. 

**Напоминание**: Точка $x_0$ предельная для $A$ $\Leftrightarrow$ любая проколотая окрестность $x_0$ содержит бесконечное число элементов множества $A$.

То есть $\forall y \in A \,\,\,\, \exists \varepsilon_y > 0: \,\,\,\, O_{\varepsilon_y}(y) \cap \{x_k\}_{k = 1}^{\infty}$ содержит конечное количество элементов. $\displaystyle\bigcup_{y \in A}O_{\varepsilon_y}(y)$ -- это открытое подкрытие $A$, а значит из него можно выделить конечное подпокрытие $\displaystyle\bigcup_{y_i \in A}O_{\varepsilon_y}(y_i)$. Получаем, что в последовательности $\{x_k: x_k \in A\}_{k = 1}^{\infty}$ конечное количество точек, а значит существует предельная точка, принадлежащаяя самой последовательности. Противоречие $\,\,\,\,\blacksquare$

::::

## Связность


:::: {#definition-41}

**Определение:**  $A \subset \mathbb{R}^n$ -- *линейно связно*, если любые две точки из $A$ можно соединить непрерывной кривой.

::::

:::: {#theorem-35}

**Теорема:**  Пусть $A \subset \mathbb{R}^n$ -- линейно связно. $B \subset \mathbb{R}^n$. Если $A \cap B \ne \varnothing$ и $A \cap (\mathbb{R}^n \setminus B) \ne \varnothing$, то $A \cap \partial B \ne \varnothing$.

*Доказательство:* без доказательства $\,\,\,\,\blacksquare$

::::

:::: {#definition-42}

**Определение:**  Если $A \subset \mathbb{R}^n$ -- открыто и линейно связно, то $A$ -- *область*.

::::

:::: {#definition-43}

**Определение:**  Замыкание области -- *замкнутая область*.

::::

:::: {#definition-44}

**Определение:**  Если любые две точки множества $A \subset \mathbb{R}^n$ можно соединить отрезком, содержащащимся в $A$, то $A$ -- *выпуклое*.

::::

# Функции в $\mathbb{R}^n$

:::: {#definition-45}

**Определение:**  Пусть $f$ -- функция в $\mathbb{R}^n$. Множество $A = \{x \in \mathbb{R}^n: \,\,\,\, f(x) = c\}$ -- *линия уровня* (для константы $c$).

::::

:::: {#definition-46}

**Определение:**  Если $x_0 \in D_f’$ (множество предельных точек области определения) и $\exists a \in \mathbb{R}: \,\,\,\, \forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x \in \mathring{O}_{\delta}(x_0) \cap D_f \,\,\,\, |f(x) - a| < \varepsilon$, то $a$ -- *предел функции* $f(x)$ в точке $x_0$.

::::

:::: {#definition-47}

**Определение:**  Сформулируйте определение по Гейне для функции многих переменных.

::::

## Локальные свойства предела


Предел суммы, произведения, частного, отделимость, предельный переход в неравенствах, ограниченность функции, имеющей предел, критерий Коши.

Все, что выше надо уметь доказывать.

:::: {#definition-48}

**Определение:**  Если $x_0 \in D_f’$ (множество предельных точек области определения), $\gamma(t)$ -- непрерывная кривая, $\gamma(t_0) = x_0$, если $\exists a \in \mathbb{R}: \,\,\,\, \forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall t \in (t_0 - \delta, t_0) \cup (t_0, t_0 + \delta) \,\,\,\, |f(x) - a| < \varepsilon$, то $a$ -- *предел функции* $f(x)$ *вдоль кривой* $\gamma$ в точке $x_0$.

::::

## Непрерывные функции


:::: {#definition-49}

**Определение:**  Если $x_0 \in D_f’$ (множество предельных точек области определения). Если существует $\displaystyle \lim_{x\to x_0}f(x) = x_0$, то функция $f(x)$ *непрерывна* в точке $x_0$.

::::

:::: {#definition-50}

**Определение:**  Множество всех непрерывных на $A \subset \mathbb{R}^n$ функций обозначается $C(A)$.

::::

### Локальные свойства непрерывных функций


Сумма, произведение и частное непрерывных функций -- непрерывная функция, композиция непрерывных функций непрерывная функция, ...

:::: {#theorem-36}

**Теорема:**  Композиция непрерывных функций непрерывна.

*Доказательство:*

::::

## Глобальные свойства непрерывных функций


:::: {#theorem-37}

**Теорема:**  (Первая теорема Вейерштрасса) Пусть $A \subset \mathbb{R}^n$ - компакт, $f(x) \in C(A)$. Тогда $f(x)$ ограничена на $A$.

*Доказательство:* как будто ничего не изменилось (не, теперь компакт, потому что в $\mathbb{R}^n$ не только отрезок компакт).

::::

:::: {#theorem-38}

**Теорема:**  (Вторая теорема Вейерштрасса) Пусть $A \subset \mathbb{R}^n$ - компакт, $f(x) \in C(A)$. Тогда $\exists x_{min}, x_{max} \in A: \,\,\,\, f(x_{min}) = \displaystyle\inf_Af(x) \,\,\,\, f(x_{max}) = \displaystyle\sup_Af(x)$.

*Доказательство:* см. выше.

::::



## Непрерывная функция принимает все промежуточные значения


:::: {#theorem-39}

**Теорема:**  Пусть $A \subset \mathbb{R}^n$ -- линейно связно. $f(x) \in C(A)$. Пусть $x_1, x_2 \in A \,\,\,\, f(x_1) = \alpha, \,\,\,\, f(x_2) = \beta \,\,\,\, (\alpha \le \beta)$. Тогда $\forall \varkappa: \,\,\,\, \alpha \le \varkappa \le \beta \,\,\,\, \exists x_{\varkappa} \in A: \,\,\,\, f(x_{\varkappa}) = \varkappa$.

*Доказательство:* $A$ -- линейно связно $\Rightarrow \exists \gamma(t): \,\,\,\, \gamma(0) = x_1, \gamma(1) = x_2$ ($\gamma$ -- непрерывная кривая). Тогда $f(\gamma(t)) \in C[0, 1]$, значит по теореме о том, что функция одной переменнной принимает все промежуточные значения, $\exists t_{\varkappa} \in [0, 1]: \,\,\,\, f(\gamma(t_{\varkappa})) = \varkappa \Rightarrow x_{\varkappa} = \gamma(t_{\varkappa}) \,\,\,\,\blacksquare$

::::

## Равномерная непрерывность


:::: {#definition-51}

**Определение:**  Как было так и осталось.

::::

:::: {#theorem-40}

**Теорема:**  Если функция непрерывна на компакте, то она равномерно непрерывна на нем.

*Доказательство:* 

::::

## Дифференцирование функций многих переменных


:::: {#definition-52}

**Определение:**  Пусть $f(x)$ определена в $O(x_0)$. Если $\exists \displaystyle \lim_{\Delta x_i\to x_0}\frac{f(x_{01}, \ldots, x_{0i} + \Delta x_i, \ldots, x_n) - f(x_0)}{\Delta x_i} := f’_{x_i} := \frac{\partial f}{\partial x_i}_{|_{x = x_0}}$, то $f’_{x_i}$ -- *частная производная* $f(x)$ по переменной $x_i$.

::::

:::: {#definition-53}

**Определение:**  Пусть $f(x)$ определена в $O(x_0)$. Если $\exists \{A_i\}_{i = 1}^n: \,\,\,\,$$$f(x) - f(x_0) = \displaystyle \sum_{i = 1}^{n}A_i(x_i - x_{0i}) + \overline{\overline{o}}(\rho(x, x_0)), \,\,\,\, x \to x_0,$$то $f(x)$ *дифференцируема* в точке $x_0$ и *дифференциал* $df_{|_{x_0}} = \sum_{i = 1}^{n}A_i(x_i - x_{0i})$.

::::

:::: {#theorem-41}

**Теорема:**  Если $f$ дифференцируема в точке $x_0$, то $\forall i \in \{1, \ldots, n\} \,\,\,\, \frac{\partial f}{\partial x_i} = A_i$.

*Доказательство:* $$\displaystyle \lim_{\Delta x_i\to x_0}\frac{f(x_{01}, \ldots, x_{0i} + \Delta x_i, \ldots, x_n) - f(x_0)}{\Delta x_i} = \displaystyle \lim_{\Delta x_i\to x_0}\frac{A_i \Delta x_i + \overline{\overline{o}}(\rho)}{\Delta x_i} = A_i \,\,\,\,\blacksquare$$

::::

:::: {#theorem-42}

**Теорема:**  Если $f(x)$ дифференцируема в точке $x_0$, то $f(x)$ непрерывна в точке $x_0$.

*Доказательство:* 

$$|f(x) - f(x_0)| = |\displaystyle \sum_{i = 1}^{n}A_i \Delta x_i + \overline{\overline{o}}(\rho)| \le |\displaystyle \sum_{i = 1}^{n}A_i \Delta x_i| + |\overline{\overline{o}}(\rho)| \le \sqrt{\displaystyle \sum_{i = 1}^{n}A_i^2}\sqrt{\displaystyle \sum_{i = 1}^{n}\Delta x_i^2} \le 2 \varepsilon \,\,\,\,\blacksquare$$

::::

## Производная по направлению

:::: {#definition-54}

**Определение:**  Пусть $f(x)$ дифференцируема в точке $x_0$. Пусть $l = (\cos \alpha_1, \cos \alpha_2, \ldots, \cos \alpha_n)$ и $||l|| = 1$.

$$\frac{\partial f}{\partial l}_{|_{x_0}} = \displaystyle \sum_{i = 1}^{n}\cos \alpha_i \cdot \frac{\partial f}{\partial x_i}$$ -- *производная* $f$ *в направлении* $l$.

::::

:::: {#definition-55}

**Определение:**  Вектор (на самом деле ковектор, т.к. вектор из сопряженного пространства) $$\left(\frac{\partial f}{\partial x_1}, \ldots, \frac{\partial f}{\partial x_n}\right)$$ -- *градиент функции* $f$. Обозначается: $\operatorname{grad} f$ или $\nabla f$.

::::


## Направление градиента -- это направление наибольшего изменения функции


:::: {#theorem-43}

**Теорема:**  Пусть $m = \frac{\operatorname{grad} f}{||\operatorname{grad} f||}_{|_{x = x_0}}$ (градиент, норма). Тогда $$\displaystyle\max_l \left|\frac{\partial f}{\partial l}_{|_{x = x_0}}\right| = \left|\frac{\partial f}{\partial m}_{|_{x = x_0}}\right|$$

*Доказательство:* $$\left|\frac{\partial f}{\partial l}_{|_{x = x_0}}\right| = |\operatorname{grad}f|\cdot\cos \varphi \le |\operatorname{grad}f|$$

$$\left|\frac{\partial f}{\partial m}_{|_{x = x_0}}\right| = \sqrt{\displaystyle \sum_{i = 1}^{n} \left(\frac{\partial f}{\partial x_i}\right)^2} \,\,\,\,\blacksquare$$

::::

## Достаточное условие дифференцируемости


:::: {#theorem-44}

**Теорема:**  Пусть $\forall i \in {1, \ldots, n} \,\,\,\, \exists \frac{\partial f}{\partial x_i}$ в $B(x_0)$ и $\forall i \in {1, \ldots, n} \,\,\,\, \frac{\partial f}{\partial x_i} \in C(B(x_0))$. Тогда $f$ дифференцируема в точке $x_0$.

*Доказательство:* Докажем для $\mathbb{R}^2$ остальное аналогично 😉. 

$$f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0) =$$
$$= f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0 + \Delta y) + f(x_0, y_0 + \Delta y) - f(x_0, y_0) =$$
$$= f’_x(x_0 + \theta \Delta x, y_0 + \Delta y) \Delta x + f’_y(x_0 + \Delta x, y_0 + \theta \Delta y) \Delta y =$$
$$= (f’_x(x_0, y_0) + \overline{\overline{o}}(\rho)) \Delta x + (f’_y(x_0, y_0) + \overline{\overline{o}}(\rho)) \Delta y =$$
$$= f’_x(x_0, y_0)\Delta x + f’_y(x_0, y_0) \Delta y + \overline{\overline{o}}(\rho) \,\,\,\,\blacksquare$$

::::

## Равенство смешанных производных


:::: {#definition-56}

**Определение:**  Если $f$ и все частные производные до $k - 1$ порядка дифференцируемы в окрестности точки $x_0$ и все $k$ производные непрерывны в точке $x_0$, то $f \in C^k(x_0)$.

::::

:::: {#theorem-45}

**Теорема:**  Если $f \in C^2(x_0)$, то $\forall i, j \,\,\,\, \frac{\partial^2 f}{\partial x_j \partial x_i} = \frac{\partial^2 f}{\partial x_i \partial x_j}$.

*Доказательство:* 

Определим:

$$\Delta_x f(x_0, y_0) = f(x_0 + \Delta x, y_0) - f(x_0, y_0)$$
$$\Delta_y f(x_0, y_0) = f(x_0, y_0 + \Delta y) - f(x_0, y_0)$$

Имеем:

$$\Delta_x \Delta_y f(x_0, y_0) = \Delta_y \Delta_x f(x_0, y_0)$$

$$\Delta_x \Delta_y f(x_0, y_0) = \Delta_x f(x_0, y_0 + \Delta y) - f(x_0, y_0) =$$
$$= \Delta_x (f’_y(x_0, y_0 + \theta \Delta y) \Delta y) =$$
$$= (f’_y(x_0 + \Delta x, y_0 + \theta \Delta y) - f’_y(x_0, y_0 + \theta \Delta y)) \Delta y =$$
$$= f’_x(f’_y(x_0 + \theta \Delta x, y_0 + \theta \Delta y))\Delta_x \Delta y$$

При $\rho \to 0 \,\,\,\, f’_x(f’_y(x_0 + \theta \Delta x, y_0 + \theta \Delta y)) = f’_x(f’_y(x_0, y_0)) + \overline{\overline{o}}(1)$. Аналогично для $\Delta_y \Delta_x f(x_0, y_0) \,\,\,\,\blacksquare$

::::

## Касательная плоскость к графику


:::: {#definition-57}

**Определение:**  Пусть $f$ определена в $B(x_0)$ и $\exists \operatorname{grad}f_{|_{x=x_0}}$. Если угол между направляющим вектором секущей к графику, проходящей через точки $(x_{01}, \ldots, x_{0n}, f(x_0))$ и $(x_{1}, \ldots, x_{n}, f(x))$ и вектором $\left(\frac{\partial f}{\partial x_1}_{|_{x = x_0}}, \ldots, \frac{\partial f}{\partial x_n}_{|_{x = x_0}}, -1\right)$ стремится к $\frac{\pi}{2}$ при $\rho \to 0$, то плоскость $Y = f(x_0) + \displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i}_{|_{x = x_0}} (x_i - x_{0i})$ -- *касательная плоскость* к графику $f$ в точке $x_0$.

::::

:::: {#theorem-46}

**Теорема:**  Если $f$ дифференцируема в точке $x_0$, то существует касательная плоскость к графику $f$ в точке $x_0$.

*Доказательство:*

Запишем уравнение секущей к графику, проходящей через точки $(x_{01}, \ldots, x_{0n}, f(x_0))$ и $(x_{1}, \ldots, x_{n}, f(x))$ в параметрическом виде:

$$l: \,\,\,\, \begin{cases}
    X_1 = x_{01} + (x_1 - x_{01}) \cdot t\\
    \vdots\\
    X_n = x_{0n} + (x_n - x_{0n}) \cdot t\\
    X_{n + 1} = f(x_0) + (f(x) - f(x_0)) \cdot t\\
\end{cases}$$

Направляющий вектор $p = (x_1 - x_{01}, \ldots, x_n - x_{0n}, f(x) - f(x_0))$.

Запишем косинус угла между $p$ и $\left(\frac{\partial f}{\partial x_1}_{|_{x = x_0}}, \ldots, \frac{\partial f}{\partial x_n}_{|_{x = x_0}}, -1\right)$:

$$\cos \varphi = \frac{\displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i} \cdot (x_i - x_{0i}) - (f(x) - f(x_0))}{\sqrt{1 + \displaystyle \sum_{i = 1}^{n} \left(\frac{\partial f}{\partial x_i}\right)^2}\cdot \sqrt{(f(x) - f(x_0))^2 + \displaystyle \sum_{i = 1}^{n}(\Delta x_i)^2}} =$$
$$= \frac{\overline{\overline{o}}(\rho)}{c\cdot \sqrt{(f(x) - f(x_0))^2 + \rho^2}} \to 0, \,\,\,\, \rho \to 0 \Rightarrow \varphi \to \frac{\pi}{2}, \,\,\,\, \rho \to 0 \,\,\,\,\blacksquare$$

::::

## Инвариантность формы первого дифференциала


:::: {#theorem-47}

**Теорема:**  Пусть $f(x)$ дифференцируема в области $\Omega \subset \mathbb{R}^n$. $x(t)$ дифференцируема в области $\Phi \subset \mathbb{R}^k$ и $x(t): \,\,\,\, \Phi \to \Omega$. Тогда $f(x(t))$ дифференцируема в области $\Phi$ и $$\frac{\partial f}{\partial t_j} = \displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i} \cdot \frac{\partial x_i}{\partial t_j}$$

*Доказательство:* 

Запишем дифференциал $f(x(t))$:

$$f(x(t + \Delta t)) - f(x(t)) =$$
$$= \displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i} (x_i(t_0 + \Delta t) - x_i(t_0)) + \overline{\overline{o}}\left(\sqrt{\displaystyle \sum_{i = 1}^{n} (x_i(t_0 + \Delta t) - x_i(t_0))^2}\right)=$$
$$=\displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i} \left(\displaystyle \sum_{j = 1}^{k} \frac{\partial x_i}{\partial t_j} \Delta t_j + \overline{\overline{o}}(\rho)\right) + ... =$$
$$= \displaystyle \sum_{j = 1}^{k} \left(\displaystyle \sum_{i = 1}^{n} \frac{\partial f}{\partial x_i} \cdot \frac{\partial x_i}{\partial t_j}\right) \Delta t_j + \overline{\overline{o}}(\rho) \,\,\,\,\blacksquare$$

::::


## Дифференциалы высших порядков


:::: {#definition-58}

**Определение:**  Пусть $f(x) \in C^2(B(x_0))$. Запишем первый дифференциал $f(x)$ в точке $x_0$. $$df(x)_{|_{x_0}} = \displaystyle \sum_{i = 1}^{n}\frac{\partial f}{\partial x_i}_{|_{x_0}}dx_i$$ Продифференцируем $df(x):$$$d(df(x)) = \displaystyle \sum_{j = 1}^{n}\frac{\partial \left(\displaystyle \sum_{i = 1}^{n}\frac{\partial f}{\partial x_i}_{|_{x_0}}dx_i\right)}{\partial x_j}dx_j = \displaystyle \sum_{i, j = 0}^{n}\frac{\partial^2 f}{\partial x_i \partial x_j}d x_i d x_j$$ -- это $2$*-й дифференциал* $f(x)$.

::::

## Формула Тейлора для функций многих переменных


:::: {#theorem-48}

**Теорема:**  $$f(x) \in C^m(B(x_0)), x_0 \in \mathbb{R}^n \Rightarrow \forall x \in B(x_0) \,\,\,\, \exists \theta \in [0, 1]:$$
$$f(x) - f(x_0) = \displaystyle \sum_{k = 1}^{m - 1} \frac1{k!} d^kf(x_0) + d^m f(x + \theta (x - x_0))$$

*Доказательство:* Пусть $t \in [0, 1]$. Тогда $x_0 +  t (x - x_0) \in B(x_0)$ и $F(t) = f(x_0 +  t (x - x_0)) \in C^m[0, 1]$.

Докажем по индукции, что $F^{(k)}(t) = d^k f(x_0 + t (x - x_0))$.

**База:** $$F’(t) = \displaystyle \sum_{i = 1}^{n}\frac{\partial f(x_0 + t (x - x_0))}{\partial x_i} (x_{0i} + t(x_i - x_{0i}))_t’ = \displaystyle \sum_{i = 1}^{n}\frac{\partial f(x_0 + t (x - x_0))}{\partial x_i} \Delta x_i$$

**Шаг:** $$F^{(k)}(t) = (F^{(k - 1)}(t))’ = (d^{k - 1} f(x_0 + t (x - x_0)))’ =$$
$$=\left(\displaystyle \sum_{i_1, \ldots, i_k = 1}^{n}\frac{\partial^{k - 1} f(x_0 + t (x - x_0))}{\partial x_{i_1} \ldots \partial x_{i_k}}dx_{i_1} \ldots d x_{i_k}\right)’=$$
$$=\displaystyle \sum_{i_1, \ldots, i_k = 1}^{n}\left(\frac{\partial^{k - 1} f(x_0 + t (x - x_0))}{\partial x_{i_1} \ldots \partial x_{i_k}} \right)’dx_{i_1} \ldots d x_{i_k}=$$
$$=\displaystyle \sum_{i_1, \ldots, i_k = 1}^{n} \displaystyle \sum_{i = 1}^{n}\frac{\partial^k f(x_0 + t (x - x_0))}{\partial x_{i_1} \ldots \partial x_{i_k} x_i} d x_i dx_{i_1} \ldots d x_{i_k} \,\,\,\,\blacksquare$$

Имеем $F(1) = f(x)$, $F(0) = f(x_0)$ и по формуле тейлора с остаточным членом в форме Лагранжа для функции одной переменной $F(1) - F(0) = \displaystyle \sum_{k = 1}^{m - 1}\frac{F^{(k)}(0)}{k!} + \frac{F^{(m)}(\theta)}{m!} \,\,\,\,\blacksquare$

::::

## Локальный экстремум


### Необходимое условие локального экстремума

### Достаточное условие локального экстремума

# Теорема о неявной функции

:::: {#theorem-49}

**Теорема:**  (О неявной функции) Пусть $F: \mathbb{R}^{n + 1} \to \mathbb{R}, \,\,\,\,\mathbf{x}, \mathbf{x_0} \in \mathbb{R}^n, \,\,\,\, y, y_0 \in \mathbb{R}$. 

Пусть $F(\mathbf{x}, y) \in C^1(B(\mathbf{x_0}, y_0)), \,\,\,\, F(\mathbf{x_0}, y_0) = 0, \,\,\,\, F_y’(\mathbf{x_0}, y_0) \ne 0$. 

Тогда $$\exists B_{\delta}(\mathbf{x_0}): \,\,\,\, \forall \mathbf{x} \in B_{\delta}(\mathbf{x_0}) \,\,\,\, \exists ! y = f(\mathbf{x}): \,\,\,\, F(x, y) = 0$$
$$f(\mathbf{x}) \in C^1(B_{\delta}(\mathbf{x_0})), \,\,\,\, y_0 = f(\mathbf{x_0})$$ и $$\forall x_i \,\,\,\, \exists f_{x_i}’(\mathbf{x_0}, y_0) = -\frac{F_{x_i}’(\mathbf{x_0}, y_0)}{F_y’(\mathbf{x_0}, y_0)}$$

*Доказательство:* 

<details>
<summary>**План**</summary>

1. Выбираем прямоугольную окрестность ($n + 1$-мерный прямоугольный параллелепипед), в которой $F(\mathbf{x}, y)$ непрерывна и $F_y’(\mathbf{x}, y)$ непрерывна. Для этого нужно условие $F(\mathbf{x}, y) \in C^1(B(\mathbf{x_0}, y_0))$, причем существование и непрерывность производных по $x_i$ не нужно в этом пункте.

2. Пользуемся тем, что $F_y’(\mathbf{x_0}, y_0) \ne 0$. Пусть $F_y’(\mathbf{x_0}, y_0) > 0$. Тогда, так как $F_y’(\mathbf{x}, y)$ непрерывна в выбранной в первом пункте окрестности, можем уменьшить окрестность, так, чтобы $\varphi(y) = F(\mathbf{x_0}, y)$ в ней монотонно возрастала.

3. Так как $\varphi(y)$ строго монотонно возрастает и $F(\mathbf{x_0}, y_0) = 0$, $F(\mathbf{x_0}, y + \delta) > 0$ и $F(\mathbf{x_0}, y + \delta) < 0$.

4. Так как $F(\mathbf{x}, y)$ непрерывна, можем еще уменьшить окрестность, чтобы $\forall (\mathbf{x}, y)$ из окрестности $F(\mathbf{x}, y + \delta) > 0$ и $F(\mathbf{x}, y + \delta) < 0$.

5. По теореме о промежуточных значениях $\forall \mathbf{x} \,\,\,\, \exists y^{*}: \,\,\,\, F(\mathbf{x}, y^{*}) = 0$ (Зафиксировали $\mathbf{x}$, тогда $F(\mathbf{x}, y + \delta) > 0$ и $F(\mathbf{x}, y + \delta) < 0$, а следовательно $\exists y^{*}: \,\,\,\, F(\mathbf{x}, y^{*}) = 0$).

6. Доказываем дифференцируемость.

</details>

1. Пусть $\Pi_{\mathbf{x_0} \delta_0} = \displaystyle\bigtimes_{i = 1}^n (x_{0i} - \delta_0, x_{0i} + \delta_0)$ ($x_{0i}$ - $i$-я координата $\mathbf{x_0}$). $\Pi_{\delta_0} = \Pi_{\mathbf{x_0} \delta_0} \times (y_0 - \delta_0, y_0 + \delta_0)$, причем $\Pi_{\delta_0}$, такова, что $\forall (\mathbf{x}, y) \in \Pi_{\delta_0} \,\,\,\, F(\mathbf{x}, y)$ и $F_y’(\mathbf{x}, y)$ непрерывны.

2. Пусть $F_y’(\mathbf{x_0}, y_0) > 0$. Рассмотрим $\varphi(y) = F(\mathbf{x_0}, y)$. Так как $\varphi(y)$ непрерывна в $\Pi_{\delta_0}$, то существует $0 < \delta_1 < \delta_0$, такая, что $\forall y \in [y_0 - \delta_1, y_0 + \delta_1] \,\,\,\, F_y’(\mathbf{x_0}, y) > 0$, а следовательно $\varphi(y)$ строго монотонно возрастает. Получили окрестность $\Pi_{\delta_1}$.

3. Так как $\varphi(y)$ строго монотонно возрастает на $\Pi_{\delta_1}$ и $F(\mathbf{x_0}, y_0) = 0$, $F(\mathbf{x_0}, y_0 + \delta_1) > 0$ и $F(\mathbf{x_0}, y_0 - \delta_1) < 0$.

4. $F$ непрерывна в $(\mathbf{x_0}, y_0 - \delta_1)$ и $(\mathbf{x_0}, y_0 + \delta_1)$ и функции $F(x, y_0 - \delta_1)$ и $F(x, y_0 + \delta_1)$, как функции $\mathbf{x}$ непрерывны в $\Pi_{\mathbf{x_0}\delta_1}$, а следовательно $\exists \delta < \delta_1: \,\,\,\, \forall \mathbf{x} \in \Pi_{\mathbf{x}\delta} \,\,\,\, F(x, y_0 - \delta_1) < 0$ и $F(x, y_0 + \delta_1) > 0$.

5. Зафиксируем $\mathbf{x} \in \Pi_{\mathbf{x}\delta}$, имеем: $\forall y \in (y_0 - \delta, y_0 + \delta) \,\,\,\, F(\mathbf{x}, y + \delta) > 0$ и $F(\mathbf{x}, y + \delta) < 0$, а следовательно по теореме о промежуточных значениях $\exists ! y^{*} \in (y_0 - \delta, y_0 + \delta): \,\,\,\, F(\mathbf{x}, y^{*}) = 0$. (единственное, так как функция строго монотонно возрастает). Соответствие $F(\mathbf{x}, y^{*}) = 0$ обозначим $y^{*} = f(\mathbf{x})$.

6. Докажем дифференцируемость $f(x)$ в $\Pi_{\mathbf{x}\delta}$. Пусть $\mathbf{x_1}, \mathbf{x_2} \in \Pi_{\mathbf{x}\delta}$. Рассмотрим $\varphi(t) = F(\mathbf{x_1} + t(\mathbf{x_2} - \mathbf{x_1}), f(\mathbf{x_1}) + t(f(\mathbf{x_2}) - f(\mathbf{x_1}))) \in C^1[0, 1]$
$$\varphi(0) = F(\mathbf{x_1}, f(\mathbf{x_1})) = 0$$
$$\varphi(1) = F(\mathbf{x_2}, f(\mathbf{x_2})) = 0$$
Следовательно, по теореме Ролля $\exists \xi \in (0, 1): \,\,\,\, \varphi’(\xi) = 0$.

$$0 = \varphi’(\xi) = \displaystyle \sum_{i = 1}^{n}\frac{\partial F}{\partial x_i}(x_{2i} - x_{1i})+$$
$$+ \frac{\partial F}{\partial y}(f(\mathbf{x_2}) - f(\mathbf{x_1}))$$

Выразим $f(\mathbf{x_2}) - f(\mathbf{x_1})$

$$f(\mathbf{x_2}) - f(\mathbf{x_1}) = -\displaystyle \sum_{i = 1}^{n}\frac{\frac{\partial F}{\partial x_i}}{\frac{\partial F}{\partial y}}(x_{2i} - x_{1i})$$


::::

## Матрица Якоби


:::: {#definition-59}

**Определение:**  Отображение $f: \mathbb{R}^n \to \mathbb{R}^m$ *дифференцируемо* в точке $x_0$, если существует линейное отображение $\varphi: \mathbb{R}^n \to \mathbb{R}^m$, такое, что $f(\mathbf{x_0} + \Delta \mathbf{x}) - f(\mathbf{x_0}) = \varphi(\Delta \mathbf{x}) + \overline{\overline{o}}(\mathbf{x_0}, \mathbf{x_0} + \Delta \mathbf{x}), \,\,\,\, \rho(\mathbf{x_0}, \mathbf{x_0} + \Delta \mathbf{x}) \to 0$.

::::

:::: {#definition-60}

**Определение:**  Пусть $f: \mathbb{R}^n \to \mathbb{R}^m, \,\,\,\, f(\mathbf{x}) = \left(\begin{array}{c}f_1(\mathbf{x})\\\vdots\\f_m(\mathbf{x})\end{array}\right), \,\,\,\, \forall \mathbf{x} \in \mathbb{R}^n$. Пусть $f(\mathbf{x})$ дифференцируемо в $B(\mathbf{x_0})$. Матрица $$\left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right)$$ -- *матрица Якоби* $f$. Если $m = n$, то определитель матрицы Якоби -- *якобиан*.

**Обозначается:** $$J$$

::::

:::: {#statement-27}

**Утверждение:**  Пусть $f: \mathbb{R}^n \to \mathbb{R}^m, \,\,\,\, f(\mathbf{x}) = \left(\begin{array}{c}f_1(\mathbf{x})\\\vdots\\f_m(\mathbf{x})\end{array}\right), \,\,\,\, \forall \mathbf{x} \in \mathbb{R}^n$. Тогда $f(\mathbf{x})$ дифференцируемо в точке $\mathbf{x_0} \in \mathbb{R}^n \Leftrightarrow f_i(\mathbf{x})$ дифференцируема в точке $\mathbf{x_0} \,\,\,\, \forall i \in \{1, \ldots, m\}$.

*Доказательство:* определение $\,\,\,\,\blacksquare$

::::

## Теорема о неявном отображении


:::: {#theorem-50}

**Теорема:**  (О неявном отображении) Пусть $F: \mathbb{R}^{n + m} \to \mathbb{R}^m$ и $F(\mathbf{x}, \mathbf{y}) = \left(\begin{array}{c}f_1(\mathbf{x}, \mathbf{y})\\\vdots\\f_m(\mathbf{x}, \mathbf{y})\end{array}\right), \,\,\,\, \forall \mathbf{x} \in \mathbb{R}^n, \,\,\,\, \mathbf{y} \in \mathbb{R}^m$. Пусть $F \in C^1(B(\mathbf{x_0}, \mathbf{y_0}))$ и 

1. $F(\mathbf{x_0}, \mathbf{y_0}) = 0$
2. $\left|\begin{array}{ccc} \frac{\partial f_1}{\partial y_1} & \dots & \frac{\partial f_1}{\partial y_m} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial y_1} & \dots & \frac{\partial f_m}{\partial y_m} \end{array}\right|_{|(\mathbf{x_0}, \mathbf{y_0})} \ne 0$

Тогда $\exists B(\mathbf{x_0}), \,\,\,\, \exists \{\varphi_i(\mathbf{x}): \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i(\mathbf{x_0}) = y_{0i}, \,\,\,\, \varphi_i \in C^1(B(\mathbf{x_0}))\}_{i = 1}^m$ и $f_i(\mathbf{x}, \varphi_1(\mathbf{x}), \ldots, \varphi_m(\mathbf{x})) = 0 \,\,\,\, \forall i \in \{1, \ldots, m\}$.

*Доказательство:* индукция по $m$ см.стр 32 во втором томе Кудрявцева

::::

:::: {#corollary-1}

**Следствие:**  (теорема об обратном отображении) Пусть $f: \mathbb{R}^n \to \mathbb{R}^n, \,\,\,\, f(\mathbf{x}) = \left(\begin{array}{c}f_1(\mathbf{x})\\\vdots\\f_m(\mathbf{x})\end{array}\right), \,\,\,\, f \in C^1(B(\mathbf{x_0})), \,\,\,\, |J|_{|\mathbf{x_0}} \ne 0$. Тогда $\exists \hat{B}(\mathbf{x_0}): \,\,\,\, \forall \hat{\mathbf{x}} \in \hat{B}(\mathbf{x_0}) \,\,\,\, \exists ! \mathbf{x} \in B(\mathbf{x_0}): \,\,\,\, f(\mathbf{x}) = \hat{\mathbf{x}}$ (это соотношение обозначается $\mathbf{x} = F^{-1}(\hat{\mathbf{x}})$) и $F^{-1} \in C^1(\hat{B}(\mathbf{x_0}))$.

*Доказательство:* $\,\,\,\,\blacksquare$

::::


<details>
<summary></summary>
что может быть больнее обмана в математике?
</details>

## Функциональная зависимость


:::: {#definition-61}

**Определение:**  Пусть $\Omega \subset \mathbb{R}^n$ - область. $\{\varphi_i: \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i \in C^1(\Omega)\}_{i = 1}^m$. Пусть $\hat{\Omega} \subset \displaystyle\bigtimes_{i = 1}^{m - 1}\varphi_i(\Omega) \subset R^{m - 1}$. Если $\exists \Phi: \mathbb{R}^{m - 1} \to \mathbb{R}, \,\,\,\, \Phi \in C^1(\hat{\Omega})$, такое, что $\varphi_m(\mathbf{x}) = \Phi(\varphi_1(\mathbf{x}), \ldots, \varphi_{m - 1}(\mathbf{x})) \,\,\,\, \forall \mathbf{x} \in \Omega$, то функции $\varphi_1, \ldots, \varphi_{m - 1}$ *функционально зависимы* от функции $\varphi_m$. Если $\exists \varphi_i$ функционально зависящая от остальных функций, то система $\varphi_1, \ldots, \varphi_m$ -- *функционально зависима*.

::::

### Необходимые условия функциональной зависимости

:::: {#statement-28}

**Утверждение:**  Пусть $\Omega \subset \mathbb{R}^n$ - область. $\{\varphi_i: \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i \in C^1(\Omega)\}_{i = 1}^m$, $m \le n$ и $f_1, \ldots, f_m$ - функционально зависимы. Тогда $\forall \mathbf{x} \in \Omega \,\,\,\, \operatorname{rk} J < m$, где $J$ - матрица Якоби системы $f_1, \ldots, f_m$.

*Доказательство:* Функции $f_1, \ldots, f_m$ функционально зависимы. Без ограничения общности, считаем, что $f_m = \Phi(f_1, \ldots, f_{m - 1})$. Имеем $\frac{\partial f_m}{\partial x_k} = \displaystyle \sum_{i = 1}^{m - 1}\frac{\partial \Phi}{\partial f_i} \frac{\partial f_i}{\partial x_k}$, то есть $m$-я строка матрицы Якоби линейно выражается через остальные $\,\,\,\,\blacksquare$

::::

:::: {#corollary-2}

**Следствие:**  Пусть $\Omega \subset \mathbb{R}^n$ - область. $\{\varphi_i: \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i \in C^1(\Omega)\}_{i = 1}^m$, $m \le n$. Если $\exists \mathbf{x_0} \in \Omega \,\,\,\, \operatorname{rk} J = m$ в точке $\mathbf{x_0}$, где $J$ - матрица Якоби системы $f_1, \ldots, f_m$, то $f_1, \ldots, f_m$ - функционально независимы. 

*Доказательство:* Такое же как выше. Только надо дописать в начало *Докажем от противного. Пусть*, а в конец *противоречие* $\,\,\,\,\blacksquare$

::::

:::: {#theorem-51}

**Теорема:**  Пусть $\Omega \subset \mathbb{R}^n$ - область. $\{\varphi_i: \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i \in C^1(\Omega)\}_{i = 1}^m$, $m > n$. Если $\operatorname{rk} J = n$, где $J$ - матрица Якоби системы $f_1, \ldots, f_m$, то $f_1, \ldots, f_m$ - функционально зависимы. 

*Доказательство:* Теорема об обратном отображении $\,\,\,\,\blacksquare$

::::

### Достаточные условия функциональной зависимости

:::: {#statement-29}

**Утверждение:**  Пусть $\Omega \subset \mathbb{R}^n$ - область. $\{\varphi_i: \mathbb{R}^n \to \mathbb{R}, \,\,\,\, \varphi_i \in C^1(\Omega)\}_{i = 1}^m$. Если $\exists \mathbf{x_0} \in \Omega \,\,\,\, \operatorname{rk} J < \min(n, m)$ в точке $\mathbf{x_0}$, где $J$ - матрица Якоби системы $f_1, \ldots, f_m$, то $f_1, \ldots, f_m$ - функционально зависима.

*Доказательство:* без доказательства $\,\,\,\,\blacksquare$

::::


## Условный экстремум


:::: {#definition-62}

**Определение:**  Пусть $f, f_1, \ldots, f_m$ определены в $B(\mathbf{x_0}), \,\,\,\, \mathbf{x_0} \in \mathbb{R}^n$. Если $\forall \mathbf{x} \in \{\mathbf{x} \in {B}(\mathbf{x_0}): \,\,\,\, f_i(\mathbf{x}) = 0, \forall i \in \{1, \ldots, m\}\} \,\,\,\, f(\mathbf{x_0}) > f(\mathbf{x})$, то $\mathbf{x_0}$ -- *условный максимум функции* $f$. Система уравнений $f_i(\mathbf{x}) = 0$ -- это *уравнения связи*.

::::


Пусть $f, f_1, \ldots, f_m \in C^1(B(\mathbf{x_0}))$,  $m \le n$ и $\operatorname{rk} \left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right) = m \,\,\,\, \forall \mathbf{x} \in B(\mathbf{x_0})$.

По утверждению система $f_1, \ldots, f_m$ -- функционально независима. Так как ранг в каждой точке окрестности равен $m$, существует матрица $mxm$, состоящая из $m$ столбцов матрицы Якоби, такая, что ее определитель не $0$. Без ограничения общности, считаем, что $\det \left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_{n - m + 1}} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_{n - m + 1}} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right) \ne 0$.

По теореме о неявном отображении существуют $\varphi_1, \ldots, \varphi_m$, такие, что в некоторой окрестности точки $\mathbf{x_0}$

$$x_{n - m + 1} = \varphi_1(x_1, \ldots, x_{x - m})$$
$$\vdots$$
$$x_{n} = \varphi_m(x_1, \ldots, x_{x - m})$$

Подставим $\varphi_i$ в $f$. Имеем 

$$g(x_1, \ldots, x_{n - m}) = f(x_1, \ldots, x_{n - m}, \varphi_1, \ldots, \varphi_m)$$

То есть $\mathbf{x_0}$ точка условного экстремума $f$, если $\mathbf{x_0}$ точка экстремума функции $g$.

### Необходимое условие условного экстремума

:::: {#theorem-52}

**Теорема:**  Пусть $f, f_1, \ldots, f_m \in C^1(B(\mathbf{x_0}))$,  $m \le n$, $\operatorname{rk} \left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right) = m \,\,\,\, \forall \mathbf{x} \in B(\mathbf{x_0})$ и $f$ имеет в точке $\mathbf{x_0}$ условный экстремум при условиях связи $f_i(\mathbf{x}) = 0$. Тогда $\operatorname{grad} f(\mathbf{x_0}), \operatorname{grad} f_1(\mathbf{x_0}),\ldots, \operatorname{grad} f_m(\mathbf{x_0})$ -- линейно зависимы.

*Доказательство:*

::::

## Метод множителей Лагранжа для нахождения условного экстремума


:::: {#definition-63}

**Определение:**  Пусть $f, f_1, \ldots, f_m$ определены в $B(\mathbf{x_0})$. Функция $\mathcal{L}(\lambda_1, \ldots, \lambda_m, x_1, \ldots, x_n) = f(\mathbf{x}) + \displaystyle \sum_{i = 1}^{m}\lambda_i \cdot f_i(\mathbf{x})$ -- *функция Лагранжа* системы $f, f_1, \ldots, f_m$. $\boldsymbol{\lambda} = (\lambda_1, \ldots, \lambda_n)$ -- *множители Лагранжа*.

::::

:::: {#theorem-53}

**Теорема:** Пусть $f, f_1, \ldots, f_m \in C^1(B(\mathbf{x_0}))$,  $m \le n$, $\operatorname{rk} \left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right) = m \,\,\,\, \forall \mathbf{x} \in B(\mathbf{x_0})$ и $f$ имеет в точке $\mathbf{x_0}$ условный экстремум при условиях связи $f_i(\mathbf{x}) = 0$. Тогда $\exists \boldsymbol{\lambda}: \,\,\,\, d\mathcal{L}(\boldsymbol{\lambda}, \mathbf{x_0}) = 0$.

*Доказательство:* Из теоремы имеем $\operatorname{grad} f(\mathbf{x_0}), \operatorname{grad} f_1(\mathbf{x_0}),\ldots, \operatorname{grad} f_m(\mathbf{x_0})$ -- линейно зависимы. Так как $\operatorname{rk} J = m$, $\operatorname{grad} f_1(\mathbf{x_0}),\ldots, \operatorname{grad} f_m(\mathbf{x_0})$ -- линейно независимы. А следовательно $\exists \boldsymbol{\lambda}: \,\,\,\, \operatorname{grad}f = - \displaystyle \sum_{i = 1}^{m}\lambda_i f_i$.

Запишем дифференциал $\mathcal{L}$ в $(\boldsymbol{\lambda}, \mathbf{x_0})$:

$$d\mathcal{L}(\boldsymbol{\lambda}, \mathbf{x_0}) = d f(\mathbf{x_0}) + \displaystyle \sum_{i = 1}^{m}\lambda_i df_i + \displaystyle \sum_{i = 1}^{m}f_i(\mathbf{x})d\lambda_i \,\,\,\,\blacksquare$$

::::

:::: {#theorem-54}

**Теорема:**  (Достаточное условие условного экстремума) Пусть $f, f_1, \ldots, f_m \in C^1(B(\mathbf{x_0}))$,  $m \le n$, $\operatorname{rk} \left(\begin{array}{ccc} \frac{\partial f_1}{\partial x_1} & \dots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \dots & \frac{\partial f_m}{\partial x_n} \end{array}\right) = m \,\,\,\, \forall \mathbf{x} \in B(\mathbf{x_0})$, $d\mathcal{L}(\boldsymbol{\lambda}, \mathbf{x_0}) = 0$. Тогда $f$ имеет в точке $\mathbf{x_0}$ условный экстремум при условиях связи $f_i(\mathbf{x}) = 0$, если $\exists \boldsymbol{\lambda}: \,\,\,\, d^2\mathcal{L}(\boldsymbol{\lambda}, если \mathbf{x_0})$ положительно или отрицательно определена, иначе экстремума нет.

*Доказательство:*

::::

