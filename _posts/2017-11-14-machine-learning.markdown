---
layout: post
title:  "Machine learning Basic"
date:   2017-11-14 12:44:13
categories: ML
permalink: /archivers/machine-learning-basic
use_math: true
---
Gradient descent algorithm

+ $$ cost(W) = {1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
+ $$ cost(W) = {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
+ $$ W := W - \alpha{\delta \over \delta W}cost(W) $$
+ $$ W := W - \alpha{\delta \over \delta W} {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
+ $$ W := W - \alpha{1 \over 2m} \sum_{i=1}^{m} 2(Wx^{(i)}-y^{(i)}) x^{(i)} $$
+ $$ W := W - \alpha{1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)}) x^{(i)} $$  


Linear Regression

* Hypothesis
\begin{align\*}
  H(x) = Wx + b
\end{align\*}
* Cost function
\begin{align\*}
  cost(W,b) = \frac{1}{m} \sum_{i=1}^m (H(x^{(i)}) - y^{(i)})^2
\end{align\*}
* Minimize cost
\begin{align\*}
  minimize cost(W,b)
\end{align\*}


Activation Function

* Sigmoid
\begin{align\*}
  \sigma(x) = \frac{1}{(1+e^2)}
\end{align\*}
* tanh
\begin{align\*}
  tanh(x)
\end{align\*}
* ReLU : Rectified Linear Unit
\begin{align\*}
  max(0,x)
\end{align\*}
* Leaky ReLU
\begin{align\*}
  max(0.1x,x)
\end{align\*}
