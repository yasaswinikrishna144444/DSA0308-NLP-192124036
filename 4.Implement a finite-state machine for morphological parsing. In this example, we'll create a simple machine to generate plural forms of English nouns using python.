class MorphologicalFSM:
    def generate_plural(self, noun):
        if noun.endswith('s'):
            return noun
        else:
            return noun + 's'

if __name__ == "_main_":
    fsm = MorphologicalFSM()

    # Test the FSM
    nouns = ['cat', 'dog', 'fox', 'house', 'box', 'bus']
    for noun in nouns:
        print(f"Plural of '{noun}': {fsm.generate_plural(noun)}")
