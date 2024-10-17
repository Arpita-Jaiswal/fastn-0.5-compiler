# EBNF 

```chatinput
<fastn> ::= <item>*
<item> ::= <module_comment> | <comment>


<module_comment> ::= (<single_module_comment> <new_line>)* <single_module_comment> (<new_line> | <eof>)
<single_module_comment> ::= ";;;" <opt_whitespace> <statement>? <opt_whitespace> 

<comment> ::= (<single_comment> <new_line>)* <single_comment> (<new_line> | <eof>)
<single_comment> ::= ";;" <opt_whitespace> <statement>? <opt_whitespace> <new_line>



<new_line> ::= "\n"
<eof> ::= "\n"
<statement> ::= <text> <opt_whitespace> | <text>
<opt_whitespace> ::= " "*
<text> ::= <character> <text> | <character>
<character> ::= <letter> | <digit>
<letter> ::= "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M" | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z" | "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m" | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z"
<digit> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```