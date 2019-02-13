# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

**vacuous** {: #vacuousdef }
: adjective
: Empty; void; lacking meaningful [content](https://en.wiktionary.org/wiki/content).[^vacuousdef-note1]

## computer science glossary

**accumulator** {: #accumulatordef }
: count noun
: A variable whose contents are [incremented](#incrementdef) to represent the results of a [running total](#runningtotaldef).[^accumulatordef-note1]

**arity** {: #aritydef }
: mass noun
: The number of [operands](#operanddef) a [subroutine](#subroutinedef) takes.[^aritydef-note1]

**assignment construct** {: #assignmentconstructdef }
: A [construct](https://en.wikipedia.org/wiki/Data_structure) that sets and/or re-sets the [value](#valuedef) stored in the storage location(s) denoted by a variable name (in other words, it copies a value into the variable). In most [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [programming languages](https://en.wikipedia.org/wiki/Programming_language) it is a fundamental construct. Assignment constructs can be [expressions](#expressiondef), [statements](#statementdef), or [operators](#assignmentoperatordef).[^assignmentconstructdef-note1]
: Hypernym of [assignment operator](#assignmentoperatordef).

**assignment operator** {: #assignmentoperatordef }
: count noun
: An [assignment construct](#assignmentconstructdef) that is an [operator](#operatordef).
: In [C++](https://en.wikipedia.org/wiki/C++), the operator is an [equality sign](https://en.wikipedia.org/wiki/Equals_sign) (`=`).[^assignmentoperatordef-note1]
: Hypernym of [augmented assignment operator](#augmentedassignmentoperatordef).
: Hyponym of [assignment construct](#assignmentconstructdef) and [operator](#operatordef).

**associativity** {: #associativitydef }
: mass noun
: The property of an [operator](#operatordef) which determines how it is grouped with operators of the same [precedence](https://en.wiktionary.org/wiki/precedence) in the absence of parentheses.[^associativitydef-note1]

**atomicity** {: #atomicitydef }
: mass noun
: The state of a [system](https://en.wiktionary.org/wiki/system) (often a [database](https://en.wiktionary.org/wiki/database) system) in which either all stages [complete](https://en.wiktionary.org/wiki/complete) or [none](https://en.wiktionary.org/wiki/none) complete.[^atomicitydef-note1]

**augmented assignment operator** {: #augmentedassignmentoperatordef }
: count noun
: An [assignment operator](#assignmentoperatordef) that is generally used to replace a [statement](#statementdef) where an operator takes a [variable](https://en.wikipedia.org/wiki/Variable_(programming)) as one of its arguments and then assigns the result back to the same variable. In [expression-oriented programming languages](https://en.wikipedia.org/wiki/Expression-oriented_programming_language) such as C, assignment and augmented assignment are expressions, which have a value. This allows their use in complex expressions. However, this can produce sequences of symbols that are difficult to read or understand, and worse, a mistype can easily produce a different sequence of gibberish that although accepted by the compiler does not produce desired results. In other languages, such as Python, assignment and augmented assignment are statements, not expressions, and thus cannot be used in complex expressions. As with assignment, in these languages augmented assignment is a form of [right-associative](https://en.wikipedia.org/wiki/Operator_associativity#Right-associativity_of_assignment_operators) assignment.
: For example, `x += 1` is expanded to `x = x + (1)`.[^augmentedassignmentoperatordef-note1]
: Hyponym of [assignment operator](#assignmentoperatordef).

**block** {: #blockdef }
: count noun
: A group of one or more [expressions](#expressiondef), [declarations](https://en.wikipedia.org/wiki/Declaration_(computer_programming)), [statements](#statementdef) or other units of code that are related in such a way as to comprise a whole. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a **block-structured programming language**. Blocks are fundamental to [structured programming](https://en.wikipedia.org/wiki/Structured_programming), where [control structures](https://en.wikipedia.org/wiki/Control_structure) are formed from blocks.  
The function of blocks in programming is to enable groups of statements to be treated as if they were one statement, and to narrow the [lexical scope](https://en.wikipedia.org/wiki/Lexical_scope) of objects such as variables and [subroutines](#subroutinedef) declared in a block so that they do not conflict with those having the same name used elsewhere. In a block-structured programming language, the objects named in outer blocks are visible inside inner blocks, unless they are [masked](https://en.wikipedia.org/wiki/Name_masking) by an object declared with the same name.[^blockdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), blocks are delimited by **curly brackets** (`{` ... `}`).

**Boolean** {: #Booleandef }
: adjective
: Having one of two possible [values](#valuedef) (usually denoted *true* and *false*), intended to represent the two [truth values](https://en.wikipedia.org/wiki/Truth_value) of [logic](https://en.wikipedia.org/wiki/Logic) and [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra).[^Booleandef-note1]

**Boolean data type** {: #Booleandatatypedef }
: proper noun
: A [data type](#datatypedef) limited to [Boolean](#Booleandef) [values](#valuedef). The Boolean data type is primarily associated with [conditional](#conditionaldef) [statements](#statementdef), which allow different actions by changing [control flow](https://en.wikipedia.org/wiki/Control_flow) depending on whether a programmer-specified Boolean *condition* evaluates to true or false.[^Booleandatatypedef-note1]
: For its etymology, it is named after [George Boole](https://en.wikipedia.org/wiki/George_Boole), who first defined an algebraic system of logic in the mid 19th century.[^Booleandatatypedef-note1]
: Hyponym of [data type](#datatypedef).

**condition-controlled loop construct** {: #conditioncontrolledloopconstructdef }
: count noun
: A [loop construct](#loopconstructdef) that [iterates](#iterationdef) while some [condition](#conditiondef) is met.[^conditioncontrolledloopconstructdef-note1]
: Hypernym of [do-while-loop construct](#dowhileloopconstructdef) and [while-loop construct](#whileloopconstructdef).
: Hyponym of [loop construct](#loopconstructdef).

**condition** {: #conditiondef }
: count noun
: A [Boolean](#Booleandef) logical clause or phrase.[^conditiondef-note1]

**conditional** {: #conditionaldef }
: count noun
: An [instruction](https://en.wiktionary.org/wiki/instruction) that [branches](https://en.wiktionary.org/wiki/branch) depending on the truth value of a [condition](#conditiondef) at that point.[^conditionaldef-note1]

**conditional expression** {: #conditionalexpressiondef }
: count noun
: An [expression](#expressiondef) that is similar to an [if-construct](#ifconstructdef), but returns a [value](#valuedef) as a result.[^conditionalexpressiondef-note1]
: 
```
if (condition) then
    (consequent)
else
    (alternative)
```
: 
`(condition) ? (consequent) : (alternative)`
: The two [pseudocode](https://en.wikipedia.org/wiki/Pseudocode) constructs above are equivalent.[^conditionalexpressiondef1]
: Hyponym of [expression](#expressiondef).

**conditional operator** {: #conditionaloperatordef }
: count noun
: A [ternary operator](https://en.wikipedia.org/wiki/Ternary_operator) that is part of the syntax for basic [conditional expressions](#conditionalexpressiondef) in several [programming languages](https://en.wikipedia.org/wiki/Programming_language).[^conditionaloperatordef-note2] A conditional operator is similar to, but not equivalent to, a [logical operator](#logicaloperatordef).[^conditionaloperatordef1] [^conditionaloperatordef-note1] It is commonly referred to as an **inline if (iif)**, or **ternary if**.[^conditionaloperatordef-note2]
: For example, `a ? b : c` evaluates to `b` if the value of `a` is true, and otherwise to `c`.[^conditionaloperatordef-note2]
: In [C++](https://en.wikipedia.org/wiki/C++), the operator is a question mark and a colon (`?:`).
: Hyponym of [operator](#operatordef).

**constant** {: #constantdef }
: count noun
: An [identifier](https://en.wiktionary.org/wiki/identifier) that is [bound](https://en.wiktionary.org/wiki/bound) to an [invariant](https://en.wiktionary.org/wiki/invariant) value; a fixed value given a name to aid in readability of [source code](https://en.wiktionary.org/wiki/source_code).[^constantdef-note1]

**control variable** {: #controlvariabledef }
: count noun
: A [variable](https://en.wikipedia.org/wiki/Variable_(computer_science)) that is used to regulate the [flow of control](https://en.wikipedia.org/wiki/Control_flow) of a program. In definite [iteration](#iterationdef), control variables are variables which are successively assigned (or bound to) [values](#valuedef) from a predetermined sequence of values.[^controlvariabledef1] [^controlvariabledef-note1]

**count-controlled loop construct** {: #countcontrolledloopconstructdef }
: count noun
: A [loop construct](#loopconstructdef) that [iterates](#iterationdef) a certain number of times.[^countcontrolledloopconstructdef-note1]
: Hypernym of [for-loop construct](#forloopconstructdef).
: Hyponym of [loop construct](#loopconstructdef).

**counter** {: #counterdef }
: count noun
: A variable whose contents are [incremented](#incrementdef) or [decremented](#decrementdef)[^counterdef-note1] by a fixed number[^counterdef] to represent the results of [counting](https://en.wikipedia.org/wiki/Counting).[^counterdef-note2]
: Hypernym of [loop counter](#loopcounterdef).

**data type** {: #datatypedef }
: count noun
: An attribute of [data](#datumdef) which tells the [compiler](https://en.wikipedia.org/wiki/Compiler) or [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) how the programmer intends to use the data. Most programming languages support common data types of [real](https://en.wikipedia.org/wiki/Real_number), [integer](https://en.wikipedia.org/wiki/Integer_(computer_science)) and [Boolean](#Booleandatatypedef). A data type constrains the [values](#valuedef) that an [expression](#expressiondef), such as a variable or a [subroutine](#subroutinedef), might take. This data type defines the operations that can be done on the data, the meaning of the data, and the way values of that type can be stored. A type of value from which an expression may take its value.[^datatypedef1] [^datatypedef2] [^datatypedef-note1]
: Hypernym of [Boolean data type](#Booleandatatypedef).

**data validation** {: #datavalidationdef }
: mass noun
: The process of ensuring [data](#datumdef) have undergone [data cleansing](https://en.wikipedia.org/wiki/Data_cleansing) to ensure they have [data quality](https://en.wikipedia.org/wiki/Data_quality), that is, that they are both correct and useful. It uses routines, often called "[validation rules](https://en.wikipedia.org/wiki/Validation_rule)" "validation constraints" or "check routines", that check for correctness, meaningfulness, and security of data that are input to the system.[^datavalidationdef-note1]

**datum** {: #datumdef }
: count noun, plurally **data**
: Any sequence of one or more [symbols](#symboldef) given meaning by one or more specific acts of interpretation.  
A datum requires interpretation to become [information](https://en.wikipedia.org/wiki/Information). To translate it to information, there must be several known factors considered. The factors involved are determined by the creator of the datum and the desired information. The term [metadata](https://en.wikipedia.org/wiki/Metadata) is used to reference the data about the data. Metadata may be implied, specified or given. Data relating to physical events or processes will also have a temporal component. In almost all cases this temporal component is implied. This is the case when a device such as a temperature logger receives data from a temperature [sensor](https://en.wikipedia.org/wiki/Sensor). When the temperature is received it is assumed that the data has a temporal references of "now". So the device records the date, time and temperature together. When the data logger communicates temperatures, it must also report the date and time ([metadata](https://en.wikipedia.org/wiki/Metadata)) for each temperature.  
[Digital data](https://en.wikipedia.org/wiki/Digital_data) is data that is represented using the [binary number](https://en.wikipedia.org/wiki/Binary_number) system of ones (1) and zeros (0), as opposed to [analog](https://en.wikipedia.org/wiki/Analog_signal) representation. In modern (post 1960) computer systems, all data is digital. Data within a computer, in most cases, moves as parallel data. Data moving to or from a computer, in most cases, moves as serial data. See [Parallel communication](https://en.wikipedia.org/wiki/Parallel_communication) and [Serial communication](https://en.wikipedia.org/wiki/Serial_communication). Data sourced from an analog device, such as a temperature sensor, must pass through an "[analog to digital converter](https://en.wikipedia.org/wiki/Analog-to-digital_converter)" or "ADC" (see [Analog-to-digital converter] to convert the analog data to digital data.  
Data representing [quantities](https://en.wikipedia.org/wiki/Quantities), characters, or symbols on which operations are performed by a [computer](https://en.wikipedia.org/wiki/Computer) are [stored](https://en.wikipedia.org/wiki/Data_storage_device) and [recorded](https://en.wikipedia.org/wiki/Record_(computer_science)) on [magnetic](https://en.wikipedia.org/wiki/Magnetic_tape_data_storage), optical, or mechanical recording media, and [transmitted](https://en.wikipedia.org/wiki/Data_transmission) in the form of digital electrical signals.[^datumdef1]  
A [program](https://en.wikipedia.org/wiki/Computer_program) is a set of data that consists of a series of coded software instructions to control the operation of a computer or other machine.[^datumdef2] Physical [computer memory](https://en.wikipedia.org/wiki/Computer_memory) elements consist of an address and a byte/word of data storage. Digital data are often stored in [relational databases](https://en.wikipedia.org/wiki/RDBMS), like [tables](https://en.wikipedia.org/wiki/Table_(database)) or SQL databases, and can generally be represented as abstract key/value pairs.  
Data can be organized in many different types of [data structures](https://en.wikipedia.org/wiki/Data_structures), including arrays, [graphs](https://en.wikipedia.org/wiki/Graph_(data_structure)), and [objects](https://en.wikipedia.org/wiki/Object_(computer_science)). Data structures can store data of many different [types](#datatypedef), including [numbers](https://en.wikipedia.org/wiki/Floating_point), [strings](https://en.wikipedia.org/wiki/String_(computer_science)) and even other [data structures](https://en.wikipedia.org/wiki/Recursive_type). Data pass in and out of computers via [peripheral devices](https://en.wikipedia.org/wiki/Peripheral). The total amount of digital data in 2007 was estimated to be 281 billion [gigabytes](https://en.wikipedia.org/wiki/Gigabytes) (= 281 [exabytes](https://en.wikipedia.org/wiki/Exabytes)).[^datumdef3] [^datumdef4] [Digital data](https://en.wikipedia.org/wiki/Digital_data) comes in these three states: [data at rest](https://en.wikipedia.org/wiki/Data_at_rest), [data in transit](https://en.wikipedia.org/wiki/Data_in_transit) and [data in use](https://en.wikipedia.org/wiki/Data_in_use). [^datumdef-note1]

**decrement** {: #decrementdef }
: verb
: To decrease in [value](#valuedef) by a basic quantity unit, especially by 1.[^decrementdef-note1]

**decrement operator** {: #decrementoperatordef }
: count noun
: A [unary](https://en.wikipedia.org/wiki/Unary_operator) [operator](#operatordef) that decreases the [value](#valuedef) of its [operand](#operanddef) by 1. The operand must have an arithmetic or [pointer](https://en.wikipedia.org/wiki/Pointer_(computer_programming)) [data type](#datatypedef), and must refer to a modifiable [data object](https://en.wikipedia.org/wiki/Data_object). Pointer values are decreased by an amount that makes them point to the next element adjacent in memory.[^decrementoperatordef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), the operator is two [hyphen-minuses](https://en.wikipedia.org/wiki/Hyphen-minus) (`--`), and its operand must be an [lvalue](#lvaluedef) [^decrementoperatordef-note2]. It can be used as a prefix (`--foo`) or a postfix (`foo--`). As a prefix, it decreases the [value](#valuedef) of its operand by 1, and the value of the expression is the resulting decremented value. As a postfix, it decreases the value of its operand by 1, but the value of the expression is the operand's original value *prior* to the decrement operation.[^decrementoperatordef-note1]
: Hyponym of [operator](#operatordef).

**do-while-loop construct** {: #dowhileloopconstructdef }
: count noun
: A [control flow](https://en.wikipedia.org/wiki/Control_flow) construct that executes a [block](#blockdef) of code at least once, and then repeatedly executes the block, or not, depending on a given [Boolean](#Booleandef) [condition](#conditiondef) at the end of the block. Because the do-while-loop construct checks the condition after the block is executed, the control structure is often also known as a **posttest loop**. Compare this with the [*while* loop construct](#whileloopconstructdef), which tests the condition *before* the code within the block is executed.[^dowhileloopconstructdef-note1]
: Hyponym of [condition-controlled loop construct](#conditioncontrolledloopconstructdef).

**else-clause** {: #elseclausedef }
: count noun
: Part of an [if-construct](#ifconstructdef) following an [if-clause](#ifclausedef).[^iforelseorelseiforclausedef-note1] [^iforelseorelseiforclausedef-note2]
: 
```
else
    (alternative)
```
: Meronym of [if-construct](#ifconstructdef).

**else-if-clause** {: #elseifclausedef }
: count noun
: Part of an [if-construct](#ifconstructdef) following an [if-clause](#ifclausedef).[^iforelseorelseiforclausedef-note1] [^iforelseorelseiforclausedef-note2]
: 
```
else if (condition) then
    (consequent 2)
```
: Meronym of [if-construct](#ifconstructdef).

**entity** {: #entitydef }
: count noun
: Anything that claims independent [existence](https://en.wikipedia.org/wiki/Existence), as opposed to merely being part of a whole. It can exist as a subject or as an object, actually or potentially, concretely or abstractly.[^entitydef-note1]

**entry point** {: #entrypointdef }
: count noun
: The point in a program where the first instructions are executed, and where the program has access to [command line arguments](https://en.wikipedia.org/wiki/Command_line_arguments).[^entrypointdef-note1] [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**expression** {: #expressiondef }
: A combination of one or more [constants](https://en.wikipedia.org/wiki/Constant_(programming)), [variables](https://en.wikipedia.org/wiki/Variable_(programming)), [operators](https://en.wikipedia.org/wiki/Operator_(programming)), and [subroutines](#subroutinedef) that a [programming language](https://en.wikipedia.org/wiki/Programming_language) interprets (according to its particular [rules of precedence](https://en.wikipedia.org/wiki/Order_of_operations) and of [association](#associativitydef)) and computes to produce ("to return", in a [stateful](https://en.wikipedia.org/wiki/State_(computer_science)) environment) another [value](#valuedef). This process, as for [mathematical expressions](https://en.wikipedia.org/wiki/Mathematical_expression), is called evaluation. In simple settings, the [resulting value](https://en.wikipedia.org/wiki/Return_type) is usually one of various [primitive types](https://en.wikipedia.org/wiki/Primitive_data_type), such as numerical, [string](https://en.wikipedia.org/wiki/String_(computer_science)), and [logical](https://en.wikipedia.org/wiki/Boolean_expression); in more elaborate settings, it can be an arbitrary [complex data type](https://en.wikipedia.org/wiki/Complex_data_type).[^expressiondef-note1]
: For example, `2+3` is an arithmetic and programming expression which evaluates to `5`. A variable is an expression because it denotes a value in memory, so `y+6` is an expression. An example of a relational expression is `4≠4`, which evaluates to `false`.[^expressiondef-note1] [^expressiondef1] [^expressiondef2]
: Hypernym of [conditional expression](#conditionalexpressiondef) and [relational expression](#relationalexpressiondef).

**flag** {: #flagdef }
: count noun
: A variable or memory location that stores a [Boolean](#Booleandef) [value](#valuedef), typically either recording the fact that a certain event has occurred or requesting that a certain optional action take place.[^flagdef-note1]

**for-loop construct** {: #forloopconstructdef }
: count noun
: A [control flow](https://en.wikipedia.org/wiki/Control_flow) construct that allows a [block](#blockdef) of code to be executed repeatedly, typically when the number of [iterations](#iterationdef) is known before entering the loop. A for-loop construct can be thought of as shorthand for a [while-loop construct](#whileloopconstructdef). A for-loop construct has two parts: a **for-loop header** specifying the iteration, and a **for-loop body** which is executed once per iteration. The header often declares an explicit [loop counter](#loopcounterdef), which allows the body to know which iteration is being executed.[^forloopconstructdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), the for-loop construct is a **pretest-loop construct**.[^forloopconstructdef1] [^forloopconstructdef-note2]
: Hyponym of [count-controlled loop construct](#countcontrolledloopconstructdef).

**if-clause** {: #ifclausedef }
: count noun
: Part of an [if-construct](#ifconstructdef).[^iforelseorelseiforclausedef-note1] [^iforelseorelseiforclausedef-note2]
: 
```
if (condition) then
    (consequent)
```
: Meronym of [if-construct](#ifconstructdef).

**if-construct** {: #ifconstructdef }
: count noun
: A [conditional](#conditionaldef) [construct](https://en.wikipedia.org/wiki/Data_structure) made up of an [if-clause](#ifclausedef) and optionally one or more [else-if-clauses](#elseifclausedef) and an [else-clause](#elseclausedef).
: 
```
if (condition) then
    (consequent)
else
    (alternative)
end if
```
: In the [pseudocode](https://en.wikipedia.org/wiki/Pseudocode) construct above, `(condition)` represents a [conditional](#conditionaldef) [statement](#statementdef), `(consequent)` represents an [expression](#expressiondef) or [statement](#statementdef), and `(alternative)` represents an [expression](#expressiondef) or [statement](#statementdef).  
When an [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) finds an `if`, it expects a [condition](#conditiondef) (`(condition)`) and evaluates that condition. If the condition is `true`, the statements following the `then` (`(consequent)`) are executed. Otherwise, the execution continues in the following clause, either in the [else clause](#elseclausedef) (which is usually optional, and in this case contains `(alternative)`) or, if there is no else clause, then after the `end if`. After either clause has been executed, [control](https://en.wikipedia.org/wiki/Control_flow) returns to the point after the `end if`.[^ifconstructdef-note1]  
: 
```
if (condition) then
    (consequent 1)
else if (condition) then
    (consequent 2)
else
    (alternative)
end if
```
: In the [pseudocode](https://en.wikipedia.org/wiki/Pseudocode) construct above, `else if` is added, making it possible to combine several [conditionals](#conditionaldef). Only the statements following the first `(condition)` that is found to be true will be executed. All other statements will be skipped.[^ifconstructdef-note2]
: Holonym of [else-clause](#elseclausedef), [else-clause](#elseifclausedef), and [if-clause](#ifclausedef).

**increment** {: #incrementdef }
: verb
: To increase in [value](#valuedef) by a basic quantity unit, especially by 1.[^incrementdef-note1]

**increment operator** {: #incrementoperatordef }
: count noun
: A [unary](https://en.wikipedia.org/wiki/Unary_operator) [operator](#operatordef) that increases the [value](#valuedef) of its operand by 1. The [operand](#operanddef) must have an arithmetic or [pointer](https://en.wikipedia.org/wiki/Pointer_(computer_programming)) [data type](#datatypedef). Pointer values are increased by an amount that makes them point to the next element adjacent in memory.[^incrementoperatordef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), the operator is two [plus signs](https://en.wikipedia.org/wiki/Plus_and_minus_signs#Plus_sign) (`++`), and its operand must be an [lvalue](#lvaluedef) [^incrementoperatordef-note2]. It can be used as a prefix (`++foo`) or a postfix (`foo++`). As a prefix, it increases the [value](#valuedef) of its operand by 1, and the value of the expression is the resulting incremented value. As a postfix, it increases the value of its operand by 1, but the value of the expression is the operand's original value *prior* to the increment operation.[^incrementoperatordef-note1]
: Hyponym of [operator](#operatordef).

**iteration** {: #iterationdef }
: count noun
: A single repetition of the [statements](#statementdef) within a repetitive process, especially a [loop construct](#loopconstructdef).[^iterationdef-note1]

**leading** {: #leadingdef }
: adjective
: Occuring at the beginning[^leadingdef] of a line.
: ⋅⋅For example, this line contains two **leading** dots.

**literal** {: #literaldef }
: count noun
: A notation for representing a fixed value in source code.[^literaldef-note1]

**logical operator** {: #logicaloperatordef }
: count noun
: An [operator](#operatordef) used to connect two or more [relational expressions](#relationalexpressiondef)[^logicaloperatordef-note4], such that the value of the expression produced depends only on that of the relational expressions. It is also called a **logical connective**, **sentential connective**, or **sentential operator**.  
The most common logical operators are **[binary](https://en.wikipedia.org/wiki/Binary_relation) operators** (also called **[dyadic](https://en.wikipedia.org/wiki/Dyadics) connectives**) which join two sentences. Also commonly, [negation](https://en.wikipedia.org/wiki/Negation) is considered to be a **[unary](https://en.wikipedia.org/wiki/Unary_function) operator**.[^logicaloperatordef-note1] [^logicaloperatordef-note2]
: In [C++](https://en.wikipedia.org/wiki/C++), the [logical negation (NOT)](https://en.wikipedia.org/wiki/Negation) reverses the truth of an expression.[^logicaloperatordef-note4] The operator is an exclamation mark (`!`), for example `!a` means **not** `a`.[^logicaloperatordef-note3]
: In [C++](https://en.wikipedia.org/wiki/C++), the [logical AND](https://en.wikipedia.org/wiki/Logical_conjunction) operator connects the logic of multiple expressions using [short-circuit evaluation](https://en.wikipedia.org/wiki/Short-circuit_evaluation).[^logicaloperatordef-note4] The operator is two ampersands (`&&`), for example `a && b` means `a` **and** `b`.[^logicaloperatordef-note3]
: In [C++](https://en.wikipedia.org/wiki/C++), the [logical inclusive OR](https://en.wiktionary.org/wiki/inclusive_or) operator connects the logic of multiple expressions using [short-circuit evaluation](https://en.wikipedia.org/wiki/Short-circuit_evaluation).[^logicaloperatordef-note4] The operator is two pipe characters (`||`), for example `a || b` means `a` **or** `b`.[^logicaloperatordef-note3]
: Hyponym of [operator](#operatordef).

**loop construct** {: #loopconstructdef }
: count noun
: A construct, made up of one or more [statements](#statementdef), that may be carried out multiple successive times in a sequence of [iterations](#iterationdef). The statements “inside” the loop construct (also known as the **body** of the loop construct) are executed in one of four possible ways: [a specified number of times](#countcontrolledloopconstructdef), [once for each of a collection of items](https://en.wikipedia.org/wiki/Foreach_loop), [while some condition is met](#conditioncontrolledloopconstructdef), or [indefinitely](https://en.wikipedia.org/wiki/Infinite_loop).[^loopconstructdef-note1]
: A loop construct has a [loop counter](#loopcounterdef).
: Hypernym of [condition-controlled loop construct](#conditioncontrolledloopconstructdef) and [count-controlled loop construct](#countcontrolledloopconstructdef).

**loop counter** {: #loopcounterdef }
: count noun
: A [counter](#counterdef) that controls the [iterations](#iterationdef) of a [loop construct](#loopconstructdef). Most uses of a loop construct result in the loop counter taking on a range of integer values in some orderly sequences (for example, starting at 0 and ending at 10 in [increments](#incrementdef) of 1). Loop counters change with each iteration of a loop, providing a unique value for each individual iteration. The loop counter is used to decide when the loop should terminate and for the program flow to continue to the next instruction after the loop.[^loopcounterdef-note1] A loop counter must be [initialized](https://en.wikipedia.org/wiki/Initialization_(programming)) before it is used.[^loopcounterdef-note2]
: Hyponym of [counter](#counterdef).

**lvalue** {: #lvaluedef }
: count noun
: A [value](#valuedef) that refers to a [data object](https://en.wikipedia.org/wiki/Data_object) that persists beyond a single [expression](#expressiondef).[^lvaluedef2] In many languages, notably the [C family](https://en.wikipedia.org/wiki/C_programming_language), an lvalue has a [storage address](https://en.wikipedia.org/wiki/Memory_address) that is programmatically accessible to the running program (for example, via some address-of operator like `&` in C/C++), meaning that it is a variable or dereferenced reference to a certain memory location.[^lvaluedef-note2]
: For its etymology, it comes from *[L](https://en.wiktionary.org/wiki/L#English)* +‎ *[value](#valuedef)*, where *L* stands for *left-hand side*, deriving from the typical mode of evaluation on the left and [right](#rvaluedef) hand side of an [assignment](#assignmentconstructdef) [statement](#statementdef).[^lvaluedef-note2] In context of the [C programming language](https://en.wiktionary.org/wiki/C#English-programming_language) it is usually expanded as *[locator](https://en.wiktionary.org/wiki/locator#English)* *value*.[^lvaluedef-note1]
: In [C](https://en.wikipedia.org/wiki/C_(programming_language)), if an lvalue refers to a modifiable data object, it is called a **modifiable lvalue**.[^lvaluedef1]
: Hyponym of [value](#valuedef).

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
: Hypernym of [assignment operator](#assignmentoperatordef), [conditional operator](#conditionaloperatordef), [decrement operator](#decrementoperatordef), [increment operator](#incrementoperatordef), [logical operator](#logicaloperatordef), and [relational operator](#relationaloperatordef).

**relational expression** {: #relationalexpressiondef }
: count noun
: An [expression](#expressiondef) created using a [relational operator](#relationaloperatordef), also called a **condition**.[^relationalexpressiondef-note1]
: Hyponym of [expression](#expressiondef).

**relational operator** {: #relationaloperatordef }
: count noun
: A [programming language](https://en.wikipedia.org/wiki/Programming_language) construct or [operator](#operatordef) that tests or defines some kind of [relation](https://en.wikipedia.org/wiki/Relation_(mathematics)) between [two entities](https://en.wikipedia.org/wiki/Binary_function). These include numerical [equality](https://en.wikipedia.org/wiki/Equality_(mathematics)) (*e.g.*, [5 = 5]) and [inequality](https://en.wikipedia.org/wiki/Inequality_(mathematics)) (*e.g.*, [4 ≥ 3]). Relational operators can be seen as special cases of logical [predicates](https://en.wikipedia.org/wiki/Predicate_(mathematical_logic)).[^relationaloperatordef-note1]
: Hyponym of [operator](#operatordef).

**running total** {: #runningtotaldef }
: A [summation](https://en.wikipedia.org/wiki/Summation) of a sequence of numbers which is updated each time a new number is added to the sequence, by adding the value of the new number to the previous running total. Another term for it is [partial sum](https://en.wikipedia.org/wiki/Series_(mathematics)#Definition).[^runningtotaldef-note1]

**rvalue** {: #rvaluedef }
: count noun
: A temporary [value](#valuedef) that does not persist beyond the [expression](#expressiondef) that uses it.[^rvaluedef1]
: For its etymology, it comes from *[R](https://en.wiktionary.org/wiki/R#English)* +‎ *[value](#valuedef)*, where *R* stands for *right-hand side*, deriving from the typical mode of evaluation on the [left](#lvaluedef) and right hand side of an [assignment](#assignmentconstructdef) [statement](#statementdef).[^rvaluedef-note1]
: Hyponym of [value](#valuedef).

**separator** {: #separatordef }
: count noun
: A token that demarcates boundaries between two separate [statements](#statementdef). A separator is also known as a **punctuator**.[^separatordef-note1]

**statement** {: #statementdef }
: count noun
: A syntactic unit of an [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [programming language](https://en.wikipedia.org/wiki/Programming_language) that changes the program state or performs some kind of action.[^statementdef1] [^statementdef-note2] It also has meaning.[^statementdef-note3] A program written in such a language is formed by a sequence of one or more statements. A statement may have internal components (e.g., [expressions](#expressiondef)). Boundaries between statements are demarcated by [separators](#separatordef), and the end of a statement is demarcated by a [terminator](#terminatordef). [^statementdef-note1]

**subroutine** {: #subroutinedef }
: count noun
: A sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed. It may be defined within a single program, or separately in a [library](https://en.wikipedia.org/wiki/Library_(computer_science)) that can be used by many programs. In different programming languages, a subroutine may be called a **procedure**, a **function**, a **routine**, a [method](https://en.wikipedia.org/wiki/Method_(computing)), or a **subprogram**. The generic term **callable unit** is sometimes used.[^subroutinedef1] [^subroutinedef-note1]
: A subroutine has [arity](#aritydef).

**switch construct** {: #switchconstructdef }
: count noun
A type of selection control mechanism used to allow the value of a [variable](https://en.wikipedia.org/wiki/Variable_(programming)) or [expression](#expressiondef) to change the [control flow](https://en.wikipedia.org/wiki/Control_flow) of program execution via search and map.[^switchconstructdef-note1]

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
: Hypernym of [lvalue](#lvaluedef) and [rvalue](#rvaluedef).

**while-loop construct** {: #whileloopconstructdef }
: count noun
: A [control flow](https://en.wikipedia.org/wiki/Control_flow) construct that allows a [block](#blockdef) of code to be executed repeatedly based on a given [Boolean](#Booleandef) [condition](#conditiondef). It can be thought of as a repeating [if-construct](#ifconstructdef). It consists of a [block](#blockdef) of code and a [condition](#conditiondef)/[expression](#expressiondef).[^whileloopconstructdef1] The condition/expression is evaluated, and if the condition/expression is *true*,[^whileloopconstructdef1] the code within the block is executed. This repeats until the condition/expression becomes [false](https://en.wikipedia.org/wiki/False_(logic)). Because the *while* loop construct checks the condition/expression before the block is executed, the control structure is often also known as a **pretest-loop construct**. Compare this with the [*do while* loop construct](#dowhileloopconstructdef), which tests the condition/expression *after* the loop has executed.[^whileloopconstructdef-note1]
: 
```
int x = 0;
while (x < 5) 
{
    printf ("x = %d\n", x);
    x++;
}
```
: For example, the code fragment above first checks whether `x` is less than 5, which it is, so then the loop body within the curly brackets is entered, where the `printf` [subroutine](#subroutinedef) is run and `x` is [incremented](#incrementdef) by 1. After completing all the statements in the loop body, the condition, (x < 5), is checked again, and the loop is executed again, this process repeating until the [variable](https://en.wikipedia.org/wiki/Variable_(programming)) `x` has the value 5.  
: 
```
while (true)
{
    //do complicated stuff
    if (someCondition) break;
    //more stuff
}
```
: The code fragment above shows that it is possible, and in some cases desirable, for the condition to *always* evaluate to true, creating an [infinite loop](https://en.wikipedia.org/wiki/Infinite_loop). When such a loop is created intentionally, there is usually another control structure (such as a [break](https://en.wikipedia.org/wiki/Control_flow) statement) that controls termination of the loop.  
The code fragments above are written in the [C programming language](https://en.wikipedia.org/wiki/C_(programming_language)) (as well as [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)),[^whileloopconstructdef2] [Objective-C](https://en.wikipedia.org/wiki/Objective-C), and [C++](https://en.wikipedia.org/wiki/C++), which [use the same syntax](https://en.wikipedia.org/wiki/Polyglot_(computing)) in this case).
: Hyponym of [condition-controlled loop construct](#conditioncontrolledloopconstructdef).

[^whileloopconstructdef1]: ["The while and do-while Statements (The Java™ Tutorials > Learning the Java Language > Language Basics)"](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html). *Dosc.oracle.com*. Retrieved 2016-10-21.
[^whileloopconstructdef2]: ["while (C# reference)"](http://msdn.microsoft.com/en-us/library/2aeyhxcd.aspx). *Msdn.microsoft.com*. Retrieved 2016-10-21.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [Assignment (computer science)](https://en.wikipedia.org/w/index.php?title=Assignment_(computer_science)&oldid=882172626)
- [Assignment operator (C++)](https://en.wikipedia.org/w/index.php?title=Assignment_operator_(C%2B%2B)&oldid=873288112)
- [Augmented assignment](https://en.wikipedia.org/w/index.php?title=Augmented_assignment&oldid=879453644)
- [Block (programming)](https://en.wikipedia.org/w/index.php?title=Block_(programming)&oldid=877703688)
- [Boolean data type](https://en.wikipedia.org/w/index.php?title=Boolean_data_type&oldid=876857392)
- [Comparison of programming languages (syntax)§Blocks](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Blocks)
- [Comparison of programming languages (syntax)§Statements](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Statements)
- [Conditional (computer programming)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Conditional (computer programming)§Else if](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=882062344#Else_if)
- [Conditional (computer programming)§If–then(–else)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Conditional (computer programming)§If–then–else expressions](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=882062344#If%E2%80%93then%E2%80%93else_expressions)
- [Conditional operator](https://en.wikipedia.org/w/index.php?title=Conditional_operator&oldid=846889637)
- [Control flow§Loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Loops)
- [Control flow§Condition-controlled loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Condition-controlled_loops)
- [Control flow§Count-controlled loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Count-controlled_loops)
- [Control variable (programming)](https://en.wikipedia.org/w/index.php?title=Control_variable_(programming)&oldid=868177931)
- [Data (computing)](https://en.wikipedia.org/w/index.php?title=Data_(computing)&oldid=881080086)
- [Data type](https://en.wikipedia.org/w/index.php?title=Data_type&oldid=879519751)
- [Data validation](https://en.wikipedia.org/w/index.php?title=Data_validation&oldid=880736882)
- [Do while loop](https://en.wikipedia.org/w/index.php?title=Do_while_loop&oldid=870917166)
- [Entity](https://en.wikipedia.org/w/index.php?title=Entity&oldid=880867147)
- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=881544189)
- [Expression (computer science)](https://en.wikipedia.org/w/index.php?title=Expression_(computer_science)&oldid=878391104)
- [For loop](https://en.wikipedia.org/w/index.php?title=For_loop&oldid=876221986).
- [For loop§Loop counters](https://en.wikipedia.org/w/index.php?title=For_loop&oldid=876221986#Loop_counters)
- [Increment and decrement operators](https://en.wikipedia.org/w/index.php?title=Increment_and_decrement_operators&oldid=879445217)
- [Lexical analysis§Token](https://en.wikipedia.org/w/index.php?title=Lexical_analysis&oldid=872271284).
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Logical connective](https://en.wikipedia.org/w/index.php?title=Logical_connective&oldid=881652068)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Operators in C and C++§Logical operators](https://en.wikipedia.org/w/index.php?title=Operators_in_C_and_C++&oldid=879923250#Logical_operators)
- [Nesting (computing)](https://en.wikipedia.org/w/index.php?title=Nesting_(computing)&oldid=877015415)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)
- [Relational operator](https://en.wikipedia.org/w/index.php?title=Relational_operator&oldid=874050383)
- [Running total](https://en.wikipedia.org/w/index.php?title=Running_total&oldid=855615611)
- [Statement (computer science)](https://en.wikipedia.org/w/index.php?title=Statement_(computer_science)&oldid=863825665)
- [Symbol rate§Symbols](https://en.wikipedia.org/w/index.php?title=Symbol_rate&oldid=870702760#Symbols)
- [Subroutine](https://en.wikipedia.org/w/index.php?title=Subroutine&oldid=879018923)
- [Switch statement](https://en.wikipedia.org/w/index.php?title=Switch_statement&oldid=866307445)
- [Value (computer science)§Assignment: l-values and r-values](https://en.wikipedia.org/w/index.php?title=Value_(computer_science)&oldid=803728831)
- [While loop](https://en.wikipedia.org/w/index.php?title=While_loop&oldid=881424645)
- [?:](https://en.wikipedia.org/w/index.php?title=%3F:&oldid=880334289)

on Wikipedia, with changes made, and:

- [arity](https://en.wiktionary.org/w/index.php?title=arity&oldid=50758406)
- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [condition](https://en.wiktionary.org/w/index.php?title=condition&oldid=51410719)
- [conditional](https://en.wiktionary.org/w/index.php?title=conditional&oldid=51276861)
- [constant](https://en.wiktionary.org/w/index.php?title=constant&oldid=51246036)
- [counter](https://en.wiktionary.org/w/index.php?title=counter&oldid=51103193)
- [decrement§verb](https://en.wiktionary.org/w/index.php?title=decrement&oldid=50276969#Verb)
- [flag](https://en.wiktionary.org/w/index.php?title=flag&oldid=51372941)
- [increment§verb](https://en.wiktionary.org/w/index.php?title=increment&oldid=51035067#Verb)
- [iteration](https://en.wiktionary.org/w/index.php?title=iteration&oldid=51175255)
- [lvalue](https://en.wiktionary.org/w/index.php?title=lvalue&oldid=50837189)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)
- [vacuous](https://en.wiktionary.org/w/index.php?title=vacuous&oldid=47613271)

on Wiktionary, with changes made.

[^runningtotaldef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Running_total).
[^accumulatordef-note1]: This definition is based on [an answer on Stack Overflow by Alberto Moriconi](https://stackoverflow.com/questions/12983063/what-is-the-difference-between-a-counter-and-an-accumulator/12983603#12983603) and on information from page 257 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^aritydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/arity), except for the removal of the words “[arguments](https://en.wiktionary.org/wiki/argument)” and “[operation](https://en.wiktionary.org/wiki/operation)”, which do not seem to apply in a computer science context.
[^assignmentconstructdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Assignment_(computer_science)).
[^assignmentoperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Assignment_operator_(C++)).
[^associativitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity).
[^atomicitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity).
[^augmentedassignmentoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Augmented_assignment).
[^blockdef-note1]: This definition is based on [Wikipedia's definition of a block as a page](https://en.wikipedia.org/wiki/Block_(programming)) and [as a section of a page](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Blocks).
[^Booleandatatypedef-note1]: This definition is based on [Wikipedia's definition of Boolean data type](https://en.wikipedia.org/wiki/Boolean_data_type) and [Data type](https://en.wikipedia.org/wiki/Data_type).
[^Booleandef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Boolean_data_type).
[^conditionaldef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/conditional).
[^conditionalexpressiondef1]: Based on information from page 199 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^conditionaloperatordef1]: Cogwheel. ["What is the difference between logical and conditional /operator/"](https://stackoverflow.com/questions/3154132/what-is-the-difference-between-logical-and-conditional-and-or-in-c). *Stack Overflow.* Retrieved 9 April 2015.
[^conditionaloperatordef-note1]: This definition is based on a definition from [Wikipedia](https://en.wikipedia.org/wiki/Conditional_operator).
[^conditionaloperatordef-note2]: This definition is based on a definition from [Wikipedia](https://en.wikipedia.org/wiki/%3F:).
[^conditioncontrolledloopconstructdef-note1]: This definition is loosely based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Control_flow#Condition-controlled_loops).
[^conditiondef-note1]: This definition is based on definitions from [Wiktionary](https://en.wiktionary.org/wiki/condition) and [Wikipedia](https://en.wikipedia.org/wiki/Conditional_(computer_programming)).
[^constantdef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/constant).
[^controlvariabledef1]: Watt, David A. (2004). *Programming Language Design Concepts.* Wiley. pp. 84–85.
[^controlvariabledef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Control_variable_(programming)).
[^countcontrolledloopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Control_flow#Count-controlled_loops).
[^counterdef]: <https://stackoverflow.com/questions/12983063/what-is-the-difference-between-a-counter-and-an-accumulator/12983603#12983603>
[^counterdef-note1]: Based on information from page 241 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^counterdef-note2]: This definition is based on a definition from [Wiktionary](https://en.wiktionary.org/wiki/counter).
[^datatypedef1]: [type](http://foldoc.org/type) at the *[Free On-line Dictionary of Computing](https://en.wikipedia.org/wiki/Free_On-line_Dictionary_of_Computing)*
[^datatypedef2]: [Shaffer, C. A. (2011). *Data Structures & Algorithm Analysis in C++* (3rd ed.). Mineola, NY: Dover. 1.2. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [978-0-486-48582-9](https://en.wikipedia.org/wiki/Special:BookSources/978-0-486-48582-9).
[^datatypedef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Data_type).
[^datavalidationdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Data_validation).
[^datumdef1]: ["data"](http://oxforddictionaries.com/definition/american_english/data). *Oxford Dictionaries*. [Archived](https://web.archive.org/web/20121006073603/http://oxforddictionaries.com/definition/american_english/data) from the original on 2012-10-06. Retrieved 2012-10-11.
[^datumdef2]: ["computer program"](http://www.encyclopedia.com/topic/computer_program.aspx#2). *The Oxford Pocket Dictionary of Current English*. [Archived](https://web.archive.org/web/20111128202415/http://www.encyclopedia.com/topic/computer_program.aspx#2) from the original on 2011-11-28. Retrieved 2012-10-11.
[^datumdef3]: Paul, Ryan (March 12, 2008). ["Study: amount of digital info > global storage capacity"](https://arstechnica.com/news.ars/post/20080312-study-amount-of-digital-info-global-storage-capacity.html). Ars Technics. [Archived](https://web.archive.org/web/20080313111238/http://arstechnica.com/news.ars/post/20080312-study-amount-of-digital-info-global-storage-capacity.html) from the original on March 13, 2008. Retrieved 2008-03-12.
[^datumdef4]: Gantz, John F.; et al. (2008). ["The Diverse and Exploding Digital Universe"](https://web.archive.org/web/20080311234210/http://www.emc.com/leadership/digital-universe/expanding-digital-universe.htm). International Data Corporation via EMC. Archived from [the original](http://www.emc.com/leadership/digital-universe/expanding-digital-universe.htm) on 2008-03-11. Retrieved 2008-03-12.
[^datumdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Data_(computing)).
[^decrementoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Increment_and_decrement_operators).
[^decrementoperatordef-note2]: Based on information from page 231 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^decrementdef-note1]: This definition is based on [Wiktionary's definition of “increment”](https://en.wiktionary.org/wiki/increment#Verb) and [Wiktionary's definition of “decrement”](https://en.wiktionary.org/wiki/decrement#Verb).
[^dowhileloopconstructdef-note1]: This definition is based on [Wikipedia's definition of “Do while loop”](https://en.wikipedia.org/wiki/Do_while_loop) and [Wikipedia's definition of “While loop”](https://en.wikipedia.org/wiki/While_loop).
[^entitydef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entity).
[^entrypointdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point), with some rewording.
[^expressiondef1]: [Javascript expressions, Mozilla](https://developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Expressions) Accessed July 6, 2009]
[^expressiondef2]: [Programming in C](https://www.cs.drexel.edu/~rweaver/COURSES/ISTC-2/TOPICS/expr.html) Accessed July 6, 2009
[^expressiondef-note1]: This definition is similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Expression_(computer_science)), with changes made.
[^flagdef-note1]: This definition is based on [Wiktionary's definition](https://en.wiktionary.org/wiki/flag#Noun).
[^forloopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/For_loop).
[^forloopconstructdef-note2]: Based on information from page 251 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^conditionalexpressiondef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then%E2%80%93else_expressions).
[^forloopconstructdef1]: <https://en.cppreference.com/w/cpp/language/for>
[^iforelseorelseiforclausedef-note1]: This definition is based on [an answer on Stack Overflow by tvanfosson](https://stackoverflow.com/questions/4877903/the-term-clause-in-the-context-of-programming/4877948#4877948).
[^iforelseorelseiforclausedef-note2]: This definition is based on [an answer on Software Engineering Stack Exchange by Robert Harvey](https://softwareengineering.stackexchange.com/questions/234331/in-an-if-statement-what-are-an-if-clause-and-a-then-clause/234337#234337).
[^ifconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then(%E2%80%93else)).
[^ifconstructdef-note2]: This definition is based on [Wikipedia's definition]https://en.wikipedia.org/wiki/Conditional_(computer_programming)#Else_if)
[^incrementdef-note1]: This definition is based on [Wiktionary's definition of “increment”](https://en.wiktionary.org/wiki/increment#Verb) and [Wiktionary's definition of “decrement”](https://en.wiktionary.org/wiki/decrement#Verb).
[^incrementoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Increment_and_decrement_operators).
[^incrementoperatordef-note2]: Based on information from page 231 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^iterationdef-note1]: This definition is based on [Wiktionary's definition](https://en.wiktionary.org/wiki/iteration).
[^leadingdef]: <https://stackoverflow.com/questions/959215/how-do-i-remove-leading-whitespace-in-python>
[^literaldef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Literal_(computer_programming)).
[^logicaloperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Logical_connective).
[^logicaloperatordef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Operators_in_C_and_C++#Logical_operators).
[^logicaloperatordef-note3]: Requires [`iso646.h`](https://en.wikipedia.org/wiki/Iso646.h) in C. See [C++ operator synonyms](https://en.wikipedia.org/wiki/Operators_in_C_and_C%2B%2B#C.2B.2B_operator_synonyms)
[^logicaloperatordef-note4]: Based on information from pages 182-187 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^loopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Control_flow#Loops).
[^loopcounterdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/For_loop#Loop_counters).
[^loopcounterdef-note2]: Based on information from page 242 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^lvaluedef1]: <https://www.geeksforgeeks.org/lvalue-and-rvalue-in-c-language/>
[^lvaluedef2]: ["Lvalues and Rvalues (Visual C++)"](https://msdn.microsoft.com/en-us/library/f90831hc.aspx). *Microsoft Developer Network.* Retrieved 3 September 2016.
[^lvaluedef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/lvalue).
[^lvaluedef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Value_(computer_science)#Assignment:_l-values_and_r-values).
[^nestdef-note1]: This definition is loosely based on [Wikipedia's definition of “nesting”](https://en.wikipedia.org/wiki/Nesting_(computing)).
[^octetdef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)), except for the removal of the phrase “in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications)”.
[^operanddef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science).
[^operatordef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming), except for modification of the grammatical number (plural to singular).
[^operatordef-note2]: Based on [information from Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity).
[^relationalexpressiondef-note1]: This definition similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^relationaloperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^rvaluedef1]: ["Lvalues and Rvalues (Visual C++)"](https://msdn.microsoft.com/en-us/library/f90831hc.aspx). *Microsoft Developer Network.* Retrieved 3 September 2016.
[^rvaluedef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Value_(computer_science)#Assignment:_l-values_and_r-values).
[^separatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement separator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^statementdef1]: ["statement"](http://www.webopedia.com/TERM/S/statement.html). webopedia. Retrieved 2015-03-03.
[^statementdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Statement_(computer_science)).
[^statementdef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then%E2%80%93else_expressions).
[^statementdef-note3]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then(%E2%80%93else)).
[^subroutinedef1]: [U.S. Election Assistance Commission](https://en.wikipedia.org/wiki/Election_Assistance_Commission "Election Assistance Commission") (2007). ["Definitions of Words with Special Meanings"](https://web.archive.org/web/20121208084203/http://www.eac.gov/vvsg/glossary.aspx). *[Voluntary Voting System Guidelines](https://en.wikipedia.org/wiki/Voluntary_Voting_System_Guidelines "Voluntary Voting System Guidelines")*. Archived from [the original](http://www.eac.gov/vvsg/glossary.aspx) on 2012-12-08. Retrieved 2013-01-14.
[^subroutinedef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Subroutine), with some rewording.
[^switchconstructdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Switch_statement).
[^symboldef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Symbol_rate#Symbols).
[^terminatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement terminator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
[^truncatedef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate).
[^vacuousdef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/vacuous).
[^valuedef-note1]: This definition is based on the definition proposed on [an answer on Stack Overflow](https://stackoverflow.com/questions/3300726/what-is-a-value-in-the-context-of-programming/3301073#3301073).
[^whileloopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/While_loop).
