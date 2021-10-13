# Roman Numerals Kata
This is a Roman Numerals Kata with RSpec tests.
Specs fail fast on first error and run in order to give a step by step flow.

Try to come up with elegant solutions without breaking or changing any spec.

## Run tests with guard
For speed and comfort we can run the specs with `bundle exec guard` which will run them
on every file change.


# Example Algorithm

## Roman to Arabic:
Given a roman number like XI, iterate through each letter and
add it's numeric value to a variable.

Example:

Input = XI

X = 10
I = 1

Result = 10 + 1 = 11

Special Cases:
- When the next letter numerical value is bigger than itself instead of adding,
we need to subtract.

Eg: IX

I = 1
X = 10

Result = -1 + 10 = 9


## Arabic to Roman
Giving a number, keep reducing it to roman figures and add them
to a string variable until the number is zero.

Example:

result = ''

number = 17 . It's less than 40 (XL) and bigger than 10 (X) so lets subtract 10.

number -= 10
result << X

number = 7  It's less than 9 (IX) and bigger than 5 (V) so lets subtract 5.

number -= 5
result << V

number = 2  It's less than 4 (IV) and bigger than 1 (I) so lets subtract 1.

number -= 1
result << I

number -= 1
result << I

result is now: XVII
