# Conducting Sentiment Analysis:

This work is a subset of the join project work done with my colleague Wang Chun Wei (wcwei2). Full project work description could be found at "https://github.com/weiwangchun/cs410.git".  As a part of this full project, following work has been done: 

Step 1: 10-Q and 10-K of a company are extracted. - Done by Wang Chun Wei (wcwei2)
Step 2: This forms the input to my program "SentimentAnalysis.py".  - Done by Venkat Rao Bhamidipathi (vrb3)
Step 3: Consolidate Step 1 and Step 2 into a single report - Done by Wang Chun Wei (wcwei2)

Here, Step 2 has been explained in detailed i.e. part of work done by me. 

Main Program : "SentimentAnalysis.py" is the python version of the Main Program. For convinience, "SentimentAnalysis.ipynb" could be used if running in Jupyter notebooks. 

Input: Text of company's Management Discussion and Analysis (MD&A) section from Form 10-Q and 10-K.
Output: Sentiment classified as either Positive or Negative along with the Sentiment confidence score in percentage

Code is written in Python and uses following libraries:

  * PANDAS
  * NLTK
  * SKLEARN
  * RANDOM
  * STATISTICS
  * PICKLE

  Following files are being used by the Main Program :
 
  * lemur-stopwords.txt:File containing STOP words. This shall be used to remove the unwanted words from the corpus. 
  * clasfuncdef.py:     Contains custom functions and classes defined by me.
  * Negative terms.csv: Training file of Negative terms denoting Negative Sentiment
  * Positive Terms.csv: Training file of Positive terms denoting Positive Sentiment
  * TestNegative.txt: Sample 10-K input file denoting Negative Sentiment. Used to test the program.
  * TestPositive.txt: Sample 10-K input file denoting Positive Sentiment. Used to test the program.


This report shall evaluate Sentiment accuracy using following classifiers and then use the classifier with highest accuracy percentage to evaluate the 10-K input.

  * Naive Bayes Classifier
  * MultinomialNB Classifier
  * BernoulliNB Classifier
  * Logistic Regression Classifier
  * SGD Classifier
  * LinerSVC Classifier


This sentiment analysis report shall use file "lemur-stopwords.txt" to ignore the most common words. It also uses Lemmatizer. It is similar to a stemmer however, the output shall be a proper word from english dictionary.

Concept of pickling has been used. Once the classifer's are trained to a desired accuracy, this program gives an option to save it under folder named "pickle". All subsequent execution of the report shall used the saved classifiers instead of evaluating them again. This shall help reduce the report execution time significantly.

Note: If we want to the report to re-evaluate without using the pickle concept, the files in the folder "pickle" needs to be deleted. Only if the file does not exist, system shall evaluate and save.


Output Explanation: Details of the output have been explained under the folder "Execution Summary". Initial execution of the report has been captured in the file "SentimentAnalysis_Initial_Evaluation.html". This doesn't use the files in the Pickle folder as this folder shall be empty. Initial executiion shall create the files in the pickle folder. 

On Second execution, this program shall use the files in pickle folder to evaluate. The output of this is in file "entimentAnalysis_2ndTime_Evaluation.html".



Executing report "SentimentAnalysis.py" / "SentimentAnalysis.ipynb":

This report shall prompt to "Enter file name to analyze the sentiment: ". Here, for testing purpose, I have used either TestNegative.txt / TestPositive.txt. We could enter any file name whose text needs to be anlysed for Sentiment. Report assumes that this file is in the same folder as the Master program.  On successful execution of the sentiment analysis, report shall prompt "Enter Yes to SAVE the trained data"  to save the classifier files under Pickle folder if selected as Yes. 

Sample output shall be :

Sentiment:  POSITIVE / NEGATIVE -> Denotes overall Sentiment of the input file
Sentiment Confidence:   %age    -> Denotes accuracy of the Sentiment analysis. 


References:
I have studied and used some of the concepts from the website : https://pythonprogramming.net
