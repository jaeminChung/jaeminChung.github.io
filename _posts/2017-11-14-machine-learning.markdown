---
layout: post
title:  "Machine learning Basic"
date:   2017-11-14 12:44:13
categories: ML
permalink: /archivers/machine-learning-basic
use_math: true
---
# Gradient descent algorithm - Linear Regression

1. $$ cost(W) = {1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
2. $$ cost(W) = {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
3. $$ W := W - \alpha{\delta \over \delta W}cost(W) $$
4. $$ W := W - \alpha{\delta \over \delta W} {1 \over 2m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)})^{2} $$
5. $$ W := W - \alpha{1 \over 2m} \sum_{i=1}^{m} 2(Wx^{(i)}-y^{(i)}) x^{(i)} $$
6. $$ W := W - \alpha{1 \over m} \sum_{i=1}^{m} (Wx^{(i)}-y^{(i)}) x^{(i)} $$  


# Linear Regression

## Hypothesis
$$
  H(x) = Wx + b
$$
## Cost function
$$
  cost(W,b) = \frac{1}{m} \sum_{i=1}^m (H(x^{(i)}) - y^{(i)})^2
$$

# Logistic classification
## Hypothesis
$$
  H(X) = \frac{1}{ 1 + e^{-W^T X}}
$$
## Cost function
1. $$ C(H(x),y) = 
    \begin{cases}
    -\log (H(x)) & : y = 1 \\
    -\log (1-H(x)) & : y = 0
    \end{cases} $$
2. $$ C(H(x),y) = -y\log (H(x)) - (1-y)\log (1-H(x)) $$
3. $$ cost(W) = - \frac{1}{m} \sum y\log (H(x)) + (1-y)\log (1-H(x)) $$

# Activation Function

## Sigmoid
$$ \sigma(x) = \frac{1}{(1+e^{-x})} $$
## tanh
$$ tanh(x) $$
## ReLU : Rectified Linear Unit
$$ max(0,x) $$
## Leaky ReLU
$$ max(0.1x,x) $$
