# Elementary Linear Algebra <small>with Professor Vladimir Shtelen</small>
## Chapter 3 - Determinants
### 3.1 Cofactor Expansion
#### Reading
- For 2 by 2 matrices,
	- The scalar `ad - bc` determines whether or not the preceding matrix A is invertible.
	- A matrix `[a d, c d]` is invertible if and only if `ad - bc ≠ 0`.
	- If `ad - bc ≠ 0`, then `A^{-1} = (1)/(ad - bc)*[d -b, -c a]`.
- For any arbitrary matrices `A` with n by b rows and columns,
	- det(A) = a_{i1}c_{i1} + a_{i2}c_{i2} + … + a_{in}c_{in}
		- This is called the **cofactor expansion** of `A` along row `i`.
#### Khan Academy - [3x3 Determinant](http://www.khanacademy.org/math/linear-algebra/v/linear-algebra--3x3-determinant)
- If `B = [a b, c d]`, then `det(B) = ad - bc`
- As long as that does not equal zero, then B is invertible.
- `B^{-1} = (1 / ad - bc)[d -b, -c a]`
### 3.2 Properties of Determinates
#### Reading
- Let `A` be an `n x n` matrix:
	1. If `B` is a matrix obtained by interchange two rows of `A`, the `det(B) = -det(A)`.
	2. If `B` is a matrix obtained by multiplying each entry of some row of `A` by a scalar `k`, then `det(A) = k*det(A)`
	3. If `B` is a matrix obtained by adding a multiple of some row of `A` to a different row, then `det(B) = det(A)`
	4. For any `n x n` elementary matrix `E`, we have `det(EA) = det(A)det(A)`
- Let `A` and `B` be square matrices of the same size. The follow statements are true:
	1. `A` is invertible if and only if `det(A) ≠ 0`
	2. `det(AB) = det(A)*det(B)`
	3. `det(A^T) = det(A)`
	4. If `A` is invertible, the `det(A)^{-1} = (1)/(det(A))`
- **Cramer's Rule**: Let `A` be an invertible `n x n` matrix, `b` be in `R^n`, and `M_i` be the matrix obtaind from `A` by replacing column `i` of `A` by `b`. Then `Ax = b` has a unique solution `u` which the components are given by: `u = det(M_i)/det(A)` for `i = 1, 2, … n`. 

## Chapter 4 - Subspaces and Their Properties 
### 4.1 Subspaces
#### Reading
- Definition:
	1. The zero vector belongs to `W`.
	2. Whenever `u` and `v` belong to `W`, the `u+v` belongs to `W`.
	3. Whenever `u` belongs to `W` and `c` is a scalar, `cu` belongs to `W'.
- The span of a finite nonempty subset of `R^n` is a subspace of `R^n`
- **Column space** of a matrix is the span of it's columns.
- **Null space** of a matrix is the solution set of `Ax = 0`.
	- If `A` is an `m x n` matrix, then `nul(A)` is a subspace of `R^n`.
- The range of a linear transformation is the same as the column space of its standard matrix.
- The null space of linear transformation is the same as the null space of its standard matrix.

#### Khan Academy - [Linear Subspaces](http://www.khanacademy.org/math/linear-algebra/v/linear-subspaces)
##### Introduction
- A linear subspace of `R^n` with `V`, a subset of `R^n`
- `R^n` is an infinitely large vector.
- `V` is a subset of `R^n`, it could be all though.
- In order for `V` to be a subspace, or linear subspace, this means, by definition, three things:
	1. `V` contains the zero vector.
	2. *Closure under scalar multiplication*
		* "If I multiply a scalar by my vector, I'm still in my subspace, my subset of `R^n`
	3. If `a` is in `V` and `b` is in `V`, `a + b` is in `V` - *Closure under addition*
		* "If I add two vectors in my set, I'm still in my set."

##### Examples
- `V = {0} = {[0, 0, 0]}`
	1. It *is* the zero vector.
	2. It is closed under multiplication.
	3. It is closed under addition.

- `S = {[x_1 x_2] .in R^2 | x_1 >= 0}`
	1. It contains the zero vector.
	2. It is closed under addition.
	3. It is *not* closed under multiplication. 

- `U = span([1 1]`
	* The span of this is the line defined by `x`.
	* "Any vector on this line added to any other vector on this line will be a vector on this line.
	* "Any vector on this line multiplied by any other vector on this line will be a vector on this line."

##### Span
- `U = span(v_1, v_2, v_3) = valid subspace of R^n` (?)
	1. `0 * v_1 + 0 * v_2 + 0 * v_3 = {0}`
		* Contains zero vector
	2. `x = c_1 * v_1 + c_2 * v_2 + c_3 * v_3`
		* Closed under multiplication
- So the span of any linear combination is a valid subspace!

### 4.2 Basis and Dimension of a Subspace 
#### Reading
- Let `V` be a nonzero subspace of `R^n`. A **basis** for `V` is a linearly independent generating set for `V`.
- The pivot columns of a matrix form a basis for its column space.
- **Reduction theorem**: Let `S` be a finite generating set for a nonzero subspace of `V` of `R^n`. Then `S` can be reduced to a basis for `V` by romping vectors from `S`.
- Let `S` be a finite subset of `R^n`. Then, the following are true:
	1. If `S` is a generating set for `R^n`, then `S` contains at least `n` vectors.
	2. If `S` is linearly independent, then `S` contains at most `n` vectors.
	3. If `S` is a basis for `R^n`, then `S` contains exactly `n` vectors.
- **Extension theorem**: Let `S` be a linearly independent subset of a nonzero subspace `V` of `R^n`. Then, `S` can be extended to a basis for `V` by inclusion of additional vectors. In particular, every nonzero subspace has a bases.
- Let `V` be a nonzero subspace of `R^n`. Then any two bases for `V` contain the same number of vectors.
- A basis is a generating set for a subspace containing the fewest possible vectors.
- A basis is linearly independent subset of a subspace that is as large as possible.
- The number of vectors in a basis for a nonzero subspace `V` of `R^n` is called the **dimension** of `V` and is denoted by `dim(V)`. It is convenient to define the dims ions of the zero subspace of `R^n` to be 0.
- Let `V` be a subspace of `R^n` with dimension `k`. Then every linearly independent subset of `V` contains at most `k` vectors; or equivalently, any finite subset of `V` containing more than `k` vectors is linearly dependent.
- Let `V` be a k-dimensional subspace of `R^n`. Suppose that `S` is a subset of `V` with exactly `k` vectors. The `S` is a basis for `V` if either `S` is linearly independent or `S` is a generating set for `V`.
- Steps to show that a set `B` is a basis for a subspace `V` of `R^n`
	1. Show that `B` is contained in `V`.
	2. Show that `B` is linearly independent (or that  is a generating set for `V`)
	3. Compute the dimension of `V`, and confirm that the number of vectors in `B` equals the dimension of `V`.

#### Lecture
- Where V is a subspace of R^n, if and only if:
	1. `o` is and element in `V`
	2. for any `u` and `v` vectors from `V: u + v` is an element in `V`
	3. for any `u` element in `V` and any alpha element in `R`, `alpha*u element in R`
- Subspaces associated with a matrix `A = ((u_1)(u_2) … (u_n))` where `A` is an `n x m` matrix
	1. `Col(A) = Span{columns of A} element in R^n`
	2. `Row(A) = Span(Rows of A) element in R^n`
	3. `Nul(A) = {Set of all solutions of AX = 0}`
	4. `Nul(A^T) = {Set of all solutions of A^(T)X = 0}`
- Basis of a subspace `V` is minimal spanning set of `V`

#### Khan Academy - [Basis of a Subspace](http://www.khanacademy.org/math/linear-algebra/v/linear-algebra--basis-of-a-subspace)
- `V = span(v_1, v_2, … v_n)` where all vectors are linearly independent.
	* The only solution to `c_1 * v_1 + c_2 *  v_2, + …  c_n * v_n` is `0`
- If `S` is a **basis** for `V`, it is a linearly independent generating set.
	* The "minimum" set of vectors that spans the subspace.

##### Examples

- `S = {[2 3],[7 0]}`
- `span(s) = ?`
	* `2c_1 + 7c_2 = x_1` => c_2 = (x_1 / 7) - (2 / 21)x_2
	* `3c_1 + 0c_2 = x_2` => c_1 = x_2 / 3
		+ The span of `S` is `R^2`
	* Being as the only solution to `x_1` and `x_2` being zero is zero, the set is linearly independent.


### 4.3 The Dimension of Subspace Associated with a Matrix
#### Reading
- The dimension of the column space of a matrix equals the rank of the matrix.
- The dimensions of the null space of a matrix equals the nullity of the matrix.
- The nonzero rows of the reduced row echelon form of a matrix constitute a basis for the row space of the matrix.

#### Lecture
##### Quick review
- For subspace `V` in `R^n`
	1. For vector `o` in `V`
	2. For all u and v in V : u + v is an element in V
	3. For all u element in V and for all alpha in R : alpha*v is an element in V
- Span of any finite set of vectors from `R^n` a subspace of `R^n`.
- Minimal spanning set is called a basis.
- Number of vectors in a basis is called the dimension of a subspace.

##### Basis and Dimension
- Let `A` be an `m` by `n` matrix. Then
	1. `Col(A) = Span{columns of A}`
		- To find a basis for `Col(A)`, `A -ERO-> A_REF` basis is set of pivotal columns of A.
		- `dim Col(A) = rank(A)`
	2. `Row(A) = Span{rows of A} element in R^n`
		- Since `Span{Rows in a} = Span{Rows A_RREF}`, then we can choose a basis of `Row(A)` set of nonzero rows of `A_RREF`
		- `dim Row(A) = rank(A)`
	3. The null space of A
		- Null(A)= {Set of all solution of AX = 0} = Span{(), ()} (The general solution of AX = 0 in vector form.)
		- `dim[Null(A)] = null(A) = n - rank(A)`
	4. The null space of A^T : Null(A^T) = {Set of all solutions of A^T X = 0} element in R^m
		- `dim[Null(A^T)] = null(A^T) = m - rank(A^T)`

##### Quiz information
- The quiz will be on the material since the exam.
- Format of quiz will be similar as first.
- One set of true false and 4 computational.
- No proofs.
- Topics:
	- LU Decomposition
	- Determinants
	- Kramer's rule
	- Subspaces

## Chapter 5 - Eigenvalues, Eigenvectors, and Diagonaization
### 5.1 Eigenvalues and Eigenvectors
#### Lecture - November 6th, 2012
- Let `A` be an `n x n` matrix. If for a non-zero vector `s : AS = λ S` for some scalar `λ`, then `S` is called an **eigenvector** of `A` and `λ` is called a corresponding **eigenvalue**.

### 5.2 The Characteristic Polynomial
#### Lecture - November 6th, 2012
- If `M` is invertible, then `M^{-1}MS = -> S = 0`. Therefore, when `M` is invertible, the nay solution of `MS = 0` is `S = 0`. Therefore, for `MS = 0` to have a non-zero solutions, `M` must be non-invertible, that is `det(A) = 0`.
- `det(M) = 0` it's polynomial equation of degree `n` in `λ`. Solutions of this equation are eigenvalues of `A`
- The dimension of the eigenspace of `A` associated with an eigenale `λ` is equal or it is less than the multi[plicty of the eigenvalue. 

### 5.3 Diagonalization of a Matrix
#### Lecture - November 9th, 2012
- Let `A` and `B` be `n x n` matrices. These matrices are called similar if there exists an invertible `n x n` matrix such that `B = C^{-1} x A x C`
	- Similar matrices have the same eigenvalues
- An `n x n` matrix `D` is called diagonal if all the elements not on the main diagonal are zero.
- An `n x n` matrix `A` is called diagonalizable if there exists an invertible matrix `S` such that `D = S^{-1} x A x S`
- Let `A` and `S` be some `n x n` matrices and let D be a diagonal `n x n` matrix. `S = ((S_1), (s_2), … (s_n)), … `
- `S` is invertible if and only is `rank(S) = n`, this means that columns of `S` are linearly independent.
- A is diagonalizable if and only if it has `n` linearly independent independent eigenvectors.
- If `A` has no repeated eigenvalues, then it is diagonalizable.
- Eigenvectors associated with different eigenvalues are linearly independent.
- If `A` has repeated eigenvalues but the dimension of each eigenspace is the same as the multiplicity of the corresponding eigenvalue, then `A` has a linearly independent eigenvector and therefore `A` is diagonalizable. Otherwise, `A` is *not* diagonalizable.

##### Test
- Determinants
- Cramer's rule
- Subspaces
- Diagonalization 

## Chapter 6
### 6.1 Geometry of Vectors
- The dot product is a function on two vectors which yields a number by multiplying `u_1 x u_2 + ... + u_n x v_n`
	1. Commutative
	2. Always greater than zero for an `u` that is non-zero.

### 6.2 Orthogonal Sets of Vectors
- Let W be a subspace of R^n. Set of all vectors from R^n that are perpendicular to any vector from W is called orthogonal complement of W and is denoted by W^⟂.

Gram-Scmhit
Projection
Least Squares

## Final Exam
- Total number of up to 11 problems, with one set of true/false questions.
- Problems on solving system using
- Formulas to memorize:
	+ `P_w = A(A^T*A)^-1*A^T`
		* See if A, is in general, the form of, where `w` is the span of something and matrix `A` is the matrices formed by the column of something `k` by `k`.
		* A here is 
	+ [a_0, a_1] = (A^TA)^-1A^TY
	+ `R_\theta = [cos\theta -sin\theta, sin\theta cos\theta]
	+ LU, QR, GS-process, A->REF->RREF
- Not on exam:
	+ Sections we skipped, something from, go to very beginning, we didn't have time to do 2.5
	+ Didn't 6.6 in consist systems
- Please review our midterms, thats practice, but not focus only on those
- Application of eigenvalues, systems of linear differential equations, y-prime, systems of differential equations, 5.5
- Diagolizations of symmetric matrices and application to quadratic curves, ellipse, hyperbola, circle, find orthogonal diagonal of symmetric, identify the curve described by quadratic equation with mixed, ientityf curve, draw the curve, figure out what the angle of rotation of coordinates, by matching the q-transposed and the rotation matrix. 
