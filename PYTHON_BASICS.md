## Python Basics
This cheatsheet base on https://www.w3schools.com/python/default.asp

1.  print function
    `print(some_variable)`
    
2.  comments:
    
    1.  multi line
        
        ```Python
        """
        This is mulit line
        comment in
        python
        """
        ```
    2.  single line
        
        ```Python
        #This is a comment.
        print("Hello, World!")
        ```
3.  Variables, [https://www.w3schools.com/python/python\_variables\_names.asp](https://www.w3schools.com/python/python_variables_names.asp)
    
    1.  Are case sensitive
        
    2.  cannot start form special character or number
        
        ```
        >>> 3a = 5
        >>> File "<stdin>", line 1
        >>> 3a = 5
        >>> ^
        >>> SyntaxError: invalid syntax</stdin>
        ```
    3.  `type()`
        
    4.  Assigning multiple values
        
        ```Python
        x, y, z = "Orange", "Banana", "Cherry"
        x = y = z = "Orange"
        
        # Unpacking variables
        
        fruits = ["apple", "banana", "cherry"]
        x, y, z = fruits
        
        print(x)
        print(y)
        print(z)
        ```
4.  Data types: https://www.w3schools.com/python/python_datatypes.asp
    
    1.  text: `str`
        
    2.  Numeric Types: `int, float, complex`
        
    3.  Sequence Types: `list, tuple`
        
    4.  Mapping Type: `dict`
        
    5.  Set Types: `set, frozenset`
        
    6.  Boolean: `bool`
        
    7.  Binary Types: `bytes, bytearray, memoryview`
        
        ```Python
        x = "Hello World" #str
        x = 20 #int
        x = 20.5 #float
        x = 1j #complex
        x = ["apple", "banana", "cherry"] #list
        x = ("apple", "banana", "cherry") #tuple
        x = range(6) #range
        x = {"name" : "John", "age" : 36} #dict
        x = {"apple", "banana", "cherry"} #set
        x = frozenset({"apple", "banana", "cherry"}) #frozenset
        x = True #bool
        x = b"Hello" #bytes
        x = bytearray(5) #bytearray
        x = memoryview(bytes(5)) #memoryview
        ```
5.  Numbers
    
    1.  Conversion: `int(), float()`
        
    2.  Random numbers:
        
        ```Python
        import random
        
        print(random.randint(10))
        ```
6.  Type conversion:
    
    ```Python
    x = int(1)   # x will be 1
    y = int(2.8) # y will be 2
    z = int("3") # z will be 3
    
    x = float(1)     # x will be 1.0
    y = float(2.8)   # y will be 2.8
    z = float("3")   # z will be 3.0
    w = float("4.2") # w will be 4.2
    
    x = str("s1") # x will be 's1'
    y = str(2)    # y will be '2'
    z = str(3.0)  # z will be '3.0'
    ```
7.  Strings: https://www.w3schools.com/python/python_strings.asp
    
    1.  Assigning string to variable
        
        ```Python
        a = "Hello"
        print(a)
        
        a = """Lorem ipsum dolor sit amet,
        consectetur adipiscing elit,
        sed do eiusmod tempor incididunt
        ut labore et dolore magna aliqua."""
        print(a)
        
        ```
    2.  Strings are array
        
        ```Python
        a = "Hello, World!"
        print(a[1])
        ```
    3.  String length. `len()`
        
        ```Python
        a = "Hello, World!"
        print(len(a))
        ```
    4.  check string
        
        ```Python
        txt = "The best things in life are free!"
        print("free" in txt)
        
        txt = "The best things in life are free!"
        print("expensive" not in txt)
        ```
    5.  Slicing strings
        
        ```Python
        b = "Hello, World!"
        print(b[2:5])
        
        b = "Hello, World!"
        print(b[:5])
        
        b = "Hello, World!"
        print(b[2:])
        
        b = "Hello, World!"
        print(b[-5:-2])
        ```
    6.  Modify Strings
        
        ```Python
        a = "Hello, World!"
        print(a.upper())
        
        a = "Hello, World!"
        print(a.lower())
        
        a = " Hello, World! "
        print(a.strip()) # returns "Hello, World!" 
        
        a = "Hello, World!"
        print(a.replace("H", "J"))
        
        a = "Hello, World!"
        print(a.split(",")) # returns ['Hello', ' World!']
        ```
    7.  Concatenate strings
        
        ```Python
        a = "Hello"
        b = "World"
        c = a + b
        print(c)
        
        a = "Hello"
        b = "World"
        c = a + " " + b
        print(c)
        ```
    8.  Format strings
        
        ```Python
        age = 36
        txt = "My name is John, and I am {}"
        print(txt.format(age))
        
        # f strings (since python3.8)
        age = 36
        txt = f"My name is John, and I am {age}"
        print(txt)
        ```
    9.  Escape characters
        
        ```Python
        txt = "We are the so-called \"Vikings\" from the north."
        ```
        
        |     |     |
        | --- | --- |
        | \\" | Double Quote |
        | \\\ | Backslash |
        | \\n | New Line |
        | \\r | Carriage Return |
        | \\t | Tab |
        | \\b | Backspace |
        | \\f | From feed |
        | \\ooo | Octal value |
        | \\xhh | Hex value |
        
    10. String Methods
        
        |     |     |
        | --- | --- |
        | [capitalize()](https://www.w3schools.com/python/ref_string_capitalize.asp) | Converts the first character to upper case |
        | [casefold()](https://www.w3schools.com/python/ref_string_casefold.asp) | Converts string into lower case |
        | [center()](https://www.w3schools.com/python/ref_string_center.asp) | Returns a centered string |
        | [count()](https://www.w3schools.com/python/ref_string_count.asp) | Returns the number of times a specified value occurs in a string |
        | [encode()](https://www.w3schools.com/python/ref_string_encode.asp) | Returns an encoded version of the string |
        | [endswith()](https://www.w3schools.com/python/ref_string_endswith.asp) | Returns true if the string ends with the specified value |
        | [expandtabs()](https://www.w3schools.com/python/ref_string_expandtabs.asp) | Sets the tab size of the string |
        | [find()](https://www.w3schools.com/python/ref_string_find.asp) | Searches the string for a specified value and returns the position of where it was found |
        | [format()](https://www.w3schools.com/python/ref_string_format.asp) | Formats specified values in a string |
        | format_map() | Formats specified values in a string |
        | [index()](https://www.w3schools.com/python/ref_string_index.asp) | Searches the string for a specified value and returns the position of where it was found |
        | [isalnum()](https://www.w3schools.com/python/ref_string_isalnum.asp) | Returns True if all characters in the string are alphanumeric |
        | [isalpha()](https://www.w3schools.com/python/ref_string_isalpha.asp) | Returns True if all characters in the string are in the alphabet |
        | [isdecimal()](https://www.w3schools.com/python/ref_string_isdecimal.asp) | Returns True if all characters in the string are decimals |
        | [isdigit()](https://www.w3schools.com/python/ref_string_isdigit.asp) | Returns True if all characters in the string are digits |
        | [isidentifier()](https://www.w3schools.com/python/ref_string_isidentifier.asp) | Returns True if the string is an identifier |
        | [islower()](https://www.w3schools.com/python/ref_string_islower.asp) | Returns True if all characters in the string are lower case |
        | [isnumeric()](https://www.w3schools.com/python/ref_string_isnumeric.asp) | Returns True if all characters in the string are numeric |
        | [isprintable()](https://www.w3schools.com/python/ref_string_isprintable.asp) | Returns True if all characters in the string are printable |
        | [isspace()](https://www.w3schools.com/python/ref_string_isspace.asp) | Returns True if all characters in the string are whitespaces |
        | [istitle()](https://www.w3schools.com/python/ref_string_istitle.asp) | Returns True if the string follows the rules of a title |
        | [isupper()](https://www.w3schools.com/python/ref_string_isupper.asp) | Returns True if all characters in the string are upper case |
        | [join()](https://www.w3schools.com/python/ref_string_join.asp) | Joins the elements of an iterable to the end of the string |
        | [ljust()](https://www.w3schools.com/python/ref_string_ljust.asp) | Returns a left justified version of the string |
        | [lower()](https://www.w3schools.com/python/ref_string_lower.asp) | Converts a string into lower case |
        | [lstrip()](https://www.w3schools.com/python/ref_string_lstrip.asp) | Returns a left trim version of the string |
        | [maketrans()](https://www.w3schools.com/python/ref_string_maketrans.asp) | Returns a translation table to be used in translations |
        | [partition()](https://www.w3schools.com/python/ref_string_partition.asp) | Returns a tuple where the string is parted into three parts |
        | [replace()](https://www.w3schools.com/python/ref_string_replace.asp) | Returns a string where a specified value is replaced with a specified value |
        | [rfind()](https://www.w3schools.com/python/ref_string_rfind.asp) | Searches the string for a specified value and returns the last position of where it was found |
        | [rindex()](https://www.w3schools.com/python/ref_string_rindex.asp) | Searches the string for a specified value and returns the last position of where it was found |
        | [rjust()](https://www.w3schools.com/python/ref_string_rjust.asp) | Returns a right justified version of the string |
        | [rpartition()](https://www.w3schools.com/python/ref_string_rpartition.asp) | Returns a tuple where the string is parted into three parts |
        | [rsplit()](https://www.w3schools.com/python/ref_string_rsplit.asp) | Splits the string at the specified separator, and returns a list |
        | [rstrip()](https://www.w3schools.com/python/ref_string_rstrip.asp) | Returns a right trim version of the string |
        | [split()](https://www.w3schools.com/python/ref_string_split.asp) | Splits the string at the specified separator, and returns a list |
        | [splitlines()](https://www.w3schools.com/python/ref_string_splitlines.asp) | Splits the string at line breaks and returns a list |
        | [startswith()](https://www.w3schools.com/python/ref_string_startswith.asp) | Returns true if the string starts with the specified value |
        | [strip()](https://www.w3schools.com/python/ref_string_strip.asp) | Returns a trimmed version of the string |
        | [swapcase()](https://www.w3schools.com/python/ref_string_swapcase.asp) | Swaps cases, lower case becomes upper case and vice versa |
        | [title()](https://www.w3schools.com/python/ref_string_title.asp) | Converts the first character of each word to upper case |
        | [translate()](https://www.w3schools.com/python/ref_string_translate.asp) | Returns a translated string |
        | [upper()](https://www.w3schools.com/python/ref_string_upper.asp) | Converts a string into upper case |
        | [zfill()](https://www.w3schools.com/python/ref_string_zfill.asp) | Fills the string with a specified number of 0 values at the beginning |
        

### 8\. Booleans

### 9\. Operators

### 10\. Lists

### 11\. Tuples

### 12\. Sets

### 13\. Dictionaries

### 14\. If Else

### 15\. For loops

### 16\. While Loops

### 17\. Functions

Other for future:

1.  Syntax (with if statement)
    1.  indentation
2.  global variables
