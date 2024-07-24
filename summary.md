---
layout: default
title: Summary 1
permalink: /summary1/
mathjax: True
---

## Machine Learning Concepts to Remember

1. Classification and Regression Problems
2. The Bayesian Approach
3. The Frequentist Approach
4. The Learning Problem
5. Probably Approximately Correct (PAC) Learning
6. Empirical Risk Minimization
7. Measure Concentration
8. Vapnick-Chervonenkis Dimension
9. Characterization of UWLLN
10. PAC Learnablity
11. VC dimensions of and Halfspaces and Neural Networks
12. Computation Learning
13. Training Error, Test Error
14. Regularization
15. Representation Capability of Neural Networks
16. Training Neural Networks
17. Modifications in Training NNs
18. Convex Sets and Convex Functions
19. Stochastic Gradient Descent
20. CNNs, Autoencoders and GANs
21. Support Vector Machines
22. Boosting
23. Gaussian Process based Learning
24. Decision Trees and Random Forests
25. Clustering
26. Recurrent Neural Networks
27. LSTM Networks
28. Transformers
29. BERT
30. GPT


### Decision Trees and Random Forests

1. Decision Trees suffer with stability with a minor change in data, therefore must be replaced with random forest of
decision trees. 
2. Deep trees also decrease the accuracy, since they make increase over fitting, hence less bias more variances
3. Random forests is an ensemble of decision of trees, a way to average the multiple deep decision trees.
4. Random forests are constructed as ensemble of decision trees at training time.
5. Booststrap aggregating or bagging, to tree learners: Say training set has $X=x_1, x_2, ..x_n$ with, train B trees using samples from training set with replacements independently, in the testing phase use the outputs from the B trees
and use average or weighted majority response. This is also called boostrapp (idea of sampling data with replacement) aggregating since each trained tree is independent


### ML Metrics

1. Accuracy
2. Sensitivity
3. Specificity
4. Precision
5. Miss rate
6. False discovery rate
7. False omission rate


### Classification and Regression Problems

X = Feature Vector $x \in X$


### K means clustering: 
Unsupervised algorithm,

psuedo code: Generate some randmo

### KNN nearest neighbors: 
Supervised algorithm

Psuedo code: 


## Classification and Regression Problem
1. X is a feature vector $x \in X$
2. y is label

Goal: Given X, predict y

### Binary classification y = {0,1}
### Multinary Classification y = {0,1,2..4}

Regression $y \in R$

### Bayesian Approach
Suppose we know the joint probability distribution and we want to predict y from x

i.e., y=h(x) be the prediction

Loss Function L(y',y): Binary Classification 1(y \neq y')

If it is regression problem, Loss function (y'-y)^2

Goal: Min E(x,y)[L(h(x),y)] # also called bayesian risk
P(x,y) = P(x).P(y|x)

P(x,y) = P(x).P(y|x)

### Frequentist approach

We don't know the joint probability distribution 
P(x,y) = P(x)P(y|x)
       = P(y)P(x|y)

we want to predict y from x, here x is observation, likelihood probability
P(x|y), probability that our x came from y

But we don't know prior distribution

The MLE h_ml(x) \in Arg Max P(x|y)
 we need to find y that maximizes the likelihood probabilities

 Coin parametried by \theta in Bernouli's case

 
 ### Asymptotic behaviour of ML: Bernouli Case

 Coin toss, parameterized by theta in [0,1]

 theta = True Parameter in [0,1]

 m iid coin flips {x1,x2,x3,..xm}

 we want to estimate the emperical mean: theta_ml = 1/m sum(x)

 expected vs true

 Markov Inequality: 
 Suppose z>0 is non-negative r.v 

 p(z>0) < EZ/a


 ### PAC  learning

 X = set of feature vectors
 y = set of labels

 H subset y, class of hypotheses

 S= {(x1,y1),... (xm,ym)}
 = labeled samples

 True hypothesis
 D= Unknown probability distribution on X

 Loss Function l(y,y)

 P(z2>a) < EZ2/a2

 P(|theta_ml - theta|>epsilon) < theta(1-theta)/epsilon*m

 Weak Law of Large Numbers
 error is greater than epsilon for a given delta
 P(|mean|>epsilon) < delta

 when m is large enough i.e., theta_ml converges to theta in probability

we learn theta in probability

 have high confidence that random labeled sample will allow us to have an accurate hypothesis


 ### Empirical Risk Minimization


 Training error of H = 1/m \sum(l(h,y))

 H is arg min that minimizes training error, minimizes error of labelled sample


 Uniform convergence in the WLLN

 WLLN states the empirical and true loss converges when number of loss samples are high

 UWLLN

 ## Measure concentration

 Z1, Z2, ..iid 
 a < Z < b are bounded random variable and mean is mu

 then P(|z-u|>epsilon) < Ze(-zm(epsilon/(b-a)2)) 



### Neural Networks

RELU: max(z,0)

Sigmoid theta(u) = 1/(1+e-u)

### Cross validation
1. Separate data into training set and test set
2. Test set
3. Validation set (we can never make sure the data is )
4. K-fold cross validation: Test, train, train, train, train
5. Train, test, train, train, train, train

### Tikhonov regularization

Bias vs Variance

Bias: Learning is biased towards certain variables in the data: Underfitting of the dataset

Variance: Overfitting can cause

Stability due to regularization: Changing data slightly doesn't change estimate too much

No overfitting
As m-> infinity
test error is close to training error

## Regression

y=f(w,x) belongs R

min_w regression -- min minimize l2 loss over all the training samples
however perform gradient descent only over the small set of samples


Binary classification:

min z $\sum^m_1[1(y=1)y(x,w)+1(y=0)(1-y(x,w))]$ -- Cross entropy loss

Cross entropy loss formula: 

H(p,q)=-E[log q]
where E is expected value operator with respect to the distribution p over a given set is defined
as follows

expected value of log of predicted loss if both are equal, then cross entropy is equal to entropy of p

also written as H(p,q) = H(p)+D(p||q)

In information theoritic sense, Cross entropy measures how many bits are needed 

H(p) is entropy of p 

## KL divergence: defines how far two distributions are different

D_KL(P||Q)


## Gradient descent 

Chain rule of dy/dz=(dy/dx)*(dx/dz)

y=wx+b, output neuron f(y) f is an activation function
y=wx+b, f(y)/dw = f(y)/dy*dy/dw, goal is to find out how much f is getting
affected by w and b, since those are the parameters, we want to learn

goal of differentiation is we want to find out, we find 


### gradient update algorithm
wn+1=wn-stepsize*Delta(L(w))
stepsize >0 non-negative, convergence analysis shows that 
Can converge to local minima

### Momemtum update over velocity update
make loss function a function of v 



### Weight update types
1. Momentum:  vn = alpha vn - etaL(w) 
Momemtum is running mean of gradient, which is
v_t+1=(rho)v_t+gradients rho is generally 
x_t+1=x_t-alpha v_t, rho is .9

RMS prop: Add element-wise scaling of gradient based on sume of squares in each dimension

### adagrad maintains cache of weights

### RMS prop
 ## 


### Several stepsize selection rules

### K nearest neighbors classifier

### Error analysis is done using taylor series

Occam's razor: Among multiple competing hypotheses, the simplest is the best


Regularization reduces the overfitting and model complexity
size we are not just minimizing the loss functions, we are also minimizing the weights



L2 regularization:  sum of squares of each weight 
L1 regularization: absolute sum of each weight


### Dropout: Only used in training phase

### Batch Normalization:

### Stochastic depth, fractional pooling



### Large datasets, data can be redundant

### don't turn down the learning rate



###  Shifting the inputs

####

###
RMS prop: changes step size for adaptively for each
gradient

SGD: Find average of gradients over mini batches.

### training loss is calculated over the gradient

RMSPROP is keep moving average of squared gradient of each weight

MeanSquare(w,t) = .9 Meansquare(w,t-1)+.1 derivative square
and divide gradient by squareroot of the above. 

## here is a path of training neural networks
1. Try gradient descent with momemtum
2. Try rmsprop and 

### stochastic gradient descent is on the batch

while True:
 data_batch = sample_training_data(data, 256)
 weights_grads = evaluate_gradient(loss_fun,data_batch,weights)
 weights += -step_size*weights_grad

### momentum has information of past gradient or direction of motion

RMSProp::  
while True:
    dx=compute_gradient(x)
    vx=rho*vx+dx
    x-= learning_rate*vx+dx(np.sqrt(grad_squared)+1e-7)


Optimizers: Adam (almost)


Adam with beta1= 0.9
beta2=.999, lr- 1e-3 or 5e-4
 is great for many models

 calculate first moment

 first_moment =beta1*first_moment + (1-beta1)*dx
 second_moment= beta2*second_moment + (1-beta2)*dx*dx
 first_unbias= first_moment /(1-beta1**t)
 second_unbias= second_moment / (1-beta2**t)
 x-=lr*first_unbias/(np.sqrt(second_unbias)+1e-7)

 add the regularize

 ## Learning rate decay

 1. Step: exponential
 2. Cosine: .5*alpha_0(1+cos(t*pi/T))


 ## usually preferred is adam(W)
 is good default choice in many cases:
 it often works ok even with constant learning rate
 SGD+Momentum can outperform Adam but may require tuning


 ### adagrad maintains previous gradients

 ### maintains 


 #### Recurrent Neural Networks: Process Sequences

 1. one to one -- 
 2. one to many
 3. many to one
 4. many to many


 ### difference between LSTM and RNN
 