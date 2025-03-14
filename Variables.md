Variables are portion of a computer's memory set aside to store a value. It requires an **identifier** and a **datatype** to create a unique variable.

The identifier of a variable has a few rules:
- It can't start with a number or a symbol except underline(\_)
- it can't use spaces, punctuation marks or symbols except underscore(\_)  as identifiers on its own or within other identifiers
- it can't be the following since they are C++ keywords:
```
 alignas, alignof, and, and_eq, asm, auto, bitand, bitor, bool, break, case, catch, char, char16_t, char32_t, class, compl, const, constexpr, const_cast, continue, decltype, default, delete, do, double, dynamic_cast, else, enum, explicit, export, extern, false, float, for, friend, goto, if, inline, int, long, mutable, namespace, new, noexcept, not, not_eq, nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, return, short, signed, sizeof, static, static_assert, static_cast, struct, switch, template, this, thread_local, throw, true, try, typedef, typeid, typename, union, unsigned, using, virtual, void, volatile, wchar_t, while, xor, xor_eq 
 ```
 C++ variables are **case sensitive**, that means identifiers written in capital letters is not the same as written in small letters.

The size of the portion of memory set aside for the variable depends on the datatype of the variable.