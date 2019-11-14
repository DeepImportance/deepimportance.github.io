---
layout: default
---


# Importance Driven Coverage of Deep Learning Systems
Deep Learning (DL) systems are key enablers for engineering intelligent applications due to their ability to solve complex tasks such as image recognition and machine translation.
Nevertheless, using DL systems in safety- and security-critical applications requires to provide testing evidence for their dependable operation.
Recent research in this direction focuses on adapting testing criteria from traditional software engineering as a means of increasing confidence for their correct behaviour.
However, they are inadequate in capturing the intrinsic properties exhibited by these systems. We bridge this gap by introducing DeepImportance, a systematic testing methodology accompanied by an _Importance-Driven_ (IDC) test adequacy criterion for DL systems.
Applying IDC enables to establish a _layer-wise functional understanding_ of the importance of DL system components  and use this information to guide the generation of _semantically-diverse_ test sets.
Our empirical evaluation on several DL systems, across multiple DL datasets and with state-of-the-art adversarial generation techniques demonstrates the usefulness and effectiveness of DeepImportance and its ability to guide the engineering of more robust DL systems.


## Overview
![over](./assets/images/overview.png)

Using a pre-trained DL system, DeepImportance analyses the training set
_T_ to establish a fundamental understanding of the overall contri bution made by internal neurons of the DL system. This enables to identify the most important neurons that are core contributors to the decision-making process. Then, DeepImportance carries out a quantisation step which produces an
automatically-determined finite set of clusters of neuron activation values that characterises, to a sufficient level, how the behaviour of the most
important neurons changes with respect to inputs from the training set. Finally, DeepImportance uses the produced clusters of the most important neurons to assess the coverage adequacy of the test set. Informally, the
Importance-Driven test adequacy criterion of DeepImportance is satisfied when all combinations of important neurons clusters are exercised

## Evaluation

### Robustness
![robust](./assets/images/robustness.png)

### Hyperparameters Chosen In Evaluation
**CW:**
```
 batch_size=1,
 confidence=0,
 learning_rate=5e-3,
 binary_search_steps=5,
 max_iterations=1000,
 abort_early=True,
 initial_const=1e-2,
 clip_min=0,
 clip_max=1
```

**FGSM:**
```
 eps=0.3,
 ord=np.inf,
 y=None,
 y_target=None,
 clip_min=None,
 clip_max=None,
 clip_grad=False,
 sanity_checks=True,
```

**BIM:**
```
 eps=0.3,
 eps_iter=0.05,
 nb_iter=10,
 y=None,
 ord=np.inf,
 clip_min=None,
 clip_max=None,
 y_target=None,
 rand_init=None,
 rand_init_eps=None,
 clip_grad=False
```

**JSMA:**
```
 theta=1,
 gamma=1,
 clip_min=0,
 clip_max=1,
 y_target=None,
 symbolic_impl=True
```

**Training Parameters for LeNet Models:**
```
loss = 'categorical_crossentropy'
optimizer = 'adadelta'  --> (learning_rate=1.0, rho=0.95)
metrics = ['accuracy']
batch_size = 256,
epochs = 10
```

**Training Parameters for CIFAR Model:**
```
loss = 'categorical_crossentropy'
optimizer = 'RMSprop'  --> (learning_rate=0.0001, decay=1e-6)
metrics = ['accuracy']
batch_size = 32,
epochs = 40
```

**Training Parameters for DAVE Model:**
```
loss = 'mse'
optimizer = 'adadelta'  --> (learning_rate=1.0, rho=0.95)
batch_size = 256,
epochs = 10
```
