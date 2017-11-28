---
layout: post
title:  "Machine learning Basic"
date:   2017-11-14 12:44:13
categories: ML
permalink: /archivers/machine-learning-basic
use_math: true
---
Gradient descent algorithm \(Linear Regression\)

1. $$ cost(W) = {1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
2. $$ cost(W) = {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
3. $$ W := W - \alpha{\delta \over \delta W}cost(W) $$
4. $$ W := W - \alpha{\delta \over \delta W} {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
5. $$ W := W - \alpha{1 \over 2m} \sum_{i=1}^{m} 2(Wx^{(i)}-y^{(i)}) x^{(i)} $$
6. $$ W := W - \alpha{1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)}) x^{(i)} $$  


Linear Regression

* Hypothesis
\begin{align\*}
  H(x) = Wx + b
\end{align\*}
* Cost function
\begin{align\*}
  cost(W,b) = \frac{1}{m} \sum_{i=1}^m (H(x^{(i)}) - y^{(i)})^2
\end{align\*}

Logistic classification
* Hypothesis
\begin{align\*}
  H(X) = \frac{1}{ 1 + e^{-W^T X}}
\end{align\*}
* Cost function
\begin{align\*}
C(H(x),y) = 
    \begin{cases}
    -\log (H(x)) & : y = 1 \\
    -\log (1-H(x)) & : y = 0 \\
    \end{cases}
\end{align\*}
\begin{align\*}
  C(H(x),y) = -y\log (H(x)) - (1-y)\log (1-H(x))
\end{align\*}
\begin{align\*}
  cost(W) = - \frac{1}{m} \sum y\log (H(x)) + (1-y)\log (1-H(x))
\end{align\*}

Activation Function

* Sigmoid
\begin{align\*}
  \sigma(x) = \frac{1}{(1+e^{-x})}
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
