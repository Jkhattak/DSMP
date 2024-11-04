# Strings in Python

## What is a String?

- A string is a `sequence of characters` enclosed within single quotes ('), double quotes ("), or triple quotes (''' or """). 
- Strings are `immutable`, meaning that once you create a string, you cannot modify its content.

```
single_quote_string = 'Hello'
double_quote_string = "World"
triple_quote_string = """This is a 
multi-line string"""
```

## Accessing Characters in a String

#### Indexing

```
word = "Python"
print(word[0])  # Output: P
print(word[-1]) # Output: n (negative index)
```

#### String Slicing 

```
word = "Python"
print(word[0:2])  # Output: Py
print(word[2:])   # Output: thon
print(word[:3])   # Output: Pyt
```


## Common String Methods

- `str.lower():` Converts the string to lowercase.

`print("HELLO".lower())  # Output: hello`


- `str.upper():` Converts the string to uppercase.

`print("hello".upper())  # Output: HELLO
`

- `str.strip():` Removes whitespace from both ends.
  
`print("  hello  ".strip())  # Output: hello`

- `str.replace(old, new):` Replaces occurrences of old with new.

`print("hello world".replace("world", "Python"))  # Output: hello Python`

- `str.split(separator):` Splits the string into a list based on the separator.

`print("apple,banana,orange".split(","))  # Output: ['apple', 'banana', 'orange']`

- `str.join(iterable):` Joins elements of an iterable into a string.

`print("-".join(["2024", "11", "01"]))  # Output: 2024-11-01`

- str.find(substring): Returns the index of the first occurrence of substring, or -1 if not found.

`print("hello".find("e"))  # Output: 1`

### Other Useful Methods

- `str.startswith(prefix):` Checks if the string starts with prefix.
- `str.endswith(suffix):` Checks if the string ends with suffix.
- `str.isdigit():` Checks if the string consists of only digits.
- `str.isalpha():` Checks if the string consists of only alphabetic characters.

## String Formatting

#### Old-Style Formatting (%)

```
name = "John"
age = 25
print("My name is %s and I am %d years old." % (name, age))
```

#### str.format() Method

```
print("My name is {} and I am {} years old.".format(name, age))
print("My name is {0} and I am {1} years old.".format(name, age))
```

#### f-Strings (Python 3.6+)

```
print(f"My name is {name} and I am {age} years old.")
```

## Escape Characters

Use a backslash (\) to escape special characters.

```
print("He said, \"Hello, World!\"")
print("Line1\nLine2")  # Newline
print("Tab\tSpace")    # Tab
```

## Raw Strings

Use `r or R` to create raw strings, which ignore escape sequences.

```
path = r"C:\Users\name\Documents"
print(path)  # Output: C:\Users\name\Documents
```

## String Operations

#### Concatenation

```
greeting = "Hello" + " " + "World"
print(greeting)  # Output: Hello World
```

#### Repetition

```
repeat = "Ha" * 3
print(repeat)  # Output: HaHaHa
```

## Checking Substrings

#### `in` and `not` in

```
text = "The quick brown fox"
print("quick" in text)      # Output: True
print("slow" not in text)   # Output: True
```
## Iterating Over Strings

```
for char in "Python":
    print(char)
```

## String Immutability

Strings are immutable in Python. You cannot change a character in a string directly.

```
word = "hello"
# word[0] = "H"  # This will raise an error
word = "Hello"   # Instead, create a new string
```

## Advanced String Manipulation

#### Using `re` Module for Regular Expressions

The `re` module is used for advanced string searching and manipulation.

```
import re
pattern = r"\d+"
text = "There are 42 apples"
matches = re.findall(pattern, text)
print(matches)  # Output: ['42']
```

## Common Use Cases

#### Palindrome Check

```
def is_palindrome(s):
    return s == s[::-1]

print(is_palindrome("racecar"))  # Output: True
```

#### Character Frequency

```
from collections import Counter
text = "hello"
print(Counter(text))  # Output: Counter({'l': 2, 'h': 1, 'e': 1, 'o': 1})
```

## String Encoding and Decoding

```
text = "Hello, World!"
encoded = text.encode("utf-8")
print(encoded)  # Output: b'Hello, World!'

decoded = encoded.decode("utf-8")
print(decoded)  # Output: Hello, World!
```