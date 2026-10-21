# Proof of the Row-Difference Formula

## Setup

Let

$$
P_t =
\begin{pmatrix}
1-\dfrac{a}{t^{p}} & \dfrac{a}{t^{p}} \\[2ex]
\dfrac{b}{t^{p}} & 1-\dfrac{b}{t^{p}}
\end{pmatrix},
\qquad a,b>0,\; p>0,
$$

and

$$
Q_n = P_1P_2\cdots P_n =
\begin{pmatrix}
x_n & 1-x_n \\
y_n & 1-y_n
\end{pmatrix},
\qquad \delta_n = x_n - y_n .
$$

## Recurrence

Since $Q_{n+1}=Q_nP_{n+1}$, matrix multiplication gives

$$
x_{n+1} = x_n\left(1-\frac{a}{(n+1)^{p}}\right) + (1-x_n)\frac{b}{(n+1)^{p}},
$$

$$
y_{n+1} = y_n\left(1-\frac{a}{(n+1)^{p}}\right) + (1-y_n)\frac{b}{(n+1)^{p}}.
$$

Subtracting the second equation from the first yields

$$
\begin{aligned}
\delta_{n+1} &= x_{n+1}-y_{n+1} \\
&= (x_n-y_n)\left(1-\frac{a+b}{(n+1)^{p}}\right),
\end{aligned}
$$

that is,

$$
\delta_{n+1} = \delta_n\left(1-\frac{a+b}{(n+1)^{p}}\right). \tag{1}
$$

## Theorem 1

For the transition matrices defined above, the row difference is

$$
\delta_n = \delta_0\prod_{t=1}^{n}\left(1-\frac{a+b}{t^{p}}\right), \tag{2}
$$

where $Q_0=I$ and $\delta_0=1$.

## Proof

We proceed by induction. For $n=0$, the product is empty and equals $1$, so the formula gives $\delta_0=1$.

Suppose the formula holds for $n$. By the recurrence relation (1),

$$
\begin{aligned}
\delta_{n+1} &= \delta_n\left(1-\frac{a+b}{(n+1)^{p}}\right) \\
&= \delta_0\prod_{t=1}^{n}\left(1-\frac{a+b}{t^{p}}\right)\left(1-\frac{a+b}{(n+1)^{p}}\right) \\
&= \delta_0\prod_{t=1}^{n+1}\left(1-\frac{a+b}{t^{p}}\right).
\end{aligned}
$$

Thus, the formula holds for $n+1$, completing the induction. $\blacksquare$
