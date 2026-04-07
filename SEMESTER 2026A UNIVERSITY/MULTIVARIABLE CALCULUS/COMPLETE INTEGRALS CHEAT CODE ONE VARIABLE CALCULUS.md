# COMPLETE CALCULUS CHEAT SHEET
## Derivatives + Limits + Main Forms

> This note matches the syntax style that works in your Obsidian setup.
> It keeps the same style as the integrals sheet, but focused on derivatives, limits, logarithms, trig, inverse trig, chain rule, and the hardest forms.
> Main additions: `a^x`, `a^{f(x)}`, `log_a x`, `log_a(f(x))`, `\ln|x|`, `\ln|f(x)|`, `x^x`, `|x|`, one-sided limits, continuity, and a compact exam section.

---

# 1) DERIVATIVE DEFINITION

## Basic definition

$$
f'(x)=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}
$$

Equivalent notation:

$$
\frac{d}{dx}f(x)=f'(x)
$$

### Example

If

$$
f(x)=x^2
$$

then

$$
f'(x)=\lim_{h\to0}\frac{(x+h)^2-x^2}{h}
$$

$$
=\lim_{h\to0}\frac{x^2+2xh+h^2-x^2}{h}
=\lim_{h\to0}\frac{2xh+h^2}{h}
=\lim_{h\to0}(2x+h)=2x
$$

---

# 2) BASIC DERIVATIVE RULES
## Constant rule

$$
\frac{d}{dx}(c)=0
$$

### Example

$$
\frac{d}{dx}(7)=0
$$

## Identity rule

$$
\frac{d}{dx}(x)=1
$$

### Example

$$
\frac{d}{dx}(x)=1
$$

## Constant multiple rule

$$
\frac{d}{dx}[c\,f(x)]=c\,f'(x)
$$

### Example

$$
\frac{d}{dx}(5x^3)=5\cdot 3x^2=15x^2
$$

## Sum rule

$$
\frac{d}{dx}[f(x)+g(x)]=f'(x)+g'(x)
$$

### Example

$$
\frac{d}{dx}(x^2+\sin x)=2x+\cos x
$$

## Difference rule

$$
\frac{d}{dx}[f(x)-g(x)]=f'(x)-g'(x)
$$

### Example

$$
\frac{d}{dx}(e^x-\ln x)=e^x-\frac1x
$$

---

# 3) POWER RULE

## Main power rule

$$
\frac{d}{dx}(x^n)=n x^{n-1}
$$

This works for real \(n\) whenever the expression is defined.

### Examples

$$
\frac{d}{dx}(x^5)=5x^4
$$

$$
\frac{d}{dx}(x^{-2})=-2x^{-3}=-\frac{2}{x^3}
$$

$$
\frac{d}{dx}(\sqrt{x})
=\frac{d}{dx}(x^{1/2})
=\frac12 x^{-1/2}
=\frac{1}{2\sqrt{x}}
$$

$$
\frac{d}{dx}\left(\frac1x\right)
=\frac{d}{dx}(x^{-1})
=-x^{-2}
=-\frac1{x^2}
$$

---

# 4) PRODUCT RULE

$$
\frac{d}{dx}[f(x)g(x)]=f'(x)g(x)+f(x)g'(x)
$$

### Example

$$
y=(x^2)(\sin x)
$$

Then

$$
y'=(2x)(\sin x)+(x^2)(\cos x)
$$

$$
y'=2x\sin x+x^2\cos x
$$

---

# 5) QUOTIENT RULE

$$
\frac{d}{dx}\left(\frac{f(x)}{g(x)}\right)
=
\frac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2}
$$

### Example

$$
y=\frac{x^2+1}{x-3}
$$

Then

$$
y'
=
\frac{(2x)(x-3)-(x^2+1)(1)}{(x-3)^2}
$$

$$
=
\frac{2x^2-6x-x^2-1}{(x-3)^2}
=
\frac{x^2-6x-1}{(x-3)^2}
$$

---

# 6) CHAIN RULE

## Main chain rule

$$
\frac{d}{dx}f(g(x))=f'(g(x))\,g'(x)
$$

### Example

$$
y=(3x^2+1)^4
$$

Outer function: \(u^4\)  
Inner function: \(u=3x^2+1\)

$$
y'=4(3x^2+1)^3\cdot 6x
$$

$$
y'=24x(3x^2+1)^3
$$

---

# 7) COMMON DERIVATIVES

## A) Polynomial and algebraic forms

$$
\frac{d}{dx}(x^n)=n x^{n-1}
$$

$$
\frac{d}{dx}\left(\frac1x\right)=-\frac1{x^2}
$$

$$
\frac{d}{dx}(\sqrt{x})=\frac{1}{2\sqrt{x}}
$$

$$
\frac{d}{dx}\left(\sqrt[n]{x}\right)=\frac{d}{dx}(x^{1/n})=\frac1n x^{1/n-1}
$$

### Examples

$$
\frac{d}{dx}(x^{3/2})=\frac32 x^{1/2}
$$

$$
\frac{d}{dx}(x^{-1/2})=-\frac12 x^{-3/2}
$$

## B) Exponential functions

### Natural exponential

$$
\frac{d}{dx}(e^x)=e^x
$$

### Example

$$
\frac{d}{dx}(e^x)=e^x
$$

### Exponential with inner function

$$
\frac{d}{dx}(e^{f(x)})=f'(x)e^{f(x)}
$$

### Example

$$
\frac{d}{dx}(e^{x^2})=2x\,e^{x^2}
$$

### General exponential \(a^x\)

$$
\frac{d}{dx}(a^x)=a^x\ln(a), \quad a>0,\ a\neq1
$$

### Example

$$
\frac{d}{dx}(2^x)=2^x\ln 2
$$

### General exponential with inner function

$$
\frac{d}{dx}(a^{f(x)})=a^{f(x)}\ln(a)\,f'(x)
$$

### Example

$$
\frac{d}{dx}(5^{x^2})=5^{x^2}\ln(5)\cdot 2x
$$

$$
=2x\,5^{x^2}\ln 5
$$

## C) Logarithmic functions

### Natural logarithm

$$
\frac{d}{dx}(\ln x)=\frac1x,\quad x>0
$$

### Example

$$
\frac{d}{dx}(\ln x)=\frac1x
$$

### Logarithm of absolute value

$$
\frac{d}{dx}(\ln|x|)=\frac1x,\quad x\neq0
$$

### Example

$$
\frac{d}{dx}(\ln|x-2|)=\frac{1}{x-2}
$$

### Natural logarithm of a function

$$
\frac{d}{dx}(\ln(f(x)))=\frac{f'(x)}{f(x)}
$$

### Example

$$
\frac{d}{dx}\ln(x^2+1)=\frac{2x}{x^2+1}
$$

### Logarithm of absolute value of a function

$$
\frac{d}{dx}(\ln|f(x)|)=\frac{f'(x)}{f(x)}
$$

### Example

$$
\frac{d}{dx}\ln|x^2-4|=\frac{2x}{x^2-4}
$$

## D) Logarithm base \(a\)

### Conversion formula

$$
\log_a x=\frac{\ln x}{\ln a}
$$

### Derivative

$$
\frac{d}{dx}(\log_a x)=\frac{1}{x\ln a},\quad a>0,\ a\neq1
$$

### Example

$$
\frac{d}{dx}(\log_2 x)=\frac{1}{x\ln 2}
$$

### Log base \(a\) of a function

$$
\frac{d}{dx}\bigl(\log_a(f(x))\bigr)=\frac{f'(x)}{f(x)\ln a}
$$

### Example

$$
\frac{d}{dx}\log_3(x^2+1)=\frac{2x}{(x^2+1)\ln 3}
$$

## E) Trigonometric functions

$$
\frac{d}{dx}(\sin x)=\cos x
$$

$$
\frac{d}{dx}(\cos x)=-\sin x
$$

$$
\frac{d}{dx}(\tan x)=\sec^2 x
$$

$$
\frac{d}{dx}(\cot x)=-\csc^2 x
$$

$$
\frac{d}{dx}(\sec x)=\sec x\tan x
$$

$$
\frac{d}{dx}(\csc x)=-\csc x\cot x
$$

### Examples

$$
\frac{d}{dx}(\sin x+\cos x)=\cos x-\sin x
$$

$$
\frac{d}{dx}(\tan x)=\sec^2 x
$$

$$
\frac{d}{dx}(\sec x)=\sec x\tan x
$$

## F) Trig of a function: chain rule forms

$$
\frac{d}{dx}(\sin(f(x)))=f'(x)\cos(f(x))
$$

### Example

$$
\frac{d}{dx}\sin(x^2)=2x\cos(x^2)
$$

$$
\frac{d}{dx}(\cos(f(x)))=-f'(x)\sin(f(x))
$$

### Example

$$
\frac{d}{dx}\cos(3x)= -3\sin(3x)
$$

$$
\frac{d}{dx}(\tan(f(x)))=f'(x)\sec^2(f(x))
$$

### Example

$$
\frac{d}{dx}\tan(x^3)=3x^2\sec^2(x^3)
$$

$$
\frac{d}{dx}(\sec(f(x)))=f'(x)\sec(f(x))\tan(f(x))
$$

### Example

$$
\frac{d}{dx}\sec(x^2)=2x\sec(x^2)\tan(x^2)
$$

$$
\frac{d}{dx}(\csc(f(x)))=-f'(x)\csc(f(x))\cot(f(x))
$$

### Example

$$
\frac{d}{dx}\csc(2x)=-2\csc(2x)\cot(2x)
$$

$$
\frac{d}{dx}(\cot(f(x)))=-f'(x)\csc^2(f(x))
$$

### Example

$$
\frac{d}{dx}\cot(5x)=-5\csc^2(5x)
$$

## G) Inverse trigonometric functions

$$
\frac{d}{dx}(\arcsin x)=\frac{1}{\sqrt{1-x^2}}
$$

$$
\frac{d}{dx}(\arccos x)=-\frac{1}{\sqrt{1-x^2}}
$$

$$
\frac{d}{dx}(\arctan x)=\frac{1}{1+x^2}
$$

$$
\frac{d}{dx}(\arccot x)=-\frac{1}{1+x^2}
$$

$$
\frac{d}{dx}(\arcsec x)=\frac{1}{|x|\sqrt{x^2-1}}
$$

$$
\frac{d}{dx}(\arccsc x)=-\frac{1}{|x|\sqrt{x^2-1}}
$$

### Examples

$$
\frac{d}{dx}(\arcsin x)=\frac{1}{\sqrt{1-x^2}}
$$

$$
\frac{d}{dx}(\arctan x)=\frac{1}{1+x^2}
$$

## H) Inverse trig with inner function

$$
\frac{d}{dx}(\arcsin(f(x)))=\frac{f'(x)}{\sqrt{1-(f(x))^2}}
$$

### Example

$$
\frac{d}{dx}\arcsin(2x)=\frac{2}{\sqrt{1-4x^2}}
$$

$$
\frac{d}{dx}(\arccos(f(x)))=-\frac{f'(x)}{\sqrt{1-(f(x))^2}}
$$

### Example

$$
\frac{d}{dx}\arccos(x^2)=-\frac{2x}{\sqrt{1-x^4}}
$$

$$
\frac{d}{dx}(\arctan(f(x)))=\frac{f'(x)}{1+(f(x))^2}
$$

### Example

$$
\frac{d}{dx}\arctan(3x^2)=\frac{6x}{1+9x^4}
$$

## I) Absolute value

For \(x\neq0\),

$$
\frac{d}{dx}|x|=\frac{x}{|x|}
$$

That means

$$
\frac{d}{dx}|x|=
\begin{cases}
1, & x>0 \\
-1, & x<0
\end{cases}
$$

It is **not differentiable** at \(x=0\).

### Example

$$
\frac{d}{dx}|x-3|=\frac{x-3}{|x-3|},\quad x\neq3
$$

---

# 8) IMPORTANT SPECIAL FORMS

## A) Power of a function

$$
\frac{d}{dx}([f(x)]^n)=n[f(x)]^{n-1}f'(x)
$$

### Example

$$
\frac{d}{dx}(x^2+1)^5=5(x^2+1)^4(2x)
$$

$$
=10x(x^2+1)^4
$$

## B) Function raised to a function

This is the hard one:

$$
y=f(x)^{g(x)}
$$

### Main formula

$$
\frac{d}{dx}(f(x)^{g(x)})
=
f(x)^{g(x)}
\left[
g'(x)\ln(f(x)) + g(x)\frac{f'(x)}{f(x)}
\right]
$$

Equivalent order:

$$
\frac{d}{dx}(f(x)^{g(x)})
=
f(x)^{g(x)}
\left[
\frac{g(x)f'(x)}{f(x)}+\ln(f(x))g'(x)
\right]
$$

### Why?

Because

$$
f(x)^{g(x)}=e^{g(x)\ln(f(x))}
$$

### Example

$$
y=(x^2+1)^x
$$

Then

$$
f(x)=x^2+1,\quad g(x)=x
$$

$$
f'(x)=2x,\quad g'(x)=1
$$

So

$$
y'=(x^2+1)^x\left[\ln(x^2+1)+x\cdot\frac{2x}{x^2+1}\right]
$$

$$
y'=(x^2+1)^x\left[\ln(x^2+1)+\frac{2x^2}{x^2+1}\right]
$$

## C) The special case \(x^x\)

$$
\frac{d}{dx}(x^x)=x^x(\ln x+1),\quad x>0
$$

### Why?

Treat it as \(f(x)^{g(x)}\) with both equal to \(x\).

### Example

$$
\frac{d}{dx}(x^x)=x^x\left(1\cdot\ln x+x\cdot\frac1x\right)=x^x(\ln x+1)
$$

## D) Logarithmic differentiation pattern

Useful when:

- powers are complicated
- many factors multiply
- variables appear in exponents

If

$$
y=\text{complicated expression}
$$

take \(\ln\) of both sides, simplify, differentiate.

### Example

$$
y=\frac{(x^2+1)^3\sqrt{x}}{(x-1)^4}
$$

Take log:

$$
\ln y=3\ln(x^2+1)+\frac12\ln x-4\ln(x-1)
$$

Differentiate:

$$
\frac{y'}{y}
=
3\frac{2x}{x^2+1}+\frac{1}{2x}-\frac{4}{x-1}
$$

So

$$
y'
=
y\left(
\frac{6x}{x^2+1}+\frac{1}{2x}-\frac{4}{x-1}
\right)
$$

Substitute back \(y\).

---

# 9) LIMITS

## A) Basic limit notation

$$
\lim_{x\to a}f(x)=L
$$

Meaning: as \(x\) gets close to \(a\), \(f(x)\) gets close to \(L\).

## B) One-sided limits

$$
\lim_{x\to a^-}f(x)
$$

means approaching \(a\) from the left.

$$
\lim_{x\to a^+}f(x)
$$

means approaching \(a\) from the right.

The two-sided limit exists only if both one-sided limits exist and are equal.

### Example

$$
f(x)=\frac{|x|}{x}
$$

Then

$$
\lim_{x\to0^-}\frac{|x|}{x}=-1
$$

$$
\lim_{x\to0^+}\frac{|x|}{x}=1
$$

So

$$
\lim_{x\to0}\frac{|x|}{x}
$$

does **not** exist.

## C) Direct substitution

If \(f\) is continuous at \(a\), then:

$$
\lim_{x\to a}f(x)=f(a)
$$

### Example

$$
\lim_{x\to2}(x^2+3x)=2^2+3(2)=10
$$

## D) Limit laws

If \(\lim_{x\to a}f(x)=L\) and \(\lim_{x\to a}g(x)=M\), then:

### Constant

$$
\lim_{x\to a}c=c
$$

### Identity

$$
\lim_{x\to a}x=a
$$

### Sum

$$
\lim_{x\to a}[f(x)+g(x)]=L+M
$$

### Difference

$$
\lim_{x\to a}[f(x)-g(x)]=L-M
$$

### Constant multiple

$$
\lim_{x\to a}[c f(x)]=cL
$$

### Product

$$
\lim_{x\to a}[f(x)g(x)]=LM
$$

### Quotient

$$
\lim_{x\to a}\frac{f(x)}{g(x)}=\frac{L}{M},\quad M\neq0
$$

### Power

$$
\lim_{x\to a}[f(x)]^n=L^n
$$

### Root

$$
\lim_{x\to a}\sqrt[n]{f(x)}=\sqrt[n]{L}
$$

when defined.

## E) Factoring limits

### Example

$$
\lim_{x\to2}\frac{x^2-5x+6}{x^2-12x+20}
$$

Factor:

$$
x^2-5x+6=(x-2)(x-3)
$$

$$
x^2-12x+20=(x-2)(x-10)
$$

So

$$
\lim_{x\to2}\frac{(x-2)(x-3)}{(x-2)(x-10)}
=
\lim_{x\to2}\frac{x-3}{x-10}
=
\frac{2-3}{2-10}
=\frac{-1}{-8}
=\frac18
$$

## F) Rationalization

Useful with roots.

### Example

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}
$$

Multiply by conjugate:

$$
\frac{\sqrt{x}-2}{x-4}\cdot\frac{\sqrt{x}+2}{\sqrt{x}+2}
=
\frac{x-4}{(x-4)(\sqrt{x}+2)}
=
\frac{1}{\sqrt{x}+2}
$$

Now let \(x\to4\):

$$
\frac{1}{2+2}=\frac14
$$

## G) Special trigonometric limits

These are very important:

$$
\lim_{x\to0}\frac{\sin x}{x}=1
$$

$$
\lim_{x\to0}\frac{\tan x}{x}=1
$$

$$
\lim_{x\to0}\frac{1-\cos x}{x}=0
$$

Also,

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12
$$

### Example

$$
\lim_{x\to0}\frac{\sin(3x)}{x}
=
3\lim_{x\to0}\frac{\sin(3x)}{3x}
=3
$$

## H) Infinite limits and asymptotic behavior

### Exponential

$$
\lim_{x\to\infty}e^x=\infty
$$

$$
\lim_{x\to-\infty}e^x=0
$$

### Logarithm

$$
\lim_{x\to\infty}\ln x=\infty
$$

$$
\lim_{x\to0^+}\ln x=-\infty
$$

### Reciprocal powers

If \(r>0\),

$$
\lim_{x\to\infty}\frac{c}{x^r}=0
$$

### Example

$$
\lim_{x\to\infty}\frac{5}{x^2}=0
$$

### Polynomial growth

For \(r>0\),

$$
\lim_{x\to\infty}x^r=\infty
$$

If \(r\) is an even integer:

$$
\lim_{x\to-\infty}x^r=\infty
$$

If \(r\) is an odd integer:

$$
\lim_{x\to-\infty}x^r=-\infty
$$

## I) Growth hierarchy

As \(x\to\infty\):

$$
\ln x \ll x^a \ll a^x
$$

for \(a>1\).

Meaning:

- logarithms grow slower than powers
- powers grow slower than exponentials

### Examples

$$
\lim_{x\to\infty}\frac{\ln x}{x}=0
$$

$$
\lim_{x\to\infty}\frac{x^2}{2^x}=0
$$

---

# 10) L’HÔPITAL’S RULE

If

$$
\lim_{x\to a}\frac{f(x)}{g(x)}
$$

gives an indeterminate form:

- \(\frac00\)
- \(\frac{\infty}{\infty}\)

and the conditions hold, then

$$
\lim_{x\to a}\frac{f(x)}{g(x)}
=
\lim_{x\to a}\frac{f'(x)}{g'(x)}
$$

if the new limit exists.

### Example

$$
\lim_{x\to0}\frac{\sin x}{x}
$$

This is \(\frac00\), so:

$$
\lim_{x\to0}\frac{\cos x}{1}=1
$$

### Another example

$$
\lim_{x\to\infty}\frac{\ln x}{x}
$$

This is \(\frac{\infty}{\infty}\), so:

$$
\lim_{x\to\infty}\frac{1/x}{1}
=
\lim_{x\to\infty}\frac1x
=0
$$

---

# 11) MEAN VALUE THEOREM

If \(f\) is:

- continuous on \([a,b]\)
- differentiable on \((a,b)\)

then there exists \(c\in(a,b)\) such that

$$
f'(c)=\frac{f(b)-f(a)}{b-a}
$$

This means: at some point, the instantaneous rate equals the average rate.

### Example

Let \(f(x)=x^2\) on \([1,3]\).

Average slope:

$$
\frac{f(3)-f(1)}{3-1}
=
\frac{9-1}{2}=4
$$

Since \(f'(x)=2x\), we set

$$
2c=4 \Rightarrow c=2
$$

So \(c=2\) is the point guaranteed by the theorem.

---

# 12) CONTINUITY CHEAT SHEET

A function is continuous at \(x=a\) if:

$$
\lim_{x\to a}f(x)=f(a)
$$

This requires:

1. \(f(a)\) exists  
2. \(\lim_{x\to a}f(x)\) exists  
3. both are equal  

Polynomials, exponentials, trig functions, and logs on their domains are continuous.

### Common discontinuities

- removable discontinuity
- jump discontinuity
- infinite discontinuity

### Example of removable discontinuity

$$
f(x)=\frac{x^2-1}{x-1}
$$

For \(x\neq1\),

$$
f(x)=x+1
$$

So the limit at \(x=1\) is \(2\), but \(f(1)\) is undefined.

That is a removable discontinuity.

---

# 13) VERY COMMON DERIVATIVE EXAMPLES

## Example 1

$$
\frac{d}{dx}(x^3+4x-7)=3x^2+4
$$

## Example 2

$$
\frac{d}{dx}(x^2\cos x)=2x\cos x-x^2\sin x
$$

## Example 3

$$
\frac{d}{dx}\left(\frac{\ln x}{x}\right)
=
\frac{(1/x)(x)-(\ln x)(1)}{x^2}
=
\frac{1-\ln x}{x^2}
$$

## Example 4

$$
\frac{d}{dx}(e^{x^2+1})=2x e^{x^2+1}
$$

## Example 5

$$
\frac{d}{dx}\sin(3x^2)=6x\cos(3x^2)
$$

## Example 6

$$
\frac{d}{dx}\log_5(x^2+4)=\frac{2x}{(x^2+4)\ln 5}
$$

## Example 7

$$
\frac{d}{dx}(x^x)=x^x(\ln x+1)
$$

## Example 8

$$
\frac{d}{dx}|x-3|=\frac{x-3}{|x-3|},\quad x\neq3
$$

---

# 14) ULTRA-COMPACT MEMORY SHEET

## Derivatives

$$
(c)'=0
$$

$$
(x)'=1
$$

$$
(x^n)'=nx^{n-1}
$$

$$
(f\pm g)'=f'\pm g'
$$

$$
(cf)'=cf'
$$

$$
(fg)'=f'g+fg'
$$

$$
\left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}
$$

$$
(f(g(x)))'=f'(g(x))g'(x)
$$

$$
(e^x)'=e^x
$$

$$
(a^x)'=a^x\ln a
$$

$$
(\ln x)'=\frac1x
$$

$$
(\ln|x|)'=\frac1x
$$

$$
(\log_a x)'=\frac1{x\ln a}
$$

$$
(\sin x)'=\cos x
$$

$$
(\cos x)'=-\sin x
$$

$$
(\tan x)'=\sec^2 x
$$

$$
(\cot x)'=-\csc^2 x
$$

$$
(\sec x)'=\sec x\tan x
$$

$$
(\csc x)'=-\csc x\cot x
$$

$$
(\arcsin x)'=\frac1{\sqrt{1-x^2}}
$$

$$
(\arccos x)'=-\frac1{\sqrt{1-x^2}}
$$

$$
(\arctan x)'=\frac1{1+x^2}
$$

$$
([f(x)]^n)'=n[f(x)]^{n-1}f'(x)
$$

$$
(e^{f(x)})'=f'(x)e^{f(x)}
$$

$$
(a^{f(x)})'=a^{f(x)}\ln(a)f'(x)
$$

$$
(\ln(f(x)))'=\frac{f'(x)}{f(x)}
$$

$$
(\ln|f(x)|)'=\frac{f'(x)}{f(x)}
$$

$$
(\log_a(f(x)))'=\frac{f'(x)}{f(x)\ln a}
$$

$$
(\sin(f(x)))'=f'(x)\cos(f(x))
$$

$$
(\cos(f(x)))'=-f'(x)\sin(f(x))
$$

$$
(\tan(f(x)))'=f'(x)\sec^2(f(x))
$$

$$
(\sec(f(x)))'=f'(x)\sec(f(x))\tan(f(x))
$$

$$
(\arctan(f(x)))'=\frac{f'(x)}{1+(f(x))^2}
$$

$$
(|x|)'=\frac{x}{|x|},\quad x\neq0
$$

$$
(f(x)^{g(x)})'
=
f(x)^{g(x)}
\left[
g'(x)\ln(f(x))+g(x)\frac{f'(x)}{f(x)}
\right]
$$

## Limits

$$
\lim_{x\to a}c=c
$$

$$
\lim_{x\to a}x=a
$$

$$
\lim_{x\to a}[f(x)\pm g(x)]=L\pm M
$$

$$
\lim_{x\to a}[f(x)g(x)]=LM
$$

$$
\lim_{x\to a}\frac{f(x)}{g(x)}=\frac{L}{M},\ M\neq0
$$

$$
\lim_{x\to0}\frac{\sin x}{x}=1
$$

$$
\lim_{x\to0}\frac{\tan x}{x}=1
$$

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12
$$

$$
\lim_{x\to\infty}e^x=\infty
$$

$$
\lim_{x\to-\infty}e^x=0
$$

$$
\lim_{x\to\infty}\ln x=\infty
$$

$$
\lim_{x\to0^+}\ln x=-\infty
$$

$$
\lim_{x\to\infty}\frac{1}{x^r}=0,\quad r>0
$$

---

# 15) FINAL IMPORTANT IDENTITY BOX

These are the ones students forget most often:

$$
\log_a x=\frac{\ln x}{\ln a}
$$

$$
\frac{d}{dx}(\log_a x)=\frac{1}{x\ln a}
$$

$$
\frac{d}{dx}(\log_a(f(x)))=\frac{f'(x)}{f(x)\ln a}
$$

$$
f(x)^{g(x)}=e^{g(x)\ln(f(x))}
$$

$$
\frac{d}{dx}(f(x)^{g(x)})
=
f(x)^{g(x)}
\left[
g'(x)\ln(f(x))+g(x)\frac{f'(x)}{f(x)}
\right]
$$

$$
\frac{d}{dx}(\ln|f(x)|)=\frac{f'(x)}{f(x)}
$$

$$
\frac{d}{dx}(x^x)=x^x(\ln x+1)
$$

---

# 16) MINI EXAM VERSION

## If you only want the shortest survival sheet

$$
(c)'=0,\quad (x)'=1,\quad (x^n)'=nx^{n-1}
$$

$$
(fg)'=f'g+fg',\quad \left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}
$$

$$
(f(g(x)))'=f'(g(x))g'(x)
$$

$$
(e^x)'=e^x,\quad (a^x)'=a^x\ln a
$$

$$
(\ln x)'=\frac1x,\quad (\log_a x)'=\frac1{x\ln a}
$$

$$
(\sin x)'=\cos x,\quad (\cos x)'=-\sin x,\quad (\tan x)'=\sec^2 x
$$

$$
(\arcsin x)'=\frac1{\sqrt{1-x^2}},\quad (\arctan x)'=\frac1{1+x^2}
$$

$$
([f(x)]^n)'=n[f(x)]^{n-1}f'(x)
$$

$$
(a^{f(x)})'=a^{f(x)}\ln(a)f'(x)
$$

$$
(\ln(f(x)))'=\frac{f'(x)}{f(x)}
$$

$$
(f(x)^{g(x)})'
=
f(x)^{g(x)}
\left[
g'(x)\ln(f(x))+g(x)\frac{f'(x)}{f(x)}
\right]
$$

$$
\lim_{x\to0}\frac{\sin x}{x}=1,\quad
\lim_{x\to0}\frac{\tan x}{x}=1,\quad
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12
$$

$$
\log_a x=\frac{\ln x}{\ln a}
$$
