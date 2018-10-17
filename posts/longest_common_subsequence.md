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

    function lcs_length( sequence1 , sequence2 , length of sequence 1 , length of sequence 2 ){  
	    if any of the lengths are 0
		    return 0
	    if the characters pointed in the sequences are the same
		    return lcs_length( sequence1 , sequence2 , length of sequence 1 , length of sequence 2 ) + 1
	    else 
		    return max length of the 2 options of the lcs length with either one shortened.
    }  
    
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMDg5NTI0MzMsMjkzNDE4ODI3XX0=
-->