
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
standard and scale it when necessary up to user defined maximum as this can be continued infinitely. Or just store it as 
struct \_future_type\_ {byte integerPart[], fractionPart[];} and implement basic operations via algorithms as the ALU does with the 
traditional types
Check fixed point arithmetic, extended precision, arbitrary-precision arithmetic

Add all arithmetic operations: +, -, *, /, //, %, \[any\]/integerPart, {any}/fractionPart

Add all logical operations: >>, <<, &, |, ~

Add all comparing operations: <(=), >(=), ==

Add binary manipulation functions: 0/1bitsCount, etc

Support direct bit manipulation via intrinsic functions: setZero/OneAt, etc

Support singed/unsigned

Support NaN (0/0), +-Infinity (\_anyNonZero\_/0)

Write in C11 and add language C++ wrappers and other languages bindings

Add math functions: round, floor, ceil, pow (power, ^, includes roots), abs (module), (arc/a)sin, (arc)cos, (arc)tg/tan, (arc)ctg/ctan, 
logE/ln, log10/lg, logAnyBiggerThenZeroAndNonOne, exp/e^any, expAnyBiggerThanZeroAndNonOne(any)/...^any, (arc/a)sh/sinh (hyperbolic sine), 
(arc)csh/cosh, (arc)th/tanh, (arc)cth/ctanh // Either with scaled versions of default algorithms used in C's standard math library or using 
approximations (Taylor/Maclaurin series)

Define constants including the transcendental ones (PI, E), as they are infinitely long they would need some precision setting

Add output and conversion functions: toString, to(U)Byte/Short/Int/Long (to use when the bits count are equal or when the arbitrary 
long number's type has insignificantly more bits than the traditional maximum sizeof(long))

Add (de)encoding functions: to(from)Hex, to(from)Base64(32)

PRECISION!!! (solve or at least mitigate that pesky 0.1 + 0.2 = 0.30000000000000004 and not exactly 0.3 problem caused by floating 
point binary representation and dec2bin/bin2dec conversions), roundoff, overflow errors

assembly specific optimizations, avx*/simd (avx2's 256 bit register, sounds interesting)

// optionally, what's the point of these numbers if they cannot be used anywhere else? - implement the applications!

Support for complex numbers (those which have real and imaginary parts and are the result of (-anyPositive)^(1/(2n)) 
(n is any integer 1,2,3...) and their algebra

Numeric methods: numeric differentiation/integration, etc

Matrices and vectors and their algebraic operations support

Algebraic expressions evaluator/processor aka calculator (the one that uses the inverse polish notation), 
like: \_future_type\_ result = eval("a + b + c^(lnb - {sin(shd))}", a, b, c, d);

fraction calculations processing, like 1/2 + 2/3 = 7/6

gpu/parallel computing: openCl, openMp, cuda, sycl, sdl3/opengl/vulkan with compute shaders

cryptography
steganography
deniable encryption/plausible deniability - sounds interesting
honey encryption (produces valid-looking but incorrect plaintexts when decrypted with the wrong key) - definitely worth playing with
multi-decryptable encryption / multi-key ciphers - I'm certainly diving into cryptography, just a few months later

### `Sounds more like a library for scientific computations`
