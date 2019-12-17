[UP](./index.md)

# Escape notation
Allows you to use characters you might not otherwise be able to type out, such as a backspace.  

Besides regular, printable characters, special characters can be encoded using escape notation:

Code	Output

	\XXX	an octal Latin-1 character.
	\'	single quote
	\"	double quote
	\\	backslash
	\n	new line
	\r	carriage return
	\v	vertical tab
	\t	tab
	\b	backspace
	\f	form feed
	\uXXXX	unicode codepoint
	\u{X} ... \u{XXXXXX}	unicode codepoint
	\xXX	the Latin-1 character