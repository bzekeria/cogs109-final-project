# Methods

**This will explain the feature engineering aspect so we can all have a better understand on how the project will be approached.**

There are great links online that'll go in more detail. Data cleaning will also be intergral to have a high accuracy so we'll have to take into account of the various ways we can clean ```name``` column.

Our main method lies in **Term Frequency-Inverse Document Frequency (TF-IDF)** which outputs a numerical representaion of the text data.
- First **tokenize** (```nltk.word_tokenize```) the text in the ```name``` column into individual words
- Then **lemmatize** (```nltk.WordNetLemmatizer()```) the words to obtain the root of the word 
    - Example: ```running```, ```ran```, ```runs``` = ```run```
- **TF-IDF (```sklearn.feature_extraction.text.TfidfVectorizer```):** outputs a numerical representation of text data 
    - **Term Frequency**: a measure of how frequently a term appears in a document (each product listing]
        - $$\text{TF}(t, d) = \frac{\text{Number of occurrences of term } t \text{ in document } d}{\text{Total number of terms in document } d}$$
    - **Inverse Document Frequency (IDF)**: measures the importance of a term across the entire corpus by considering how many documents contain that term (all product listings)
        - $$\text{IDF}(t, D) = \log \frac{\text{Total number of documents in the corpus } D}{\text{Number of documents containing term } t}$$
    - **TF-IDF**: provide a weight for each term in each document
        - $$\text{TF-IDF}(t, d, D) = \text{TF}(t, d) \times \text{IDF}(t, D)$$
        - Gives higher weights to terms that are frequent in a specific document but rare across the entire corpus
 - Construct a vocabulary 
    - ```electronics_vocabulary = ['accessories', 'audio', 'camera', ...]```
    - We use the methods above + iterate the different categories to create its respective vocabulary
    - Capture the distinct language patterns and keywords associated with different types of products
    - Transforms it into a numerical representation
 - Apply an ML algorithm to train/test our data 
        
Another most common NLP technique is the **Bag-of-Words (BOW)** model which counts the occurences of words in a document (great for sentiment analysis). Though in order to have a more robust analysis for our project, TF-IDF, takes into account context and importance of words across the corpus which is what we want to have a high accuracy in predicting the category for a given product.
