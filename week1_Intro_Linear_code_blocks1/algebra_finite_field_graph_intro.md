# Code on algebra
1. Needs number theory. Group, ring, fields.
2. Finite fields are used for our analysis.

# Block code
0. Simply think about G matrix and H matrix.
1. A subspace of a vector space.  We must find the basis or the normal vector of the subspace, inner product. Normal vectors exists with $R^{n-k}$. This result can be easily derived from SVD.
2. Consider $A^{n x m}$. $R(A)^{\perp}$ is the normal vector subspace we would like to focus on.
3. 2G, 3G uses BCH and RS codes.
4. 5G uses Polar code and LPDC codes for information transmission.


# [7,4,3]Hamming Code
0. [N,K,D]
1. Length N = 7, all consists of (1,0), having $2^7$ combinations bit strings.
2. K= 4 bits are information bits. D = 3 are denoted as the hamming distance.
3. Hamming distance meaning, from a bit string to another bit string requires at least a hamming distance of 3, i.e. changing 3 bits to reach.
4. Thus 7 bits can be transmitted, however if we send 7 bits through a medium, error might occurs. How do I detect the error?
5. The hamming distance specify allows self correcting through drawing a certain set. If the after changed is still within this set, it can be corrected.
6. Usually we hope K and D to be as large as possible under a fixed N. $\exist set (K,D)$ that reach the best performance which are proven by mathematician.

> Like in ASCII, we add a parity bit in the last bit in bit string, the receiver can immediatly detect error through the parity bit.

1. Right now 6 bits are contenets, reserve 1 bit for partiy bit. Used to check whether the bit is even or odd. Yet I cannot fix the error like this.

# Graph descrition
1. We want the code falls within these 3 sets, we want all of the whole sets to be even.
2. The information bit within the intersection can be chose as the carrier. Other 3 bits are used as error checking bits.
3. We represent the finite field representation in matrix form using hamming encoding.
4. From linear algebra, if we impose a constraint, the dimension of the range space went down by 1. If 3, rank(A) went dowm by 3.

# Hamming distance
1. 1,7,7,1
2. The swap in bits to get to another encoded string.
3. In this arithemtic space, even means 0, odd means 1. Due to the finite binary field property.
4. Finite filed space {0,1}.
5. We can definitely find 4 independent vectors from this code.
# Steps
1. G is used as encoder, H is used as decoder step.


# Generalization
1. Hamming coding has the following property.
<br />
$rank(H) = r$
<br />
$[2^r-1,2^r-1-r,3]$ Hamming code is thus generated


# Finite fields
## Prime field
1. As long as p is prime
2. In prime field, we use the quotient of prime p as our number that falls within this field.
## Extension field
1. In Extension field, we consider polynomials' quotients. Their quotients are a field.
2. As long as the quotient are not decomposible, this field generated is a finite field.
3. The quotient of polynomial with the higher order is called the primitive polynomial.

## Decoding region
1. $2^{n-k}$ want the decoding region to be average for every set.
2. Usually we want the probability of decoding, so we want tho find the maximum posterior for a particular encoding schememe.
3. We will not use MLD(Maximum likelihood decoding) in practice, because this is simplfy brute force.
4. t-error detecting means if we have t errors in bit-string, we can still distinguish where this error bit string is from.

## Code on graph
1. Describe codes using graph instead of using finite field.
2. Trellis of convolutional code.
3. General factor graph and the sum product algorithm.

### Factor graph
1. Decompose a function into product of sub-functions.
2. Cycle leads to non-optimal decoding.
3. Different graph can be drawn from two forms of the same function, one is using a single node, another uses multiple nodes, however, this multiple nodes desciption might be acylitic.
4. We can describe any code into tanner graph.
5. Usually we would want the check, + , to have the same number of connections outward. We can run decoding on this graph.
6. Trellis, $[(s0,c1,s2)]$ s0,s1 is a node, from s0 to s1, c1 is the weight on the edge.
7. Turbo code connects a random interlever. Trellis leads to delay though performance is great.