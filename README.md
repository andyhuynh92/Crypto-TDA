# Topological Data Analysis of Cryptocurrencies

I analyze cryptocurrencies focusing on Bitcoin(BTC) using topological data analysis. [This article](https://arxiv.org/abs/1703.04385) provides a method to apply TDA to stocks. I will use an adaptation of this method.  

An initial analysis of bitcoin shows a cyclic structure. One feature of Bitcoin is the halving occuring around every 4 years. This is when the reward of bitcoin after mining is cut in half. This halving might be the reason or a contribution to the cyclic structure of BTC. At the time of this writing, there have been 3 halvings so far. Using the halving dates as reference points to measure between cycles, I want to analyze the time series of the BTC-USD price using topological data analysis. 

## Technical Details

Given a time series $\{x^k_n\}$, we define a point $$x(t_n) = (x_n^1, x_n^2, \dots, x_n^d) \in \mathbb{R}^d.$$ Given a window size $w$, we define $X_n$ to be the point cloud $$X_n = (x(t_n), x(t_{n+1}), \dots , x(t_{t+w-1}).$$ This allows us to apply the techniques of topological data analysis, and use persisten homology.

From the persistent homology, we are able to get features such as the persistence barcode, persistence diagram, and the persistence landscape. In particular, for the persistence landscape, we can measure its $L^p$ norm. For a function $f(x)$, its $L^p$ norm is defined to be $$ \left(\int |f(x)|^p dx\right)^\frac{1}{p}. $$

The paper claims that the $L^p$ norms when analyzing stock market data exhibits strong growth right before a crash.
