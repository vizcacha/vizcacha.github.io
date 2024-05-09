---
title: Euler's Homogeneous Function Theorem
author: Steven Canning
---

While reading Landau and Lifschitz's Mechanics book I came across a theorem that I had not encountered before.
First, let us define a homogeneous function.

<div class="definition">
A function $f$ is *homogeneous* of order $k$ if $f(tx_1, \dots, tx_n) = t^k f(x_1, \dots, x_n)$.
</div>

Euler's Homogeneous Function Theorem then states
<div class="theorem">
Let $f(x_1, \dots, x_n)$ be a homogeneous function of order $k$. Then
$$ k f(x_1, \dots, x_n) = \sum_{i=1}^n x_i \frac{\partial f}{\partial x_i}$$
</div>

<div class="proof">
Since $f$ is homogeneous of order $k$, we have $f(tx_1, \dots, tx_n) = t^k f(x_1, \dots, x_n)$.
Taking the derivative with respect to $t$ yields

$$ \sum_{i=1}^n \frac{\partial f}{\partial (tx_i)} \frac{\partial (tx_i)}{\partial t}  = kt^{k-1} f(x_1, \dots, x_n) $$
$$ \sum_{i=1}^n x_i \frac{\partial f}{\partial (tx_i)} = kt^{k-1} f(x_1, \dots, x_n) $$

Taking $t=1$ then yields

$$ \sum_{i=1}^n x_i \frac{\partial f}{\partial (x_i)} = k f(x_1, \dots, x_n) $$
</div>
