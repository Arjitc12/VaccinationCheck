# VaccinationCheck
To check if the user is already existing in database, using Bloom Filter Technique.

The simplest and most well-known data structure that solves the membership problem is the Bloom filter which was proposed by Burton Howard Bloom in 1970. It is a space-efficient probabilistic data structure for representing a dataset D = {x1, x2, . . . , xn } of n elements that supports only two operations:

1. Adding an element into the set, and
2. Testing whether an element is or is not a member of the set.

The Bloom filter can store a large set very efficiently by discarding the identity of the elements; it stores only an (almost) unique set of bits corresponding to some number of hash functions that are applied to the element by the algorithm.

Practically, the Bloom filter is represented by a bit array and can be k described by its length m and number of different hash functions {hi}i=1.
It is assumed that m is proportional to the number of expected elements n, while k is much smaller than m. Hash functions hi should be independent and uniformly distributed. 

In this way, we randomize the hash values uniformly (you can think of it as using hash functions as some kind of random-number generator) in the filter and decrease the probability of hash collisions.

Such an approach drastically reduces the storage space and, regardless of the number of elements in the data structure and their size, requires a constant number of bits by reserving a few bits per element.
