# Topological Data Analysis of Cryptocurrencies

I analyze cryptocurrencies focusing on Bitcoin(BTC) using topological data analysis. [This article](https://arxiv.org/abs/1703.04385) provides a method to do so. 

Given a time series $\{x^k_n\}$, we define a point $$ x(t_n) = (x_n^1, x_n^2, \dots, x_n^d) \in \mathbb{R}^d. $$ Given a window size $w$, we define $X_n$ to be the point cloud $$X_n = (x(t_n), x(t_{n+1}), \dots , x(t_{t+w-1}).$$ This allows us to apply the techniques of topological data analysis, and use persisten homology.

From the persistent homology, we are able to get features such as the persistence barcode, persistence diagram, and the persistence landscape. In particular, for the persistence landscape, we can measure its $L^p$ norm. For a function $f(x)$, its $L^p$ norm $\lVert f(x) \rVert_p$ is defined to be $$ \left(\int |f(x)|^p dx\right)^\frac{1}{p}. $$
