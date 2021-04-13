# emsemble_learning

## task-7 14th Apr. 打卡

### voting and bagging

### 为什么voting/bagging能让模型表现更好呢？
- model performance depends on bias and variance
- voting won't deteriorate nor improve model bias but it helps reduce 
variance 
  - why? Var(emsemble model) = 1/N Var(meta models)
  - assume we are emsembling by mean
    
但是上述公式成立的条件是 1 emsemble by mean 2 mega models are indepedents

在实际操作中，所有的模型都是condition on training data的，那怎么做才能增加model
independence呢？
- bagging! 
- every meta model is conditioning on a bootstapped training data

![image info](./figures/formula1.jpeg)

所以 rho 越小，模型的方差越小，因此为了减少模型方差，使用了bagging,让每一个meta model
所对应的训练数据是不一样的，因而降低了模型间的相关性。