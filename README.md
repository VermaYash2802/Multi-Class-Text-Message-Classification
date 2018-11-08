# Multi-Class-Text-Message-Classification
Goal - Given a new text message, we want to assign it into one of the 6 categories. 

Classes taken (class_id) - 
1. personal
2. promotional
3. Temporary/ OTP
4. bank 
5. Promotions from service provider (like Vodafone)
6. miscellanous (orders, temporary OTP*)

Goal - Given a new text message, we want to assign it into one of these 6 categories. (We've assumed that the incoming message would fall into any of these 6 categories). We've already cleaned the data in the excel file. (We've not used a .csv file because of the fact that 'utf-8' codec cannot be decode byte 0x89 in a csv file)

Most of the classifiers and learning algorithms expect numerical feature vectors with a fixed size rather than raw text documents with variable length (as they cannot directly process the text). Therefore, during the preprocessing step, the texts are converted to a more manageable representation.
Specifically, for each term in our dataset, we calculate a measure called Term Frequency, Inverse Document Frequency, abbreviated to tf-idf. For each document, the message in our case, the presence (and often the frequency) of words is taken into consideration, but the order in which they occur is ignored.
We have tested different machine learning models, evaluating their accuracies to identify the best model. 4 Models used - Logistic Regression, Multinomial Naive Bayes, Linear Support Vector Machine, Random Forest.
