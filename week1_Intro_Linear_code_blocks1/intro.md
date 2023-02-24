# Introduction
## Coding types

1. Inputs k bits, output n bits. Usually n is greater than k.
   - $u(i) = (u_1,u_2,u_3,....,u_k)$ and $c(i)=(c_1,c_2,c_3,...,c_n)$
2. We focuses mainly on linear coding.
3. Since it is linear, we can perform Z(D)-transform then converting it into frequency domain.
4. Linear transform property, memoryless property.

## Two major code before midterm, Block code and convolutional code.
5. Block coding is memoryless.
6. Convoulutional code however, is not memoryless.
## Is block coding a special case for convolutional code?
> In general case, in convolutional code, the k and n are usually small. In block code,k and n are usually very large, so they are not the same.Alias can occurs if you try to use block coding as a case of convolutional code.

7. In common case, we assume within memory has only 0 bytes.

## How about other code Turbo,LDPC?
> Other codes like turbo code, polar code are usually just a combination or extension of block & convolutional code

## Algebra Representation for code is important!
1. ECC focuses a lot on subspaces which lies within vector space.
2. However, now field comes from finite space, the are no longer $R$ or $C$, now the filed in $F^4$, a finite integer field.


# Geometry
1. Trellis, factor graph and factor graph