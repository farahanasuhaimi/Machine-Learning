# Regular Expressions (regex)

#### Date: 14 Feb 2021

## TOC

### What?

1. strings with special syntax
2. allow us to match patterns in other strings
3. offer referred as regex

### Some Applications:

1. Find all web links in a document
2. Parse email addresses
3. Remove unwanted strings and characters

### Common Patterns:

| pattern |     matches     |    example    |
| :-----: | :-------------: | :-----------: |
|   \w+   |      word       |    'magic'    |
|   \w    |     letter      | 'm', 'a', ... |
|   \d    |      digit      |       9       |
|   \s    |      space      |      ' '      |
|   .\*   |    wildcard     |               |
|   \S    |    not space    |  'no_spaces'  |
|  [a-z]  | lowercase group |   'abcdefg'   |

### Example of Python `re` module

- `re` module
- `split` split a string on regex
- `findall` find all patterns in a string
- `search` search for a pattern
- `match` match an entire string or substring based on a pattern
- rule: pattern first, and string second
