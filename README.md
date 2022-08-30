# deep-learning-challenge

### Robert Lane  
[LinkedIn](https://www.linkedin.com/in/robert-lane-jr/) [GitHub](https://github.com/RL-Lane)

## Overview  
The goal of this project is to train a neural network (via Tensorflow) to predict whether or not charitable funding applications will be successfully funded.  This dataset contains over 34,000 organizations which have receive funding in the past.

## Results  
The neural network model initially managed to correctly predict funding status approximately 74% of the time, but after adding the NAME column back into the dataset, accuracy  was increased to about 96% with lower model losses.

  * **Data Preprocessing**
    * The target column used for training this network is IS_SUCCESSFUL.
    * NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT are all variables which have been used to create the model.
    * EIN, STATUS, and SPECIAL_CONSIDERATIONS seem to not affect the outcome by a useful amount, and were thus ignored.
  * **Compiling, Training, and Evaluating the Model**
    * The final model uses 100 neurons on both hidden layers.  Two different activation functions were used in hopes that different strengths of each function would help achieve a better result.  Although the saved notebook may not show it, Over 12 individual functions were tried with varying success.  By far, the biggest factor which increased the score of this model was by making better selections of input variables.
    * The target of 75% accuracy was exceeded by a healthy margin.
    * Several activation functions were used in an attempt to increase the scores over several epochs: avg_pool, crelu, elu, relu, adam,  gelu, pool, selu, relu6, and tanh; of these, only marginal differences in performance were noted.  In addition, several optimizer algorithms were tried: Adamax, Adam, RMSprop, SGD, and Ftrl; the final score was largely the same with these optimizers, except for Ftrl, which in this case scored about 51%.
    
## Summary  
It is worth experimenting with different types of machine learning algorithms.  A more intricate model does not always yield more precise results.  Instead, the first step should always be to thoroughly explore the data in an attempt to discern which inputs are actually tied to the training target.

Bad data will always yield bad results.

If one is asked to recommend a model, the best place to start with would be the simplest and fastest models first.  It could well be that a simpler model is all that is needed to solve a problem, but checking several different types is always a good idea.