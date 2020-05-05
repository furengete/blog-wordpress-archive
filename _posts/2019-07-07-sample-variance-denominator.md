---
title: "为什么样本方差 (sample variance) 的分母是 n-1？"
date: "2019-07-07"
---

用樣本的表現估測總體的表現，是和總體有差距的，並且會低估總體的表現.

當分母為 $latex n$ 時，即 $latex S\_{n}^{2}=\\frac{\\sum\_{i=1}^{n}{(x\_{i}-\\bar{x})^{2}}}{n}$

$latex \\bar{x}$ 為樣本的平均值，總體的平均值為 $latex \\mu$ ，這裏我們不知道總體的均值是多少

通過大量統計數據發現相較於總體方差 $latex \\sigma^{2}$

$latex S\_{n}^{2}$ 的結果更接近 $latex \\frac{n-1}{n}\\cdot \\sigma^{2}$

為了讓樣本方差的計算結果 $latex \\frac{n-1}{n}\\cdot \\sigma^{2}$ 接近總體方差 $latex \\sigma^{2}$

$latex \\Rightarrow\\frac{n-1}{n}\\cdot \\sigma^{2}\\cdot \\frac{n}{n-1}=\\sigma^{2}$

$latex \\frac{\\sum\_{i=1}^{n}{(x\_{i}-\\bar{x})^{2}}}{n} \\cdot \\frac{n}{n-1}=\\frac{\\sum\_{i=1}^{n}{(x\_{i}-\\bar{x})^{2}}}{n-1} = S\_{n-1}^{2}$

大家看到公式會認為是分母被設為 $latex n-1$ ，但實際上是 $latex S\_{n}^{2}\\cdot \\frac{n}{n-1}$ 的結果.

所以現在有兩個，一個不那麼準，另一個更準確.

$latex S\_{n}^{2}=\\frac{\\sum\_{i=1}^{n}{(x\_{i}-\\bar{x})^{2}}}{n}$ (biased estimate)

$latex S\_{n-1}^{2}=\\frac{\\sum\_{i=1}^{n}{(x\_{i}-\\bar{x})^{2}}}{n-1}$ (unbiased estimate)

平時看到的 $latex S^{2}$ 大概就是指 unbiased estimate ，雖然沒有標明是 $latex n$ 還是 $latex n-1$ .
