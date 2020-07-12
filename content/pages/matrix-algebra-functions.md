Title: Matrix Algebra Functions
Date: 2014-10-06 15:08
Author: gavin
Slug: matrix-algebra-functions
Status: published

I have implemented a set of basic matrix algebra functions in Python
that I source within other Python scripts. I have tried to write them in
such a way that size and shape of the matrix is irrelevant, with the
exception of the determinant functions where I have hardcoded 2x2 and
3x3 functions. They work, but there is no guarantee that they use the
most efficient algorithms when used with large matrices.

The full set of functions can be found on
[GitHub](https://github.com/ghevcoul/matrixAlg), which includes:

-   2x2 and 3x3 determinants
-   Transpose
-   Dot product
-   Vector length
-   Matrix multiplication
-   Reduced row echelon form
-   Inverse
-   Print

