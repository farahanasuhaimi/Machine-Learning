# Tokenization

#### Date: 14 Feb 2021

## TOC

### What?

1. change string or document to smaller chunks
2. these chunks are the tokens
3. a preparation step for NLP
4. can be set with own rules to get tokens using regular expression

### Some Rule Examples:

1. breaking out words or sentences
2. separating punctuation
3. tokenize part of the string

### Why?

- can help with simple preprocessing tasks
- map part of speech
- matching common words
- remove unwanted tokens

### Example of Python `nltk` module

- `sent_tokenize`: tokenize a document into sentences
- `regexp_tokenize`: tokenize a string or document based on a regular expression patterns
- `TweetTokenizer`: special class just for tweet tokenization

### Advanced Tokenization with `NLTK` + `regex`

#### 1. Regex `or` grouping using `|`

- define a group using `()`
- define explicit ranges using `[]`
- examples:
  ```python
  import re
  match_digits_and_words = ('(\d+|\w+)')
  re.findall(match_digits_and_words, 'He has 11 cats.') #['He', 'has', '11', 'cats']
  ```
- regex ranges and groups

  |    pattern    |                    matches                    |     example      |
  | :-----------: | :-------------------------------------------: | :--------------: |
  |   [A-Za-z]+   |     upper and lowercase English alphabet      |  'ABCDEFghijk'   |
  | [A-Za-z\-\.]+ | upper and lowercase English alphabet, - and . | 'My-website.com' |
  |     [0-9]     |              numbers from 0 to 9              |        9         |
  |     (a-z)     |                  a, - and z                   |      'a-z'       |
  |   (\s+\|,)    |               spaces or a comma               |       ', '       |
