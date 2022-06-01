# Intro-to-Convolutional-Neural-Nets-with-Keras

## 1. Introduction
- What is your MSE/MAE with linreg vs tuned network? 
  - The training MSE/MAE decreased from 21.4733/3.3258 with LinReg to 12.6839/2.5322 and the test MSE decreased from 22.04 with LinReg to 13.44 by simply widening the input alyer from 13 to 32 and deepening the model by adding one layer of size 16.
- What happens to your train and test results if you add 5 hidden layers with 128 neurons each?
  - The training MSE/MAE decrease from 12.6839/2.5322 in the simpler tuned model to 9.6648/2.4278 in the 5 hidden layer model, however, the test MSE actually icnreases from 13.44 to 13.84 which indicates that our model is beginning to become overfit to the training data. It also takes a bit longer to run due to the increased size and number of layers.

## 2. Intro to convolution operations: padding
  - What is a response layer? (Give a brief, 1-sentence description)
    - A response layer is a slightly smaller (in the x,y dimension), but deeper (in the z dimension) convulution of the original input.
  - Given the filter shape of (26, 26, 32), what does each number represent?
    - The 26s are the x and y number of pizels of the filter shape and the 32 is how many filters there are, so in this example we would have 32 stacked (26x26) filter layers.
  - Given 6x6 input and filter of (3,3): what is the response shape that we get? 
    - The response shape would be (4,4)
  - Given (33, 33, 1) input and filter of (2,2): what is the response shape that we get? 
    - 33-3+1 = 31 so (31,31)
  - What is the difference between ‘valid’ and ‘same’ padding? Given 6x6 input and filter of (3,3), what are the response shapes for both options?
    - The default option is valid padding which is no padding or disabled padding. Same padding is padding with an equal input and output size. Thus, the response shape for both options would be the same size of (4,4)

## 3. Convolution parameters: stride and pooling
  - What is max pooling? (Give a brief, 1-sentence description)
    - An aggressive downsampling technique where the downsampled output is the max of the given window.
  - If I apply pooling of 2 (2,2 window with a stride of 2) to a (6,6) array, what is the resulting size?
    - (3,3)

## 4. ConvNet Architectures, layers
  - Define I, O, F, S, P as used in this lecture (Give a brief, 1-sentence description)
    - I: Input Volume (ex. size of the image), F: filter (ex. kernel zie), S: Stride, P: padding (usually zero padding) these are the pieces that make up every ConvNet architecture.
  - What is my output size if Input = (100, 100), kernel size=(2, 2), the stride of 1, and no pooling?
    - (I-F+2P)/S + 1 = (100-2+2(0))/1 + 1 = 99 so (99, 99)
  - How many weights do I have if I have 24 such filters stacked (conv2_24)?
    - 2x2x1x24x24 = 2304
  - Solve for the padding (P), in terms of I, F, and S, if we want the input and output size to remain the same. 
    - P = (S + F)/2

## 5. Practical patterns
  - What can we use the ImageDataGenerator for? What can it help us fight? (Give a brief, 1-sentence description)
    - It can turn image files into pre-processed tensors for our machine learning models, but it can also help fight overfitting by randomly generating image transformations or "augmented" data which allows the model to generalize better.
  - What is a better idea: To use one larger kernel (8,8) or multiple stacked smaller ones, 4x(2,2)? Why? Show the number of weights for each option. 
    - 









