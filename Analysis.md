In this deep-learning neural ntework model, there are total three hidden layers with 84, 50 and 20 neurons respectively. The input shape was (42,) and output layer's neurons was 1 (binary_classification). The optimizer is adam and loss metrics setting is binary_crossentropy.

The model's predictive accuracy was under 75%, which means the model was not able to predict correctly whether or not a target company will be re-funded over 57% of the time.

In order to try and improve the model predictive performance, I tried to remove outliers and noisy in ASK_AMT variable by using 3 times of zscore method. In addition, removing irrelerant variables provided a few improvement. remove_outliers.PNG

Despite of reducing dimensionality with PCA (Principal Component Analysis), the model's accuracy didn't significantly improve.

I tried to add a LeakyReLU layer to deep-learning model, but it didn't work as I expected. Furthermore, adding some regularizers on nauron's kernel still failed.

![Alt text](Images\accuracy_score.PNG "Optional Title")
