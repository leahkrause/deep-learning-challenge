# deep-learning-challenge

Overview of the analysis:
Using a variety of different factors, this tool predicts whether or not applicants will be successful if funded by Alphabet Soup.

Results: 

Data Preprocessing
- Whether or not the applicant is successful (whether the money is used effectively) is the target for the model
- The features of the model include application type, affiliated sector of industry, government organization classification, use case for funding, organization type, active status, income classification, special considerations for application, and funding amount requested
- Variables removed from data because they are neither features nor targets are the EIN and NAME (identification columns)


Compiling, Training, and Evaluating the Model
- Although the model performance never surpassed the target 75% accuracy prediction, it did get close with the closest accuracy prediction being 72.6%
- The model that had a 72.6% accuracy prediction utilized two hidden layers (with 80 and 30 neurons, respectively), relu activation function, and 100 epochs. This was utilized due to it's high accuracy
- In an effort to increase model performance, I binned and replaced ASK_AMT with the same binning and replacement method used for APPLICATION_TYPE and CLASSIFICATION. I used a cutoff value of 25398 for this binning. This did not improve the accuracy prediction, so next I doubled the amount of neurons for each one of the hidden layers (160 and 60 neurons, respectively). This effort did not increase the accuracy prediction either, so lastly I added a third hidden layer using 15 neurons. Unfortunately, none of these attempts were able to improve the 72.6% accuracy prediction score. 

Overall, this model can be trusted to predict the accuracy of whether or not applicants will be successful if funded by Alphabet Soup 72.6% of the time. While this is the majority of the time, the score is low enough for me to recommend additional efforts to be made in order to increase this rate. I would suggest to next try changing the epochs, or adjusting which columns are being utilized in prediction and more binning to rid outliers. 
