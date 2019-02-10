# C++ reference
## operators

This is a list of [operators](https://en.wikipedia.org/wiki/Operator_(programming)) in the [C](https://en.wikipedia.org/wiki/C_(programming_language)) and [C++](https://en.wikipedia.org/wiki/C++) [programming languages](https://en.wikipedia.org/wiki/Programming_language). All the operators listed exist in C++; the fourth column “Included in C”, states whether an operator is also present in C. Note that C does not support [operator overloading](https://en.wikipedia.org/wiki/Operator_overloading).

When not overloaded, for the operators `&&`, `||`, and `,` (the [comma operator](https://en.wikipedia.org/wiki/Comma_operator)), there is a [sequence point](https://en.wikipedia.org/wiki/Sequence_point) after the evaluation of the first operand.

C++ also contains the [type conversion](https://en.wikipedia.org/wiki/Type_conversion "Type conversion") operators `const_cast`, `static_cast`, `dynamic_cast`, and `reinterpret_cast`. The formatting of these operators means that their precedence level is unimportant.

Most of the operators available in C and C++ are also available in other languages such as [C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)), [D](https://en.wikipedia.org/wiki/D_(programming_language)), [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [Perl](https://en.wikipedia.org/wiki/Perl), and [PHP](https://en.wikipedia.org/wiki/PHP) with the same precedence, associativity, and semantics.

For the purposes of these tables, `a`, `b`, and `c` represent valid values (literals, values from variables, or return value), object names, or lvalues, as appropriate. `R`, `S` and `T` stand for any type(s), and `K` for a class type or enumerated type.

| Type                  | Name                                                                            | Syntax                                                 | Can overload in C++ | Included in [C] | C++ prototype example: as member of K | C++ prototype example: outside class definitions
|:----------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------|:--------------------|:----------------|:-|:-
| arithmetic            | [Basic assignment]                                                              | `a = b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R& K::operator =(S b);` | N/A
| arithmetic            | [Addition]                                                                      | `a + b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator +(S b);` | `R operator +(K a, S b);`
| arithmetic            | [Subtraction]                                                                   | `a - b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator -(S b);` | `R operator -(K a, S b);`
| arithmetic            | [Unary] plus ([integer promotion])                                              | `+a`                                                   | Yes{: .yes}         | Yes{: .yes}     | `R K::operator +();` | `R operator +(K a);`
| arithmetic            | Unary minus ([additive inverse])                                                | `-a`                                                   | Yes{: .yes}         | Yes{: .yes}     | `R K::operator -();` | `R operator -(K a);`
| arithmetic            | [Multiplication]                                                                | `a * b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator *(S b);` | `R operator *(K a, S b);`
| arithmetic            | [Division]                                                                      | `a / b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator /(S b);` | `R operator /(K a, S b);`
| arithmetic            | [Modulo] (integer remainder)[^Cpprefr-note1]                                    | `a % b`                                                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator %(S b);` | `R operator %(K a, S b);`
| arithmetic            | [Increment] prefix                                                              | `++a`                                                  | Yes{: .yes}         | Yes{: .yes}     | `R& K::operator ++();` | `R& operator ++(K& a);`
| arithmetic            | [Increment] postfix                                                             | `a++`                                                  | Yes{: .yes}         | Yes{: .yes}     | `R K::operator ++(int);`[^Cpprefr-note2] | `R operator ++(K& a, int);`[^Cpprefr-note2]
| arithmetic            | [Decrement] Prefix                                                              | `--a`                                                  | Yes{: .yes}         | Yes{: .yes}     | `R& K::operator --();` | `R& operator --(K& a);`
| arithmetic            | [Decrement] Postfix                                                             | `a--`                                                  | Yes{: .yes}         | Yes{: .yes}     | `R K::operator --(int);`[^Cpprefr-note3] | `R operator --(K& a, int);`[^Cpprefr-note3]
| bitwise               | [Bitwise NOT]                                                                   | `~a`<br>`compl a`[^Cpprefr-note4]                      | Yes{: .yes}         | Yes{: .yes}     | `R K::operator ~();` | `R operator ~(K a);`
| bitwise               | [Bitwise AND]                                                                   | `a & b`<br>`a bitand b`[^Cpprefr-note4]                | Yes{: .yes}         | Yes{: .yes}     | `R K::operator &(S b);` | `R operator &(K a, S b);`
| bitwise               | [Bitwise OR]                                                                    | `a | b`<br>`a bitor b`[^Cpprefr-note4]                 | Yes{: .yes}         | Yes{: .yes}     | `R K::operator |(S b);` | `R operator |(K a, S b);`
| bitwise               | [Bitwise XOR]                                                                   | `a ^ b`<br>`a xor b`[^Cpprefr-note4]                   | Yes{: .yes}         | Yes{: .yes}     | `R K::operator ^(S b);` | `R operator ^(K a, S b);`
| bitwise               | [Bitwise left shift] [^Cpprefr-note5]                                           | `a << b`                                               | Yes{: .yes}         | Yes{: .yes}     | `R K::operator <<(S b);` | `R operator <<(K a, S b);`
| bitwise               | [Bitwise right shift] [^Cpprefr-note5] [^Cpprefr-note6]                         | `a >> b`                                               | Yes{: .yes}         | Yes{: .yes}     | `R K::operator >>(S b);` | `R operator >>(K a, S b);`
| comparison/relational | Equal to                                                                        | `a == b`                                               | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator ==(S const& b);` | `bool operator ==(K const& a, S const& b);`
| comparison/relational | Not equal to                                                                    | `a != b`<br>`a not_eq b`[^Cpprefr-note4]               | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator !=(S const& b);` `bool K::operator !=(S const& b) const;` | `bool operator !=(K const& a, S const& b);`
| comparison/relational | Greater than                                                                    | `a > b`                                                | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator >(S const& b) const;` | `bool operator >(K const& a, S const& b);`
| comparison/relational | Less than                                                                       | `a < b`                                                | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator <(S const& b)const;` | `bool operator <(K const& a, S const& b);`
| comparison/relational | Greater than or equal to                                                        | `a >= b`                                               | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator >=(S const& b) const;` | `bool operator >=(K const& a, S const& b);`
| comparison/relational | Less than or equal to                                                           | `a <= b`                                               | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator <=(S const& b);` | `bool operator <=(K const& a, S const& b);`
| logical               | [Logical negation (NOT)]                                                        | `!a`<br>`not a`[^Cpprefr-note4]                        | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator !();` | `bool operator !(K a);`
| logical               | [Logical AND]                                                                   | `a && b`<br>`a and b`[^Cpprefr-note4]                  | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator &&(S b);` | `bool operator &&(K a, S b);`
| logical               | [Logical OR]                                                                    | `a || b`<br>`a or b`[^Cpprefr-note4]                   | Yes{: .yes}         | Yes{: .yes}     | `bool K::operator ||(S b);` | `bool operator ||(K a, S b);`
| member and pointer    | [Subscript]                                                                     | `a[b]`                                                 | Yes{: .yes}         | Yes{: .yes}     | `R& K::operator [](S b);` | N/A
| member and pointer    | Indirection (“object pointed to by *a*”)                                        | `*a`                                                   | Yes{: .yes}         | Yes{: .yes}     | `R& K::operator *();` | `R& operator *(K a);`
| member and pointer    | Address-of (“address of *a*”)                                                   | `&a`                                                   | Yes{: .yes}         | Yes{: .yes}     | `R* K::operator &();` | `R* operator &(K a);`
| member and pointer    | Structure dereference (“member *b* of object pointed to by *a*”)                | `a->b`                                                 | Yes{: .yes}         | Yes{: .yes}     | `R* K::operator ->();`[^Cpprefr-note7] | N/A
| member and pointer    | Structure reference (“member *b* of object *a*”)                                | `a.b`                                                  | No{: .no}           | Yes{: .yes}     | N/A | N/A
| member and pointer    | Member selected by pointer-to-member *b* of object pointed to by *a*[^Cpprefr3] | `a->*b`                                                | Yes{: .yes}         | No{: .no}       | `R& K::operator ->*(S b);` | `R& operator ->*(K a, S b);`
| member and pointer    | Member of object *a* selected by pointer-to-member *b*                          | `a.*b`                                                 | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [Function] call (see [Function object])                                         | `a(a1, a2)`                                            | Yes{: .yes}         | Yes{: .yes}     | `R K::operator ()(S a, T b, ...);` | N/A
| other                 | [Comma]                                                                         | `a, b`                                                 | Yes{: .yes}         | Yes{: .yes}     | `R K::operator ,(S b);` | `R operator ,(K a, S b);`
| other                 | [Ternary conditional]                                                           | `a ? b : c`                                            | No{: .no}           | Yes{: .yes}     | N/A | N/A
| other                 | [Scope resolution]                                                              | `a::b`                                                 | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | User-defined literals[^Cpprefr-note8] (since C++11)                             | `"a"_b`                                                | Yes{: .yes}         | No{: .no}       | N/A | `R operator "" _b(T a)`
| other                 | [Size-of]                                                                       | `sizeof (a)`[^Cpprefr-note9]<br>`sizeof (type)`        | No{: .no}           | Yes{: .yes}     | N/A | N/A
| other                 | Size of [parameter pack] (since C++11)                                          | `sizeof...(Args)`                                      | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | Align-of (since C++11)                                                          | `alignof (type)` or `_Alignof (type)`[^Cpprefr-note10] | No{: .no}           | Yes{: .yes}     | N/A | N/A
| other                 | Type identification                                                             | `typeid (a)`<br>`typeid (type)`                        | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [Conversion] (C-style cast)                                                     | `(type) a`                                             | No{: .no}           | Yes{: .yes}     | N/A | N/A
| other                 | [Conversion] [^Cpprefr-note11]                                                                   | `type(a)`                             | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [static_cast] conversion[^Cpprefr-note12]                                       | `static_cast<type>(a)`                                 | Yes{: .yes}         | No{: .no}       | `K::operator R();` | `explicit K::operator R();` (since C++11) | N/A
| other                 | [dynamic cast] conversion                                                       | `dynamic_cast<type>(a)`                                | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [const_cast] conversion                                                         | `const_cast<type>(a)`                                  | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [reinterpret_cast] conversion                                                   | `reinterpret_cast<type>(a)`                            | No{: .no}           | No{: .no}       | N/A | N/A
| other                 | [Allocate storage]                                                              | `new type`                                             | Yes{: .yes}         | No{: .no}       | `void* K::operator new(size_t x);` | `void* operator new(size_t x);`
| other                 | Allocate storage (array)                                                        | `new type[n]`                                          | Yes{: .yes}         | No{: .no}       | `void* K::operator new[](size_t a);` | `void* operator new[](size_t a);`
| other                 | [Deallocate storage]                                                            | `delete a`                                             | Yes{: .yes}         | No{: .no}       | `void K::operator delete(void *a);` | `void operator delete(void *a);`
| other                 | Deallocate storage (array)                                                      | `delete[] a`                                           | Yes{: .yes}         | No{: .no}       | `void K::operator delete[](void *a);` | `void operator delete[](void *a);`
| other                 | Exception check (since C++11)                                                   | `noexcept(a)`                                          | No{: .no}           | No{: .no}       | N/A | N/A

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [Operators in C and C++](https://en.wikipedia.org/wiki/Operators_in_C_and_C++) on Wikipedia, with changes made.

[Addition]: https://en.wikipedia.org/wiki/Addition
[Allocate storage]: https://en.wikipedia.org/wiki/New_(c++)
[Basic assignment]: https://en.wikipedia.org/wiki/Assignment_operator_in_C++
[Bitwise AND]: https://en.wikipedia.org/wiki/Bitwise_operation#AND
[Bitwise NOT]: https://en.wikipedia.org/wiki/Bitwise_operation#NOT
[Bitwise OR]: https://en.wikipedia.org/wiki/Bitwise_operation#OR
[Bitwise XOR]: https://en.wikipedia.org/wiki/Bitwise_operation#XOR
[Bitwise left shift]: https://en.wikipedia.org/wiki/Bitwise_shift
[Bitwise right shift]: https://en.wikipedia.org/wiki/Bitwise_shift
[C]: https://en.wikipedia.org/wiki/C_(programming_language)
[Comma]: https://en.wikipedia.org/wiki/Comma_operator
[Conversion]: https://en.wikipedia.org/wiki/Type_conversion
[Deallocate storage]: https://en.wikipedia.org/wiki/Operator_delete
[Decrement]: https://en.wikipedia.org/wiki/Increment_and_decrement_operators
[Division]: https://en.wikipedia.org/wiki/Division_(mathematics)
[Function object]: https://en.wikipedia.org/wiki/Function_object
[Function]: https://en.wikipedia.org/wiki/Function_(programming)
[Increment]: https://en.wikipedia.org/wiki/Increment_and_decrement_operators
[Logical AND]: https://en.wikipedia.org/wiki/Logical_conjunction
[Logical OR]: https://en.wikipedia.org/wiki/Logical_disjunction
[Logical negation (NOT)]: https://en.wikipedia.org/wiki/Negation
[Modulo]: https://en.wikipedia.org/wiki/Modulo_operation
[Multiplication]: https://en.wikipedia.org/wiki/Multiplication
[Scope resolution]: https://en.wikipedia.org/wiki/Scope_resolution_operator#C++
[Size-of]: https://en.wikipedia.org/wiki/Sizeof
[Subscript]: https://en.wikipedia.org/wiki/Indexer_(programming)
[Subtraction]: https://en.wikipedia.org/wiki/Subtraction
[Ternary conditional]: https://en.wikipedia.org/wiki/%3F:
[Unary]: https://en.wikipedia.org/wiki/Unary_operation
[additive inverse]: https://en.wikipedia.org/wiki/Additive_inverse
[const_cast]: https://en.wikipedia.org/wiki/Const_cast
[dynamic cast]: https://en.wikipedia.org/wiki/Dynamic_cast
[integer promotion]: https://en.wikipedia.org/wiki/Type_conversion#Type_promotion
[parameter pack]: https://en.wikipedia.org/wiki/Variadic_template
[reinterpret_cast]: https://en.wikipedia.org/wiki/Reinterpret_cast
[static_cast]: https://en.wikipedia.org/wiki/Static_cast
[^Cpprefr1]: "Integers implementation", [GCC 4.3.3](https://gcc.gnu.org/onlinedocs/gcc-4.3.3/gcc/Integers-implementation.html#Integers-implementation), GNU.
[^Cpprefr2]: [Explicit type conversion](http://en.cppreference.com/w/cpp/language/explicit_cast) in C++
[^Cpprefr3]: Meyers, Scott (Oct 1999), ["Implementing operator->\* for Smart Pointers"](http://aristeia.com/Papers/DDJ_Oct_1999.pdf) ([PDF](https://en.wikipedia.org/wiki/PDF)), *Dr.Dobbs*, Aristeia.
[^Cpprefr-note1]: The modulus operator works just with integer operands, for floating point numbers a library function must be used instead (like [`fmod`](https://en.wikipedia.org/wiki/Math.h)).
[^Cpprefr-note2]: [C++](https://en.wikipedia.org/wiki/C++) uses the unnamed dummy-parameter `int` to differentiate between prefix and postfix increment operators.
[^Cpprefr-note3]: [C++](https://en.wikipedia.org/wiki/C++) uses the unnamed dummy-parameter `int` to differentiate between prefix and postfix decrement operators.
[^Cpprefr-note4]: Requires `iso646.h` in C. See [C++ operator synonyms](#C.2B.2B_operator_synonyms)
[^Cpprefr-note5]: In the context of [iostreams](https://en.wikipedia.org/wiki/Iostream), writers often will refer to `<<` and `>>` as the “put-to” or “stream insertion” and “get-from” or “stream extraction” operators, respectively.
[^Cpprefr-note6]: According to the C99 standard, the right shift of a negative number is implementation defined. Most implementations, e.g., the GCC,[^Cpprefr1] use an [arithmetic shift](https://en.wikipedia.org/wiki/Arithmetic_shift) (i.e., sign extension), but a [logical shift](https://en.wikipedia.org/wiki/Logical_shift) is possible.
[^Cpprefr-note7]: The return type of `operator->()` must be a type for which the `->` operation can be applied, such as a pointer type. If `x` is of type `C` where `C` overloads `operator->()`, `x->y` gets expanded to `x.operator->()->y`.
[^Cpprefr-note8]: About [C++11 User-defined literals](http://en.cppreference.com/w/cpp/language/user_literal)
[^Cpprefr-note9]: The parentheses are not necessary when taking the size of a value, only when taking the size of a type. However, they are usually used regardless.
[^Cpprefr-note10]: C++ defines `alignof` operator, whereas C defines `_Alignof`. Both operators have the same semantics.
[^Cpprefr-note11]: For prototype examples, behaves like `const_cast/static_cast/reinterpret_cast`[^Cpprefr2]
[^Cpprefr-note12]: For prototype examples, for user-defined conversions, the return type implicitly and necessarily matches the operator name.
