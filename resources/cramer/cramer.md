---

title: Cramer's Rule

layout: single

style: single

---

Cramer's Rule
-------------

Cramer's rule is a method of solving $n$ simultaneous equations for $n$
unknowns.

-   Any system of equations of this kind can be written in the form

    $$\begin{array}{c}
    a_{11} \, x_1 + a_{12} \, x_2 + ... + a_{1n} \, x_n = b_{1} \\
    a_{21} \, x_1 + a_{22} \, x_2 + ... + a_{2n} \, x_n = b_{2} \\
    \vdots \\
    a_{n1} \, x_1 + a_{n2} \, x_n + ... + a_{nn} \, x_n = b_{n} 
    \end{array}
    \label{eq:neq}$$

-   The coefficients on the left side of Eq.'s 1 can be written as a
    matrix,

    $$A = 
    \left(
    \begin{array}{cccc}
    a_{11}  & a_{12} & ...    & a_{1n} \\
    a_{21}  & a_{22} & ...    & a_{2n} \\
    \vdots  &\vdots  & \ddots & \vdots \\
    a_{n1}  & a_{n2} & ...    & a_{nn}
    \end{array}
    \right)$$

-   The value of any of the $x_i$ can be found via

    $$x_i = \frac{|B_i|}{|A|}
    \label{eq:sols}$$

    where the notation $|A|$ and $|B_i|$ denote the determinants of
    matrices $A$ and $B_i$, and the matrix $B_i$ is obtained by
    replacing the $i^{th}$ column of matrix $A$ with the coefficients on
    the left side of Eq.'s 1 For example,

    $$B_2 = 
    \left(
    \begin{array}{cccc}
    a_{11} & b_1    & ...    & a_{1n} \\
    a_{21} & b_2    & ...    & a_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{n1} & b_n    & ...    & a_{nn}
    \end{array}
    \right)$$

### The $\mathbf{n=2}$ Case

-   Two equations involving two unknowns can be written in the form

    $$\begin{array}{c}
    a_{11} \, x_1 + a_{12} \, x_2 = b_{1} \\
    a_{21} \, x_1 + a_{22} \, x_2 = b_{2} 
    \end{array}$$

    which yields

    $$A = 
    \left(
    \begin{array}{cc}
    a_{11} & a_{12} \\
    a_{21} & a_{22} 
    \end{array}
    \right)$$

-   Eq. 3 gives

    $$x_1 = 
    \frac{
    \left|
    \begin{array}{cc}
    b_1 & a_{12} \\
    b_2 & a_{22} 
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{cc}
    a_{11} & a_{12} \\
    a_{21} & a_{22} 
    \end{array}
    \right|
    }
    =
    \frac{b_1 \, a_{22} - a_{12} \, b_2}
    {a_{11} \, a_{22} - a_{12} \, a_{21}}$$

    and

    $$x_2 = \frac{
    \left|
    \begin{array}{cc}
    a_{11} & b_1 \\
    a_{21} & b_2 
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{cc}
    a_{11} & a_{12} \\
    a_{21} & a_{22} 
    \end{array}
    \right|
    }
    =
    \frac{a_{11} \, b_2 - b_1 \, a_{21}}
    {a_{11} \, a_{22} - a_{12} \, a_{21}}$$

### An $\mathbf{n=2}$ Example

-   The system of equations

    $$\begin{array}{c}
    2 \, x_1 - \, x_2 = 1 \\
    5 \, x_1 + 3 \, x_2 = 2
    \end{array}
    \label{eq:2eq}$$

    has solutions

    $$x_1 = 
    \frac{
    \left|
    \begin{array}{cc}
    1 & -1 \\
    2 & 3 
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{cc}
    2 & -1 \\
    5 & 3 
    \end{array}
    \right|
    }
    = \frac{5}{11}$$

    and

    $$x_2 = 
    \frac{
    \left|
    \begin{array}{cc}
    2 & 1 \\
    5 & 2 
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{cc}
    2 & -1 \\
    5 & 3 
    \end{array}
    \right|
    }
    = -\frac{1}{11}$$

-   The results can be verified by substituting them into either of
    Eq.'s 9,

    $$\frac{10}{11} + \frac{1}{11}  = \frac{11}{11} = 1
    \hspace{24pt}\checkmark$$

### An $\mathbf{n=3}$ Example

-   The system of equations

    $$\begin{array}{c}
    2 \, x_1 - ~ \, x_2 + 4 \, x_3 = 2 \\
    5 \, x_1 + 3 \, x_2 + 2 \, x_3 = 1 \\
    ~~~ \, x_1 + 6 \, x_2 + ~~ \, x_3 = -3 \\
    \end{array}
    \label{eq:3eq}$$

    has solutions

    $$\nonumber
    x_1 = 
    \frac{
    \left|
    \begin{array}{ccc}
     2 & -1 & 4 \\
     1 &  3 & 2 \\
    -3 &  6 & 1
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{ccc}
     2 & -1 & 4 \\
     5 &  3 & 2 \\
     1 &  6 & 1
    \end{array}
    \right|
    }$$

    $$x_1 = 
    \frac{
        2 (3 \cdot 1 - 2 \cdot 6)
    - (-1)(1 \cdot 1 - 2 \cdot -3)
    +   4 (1 \cdot 6 - 3 \cdot -3)
    }{
        2 (3 \cdot 1 - 2 \cdot 6)
    - (-1)(5 \cdot 1 - 2 \cdot 1)
    +   4 (5 \cdot 6 - 3 \cdot 1)
    } = \frac{49}{93}$$

    $$x_2 =
    \frac{
    \left|
    \begin{array}{ccc}
     2 &  2 & 4 \\
     5 &  1 & 2 \\
     1 & -3 & 1
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{ccc}
     2 & -1 & 4 \\
     5 &  3 & 2 \\
     1 &  6 & 1
    \end{array}
    \right|
    }$$

    $$=  
    \frac{
      2 (1 \cdot 1 - 2 \cdot -3)
    - 2 (5 \cdot 1 - 2 \cdot  1)
    + 4 (5 \cdot -3 - 1 \cdot 1)
    }{93} 
    = -\frac{56}{93}$$

    and

    $$x_3 =
    \frac{
    \left|
    \begin{array}{ccc}
     2 & -1 &  2 \\
     5 &  3 &  1 \\
     1 &  6 & -3
    \end{array}
    \right|
    }{
    \left|
    \begin{array}{ccc}
     2 & -1 & 4 \\
     5 &  3 & 2 \\
     1 &  6 & 1
    \end{array}
    \right|
    }$$

    $$=
    \frac{
        2 (3 \cdot -3 - 1 \cdot 6)
    - (-1)(5 \cdot -3 - 1 \cdot 1)
    +   2 (5 \cdot  6 - 3 \cdot 1)
    }
    {93}
    =
    \frac{8}{93}$$

-   The results can be verified by substituting them into any of
    Eq.'s 13,

    $$\frac{2 \cdot 49 - (-56) + 4 \cdot 8}{93} = \frac{186}{93} = 2
    \hspace{24pt}\checkmark$$

This work is licensed under the Creative Commons Attribution-ShareAlike
4.0 International License:
<http://creativecommons.org/licenses/by-sa/4.0/>.\
L.A. Riley (`lriley@ursinus.edu`), updated June 2021
