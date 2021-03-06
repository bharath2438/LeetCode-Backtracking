# LeetCode-Backtracking

## Problem Set

[ProblemSet](https://seanprashad.com/leetcode-patterns/)

### Word Search 
[Problem](https://leetcode.com/problems/word-search/)
* Initially, find the letter on the board which corresponds to the given 1st letter of the word.
* From this letter, explore in the 4 different directions and try to find the remaining letters of the word recursively.
* If you reach the end of the word, return True...you have found a match
* If you have tried exploring all directions and cannot find the matching word, return False.
* If no letter starting with the first letter of the word yields a match, return False finally.

### Letter Case Permutation
[Problem](https://leetcode.com/problems/letter-case-permutation/)
* Start with an empty string
* Next, start adding characters one by one recursively to this string.
* If the character is not an alphabet, just add it to the string, else branch out into normal case and swapped version
* Finally, if a permutation equal in length to the original string is found, add it to the result

### Subsets
[Problem](https://leetcode.com/problems/subsets/)
* Start with an empty subset
* Branch into two permutations - one with the element at the current index, and the other without.
* Return if the current index exceeds the limit of the given list after adding the subset to the result

### Subsets 2
[Problem](https://leetcode.com/problems/subsets-ii/)
* Start with empty subset
* The idea is to branch into two permutations - one with the element at the current index and the other without, but in the latter, children cannot include the element at the current index.
* In order to achieve this, we sort he initial list and then loop till a new element is found and carry out expansion of the second branch, recursively.
* When starting index passes the length of the given list, add the combination to the result.

### Permutations
[Problem](https://leetcode.com/problems/permutations/)
* Start with empty combination
* Maintain a list called rest. Rest contains all elements other than the current element.
* Add the current element into the combination and recursively try to find the permutations for the rest of the of the elements.
* Stop when the rest list is empty and add the combination to the result.

### Permutations 2
[Problem](https://leetcode.com/problems/permutations-ii/)
* Start with empty combination
* Sort the given list, to eliminate duplicates.
* Follow the same procedure as permutation 1, except that carry out backtracking only for distinct elements.
* This is done by checking if an element is equal to its predecessor.

### Combinations
[Problem](https://leetcode.com/problems/combinations/)
* Start with empty combination
* Add each possible element (every element to the right of the current) to the combination and backtrack recursively
* Terminate when the length of the combination is equal to k.
* Add the combination to the list before termination

### Combination Sum
[Problem](https://leetcode.com/problems/combination-sum/)
* Start with empty combination
* Branch into a two way decision tree - one with the element at the current index and the other without.
* Add up the numbers and compare with target; if equal, add to result, if greater or end of candidates is reached, return.

### Combination Sum 2
[Problem](https://leetcode.com/problems/combination-sum-ii/)
* Start with empty combination
* Sort the list since duplicate combinations are not allowed
* Branch into a two way decision tree - one with the current element and the other without (for the without part, keep moving forward until you find the next element)
* Add the combination to the result when the total is reached.
* Return when the total exceeds the target or the current position crosses the size of candidates.

### Combination Sum 3
[Problem](https://leetcode.com/problems/combination-sum-iii/)
* Start with empty combination
* Branch into two branches - one with the current and element and the other without the current element.
* If a combination has size k and adds up to the given number, add it to the result
* If the size of the combination exceeds k or the sum is greater than the target, terminate

### Generate parantheses 
[Problem](https://leetcode.com/problems/generate-parentheses/)
* Start with empty combination
* Branch into two - one with "(" and the other with ")"
* Assign scores for addition - +1 for "(" and -1 for ")". Your scores should always be within the range 0 <= score <= n
* Add combination to result and terminate if score is out of the boundaries of the given range.

### Palindrome partition
[Problem](https://leetcode.com/problems/palindrome-partitioning/)
* Start with empty combination
* Loop through each index in the string and partition the string.
* If the left portion is a palindrome, add it to the combination and bactrack for the right portion.
* Add the combination to the result if the index has reached the end of the string.

### Phone number
[Problem](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
* Create a dictionary matching the the numbers to their corresponding strings
* The variable start loops through the given digits string.
* Create n branches, where n is the number of letters associated with the number at start.
* Add each value to the combination, and backtrack.
* Add the combination to the result when the length of digits is reached.

### Sudoku solver
[Problem](https://leetcode.com/problems/sudoku-solver/)
* Create a check valid function to return true if a number is valid in a certain position and return false otherwise based on standard sudoku rules.
* Try to find the solution after placing a value at a certain position. If not possible, backtrack....

### N Queens
[Problem](https://leetcode.com/problems/n-queens/)
* We store only the column numbers of the positions where the Queen is placed.
* To check for diagonals, always one diagonal will have constant r+c value and the other will have constant r-c value.
* Maintain two sets which keep track of these invalid diagonals.
* Backtrack by placing queen in certain row, note down the column, diagonal values. Move on to the next row.
* Convert the list data into string data and add to result.



