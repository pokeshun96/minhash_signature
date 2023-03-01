# minhash_signature
This code contains four functions: ‘subsets’, ‘minhash’, ‘jaccard’, 
‘SIG_similarity’. ‘subsets’ function takes two arguments L and density, it creates a subset of integers from 0 to L-1 
with a probability of density for each element, and also creates a binary representation of this subset in which 1 
represents the presence of the element in the subset and 0 represents the absence. ‘minhash’ function takes two 
arguments M and hash_value_list, it creates a matrix SIG with dimensions (number of rows of hash_value_list) by 
(number of columns of M) and fill with infinity. Then it iterates over the first min(number of rows of M, number 
of rows of hash_value_list) rows of both matrices. For each row of M, it checks if an element is equal to 1 and if so, 
it updates the corresponding column of the SIG matrix with the minimum value between the current value and the 
corresponding value of the row of hash_value_list. ‘jaccard’ function takes two arguments a and b, it converts them 
into sets and returns the Jaccard similarity between them which is the length of the intersection of the two sets 
divided by the length of the union of the two sets. ‘SIG_similarity’ function takes three arguments SIG, i, and j, it 
returns the similarity between the ith and jth row of the SIG matrix by calculating the proportion of elements that 
are equal between the two rows.
