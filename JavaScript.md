# Js

- adding floating point with 3/8 giving weird outputs.
ex: 1.2 + 1.3 = 2.4000000000000004
ex: 1.2 + 1.8 = 2.9000000000000004

It's because Js only has double Number type no specific int.
So 1 and 1.0 are the same value.

## Good Parts
-> Integer overflow can be avoided.
-> All you need to know is about number is that it's a number.
