# DTSA-5511-NLP

## Project Description

This project is a Kaggles competition and an assignment for DTSA 5511. As I said, the dataset I'm using here is from Kaggle and consists of tweets with labels indicating whether a tweet is a catastrophic tweet (a tweet describing a disaster). Through the data exploration and EDA in the first part, it is found that the data includes 7613 tweets (Text column) and labels (Target column), whether they are talking about a real disaster or not. There are 3271 lines for actual disasters and 4342 lines for non-actual disasters.

To give you a better understanding of this project, I have divided this project into two sections. In the first Section I will import the data and do some visual analysis. Finally, do some preprocessing operations on the data

Another section is a module for building models. Here I have built two models, the CNN model and the LSTM model. I compared the loss and acc of the two of them, and finally chose LSTM as my final model

## Model Description 
I trained an LSTM model, you can see the image below, which is an architecture diagram of the model.
1. I use Sigmoid as the activation of the model output because this is a binary classification problem.


2. I initially set a Dropout rate of 0.3, as the initial value, this is not too large, and can also be used to prevent overfitting

3. Most importantly, when I fit the model, I introduced EarlyStopping, which effectively increases the training efficiency of the model, because with the increase of epoch, if the test loss is found to rise on the validation set, the model will stop training

Finally, the val_loss of the model is 0.4103, and the val accuracy is 0.8139

![Structure of LSTM](https://github.com/HughJin-001/DTSA-5511-NLP/blob/main/Screen%20Shot%202022-08-14%20at%2010.41.37%20PM.png)

I trained another CNN model. In order to better compare the model, I use similar parameters, the output activation is also set to sigmoid, and the loss function is also binary_crossentropy. But I set the dropout rate of the hidden node of the CNN model to 0.5, because through cross-validation, when the dropout of the hidden function is 0.5, the effect is good

The CNN model architecture is as follows

![Structure of CNN](https://github.com/HughJin-001/DTSA-5511-NLP/blob/main/Screen%20Shot%202022-08-14%20at%2010.47.53%20PM.png)


## Summary
After comparison, we can see that the LSTM model will perform better than the CNN model on this problem. The final validation loss of the LSTM model is about 0.41, and the validation accuracy is about 0.813. On the contrary, the validation loss of the CNN model is about 0.43 and the validation accuracy is about 0.810. So I ended up choosing LSTM as my final model
