# DTSA-5511-NLP

## Project Description

This project is a Kaggles competition and an assignment for DTSA 5511. As I said, the dataset I'm using here is from Kaggle and consists of tweets with labels indicating whether a tweet is a catastrophic tweet (a tweet describing a disaster). Through the data exploration and EDA in the first part, it is found that the data includes 7613 tweets (Text column) and labels (Target column), whether they are talking about a real disaster or not. There are 3271 lines for actual disasters and 4342 lines for non-actual disasters.

To give you a better understanding of this project, I have divided this project into two sections. In the first Section I will import the data and do some visual analysis. Finally, do some preprocessing operations on the data

Another section is a module for building models. Here I have built two models, the CNN model and the LSTM model. I compared the loss and acc of the two of them, and finally chose LSTM as my final model

## Summary
After comparison, we can see that the LSTM model will perform better than the CNN model on this problem. The final validation loss of the LSTM model is about 0.41, and the validation accuracy is about 0.813. On the contrary, the validation loss of the CNN model is about 0.43 and the validation accuracy is about 0.810. So I ended up choosing LSTM as my final model
