# Intro-to-Convolutional-Neural-Nets-with-Keras

## 1. Introduction
- What is your MSE/MAE with linreg vs tuned network? 
  - The training MSE/MAE decreased from 21.4733/3.3258 with LinReg to 12.6839/2.5322 and the test MSE decreased from 22.04 with LinReg to 13.44 by simply widening the input alyer from 13 to 32 and deepening the model by adding one layer of size 16.
- What happens to your train and test results if you add 5 hidden layers with 128 neurons each?
  - The training MSE/MAE decrease from 12.6839/2.5322 in the simpler tuned model to 9.6648/2.4278 in the 5 hidden layer model, however, the test MSE actually icnreases from 13.44 to 13.84 which indicates that our model is beginning to become overfit to the training data. It also takes a bit longer to run due to the increased size and number of layers.

## 2. Intro to convolution operations: padding
  - What is a response layer? (Give a brief, 1-sentence description)
  - Given the filter shape of (26, 26, 32), what does each number represent?
  - Given 6x6 input and filter of (3,3): what is the response shape that we get? 
  - Given (33, 33, 1) input and filter of (2,2): what is the response shape that we get? 
  - What is the difference between ‘valid’ and ‘same’ padding? Given 6x6 input and filter of (3,3), what are the response shapes for both options? 
