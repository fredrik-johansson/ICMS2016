#  ICMS 2016 Session: High-precision arithmetic, effective analysis and special functions

ICMS 2016: [Home](http://icms2016.zib.de/), [Sessions](http://icms2016.zib.de/sessions.html)

## Organizers

* Fredrik Johansson (INRIA Bordeaux) <fredrik.johansson@gmail.com>

## Aim and Scope

High-precision methods have become an important tool to get reliable results when solving numerical problems of increased size and complexity. The goal of this session is to present advances in software for high-precision or certified numerical methods, particularly in the context of effective complex analysis and computation of transcendental functions. Possible subjects include but are not limited to:

* Arbitrary-precision and mixed-precision arithmetic
* Interval arithmetic and Taylor methods
* High-precision or rigorous computation of D-finite functions, L-functions and modular forms
* Certified numerical integration and solution of ODEs
* Applications, for instance in number theory, combinatorics, and mathematical physics 

Work in these areas combining numerical methods with computer algebra is particularly welcome.

## Publications

A *short abstract* will appear on the permanent conference web page (see below) as soon as accepted.

An *extended abstract* will appear on the permanent conference web page (see below) as soon as accepted.
It will also appear on the proceedings that will be distributed during the meeting.

## Submission Guidelines

If you would like to give a talk at ICMS, you need to submit first a short abstract and then later an extended abstract. See the guideline for the details.

After the meeting, the submission guideline for a journal special issue will be communicated to you by the session organizers. 

## Talks/Abstracts

### On the computation of confluent hypergeometric functions for large imaginary part of b and z

Authors:
* Guillermo Navas-Palencia (Dept. Computer Science, Universitat Politècnica de Catalunya and Numerical Algorithms Group, Oxford)
* Argimiro Arratia (Dept. Computer Science/BGSMath, Universitat Politècnica de Catalunya)

We present an efficient algorithm for the confluent hypergeometric functions when the imaginary part of b and z is large. The algorithm is based on the steepest descent method, applied to a suitable representation of the confluent hypergeometric function as a highly oscillatory integral, which is then integrated by using various quadrature methods.

The performance of the algorithm is compared with open-source and commercial software solutions with arbitrary precision, and for many cases the algorithm achieves high accuracy in both the real and imaginary part. Our motivation comes from the need for accurate computation of the characteristic function of the Arcsine distribution and the Beta distribution; the latter being required in several financial applications, for example, modeling the loss given default in the context of portfolio credit risk.

### Rigorous Multiple-Precision Evaluation of D-Finite Functions in Sage

Author: Marc Mezzarobba (LIP6, Université Pierre et Marie Curie)

We present an implementation, on top of the SageMath computer algebra
system, of various algorithms for the numerical evaluation of
so-called D-finite functions. A complex analytic function is D-finite
when it satisfies an ordinary differential equation whose coefficients
are polynomial in the independent variable. D-finite functions can be
viewed as a class of special functions analogous to those of algebraic
or hypergeometric functions (but more general). They come up in areas
such as analytic combinatorics and mathematical physics, and lend
themselves well to symbolic manipulation by computer algebra systems.

The main task our package performs is the “numerical analytic
continuation” of D-finite functions. This process results in a
numerical approximation of the transition matrix that maps “initial
values” of an ODE somewhere on the complex plane to “initial values”
elsewhere that define the same solution. Numerical analytic
continuation then serves to compute things like values or polynomial
approximations of D-finite functions anywhere on their Riemann
surfaces, and monodromy matrices of differential operators. The code
supports the important limit case where the (generalized) initial
values are provided at regular singular points of the ODE, making it
possible in particular to compute connection constants between regular
singularities. It is rigorous in the sense that it returns interval
results that are guaranteed to enclose the exact mathematical result.

The new package can be considered a successor of NumGfun, a Maple
package by the same author with similar features.

### Title TBA

Author: Pascal Molin

### Title TBA

Author: Elias Tsigaridas

### Recursive double-size fixed precision arithmetic

Authors: Alexis Breust, Christophe Chabot, Jean-Guillaume Dumas, Laurent Fousse, Pascal Giorgi

We propose a new fixed precision arithmetic package called RecInt.
It uses a recursive double-size data-structure.
Contrary to arbitrary precision packages like GMP, 
that create vectors of words on the heap, RecInt large integers are
created on the stack. 
The space allocated for these integers is a power of two and
arithmetic is performed modulo that power. 
Arithmetic operations are thus easily implemented recursively by a divide and
conquer strategy. 
Among those, we show that this packages is particularly well adapted to
Newton-Raphson like iterations or Montgomery reduction.
Recursivity is implemented via doubling algorithms on templated data-types.
The idea is to extend machine word functionality to any power of two
and to use template partial specialization to adapt the
implemented routines to some specific sizes and thresholds.
The main target precision is for cryptographic sizes, that is up to
several tens of machine words. 
Preliminary experiments show that good performance can be attained when
comparing to the state of art GMP library: it can be several order of magnitude
faster when used with very few machine words.
This package is now integrated within the Givaro C++ library and has
been used for efficient exact linear algebra computations.
