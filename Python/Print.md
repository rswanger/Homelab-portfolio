
Print("hello, world")

## Definition and Usage

The `print()` function prints the specified message to the screen, or other standard output device.

The message can be a string, or any other object, the object will be converted into a string before written to the screen.

---

## Syntax

print_(object(s)_, sep=_separator_, end=_end_, file=_file_, flush=_flush_)

## Parameter Values

|Parameter|Description|
|---|---|
|_object(s)_|Any object, and as many as you like. Will be converted to string before printed|
|sep='_separator_'|Optional. Specify how to separate the objects, if there is more than one. Default is ' '|
|end='_end_'|Optional. Specify what to print at the end. Default is '\n' (line feed)|
|_file_|Optional. An object with a write method. Default is sys.stdout|
|_flush_|Optional. A Boolean, specifying if the output is flushed (True) or buffered (False). Default is False|

---

## More Examples

### Example

Print more than one object:

print("Hello", "how are you?")

### Example

Print a tuple:

x = ("apple", "banana", "cherry")  
print(x)

### Example

Print two messages, and specify the separator:

print("Hello", "how are you?", sep="---")