
**Int()** tells python that the text inside the parentheses is a number.   Without Int() even numbers are viewed as text inputs.

**Float()**
_class_ float(_number=0.0_, _/_)[](https://docs.python.org/3/library/functions.html#float "Link to this definition")

_class_ float(_string_, _/_)

Return a floating-point number constructed from a number or a string.

Examples:

float('+1.23')
1.23
float('   -12345\n')
-12345.0
float('1e-003')
0.001
float('+1E6')
1000000.0
float('-Infinity')
-inf

If the argument is a string, it should contain a decimal number, optionally preceded by a sign, and optionally embedded in whitespace. The optional sign may be `'+'` or `'-'`; a `'+'` sign has no effect on the value produced. The argument may also be a string representing a NaN (not-a-number), or positive or negative infinity. More precisely, the input must conform to the [`floatvalue`](https://docs.python.org/3/library/functions.html#grammar-token-float-floatvalue) production rule in the following grammar, after leading and trailing whitespace characters are removed:

**sign**:          "+" | "-"
**infinity**:      "Infinity" | "inf"
**nan**:           "nan"
**digit**:         <a Unicode decimal digit, i.e. characters in Unicode general category Nd>
**digitpart**:     [`digit`](https://docs.python.org/3/library/functions.html#grammar-token-float-digit) (["_"] [`digit`](https://docs.python.org/3/library/functions.html#grammar-token-float-digit))*
**number**:        [[`digitpart`](https://docs.python.org/3/library/functions.html#grammar-token-float-digitpart)] "." [`digitpart`](https://docs.python.org/3/library/functions.html#grammar-token-float-digitpart) | [`digitpart`](https://docs.python.org/3/library/functions.html#grammar-token-float-digitpart) ["."]
**exponent**:      ("e" | "E") [[`sign`](https://docs.python.org/3/library/functions.html#grammar-token-float-sign)] [`digitpart`](https://docs.python.org/3/library/functions.html#grammar-token-float-digitpart)
**floatnumber**:   [`number`](https://docs.python.org/3/library/functions.html#grammar-token-float-number) [[`exponent`](https://docs.python.org/3/library/functions.html#grammar-token-float-exponent)]
**absfloatvalue**: [`floatnumber`](https://docs.python.org/3/library/functions.html#grammar-token-float-floatnumber) | [`infinity`](https://docs.python.org/3/library/functions.html#grammar-token-float-infinity) | [`nan`](https://docs.python.org/3/library/functions.html#grammar-token-float-nan)
**floatvalue**:    [[`sign`](https://docs.python.org/3/library/functions.html#grammar-token-float-sign)] [`absfloatvalue`](https://docs.python.org/3/library/functions.html#grammar-token-float-absfloatvalue)

Case is not significant, so, for example, “inf”, “Inf”, “INFINITY”, and “iNfINity” are all acceptable spellings for positive infinity.

Otherwise, if the argument is an integer or a floating-point number, a floating-point number with the same value (within Python’s floating-point precision) is returned. If the argument is outside the range of a Python float, an [`OverflowError`](https://docs.python.org/3/library/exceptions.html#OverflowError "OverflowError") will be raised.

For a general Python object `x`, `float(x)` delegates to `x.__float__()`. If [`__float__()`](https://docs.python.org/3/reference/datamodel.html#object.__float__ "object.__float__") is not defined then it falls back to [`__index__()`](https://docs.python.org/3/reference/datamodel.html#object.__index__ "object.__index__").

See also [`float.from_number()`](https://docs.python.org/3/library/stdtypes.html#float.from_number "float.from_number") which only accepts a numeric argument.

If no argument is given, `0.0` is returned.

The float type is described in [Numeric Types — int, float, complex](https://docs.python.org/3/library/stdtypes.html#typesnumeric).

Changed in version 3.6: Grouping digits with underscores as in code literals is allowed.

Changed in version 3.7: The parameter is now positional-only.

Changed in version 3.8: Falls back to [`__index__()`](https://docs.python.org/3/reference/datamodel.html#object.__index__ "object.__index__") if [`__float__()`](https://docs.python.org/3/reference/datamodel.html#object.__float__ "object.__float__") is not defined.

**Round**(_number_, _ndigits=None_)[](https://docs.python.org/3/library/functions.html#round "Link to this definition")

Return _number_ rounded to _ndigits_ precision after the decimal point. If _ndigits_ is omitted or is `None`, it returns the nearest integer to its input.

For the built-in types supporting `round()`, values are rounded to the closest multiple of 10 to the power minus _ndigits_; if two multiples are equally close, rounding is done toward the even choice (so, for example, both `round(0.5)` and `round(-0.5)` are `0`, and `round(1.5)` is `2`). Any integer value is valid for _ndigits_ (positive, zero, or negative). The return value is an integer if _ndigits_ is omitted or `None`. Otherwise, the return value has the same type as _number_.

For a general Python object `number`, `round` delegates to `number.__round__`.

Note

 

The behavior of `round()` for floats can be surprising: for example, `round(2.675, 2)` gives `2.67` instead of the expected `2.68`. This is not a bug: it’s a result of the fact that most decimal fractions can’t be represented exactly as a float. See [Floating-Point Arithmetic: Issues and Limitations](https://docs.python.org/3/tutorial/floatingpoint.html#tut-fp-issues) for more information.

