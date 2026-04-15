# Break Eternity C++ Version
A recreation of break_eternity .js but instead of using javascript it uses C++, which supports numbers to 10^^(2^1024).

# All the credit goes to Patashu, the creator of Break Eternity JS. I used his project's name here.

# Information
Break-Eternity-CPP is a project made to compute numbers up to 10^^(2^1024), same as break_eternity.js.
The actual point here is that i remade it but in C++, so you can use C++ libraries with it.

# Features
EternityNum struct, addition, subtraction, multiplication, division, exponentation, tetration, normalization (fixNum),
log10, pow10, natural logarithm (ln), logarithm (customizable base too), isEqual, isHigher, isLower, slog (slightly inaccurate)

# How to use
You start off by making a EternityNum struct with two double variables: the layer and the value.
To set a variable, you don't just set 1e+400, as this will result in an error and isn't a struct.
To actually make it 1e+400, you need to make {1, 400}. Why? The '1' is how much e's are there (or 10^'s) and
the 400 is the value, so {3, 300} will be eee300.
ADDITION: To add to a variable, you need to set x = addNum(y, z) where x, y and z are ENums (eternitynums). Put anything like {1, 10} and {0, 1000000000}, it will return ~{1, 10.04} or ~10.04F1.
SUBTRACTION: You get the point, it's the same with the addition, but it subtracts it. subNum(y, z) returns y - z.
MULTIPLICATION: here, {1, 10} and {1, 9} would result in {1, 19}, because 10^x * 10^y is always 10^(x+y).
DIVISION: Inverted multiplication. {1, 10} and {1, 9} returns {1, 1} because 10^x / 10^y is always 10^(x-y).
TETRATION: It currently tetrates by 2 n times, it will be improved later. Once it's improved, i will add it here
LOG10: If the layer is 1 or higher, it subtracts it, if it's 0, it log10s the value.
POW10: This is the function that took like 30 seconds to make. It adds the layer by 1.
FACTORIAL: It will also be improved later, basically n! = n * n-1 * n-2 ... n times ... * 1. There is a bug that it can explode from 99093F1 to 99099F2 and then each factorial by itself adds the F2's value by ~5
NATURAL LOGARITHM: This is a logarithm with the base equal to 'e' (~2.71).
LOGARITHM: One of the 2 only functions with 1 line inside. Its formula is ln(a) / ln(b).
ISEQUAL: Input two variables, and depending on what you put there, it will return 0 or 1 (false or true)
ISHIGHER: Input two variables, and says if a > b is true or false. To recreate ">=", you need to use isHigher && isEqual for now.
ISLOWER: Input two variables, and it says the exact opposite of isHigher.
SLOG (NEW): The opposite of tetration, but it's sadly slightly inaccurate. Will be fixed later

# Stuff to fix
1. Factorial inaccuracy: fact(99093F1) will result in 99099F2
2. Slog inaccuracy: Results may be off, like it was once tested, it said ~2.84 where it had to be ~2.89.

# Extras
The code comes with a calculator, ready for you to test. If you can, tell me if there's any issues except for factorial/slog inaccuracy.
