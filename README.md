# Document Similarity using POS Tags
## OBJECTIVE
Finding Similarity between documents using Jaccard Similarity and including Parts Of Speech(POS) Tags of the words in the model to better find the synchronous relationship between documents 

## Data
The data for the task at hand is webscraped from the three different articles:
1. Wikipedia page: We screaped the data from wikipedia page of UIC. So, as one can expect, the text in this document contains all the programs offered by the university, the history of the institution, college fees, alumni and also the clubs present at UIC.
2. NY Times Political Article: We scraped a news article from NY times which discusses a political event under the heading "The key moments from the first one-on-one Democratic debate between Hillary Clinton and Senator Bernie Sanders"
3. ESPN Article: We scraped a web-page from ESPN which contains a very specific artcile related to American Football.

## Analysis
We start with the data cleaning:

a) Removing the punctuations (not all of them, as we want to capture the correct POS tags)
![GitHub Logo](/images/text_cleaning.PNG)

b) Tokenize the words
![GitHub Logo](/images/tokenize.PNG)

c) Capturing the POS tags of the words using **tag library from NLTK**
![GitHub Logo](/images/postag.PNG)

d) Get the counts of the POS tags to use as the medium to capture the similarity between the documents
![GitHub Logo](/images/counting.PNG)

e) 
