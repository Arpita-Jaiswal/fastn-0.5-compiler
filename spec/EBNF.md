# EBNF 

```chatinput
<fastn> ::= <item>*
<item> ::= <module_comment> | <comment> | <section>


<module_comment> ::= (<single_module_comment> <new_line>)* <single_module_comment> (<new_line> | <eof>)
<single_module_comment> ::= ";;;" <opt_whitespace> <statement>? <opt_whitespace> 

<comment> ::= (<single_comment> <new_line>)* <single_comment> (<new_line> | <eof>)
<single_comment> ::= ";;" <opt_whitespace> <statement>? <opt_whitespace> <new_line>


<section> ::= <start_marker> <opt_whitespace> <section_declaration>?
<section_declaration> ::= (<section_kind> <whitespace>)? <section_name> <colon> <opt_whitespace> <section_value>? <opt_whitespace> 
<section_kind> ::= <text>
<section_name> ::= <text>
<section_value> ::= <text>



<start_marker> ::= "--"
<end_marker> ::= "--" <whitespace> "end:" <opt_whitespace>
<new_line> ::= "\n"
<eof> ::= "\n"
<colon> ::= ":"

<statement> ::= <text> <opt_whitespace> | <text>
<opt_whitespace> ::= " "*
<whitespace> ::= " "+
<text> ::= <character> <text> | <character>
<character> ::= <letter> | <digit>
<letter> ::= "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M" | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z" | "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m" | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z"
<digit> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```