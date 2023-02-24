# Linear block codes
## [7,6,2] codes
1. Consider a [7,6,2] parity check code.
2. We want to find H matrix and G matrix.
3. Dimension the rank of H is 1 => G is 7-1 = 6. By rank-nullity.
4. Thus the solution space G is of 6. Thus we can pick 6 l.i vectors as the basis for our G matrix. However, G still need to maintain as 6x7.
5. H and G is not unique.

## [7,1,7] codes
1. It is not unique, as long as column space are preserved, it is a valid H or G.

## [7,4,3] hamming code
0. 7 bit code. As space of dimension 7.
1. 3 constraints rank(H) = 3, rank(G) = 7-3 = 4. With a hamming distance of 3.
2. This kind of design can ensure hamming distance is 3.
3. This can be extended to a more generalised version.
4. Hamming code can be easily described by H matrix. Since G is simply the perp of H.
5. The solution space == kernal of A.
6. H is the kernal of the code. G is the range. Possible l.c. of vectors I have.
7. The row vectors of G is the basis of the space.
8. G is known as the generation matrix.
9. Similiary, use H to describe. H is this parity check matrix. C matrix is the kernal space of H. H is the decoding matrix.

# What makes the best code?
> Hamming code is one of it. As one of the Linear Block codes $C(n,M,d)$

<br />Having M code words


# Hamming distance DEF
1. Simply look at the difference in bits.
2. This hamming distance is the inner product of this finite binray dimensional field.
3. This sastify all the property of finite dimensional inner product space.
4. Minimum hamming distance.
5. For a non-linear code. Need n choose 2 times to find the minimum hamming distance.

# Q-ary block code.
1. The finite space field is now of Q different possiblity. No longer binary only. The code implementation still works.
2. Linear $(N,K,D)$
3. Block code $C(n,M,d)$
4. For a linear code, we can represent $C[n,k,d]$ using G generator blocks and H generator blocks.