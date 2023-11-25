---
layout: post
title: 改进大O记号
des: 大O记号破坏了等于和一众运算的和平！
tags: number-theory
---

大O记号，确实是一众渐近符号里最好用的一个，然而确有很多的弊端。

首先，它严重破坏了等于号的传递性。

$$
\begin{array}{c}
1= \mathcal O(1)\\
1= \mathcal O(x)\\
\not\Rightarrow \mathcal O(1)= \mathcal O(x)
\end{array}
$$

对于这一点，我想到了一种解决方案：把等于号改成 $\lesssim$ 。
若 $\exists M>0,\forall x>a,|f(x)|<Mg(x)$，则称
$f(x)\lesssim \mathcal{O}(g(x)). $
 $\lesssim$ 具有和 $\le$ 类似的性质。


其次，它不能进行乘除法。不过可以证明这种替代：

$$
f(x)\lesssim\mathcal{O}(ag(x))\Leftrightarrow f(x)\lesssim\sum_{i=1}^{a} \mathcal{O}(g(x))\quad(a>0)
$$

