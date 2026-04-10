
## Solving Linear Equations

#### Substitution
$$
\begin{align} 
a_{11}x_{1}+a_{12}x_{2}&=c_{1}\\
a_{21}x_{1}+a_{22}x_{2}&=c_{2}\cdots solving:x_{1}\\
x_{1}&=\frac{c_{2}}{a_{21}}-\frac{a_{22}x_{2}}{a_{21}}\cdots substituting:x_{1} \\
a_{11}(\frac{c_{2}}{a_{21}}-\frac{a_{22}x_{2}}{a_{21}})+a_{12}x_{2}&=c_{1}\\
x_{2}(a_{12}-\frac{a_{22}a_{11}}{a_{21}}) &= c_{1} - \frac{a_{11}c_{2}}{a_{21}} \\
x_{2}&=\frac{c_{1}a_{21}-a_{11}c_{2}}{a_{12}a_{21}-a_{22}a_{11}} 
\end{align}
$$

#### Gaussian elimination
$$
\begin{pmatrix}
a_{11} & a_{12} & c_{1} \\
a_{21} & a_{22} &  c_{2} 
\end{pmatrix}

$$
r1 => r1/a11
r2 => r2 - a21*r1 
$$
\begin{pmatrix}
1 & \frac{a_{12}}{a_{11}} & \frac{c_{1}}{a_{11}} \\
0 & \frac{a_{22}a_{11}-a_{21}a_{12}}{a_{11}} & \frac{c_{2}a_{11} - a_{21}c_{1}}{a_{11}}
\end{pmatrix}
$$

r2 = r2 * a11/(a22a11-a21a12)
$$
\begin{pmatrix}
1 & \frac{a_{12}}{a_{11}} & \frac{c_{1}}{a_{11}} \\ \\
0 & 1 & \frac{c_{2}a_{11}-a_{21}c_{1}}{a_{22}a_{11}-a_{21}a_{12}}
\end{pmatrix}
$$


## Vectors, vector spaces & subspaces

- vectors are things that define a magnitude and direction
- ordered list of numbers that describe something
- anything that can be added together and multiplied by a scalar to give another of itself????

So, taking the vector u = (3,2), defined as an ordered list of numbers, it would be mapped to:

![Tux, the Linux mascot](C:\images\a.png)

They are essentially the same thing.

### Vector Addition

$$
\begin{align}
u &= \begin{bmatrix}
3 \\
2
\end{bmatrix} \\
v &= \begin{bmatrix}
4 \\
-1
\end{bmatrix} \\
w &= u + v \\
w &= \begin{bmatrix}
3 \\
2
\end{bmatrix} + \begin{bmatrix}
4 \\
-1
\end{bmatrix}  \\
w & = \begin{bmatrix}
7 \\
1
\end{bmatrix}
\end{align}
$$
Graphically, this can be represented as:

![vector addition](C:\images\vector_addition.png)



### Dot Product



![dot Multiplication](C:\images\vector_dot.png)

By the cosine law, the length of u-v and u and v are related by the formula:
$$
\begin{align}
c^2 & = a^2 + b^2 - 2ab\cos\theta\ \\
c & = \lVert u- v\rVert \\
a &= \lVert u \rVert , b= \lVert v \rVert \\
\lVert u-v \rVert ^2&= \lVert u \rVert ^2 + \lVert v \rVert ^2 - 2 \lVert u \rVert \lVert v \rVert \cos\theta \\
(u-v)\cdot(u-v) &= \lVert u \rVert ^2 + \lVert v \rVert ^2 - 2 \lVert u \rVert \lVert v \rVert \cos\theta \\
\lVert u \rVert ^2 + \lVert v \rVert ^2-2u\cdot v &= \lVert u \rVert ^2 + \lVert v \rVert ^2 - 2 \lVert u \rVert \lVert v \rVert \cos\theta \\
u\cdot v&= \lVert u \rVert \lVert v \rVert \cos\theta
\end{align}
$$

According to the image, the projection of u onto v is:
$$
\begin{align}
\lVert Proj \rVert _{uv} &= \lVert u \rVert \cos \theta \\
u\cdot v&= \lVert u \rVert \lVert v \rVert \cos\theta \\
u\cdot v &=  \lVert Proj \rVert _{uv} \cdot \lVert v \rVert \\
 \lVert Proj \rVert _{uv} &=  \frac{u \cdot v}{\lVert v \rVert} \\
Proj _{uv} &=  \frac{u \cdot v}{\lVert v \rVert^2} v
\end{align}
$$

So, the dot product can be defined as the magnitude of the vector that is the result of the orthogonal of one vector on the other, multiplied by the vector it is projected onto.

$$
\begin{align}
u\cdot v &= u_{x}v_{x} + u_{y}v_{y}
\end{align}
$$
### Scalar Multiplication

Scalar multiplication is literally "scaling" by some amount.


## Matrices and Matrix Operations

Matrixes are numbers arranged in rows and columns.

$$
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$
This matrix has m rows and n columns, so it is a mxn matrix.

Does it have other meaning?
- it is a representation of a linear transformation: it takes a vector in and spits out a vector. If applied to a set of vectors like a vector space, then it transforms the vector space 

#### Matrix addition
Add corresponding elements.


## The rest


- Linear independence, basis, rank
- Linear mappings (transformations)
- Affine spaces


