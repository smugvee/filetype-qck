# qcktypes
*Python implementation of [Dyne's file extension list](https://github.com/dyne/file-extension-list)*
## What does that even mean
There I was, trying to get files out of a directory and categorize them based on their file extension. "This is probably already a module" I said. I was right, there it was glorious [filetype](https://pypi.org/project/filetype/).

"Wait... what is a mime bruh 😭"

## I don't want to validate files actually, just tell me what they are
The module [filetype](https://pypi.org/project/filetype/) validates files with their [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)) or whatever, but I didn't want that. I found [Dyne's file extension list](https://github.com/dyne/file-extension-list) and quickly wrote up this module since I couldn't find anything similar. I would write more features but I know literally nobody will ever use this so it's probably fine. 

Rather than validating files with their magic numbers this module simply checks the extension of an input file and compares it with a dictionary of types and returns its category.

## Quick example
```python
import qcktypes

file =  'example.txt'
category = qcktypes.find_type(file)

print(f'{file} is in category: {category}!')
```
**output :**
```
$ python3 example.py
example.txt is in category: text!
```

