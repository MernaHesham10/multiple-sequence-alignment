# multiple-sequence-alignment
### Introduction
- It's Global Alignment Algorithm
- This module uses dynamic programming to find the optimal alignment of multiple sequences/ strings of similar length.
- Its the optimized version of the algorithm.

### Model
- In this model there's 3 function:
	- calculate_scorematrix():
		- It creates a scorematrix with help of the substitution matrix and rewards/ penalties
    		- Args:
        		score_matrix (np matrix): substitution matrix inside initialized matrix
        		ls1 (int): len first sequence to alignt
        		ls2 (int): len second sequence to alignt
        		ls3 (int): len third sequence to alignt

    		- Returns:numpy matrix: scorematrix
		
        - traceback():
		- traceback from bottom right corner to upper left corner. Finds best scoring path via greedy-algorithm.

    		- Args:
        		score_matrix numpy matrix: scorematrix
        		ls1 (int): len first sequence to alignt
        		ls2 (int): len second sequence to alignt
        		seq1 (str): first sequence to alignt
        		seq2 (str): second sequence to alignt

    		- Returns:
 			seq1_new (str): redesigned first sequence
        		seq2_new (str): redesigned second sequence

 	- output():
		- generates and prints an alignment output string which shows matches (|) and mismatches (*)

    		- Args:
        		seq1_new (str): redesigned first sequence
        		seq2_new (str): redesigned second sequence

    		- Returns:
 			str: alignment output string which consists of "|" and "*" symbols
