---
layout: post
title: 牛莱公式的新证明
des: 复分析里的Newton-Leibniz公式
tags: analysis
---
本想再证Cauchy-Goursat积分定理，写下来却发现漏洞，故作罢。然其中过程颇有趣，而后又偶见Abel求和公式之证明，忽灵感涌现，想出此证明。

任取区域 $D$ 内一条简单曲线 $L$ ，在 $L$ 上取分点 $z_0,z_1\cdots z_n$ ，其中 $z_0$ 是 $L$ 的起点而 $z_n$ 是 $L$ 的终点. 
设 $F(z)$ 是 $D$ 上的解析函数，并且在 $D$ 内有 $F'(z)=f(z)$ . So we have

$$
f(z_i)=\lim_{\lambda\to 0}\frac{F(z_{i+1})-F(z_i)}{z_{i+1}-z_i}
$$

Hence

$$\begin{align*}
\int_{L}f(z)\mathrm dz
=&\int_{z_0}^{z_n}f(z)\mathrm dz\\
=&\lim_{\lambda\to 0}\sum_{i=0}^{n-1}\frac{F(z_{i+1})-F(z_i)}{z_{i+1}-z_i}(z_{i+1}-z_i)\\
=&\lim_{\lambda\to 0}\sum_{i=0}^{n-1}F(z_{i+1})-F(z_i)\\
=&F(z_{n})-F(z_0)\\
\end{align*}
$$

Q.E.D.