# SentimentAnalysis of Google Playstore app reviews using Bert(Transformers)
Dataset: Google Play app reviews dataset
This is a multiclass classificxation problem. 
Initially the dataset had 5 classes(1,2,3,4,5) of review scores/ratings. But since the clasess were imbalanced so the classes were converted to just three classes(negative, neutral, positive) to reduce the class imbalance problem. ratings less than 3 were grouped to class 'Negative':0 , ratings equals to 3 were grouped to class 'Neutral':1 and ratings equals to 3 were grouped to class 'Postive':2 👍 

No of classes: 3
Classes: ['Negative', 'Neutral, 'Positive']

Train dataset size: (14171, 12)

Validation dataset size: (787, 12)

Test dataset size: (788, 12)

Tokenization and Attention mask were generated using BERT tokenizer

### Model: PyTorch
BERT cotextual embedding layer,
Dropout layer for regularization,
FC linear layer for classification

Optimizer:Adam optimizer with fixed weight decay

Batch size: 16

Learning Rate: 2e-5

Epochs: 10

Loss function: CrossEntropy Loss

Metrics: Accuracy, Loss

### Result:
Train--> loss 0.0420, accuracy 0.9865

Val-->   loss 0.9834, accuracy 0.8703

### Classification Report:
The F1 score for Negative review: 0.89, Neutral: 0.85, Positive: 0.93
