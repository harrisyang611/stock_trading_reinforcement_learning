In this project, we will use Reinforcement Learning to train our trading stragety.

It is originally depends on the Tatsat's book: Machine Learning and Data Science Blueprints for Finance. You can find the original code from [Github Link](https://github.com/tatsath/fin-ml)

There are two main notebooks you can refer, both of them works but slightly different.

The change I made is the following:

- change Relu to LeakyRelu to keep the negative values from the state
- introduce act selection mechnism given inventory to prevent short selling happening
- disable epsilon soft act selection during the test/evaluation phrase to avoid our final test result being affected from the random selected actions
- (optional) I tried with and without sigmoid function during the state convertion in scripts ReinforcementLearningBasedTradingStrategy_leaky_relu.ipynb and ReinforcementLearningBasedTradingStrategy_without_sigmoid.ipynb and both of them provide good result, but to use which model, it's up to the users' objective.

Those corrections cure the original issues like short selling, non consistent test result, etc.



