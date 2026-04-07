# COMPLETE INTEGRALS CHEAT CODE ONE VARIABLE CALCULUS
### Focus: Indefinite integrals, definite integrals, substitution, integration by parts, trig integrals, inverse trig forms, logarithmic forms, and common exam patterns

> This note is the companion to the derivatives sheet.
> It keeps the same style and includes the most useful formulas, examples, and compact memory blocks.

---

# 1) WHAT AN INTEGRAL MEANS

## Indefinite integral

$$
\int f(x)\\,dx = F(x)+C
$$

This means:

$$
F'(x)=f(x)
$$

So integration is the reverse of differentiation.

### Example

$$
\int 3x^2\,dx = x^3 + C
$$

because

$$
\frac{d}{dx}(x^3)=3x^2
$$

## Constant of integration

When you integrate, always add:

$$
+C
$$

because many different antiderivatives differ by a constant.

### Example

$$
\frac{d}{dx}(x^2+5)=2x
$$

and also

$$
\frac{d}{dx}(x^2-9)=2x
$$

So

$$
\int 2x\\,dx = x^2 + C
$$

---

# 2) BASIC INTEGRAL RULES

## Constant rule

$$
\int c\\,dx = cx + C
$$

### Example

$$
\int 7\\,dx = 7x + C
$$

## Constant multiple rule

$$
\int c\,f(x)\\,dx = c\int f(x)\\,dx
$$

### Example

$$
\int 5x^2\\,dx = 5\int x^2\\,dx = 5\cdot \frac{x^3}{3}+C
$$

$$
= \frac{5x^3}{3}+C
$$

## Sum rule

$$
\int [f(x)+g(x)]\\,dx = \int f(x)\\,dx + \int g(x)\\,dx
$$

### Example

$$
\int (x^2+\sin x)\\,dx = \int x^2\\,dx + \int \sin x\\,dx
$$

$$
= \frac{x^3}{3} - \cos x + C
$$

## Difference rule

$$
\int [f(x)-g(x)]\\,dx = \int f(x)\\,dx - \int g(x)\\,dx
$$

### Example

$$
\int (e^x-\frac1x)\\,dx = e^x - \ln|x| + C
$$

---

# 3) POWER RULE FOR INTEGRATION

## Main power rule

$$
\int x^n\\,dx = \frac{x^{n+1}}{n+1}+C,\quad n\neq -1
$$

### Examples

$$
\int x^5\\,dx = \frac{x^6}{6}+C
$$

$$
\int x^{-2}\\,dx = \frac{x^{-1}}{-1}+C = -\frac1x + C
$$

$$
\int \sqrt{x}\\,dx = \int x^{1/2}\\,dx = \frac{x^{3/2}}{3/2}+C
$$

$$
= \frac23 x^{3/2}+C
$$

## The exceptional case

If \(n=-1\), then the power rule does **not** work.

Instead:

$$
\int \frac1x\\,dx = \ln|x|+C
$$

### Example

$$
\int \frac{1}{x}\\,dx = \ln|x|+C
$$

---

# 4) COMMON INDEFINITE INTEGRALS

## A) Algebraic forms

$$
\int x^n\\,dx = \frac{x^{n+1}}{n+1}+C,\quad n\neq -1
$$

$$
\int \frac1x\\,dx = \ln|x|+C
$$

$$
\int \frac{1}{ax+b}\\,dx = \frac1a\ln|ax+b|+C,\quad a\neq0
$$

### Examples

$$
\int \frac{1}{3x+2}\\,dx = \frac13 \ln|3x+2|+C
$$

$$
\int (2x+1)^5\\,dx = \frac{(2x+1)^6}{12}+C
$$

because substitution is hidden there.

## B) Exponential functions

$$
\int e^x\\,dx = e^x + C
$$

$$
\int e^{f(x)}f'(x)\\,dx = e^{f(x)}+C
$$

### Example

$$
\int 2x e^{x^2}\\,dx = e^{x^2}+C
$$

### General exponential \(a^x\)

$$
\int a^x\\,dx = \frac{a^x}{\ln a}+C,\quad a>0,\ a\neq1
$$

### Example

$$
\int 2^x\\,dx = \frac{2^x}{\ln 2}+C
$$

### General exponential with inner function

$$
\int a^{f(x)}f'(x)\\,dx = \frac{a^{f(x)}}{\ln a}+C
$$

### Example

$$
\int 2x\cdot 5^{x^2}\\,dx = \frac{5^{x^2}}{\ln 5}+C
$$

## C) Logarithmic functions

$$
\int \frac{1}{x}\\,dx=\ln|x|+C
$$

$$
\int \frac{f'(x)}{f(x)}\\,dx=\ln|f(x)|+C
$$

### Example

$$
\int \frac{2x}{x^2+1}\\,dx = \ln(x^2+1)+C
$$

### Important special formula

$$
\int \ln x\\,dx = x\ln x - x + C,\quad x>0
$$

### Example

$$
\int \ln x\\,dx = x\ln x - x + C
$$

## D) Trigonometric functions

$$
\int \sin x\\,dx = -\cos x + C
$$

$$
\int \cos x\\,dx = \sin x + C
$$

$$
\int \sec^2 x\\,dx = \tan x + C
$$

$$
\int \csc^2 x\\,dx = -\cot x + C
$$

$$
\int \sec x\tan x\\,dx = \sec x + C
$$

$$
\int \csc x\cot x\\,dx = -\csc x + C
$$

$$
\int \tan x\\,dx = -\ln|\cos x| + C
$$

Equivalent form:

$$
\int \tan x\\,dx = \ln|\sec x| + C
$$

$$
\int \cot x\\,dx = \ln|\sin x| + C
$$

$$
\int \sec x\\,dx = \ln|\sec x+\tan x| + C
$$

$$
\int \csc x\\,dx = \ln|\csc x-\cot x| + C
$$

### Examples

$$
\int \sin x\\,dx = -\cos x + C
$$

$$
\int \sec^2 x\\,dx = \tan x + C
$$

$$
\int \tan x\\,dx = -\ln|\cos x|+C
$$

## E) Trig of a function: chain-rule reversal

$$
\int \cos(f(x))f'(x)\\,dx = \sin(f(x))+C
$$

### Example

$$
\int 2x\cos(x^2)\\,dx = \sin(x^2)+C
$$

$$
\int \sin(f(x))f'(x)\\,dx = -\cos(f(x))+C
$$

### Example

$$
\int 3x^2\sin(x^3)\\,dx = -\cos(x^3)+C
$$

$$
\int \sec^2(f(x))f'(x)\\,dx = \tan(f(x))+C
$$

### Example

$$
\int 5\sec^2(5x)\\,dx = \tan(5x)+C
$$

$$
\int \frac{f'(x)}{1+(f(x))^2}\\,dx = \arctan(f(x))+C
$$

### Example

$$
\int \frac{6x}{1+9x^4}\\,dx = \arctan(3x^2)+C
$$

$$
\int \frac{f'(x)}{\sqrt{1-(f(x))^2}}\\,dx = \arcsin(f(x))+C
$$

### Example

$$
\int \frac{2}{\sqrt{1-4x^2}}\\,dx = \arcsin(2x)+C
$$

## F) Inverse trig forms

$$
\int \frac{1}{1+x^2}\\,dx = \arctan x + C
$$

$$
\int \frac{1}{\sqrt{1-x^2}}\\,dx = \arcsin x + C
$$

### Scaled versions

$$
\int \frac{1}{a^2+x^2}\\,dx = \frac1a \arctan\left(\frac{x}{a}\right)+C,\quad a>0
$$

$$
\int \frac{1}{\sqrt{a^2-x^2}}\\,dx = \arcsin\left(\frac{x}{a}\right)+C,\quad a>0
$$

### Examples

$$
\int \frac{1}{4+x^2}\\,dx = \frac12 \arctan\left(\frac{x}{2}\right)+C
$$

$$
\int \frac{1}{\sqrt{9-x^2}}\\,dx = \arcsin\left(\frac{x}{3}\right)+C
$$

---

# 5) SUBSTITUTION

## Main idea

If you see:

$$
\int f(g(x))g'(x)\\,dx
$$

set

$$
u=g(x)
$$

then

$$
du=g'(x)\\,dx
$$

and the integral becomes:

$$
\int f(u)\,du
$$

## Formula

$$
\int f(g(x))g'(x)\\,dx = \int f(u)\,du
$$

### Example 1

$$
\int 2x\cos(x^2)\\,dx
$$

Let

$$
u=x^2,\quad du=2x\\,dx
$$

Then

$$
\int 2x\cos(x^2)\\,dx = \int \cos u\,du = \sin u + C
$$

$$
= \sin(x^2)+C
$$

### Example 2

$$
\int \frac{3x^2}{x^3+1}\\,dx
$$

Let

$$
u=x^3+1,\quad du=3x^2\\,dx
$$

Then

$$
\int \frac{3x^2}{x^3+1}\\,dx = \int \frac1u\,du = \ln|u|+C
$$

$$
= \ln|x^3+1|+C
$$

### Example 3

$$
\int (5x-1)^7\\,dx
$$

Let

$$
u=5x-1,\quad du=5\\,dx,\quad\,dx=\frac{du}{5}
$$

Then

$$
\int (5x-1)^7\\,dx = \frac15\int u^7\,du
$$

$$
= \frac15\cdot \frac{u^8}{8}+C
$$

$$
= \frac{(5x-1)^8}{40}+C
$$

---

# 6) INTEGRATION BY PARTS

## Formula

$$
\int u\,dv = uv - \int v\,du
$$

This is useful when the integrand is a product and substitution is not enough.

## Good cases

- polynomial \(\times\) exponential
- polynomial \(\times\) trig
- polynomial \(\times\) logarithm
- \(\ln x\)
- inverse trig functions

## LIATE hint

A common rule for choosing \(u\):

- Logarithmic
- Inverse trig
- Algebraic
- Trig
- Exponential

Choose earlier types as \(u\), later types as \(dv\).

### Example 1

$$
\int x e^x\\,dx
$$

Let

$$
u=x,\quad dv=e^x\\,dx
$$

Then

$$
du=dx,\quad v=e^x
$$

So

$$
\int xe^x\\,dx = xe^x - \int e^x\\,dx
$$

$$
= xe^x - e^x + C
$$

$$
= e^x(x-1)+C
$$

### Example 2

$$
\int x\cos x\\,dx
$$

Let

$$
u=x,\quad dv=\cos x\\,dx
$$

Then

$$
du=dx,\quad v=\sin x
$$

So

$$
\int x\cos x\\,dx = x\sin x - \int \sin x\\,dx
$$

$$
= x\sin x + \cos x + C
$$

### Example 3

$$
\int \ln x\\,dx
$$

Write it as:

$$
\int \ln x\cdot 1\\,dx
$$

Let

$$
u=\ln x,\quad dv=dx
$$

Then

$$
du=\frac1x\\,dx,\quad v=x
$$

So

$$
\int \ln x\\,dx = x\ln x - \int x\cdot \frac1x\\,dx
$$

$$
= x\ln x - \int 1\\,dx
$$

$$
= x\ln x - x + C
$$

---

# 7) DEFINITE INTEGRALS

## Definition idea

$$
\int_a^b f(x)\\,dx
$$

gives signed area from \(x=a\) to \(x=b\).

## Fundamental Theorem of Calculus

If \(F'(x)=f(x)\), then

$$
\int_a^b f(x)\\,dx = F(b)-F(a)
$$

### Example

$$
\int_0^2 3x^2\\,dx
$$

Antiderivative:

$$
F(x)=x^3
$$

Then

$$
\int_0^2 3x^2\\,dx = x^3\Big|_0^2 = 2^3-0^3 = 8
$$

### Example 2

$$
\int_0^\pi \sin x\\,dx
$$

Antiderivative:

$$
-\cos x
$$

Then

$$
\int_0^\pi \sin x\\,dx = -\cos x\Big|_0^\pi
$$

$$
= -\cos\pi - (-\cos0)= -(-1)-(-1)=2
$$

## Properties

### Reverse limits

$$
\int_a^b f(x)\\,dx = -\int_b^a f(x)\\,dx
$$

### Same limits

$$
\int_a^a f(x)\\,dx = 0
$$

### Add intervals

$$
\int_a^b f(x)\\,dx + \int_b^c f(x)\\,dx = \int_a^c f(x)\\,dx
$$

### Constant multiple

$$
\int_a^b c f(x)\\,dx = c\int_a^b f(x)\\,dx
$$

### Sum

$$
\int_a^b [f(x)+g(x)]\\,dx = \int_a^b f(x)\\,dx + \int_a^b g(x)\\,dx
$$

---

# 8) u-SUBSTITUTION IN DEFINITE INTEGRALS

If

$$
u=g(x)
$$

then you can change bounds too.

## Formula

$$
\int_a^b f(g(x))g'(x)\\,dx = \int_{u(a)}^{u(b)} f(u)\,du
$$

### Example

$$
\int_0^1 2x\cos(x^2)\\,dx
$$

Let

$$
u=x^2,\quad du=2x\\,dx
$$

Change bounds:

- when \(x=0\), \(u=0\)
- when \(x=1\), \(u=1\)

So

$$
\int_0^1 2x\cos(x^2)\\,dx = \int_0^1 \cos u\,du
$$

$$
= \sin u\Big|_0^1 = \sin 1
$$

---

# 9) AREA AND SIGN

If \(f(x)\ge 0\) on \([a,b]\), then

$$
\int_a^b f(x)\\,dx
$$

is the usual area.

If \(f(x)<0\) somewhere, the definite integral gives **signed area**.

## Example

$$
\int_{-1}^1 x\\,dx = 0
$$

because the negative and positive parts cancel.

But the geometric area is not zero.

For total geometric area, use:

$$
\int_a^b |f(x)|\\,dx
$$

---

# 10) IMPROPER INTEGRALS

These happen when:

- interval is infinite
- function blows up inside the interval

## Infinite interval

$$
\int_a^\infty f(x)\\,dx = \lim_{b\to\infty}\int_a^b f(x)\\,dx
$$

### Example

$$
\int_1^\infty \frac1{x^2}\\,dx
$$

$$
= \lim_{b\to\infty}\int_1^b x^{-2}\\,dx
$$

$$
= \lim_{b\to\infty}\left[-\frac1x\right]_1^b
$$

$$
= \lim_{b\to\infty}\left(-\frac1b+1\right)=1
$$

So it converges.

## Vertical asymptote in interval

$$
\int_a^b f(x)\\,dx
$$

with blow-up at \(c\in[a,b]\) becomes limits.

### Example

$$
\int_0^1 \frac1{\sqrt{x}}\\,dx
$$

$$
= \lim_{t\to0^+}\int_t^1 x^{-1/2}\\,dx
$$

$$
= \lim_{t\to0^+}\left[2\sqrt{x}\right]_t^1
= \lim_{t\to0^+}(2-2\sqrt{t})=2
$$

---

# 11) COMMON PATTERNS TO RECOGNIZE FAST

## Pattern 1: derivative over function

$$
\int \frac{f'(x)}{f(x)}\\,dx = \ln|f(x)|+C
$$

### Example

$$
\int \frac{4x^3}{x^4+7}\\,dx = \ln(x^4+7)+C
$$

## Pattern 2: inside function and its derivative

$$
\int f(g(x))g'(x)\\,dx
$$

Use substitution.

### Example

$$
\int \cos(5x)\\,dx = \frac15\sin(5x)+C
$$

## Pattern 3: \(1+u^2\)

$$
\int \frac{u'}{1+u^2}\\,dx = \arctan(u)+C
$$

### Example

$$
\int \frac{2x}{1+x^4}\\,dx = \arctan(x^2)+C
$$

## Pattern 4: \(\sqrt{1-u^2}\)

$$
\int \frac{u'}{\sqrt{1-u^2}}\\,dx = \arcsin(u)+C
$$

### Example

$$
\int \frac{3}{\sqrt{1-9x^2}}\\,dx = \arcsin(3x)+C
$$

## Pattern 5: product that suggests parts

$$
\int x e^x\\,dx,\quad \int x\sin x\\,dx,\quad \int \ln x\\,dx
$$

Use integration by parts.

---

# 12) VERY COMMON INTEGRAL EXAMPLES

## Example 1

$$
\int (x^3+4x-7)\\,dx = \frac{x^4}{4}+2x^2-7x+C
$$

## Example 2

$$
\int x^2\cos x\\,dx
$$

This one needs integration by parts twice.

Result:

$$
x^2\sin x + 2x\cos x - 2\sin x + C
$$

## Example 3

$$
\int \frac{\ln x}{x}\\,dx
$$

Let

$$
u=\ln x,\quad du=\frac1x\\,dx
$$

Then

$$
\int \frac{\ln x}{x}\\,dx = \int u\,du = \frac{u^2}{2}+C
$$

$$
= \frac{(\ln x)^2}{2}+C
$$

## Example 4

$$
\int e^{x^2+1}2x\\,dx = e^{x^2+1}+C
$$

## Example 5

$$
\int \sin(3x^2)6x\\,dx = -\cos(3x^2)+C
$$

## Example 6

$$
\int \frac{2x}{(x^2+4)\ln 5}\\,dx = \log_5(x^2+4)+C
$$

because

$$
\frac{d}{dx}\log_5(x^2+4)=\frac{2x}{(x^2+4)\ln 5}
$$

## Example 7

$$
\int \frac{1}{4+x^2}\\,dx = \frac12\arctan\left(\frac{x}{2}\right)+C
$$

## Example 8

$$
\int |x|\\,dx
$$

This is piecewise:

$$
\int |x|\\,dx=
\begin{cases}
\frac{x^2}{2}+C, & x\ge0 \\
-\frac{x^2}{2}+C, & x<0
\end{cases}
$$

A compact form is:

$$
\int |x|\\,dx = \frac{x|x|}{2}+C
$$

---

# 13) ULTRA-COMPACT MEMORY SHEET

## Indefinite integrals

$$
\int c\\,dx = cx+C
$$

$$
\int x^n\\,dx = \frac{x^{n+1}}{n+1}+C,\quad n\neq -1
$$

$$
\int \frac1x\\,dx = \ln|x|+C
$$

$$
\int e^x\\,dx = e^x+C
$$

$$
\int a^x\\,dx = \frac{a^x}{\ln a}+C
$$

$$
\int \sin x\\,dx = -\cos x+C
$$

$$
\int \cos x\\,dx = \sin x+C
$$

$$
\int \sec^2 x\\,dx = \tan x+C
$$

$$
\int \csc^2 x\\,dx = -\cot x+C
$$

$$
\int \sec x\tan x\\,dx = \sec x+C
$$

$$
\int \csc x\cot x\\,dx = -\csc x+C
$$

$$
\int \tan x\\,dx = -\ln|\cos x|+C
$$

$$
\int \cot x\\,dx = \ln|\sin x|+C
$$

$$
\int \sec x\\,dx = \ln|\sec x+\tan x|+C
$$

$$
\int \csc x\\,dx = \ln|\csc x-\cot x|+C
$$

$$
\int \frac{1}{1+x^2}\\,dx = \arctan x+C
$$

$$
\int \frac{1}{\sqrt{1-x^2}}\\,dx = \arcsin x+C
$$

$$
\int \frac{f'(x)}{f(x)}\\,dx = \ln|f(x)|+C
$$

$$
\int \cos(f(x))f'(x)\\,dx = \sin(f(x))+C
$$

$$
\int \sin(f(x))f'(x)\\,dx = -\cos(f(x))+C
$$

$$
\int a^{f(x)}f'(x)\\,dx = \frac{a^{f(x)}}{\ln a}+C
$$

$$
\int \frac{f'(x)}{1+(f(x))^2}\\,dx = \arctan(f(x))+C
$$

$$
\int \frac{f'(x)}{\sqrt{1-(f(x))^2}}\\,dx = \arcsin(f(x))+C
$$

## Methods

$$
u=g(x),\quad du=g'(x)\\,dx
$$

$$
\int u\,dv = uv-\int v\,du
$$

## Definite integrals

$$
\int_a^b f(x)\\,dx = F(b)-F(a)
$$

$$
\int_a^b f(x)\\,dx = -\int_b^a f(x)\\,dx
$$

$$
\int_a^a f(x)\\,dx = 0
$$

$$
\int_a^b f(x)\\,dx+\int_b^c f(x)\\,dx=\int_a^c f(x)\\,dx
$$

---

# 14) FINAL IMPORTANT IDENTITY BOX

These are the ones students forget most often:

$$
\int \frac1x\\,dx = \ln|x|+C
$$

$$
\int \frac{1}{ax+b}\\,dx = \frac1a\ln|ax+b|+C
$$

$$
\int a^x\\,dx = \frac{a^x}{\ln a}+C
$$

$$
\int \ln x\\,dx = x\ln x-x+C
$$

$$
\int \tan x\\,dx = -\ln|\cos x|+C = \ln|\sec x|+C
$$

$$
\int \frac{1}{a^2+x^2}\\,dx = \frac1a\arctan\left(\frac{x}{a}\right)+C
$$

$$
\int \frac{1}{\sqrt{a^2-x^2}}\\,dx = \arcsin\left(\frac{x}{a}\right)+C
$$

$$
\int |x|\\,dx = \frac{x|x|}{2}+C
$$

---

# 15) MINI EXAM VERSION

## If you only want the shortest survival sheet

$$
\int x^n\\,dx = \frac{x^{n+1}}{n+1}+C,\quad n\neq-1
$$

$$
\int \frac1x\\,dx = \ln|x|+C
$$

$$
\int e^x\\,dx = e^x+C,\quad
\int a^x\\,dx = \frac{a^x}{\ln a}+C
$$

$$
\int \sin x\\,dx = -\cos x+C,\quad
\int \cos x\\,dx = \sin x+C
$$

$$
\int \sec^2 x\\,dx = \tan x+C,\quad
\int \frac{1}{1+x^2}\\,dx = \arctan x+C
$$

$$
\int \frac{1}{\sqrt{1-x^2}}\\,dx = \arcsin x+C
$$

$$
\int \frac{f'(x)}{f(x)}\\,dx = \ln|f(x)|+C
$$

$$
u=g(x),\ du=g'(x)\\,dx
$$

$$
\int u\,dv = uv-\int v\,du
$$

$$
\int_a^b f(x)\\,dx = F(b)-F(a)
$$

