The problem was taken from here [http://www.techiedelight.com/longest-common-subsequence/](http://www.techiedelight.com/longest-common-subsequence/)

The problem is stated as thus:  

    The longest common subsequence (LCS) problem is the problem of finding the  
    longest subsequence that is present in given two sequences in the same order.  
    i.e. find a longest sequence which can be obtained from the first original  
    sequence by deleting some items, and from the second original sequence by  
    deleting other items.

This is a dynamic problem. The conditions of optimal substructure and overlapping sub-problems are both satisfied as thus:
1. Optimal substructure: This can be thought of as a graph with problems being broken down into finding the longest common strings by shortening the string length.
2. Overlapping sub-problems: The recurring problem is to return the the length of sequence when both the strings are identical.     
```
    function lcs_length( sequence1 , sequence2 , sequence_1_pointer , sequence_2_pointer ){  
	    if sequence_1_pointer==0 OR sequence_2_pointer==0
		    return 0
	    if 
		    return lcs_length( sequence1 , sequence2 , sequence_1_pointer -1 , sequence_2_pointer -1 ) + 1
	    else 
		    return maximum( lcs_length( sequence1 , sequence2 ,  , sequence_1_pointer , sequence_2_pointer -1 ) ,  lcs_length( sequence1 , sequence2 ,  , sequence_1_pointer-1 , sequence_2_pointer ) )
    }  

    print lcs_length( string1 , string2 , length_string_1 , length_string_2 )
 ```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0ODA0MTc4NDAsLTk5MDE5ODgxNSwyOT
M0MTg4MjddfQ==
-->