# Kaggle Cancer Detection

This is my second submission to a Kaggle Competition, apart from MNIST. I completed this activity after the competition was over, since it was a simpler model that did not need too much background knowledge. The reason for this is to acquaint myself with Keras, refamiliarise myself with developing Machine Learning models, and properly introduce myself to Kaggle Competitions.

I implemented a simple CNN model to classify whether a lymph node scan was cancerous or not. My model has 5 convolutional layers, each with 64 units. There is a fully connected dense layer with 128 units, before a binary output. I added a 30% dropout layer before the binary output.

I have submitted my predictions after training for 7 epochs (1000 steps * 64 batch size per epoch). It scores:
  * 94% on training data
  * 83.1% on testing data
  
These are not very competitive scores. I am approximately 900th out of 1157. The model can be improved with the following steps:

* Train for longer. Accuracy seems to be slowing down, but it has not converged to the point that continuing training would be redundant.
* If training accuracy improves, but testing accuracy doesn't,
  * Increase dropout value/number of layers
  * Data augmentation
* Do research and apply image processing techniques to emphasise specific features that represent what "is" a cancer. This could also be done by looking for similarities in the false positives and false negatives.
  * This may rely on domain specific knowledge
  * This may not be applicable since the difference between cancer and non-cancer is very small in these images

