class Parser:
    def __init__(self, grammar):
        self.grammar = grammar

    def parse(self, input_string):
        self.input_string = input_string
        self.index = 0
        self.valid = True
        self.parse_non_terminal('S')

        print("Parsing successful" if self.index == len(self.input_string) and self.valid else "Parsing failed")

    def parse_non_terminal(self, non_terminal):
        if non_terminal in self.grammar:
            for production in self.grammar[non_terminal]:
                for symbol in production:
                    if self.valid:
                        if symbol in self.grammar:
                            self.parse_non_terminal(symbol)
                        elif self.input_string[self.index] == symbol:
                            self.index += 1
                        else:
                            self.valid = False

# Example grammar
grammar = {
    'S': [['A', 'B'], ['B', 'C']],
    'A': [['a']],
    'B': [['b']],
    'C': [['c']]
}

# Example input string
input_string = "abc"

# Create a parser object and parse the input string
parser = Parser(grammar)
parser.parse(input_string)
