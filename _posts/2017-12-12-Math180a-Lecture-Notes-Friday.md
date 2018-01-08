#20171208 Math180a Lecture Notes Friday
@(Cabinet)[Math180a, Lecture Notes]

[TOC]

## Midterm problem 

Given Random Variable $X$ with pdf $f_X(x)$

$$
f_X(x)
\begin{cases}
\frac{1}{2} & -1 < x < 1 \\
0 & \text otherwise
\end{cases}
$$

And $Y = X^2$

1. $E[Y] = E[X^2]$
$$
\begin{align*}
\int_{-\infty}^{\infty} x^2 \cdot f_X(x)dx 
&= \int_{-1}^{1} \frac{1}{2}x^2 \cdot f_X(x)dx \\
&= \frac{1}{6}x^3 \Bigg |_{-1}^{1} = \frac{1}{3}
\end{align*}
$$

2. Find pdf $f_Y(y)$ of $Y$
Possible value for $Y$...$X \in [-1, 1] \to Y \in [0, 1]$ 

Now fix $y \in [0,1]$

$$
\begin{align*}
F_Y(y) &= P(Y \le y) \\
&= P(X^2 \le y) \\
&= P \left(-\sqrt{y} \le X \le \sqrt{y} \right) \\
&= \int_{-\sqrt{y}}^{\sqrt{y}} f_X(x) dx \\
&= \int_{-\sqrt{y}}^{\sqrt{y}} \frac{1}{2} dx \\
&= \frac{2}{2} \sqrt{y} = \sqrt{y}
\end{align*}
$$

$$
f_Y(y) = \frac{d}{dy} F_Y(y) = \frac{1}{2 \sqrt{y}} \\
f_Y(y) = \begin{cases} \frac{1}{2 \sqrt{y}} & 0 < y < 1 \\ 0 & otherwise \end{cases}
$$

## Homework problem 

$X$ : grade of a random student in class.

* Half of the students got about 80
* 10% of the students got about 95

Suppose $X$ has a normal distribution. 

find $P(X < 70)$

1. $\mu = 80$
2. $P(X > 95) = 0.1 \Rightarrow 1 - \Phi(\frac{15}{\sigma}) = 0.1 \Rightarrow \Phi(\frac{15}{\sigma}) = .9 \Rightarrow \frac{15}{\sigma} = 1.28 \Rightarrow \sigma = 11.72$

## Bounds

Suppose $X$ is the weight of a randomly selected apple 

1. $E[X] = 75$, what can you say about $P( X > 85)$? 

> For a non-negative random variable with a known expected value, use Markov's Inequality

$$P(X > 85) \le \frac{E[X]}{85} = \frac{75}{85} = 0.88$$

2. Now suppose we know the standard deviation of $X$ is 5. 
Question: What can you say about $P(65 \le X \le 85)$? 

> By knowing standard deviation, we can use Chebyshev's 

$$P( | X - \mu | \ge a) \le \frac{Var(X)}{a^2}$$
$$P( | X - 75 | \ge 10) = 1 - P(|X - 75| > 10) \le \frac{5^2}{10^2} = 0.25$$
$$P(|X - 75| > 10) \ge 1 - 0.25 = 0.75$$

3. Suppose we now have 100 apples. What can you say about $P( \bar{S}_{100} \ge 80)$, When $\bar{S}_{100}$ is the average weight of 100 apple. 

> By the central limit theorem...

$$E[\bar{S}_{100}] = 75$$
$$Var(\bar{S}_{100}) = \frac{Var(X)}{100} = 0.25$$
$$ \bar{S}_{100} \approx N(75, 0.25) $$

























