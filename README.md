# Document Similarity using POS Tags
## OBJECTIVE
Finding Similarity between documents using Jaccard Similarity and including Parts Of Speech(POS) Tags of the words in the model to better find the synchronous relationship between documents 

## TECHNOLOGIES
Project is created with:

* Python - **NLTK, Collections, sklearn, numpy, pandas, matplotlib.pyplot, glove**

## DATA
The data for the task at hand is webscraped from the three different articles which can be found [here](https://github.com/VipanchiKatthula/DocumentSimilarity_With_POSTags/tree/master/Data):
1. **Wikipedia page**: We screaped the data from wikipedia page of UIC. So, as one can expect, the text in this document contains all the programs offered by the university, the history of the institution, college fees, alumni and also the clubs present at UIC.
2. **NY Times Political Article**: We scraped a news article from NY times which discusses a political event under the heading "The key moments from the first one-on-one Democratic debate between Hillary Clinton and Senator Bernie Sanders"
3. **ESPN Article**: We scraped a web-page from ESPN which contains a very specific artcile related to American Football.

## ANALYSIS

a) We start with the data cleaning: Removing the punctuations (not all of them, as we want to capture the correct POS tags)
![GitHub Logo](/images/text_cleaning.PNG)

b) Tokenize the words
![GitHub Logo](/images/tokenize.PNG)

c) Capturing the POS tags of the words using **tag library from NLTK**
![GitHub Logo](/images/postag.PNG)

d) Get the counts of the POS tags to use as the medium to capture the similarity between the documents
![GitHub Logo](/images/counting.PNG)

e) Using **Jaccard Similarity** on the count of POS tags to find the similarity between the webscraped documents.
![GitHub Logo](/images/jaccardsimilarity.PNG)

## WORD EMBEDDING
I used Glove library to get create a corpus object and then we train the corpus to generate the co occurence matrix which is used in GloVe. We create a Glove object which will use the matrix created in the above lines to create embeddings. We can set the learning rate as it uses Gradient Descent and number of components. We set the number of components to 10 which means we generate a 10 columned vector foe every word in the input data article. We use the default learning rate which is 0.05. The output of the embedded vectors on a 2D plane show the following figure:
![GitHub Logo](/images/embedding.PNG)

## RESULTS and CONCLUSION
We see higher similarity between UIC and rest of the data files as UIC's wikipedia page has political information and also sports information from their football teams. However, the imilarity between NY Times and ESPN  articles is only 0.673 which shows that they do not have higher similarity.
