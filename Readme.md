
# Gleana

A low-level library for arbitrary long numeric data types (both integer and fractional) with support for arithmetic and 
standard math functions for them and maybe even with an extension to the complex field and with support for numeric methods/
approximate calculations/computation math [planned, concept, no development yet]

// There will be a lot of math involved here...

## This project is currently just an idea, there won't be anything here for several months

/*
Gotta refresh my higher math (calculus/math analysis, linear algebra, computational math), discrete math (math logic, 
algorithm theory), mathematical foundations of computers (aka informatics/computer science), information theory and 
computer architecture/science knowledge before I take on this - remembering all that foundational stuff from the university 
in short, this is gonna be long...
*/

### Planned license

Apache 2.0 or LGPL 2.0 or Mit, will decide later but it will definitely be permissive (fair restrictions so it can be used with 
other proprietary projects)

### Notes/Todos/What the finished result should implement

Represent all numbers as fractions and since the space isn't limited use fixed-point format. Maybe just take the `IEEE 754-2008` 
standard and scale it when necessary up to user defined maximum as this can be continued til the infinity. Or just sore it as 
struct \_type\_ {byte integerPart[], fractionPart[];} and implement basic operations via algorithms as the ALU does with the 
traditional types

Add all arithmetic operations: +, -, *, /, //, %, \[any\]/integerPart, {any}/fractionPart

Add all logical operations: >>, <<, &, |, ~

Add all comparing operations: <(=), >(=), ==

Add binary manipulation functions: 0/1bitsCount, etc

Support direct bit manipulation via intrinsic functions: setZero/OneAt, etc

Support singed/unsigned

Support NaN (0/0), +-Infinity (\_anyNonZero\_/0)

Write in C11 and add language C++ wrappers and other languages bindings

Add math functions: round, floor, bottom, pow (power, ^, includes roots), abs, (arc)sin, (arc)cos, (arc)tg/tan, (arc)ctg/ctan, 
logE/ln, log10/lg, logAnyBiggerThenZeroAndNotOne, exp/e^any, sh/sinh, csh/cosh, th/tanh, cth/ctanh // Either with scaled versions 
of default algorithms used in C's standard math library or using approximations (Taylor/Maclaurin series)

Define constants including the transcendental ones (PI, E), as they are infinitely long they would need some precision setting

Add output and conversion functions: toString, to(U)Byte/Short/Int/Long (to use when the bits count are equal or when the arbitrary 
long number's type has insignificantly more bits than the traditional maximum sizeof(long))

Add (de)encoding functions: to(from)Hex, to(from)Base64(32)

// optionally, what's the point of these numbers if they cannot be used anywhere else? - implement the applications!

Numeric methods: numeric differentiation/integration, etc

Matrices and vectors and their algebra operations support

Algebraic expressions evaluator/processor aka calculator (the one that uses the inverse polish notation), 
like: \_future_type\_ result = eval("a + b + c^(lnb - {sin(shd))}", a, b, c, d);
