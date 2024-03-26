import nltk

# Define PCFG productions
productions = [
    nltk.Production('S', ['NP', 'VP'], prob=0.9),
    nltk.Production('S', ['Aux', 'NP', 'VP'], prob=0.1),
    nltk.Production('NP', ['Det', 'N'], prob=0.6),
    nltk.Production('NP', ['NP', 'PP'], prob=0.4),
    nltk.Production('PP', ['P', 'NP'], prob=1.0),
    nltk.Production('VP', ['V', 'NP'], prob=0.7),
    nltk.Production('VP', ['VP', 'PP'], prob=0.3),
    nltk.Production('Det', ['the'], prob=0.4),
    nltk.Production('Det', ['a'], prob=0.6),
    nltk.Production('N', ['man'], prob=0.5),
    nltk.Production('N', ['park'], prob=0.5),
    nltk.Production('V', ['saw'], prob=0.5),
    nltk.Production('V', ['ate'], prob=0.5),
    nltk.Production('P', ['in'], prob=1.0),
    nltk.Production('Aux', ['did'], prob=1.0)
]

# Create PCFG grammar
pcfg_grammar = nltk.induce_pcfg(nltk.Nonterminal('S'), productions)

# Create PCFG parser
parser = nltk.ViterbiParser(pcfg_grammar)

# Example sentence
sentence = "the man saw a park in the city"

# Tokenize sentence
tokens = sentence.split()

# Parse the sentence
trees = parser.parse(tokens)

# Print the most probable parse tree
for tree in trees:
    print(tree)
