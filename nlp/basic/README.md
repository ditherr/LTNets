## **BASIC NATURAL LANGUAGE PROCESSING - NLP**
### **1. Text Cleaning**
**Text Cleaning** → **Remove** the additional space, special characters, numbers (if needed), mentions (@), hashtag (h), link (https:/), and also replace the miss-spelling of words

### **2. Preprocessing**
- **Tokenizer**

    → **Convert corpus into tokens** (*sentences*), and then into words (based on 'space', 'dot', etc).

    🧑🏻‍🏫***Example***:
    ```
        Corpus: “I like to drink Strawberry Juice, but He likes to drink Mango Juice.*”
        Vocabulary: [i, like, to, drink, Strawberry, Juice, but, He, Mango]
    ```

- **Stemming**

    → **Reducing a word to its word stem** that affixes to the roots of words (lemma), or suffixes and prefixes. We can use several methods, such as: `PorterStemmer`, `RegexpStemmer`, `SnowballStemmer`, etc.

    **Major Disadvantage** for using *stemming* → some words may not get their actual or correct stem. But, it will solves with `Lemmatization`.

    🧑🏻‍🏫***Example***:
    ```
        Corpus:
        Vocabulary:
    ```

- **Lemmatization**

    → Lemma is a **root of word** rather than a root stem. So **it doesn’t change the meaning of the word.**

    In this case, will use `WordNetLemmatizer` from `nltk` → a thin wrapper around the wordnet corpus, that using `morphy()` as a function to find a *Lemma*. But, it will take more time than the Stemmer.

    🧑🏻‍🏫***Example***:
    ```
        Corpus:
        Vocabulary:
    ```

- **Stopwords**

    → focusing more with the importance words, and remove the rest. Removing the word based on list inside the dictionary in this case we use `stopwords` from `nltk`.

    🧑🏻‍🏫***Example***:
    ```
        List stopwords:
    ```

### **3. Word Embedding**
- **BOW (Bag Of Word)**

    → a simple document **embedding technique based on word frequency**. Conceptually, we think of the whole document as a “bag” of words, rather than a sequence. We represent the document simply by the frequency of each word.

    We will use `CountVectorizer()` from `scikit-learn` to get a list of BOW.

- **TF-IDF (*Term Frequency - Inverse Document Frequency*)**

    → It measures **how important a term is within a document relative to a collection of documents** (i.e., relative to a corpus).

    We will use `TfidfVectorizer()` from `scikit-learn` to get a list of BOW.

- **Word2Vec**

    → Similar with the other, it is one way to **convert the Word into the Vector**. But, in `Word2Vec` we will use a pre-train model.