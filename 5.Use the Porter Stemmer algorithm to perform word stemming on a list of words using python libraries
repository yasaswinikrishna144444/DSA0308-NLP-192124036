import nltk
from nltk.stem import PorterStemmer

# Initialize the Porter Stemmer
porter_stemmer = PorterStemmer()

# List of words to be stemmed
words = ["running", "easily", "friendship", "swimming", "flies", "agreed"]

# Perform stemming on each word in the list
stemmed_words = [porter_stemmer.stem(word) for word in words]

# Print the original words and their stemmed forms
for original, stemmed in zip(words, stemmed_words):
    print(f"Original: {original} --> Stemmed: {stemmed}")
