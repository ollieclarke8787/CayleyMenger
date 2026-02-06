# Macaulay2 Circuit Polynomial code

This folder contains a translation of some of the circuit polynomial output in `../CircuitPolynomials/` into the Macaulay2 language. Note that some of these files are very large and Macaulay2 may require additional resources to open them.

Each circuit polynomial is given as a **univariate polynomial** whose variable corresponds to a certain 'additional edge' of the rigidity circuit. In general the polynomial ring containing the circuit polyomial has the following form:

```
R = QQ[x_e : E(G) \ {a}][x_a]
```
where 'a' is the 'additional edge'.

## K4_circuit.m2

This file contains the circuit polynomial of K_4, which is a rigidity circuit. Its vertices are labelled by 1,2,3,4. The edge {3,4} is treated as the additional edge, i.e., the circuit polynomial is given in the ring:

```
R = QQ[x_(1,2),x_(1,3),x_(1,4),x_(2,3),x_(2,4)][x_(3,4)]
```

which is a univariate polynomial ring in variable x_(3,4).

## K33_plus_edge.m2

This file contains code for the rigidity circuit consisting of the graph K_3,3, together with an additional edge. The labelling of the graph is as follows: the two maximal independent sets are {1,4,5} and {2,3,6}; the additional edge is {4,5}.

## prism_plus_one.m2

This fle contains code for the circuit polynomial of the rigidity circuit consisting of the prism with an additional edge. The prism graph looks as follows

```
1------2
|\    /|
| 5--6 |
|/    \|
4------3
```

and the additional edge is {2,5}.

