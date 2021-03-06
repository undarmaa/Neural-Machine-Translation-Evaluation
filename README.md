# Neural-Machine-Translation-Evaluation

• Built a classifier for evaluating quality of machine translation to predict best matching sentence to the reference sentence.

• Performed feature engineering to select metrics like METEOR and BLEU for evaluating quality of machine translation
using Python libraries such as nltk, sklearn and numpy.

• Computed features once on the training data (consisiting of sentences) like cosine similarity from neural skip n-gram models and pos tagging to better take context into account and then stored them as file.

• Trained a combination of SVM, RandomForest, neural MLP based voting classifier on the computed features. 

• Saved the model using Python Pickle library to a file for quick use next time to classify new test data.

• Outperformed other classmates to be in top 5 among 180. 

# Running instructions

• First paramter is the training data set file containing two sentences along with the reference sentence and the second paramter is the     file containing labels for supervised learning

  python computeTrainFeatures.py -i dev.train -l data/dev.train.answers -n 38234

• Use: "python computeTrainFeatures.py -h" cmd for getting help regarding explaination of parameters.

• Similarly test features can be computed using: python computeTestFeatures.py -i dev.test -n 18351

• Compute the model on the computed features using: python runModel.py

• Run the model for generating predictions and getting accuracy score
  
  python compare-with-human-evaluation -i dev.test -t data/dev.test.answers < eval.out
