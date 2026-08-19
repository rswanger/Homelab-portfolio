str

Strings in python are surrounded by either single quotation marks, or double quotation marks.

'hello' is the same as "hello".

You can display a string literal with the `[print()](https://www.w3schools.com/python/ref_func_print.asp)` function:

### Example

print("Hello")  
print('Hello')

---

## Quotes Inside Quotes

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

### Example

print("It's alright")  
print("He is called 'Johnny'")  
print('He is called "Johnny"')

---

## Assign String to a Variable

Assigning a string to a variable is done with the variable name followed by an equal sign and the string:

### Example

a = "Hello"  
print(a)

---

## Multiline Strings

You can assign a multiline string to a variable by using three quotes:

### Example

You can use three double quotes:

a = """Lorem ipsum dolor sit amet,  
consectetur adipiscing elit,  
sed do eiusmod tempor incididunt  
ut labore et dolore magna aliqua."""  
print(a)

Or three single quotes:

### Example

a = '''Lorem ipsum dolor sit amet,  
consectetur adipiscing elit,  
sed do eiusmod tempor incididunt  
ut labore et dolore magna aliqua.'''  
print(a)

**Note:** in the result, the line breaks are inserted at the same position as in the code.

---

## Strings are Arrays

Like many other popular programming languages, strings in Python are arrays of unicode characters.

However, Python does not have a character data type, a single character is simply a string with a length of 1.

Square brackets can be used to access elements of the string.

### Example

Get the character at position 1 (remember that the first character has the position 0):

a = "Hello, World!"  
print(a[1])

---

## Looping Through a String

Since strings are arrays, we can loop through the characters in a string, with a `[for](https://www.w3schools.com/python/ref_keyword_for.asp)` loop.

### Example

Loop through the letters in the word "banana":

for x in "banana":  
  print(x)

Learn more about For Loops in our [Python For Loops](https://www.w3schools.com/python/python_for_loops.asp) chapter.

---

## String Length

To get the length of a string, use the `[len()](https://www.w3schools.com/python/ref_func_len.asp)` function.

### Example

The `[len()](https://www.w3schools.com/python/ref_func_len.asp)` function returns the length of a string:

a = "Hello, World!"  
print(len(a))

---

## Check String

To check if a certain phrase or character is present in a string, we can use the keyword `[in](https://www.w3schools.com/python/ref_keyword_in.asp)`.

### Example

Check if "free" is present in the following text:

txt = "The best things in life are free!"  
print("free" in txt)  

Use it in an `[if](https://www.w3schools.com/python/ref_keyword_if.asp)` statement:

### Example

Print only if "free" is present:

txt = "The best things in life are free!"  
if "free" in txt:  
  print("Yes, 'free' is present.")

Learn more about If statements in our [Python If...Else](https://www.w3schools.com/python/python_conditions.asp) chapter.

---

## Check if NOT

To check if a certain phrase or character is NOT present in a string, we can use the keyword `[not in](https://www.w3schools.com/python/ref_keyword_not.asp)`.

### Example

Check if "expensive" is NOT present in the following text:

txt = "The best things in life are free!"  
print("expensive" not in txt)

Use it in an `[if](https://www.w3schools.com/python/ref_keyword_if.asp)` statement:

### Example

print only if "expensive" is NOT present:

txt = "The best things in life are free!"  
if "expensive" not in txt:  
  print("No, 'expensive' is NOT present.")
  
  |Method|Description|
|---|---|
|[capitalize()](https://www.w3schools.com/python/ref_string_capitalize.asp)|Converts the first character to upper case|
|[casefold()](https://www.w3schools.com/python/ref_string_casefold.asp)|Converts string into lower case|
|[center()](https://www.w3schools.com/python/ref_string_center.asp)|Returns a centered string|
|[count()](https://www.w3schools.com/python/ref_string_count.asp)|Returns the number of times a specified value occurs in a string|
|[encode()](https://www.w3schools.com/python/ref_string_encode.asp)|Returns an encoded version of the string|
|[endswith()](https://www.w3schools.com/python/ref_string_endswith.asp)|Returns true if the string ends with the specified value|
|[expandtabs()](https://www.w3schools.com/python/ref_string_expandtabs.asp)|Sets the tab size of the string|
|[find()](https://www.w3schools.com/python/ref_string_find.asp)|Searches the string for a specified value and returns the position of where it was found|
|[format()](https://www.w3schools.com/python/ref_string_format.asp)|Formats specified values in a string|
|[format_map()](https://www.w3schools.com/python/ref_string_format_map.asp)|Formats specified values from a dictionary in a string|
|[index()](https://www.w3schools.com/python/ref_string_index.asp)|Searches the string for a specified value and returns the position of where it was found|
|[isalnum()](https://www.w3schools.com/python/ref_string_isalnum.asp)|Returns True if all characters in the string are alphanumeric|
|[isalpha()](https://www.w3schools.com/python/ref_string_isalpha.asp)|Returns True if all characters in the string are in the alphabet|
|[isascii()](https://www.w3schools.com/python/ref_string_isascii.asp)|Returns True if all characters in the string are ascii characters|
|[isdecimal()](https://www.w3schools.com/python/ref_string_isdecimal.asp)|Returns True if all characters in the string are decimals|
|[isdigit()](https://www.w3schools.com/python/ref_string_isdigit.asp)|Returns True if all characters in the string are digits|
|[isidentifier()](https://www.w3schools.com/python/ref_string_isidentifier.asp)|Returns True if the string is an identifier|
|[islower()](https://www.w3schools.com/python/ref_string_islower.asp)|Returns True if all characters in the string are lower case|
|[isnumeric()](https://www.w3schools.com/python/ref_string_isnumeric.asp)|Returns True if all characters in the string are numeric|
|[isprintable()](https://www.w3schools.com/python/ref_string_isprintable.asp)|Returns True if all characters in the string are printable|
|[isspace()](https://www.w3schools.com/python/ref_string_isspace.asp)|Returns True if all characters in the string are whitespaces|
|[istitle()](https://www.w3schools.com/python/ref_string_istitle.asp)|Returns True if the string follows the rules of a title|
|[isupper()](https://www.w3schools.com/python/ref_string_isupper.asp)|Returns True if all characters in the string are upper case|
|[join()](https://www.w3schools.com/python/ref_string_join.asp)|Converts the elements of an iterable into a string|
|[ljust()](https://www.w3schools.com/python/ref_string_ljust.asp)|Returns a left justified version of the string|
|[lower()](https://www.w3schools.com/python/ref_string_lower.asp)|Converts a string into lower case|
|[lstrip()](https://www.w3schools.com/python/ref_string_lstrip.asp)|Returns a left trim version of the string|
|[maketrans()](https://www.w3schools.com/python/ref_string_maketrans.asp)|Returns a translation table to be used in translations|
|[partition()](https://www.w3schools.com/python/ref_string_partition.asp)|Returns a tuple where the string is parted into three parts|
|[replace()](https://www.w3schools.com/python/ref_string_replace.asp)|Returns a string where a specified value is replaced with a specified value|
|[rfind()](https://www.w3schools.com/python/ref_string_rfind.asp)|Searches the string for a specified value and returns the last position of where it was found|
|[rindex()](https://www.w3schools.com/python/ref_string_rindex.asp)|Searches the string for a specified value and returns the last position of where it was found|
|[rjust()](https://www.w3schools.com/python/ref_string_rjust.asp)|Returns a right justified version of the string|
|[rpartition()](https://www.w3schools.com/python/ref_string_rpartition.asp)|Returns a tuple where the string is parted into three parts|
|[rsplit()](https://www.w3schools.com/python/ref_string_rsplit.asp)|Splits the string at the specified separator, and returns a list|
|[rstrip()](https://www.w3schools.com/python/ref_string_rstrip.asp)|Returns a right trim version of the string|
|[split()](https://www.w3schools.com/python/ref_string_split.asp)|Splits the string at the specified separator, and returns a list|
|[splitlines()](https://www.w3schools.com/python/ref_string_splitlines.asp)|Splits the string at line breaks and returns a list|
|[startswith()](https://www.w3schools.com/python/ref_string_startswith.asp)|Returns true if the string starts with the specified value|
|[strip()](https://www.w3schools.com/python/ref_string_strip.asp)|Returns a trimmed version of the string|
|[swapcase()](https://www.w3schools.com/python/ref_string_swapcase.asp)|Swaps cases, lower case becomes upper case and vice versa|
|[title()](https://www.w3schools.com/python/ref_string_title.asp)|Converts the first character of each word to upper case|
|[translate()](https://www.w3schools.com/python/ref_string_translate.asp)|Returns a translated string|
|[upper()](https://www.w3schools.com/python/ref_string_upper.asp)|Converts a string into upper case|
|[zfill()](https://www.w3schools.com/python/ref_string_zfill.asp)|Fills the string with a specified number of 0 values at the beginning|
