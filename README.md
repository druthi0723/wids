# wids mid - term report
This code trains from the given data and then predicts the next text this code is not yet optimized so it generates random gliberish english results
First, it checks whether the file input.txt exists. If not, it automatically downloads the Shakespeare text. Finally, it reads in the full text:

As it is a character-based encoding , unique characters in the text are collected. Each character is then assigned a number and a dictionary for mapping numbers to characters is created.

Finally, the entire text is converted to a PyTorch tensor. The text data itself is divided into 90% training data and 10% validation data. The batch size is set to 8, that means at any instant the model has  8 characters and has to predict the next character.this is done because we dont want our model to remember the example set that we have given but it needs to train and shld be able to predict the next letter

During training, the data are taken in small batches. For every input sequence, the target is the same sequence shifted by one character. This helps the model learn what character usually comes next.

This is a simple Bigram model. Each character has a table, which directly provides scores for the next character. The error between the prediction and the correct character is calculated using cross-entropy loss.
The training process is carried out for a total of 5,000 steps, utilizing the optimizer. During these steps, prediction, calculation of loss, and weight adjustments for improved performance are carried out by the model.


