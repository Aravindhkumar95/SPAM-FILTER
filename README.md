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

<img src="https://user-images.githubusercontent.com/57459830/101291667-94921f80-37d8-11eb-8238-3457dfaeb47a.png" alt="Body Length Distribution"> <img src="https://user-images.githubusercontent.com/57459830/101291811-7f69c080-37d9-11eb-8c0b-744308b6fa0c.png" alt="Punctuation Percentage Distribution"> 

<h3>Analyzing the New Feature</h3>
<p>I used histogram to plot the distribution of Length of Message and Percentage of Punctuation separately for Spam and Ham. From the below graph we can understand, Spam Messages have more text and more punctuation.</p>

<img src="https://user-images.githubusercontent.com/57459830/101295532-25bec180-37ec-11eb-9bac-2834586c1ebd.png" alt="Body Length Distribution - Spam Vs Ham "> <img src="https://user-images.githubusercontent.com/57459830/101295558-5f8fc800-37ec-11eb-88bc-ef243aab60cf.png" alt="Punctuation Percentage Distribution - Spam Vs Ham ">

<h2>Cleaning Text</h2>
<p>In order to predict the messages as spam or ham, It is necessary to convert the messages to Machine understanding form. The process involved in cleaning procoess are:</p>
<ol>
  <li>Removing Punctuation</li>
  <li>Tokenization</li>
  <li>Lemmatizing or Stemming</li>
  <li>Removing Stopwords</li>
</ol>
<p>
<i>Removing Punctuation:</i>In this approach, I am removing punctuation from the messages. In case if you wish, you can vectorize each punctuation to increase the number of variables for supporting the algorithm.
  
<i>Tokenization:</i>It is the process of splitting some string or sentence into a list of words. Along the with single or multiple white spaces we also need to consider the special characters that separate the words. 

<i>Stemming:</i>It is the process of reducing inflected words to their word stem or root. It blindly remove the end of the word to leave only the base. 
<ul>
  <li>Stemming/Stemmed  -->  Stem</li>
  <li>Electricity/Electrical  -->  Electr</li>
  <li>Berries/Berry  -->  Berri</li>
  <li>Connection/Connected/Connective  -->  Connect</li>
</ul>
<i>Lemmatizing:</i>It is the process of vocabulary analysis of words inorder to remove inflectional root words to leave only the dictionary form of a word.</p>

<table>
  <tr>
    <th>Words</th>
    <th>Stemming</th>
    <th>Lemmatizing</th>
  </tr>
  <tr>
    <td>Meanness/Meaning</td>
    <td>Mean</td>
    <td>Meanness/Meaning</td>
  </tr>
  <tr>
    <td>Goose/Geese</td>
    <td>Goos/Gees</td>
    <td>Goose/Goose</td>
  </tr>
</table>
<p>I used Stemming in this filtering process, because it is fast when compared to the Lemmaztizing</p>


<i>Removing Stopwords:</i> Words like <i>the, but, if, that</i> don't contribute much to the meaning of a sentence. So, the last step of cleaning the data involves removing those stopwords

'''python
  import nltk
  stopwords = nltk.corpus.stopwords.words('english')
'''



