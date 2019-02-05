# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

## computer science glossary

**arity** {: #aritydef }
: mass noun
: The number of [operands](#operanddef) a [subroutine](#subroutinedef) takes.[^aritydef-note1]

**associativity** {: #associativitydef }
: mass noun
: The property of an [operator](#operatordef) which determines how it is grouped with operators of the same [precedence](https://en.wiktionary.org/wiki/precedence) in the absence of parentheses.[^associativitydef-note1]

**atomicity** {: #atomicitydef }
: mass noun
: The state of a [system](https://en.wiktionary.org/wiki/system) (often a [database](https://en.wiktionary.org/wiki/database) system) in which either all stages [complete](https://en.wiktionary.org/wiki/complete) or [none](https://en.wiktionary.org/wiki/none) complete.[^atomicitydef-note1]

**entry point** {: #entrypointdef }
: count noun
: The point in a program where the first instructions are executed, and where the program has access to [command line arguments](https://en.wikipedia.org/wiki/Command_line_arguments).[^entrypointdef-note1] [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**expression** {: #expressiondef }
: A combination of one or more [constants](https://en.wikipedia.org/wiki/Constant_(programming)), [variables](https://en.wikipedia.org/wiki/Variable_(programming)), [operators](https://en.wikipedia.org/wiki/Operator_(programming)), and [subroutines](#subroutinedef) that a [programming language](https://en.wikipedia.org/wiki/Programming_language) interprets (according to its particular [rules of precedence](https://en.wikipedia.org/wiki/Order_of_operations) and of [association](#associativitydef)) and computes to produce ("to return", in a [stateful](https://en.wikipedia.org/wiki/State_(computer_science)) environment) another value. This process, as for [mathematical expressions](https://en.wikipedia.org/wiki/Mathematical_expression), is called evaluation. In simple settings, the [resulting value](https://en.wikipedia.org/wiki/Return_type) is usually one of various [primitive types](https://en.wikipedia.org/wiki/Primitive_data_type), such as numerical, [string](https://en.wikipedia.org/wiki/String_(computer_science)), and [logical](https://en.wikipedia.org/wiki/Boolean_expression); in more elaborate settings, it can be an arbitrary [complex data type](https://en.wikipedia.org/wiki/Complex_data_type).[^expressiondef-note1]
: For example, `2+3` is an arithmetic and programming expression which evaluates to `5`. A variable is an expression because it denotes a value in memory, so `y+6` is an expression. An example of a relational expression is `4≠4`, which evaluates to `false`.[^expressiondef-note1] [^expressiondef1] [^expressiondef2]
: Hypernym of [relational expression](#relationalexpressiondef).

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

**operator** {: #operatordef }
: count noun
: A construct which behaves generally like a [subroutine](#subroutinedef), but which differs [syntactically](https://en.wikipedia.org/wiki/Syntax_(programming_languages)) or [semantically](https://en.wikipedia.org/wiki/Semantics_(computer_science)) from a usual subroutine.[^operatordef-note1]
: Operators have [associativity](#associativitydef). They may be **associative, left-associative, right-associative** or **non-associative**. For **associative** operators, the operations can be grouped arbitrarily. For **left-associative** operators, the operations are grouped from the left. For **right-associative** operators, the operations are grouped from the right. For **non-associative** operators, the operations cannot be chained, often because the output type is incompatible with the input types.[^operatordef-note2]
: Hypernym of [relational operator](#relationaloperatordef).

**relational expression** {: #relationalexpressiondef }
: count noun
: An [expression](#expressiondef) created using a [relational operator](#relationaloperatordef), also called a **condition**.[^relationalexpressiondef-note1]
: Hyponym of [expression](#expressiondef).

**relational operator** {: #relationaloperatordef }
: count noun
: A [programming language](https://en.wikipedia.org/wiki/Programming_language) construct or [operator](#operatordef) that tests or defines some kind of [relation](https://en.wikipedia.org/wiki/Relation_(mathematics)) between [two entities](https://en.wikipedia.org/wiki/Binary_function). These include numerical [equality](https://en.wikipedia.org/wiki/Equality_(mathematics)) (*e.g.*, [5 = 5]) and [inequality](https://en.wikipedia.org/wiki/Inequality_(mathematics)) (*e.g.*, [4 ≥ 3]). Relational operators can be seen as special cases of logical [predicates](https://en.wikipedia.org/wiki/Predicate_(mathematical_logic)).[^relationaloperatordef-note1]
: Hyponym of [operator](#operatordef).

**subroutine** {: #subroutinedef }
: count noun
: A sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed. It may be defined within a single program, or separately in a [library](https://en.wikipedia.org/wiki/Library_(computer_science)) that can be used by many programs. In different programming languages, a subroutine may be called a **procedure**, a **function**, a **routine**, a [method](https://en.wikipedia.org/wiki/Method_(computing)), or a **subprogram**. The generic term **callable unit** is sometimes used.[^subroutinedef1] [^subroutinedef-note1]
: Subroutines have [arity](#aritydef).

**trailing** {: #trailingdef }
: adjective
: Occuring at the end[^trailingdef] of a line.
: For example, this line contains two **trailing** dots.⋅⋅

**truncate** {: #truncatedef }
: verb
: To shorten a [decimal](https://en.wiktionary.org/wiki/decimal) [number](https://en.wiktionary.org/wiki/number) by removing [trailing](#trailingdef) or [leading](#leadingdef) [digits](https://en.wiktionary.org/wiki/digit).[^truncatedef-note1]

**value** {: #valuedef }
: count noun
: A member of the set of possible results brought about by an act of computation.[^valuedef-note1]

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=881544189)
- [Expression (computer science)](https://en.wikipedia.org/w/index.php?title=Expression_(computer_science)&oldid=878391104)
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Nesting (computing)](https://en.wikipedia.org/w/index.php?title=Nesting_(computing)&oldid=877015415)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)
- [Relational operator](https://en.wikipedia.org/w/index.php?title=Relational_operator&oldid=874050383)
- [Subroutine](https://en.wikipedia.org/w/index.php?title=Subroutine&oldid=879018923)

on Wikipedia, with changes made, and:

- [arity](https://en.wiktionary.org/w/index.php?title=arity&oldid=50758406)
- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)

on Wiktionary, with changes made.

[^aritydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/arity), except for the removal of the words “[arguments](https://en.wiktionary.org/wiki/argument)” and “[operation](https://en.wiktionary.org/wiki/operation)”, which do not seem to apply in a computer science context.
[^associativitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity).
[^atomicitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity).
[^entrypointdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point), with some rewording.
[^expressiondef1]: [Javascript expressions, Mozilla](https://developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Expressions) Accessed July 6, 2009]
[^expressiondef2]: [Programming in C](https://www.cs.drexel.edu/~rweaver/COURSES/ISTC-2/TOPICS/expr.html) Accessed July 6, 2009
[^expressiondef-note1]: This definition is similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Expression_(computer_science)), with changes made.
[^leadingdef]: <https://stackoverflow.com/questions/959215/how-do-i-remove-leading-whitespace-in-python>
[^literaldef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Literal_(computer_programming)).
[^nestdef-note1]: This definition is loosely based on [Wikipedia's definition of “nesting”](https://en.wikipedia.org/wiki/Nesting_(computing)).
[^octetdef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)), except for the removal of the phrase “in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications)”.
[^operanddef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science).
[^operatordef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming), except for modification of the grammatical number (plural to singular).
[^operatordef-note2]: Based on [information from Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity).
[^relationalexpressiondef-note1]: This definition similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^relationaloperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^subroutinedef1]: [U.S. Election Assistance Commission](https://en.wikipedia.org/wiki/Election_Assistance_Commission "Election Assistance Commission") (2007). ["Definitions of Words with Special Meanings"](https://web.archive.org/web/20121208084203/http://www.eac.gov/vvsg/glossary.aspx). *[Voluntary Voting System Guidelines](https://en.wikipedia.org/wiki/Voluntary_Voting_System_Guidelines "Voluntary Voting System Guidelines")*. Archived from [the original](http://www.eac.gov/vvsg/glossary.aspx) on 2012-12-08. Retrieved 2013-01-14.
[^subroutinedef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Subroutine), with some rewording.
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
[^truncatedef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate).
[^valuedef-note1]: This is a **personal definition** based on the definition proposed on [an answer on Stack Overflow](https://stackoverflow.com/questions/3300726/what-is-a-value-in-the-context-of-programming/3301073#3301073).
