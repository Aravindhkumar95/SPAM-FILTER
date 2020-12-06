# SPAM / HAM CLASSIFICATION
<h2>Objective</h2>
<p>This project is aimed to explore various techniques in NLP to classify a SMS as Spam or Not Spam. We will be using two Machine Learning Models Random Forest and Gradient Boosting to predict Spam Message.</p>

<h2>Dataset</h2>
<p>The data used for this project is <a href="https://www.kaggle.com/uciml/sms-spam-collection-dataset">Kaggle - SMS Spam Collection Dataset</a>. This dataset contains 5567 Messages in which 746 are spam and 4821 are ham.</p>

<h2>Understanding the Dataset</h2>
<p>Before getting into project, it is necessary to understand the dataset. Visualizing the dataset will help to understand various insights or stories hidden behind the dataset. It will help us to identify right approaches to predict the results.</p>

<h3><i>Calculating Length of Message</i></h3>
<p>First I calculated the length of message. I considered only the words in the message and not the blank spaces.</p> 

<h3><i>Calculating Percentage of Punctuation</i></h3>
<p>I also calculated percentage of punctuation in each message.</p> 

<p>For better understanding I used histogram to plot the <b>Length of Message</b> and <b>Percentage of Punctuation</b>. This will helps us to understand the distribution of both in overall dataset.</p>

<p style="text-align:center> <img src="https://user-images.githubusercontent.com/57459830/101291667-94921f80-37d8-11eb-8238-3457dfaeb47a.png" alt="Body Length Distribution"> <img src="https://user-images.githubusercontent.com/57459830/101291811-7f69c080-37d9-11eb-8c0b-744308b6fa0c.png" alt="Punctuation Percentage Distribution"> </p>


