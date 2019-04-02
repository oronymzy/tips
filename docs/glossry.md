# Glossary
These are concepts I find especially confusing, ambiguous, or difficult to remember.

**abstraction** {: #abstractiondef }
: mass noun
: A process or result of generalization, removal of properties, or distancing of ideas from objects.[^abstractiondef-note1]

**calculate** {: #calculatedef }
: verb
: To determine mathematically in the case of a number or amount, or in the case of an abstract problem to deduce the answer using logic, reason or common sense.[^calculatedef1] [^calculatedef-note1]

**greenfield project** {: #greenfieldprojectdef }
: count noun
: A project that lacks constraints imposed by prior work.
: The analogy is to that of construction on [greenfield land](https://en.wikipedia.org/wiki/Greenfield_land) where there is no need to work within the constraints of existing buildings or infrastructure.[^greenfieldprojectdef1] [^greenfieldprojectdef-note1]

**intelligence** {: #intelligencedef }
: mass noun
: The ability to perceive or infer [information](https://en.wikipedia.org/wiki/Information), and to retain it as [knowledge](https://en.wikipedia.org/wiki/Knowledge) to be applied towards adaptive behaviors within an environment or context.[^intelligencedef-note1]

**obsolescence** {: #obsolescencedef }
: mass noun
: The state of being which occurs when an object, service, or practice is no longer wanted even though it may still be in good working order.[^obsolescencedef-note1]

**playback** {: #playbackdef }
: mass noun
: The [replaying](https://en.wiktionary.org/wiki/replay) of something previously recorded, especially [sound](https://en.wiktionary.org/wiki/sound) or moving [images](https://en.wiktionary.org/wiki/image).[^playbackdef-note1]

**rabbit hole** {: #rabbitholedef }
: count noun
: A [time-consuming](https://en.wiktionary.org/wiki/time-consuming) [tangent](https://en.wiktionary.org/wiki/tangent) or [detour](https://en.wiktionary.org/wiki/detour), often from which it is difficult to extricate oneself.[^rabbitholedef-note1]

**system** {: #systemdef }
: count noun
: A group of interacting or interrelated entities that form a unified whole.[^systemdef1] A system is delineated by its spatial and temporal boundaries, surrounded and influenced by its environment, described by its structure and purpose and expressed in its functioning.[^systemdef-note1]

**vacuous** {: #vacuousdef }
: adjective
: Empty; void; lacking meaningful [content](https://en.wiktionary.org/wiki/content).[^vacuousdef-note1]

## computer science glossary

**accumulator** {: #accumulatordef }
: count noun
: A [variable](#variabledef) whose contents are [incremented](#incrementdef) to represent the results of a [running total](#runningtotaldef).[^accumulatordef-note1]
: Hyponym of [variable](#variabledef).

**arity** {: #aritydef }
: mass noun
: The number of [operands](#operanddef) a [subroutine](#subroutinedef) takes.[^aritydef-note1]

**array** {: #arraydef }
: count noun
: A collection of same-type data items that can be selected by indices computed at run-time.[^arraydef-note1]
: Hypernym of [array data structure](#arraydatastructuredef).

**array data structure** {: #arraydatastructuredef }
: count noun
: A [data structure](https://en.wikipedia.org/wiki/Data_structure) consisting of a collection of **elements** ([values](#valuedef) or [variables](#variablede), each identified by at least one **array index** or **key**. An array is stored such that the position of each element can be computed from its index [tuple](https://en.wikipedia.org/wiki/Tuple) by a mathematical formula.[^arraydatastructuredef1] [^arraydatastructuredef2] [^arraydatastructuredef3] The simplest type of data structure is a **linear array**, also called **one-dimensional array**. The memory address of the first element of an array is called **first address** or **foundation address**.[^arraydatastructuredef-note1]
: The term *array* is often used to mean [array data type](https://en.wikipedia.org/wiki/Array_data_type), a kind of [data type](#datatypedef) provided by most [high-level programming languages](https://en.wikipedia.org/wiki/High-level_programming_language) that consists of a collection of values or variables that can be selected by one or more indices computed at run-time. Array types are often implemented by array structures; however, in some languages they may be implemented by [hash tables](https://en.wikipedia.org/wiki/Hash_table), [linked lists](https://en.wikipedia.org/wiki/Linked_list), [search trees](https://en.wikipedia.org/wiki/Search_tree), or other data structures.[^arraydatastructuredef-note1]
: Because the mathematical concept of a [matrix](https://en.wikipedia.org/wiki/Matrix_(mathematics)) can be represented as a two-dimensional grid, two-dimensional arrays are also sometimes called matrices. In some cases the term "vector" is used in computing to refer to an array, although [tuples](https://en.wikipedia.org/wiki/Tuple) rather than [vectors](https://en.wikipedia.org/wiki/Vector_space) are the more mathematically correct equivalent. [Tables](https://en.wikipedia.org/wiki/Table_(information)) are often implemented in the form of arrays, especially [lookup tables](https://en.wikipedia.org/wiki/Lookup_table); the word *table* is sometimes used as a synonym of *array*.[^arraydatastructuredef-note1]
: Arrays are among the oldest and most important data structures, and are used by almost every program. They are also used to implement many other data structures, such as [lists](https://en.wikipedia.org/wiki/List_(computing)) and [strings](https://en.wikipedia.org/wiki/String_(computer_science)). They effectively exploit the addressing logic of computers. In most modern computers and many [external storage](https://en.wikipedia.org/wiki/External_storage) devices, the memory is a one-dimensional array of words, whose indices are their addresses. [Processors](https://en.wikipedia.org/wiki/Central_processing_unit), especially [vector processors](https://en.wikipedia.org/wiki/Vector_processor), are often optimized for array operations.[^arraydatastructuredef-note1]
: Arrays are useful mostly because the element indices can be computed at [run time](https://en.wikipedia.org/wiki/Run_time_(program_lifecycle_phase)). Among other things, this feature allows a single iterative [statement](#statementdef) to process arbitrarily many elements of an array. For that reason, the elements of an array data structure are required to have the same size and should use the same data representation. The set of valid index tuples and the addresses of the elements (and hence the element addressing formula) are usually,[^arraydatastructuredef3] [^arraydatastructuredef5] but not always,[^arraydatastructuredef2] fixed while the array is in use.[^arraydatastructuredef-note1]
: The term is also used, especially in the description of [algorithms](https://en.wikipedia.org/wiki/Algorithm), to mean [associative array](https://en.wikipedia.org/wiki/Associative_array) or "abstract array", a [theoretical computer science](https://en.wikipedia.org/wiki/Theoretical_computer_science) model (an [abstract data type](https://en.wikipedia.org/wiki/Abstract_data_type) or ADT) intended to capture the essential properties of arrays.
: An array data structure is also known simply as an **array**.[^arraydatastructuredef-note1]
: For example, an array of 10 32-bit integer variables, with indices 0 through 9, may be stored as 10 [words](https://en.wikipedia.org/wiki/Word_(data_type)) at memory addresses 2000, 2004, 2008, ... 2036, so that the element with index *i* has the address 2000 + 4 × *i*.[^arraydatastructuredef4] [^arraydatastructuredef-note1]
: Hyponym of [array](#arraydef).

**assignment construct** {: #assignmentconstructdef }
: A [construct](https://en.wikipedia.org/wiki/Data_structure) that sets and/or re-sets the [value](#valuedef) stored in the storage location(s) denoted by a variable name (in other words, it copies a value into the [variable](#variabledef)). In most [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [programming languages](https://en.wikipedia.org/wiki/Programming_language) it is a fundamental construct. Assignment constructs can be [expressions](#expressiondef), [statements](#statementdef), or [operators](#assignmentoperatordef).[^assignmentconstructdef-note1]
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
: An [assignment operator](#assignmentoperatordef) that is generally used to replace a [statement](#statementdef) where an operator takes a [variable](#variabledef) as one of its arguments and then assigns the result back to the same variable. In [expression-oriented programming languages](https://en.wikipedia.org/wiki/Expression-oriented_programming_language) such as C, assignment and augmented assignment are expressions, which have a value. This allows their use in complex expressions. However, this can produce sequences of symbols that are difficult to read or understand, and worse, a mistype can easily produce a different sequence of gibberish that although accepted by the compiler does not produce desired results. In other languages, such as Python, assignment and augmented assignment are statements, not expressions, and thus cannot be used in complex expressions. As with assignment, in these languages augmented assignment is a form of [right-associative](https://en.wikipedia.org/wiki/Operator_associativity#Right-associativity_of_assignment_operators) assignment.
: For example, `x += 1` is expanded to `x = x + (1)`.[^augmentedassignmentoperatordef-note1]
: Hyponym of [assignment operator](#assignmentoperatordef).

**binary file** {: #binaryfiledef }
: count noun
: A type of [file](#filedef) that is not a [text file](#textfiledef).[^binaryfiledef1] Binary files are usually thought of as being a sequence of [octets](#octetdef), and typically contain octets that are intended to be interpreted as something other than text [characters](https://en.wikipedia.org/wiki/Character_(computing)). [Compiled](https://en.wikipedia.org/wiki/Compiled "Compiled") computer programs are typical examples; indeed, compiled applications are sometimes referred to, particularly by programmers, as **binaries**. But binary files can also mean that they contain any type of file content[^binaryfiledef1], including (but not limited to) images, sounds, and compressed versions of other files.  
Some binary files contain [headers](https://en.wikipedia.org/wiki/Header_(computing)), blocks of [metadata](https://en.wikipedia.org/wiki/Metadata) used by a [computer program](https://en.wikipedia.org/wiki/Computer_program) to interpret the [data](#datumdef) in the file. The header often contains a [signature or *magic* number](https://en.wikipedia.org/wiki/List_of_file_signatures) which can [identify](#identifierdef) the [format](https://en.wikipedia.org/wiki/File_format). For example, a [GIF](https://en.wikipedia.org/wiki/GIF) file can contain multiple images, and headers are used to identify and describe each block of image data. The leading bytes of the header would contain text like *GIF87a* or *GIF89a* that can identify the binary as a GIF file. If a binary file does not contain any headers, it may be called a **flat binary file**.[^binaryfiledef-note1]
: Hyponym of [file](#filedef).

**block** {: #blockdef }
: count noun
: A group of one or more [expressions](#expressiondef), [declarations](#declarationdef), [statements](#statementdef) or other units of code that are related in such a way as to comprise a whole. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a **block-structured programming language**. Blocks are fundamental to [structured programming](https://en.wikipedia.org/wiki/Structured_programming), where [control structures](#controlstructuredef) are formed from blocks.  
The function of blocks in programming is to enable groups of statements to be treated as if they were one statement, and to narrow the [lexical scope](https://en.wikipedia.org/wiki/Lexical_scope) of objects such as [variables](#variabledef) and [subroutines](#subroutinedef) declared in a block so that they do not conflict with those having the same name used elsewhere. In a block-structured programming language, the objects named in outer blocks are visible inside inner blocks, unless they are [masked](https://en.wikipedia.org/wiki/Name_masking) by an object declared with the same name.[^blockdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), blocks are delimited by **curly brackets** (`{` ... `}`).

**Boolean** {: #Booleandef }
: adjective
: Having one of two possible [values](#valuedef) (usually denoted *true* and *false*), intended to represent the two [truth values](https://en.wikipedia.org/wiki/Truth_value) of [logic](https://en.wikipedia.org/wiki/Logic) and [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra).[^Booleandef-note1]

**Boolean data type** {: #Booleandatatypedef }
: proper noun
: A [data type](#datatypedef) limited to [Boolean](#Booleandef) [values](#valuedef). The Boolean data type is primarily associated with [conditional](#conditionaldef) [statements](#statementdef), which allow different actions by changing [control flow](#controlflowdef) depending on whether a programmer-specified Boolean *condition* evaluates to true or false.[^Booleandatatypedef-note1]
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
: An [identifier](#identifierdef) that is [bound](https://en.wiktionary.org/wiki/bound) to an [invariant](https://en.wiktionary.org/wiki/invariant) [value](#valuedef); a fixed value given a name to aid in readability of [source code](https://en.wiktionary.org/wiki/source_code).[^constantdef-note1]

**control flow** {: #controlflowdef }
: mass noun
: The order in which individual [statements](#statementdef), [instructions](https://en.wikipedia.org/wiki/Instruction_(computer_science)) or [function calls](https://en.wikipedia.org/wiki/Function_call) of an [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [program](https://en.wikipedia.org/wiki/Computer_program) are [executed](https://en.wikipedia.org/wiki/Execution_(computing)) or evaluated. The emphasis on explicit control flow distinguishes an *[imperative programming](https://en.wikipedia.org/wiki/Imperative_programming)* language from a *[declarative programming](https://en.wikipedia.org/wiki/Declarative_programming)* language. Within an imperative [programming language](https://en.wikipedia.org/wiki/Programming_language), a [control structure](#controlstructuredef) is a construct that directs the control flow, and a *control flow statement* is a [statement](#statementdef), the execution of which results in a choice being made as to which of two or more paths to follow. For [non-strict](https://en.wikipedia.org/wiki/Strict_programming_language) functional languages, functions and language constructs exist to achieve the same result, but they are usually not termed control flow statements. A set of statements is in turn generally structured as a [block](https://en.wikipedia.org/wiki/Block_(programming)) which, in addition to grouping, also defines a [lexical scope](https://en.wikipedia.org/wiki/Lexical_scope). [Interrupts](https://en.wikipedia.org/wiki/Interrupt) and [signals](https://en.wikipedia.org/wiki/Signal_(computing)) are low-level mechanisms that can alter the flow of control in a way similar to a [subroutine](#subroutinedef), but usually occur as a response to some external stimulus or event (that can occur [asynchronously](https://en.wikipedia.org/wiki/Asynchronous_systems)), rather than execution of an *in-line* control flow statement.[^controlflowdef-note1]
: Control flow is also known as **flow of control**.[^controlflowdef-note1]

**control structure** {: #controlstructuredef }
: count noun
: A construct, made up of one or more [blocks](#blockdef), that directs the [control flow](#controlflowdef) of a program when given certain conditions and parameters. It is the basic decision-making process in computing. Its initial conditions and parameters are called *preconditions.* Preconditions are the state of variables before entering a control structure. Based on those preconditions, the computer runs an *algorithm* (the control structure) to determine what to do. The result is called a *postcondition.* Postconditions are the state of variables after the algorithm is run.[^controlstructuredef-note1]
: By analogy, suppose the [flow of control](#controlflowdef) is the flow of traffic, and the control structure is an intersection. A vehicle is arriving at the intersection, and the traffic light at the intersection is red. The control structure must determine the proper course of action to assign to the vehicle. **Precondition:** The vehicle is in motion. **Treatment of information through a control structure begins.** Is the traffic light green? If so, then the vehicle may stay in motion. Is the traffic light red? If so, then the vehicle must stop. **Treatment ends. Postcondition:** The vehicle comes to a stop. Thus, upon exiting the control structure, the vehicle is stopped.[^controlstructuredef-note1]

**control variable** {: #controlvariabledef }
: count noun
: A [variable](#variabledef) that is used to regulate the [flow of control](#controlflowdef) of a program. In definite [iteration](#iterationdef), control variables are variables which are successively assigned (or bound to) [values](#valuedef) from a predetermined sequence of values.[^controlvariabledef1] [^controlvariabledef-note1]
: Hyponym of [variable](#variabledef).

**count-controlled loop construct** {: #countcontrolledloopconstructdef }
: count noun
: A [loop construct](#loopconstructdef) that [iterates](#iterationdef) a certain number of times.[^countcontrolledloopconstructdef-note1]
: Hypernym of [for-loop construct](#forloopconstructdef).
: Hyponym of [loop construct](#loopconstructdef).

**counter** {: #counterdef }
: count noun
: A [variable](#variabledef) whose contents are [incremented](#incrementdef) or [decremented](#decrementdef)[^counterdef-note1] by a fixed number[^counterdef] to represent the results of [counting](https://en.wikipedia.org/wiki/Counting).[^counterdef-note2]
: Hypernym of [loop counter](#loopcounterdef).
: Hyponym of [variable](#variabledef).

**data type** {: #datatypedef }
: count noun
: An attribute of [data](#datumdef) which tells the [compiler](https://en.wikipedia.org/wiki/Compiler) or [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) how the programmer intends to use the data. Most programming languages support common data types of [real](https://en.wikipedia.org/wiki/Real_number), [integer](https://en.wikipedia.org/wiki/Integer_(computer_science)) and [Boolean](#Booleandatatypedef). A data type constrains the [values](#valuedef) that an [expression](#expressiondef), such as a [variable](#variabledef) or a [subroutine](#subroutinedef), might take. This data type defines the operations that can be done on the data, the meaning of the data, and the way values of that type can be stored. A type of value from which an expression may take its value.[^datatypedef1] [^datatypedef2] [^datatypedef-note1]
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

**declaration** {: #declarationdef }
: count noun
: A [language construct](https://en.wikipedia.org/wiki/Language_construct) that introduces an [identifier](#identifierdef), specifies its properties, and declares its meaning.[^declarationdef1] Declarations are most commonly used for [subroutines](#subroutinedef), [variables](#variabledef), [constants](#constantdef), and [classes](https://en.wikipedia.org/wiki/Class_(computer_programming)), but can also be used for other entities such as enumerations and type definitions.[^declarationdef1] Beyond the name (the identifier itself) and the kind of [entity](#entitydef) (subroutine, variable, etc.), declarations typically specify the [data type](#datatypedef) for variables and constants, or the [type signature](https://en.wikipedia.org/wiki/Type_signature) for subroutines. Types may also include dimensions, such as for arrays. A declaration is used to announce the existence of the entity to the [compiler](https://en.wikipedia.org/wiki/Compiler); this is important in those [strongly typed](https://en.wikipedia.org/wiki/Strongly_typed) languages that require functions, variables, and constants, and their types to be specified with a declaration before use, and is used in [forward declaration](https://en.wikipedia.org/wiki/Forward_declaration).[^declarationdef2] The term "declaration" is frequently contrasted with the term "[definition](#definitiondef)",[^declarationdef1] but meaning and usage varies significantly between programming languages.[^declarationdef-note1]
: In informal usage, it refers only to a pure declaration (types only, no value or body).[^declarationdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), declarations introduce (or re-introduce) names into a C++ program. Each kind of entity is declared differently. [Definitions](#definitiondef) are declarations that are sufficient to use the entity identified by the name.[^declarationdef-note2] A declaration of a function that does not include a body is called a [function prototype](https://en.wikipedia.org/wiki/Function_prototype).[^declarationdef-note1]

**decrement** {: #decrementdef }
: verb
: To decrease in [value](#valuedef) by a basic quantity unit, especially by 1.[^decrementdef-note1]

**decrement operator** {: #decrementoperatordef }
: count noun
: A [unary](https://en.wikipedia.org/wiki/Unary_operator) [operator](#operatordef) that decreases the [value](#valuedef) of its [operand](#operanddef) by 1. The operand must have an arithmetic or [pointer](https://en.wikipedia.org/wiki/Pointer_(computer_programming)) [data type](#datatypedef), and must refer to a modifiable [data object](https://en.wikipedia.org/wiki/Data_object). Pointer values are decreased by an amount that makes them point to the next element adjacent in memory.[^decrementoperatordef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), the operator is two [hyphen-minuses](https://en.wikipedia.org/wiki/Hyphen-minus) (`--`), and its operand must be an [lvalue](#lvaluedef) [^decrementoperatordef-note2]. It can be used as a prefix (`--foo`) or a postfix (`foo--`). As a prefix, it decreases the [value](#valuedef) of its operand by 1, and the value of the expression is the resulting decremented value. As a postfix, it decreases the value of its operand by 1, but the value of the expression is the operand's original value *prior* to the decrement operation.[^decrementoperatordef-note1]
: Hyponym of [operator](#operatordef).

**definition** {: #definitiondef }
: count noun
: A [language construct](https://en.wikipedia.org/wiki/Language_construct) that instantiates or implements an [identifier](#identifierdef).[^definitiondef-note1]
: In informal usage, it refers to a [declaration](#declarationdef) that includes a [value](#valuedef) or body.[^definitiondef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), definitions are [declarations](#declarationdef) that fully define the [entity](#entitydef) introduced by the declaration.[^definitiondef-note2]

**direct access** {: #directaccessdef }
: mass noun
: The ability to access an arbitrary element of a sequence in equal time or any item of data from a population of [addressable](https://en.wikipedia.org/wiki/Address_space) elements roughly as easily and efficiently as any other, no matter how many elements may be in the set. It is typically contrasted to [sequential access](https://en.wikipedia.org/wiki/Sequential_access).  
For example, data might be stored notionally in a single sequence like a row, in two dimensions like rows and columns on a surface, or in multiple dimensions. However, given all the coordinates, a program can access each record about as quickly and easily as any other. In this sense the choice of data item is arbitrary in the sense that no matter which item is sought, all that is needed to find it, is its address, that is to say, the coordinates at which it is located, such as its row and column (or its track and record number on a [magnetic drum](https://en.wikipedia.org/wiki/Drum_memory)). The opposite is [sequential access](https://en.wikipedia.org/wiki/Sequential_access), where a remote element takes longer time to access.[\[1\]](https://technet.microsoft.com/en-us/library/cc938619.aspx) For example, compare an ancient [scroll](https://en.wikipedia.org/wiki/Scroll_(parchment) (sequential: all material prior to the data needed must be unrolled) and a [book](https://en.wikipedia.org/wiki/Book) (direct: can be immediately flipped open to any arbitrary [page](https://en.wikipedia.org/wiki/Page_(paper))). A more modern example is a cassette tape (sequential: one must fast forward through earlier songs to get to later ones) and a [CD](https://en.wikipedia.org/wiki/CD) (direct access: one can skip to the track wanted, knowing that it would be the one retrieved).  
In [data structures](https://en.wikipedia.org/wiki/Data_structure), direct access implies the ability to access any entry in a [list](https://en.wikipedia.org/wiki/List_(computing)) in [constant time](https://en.wikipedia.org/wiki/Constant_time) (independent of its position in the list and of list's size). Very few data structures can guarantee this, other than [arrays](https://en.wikipedia.org/wiki/Array_data_structure) (and related structures like [dynamic arrays](https://en.wikipedia.org/wiki/Dynamic_array)). Direct access is required, or at least valuable, in many algorithms such as [binary search](https://en.wikipedia.org/wiki/Binary_search), [integer sorting](https://en.wikipedia.org/wiki/Integer_sorting) or certain versions of [sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes).[^directaccessdef3] Other data structures, such as [linked lists](https://en.wikipedia.org/wiki/Linked_list), sacrifice direct access to permit efficient inserts, deletes, or reordering of data. [Self-balancing binary search trees](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree) may provide an acceptable compromise, where access time is not equal for all members of a collection, but the maximum time to retrieve a given member grows only [logarithmically](https://en.wikipedia.org/wiki/Logarithmically) with its size.[^directaccessdef-note1]
: It is also less precisely known as **random access**. At first the term was used because the process had to be capable of finding records no matter in which sequence they were required.[^directaccessdef1] However, soon the term "direct access" gained favor because one could directly retrieve a record, no matter what its position might be.[^directaccessdef2] The operative attribute however is that the device can access any required record immediately on demand.[^directaccessdef-note1]

**do-while-loop construct** {: #dowhileloopconstructdef }
: count noun
: A [control flow](#controlflowdef) construct that executes a [block](#blockdef) of code at least once, and then repeatedly executes the block, or not, depending on a given [Boolean](#Booleandef) [condition](#conditiondef) at the end of the block. Because the do-while-loop construct checks the condition after the block is executed, the control structure is often also known as a **posttest loop**. Compare this with the [*while* loop construct](#whileloopconstructdef), which tests the condition *before* the code within the block is executed.[^dowhileloopconstructdef-note1]
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
: In computer science, entities include [classes](https://en.wikipedia.org/wiki/Class_(computer_programming)), [constants](#constantdef), [data types](#datatypedef), enumerations, [labels](https://en.wikipedia.org/wiki/Label_(programming_language)), [packages](https://en.wikipedia.org/wiki/Modular_programming), [subroutines](#subroutinedef), type definitions, [variables](#variabledef).[^entitydef-note3]
: In [C++](https://en.wikipedia.org/wiki/C++), entities include [values](#valuedef), [objects](https://en.cppreference.com/w/cpp/language/objects), [references](https://en.cppreference.com/w/cpp/language/reference), [structured bindings](https://en.cppreference.com/w/cpp/language/structured_binding) (since C++17), [functions](https://en.cppreference.com/w/cpp/language/functions), [enumerators](https://en.cppreference.com/w/cpp/language/enum), [types](https://en.cppreference.com/w/cpp/language/type), class members, [templates](https://en.cppreference.com/w/cpp/language/templates), [template specializations](https://en.cppreference.com/w/cpp/language/template_specialization), [namespaces](https://en.cppreference.com/w/cpp/language/namespace), and [parameter packs](https://en.cppreference.com/w/cpp/language/parameter_pack). Preprocessor [macros](https://en.cppreference.com/w/cpp/preprocessor/replace) are not C++ entities.[^entitydef-note2]

**entry point** {: #entrypointdef }
: count noun
: The point in a program where the first instructions are executed, and where the program has access to [command line arguments](https://en.wikipedia.org/wiki/Command_line_arguments).[^entrypointdef-note1] [Python-Markdown has a different, unclear definition in the context of extensions](https://python-markdown.github.io/extensions/#officially-supported-extensions).

**expression** {: #expressiondef }
: A combination of one or more [constants](#constantdef), [variables](#variabledef), [operators](#operatordef), and [subroutines](#subroutinedef) that a [programming language](https://en.wikipedia.org/wiki/Programming_language) interprets (according to its particular [rules of precedence](https://en.wikipedia.org/wiki/Order_of_operations) and of [association](#associativitydef)) and computes to produce ("to return", in a [stateful](https://en.wikipedia.org/wiki/State_(computer_science)) environment) another [value](#valuedef). This process, as for [mathematical expressions](https://en.wikipedia.org/wiki/Mathematical_expression), is called evaluation. In simple settings, the [resulting value](https://en.wikipedia.org/wiki/Return_type) is usually one of various [primitive types](https://en.wikipedia.org/wiki/Primitive_data_type), such as numerical, [string](https://en.wikipedia.org/wiki/String_(computer_science)), and [logical](https://en.wikipedia.org/wiki/Boolean_expression); in more elaborate settings, it can be an arbitrary [complex data type](https://en.wikipedia.org/wiki/Complex_data_type).[^expressiondef-note1]
: For example, `2+3` is an arithmetic and programming expression which evaluates to `5`. A variable is an expression because it denotes a value in memory, so `y+6` is an expression. An example of a relational expression is `4≠4`, which evaluates to `false`.[^expressiondef-note1] [^expressiondef1] [^expressiondef2]
: Hypernym of [conditional expression](#conditionalexpressiondef) and [relational expression](#relationalexpressiondef).

**file** {: #filedef }
: count noun
: An [aggregation](https://en.wiktionary.org/wiki/aggregation) of [data](#datumdef) on a [storage](https://en.wiktionary.org/wiki/storage) [device](https://en.wiktionary.org/wiki/device), [identified](#identifierdef) by a [name](https://en.wiktionary.org/wiki/name). On most modern [operating systems](https://en.wikipedia.org/wiki/Operating_syste), files are organized into one-dimensional arrays of [bytes](https://en.wikipedia.org/wiki/Byte). By using computer programs, a person can open, read, change, save, and close a computer file. Computer files may be reopened, modified, and copied an arbitrary number of times. Typically, files are organised in a [file system](https://en.wikipedia.org/wiki/File_system), which keeps track of where the files are located on disk and enables user access. The [format](https://en.wikipedia.org/wiki/File_format) of a file is defined by its content since a file is solely a container for data, although, on some platforms the format is usually indicated by its [filename extension](https://en.wikipedia.org/wiki/Filename_extension), specifying the rules for how the bytes must be organized and interpreted meaningfully. For example, the bytes of a plain text file (`.txt` in Windows) are associated with either [ASCII](https://en.wikipedia.org/wiki/ASCII) or [UTF-8](https://en.wikipedia.org/wiki/UTF-8) characters, while the bytes of image, video, and audio files are interpreted otherwise. Most file types also allocate a few bytes for [metadata](https://en.wikipedia.org/wiki/Metadata), which allows a file to carry some basic information about itself.[^filedef-note1]
: The six most basic **file operations** a program can perform on a file are: create a new file, change the [access permissions](https://en.wikipedia.org/wiki/File_system_permissions) and [attributes](https://en.wikipedia.org/wiki/File_attribute) of a file, [open](https://en.wikipedia.org/wiki/Open_(system_call)) a file and make the file contents available to the program, [read](https://en.wikipedia.org/wiki/Read_(system_call)) data from a file, [write](https://en.wikipedia.org/wiki/Write_(system_call)) data to a file, or [close](https://en.wikipedia.org/wiki/Close_(system_call)) a file and terminate the association between it and the program.
: Hypernym of [binary file](#binaryfiledef) and [text file](#textfiledef).

**flag** {: #flagdef }
: count noun
: A [variable](#variabledef) or memory location that stores a [Boolean](#Booleandef) [value](#valuedef), typically either recording the fact that a certain event has occurred or requesting that a certain optional action take place.[^flagdef-note1]
: Hyponym of [variable](#variabledef).

**for-loop construct** {: #forloopconstructdef }
: count noun
: A [control flow](#controlflowdef) construct that allows a [block](#blockdef) of code to be executed repeatedly, typically when the number of [iterations](#iterationdef) is known before entering the loop. A for-loop construct can be thought of as shorthand for a [while-loop construct](#whileloopconstructdef). A for-loop construct has two parts: a **for-loop header** specifying the iteration, and a **for-loop body** which is executed once per iteration. The header often [declares](#declarationdef) an explicit [loop counter](#loopcounterdef), which allows the body to know which iteration is being executed.[^forloopconstructdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), the for-loop construct is a **pretest-loop construct**.[^forloopconstructdef1] [^forloopconstructdef-note2]
: Hyponym of [count-controlled loop construct](#countcontrolledloopconstructdef).

**identifier** {: #identifierdef }
: count noun
: A [lexical](https://en.wikipedia.org/wiki/Lexical_(semiotics)) [token](https://en.wikipedia.org/wiki/Token_(parser)) that names an [entity](#entitydef). Identifiers are used extensively in virtually all [information processing systems](https://en.wikipedia.org/wiki/Information_processing_system). Identifying entities makes it possible to refer to them, which is essential for any kind of symbolic processing.[^identifierdef-note1]
: In [computer languages](https://en.wikipedia.org/wiki/Computer_language), an identifier is a token that names a computer language entity. Some of the kinds of entities an identifier might denote include [variables](#variabledef), [constants](#constantdef), [data types](#datatypedef), [labels](https://en.wikipedia.org/wiki/Label_(programming_language)), [subroutines](#subroutinedef), and [packages](https://en.wikipedia.org/wiki/Modular_programming).[^identifierdef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++) identifiers are labels used for various things, including [functions](#subroutinedef), classes, namespaces, and [variables](#variabledef). The rules for identifiers are the same whether the identifier refers to a variable, function, or whatever else. In general, the name of an identifier must consist of the characters `a-z`, `A-Z`, `0-9` and `_`, not begin with a digit or `_` and not be a [keyword](https://en.cppreference.com/book/glossary#keyword). There are more rules that must be followed.  
Identifiers are usually not stored in the final program (unless certain debugging settings are used) so the user need not worry about descriptive names giving hackers clues. They also don't have to worry about the size of identifiers; if they're stripped out, they take up no space in the final program.[^identifierdef-note2]

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
When an [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing)) finds an `if`, it expects a [condition](#conditiondef) (`(condition)`) and evaluates that condition. If the condition is `true`, the statements following the `then` (`(consequent)`) are executed. Otherwise, the execution continues in the following clause, either in the [else clause](#elseclausedef) (which is usually optional, and in this case contains `(alternative)`) or, if there is no else clause, then after the `end if`. After either clause has been executed, [control](#controlflowdef) returns to the point after the `end if`.[^ifconstructdef-note1]  
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
: Holonym of [else-clause](#elseclausedef), [else-if-clause](#elseifclausedef), and [if-clause](#ifclausedef).

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
: A [counter](#counterdef) that controls the [iterations](#iterationdef) of a [loop construct](#loopconstructdef). Most uses of a loop construct result in the loop counter taking on a range of integer values in some orderly sequences (for example, starting at 0 and ending at 10 in [increments](#incrementdef) of 1). Loop counters change with each iteration of a loop, providing a unique value for each individual iteration. The loop counter is used to decide when the loop should terminate and for the [program flow](#controlflowdef) to continue to the next instruction after the loop.[^loopcounterdef-note1] A loop counter must be [initialized](https://en.wikipedia.org/wiki/Initialization_(programming)) before it is used.[^loopcounterdef-note2]
: Hyponym of [counter](#counterdef).

**lvalue** {: #lvaluedef }
: count noun
: A [value](#valuedef) that refers to a [data object](https://en.wikipedia.org/wiki/Data_object) that persists beyond a single [expression](#expressiondef).[^lvaluedef2] In many languages, notably the [C family](https://en.wikipedia.org/wiki/C_programming_language), an lvalue has a [storage address](https://en.wikipedia.org/wiki/Memory_address) that is programmatically accessible to the running program (for example, via some address-of operator like `&` in C/C++), meaning that it is a [variable](#variabledef) or dereferenced reference to a certain memory location.[^lvaluedef-note2]
: For its etymology, it comes from *[L](https://en.wiktionary.org/wiki/L#English)* +‎ *[value](#valuedef)*, where *L* stands for *left-hand side*, deriving from the typical mode of evaluation on the left and [right](#rvaluedef) hand side of an [assignment](#assignmentconstructdef) [statement](#statementdef).[^lvaluedef-note2] In context of the [C programming language](https://en.wiktionary.org/wiki/C#English-programming_language) it is usually expanded as *[locator](https://en.wiktionary.org/wiki/locator#English)* *value*.[^lvaluedef-note1]
: In [C](https://en.wikipedia.org/wiki/C_(programming_language)), if an lvalue refers to a modifiable data object, it is called a **modifiable lvalue**.[^lvaluedef1]
: Hyponym of [value](#valuedef).

**nest** {: #nestdef }
: verb
: To [contain an object within a similar object](https://en.wikipedia.org/wiki/Self-similarity).[^nestdef-note1]
: To organize information into layers.[^nestdef-note1]

**object** {: #objectdef }
: count noun
: A [value](#valuedef) in [memory](https://en.wikipedia.org/wiki/Memory_address) referenced by an [identifier](#identifierdef), such as a [variable](#variabledef), a [data structure](https://en.wikipedia.org/wiki/Data_structure), a [subroutine](#subroutinedef), or a [method](https://en.wikipedia.org/wiki/Method_(computer_programming)).[^objectdef-note1]
: In [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) (a [class-based](https://en.wikipedia.org/wiki/Class-based_programming) paradigm), *object* refers to a particular [instance](https://en.wikipedia.org/wiki/Instance_(computer_science)) of a [class](https://en.wikipedia.org/wiki/Class_(computer_science)), where the object can be a combination of [variables](#variabledef), [subroutines](#subroutinedef), and data structures.[^objectdef-note1]

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

**performant** {: #performantdef }
: adjective
: Capable of or characterized by an [adequate](https://en.wiktionary.org/wiki/adequate) or [excellent](https://en.wiktionary.org/wiki/excellent) level of [performance](https://en.wiktionary.org/wiki/performance) or [efficiency](https://en.wiktionary.org/wiki/efficiency).
: Usage notes: In computing jargon, something *performant* is not necessarily *[efficient](https://en.wiktionary.org/wiki/efficient)* or *[optimal](https://en.wiktionary.org/wiki/optimal#English)*; it is “good enough” in a sense that performance levels meet or exceed the expectations of end users.[^performantdef-note1]

**programmatical freedom** {: #programmaticalfreedomdef }
: mass noun
: The ability to run a program for any purpose and to study, change, and distribute it and any adapted versions.[^programmaticalfreedomdef-note1] This ability can be explained in more detail with **four freedoms** that specify the actions that can be taken on or with a program. The first action that can be performed (or **freedom zero**) is to run a program as one wishes, for any purpose. The second action that can be performed (or **freedom one**) is to study how a program works and change it to do one's computing as one wishes. The third action that can be performed (or **freedom two**) is to redistribute copies of a program. The fourth action that can be performed (or **freedom three**) is to distribute copies of a program one has changed. Freedoms one and three require the program's [source code](https://en.wikipedia.org/wiki/Source_code) to be available.[^programmaticalfreedomdef-note2] Taken together, freedoms zero, one, and three make [forking](https://en.wikipedia.org/wiki/Fork_(software_development)) possible.

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

**sentinel value** {: #sentinelvaluedef }
: count noun
: A [value](#valuedef) that marks the end of sequence, typically in a [loop construct](#loopconstructdef) or recursive [algorithm](https://en.wikipedia.org/wiki/Algorithm).[^sentinelvaluedef-note1]
: A sentinel value is also referred to as a **flag value**, **trip value**, **rogue value**, **signal value**, or **dummy data**[^sentinelvaluedef1], and is sometimes known as an **[Elephant in Cairo](https://en.wikipedia.org/wiki/Elephant_in_Cairo)** due to a joke where this is used as a physical sentinel. In safe languages, most uses of sentinel values could be replaced with [option types](https://en.wikipedia.org/wiki/Option_type), which enforce explicit handling of the exceptional case.
: Hyponym of [value](#valuedef).

**separator** {: #separatordef }
: count noun
: A token that demarcates boundaries between two separate [statements](#statementdef). A separator is also known as a **punctuator**.[^separatordef-note1]

**sequential access** {: #sequentialaccessdef }
: mass noun
: Accessing a group of elements (such as data in a memory array or a [disk](https://en.wikipedia.org/wiki/Hard_disk_drive) file or on [magnetic tape data storage](https://en.wikipedia.org/wiki/Magnetic_tape_data_storage) in a predetermined, ordered [sequence](https://en.wikipedia.org/wiki/Sequence). Sequential access is sometimes the only way of accessing the data, for example if it is on a tape. It may also be the access method of choice, for example if all that is wanted is to process a sequence of data elements in order.[^sequentialaccessdef1] However, there is no consistent definition of sequential access or sequentiality.[^sequentialaccessdef2] [^sequentialaccessdef3] [^sequentialaccessdef4] [^sequentialaccessdef5] [^sequentialaccessdef6] [^sequentialaccessdef7] [^sequentialaccessdef8] [^sequentialaccessdef9] In fact, different sequentiality definitions can lead to different sequentiality quantification results. In spatial dimension, request size, strided distance, backward accesses, re-accesses can affect sequentiality. For temporal sequentiality, characteristics such as multi-stream and inter-arrival time threshold has impact on the definition of sequentiality.[^sequentialaccessdef10] [^sequentialaccessdef-note1]  
: In [data structures](https://en.wikipedia.org/wiki/Data_structure), a data structure is said to have sequential access if one can only visit the values it contains in one particular order. The canonical example is the [linked list](https://en.wikipedia.org/wiki/Linked_list). Indexing into a list that has sequential access requires [O](https://en.wikipedia.org/wiki/Big_O_notation)(*n*) time, where *n* is the index. As a result, many algorithms such as [quicksort](https://en.wikipedia.org/wiki/Quicksort) and [binary search](https://en.wikipedia.org/wiki/Binary_search_algorithm") degenerate into bad algorithms that are even less efficient than their naive alternatives; these algorithms are impractical without [direct access](#directaccessdef). On the other hand, some algorithms, typically those that do not have index, require only sequential access, such as [mergesort](https://en.wikipedia.org/wiki/Mergesort), and face no penalty.[^sequentialaccessdef-note1]

**statement** {: #statementdef }
: count noun
: A syntactic unit of an [imperative](https://en.wikipedia.org/wiki/Imperative_programming) [programming language](https://en.wikipedia.org/wiki/Programming_language) that changes the program state or performs some kind of action.[^statementdef1] [^statementdef-note2] It also has meaning.[^statementdef-note3] A program written in such a language is formed by a sequence of one or more statements. A statement may have internal components (e.g., [expressions](#expressiondef)). Boundaries between statements are demarcated by [separators](#separatordef), and the end of a statement is demarcated by a [terminator](#terminatordef). [^statementdef-note1]

**subroutine** {: #subroutinedef }
: count noun
: A sequence of program instructions that performs a specific task, packaged as a unit. This unit can then be used in programs wherever that particular task should be performed. It may be defined within a single program, or separately in a [library](https://en.wikipedia.org/wiki/Library_(computer_science)) that can be used by many programs. In different programming languages, a subroutine may be called a **procedure**, a **function**, a **routine**, a [method](https://en.wikipedia.org/wiki/Method_(computing)), or a **subprogram**. The generic term **callable unit** is sometimes used.[^subroutinedef1] [^subroutinedef-note1]
: A subroutine has [arity](#aritydef).
: In [C++](https://en.wikipedia.org/wiki/C++), subroutines are called [functions](https://en.cppreference.com/w/cpp/language/functions) (further classified as *member functions* when associated with a [class](https://en.wikipedia.org/wiki/Class_(computer_programming)), or *free functions*[^subroutinedef2] when not). These languages use the special keyword `void` to indicate that a function takes no parameters or does not return any value. Note that C++ functions can have side-effects, including modifying any [variables](#variabledef) whose addresses are passed as parameters (that is, *passed by reference*).[^subroutinedef-note1]

**switch construct** {: #switchconstructdef }
: count noun
A type of selection control mechanism used to allow the value of a [variable](#variabledef) or [expression](#expressiondef) to change the [control flow](#controlflowdef) of program execution via search and map.[^switchconstructdef-note1]

**symbol** {: #symboldef }
: count noun
: A waveform, a state or a significant condition of a communication channel that persists for a fixed period of time. It may be described as either a pulse in digital baseband transmission or a tone in passband transmission using modems. A sending device places symbols on the channel at a fixed and known symbol rate, and the receiving device has the job of detecting the sequence of symbols in order to reconstruct the transmitted [data](#datumdef). There may be a direct correspondence between a symbol and a small unit of data. For example, each symbol may encode one or several binary digits or 'bits'. The data may also be represented by the transitions between symbols, or even by a sequence of many symbols.[^symboldef-note1]

**syntax highlighting** {: #syntaxhighlightingdef }
: mass noun
: The displaying of text, especially [source code](https://en.wikipedia.org/wiki/Source_code), in different colors and fonts to indicate syntactic structure.[^syntaxhighlightingdef-note1]

**terminator** {: #terminatordef }
: count noun
: A token that demarcates the end of an individual [statement](#statementdef).[^terminatordef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), it is a semicolon (`;`).

**text file** {: #textfiledef }
: count noun
: A type of [file](#filedef) that is structured as a sequence of [lines](https://en.wikipedia.org/wiki/Line_(text_file)) of [electronic text](https://en.wikipedia.org/wiki/Electronic_text). A text file exists [stored as data](https://en.wikipedia.org/wiki/Data_storage) within a [file system](https://en.wikipedia.org/wiki/File_system). It refers to a type of container, while [plain text](https://en.wikipedia.org/wiki/Plain_text) refers to a type of content.[^textfiledef-note1]
: Hyponym of [file](#filedef).

**trailing** {: #trailingdef }
: adjective
: Occuring at the end[^trailingdef] of a line.
: For example, this line contains two **trailing** dots.⋅⋅

**truncate** {: #truncatedef }
: verb
: To shorten a [decimal](https://en.wiktionary.org/wiki/decimal) [number](https://en.wiktionary.org/wiki/number) by removing [trailing](#trailingdef) or [leading](#leadingdef) [digits](https://en.wiktionary.org/wiki/digit).[^truncatedef-note1]

**value** {: #valuedef }
: count noun
: A known or unknown quantity of information.[^valuedef-note1]
: Hypernym of [lvalue](#lvaluedef), [rvalue](#rvaluedef), and [sentinel value](#sentinelvaluedef).

**variable** {: #variabledef }
: count noun
: An [object](#objectdef) whose [value](#valuedef) can change. This is in contrast with a [constant](#constantdef), whose value cannot change. Variables are fundamental to programming, because without them, a program's behavior could not change (it would run the same way every time) and even simple programs would require enormous amounts of memory because, if objects' values cannot change, each new value needed would need a new object.  
The variable [identifier](#identifierdef) is the usual way to [reference](https://en.wikipedia.org/wiki/Reference_(computer_science)) the stored value, in addition to referring to the variable itself, depending on the context. This separation of identifier and content allows the identifier to be used independently of the exact information it represents. The variable identifier in computer [source code](https://en.wikipedia.org/wiki/Source_code) can be [bound](https://en.wikipedia.org/wiki/Name_binding) to a [value](#valuedef) during [run time](https://en.wikipedia.org/wiki/Run_time_(program_lifecycle_phase)), and the value of the variable may thus change during the course of [program execution](https://en.wikipedia.org/wiki/Execution_(computing)).[^variabledef1] [^variabledef2] [^variabledef-note1]
: A variable is also known as a **scalar**.[^variabledef-note1]
: In [C++](https://en.wikipedia.org/wiki/C++), a variable is a quantity of memory that has been reserved for the program's use. It is referred to using a variable [identifier](#identifierdef), so the user doesn't need to worry about where it is in memory (though they can find out its memory address, and even specify its location, if they want). The C++ type system keeps track of the size of the memory block, and how to interpret the value in it (that is, it will know whether the value `65` in a certain memory block actually refers to the number 65, the letter '`A`' (the ASCII/Unicode code number for the character 'A' is `65`), or even perhaps a complex number with real part 6 and imaginary part 5). Creating a variable in C++ requires at least two things: a variable [identifier](#identifierdef) and a type.[^variabledef-note2]
: Hypernym of [accumulator](#accumulatordef), [control variable](#controlvariabledef), [counter](#counterdef), and [flag](#flagdef).

**while-loop construct** {: #whileloopconstructdef }
: count noun
: A [control flow](#controlflowdef) construct that allows a [block](#blockdef) of code to be executed repeatedly based on a given [Boolean](#Booleandef) [condition](#conditiondef). It can be thought of as a repeating [if-construct](#ifconstructdef). It consists of a [block](#blockdef) of code and a [condition](#conditiondef)/[expression](#expressiondef).[^whileloopconstructdef1] The condition/expression is evaluated, and if the condition/expression is *true*,[^whileloopconstructdef1] the code within the block is executed. This repeats until the condition/expression becomes [false](https://en.wikipedia.org/wiki/False_(logic)). Because the *while* loop construct checks the condition/expression before the block is executed, the [control structure](#controlstructuredef) is often also known as a **pretest-loop construct**. Compare this with the [*do while* loop construct](#dowhileloopconstructdef), which tests the condition/expression *after* the loop has executed.[^whileloopconstructdef-note1]
: 
```
int x = 0;
while (x < 5) 
{
    printf ("x = %d\n", x);
    x++;
}
```
: For example, the code fragment above first checks whether `x` is less than 5, which it is, so then the loop body within the curly brackets is entered, where the `printf` [subroutine](#subroutinedef) is run and `x` is [incremented](#incrementdef) by 1. After completing all the statements in the loop body, the condition, (x < 5), is checked again, and the loop is executed again, this process repeating until the [variable](#variabledef) `x` has the value 5.  
: 
```
while (true)
{
    //do complicated stuff
    if (someCondition) break;
    //more stuff
}
```
: The code fragment above shows that it is possible, and in some cases desirable, for the condition to *always* evaluate to true, creating an [infinite loop](https://en.wikipedia.org/wiki/Infinite_loop). When such a loop is created intentionally, there is usually another [control structure](#controlstructuredef) (such as a [break](https://en.wikipedia.org/wiki/Control_flow) statement) that controls termination of the loop.  
The code fragments above are written in the [C programming language](https://en.wikipedia.org/wiki/C_(programming_language)) (as well as [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)),[^whileloopconstructdef2] [Objective-C](https://en.wikipedia.org/wiki/Objective-C), and [C++](https://en.wikipedia.org/wiki/C++), which [use the same syntax](https://en.wikipedia.org/wiki/Polyglot_(computing)) in this case).
: Hyponym of [condition-controlled loop construct](#conditioncontrolledloopconstructdef).

## [protologism] section

**post-endmost-slash path component** {: #postendmostslashpathcomponentdef }
: [compound] count noun
: The [path component of a URL](https://en.wikipedia.org/wiki/URL#Syntax) after the endmost slash (`/`).
: For example, [the Git page on Wikibooks](https://en.wikibooks.org/wiki/Git) URL is `https://en.wikibooks.org/wiki/Git`, so its post-endmost-slash path component would be `Git`.
: I have created this word because I could not find an existing word specificially referring to the path component of a URL after the endmost slash.

[compound]: https://en.wiktionary.org/wiki/compound_word
[protologism]: https://en.wikipedia.org/wiki/Protologism

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).**[^glossry1] Includes significant content from:

- [Abstraction (disambiguation)](https://en.wikipedia.org/w/index.php?title=Abstraction_(disambiguation)&oldid=864262592)
- [Array§Computer science](https://en.wikipedia.org/w/index.php?title=Array&oldid=874587697#Computer_science)
- [Array data structure](https://en.wikipedia.org/w/index.php?title=Array_data_structure&oldid=885176766)
- [Assignment (computer science)](https://en.wikipedia.org/w/index.php?title=Assignment_(computer_science)&oldid=882172626)
- [Assignment operator (C++)](https://en.wikipedia.org/w/index.php?title=Assignment_operator_(C%2B%2B)&oldid=873288112)
- [Augmented assignment](https://en.wikipedia.org/w/index.php?title=Augmented_assignment&oldid=879453644)
- [Binary file](https://en.wikipedia.org/w/index.php?title=Binary_file&oldid=876032410)
- [Block (programming)](https://en.wikipedia.org/w/index.php?title=Block_(programming)&oldid=877703688)
- [Boolean data type](https://en.wikipedia.org/w/index.php?title=Boolean_data_type&oldid=876857392)
- [Calculation](https://en.wikipedia.org/w/index.php?title=Calculation&oldid=884039961)
- [Comparison of programming languages (syntax)§Blocks](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Blocks)
- [Comparison of programming languages (syntax)§Statements](https://en.wikipedia.org/w/index.php?title=Comparison_of_programming_languages_(syntax)&oldid=871969304#Statements)
- [Computer file](https://en.wikipedia.org/w/index.php?title=Computer_file&oldid=883194383)
- [Computer file§File contents](https://en.wikipedia.org/w/index.php?title=Computer_file&oldid=883194383#File_contents)
- [Conditional (computer programming)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Conditional (computer programming)§Else if](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=882062344#Else_if)
- [Conditional (computer programming)§If–then(–else)](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=881570939)
- [Conditional (computer programming)§If–then–else expressions](https://en.wikipedia.org/w/index.php?title=Conditional_(computer_programming)&oldid=882062344#If%E2%80%93then%E2%80%93else_expressions)
- [Conditional operator](https://en.wikipedia.org/w/index.php?title=Conditional_operator&oldid=846889637)
- [Control flow](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=885162294)
- [Control flow§Loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Loops)
- [Control flow§Condition-controlled loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Condition-controlled_loops)
- [Control flow§Count-controlled loops](https://en.wikipedia.org/w/index.php?title=Control_flow&oldid=882692944#Count-controlled_loops)
- [Control variable (programming)](https://en.wikipedia.org/w/index.php?title=Control_variable_(programming)&oldid=868177931)
- [Data (computing)](https://en.wikipedia.org/w/index.php?title=Data_(computing)&oldid=881080086)
- [Data type](https://en.wikipedia.org/w/index.php?title=Data_type&oldid=879519751)
- [Data validation](https://en.wikipedia.org/w/index.php?title=Data_validation&oldid=880736882)
- [Declaration (computer programming)](https://en.wikipedia.org/w/index.php?title=Declaration_(computer_programming)&oldid=839247186)
- [Do while loop](https://en.wikipedia.org/w/index.php?title=Do_while_loop&oldid=870917166)
- [Entity](https://en.wikipedia.org/w/index.php?title=Entity&oldid=880867147)
- [Entry point](https://en.wikipedia.org/w/index.php?title=Entry_point&oldid=881544189)
- [Expression (computer science)](https://en.wikipedia.org/w/index.php?title=Expression_(computer_science)&oldid=878391104)
- [For loop](https://en.wikipedia.org/w/index.php?title=For_loop&oldid=876221986).
- [For loop§Loop counters](https://en.wikipedia.org/w/index.php?title=For_loop&oldid=876221986#Loop_counters)
- [Free software](https://en.wikipedia.org/w/index.php?title=Free_software&oldid=882024123)
- [Greenfield project](https://en.wikipedia.org/w/index.php?title=Greenfield_project&oldid=859894075)
- [Identifier§In computer languages](https://en.wikipedia.org/w/index.php?title=Identifier&oldid=882722496#In_computer_languages)
- [Identifier§In computer science](https://en.wikipedia.org/w/index.php?title=Identifier&oldid=882722496#In_computer_science)
- [Increment and decrement operators](https://en.wikipedia.org/w/index.php?title=Increment_and_decrement_operators&oldid=879445217)
- [Intelligence](https://en.wikipedia.org/w/index.php?title=Intelligence&oldid=888776338)
- [Lexical analysis§Token](https://en.wikipedia.org/w/index.php?title=Lexical_analysis&oldid=872271284).
- [Literal (computer programming)](https://en.wikipedia.org/w/index.php?title=Literal_(computer_programming)&oldid=849448036)
- [Logical connective](https://en.wikipedia.org/w/index.php?title=Logical_connective&oldid=881652068)
- [Object (computer science)](https://en.wikipedia.org/w/index.php?title=Object_(computer_science)&oldid=875165207)
- [Obsolescence](https://en.wikipedia.org/w/index.php?title=Obsolescence&oldid=886476203)
- [Octet (computing)](https://en.wikipedia.org/w/index.php?title=Octet_(computing)&oldid=852309529)
- [Operators in C and C++§Logical operators](https://en.wikipedia.org/w/index.php?title=Operators_in_C_and_C++&oldid=879923250#Logical_operators)
- [Nesting (computing)](https://en.wikipedia.org/w/index.php?title=Nesting_(computing)&oldid=877015415)
- [Operand§Computer science](https://en.wikipedia.org/w/index.php?title=Operand&oldid=874322196#Computer_science)
- [Operator (computer programming)](https://en.wikipedia.org/w/index.php?title=Operator_(computer_programming)&oldid=879934681)
- [Operator associativity](https://en.wikipedia.org/w/index.php?title=Operator_associativity&oldid=876220651)
- [Random access](https://en.wikipedia.org/w/index.php?title=Random_access&oldid=863225048)
- [Relational operator](https://en.wikipedia.org/w/index.php?title=Relational_operator&oldid=874050383)
- [Running total](https://en.wikipedia.org/w/index.php?title=Running_total&oldid=855615611)
- [Sentinel value](https://en.wikipedia.org/w/index.php?title=Sentinel_value&oldid=866344491)
- [Sequential access](https://en.wikipedia.org/w/index.php?title=Sequential_access&oldid=877118050)
- [Statement (computer science)](https://en.wikipedia.org/w/index.php?title=Statement_(computer_science)&oldid=863825665)
- [Symbol rate§Symbols](https://en.wikipedia.org/w/index.php?title=Symbol_rate&oldid=870702760#Symbols)
- [Subroutine](https://en.wikipedia.org/w/index.php?title=Subroutine&oldid=879018923)
- [Subroutine§C and C++ examples](https://en.wikipedia.org/w/index.php?title=Subroutine&oldid=883485600#C_and_C++_examples)
- [Switch statement](https://en.wikipedia.org/w/index.php?title=Switch_statement&oldid=866307445)
- [Syntax highlighting](https://en.wikipedia.org/w/index.php?title=Syntax_highlighting&oldid=887459958)
- [System](https://en.wikipedia.org/w/index.php?title=System&oldid=887887227)
- [Text file](https://en.wikipedia.org/w/index.php?title=Text_file&oldid=881932349)
- [Value (computer science)§Assignment: l-values and r-values](https://en.wikipedia.org/w/index.php?title=Value_(computer_science)&oldid=803728831)
- [Variable (computer science)](https://en.wikipedia.org/w/index.php?title=Variable_(computer_science)&oldid=882244717)
- [While loop](https://en.wikipedia.org/w/index.php?title=While_loop&oldid=881424645)
- [?:](https://en.wikipedia.org/w/index.php?title=%3F:&oldid=880334289)

on Wikipedia, with changes made, and:

- [Control structures](https://en.wikiversity.org/w/index.php?title=Control_structures&oldid=1856357)

on Wikiversity, with changes made, and:

- [arity](https://en.wiktionary.org/w/index.php?title=arity&oldid=50758406)
- [associativity](https://en.wiktionary.org/w/index.php?title=associativity&oldid=49893698)
- [atomicity](https://en.wiktionary.org/w/index.php?title=atomicity&oldid=50343477)
- [condition](https://en.wiktionary.org/w/index.php?title=condition&oldid=51410719)
- [conditional](https://en.wiktionary.org/w/index.php?title=conditional&oldid=51276861)
- [constant](https://en.wiktionary.org/w/index.php?title=constant&oldid=51246036)
- [counter](https://en.wiktionary.org/w/index.php?title=counter&oldid=51103193)
- [decrement§verb](https://en.wiktionary.org/w/index.php?title=decrement&oldid=50276969#Verb)
- [file](https://en.wiktionary.org/w/index.php?title=file&oldid=51417152)
- [flag](https://en.wiktionary.org/w/index.php?title=flag&oldid=51372941)
- [increment§verb](https://en.wiktionary.org/w/index.php?title=increment&oldid=51035067#Verb)
- [iteration](https://en.wiktionary.org/w/index.php?title=iteration&oldid=51175255)
- [lvalue](https://en.wiktionary.org/w/index.php?title=lvalue&oldid=50837189)
- [performant](https://en.wiktionary.org/w/index.php?title=performant&oldid=51350068)
- [playback](https://en.wiktionary.org/w/index.php?title=playback&oldid=50652068)
- [rabbit hole](https://en.wiktionary.org/w/index.php?title=rabbit_hole&oldid=51654654)
- [syntax highlighting](https://en.wiktionary.org/w/index.php?title=syntax_highlighting&oldid=47903468)
- [truncate](https://en.wiktionary.org/w/index.php?title=truncate&oldid=51196049)
- [vacuous](https://en.wiktionary.org/w/index.php?title=vacuous&oldid=47613271)

on Wiktionary, with changes made, and:

- [an answer on Stack Overflow by sbi](https://stackoverflow.com/questions/1410563/what-is-the-difference-between-a-definition-and-a-declaration/1410632#1410632)

on Stack Overflow, with changes made, and:

- [Basic concepts](https://en.cppreference.com/mwiki/index.php?title=cpp/language/basic_concepts&oldid=108663)
- [Declarations](https://en.cppreference.com/mwiki/index.php?title=cpp/language/declarations&oldid=107424)
- [Definitions and ODR](https://en.cppreference.com/mwiki/index.php?title=cpp/language/definition&oldid=108342)
- [Variables](https://en.cppreference.com/bookwiki/index.php?title=intro/variables&oldid=870)
- [Variables§Identifiers](https://en.cppreference.com/bookwiki/index.php?title=intro/variables&oldid=870#Identifiers)
- [Variables§Variables in C++](https://en.cppreference.com/bookwiki/index.php?title=intro/variables&oldid=870#Variables_in_C.2B.2B)

on cppreference.com, with changes made.

[^runningtotaldef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Running_total).
[^abstractiondef-note1]: This definition is based on information from [Wikipedia's definition of “abstraction”](https://en.wikipedia.org/wiki/Abstraction_(disambiguation)).
[^accumulatordef-note1]: This definition is based on [an answer on Stack Overflow by Alberto Moriconi](https://stackoverflow.com/questions/12983063/what-is-the-difference-between-a-counter-and-an-accumulator/12983603#12983603) and on information from page 257 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^aritydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/arity), except for the removal of the words “[arguments](https://en.wiktionary.org/wiki/argument)” and “[operation](https://en.wiktionary.org/wiki/operation)”, which do not seem to apply in a computer science context.
[^arraydef-note1]: This definition is based on information from [Wikipedia's definition of an array in the context of computer science](https://en.wikipedia.org/wiki/Array#Computer_science).
[^arraydatastructuredef-note1]: This definition is based on information from [Wikipedia's definition of “array data structure”](https://en.wikipedia.org/wiki/Array_data_structure).
[^arraydatastructuredef1]: Black, Paul E. (13 November 2008). ["array"](https://xlinux.nist.gov/dads/HTML/array.html). *[Dictionary of Algorithms and Data Structures](https://en.wikipedia.org/wiki/Dictionary_of_Algorithms_and_Data_Structures)*. [National Institute of Standards and Technology](https://en.wikipedia.org/wiki/National_Institute_of_Standards_and_Technology). Retrieved 22 August 2010.
[^arraydatastructuredef2]: Bjoern Andres; Ullrich Koethe; Thorben Kroeger; Hamprecht (2010). "Runtime-Flexible Multi-dimensional Arrays and Views for C++98 and C++0x". [arXiv](https://en.wikipedia.org/wiki/ArXiv):[1008.2909](https://arxiv.org/abs/1008.2909) \[[cs.DS](https://arxiv.org/archive/cs.DS)\].
[^arraydatastructuredef3]: Garcia, Ronald; Lumsdaine, Andrew (2005). "MultiArray: a C++ library for generic programming with arrays". *Software: Practice and Experience*. **35** (2): 159–188. [doi](https://en.wikipedia.org/wiki/Digital_object_identifier):[10.1002/spe.630](https://doi.org/10.1002%2Fspe.630). [ISSN](https://en.wikipedia.org/wiki/International_Standard_Serial_Number) [0038-0644](https://www.worldcat.org/issn/0038-0644).
[^arraydatastructuredef4]: David R. Richardson (2002), The Book on Data Structures. iUniverse, 112 pages. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [0-595-24039-9](https://en.wikipedia.org/wiki/Special:BookSources/0-595-24039-9) [978-0-595-24039-5](https://en.wikipedia.org/wiki/Special:BookSources/978-0-595-24039-5).
[^arraydatastructuredef5]: Veldhuizen, Todd L. (December 1998). [*Arrays in Blitz++*](http://ubietylab.net/ubigraph/content/Papers/pdf/BlitzArrays.pdf) (PDF). Computing in Object-Oriented Parallel Environments. Lecture Notes in Computer Science. **1505**. Springer Berlin Heidelberg. pp. 223–230. [doi](https://en.wikipedia.org/wiki/Digital_object_identifier):[10.1007/3-540-49372-7\_24](https://doi.org/10.1007%2F3-540-49372-7_24). [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [978-3-540-65387-5](https://en.wikipedia.org/wiki/Special:BookSources/978-3-540-65387-5).
[^assignmentconstructdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Assignment_(computer_science)).
[^assignmentoperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Assignment_operator_(C++)).
[^associativitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/associativity).
[^atomicitydef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/atomicity).
[^augmentedassignmentoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Augmented_assignment).
[^binaryfiledef1]: ["Binary file definition by The Linux Information Project (LINFO)"](http://www.linfo.org/binary_file.html). *www.linfo.org*. Retrieved 2017-10-12.
[^binaryfiledef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Binary_file).
[^blockdef-note1]: This definition is based on [Wikipedia's definition of a block as a page](https://en.wikipedia.org/wiki/Block_(programming)) and [as a section of a page](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Blocks).
[^Booleandatatypedef-note1]: This definition is based on [Wikipedia's definition of Boolean data type](https://en.wikipedia.org/wiki/Boolean_data_type) and [Data type](https://en.wikipedia.org/wiki/Data_type).
[^Booleandef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Boolean_data_type).
[^calculatedef1]: ["calculate | Definition of calculate in English by Oxford Dictionaries"](https://en.oxforddictionaries.com/definition/calculate). *Oxford Dictionaries | English*. Retrieved 2018-08-30.
[^calculatedef-note1]: This definition is based on information from [the “Calculation” page on Wikipedia](https://en.wikipedia.org/wiki/Calculation).
[^conditionaldef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/conditional).
[^conditionalexpressiondef1]: Based on information from page 199 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^conditionaloperatordef1]: Cogwheel. ["What is the difference between logical and conditional /operator/"](https://stackoverflow.com/questions/3154132/what-is-the-difference-between-logical-and-conditional-and-or-in-c). *Stack Overflow.* Retrieved 9 April 2015.
[^conditionaloperatordef-note1]: This definition is based on a definition from [Wikipedia](https://en.wikipedia.org/wiki/Conditional_operator).
[^conditionaloperatordef-note2]: This definition is based on a definition from [Wikipedia](https://en.wikipedia.org/wiki/%3F:).
[^conditioncontrolledloopconstructdef-note1]: This definition is loosely based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Control_flow#Condition-controlled_loops).
[^conditiondef-note1]: This definition is based on definitions from [Wiktionary](https://en.wiktionary.org/wiki/condition) and [Wikipedia](https://en.wikipedia.org/wiki/Conditional_(computer_programming)).
[^constantdef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/constant).
[^controlflowdef-note1]: This definition is based on information from [Wikipedia's definition of “control flow”](https://en.wikipedia.org/wiki/Control_flow).
[^controlstructuredef-note1]: This definition is based on information from [the “Category:Control Structures” page on Rosetta Code](https://rosettacode.org/wiki/Category:Control_Structures), [Control structures and statements in C and C++](http://www.circuitstoday.com/control-structures-in-c-and-cpp), and [Wikiversity's definition of “control structure”](https://en.wikiversity.org/wiki/Control_structures).
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
[^declarationdef1]:
    "A declaration specifies the interpretation and attributes of a set of identifiers. A *definition* of an identifier is a declaration for that identifier that:

    - for an object [variable or constant], causes storage to be reserved for that object;
    - for a function, includes the function body;
    - for an enumeration constant, is the (only) declaration of the identifier;
    - for a typedef name, is the first (or only) declaration of the identifier."

    C11 specification, 6.7: Declarations, paragraph 5.
[^declarationdef2]: Mike Banahan. ["2.5. Declaration of variables"](http://publications.gbdirect.co.uk/c_book/chapter2/variable_declaration.html). <http://publications.gbdirect.co.uk/c_book/>: GBdirect. Retrieved 2011-06-08. “[A] declaration [...] introduces just the name and type of something but allocates no storage[...].”
[^declarationdef-note1]: This definition is based on [Wikipedia's definition of a declaration](https://en.wikipedia.org/wiki/Declaration_(computer_programming)) and [an answer on Stack Overflow by sbi](https://stackoverflow.com/questions/1410563/what-is-the-difference-between-a-definition-and-a-declaration/1410632#1410632).
[^declarationdef-note2]: This definition is based on information from [the “Declarations” page on cppreference.com](https://en.cppreference.com/w/cpp/language/declarations).
[^decrementoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Increment_and_decrement_operators).
[^decrementoperatordef-note2]: Based on information from page 231 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^decrementdef-note1]: This definition is based on [Wiktionary's definition of “increment”](https://en.wiktionary.org/wiki/increment#Verb) and [Wiktionary's definition of “decrement”](https://en.wiktionary.org/wiki/decrement#Verb).
[^definitiondef-note1]: This definition is based on [Wikipedia's definition of a declaration](https://en.wikipedia.org/wiki/Declaration_(computer_programming)) and [an answer on Stack Overflow by sbi](https://stackoverflow.com/questions/1410563/what-is-the-difference-between-a-definition-and-a-declaration/1410632#1410632).
[^definitiondef-note2]: This definition is based on information from [the “Definitions and ODR” page on cppreference.com](https://en.cppreference.com/w/cpp/language/definition).
[^directaccessdef1]: National Computer Conference and Exposition (1957). [*Proceedings*](https://books.google.com/books?id=lQQrAQAAIAAJ). Retrieved 2 October 2013.
[^directaccessdef2]: International Business Machines Corporation. Data Processing Division (1966). [*Introduction to IBM Direct-access Storage Devices and Organization Methods*](https://books.google.com/books?id=i6vWAAAAMAAJ&pg=SA3-PA24). International Business Machines Corporation. pp. 3–. Retrieved 2 October 2013.
[^directaccessdef3]: D. E. KNUTH (1969). [*The Art of Computer Programming. Vol. 3. Sorting and Searching*](https://books.google.com/books?id=ZQu9mgEACAAJ). Addison-Wesley. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [978-0-201-03803-3](https://en.wikipedia.org/wiki/Special:BookSources/978-0-201-03803-3). Retrieved 2 October 2013.
[^directaccessdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Random_access).
[^dowhileloopconstructdef-note1]: This definition is based on [Wikipedia's definition of “Do while loop”](https://en.wikipedia.org/wiki/Do_while_loop) and [Wikipedia's definition of “While loop”](https://en.wikipedia.org/wiki/While_loop).
[^entitydef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entity).
[^entitydef-note2]: This definition is based on information from [the “Basic concepts” page on cppreference.com](https://en.cppreference.com/w/cpp/language/basic_concepts).
[^entitydef-note3]: This definition is based on [Wikipedia's definition of a declaration](https://en.wikipedia.org/wiki/Declaration_(computer_programming)) and [Wikipedia's definition of an identifier](https://en.wikipedia.org/wiki/Identifier).
[^entrypointdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Entry_point), with some rewording.
[^expressiondef1]: [Javascript expressions, Mozilla](https://developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Expressions) Accessed July 6, 2009]
[^expressiondef2]: [Programming in C](https://www.cs.drexel.edu/~rweaver/COURSES/ISTC-2/TOPICS/expr.html) Accessed July 6, 2009
[^expressiondef-note1]: This definition is similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Expression_(computer_science)), with changes made.
[^filedef-note1]: This definition is based on [Wiktionary's definition](https://en.wiktionary.org/wiki/file) and [Wikipedia's definition](https://en.wikipedia.org/wiki/Computer_file).
[^flagdef-note1]: This definition is based on [Wiktionary's definition](https://en.wiktionary.org/wiki/flag#Noun).
[^forloopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/For_loop).
[^forloopconstructdef-note2]: Based on information from page 251 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^conditionalexpressiondef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then%E2%80%93else_expressions).
[^forloopconstructdef1]: <https://en.cppreference.com/w/cpp/language/for>
[^glossry1]: <https://en.cppreference.com/w/Cppreference:FAQ>
[^greenfieldprojectdef1]: Gupta, Rajeev (2011). *Project Management*. Prentice-Hall of India. p. 21. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [978-8120344259](https://en.wikipedia.org/wiki/Special:BookSources/978-8120344259).
[^greenfieldprojectdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Greenfield_project).
[^identifierdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Identifier).
[^identifierdef-note2]: This definition is based on [a definition from the “Identifiers” section of the “Variables” page on cppreference.com](https://en.cppreference.com/book/intro/variables#Identifiers).
[^iforelseorelseiforclausedef-note1]: This definition is based on [an answer on Stack Overflow by tvanfosson](https://stackoverflow.com/questions/4877903/the-term-clause-in-the-context-of-programming/4877948#4877948).
[^iforelseorelseiforclausedef-note2]: This definition is based on [an answer on Software Engineering Stack Exchange by Robert Harvey](https://softwareengineering.stackexchange.com/questions/234331/in-an-if-statement-what-are-an-if-clause-and-a-then-clause/234337#234337).
[^ifconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then(%E2%80%93else)).
[^ifconstructdef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#Else_if)
[^incrementdef-note1]: This definition is based on [Wiktionary's definition of “increment”](https://en.wiktionary.org/wiki/increment#Verb) and [Wiktionary's definition of “decrement”](https://en.wiktionary.org/wiki/decrement#Verb).
[^incrementoperatordef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Increment_and_decrement_operators).
[^incrementoperatordef-note2]: Based on information from page 231 of “Starting Out with C++: From Control through Objects - Edition: 8th”, ISBN 978-0-13-4037325.
[^intelligencedef-note1]: This definition is based on information from [the “Intelligence” page on Wikipedia](https://en.wikipedia.org/wiki/Intelligence).
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
[^objectdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Object_(computer_science)).
[^obsolescencedef-note1]: This definition is based on information from [Wikipedia's definition of “obsolescence”](https://en.wikipedia.org/wiki/Obsolescence).
[^octetdef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Octet_(computing)), except for the removal of the phrase “in [computing](https://en.wikipedia.org/wiki/Computing) and [telecommunications](https://en.wikipedia.org/wiki/Telecommunications)”.
[^operanddef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operand#Computer_science).
[^operatordef-note1]: This definition is the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Operator_(computer_programming), except for modification of the grammatical number (plural to singular).
[^operatordef-note2]: Based on [information from Wikipedia](https://en.wikipedia.org/wiki/Operator_associativity).
[^performantdef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/performant).
[^playbackdef-note1]: This definition is the same as [Wiktionary's definition of “playback”](https://en.wikipedia.org/wiki/Array_data_structure).
[^programmaticalfreedomdef-note1]: This definition is based on [Wikipedia's definition of free software](https://en.wikipedia.org/wiki/Free_software) and [Wikipedia's definition of freedom](https://en.wikipedia.org/wiki/Freedom).
[^programmaticalfreedomdef-note2]: This definition is based on [the GNU prject's definition of free software](https://www.gnu.org/philosophy/free-sw.html.en).
[^rabbitholedef-note1]: This definition is based on information from [Wiktionary's definition of “rabbit hole”](https://en.wiktionary.org/wiki/rabbit_hole).
[^relationalexpressiondef-note1]: This definition similar to [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^relationaloperatordef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Relational_operator).
[^rvaluedef1]: ["Lvalues and Rvalues (Visual C++)"](https://msdn.microsoft.com/en-us/library/f90831hc.aspx). *Microsoft Developer Network.* Retrieved 3 September 2016.
[^rvaluedef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Value_(computer_science)#Assignment:_l-values_and_r-values).
[^sentinelvaluedef1]: [Knuth, Donald](https://en.wikipedia.org/wiki/Donald_Knuth) (1973). *The Art of Computer Programming, Volume 1: Fundamental Algorithms (second edition)*. [Addison-Wesley](https://en.wikipedia.org/wiki/Addison-Wesley). pp. 213–214, also p. 631. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [0-201-03809-9](https://en.wikipedia.org/wiki/Special:BookSources/0-201-03809-9).
[^sentinelvaluedef-note1]: This definition is based on [Wikipedia's definition of a sentinel value](https://en.wikipedia.org/wiki/Sentinel_value) and [an answer on Stack Overflow by Tony the Pony](https://stackoverflow.com/questions/21666508/can-someone-explain-to-me-what-a-sentinel-does-in-java-or-how-it-works/21666543#21666543).
[^separatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement separator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^sequentialaccessdef1]: [Random and Sequential Data Access](https://technet.microsoft.com/en-us/library/cc938619.aspx), Microsoft TechNet
[^sequentialaccessdef2]: *Irfan Ahmad*, [Easy and Efficient Disk I/O Workload Characterization in VMware ESX Server](http://www.vmware.com/files/pdf/iiswc_2007_distribute.pdf), IISWC, 2007.
[^sequentialaccessdef3]: *Eric Anderson*, [Capture, Conversion, and Analysis of an Intense NFS Workload](https://www.usenix.org/legacy/event/fast09/tech/full_papers/anderson/anderson.pdf), FAST, 2009.
[^sequentialaccessdef4]: *Yanpei Chen et al.* [Design Implications for Enterprise Storage Systems via Multi-dimensional Trace Analysis](http://dl.acm.org/citation.cfm?id=2043562). SOSP. 2011
[^sequentialaccessdef5]: *Andrew Leung et al.* [Measurement and Analysis of Large-scale Network File System Workloads](http://www.ssrc.ucsc.edu/Papers/leung-usenix08.pdf). USENIX ATC. 2008
[^sequentialaccessdef6]: *Frank Schmuck and Roger Haskin*, [GPFS: A Shared-Disk File System for Large Computing Clusters](https://www.usenix.org/legacy/events/fast02/full_papers/schmuck/schmuck.pdf), FAST. 2002
[^sequentialaccessdef7]: *Alan Smith*. [Sequentiality and Prefetching in Database Systems](http://www-inst.eecs.berkeley.edu/~cs266/sp10/readings/smith78.pdf). ACM TOS
[^sequentialaccessdef8]: *Hyong Shim et al.* [Characterization of Incremental Data Changes for Efficient Data Protection](http://0b4af6cdc2f0c5998459-c0245c5c937c5dedcca3f1764ecc9b2f.r43.cf2.rackcdn.com/11747-atc13-shim.pdf). USENIX ATC. 2013.
[^sequentialaccessdef9]: *Avishay Traeger et al.* [A Nine Year Study of File System and Storage Benchmarking](http://www.fsl.cs.sunysb.edu/docs/fsbench/fsbench.pdf). ACM TOS. 2007.
[^sequentialaccessdef10]: *Cheng Li et al.* [Assert(!Defined(Sequential I/O))](https://www.usenix.org/node/183622). HotStorage. 2014
[^sequentialaccessdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Sequential_access)
[^statementdef1]: ["statement"](http://www.webopedia.com/TERM/S/statement.html). webopedia. Retrieved 2015-03-03.
[^statementdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Statement_(computer_science)).
[^statementdef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then%E2%80%93else_expressions).
[^statementdef-note3]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Conditional_(computer_programming)#If%E2%80%93then(%E2%80%93else)).
[^subroutinedef1]: [U.S. Election Assistance Commission](https://en.wikipedia.org/wiki/Election_Assistance_Commission "Election Assistance Commission") (2007). ["Definitions of Words with Special Meanings"](https://web.archive.org/web/20121208084203/http://www.eac.gov/vvsg/glossary.aspx). *[Voluntary Voting System Guidelines](https://en.wikipedia.org/wiki/Voluntary_Voting_System_Guidelines "Voluntary Voting System Guidelines")*. Archived from [the original](http://www.eac.gov/vvsg/glossary.aspx) on 2012-12-08. Retrieved 2013-01-14.
[^subroutinedef2]: [""what is meant by a free function""](https://stackoverflow.com/questions/4861914/what-is-the-meaning-of-the-term-free-function-in-c).
[^subroutinedef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Subroutine), with some rewording.
[^subroutinedef-note2]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Subroutine#C_and_C++_examples).
[^switchconstructdef-note1]: This definition is essentially the same as [Wikipedia's definition](https://en.wikipedia.org/wiki/Switch_statement).
[^symboldef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Symbol_rate#Symbols).
[^syntaxhighlightingdef-note1]: This definition is based on information from [the “Syntax highlighting” page on Wikipedia](https://en.wikipedia.org/wiki/Syntax_highlighting) and [the “syntax highlighting” page on Wiktionary](https://en.wiktionary.org/wiki/syntax_highlighting).
[^systemdef1]: ["Definition of system"](http://www.merriam-webster.com/dictionary/system). *Merriam-Webster*. Springfield, MA, USA. Retrieved 2019-01-13.
[^systemdef-note1]: This definition is based on information from [the “System” page on Wikipedia](https://en.wikipedia.org/wiki/System).
[^terminatordef-note1]: This definition is based on [Wikipedia's definition of a token](https://en.wikipedia.org/wiki/Lexical_analysis#Token) and [Wikipedia's definition of a statement terminator](https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#Statements).
[^textfiledef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/Text_file).
[^trailingdef]: <https://stackoverflow.com/questions/22273233/what-is-meant-by-trailing-space-and-whats-the-difference-between-it-and-a-blank/22273264#22273264>
[^truncatedef-note1]: This definition is essentially the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/truncate).
[^vacuousdef-note1]: This definition is the same as [Wiktionary's definition](https://en.wiktionary.org/wiki/vacuous).
[^valuedef-note1]: This definition is based on information from [Wikipedia's definition of a variable](https://en.wikipedia.org/wiki/Variable_(computer_science)).
[^variabledef1]: *[Compilers: Principles, Techniques, and Tools](https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools)*, pp. 26–28
[^variabledef2]: Knuth, Donald (1997). *The Art of Computer Programming*. **1** (3rd ed.). Reading, Massachusetts: Addison-Wesley. p. 3-4. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [0-201-89683-4](https://en.wikipedia.org/wiki/Special:BookSources/0-201-89683-4).
[^variabledef-note1]: This definition is based on [a definition from the “Variables” page on cppreference.com](https://en.cppreference.com/book/intro/variables) and [a definition from Wikipedia's “Variable (computer science” page](https://en.wikipedia.org/wiki/Variable_(computer_science)).
[^variabledef-note2]: This definition is based on [a definition from the “Variables in C++” section of the “Variables” page on cppreference.com](https://en.cppreference.com/book/intro/variables#Variables_in_C.2B.2B)
[^whileloopconstructdef1]: ["The while and do-while Statements (The Java™ Tutorials > Learning the Java Language > Language Basics)"](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html). *Dosc.oracle.com*. Retrieved 2016-10-21.
[^whileloopconstructdef2]: ["while (C# reference)"](http://msdn.microsoft.com/en-us/library/2aeyhxcd.aspx). *Msdn.microsoft.com*. Retrieved 2016-10-21.
[^whileloopconstructdef-note1]: This definition is based on [Wikipedia's definition](https://en.wikipedia.org/wiki/While_loop).
