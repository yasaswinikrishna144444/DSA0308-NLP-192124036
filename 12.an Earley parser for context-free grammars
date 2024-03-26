def earley_parse(grammar, input_string):
    chart = [[] for _ in range(len(input_string) + 1)]
    chart[0] = [('', 0, 'S', '')]
    for i in range(len(input_string) + 1):
        for state in chart[i]:
            _, j, lhs, rhs = state
            if j < len(grammar.get(lhs, [])):
                chart[i].extend([(lhs, 0, symbol, lhs + symbol) for symbol in grammar.get(lhs, [])[j]])
            elif j == len(grammar.get(lhs, [])):
                for prev_state in chart[i - len(rhs)]:
                    _, _, prev_lhs, _ = prev_state
                    if prev_lhs and grammar.get(prev_lhs, []) and lhs == grammar[prev_lhs][-1]:
                        chart[i].append((prev_lhs, prev_state[1] + 1, lhs, prev_state[3] + lhs))

    return any(state == ('', len(lhs), 'S', lhs) for state in chart[len(input_string)])


# Example grammar
grammar = {
    'S': [['A', 'B'], ['B', 'C']],
    'A': [['a']],
    'B': [['b']],
    'C': [['c']]
}

# Example input string
input_string = "abc"

# Parse input string using Earley parser
result = earley_parse(grammar, input_string)

# Output result
print("Parsing successful" if result else "Parsing failed")
