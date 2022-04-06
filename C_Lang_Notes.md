## atoi()
In the C Programming Language, the atoi function converts a string to an integer. The atoi function skips all white-space characters at the beginning of the string, converts the subsequent characters as part of the number, and then stops when it encounters the first character that isn't a number.

## strcmp()
The C library function int strcmp(const char *str1, const char *str2) compares the string pointed to, by str1 to the string pointed to by str2.

- The strcmp() function compares two strings and returns 0 if both strings are identical.
- int strcmp (const char* str1, const char* str2);
- The strcmp() function takes two strings and returns an integer.
- The strcmp() compares two strings character by character.
- It is defined in the **string.h** header file.

## Lex
Specify all pattern matching rule.

## Yacc
Specify Grammer rules.

Yacc reads the grammar descriptions in file.y and generates a parser,

## Intro to Lex and [Yacc](Yacc)
Yacc reads the grammar descriptions in bas.y and generates a parser, function
yyparse, in file y.tab.c. Included in file bas.y are token declarations. The –d option
causes yacc to generate definitions for tokens and place them in file y.tab.h. Lex reads
the pattern descriptions in bas.l, includes file y.tab.h, and generates a lexical
analyzer, function yylex, in file lex.yy.c.

Finally, the lexer and parser are compiled and linked together to form the executable,

## getchar()
It takes one charecter as input.

## putchar()
It put one charecter as output.
