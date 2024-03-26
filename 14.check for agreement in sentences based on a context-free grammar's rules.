def check_agreement(grammar, sentence):
    errors = [word.split('/')[0] for word in sentence.split() if word.split('/')[1] not in grammar.get(word.split('/')[1], [])]
    print("Agreement errors found:" if errors else "Agreement is correct.")
    for error in errors:
        print(f"- {error}")

# Example grammar with agreement rules
grammar = {
    'Noun': ['s', 'es'],  # Example: cat/cats, dog/dogs
    'Verb': ['s', 'es', 'ed'],  # Example: eat/eats, chase/chases, chased
    'Adjective': ['er', 'est']  # Example: fast/faster, fast/fastest
}

# Example sentence
sentence = "The cat eats fishes quickly."

# Check agreement in the sentence
check_agreement(grammar, sentence)
