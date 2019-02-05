# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

## computer science glossary

**arity** {: #aritydef }
: mass noun
: The number of [operands](#operanddef) a [function](https://en.wiktionary.org/wiki/function) takes.[^aritydef-note1]

**associativity** {: #associativitydef }
: mass noun
: The property of an [operator](#operatordef) which determines how it is grouped with operators of the same [precedence](https://en.wiktionary.org/wiki/precedence) in the absence of parentheses.[^associativitydef-note1]

**atomicity** {: #atomicitydef }
: mass noun
: The state of a [system](https://en.wiktionary.org/wiki/system) (often a [database](https://en.wiktionary.org/wiki/database) system) in which either all stages [complete](https://en.wiktionary.org/wiki/complete) or [none](https://en.wiktionary.org/wiki/none) complete.[^atomicitydef-note1]

**entry point** {: #entrypointdef }
: count noun
: The point in a program where the first instructions are executed, and where the program has access to [command line arguments](https://en.wikipedia.org/wiki/Command_line_arguments).[^entrypointdef-note1] [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**leading** {: #leadingdef }
: adjective
: Occuring at the beginning[^leadingdef] of a line.
: ⋅⋅For example, this line contains two **leading** dots.

**literal** {: #literaldef }
: count noun
: A notation for representing a fixed value in source code.[^literaldef-note1]

**nest** {: #nestdef }
: verb
: To [contain an object within a similar object](https://en.wikipedia.org/wiki/Self-similarity).[^nestdef-note1]
: To organize information into layers.[^nestdef-note1]

**octet** {: #octetdef }
: count noun
: A [unit of digital information](https://en.wikipedia.org/wiki/Units_of_information) that consists of eight [bits](https://en.wikipedia.org/wiki/Bit). The term is often used when the term [byte](https://en.wikipedia.org/wiki/Byte) might be ambiguous, as the byte has historically been used for storage units of a variety of sizes.[^octetdef-note1]

**operand** {: #operanddef }
: count noun
: The part of a computer instruction which specifies what data is to be manipulated or operated on, while at the same time representing the data itself.
: Operands have [arity](#aritydef).

**operator** {: #operatordef }
: count noun
: A construct which behaves generally like a function, but which differs [syntactically](https://en.wikipedia.org/wiki/Syntax_(programming_languages)) or [semantically](https://en.wikipedia.org/wiki/Semantics_(computer_science)) from a usual function.[^operatordef-note1]
: Operators have [associativity](#associativitydef). they may be **associative, left-associative, right-associative** or **non-associative**. For **associative** operators, the operations can be grouped arbitrarily. For **left-associative** operators, the operations are grouped from the left. For **right-associative** operators, the operations are grouped from the right. For **non-associative** operators, the operations cannot be chained, often because the output type is incompatible with the input types.[^operatordef-note2]

**trailing** {: #trailingdef }
: adjective
: Occuring at the end[^trailingdef] of a line.
: For example, this line contains two **trailing** dots.⋅⋅

**truncate** {: #truncatedef }
: verb
: To shorten a [decimal](https://en.wiktionary.org/wiki/decimal) [number](https://en.wiktionary.org/wiki/number) by removing [trailing](#trailingdef) or [leading](#leadingdef) [digits](https://en.wiktionary.org/wiki/digit).[^truncatedef-note1]

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=881544189)
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Nesting (computing)](https://en.wikipedia.org/w/index.php?title=Nesting_(computing)&oldid=877015415)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)

on Wikipedia, with changes made, and:

- [arity](https://en.wiktionary.org/w/index.php?title=arity&oldid=50758406)
- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)

on Wiktionary, with changes made.

[^aritydef-note1]: This is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/arity), except for the removal of the words “[arguments](https://en.wiktionary.org/wiki/argument)” and “[operation](https://en.wiktionary.org/wiki/operation)”, which do not seem to apply in a computer science context.
[^associativitydef-note1]: This is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity).
[^atomicitydef-note1]: This is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity).
[^entrypointdef-note1]: This is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point), with some rewording.
[^leadingdef]: <https://stackoverflow.com/questions/959215/how-do-i-remove-leading-whitespace-in-python>
[^literaldef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Literal_(computer_programming)).
[^nestdef-note1]: This definition is loosely based on [Wikipedia's definition of “nesting”](https://en.wikipedia.org/wiki/Nesting_(computing)).
[^octetdef-note1]: This is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)), except for the removal of the phrase “in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications)”.
[^operanddef-note1]: This is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science).
[^operatordef-note1]: This is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming), except for modification of the grammatical number (plural to singular).
[^operatordef-note2]: Based on [information from Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity).
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
[^truncatedef-note1]: This is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate).
