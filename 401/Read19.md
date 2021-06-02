# Automation

## Python Regular Expression

- Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. 

If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use.

- They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc.

- You will start with importing `re` Python library that supports regular expressions
Then you will see how basic/ordinary characters are used for performing matches
Next, you'll learn about using repetitions in your regular expressions

you have to import this module with the help of import:

    `import re`


### Wild Card Characters: Special Characters
- Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression.

- For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

- But before you do, the examples below make use of two functions namely: search() and group().

**.** A period. Matches any single character except the newline character.

        ```
        re.search(r'Co.k.e', 'Cookie').group()
        ```
        `'Cookie'`

**^** A caret. Matches the start of the string.

        `re.search(r'^Eat', "Eat cake!").group()`
        `'Eat'`

**$** Matches the end of string.

        ```
        re.search(r'cake$', "Cake! Let's eat cake").group()
        ```
        `'cake'`

**\[abc\]** Matches a or b or c.
**\[a-zA-Z0-9\]** Matches any letter from (a to z) or (A to Z) or (0 to 9).

        ```
        re.search(r'[0-6]', 'Number: 5').group()
        ```
        `'5'`

**\\** Backslash.

- If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)
- Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).
- \ can be used in front of all the metacharacters to remove their special meaning (Scenario 3).

        ```
        re.search(r'Just a \regular character', 'Just a \regular character').group()
        ```
        `'Just a \regular character'`

**\w** Lowercase 'w'. Matches any single letter, digit, or underscore.
**\W** Uppercase 'W'. Matches any character not part of \w (lowercase w).

        ```
        print("Lowercase w:", re.search(r'Co\wk\we', 'Cookie').group())
        ```
    `Lowercase w: Cookie`

**\s** Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
**\S** Uppercase 'S'. Matches any character not part of \s (lowercase s).

        ```
        print("Lowercase s:", re.search(r'Eat\scake', 'Eat cake').group())
        ```
        `Lowercase s: Eat cake`

**\t** Lowercase t. Matches tab.
**\n** Lowercase n. Matches newline.
**\r** Lowercase r. Matches return.
**\A** Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
**\Z** Uppercase z. Matches only at the end of the string.

TIP: ^ and \A are effectively the same, and so are $ and \Z. Except when dealing with MULTILINE mode. Learn more about it in the flags section.

**\b** Lowercase b. Matches only the beginning or end of the word.

        ```
        print("\\t (TAB) example: ", re.search(r'Eat\tcake', 'Eat    cake').group())
        ```
        `\t (TAB) example:  Eat    cake`

### Repetitions

**\+** Checks if the preceding character appears one or more times starting from that position.

        ```
        re.search(r'Co+kie', 'Cooookie').group()
        ```
        `'Cooookie'`

**\*** Checks if the preceding character appears zero or more times starting from that position.

        ```
        re.search(r'Ca*o*kie', 'Cookie').group()
        ```
        `'Cookie'`

**?** Checks if the preceding character appears exactly zero or one time starting from that position.

        ```
        re.search(r'Colou?r', 'Color').group()
        ```
        `'Color'`

`{x}` Repeat exactly x number of times.
`{x,}` Repeat at least x times or more.
`{x, y}` Repeat at least x times but no more than y times.

### Basic Patterns: Ordinary Characters

You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions.

Ordinary characters can be used to perform simple exact matches:

        ```
        pattern = r"Cookie"
        sequence = "Cookie"
        if re.match(pattern, sequence):
            print("Match!")
        else: print("Not a match!")
        ```

        `Match!`

- Most alphabets and characters will match themselves, as you saw in the example.

- The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. The re module also contains several other functions, and you will learn some of them later on in the tutorial.
