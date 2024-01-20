# LeetCode Reflections

This Markdown file serves as a personal repository of insights, strategies, and key learnings from my journey through LeetCode problems. For each problem tackled, it documents:

- **Problem Overview**: A brief summary of each LeetCode problem, including its title, difficulty level, and key concepts involved.

- **Solution Approach**: My approach to solving the problem, including initial thoughts, algorithms used, and any specific programming techniques or data structures employed.

- **Challenges & Overcoming Them**: Challenges encountered while solving the problem and how I addressed them. This could include debugging issues, optimizing for time or space complexity, or understanding the problem's intricacies.

- **Key Takeaways**: Crucial lessons learned from each problem, encompassing algorithmic insights, coding best practices, and any new programming concepts discovered or reinforced.

- **Additional Notes**: Any extra observations, such as comparisons to similar problems, alternative solutions explored, and references to helpful resources or discussions.

This file is not just a record of problems solved but a reflection of my growth as a programmer. It's a living document, evolving with each problem I solve and each new insight I gain.

## Template

### [Name](link)

#### **Problem Overview**:
- **Difficulty**:
- **Key Problem Aspects**:
  - 
- **Input/Output**:
  - 
- **Data Structures Used**:
  - 
- **Algorithms Used**:
  - 
- **Time Complexity**:
  - 
- **Space Complexity**:
  - 

####  **Solution Approach**:
- 

####  **Challenges & Overcoming Them**:
- 

#### **Key Takeaways**:
- 

#### **Additional Notes**:
- 

## Grind 75

### [Two Sum](https://leetcode.com/problems/two-sum/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Finding two numbers in an array that sum up to a specific target.
  - Returning the indices of the two numbers.
  - Ensuring the solution has exactly one result and does not use the same element twice.
  - Involves array manipulation and efficient searching techniques.
- **Input/Output**:
  - Input: An array of integers (`nums`), and a target integer (`target`).
  - Output: An array of two integers, representing the indices of the two numbers that add up to the target.
- **Data Structures Used**:
  - Hash table (to store numbers and their indices from the array).
- **Algorithms Used**:
  - One-pass Hash Table (to check for the complement of each number and store numbers in the hash table simultaneously).
- **Time Complexity**:
  - O(n) - The list is traversed only once, and each look-up in the hash table costs O(1) time.
- **Space Complexity**:
  - O(n) - Extra space is required for the hash table, which in the worst case needs to store all elements from the array.

####  **Solution Approach**:
- Utilized a hash table (dictionary in Python) to store and quickly access the numbers encountered in the array.
- Iterated through the array using a `for` loop with `enumerate`, which provides both the index and the value of each item in the array.
- For each number, calculated its complement (target - current number) and checked if this complement already exists in the hash table.
- If the complement was found, returned the indices of the current number and its complement as the solution.
- Otherwise, stored the current number with its index in the hash table for future reference.

####  **Challenges & Overcoming Them**:
- Ensuring efficient lookup to find if the complement of a number exists in the array.
- Overcame this by using a hash table for O(1) lookup time, significantly reducing the overall time complexity.

#### **Key Takeaways**:
- The `enumerate` function in Python is extremely useful for looping through items in a list while having access to both the item and its index.
- Using a hash table to store and access data can greatly optimize the solution, especially for problems involving pair finding or complement checks.
- Always consider the trade-off between time and space complexity. Here, using extra space for the hash table improved time efficiency.

#### **Additional Notes**:
- This approach highlights the importance of choosing the right data structure for the problem at hand.
- It also demonstrates a common pattern in solving array-related problems where you need to find pairs that satisfy certain conditions.

### [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Validating if an input string containing only '(', ')', '{', '}', '[' and ']' is properly closed and nested.
- **Input/Output**:
  - Input: A string `s` containing just the characters '(', ')', '{', '}', '[' and ']'.
  - Output: A boolean, `True` if the input string is valid, otherwise `False`.
- **Data Structures Used**:
  - Stack (implemented using a list in Python).
  - Dictionary for mapping closing to opening symbols.
- **Algorithms Used**:
  - Stack-based validation for matching pairs of parentheses.
- **Time Complexity**:
  - O(n) - Linear, as each character is visited once.
- **Space Complexity**:
  - O(n) - Linear, in the worst case, all opening brackets are stored in the stack.

####  **Solution Approach**:
- Used a dictionary (`closing_symbols`) to map each closing symbol to its corresponding opening symbol. 
- Iterated through each character in the string, using a stack (`opening_symbols`) to keep track of the opening symbols.
- For each closing symbol encountered, checked if the stack is not empty and if the top of the stack matches the corresponding opening symbol. If not, returned `False`.
- Returned `True` if the stack is empty at the end, indicating all symbols have been properly closed.

####  **Challenges & Overcoming Them**:
- Ensuring that each closing symbol correctly matches the most recent opening symbol. This was effectively handled using a stack.

#### **Key Takeaways**:
- The use of `dict()` instead of `{}` for creating the `closing_symbols` dictionary. While both create a dictionary, using `dict()` can be clearer, especially for beginners or in situations where readability is paramount. It also allows for dynamic creation of dictionaries from sequences of key-value pairs.
- Effective use of key-value pairs in the dictionary to map closing symbols to their corresponding opening symbols, demonstrating an understanding of how to leverage Python's data structures to solve specific problems.

#### **Additional Notes**:
- This solution is a classic example of the stack data structure being used to solve problems related to sequence processing and validation.
- The approach can be extended or modified for similar problems involving nested structures or sequence validation.

### [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Merging two sorted linked lists into one sorted linked list.
- **Input/Output**:
  - Input: Two sorted linked lists (`list1` and `list2`).
  - Output: A single sorted linked list.
- **Data Structures Used**:
  - Linked Lists.
- **Algorithms Used**:
  - Two-pointer technique.
- **Time Complexity**:
  - O(n + m) - Linear, iterating through each element of both lists.
- **Space Complexity**:
  - O(1) - No additional space proportional to the input size is used.

####  **Solution Approach**:
- Utilized a sentinel (dummy) node to simplify the merging process and manage edge cases.
- Employed a two-pointer approach, moving through both lists and appending the smaller value node to the merged list.
- Handled the remaining elements in one of the lists after one list is fully traversed.

####  **Challenges & Overcoming Them**:
- Initial challenge with the terminating condition of the loop. Resolved by changing the condition from `and` to `or` to correctly handle the scenario when one list is longer than the other.
- Incorrectly returning the opposite list when one of the input lists was empty. Corrected by returning the non-null list in such cases.

#### **Key Takeaways**:
- Understanding the importance of the loop's terminating condition in linked list manipulation.
- The effectiveness of using a sentinel node in linked list problems to simplify edge case handling and make the code more readable.
- Realizing the significance of carefully handling edge cases in algorithms, especially in data structure manipulations.

#### **Additional Notes**:
- This problem was a good example of the practical use of two-pointer technique in linked lists.
- The experience highlights how small mistakes in logic, like the loop condition and return statements, can significantly impact the algorithm's correctness.

### [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Finding the maximum profit that can be made by buying and selling a stock on different days.
- **Input/Output**:
  - Input: An array `prices` where `prices[i]` is the price of a given stock on the `i`th day.
  - Output: The maximum profit that can be achieved.
- **Data Structures Used**:
  - None beyond basic variables.
- **Algorithms Used**:
  - Single pass linear scan.
- **Time Complexity**:
  - O(n) - Linear, iterating through the array once.
- **Space Complexity**:
  - O(1) - Constant, using a fixed number of variables.

####  **Solution Approach**:
- Utilized `float("inf")` to initialize the lowest price to the highest possible value at the start.
- Iterated over the price list, updating the lowest price when a lower price was found.
- Calculated the maximum profit using `max()` function at each step by comparing the current profit with the difference between the current price and the lowest price found.

####  **Challenges & Overcoming Them**:
- Recognized the need to remove the unnecessary variable `highest_price`. Realized that once a new low price is found, the previous high price becomes irrelevant.

#### **Key Takeaways**:
- The use of `float("inf")` is helpful in initializing variables to a very high value for minimization problems.
- The `max()` function in Python is efficient for comparing and updating the maximum value during iterations.
- Simplifying the solution by removing redundant variables can make the code more efficient and easier to understand.

#### **Additional Notes**:
- This problem is a classic example of finding the maximum difference in an array, demonstrating the importance of single pass solutions and efficient variable usage.
- The approach underscores the value of understanding problem constraints to optimize variable initialization and update logic.

### [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Determining if a string is a palindrome after converting all uppercase letters to lowercase and removing non-alphanumeric characters.
- **Input/Output**:
  - Input: A string `s`.
  - Output: `True` if `s` is a palindrome, `False` otherwise.
- **Data Structures Used**:
  - String manipulation.
- **Algorithms Used**:
  - String filtering and comparison.
- **Time Complexity**:
  - O(n) - Linear, where n is the length of the string.
- **Space Complexity**:
  - O(n) - Linear, for storing the filtered and normalized string.

####  **Solution Approach**:
- Created a new string `new_string` to store the alphanumeric, lowercase version of the input string.
- Used `isalnum()` to filter out non-alphanumeric characters and `lower()` to convert characters to lowercase.
- Compared each character of the first half of `new_string` with its corresponding character in the second half.

####  **Challenges & Overcoming Them**:
- Initially used the wrong string (`s` instead of `new_string`) in the comparison loop.
- Corrected an off-by-one error in the comparison loop by adjusting the index in `new_string[-i - 1]`.
- Discovered an alternate method using string slicing `[::-1]` and `join` function for a more concise solution.

#### **Key Takeaways**:
- The `lower()` and `isalnum()` functions are efficient for normalizing strings in Python.
- Recognized the importance of accurately indexing when comparing characters in a palindrome.
- Learned a new method of reversing a string using slicing `[::-1]`, and constructing strings efficiently with `join`, which are valuable techniques for future string manipulation problems.

#### **Additional Notes**:
- The second method using `[::-1]` for string reversal is more Pythonic and succinct, showing the power of Python's string slicing capabilities.
- The use of `join` with a generator expression for creating a normalized string is an elegant and efficient approach.
- This problem illustrates the importance of attention to detail in string processing and the usefulness of Python's built-in string methods.

### [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Inverting a binary tree so that the left and right children of all nodes are swapped.
- **Input/Output**:
  - Input: The root of a binary tree (`root`).
  - Output: The root of the inverted binary tree.
- **Data Structures Used**:
  - Binary Tree.
- **Algorithms Used**:
  - Tree Traversal, Recursion.
- **Time Complexity**:
  - O(n) - Each node in the tree is visited once, where n is the number of nodes.
- **Space Complexity**:
  - O(h) - Recursion stack space, where h is the height of the tree.

####  **Solution Approach**:
- Implemented a recursive function to invert the tree.
- Checked if the current node is not `None`. If not, swapped the left and right children of the node.
- Recursively called the function on the left and right children of the current node.

####  **Challenges & Overcoming Them**:
- Initially used a `while` loop instead of an `if` statement, which was incorrect for the recursive approach.
- Corrected the approach to apply recursion, calling the `invertTree` method on each child node.

#### **Key Takeaways**:
- Understanding that recursion is suitable for tree problems, as it naturally follows the tree's structure.
- Recognizing the difference between using a `while` loop and an `if` statement in the context of recursion.
- Time Complexity (O(n)): The function visits each node exactly once, hence the linear time complexity. In a tree traversal, the number of recursive calls is equal to the number of nodes.
- Space Complexity (O(h)): The space complexity is determined by the height of the tree due to the recursion stack. In the worst case (a skewed tree), the recursion can go as deep as the tree's height.

#### **Additional Notes**:
- This problem is a fundamental example of understanding recursion in tree data structures.
- The solution illustrates how a simple action (swapping left and right children) at each step can lead to a significant transformation of the entire tree structure.

### [Valid Anagram](https://leetcode.com/problems/valid-anagram/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Checking whether two strings are anagrams of each other.
- **Input/Output**:
  - Input: Two strings `s` and `t`.
  - Output: `True` if `t` is an anagram of `s`, and `False` otherwise.
- **Data Structures Used**:
  - Dictionary (hash table).
- **Algorithms Used**:
  - Frequency counting.
- **Time Complexity**:
  - O(n + m) - Linear, where `n` is the length of string `s` and `m` is the length of string `t`.
- **Space Complexity**:
  - O(n) - Linear, or O(1) if considering the character set as fixed (e.g., ASCII).

####  **Solution Approach**:
- Created a dictionary `letter_dict` to count the frequency of each character in `s`.
- Iterated through `t`, decreasing the count of each character in `letter_dict`. Returned `False` if a character was not found or its count was zero.
- Checked if all counts in `letter_dict` were zero, which is necessary to confirm an anagram.

####  **Challenges & Overcoming Them**:
- Discovered that the order of conditions in `if letter_dict[letter] > 0 and letter in letter_dict` can lead to an error because the key might not exist in the dictionary. Learned that reversing the order to `if letter in letter_dict and letter_dict[letter] > 0` avoids this issue by ensuring the key exists before accessing its value.

#### **Key Takeaways**:
- The importance of considering the order of conditions in a logical statement to avoid key errors in dictionaries.
- The necessity of a final check to ensure all character counts return to zero, which is crucial for validating anagrams.
- The application of hash tables (dictionaries in Python) for efficient frequency counting in strings.

#### **Additional Notes**:
- This solution demonstrates a fundamental technique in string manipulation and comparison - frequency counting using hash tables.
- It also highlights a typical use case where space complexity can be considered constant due to a limited character set, despite technically being O(n).

### [Binary Search](https://leetcode.com/problems/binary-search/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Implementing binary search to find a target value within a sorted array.
- **Input/Output**:
  - Input: A sorted array `nums` and a target value `target`.
  - Output: The index of `target` in `nums`, or `-1` if `target` is not found.
- **Data Structures Used**:
  - Array.
- **Algorithms Used**:
  - Binary Search.
- **Time Complexity**:
  - O(log(n)) - Logarithmic, as the search space is halved with each step.
- **Space Complexity**:
  - O(1) - Constant, as no extra space is used proportional to the input size.

####  **Solution Approach**:
- Used `left` and `right` pointers to maintain the current search space, improving clarity over using variables like `i` and `j`.
- Calculated the midpoint `mid` as `(left + right) // 2` to determine the current element to compare with the target.
- Used a `while left <= right:` loop, ensuring that the element at the current `mid` is also checked.
- Incremented `left` to `mid + 1` and decremented `right` to `mid - 1` when adjusting the search space to prevent infinite loops.

####  **Challenges & Overcoming Them**:
- Initially failed to update `left` and `right` correctly, leading to incorrect results. Fixed by properly incrementing/decrementing the `mid` index.
- Learned about an alternative midpoint calculation method to prevent integer overflow: `mid = left + (right - left) // 2`.

#### **Key Takeaways**:
- The importance of using clear and descriptive variable names like `left`, `right`, and `mid` in binary search algorithms.
- Understanding why `while left <= right:` is preferable, as it includes the scenario where the target is at the current midpoint.
- The alternative method to calculate `mid` is particularly relevant in languages with limited integer range, preventing overflow by adding half of the interval to the lower bound.

#### **Additional Notes**:
- This problem reinforces the fundamental concept of binary search and its efficiency in searching sorted arrays.
- It also highlights common pitfalls in implementing binary search, such as proper updating of search boundaries and choosing the right loop condition.
