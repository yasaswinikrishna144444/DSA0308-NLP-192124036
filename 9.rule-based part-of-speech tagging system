import re

def rule_based_pos_tagging(text):
    pos_tags = []
    for word in text.split():
        # Apply regular expression rules to assign POS tags
        if re.match(r'\b[A-Z][a-z]*\b', word):
            pos_tags.append((word, 'NNP'))  # Proper noun
        elif re.match(r'\b[a-z]+ly\b', word):
            pos_tags.append((word, 'RB'))   # Adverb ending in -ly
        else:
            pos_tags.append((word, 'NN'))   # Default to noun
    return pos_tags

text = "This is a rule-based part-of-speech tagging system using regular expressions."
pos_tags = rule_based_pos_tagging(text)
print(pos_tags)
