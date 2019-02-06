# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

**vacuous** {: #vacuousdef }
: adjective
: Empty; void; lacking meaningful [content](https://en.wiktionary.org/wiki/content).[^vacuousdef-note1]

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

**block** {: #blockdef }
: count noun
: A group of one or more [expressions](#expressiondef), [declarations](https://en.wikipedia.org/wiki/Declaration_(computer_programming)), [statements](#statementdef) or other units of code that are related in such a way as to comprise a whole. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a **block-structured programming language**. Blocks are fundamental to [structured programming](https://en.wikipedia.org/wiki/Structured_programming), where [control structures](https://en.wikipedia.org/wiki/Control_structure) are formed from blocks.  
The function of blocks in programming is to enable groups of statements to be treated as if they were one statement, and to narrow the [lexical scope](https://en.wikipedia.org/wiki/Lexical_scope) of objects such as variables and [subroutines](#subroutinedef) declared in a block so that they do not conflict with those having the same name used elsewhere. In a block-structured programming language, the objects named in outer blocks are visible inside inner blocks, unless they are [masked](https://en.wikipedia.org/wiki/Name_masking) by an object declared with the same name.[^blockdef-note1] Boundaries between blocks are demarcated by [separators](#separatordef).
: In [C++](https://en.wikipedia.org/wiki/C++), blocks are delimited by **curly brackets** (`{` ... `}`).

**Boolean** {: #Booleandef }
: adjective
: Having one of two possible [values](#valuedef) (usually denoted *true* and *false*), intended to represent the two [truth values](https://en.wikipedia.org/wiki/Truth_value) of [logic](https://en.wikipedia.org/wiki/Logic) and [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra).[^Booleandef-note1]

**Boolean data type** {: #Booleandatatypedef }
: proper noun
: A [data type](#datatypedef) limited to [Boolean](#Booleandef) [values](#valuedef). The Boolean data type is primarily associated with [conditional](#conditionaldef) [statements](#statementdef), which allow different actions by changing [control flow](https://en.wikipedia.org/wiki/Control_flow) depending on whether a programmer-specified Boolean *condition* evaluates to true or false.[^Booleandatatypedef-note1]
: For its etymology, it is named after [George Boole](https://en.wikipedia.org/wiki/George_Boole), who first defined an algebraic system of logic in the mid 19th century.[^Booleandatatypedef-note1]
: Hyponym of [data type](#datatypedef).

**condition** {: #conditiondef }
: count noun
: A [Boolean](#Booleandef) logical clause or phrase.[^conditiondef-note1]

**conditional** {: #conditionaldef }
: count noun
: An [instruction](https://en.wiktionary.org/wiki/instruction) that [branches](https://en.wiktionary.org/wiki/branch) depending on the truth value of a [condition](#conditiondef) at that point.[^conditionaldef-note1]

**datum** {: #datumdef }
: count noun, plurally **data**
: Any sequence of one or more [symbols](#symboldef) given meaning by one or more specific acts of interpretation.  
A datum requires interpretation to become [information](https://en.wikipedia.org/wiki/Information). To translate it to information, there must be several known factors considered. The factors involved are determined by the creator of the datum and the desired information. The term [metadata](https://en.wikipedia.org/wiki/Metadata) is used to reference the data about the data. Metadata may be implied, specified or given. Data relating to physical events or processes will also have a temporal component. In almost all cases this temporal component is implied. This is the case when a device such as a temperature logger receives data from a temperature [sensor](https://en.wikipedia.org/wiki/Sensor). When the temperature is received it is assumed that the data has a temporal references of "now". So the device records the date, time and temperature together. When the data logger communicates temperatures, it must also report the date and time ([metadata](https://en.wikipedia.org/wiki/Metadata)) for each temperature.  
[Digital data](https://en.wikipedia.org/wiki/Digital_data) is data that is represented using the [binary number](https://en.wikipedia.org/wiki/Binary_number) system of ones (1) and zeros (0), as opposed to [analog](https://en.wikipedia.org/wiki/Analog_signal) representation. In modern (post 1960) computer systems, all data is digital. Data within a computer, in most cases, moves as parallel data. Data moving to or from a computer, in most cases, moves as serial data. See [Parallel communication](https://en.wikipedia.org/wiki/Parallel_communication) and [Serial communication](https://en.wikipedia.org/wiki/Serial_communication). Data sourced from an analog device, such as a temperature sensor, must pass through an "[analog to digital converter](https://en.wikipedia.org/wiki/Analog-to-digital_converter)" or "ADC" (see [Analog-to-digital converter] to convert the analog data to digital data.  
Data representing [quantities](https://en.wikipedia.org/wiki/Quantities), characters, or symbols on which operations are performed by a [computer](https://en.wikipedia.org/wiki/Computer) are [stored](https://en.wikipedia.org/wiki/Data_storage_device) and [recorded](https://en.wikipedia.org/wiki/Record_(computer_science)) on [magnetic](https://en.wikipedia.org/wiki/Magnetic_tape_data_storage), optical, or mechanical recording media, and [transmitted](https://en.wikipedia.org/wiki/Data_transmission) in the form of digital electrical signals.[^datumdef1]  
A [program](https://en.wikipedia.org/wiki/Computer_program) is a set of data that consists of a series of coded software instructions to control the operation of a computer or other machine.[^datumdef2] Physical [computer memory](https://en.wikipedia.org/wiki/Computer_memory) elements consist of an address and a byte/word of data storage. Digital data are often stored in [relational databases](https://en.wikipedia.org/wiki/RDBMS), like [tables](https://en.wikipedia.org/wiki/Table_(database)) or SQL databases, and can generally be represented as abstract key/value pairs.  
Data can be organized in many different types of [data structures](https://en.wikipedia.org/wiki/Data_structures), including arrays, [graphs](https://en.wikipedia.org/wiki/Graph_(data_structure)), and [objects](https://en.wikipedia.org/wiki/Object_(computer_science)). Data structures can store data of many different [types](#datatypedef), including [numbers](https://en.wikipedia.org/wiki/Floating_point), [strings](https://en.wikipedia.org/wiki/String_(computer_science)) and even other [data structures](https://en.wikipedia.org/wiki/Recursive_type). Data pass in and out of computers via [peripheral devices](https://en.wikipedia.org/wiki/Peripheral). The total amount of digital data in 2007 was estimated to be 281 billion [gigabytes](https://en.wikipedia.org/wiki/Gigabytes) (= 281 [exabytes](https://en.wikipedia.org/wiki/Exabytes)).[^datumdef3] [^datumdef4] [Digital data](https://en.wikipedia.org/wiki/Digital_data) comes in these three states: [data at rest](https://en.wikipedia.org/wiki/Data_at_rest), [data in transit](https://en.wikipedia.org/wiki/Data_in_transit) and [data in use](https://en.wikipedia.org/wiki/Data_in_use). [^datumdef-note1]

**data type** {: #datatypedef }
: count noun
: An attribute of [data](#datumdef) which tells the [compiler](https://en.wikipedia.org/wiki/Compiler) or [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) how the programmer intends to use the data. Most programming languages support common data types of [real](https://en.wikipedia.org/wiki/Real_number), [integer](https://en.wikipedia.org/wiki/Integer_(computer_science)) and [Boolean](#Booleandatatypedef). A data type constrains the [values](#valuedef) that an [expression](#expressiondef), such as a variable or a [subroutine](#subroutinedef), might take. This data type defines the operations that can be done on the data, the meaning of the data, and the way values of that type can be stored. A type of value from which an expression may take its value.[^datatypedef1] [^datatypedef2] [^datatypedef-note1]
: Hypernym of [Boolean data type](#Booleandatatypedef).

**entry point** {: #entrypointdef }
: count noun
: The point in a program where the first instructions are executed, and where the program has access to [command line arguments](https://en.wikipedia.org/wiki/Command_line_arguments).[^entrypointdef-note1] [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**expression** {: #expressiondef }
: A combination of one or more [constants](https://en.wikipedia.org/wiki/Constant_(programming)), [variables](https://en.wikipedia.org/wiki/Variable_(programming)), [operators](https://en.wikipedia.org/wiki/Operator_(programming)), and [subroutines](#subroutinedef) that a [programming language](https://en.wikipedia.org/wiki/Programming_language) interprets (according to its particular [rules of precedence](https://en.wikipedia.org/wiki/Order_of_operations) and of [association](#associativitydef)) and computes to produce ("to return", in a [stateful](https://en.wikipedia.org/wiki/State_(computer_science)) environment) another [value](#valuedef). This process, as for [mathematical expressions](https://en.wikipedia.org/wiki/Mathematical_expression), is called evaluation. In simple settings, the [resulting value](https://en.wikipedia.org/wiki/Return_type) is usually one of various [primitive types](https://en.wikipedia.org/wiki/Primitive_data_type), such as numerical, [string](https://en.wikipedia.org/wiki/String_(computer_science)), and [logical](https://en.wikipedia.org/wiki/Boolean_expression); in more elaborate settings, it can be an arbitrary [complex data type](https://en.wikipedia.org/wiki/Complex_data_type).[^expressiondef-note1]
: For example, `2+3` is an arithmetic and programming expression which evaluates to `5`. A variable is an expression because it denotes a value in memory, so `y+6` is an expression. An example of a relational expression is `4≠4`, which evaluates to `false`.[^expressiondef-note1] [^expressiondef1] [^expressiondef2]
: Hypernym of [relational expression](#relationalexpressiondef).

**if-statement** {: #ifstatementdef }
: count noun
: A [conditional](#conditionaldef) [statement](#statementdef).
: 
```
If (condition) Then
    (consequent)
Else
    (alternative)
End If
```
: In the [pseudocode](https://en.wikipedia.org/wiki/Pseudocode) construct above, the part represented by *(condition)* constitutes a conditional *[expression](#expressiondef)*, having intrinsic value (for example, it may be substituted by either of the [values](#valuedef) `True` or `False`) but having no intrinsic meaning. In contrast, the combination of this expression, the `If` and `Then` surrounding it, and the consequent that follows afterward constitute a conditional *[statement](#statementdef)*, having intrinsic meaning (for example, expressing a coherent logical rule) but no intrinsic value.  
When an [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) finds an `If`, it expects a [condition](#conditiondef) (for example, `x > 0`, which means "the variable x contains a number that is greater than zero") and evaluates that condition. If the condition is `true`, the statements following the `then` are executed. Otherwise, the execution continues in the following branch, either in the `else` [block](https://en.wikipedia.org/wiki/Block_(programming)) (which is usually optional), or if there is no `else` branch, then after the `end If`.  
After either branch has been executed, [control](https://en.wikipedia.org/wiki/Control_flow) returns to the point after the `end If`.[^ifstatementdef-note1]
: Hyponym of [statement](#statementdef).

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
: The part of a computer instruction which specifies what [data](#datumdef) is to be manipulated or operated on, while at the same time representing the data itself.

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

**separator** {: #separatordef }
: count noun
: A token that demarcates boundaries between two separate [statements](#statementdef). A separator is also known as a **punctuator**.[^separatordef-note1]

**statement** {: #statementdef }
: count noun
: A syntactic unit of an [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [programming language](https://en.wikipedia.org/wiki/Programming_language) that expresses some action to be carried out.[^statementdef1] A program written in such a language is formed by a sequence of one or more statements. A statement may have internal components (e.g., [expressions](#expressiondef)). Boundaries between statements are demarcated by [separators](#separatordef), and the end of a statement is demarcated by a [terminator](#terminatordef). [^statementdef-note1]
: Hypernym of [if-statement](#ifstatementdef).

**subroutine** {: #subroutinedef }
: count noun
: A sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed. It may be defined within a single program, or separately in a [library](https://en.wikipedia.org/wiki/Library_(computer_science)) that can be used by many programs. In different programming languages, a subroutine may be called a **procedure**, a **function**, a **routine**, a [method](https://en.wikipedia.org/wiki/Method_(computing)), or a **subprogram**. The generic term **callable unit** is sometimes used.[^subroutinedef1] [^subroutinedef-note1]
: Subroutines have [arity](#aritydef).

**symbol** {: #symboldef }
: count noun
: A waveform, a state or a significant condition of a communication channel that persists for a fixed period of time. It may be described as either a pulse in digital baseband transmission or a tone in passband transmission using modems. A sending device places symbols on the channel at a fixed and known symbol rate, and the receiving device has the job of detecting the sequence of symbols in order to reconstruct the transmitted [data](#datumdef). There may be a direct correspondence between a symbol and a small unit of data. For example, each symbol may encode one or several binary digits or 'bits'. The data may also be represented by the transitions between symbols, or even by a sequence of many symbols.[^symboldef-note1]

**terminator** {: #terminatordef }
: count noun
: A token that demarcates the end of an individual [statement](#statementdef).[^terminatordef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), it is a semicolon (`;`).

**trailing** {: #trailingdef }
: adjective
: Occuring at the end[^trailingdef] of a line.
: For example, this line contains two **trailing** dots.⋅⋅

**truncate** {: #truncatedef }
: verb
: To shorten a [decimal](https://en.wiktionary.org/wiki/decimal) [number](https://en.wiktionary.org/wiki/number) by removing [trailing](#trailingdef) or [leading](#leadingdef) [digits](https://en.wiktionary.org/wiki/digit).[^truncatedef-note1]

**value** {: #valuedef }
: count noun
: A member of the set of possible interpretations of any possibly-infinite sequence of [symbols](#symboldef).[^valuedef-note1]

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [Block (programming)](https://en.wikipedia.org/w/index.php?title=Block_(programming)&oldid=877703688)
- [Boolean data type](https://en.wikipedia.org/w/index.php?title=Boolean_data_type&oldid=876857392)
- [Comparison of programming languages (syntax)§Blocks](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Blocks)
- [Comparison of programming languages (syntax)§Statements](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Statements)
- [Conditional (computer programming)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Conditional (computer programming)§If–then(–else)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Data (computing)](https://en.wikipedia.org/w/index.php?title=Data_(computing)&oldid=881080086)
- [Data type](https://en.wikipedia.org/w/index.php?title=Data_type&oldid=879519751)
- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=881544189)
- [Expression (computer science)](https://en.wikipedia.org/w/index.php?title=Expression_(computer_science)&oldid=878391104)
- [Lexical analysis§Token](https://en.wikipedia.org/w/index.php?title=Lexical_analysis&oldid=872271284).
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Nesting (computing)](https://en.wikipedia.org/w/index.php?title=Nesting_(computing)&oldid=877015415)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)
- [Relational operator](https://en.wikipedia.org/w/index.php?title=Relational_operator&oldid=874050383)
- [Statement (computer science)](https://en.wikipedia.org/w/index.php?title=Statement_(computer_science)&oldid=863825665)
- [Symbol rate§Symbols](https://en.wikipedia.org/w/index.php?title=Symbol_rate&oldid=870702760#Symbols)
- [Subroutine](https://en.wikipedia.org/w/index.php?title=Subroutine&oldid=879018923)

on Wikipedia, with changes made, and:

- [arity](https://en.wiktionary.org/w/index.php?title=arity&oldid=50758406)
- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [condition](https://en.wiktionary.org/w/index.php?title=condition&oldid=51410719)
- [conditional](https://en.wiktionary.org/w/index.php?title=conditional&oldid=51276861)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)
- [vacuous](https://en.wiktionary.org/w/index.php?title=vacuous&oldid=47613271)

on Wiktionary, with changes made.

[^aritydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/arity), except for the removal of the words “[arguments](https://en.wiktionary.org/wiki/argument)” and “[operation](https://en.wiktionary.org/wiki/operation)”, which do not seem to apply in a computer science context.
[^associativitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity).
[^atomicitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity).
[^blockdef-note1]: This definition is based on [Wikipedia's definition of a block as a page](https://en.wikipedia.org/wiki/Block_(programming)) and [as a section of a page](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Blocks).
[^Booleandatatypedef-note1]: This definition is based on [Wikipedia's definition of Boolean data type](https://en.wikipedia.org/wiki/Boolean_data_type) and [Data type](https://en.wikipedia.org/wiki/Data_type).
[^Booleandef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Boolean_data_type).
[^conditionaldef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/conditional).
[^conditiondef-note1]: This definition is based on definitions from [Wiktionary](https://en.wiktionary.org/wiki/condition) and [Wikipedia](https://en.wikipedia.org/wiki/Conditional_(computer_programming)).
[^datatypedef1]: [type](http://foldoc.org/type) at the *[Free On-line Dictionary of Computing](https://en.wikipedia.org/wiki/Free_On-line_Dictionary_of_Computing)*
[^datatypedef2]: [Shaffer, C. A. (2011). *Data Structures & Algorithm Analysis in C++* (3rd ed.). Mineola, NY: Dover. 1.2. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [978-0-486-48582-9](https://en.wikipedia.org/wiki/Special:BookSources/978-0-486-48582-9).
[^datatypedef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Data_type).
[^datumdef1]: ["data"](http://oxforddictionaries.com/definition/american_english/data). *Oxford Dictionaries*. [Archived](https://web.archive.org/web/20121006073603/http://oxforddictionaries.com/definition/american_english/data) from the original on 2012-10-06. Retrieved 2012-10-11.
[^datumdef2]: ["computer program"](http://www.encyclopedia.com/topic/computer_program.aspx#2). *The Oxford Pocket Dictionary of Current English*. [Archived](https://web.archive.org/web/20111128202415/http://www.encyclopedia.com/topic/computer_program.aspx#2) from the original on 2011-11-28. Retrieved 2012-10-11.
[^datumdef3]: Paul, Ryan (March 12, 2008). ["Study: amount of digital info > global storage capacity"](https://arstechnica.com/news.ars/post/20080312-study-amount-of-digital-info-global-storage-capacity.html). Ars Technics. [Archived](https://web.archive.org/web/20080313111238/http://arstechnica.com/news.ars/post/20080312-study-amount-of-digital-info-global-storage-capacity.html) from the original on March 13, 2008. Retrieved 2008-03-12.
[^datumdef4]: Gantz, John F.; et al. (2008). ["The Diverse and Exploding Digital Universe"](https://web.archive.org/web/20080311234210/http://www.emc.com/leadership/digital-universe/expanding-digital-universe.htm). International Data Corporation via EMC. Archived from [the original](http://www.emc.com/leadership/digital-universe/expanding-digital-universe.htm) on 2008-03-11. Retrieved 2008-03-12.
[^datumdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Data_(computing)).
[^entrypointdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point), with some rewording.
[^expressiondef1]: [Javascript expressions, Mozilla](https://developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Expressions) Accessed July 6, 2009]
[^expressiondef2]: [Programming in C](https://www.cs.drexel.edu/~rweaver/COURSES/ISTC-2/TOPICS/expr.html) Accessed July 6, 2009
[^expressiondef-note1]: This definition is similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Expression_(computer_science)), with changes made.
[^ifstatementdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then(%E2%80%93else)).
[^leadingdef]: <https://stackoverflow.com/questions/959215/how-do-i-remove-leading-whitespace-in-python>
[^literaldef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Literal_(computer_programming)).
[^nestdef-note1]: This definition is loosely based on [Wikipedia's definition of “nesting”](https://en.wikipedia.org/wiki/Nesting_(computing)).
[^octetdef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)), except for the removal of the phrase “in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications)”.
[^operanddef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science).
[^operatordef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming), except for modification of the grammatical number (plural to singular).
[^operatordef-note2]: Based on [information from Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity).
[^relationalexpressiondef-note1]: This definition similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^relationaloperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^separatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement separator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^statementdef1]: ["statement"](http://www.webopedia.com/TERM/S/statement.html). webopedia. Retrieved 2015-03-03.
[^statementdef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Statement_(computer_science)).
[^subroutinedef1]: [U.S. Election Assistance Commission](https://en.wikipedia.org/wiki/Election_Assistance_Commission "Election Assistance Commission") (2007). ["Definitions of Words with Special Meanings"](https://web.archive.org/web/20121208084203/http://www.eac.gov/vvsg/glossary.aspx). *[Voluntary Voting System Guidelines](https://en.wikipedia.org/wiki/Voluntary_Voting_System_Guidelines "Voluntary Voting System Guidelines")*. Archived from [the original](http://www.eac.gov/vvsg/glossary.aspx) on 2012-12-08. Retrieved 2013-01-14.
[^subroutinedef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Subroutine), with some rewording.
[^symboldef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Symbol_rate#Symbols).
[^terminatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement terminator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
[^truncatedef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate).
[^vacuousdef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/vacuous).
[^valuedef-note1]: This definition is based on the definition proposed on [an answer on Stack Overflow](https://stackoverflow.com/questions/3300726/what-is-a-value-in-the-context-of-programming/3301073#3301073).
