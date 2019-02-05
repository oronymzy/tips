# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

## computer science glossary

**associativity** {: #associativitydef }
: mass noun
: [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity) is “the property of an [operator](#operatordef) which determines how it is grouped with operators of the same [precedence](https://en.wiktionary.org/wiki/precedence) in the absence of parentheses”.

**atomicity** {: #atomicitydef }
: mass noun
: [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity) is “the state of a [system](https://en.wiktionary.org/wiki/system) (often a [database](https://en.wiktionary.org/wiki/database) system) in which either all stages [complete](https://en.wiktionary.org/wiki/complete) or [none](https://en.wiktionary.org/wiki/none) complete”.

**entry point** {: #entrypointdef }
: count noun
: [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point) is “where the first instructions in a computer program are executed, and where the program then processes command line arguments, which in most common operating systems, are usually set after the file path to the program in the command shell”. [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**leading** {: #leadingdef }
: adjective
: Occuring at the beginning[^leadingdef] of a line.
: ⋅⋅For example, this line contains two **leading** dots.

**literal** {: #literaldef }
: count noun
: [Wikipedia's definition](https://en.wikipedia.org/wiki/Literal_(computer_programming)) is “a notation for representing a fixed value in source code”.

**octet** {: #octetdef }
: count noun
: [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)) is “a [unit of digital information](https://en.wikipedia.org/wiki/Units_of_information) in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications) that consists of eight [bits](https://en.wikipedia.org/wiki/Bit). The term is often used when the term [byte](https://en.wikipedia.org/wiki/Byte) might be ambiguous, as the byte has historically been used for storage units of a variety of sizes.”

**operand** {: #operanddef }
: count noun
: [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science) is “the part of a computer instruction which specifies what data is to be manipulated or operated on, while at the same time representing the data itself”.

**operator** {: #operatordef }
: count noun
: [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming))[^operatordef-note1] is “a construct which behaves generally like a function, but which differs [syntactically](https://en.wikipedia.org/wiki/Syntax_(programming_languages)) or [semantically](https://en.wikipedia.org/wiki/Semantics_(computer_science)) from a usual function.”
: Operators have [associativity](#associativitydef). [According to Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity), they may be **associative, left-associative, right-associative** or **non-associative**. For **associative** operators, the operations can be grouped arbitrarily. For **left-associative** operators, the operations are grouped from the left. For **right-associative** operators, the operations are grouped from the right. For **non-associative** operators, the operations cannot be chained, often because the output type is incompatible with the input types.

**trailing** {: #trailingdef }
: adjective
: Occuring at the end[^trailingdef] of a line.
: For example, this line contains two **trailing** dots.⋅⋅

**truncate** {: #truncatedef }
: verb
: [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate) is “to shorten (a [decimal](https://en.wiktionary.org/wiki/decimal) [number](https://en.wiktionary.org/wiki/number)) by removing [trailing](#trailingdef) (or [leading](#leadingdef)) [digits](https://en.wiktionary.org/wiki/digit)”.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=871836841)
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)

on Wikipedia, with changes made, and:

- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)

on Wiktionary, with changes made.

[^leadingdef]: <https://stackoverflow.com/questions/959215/how-do-i-remove-leading-whitespace-in-python>
[^operatordef-note1]: The grammatical number has been modified (plural to singular).
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
