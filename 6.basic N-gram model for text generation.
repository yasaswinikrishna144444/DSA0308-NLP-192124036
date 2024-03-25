import random
from collections import defaultdict

def train_bigram_model(text):
    bigram_model = defaultdict(list)
    words = text.split()
    for i in range(len(words) - 1):
        bigram_model[words[i]].append(words[i + 1])
    return bigram_model

def generate_text(bigram_model, length=10):
    word = random.choice(list(bigram_model.keys()))
    text = [word]
    for _ in range(length - 1):
        if word in bigram_model and bigram_model[word]:  # Check if word has successors
            next_word = random.choice(bigram_model[word])
            text.append(next_word)
            word = next_word
        else:
            break  # Break if the word has no successors
    return ' '.join(text)

text = "This is a sample text for testing the bigram model."
bigram_model = train_bigram_model(text)
generated_text = generate_text(bigram_model)
print(generated_text)
