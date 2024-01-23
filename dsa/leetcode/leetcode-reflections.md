# LeetCode Reflections

This Markdown file serves as a personal repository of insights, strategies, and key learnings from my journey through LeetCode problems. For each problem tackled, it documents:

- **Problem Overview**: A brief summary of each LeetCode problem, including its title, difficulty level, and key concepts involved.

- **Solution Approach**: My approach to solving the problem, including initial thoughts, algorithms used, and any specific programming techniques or data structures employed.

- **Challenges & Overcoming Them**: Challenges encountered while solving the problem and how I addressed them. This could include debugging issues, optimizing for time or space complexity, or understanding the problem's intricacies.

- **Key Takeaways**: Crucial lessons learned from each problem, encompassing algorithmic insights, coding best practices, and any new programming concepts discovered or reinforced.

- **Additional Notes**: Any extra observations, such as comparisons to similar problems, alternative solutions explored, and references to helpful resources or discussions.

This file is not just a record of problems solved but a reflection of my growth as a programmer. It's a living document, evolving with each problem I solve and each new insight I gain.

<!--

## Template

### [Name](link)

#### **Problem Overview**:
- **Difficulty**:
- **Key Problem Aspects**:
  - 
- **Edge Cases**:
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

-->

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

### [Flood Fill](https://leetcode.com/problems/flood-fill/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Performing a flood fill on an image represented by an integer grid, starting from a specific pixel.
- **Edge Cases**:
  - The starting pixel already being the new color.
  - Empty image input.
- **Input/Output**:
  - Input: A 2D integer grid `image`, and integers `sr`, `sc`, `new_color`.
  - Output: The modified `image` after performing the flood fill.
- **Data Structures Used**:
  - 2D Array (Grid).
- **Algorithms Used**:
  - Depth-First Search (DFS).
- **Time Complexity**:
  - O(n) - Linear, where n is the number of pixels in the image.
- **Space Complexity**:
  - O(h) - The maximum depth of the recursion stack, where h is the height of the stack.

####  **Solution Approach**:
- Used a recursive depth-first search (DFS) function to update pixels.
- Implemented conditional statements to check boundaries and whether the current pixel matches the original color.
- Handled edge cases such as an empty image and the starting pixel already being the new color.

####  **Challenges & Overcoming Them**:
- Learned to format multi-condition `if` statements in Python for readability.
- Understood how to handle edge cases in a matrix-based problem.

#### **Key Takeaways**:
- The DFS algorithm is effective for problems involving grid traversal and updating connected components.
- Properly handling edge cases is crucial to ensure the correctness of the solution.
- Writing clear and readable conditional statements helps in understanding and debugging the code.

#### **Additional Notes**:
- This problem serves as a practical application of DFS in a grid, demonstrating how to traverse and manipulate 2D arrays.
- The approach and considerations in this problem can be applied to similar matrix or grid-based problems.

### [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Determining if a binary tree is height-balanced, meaning the depths of any two leaf nodes differ by no more than one.
- **Input/Output**:
  - Input: The root of a binary tree (`root`).
  - Output: `True` if the tree is balanced, `False` otherwise.
- **Data Structures Used**:
  - Binary Tree.
- **Algorithms Used**:
  - Depth-First Search (DFS) in a recursive manner.
- **Time Complexity**:
  - O(n) - The algorithm traverses each node once.
- **Space Complexity**:
  - O(h) - The recursion stack can go as deep as the height of the tree.

####  **Solution Approach**:
- Implemented a recursive function `check` that traverses the tree using DFS.
- For each node, the function checks the height and balance of its left and right subtrees.
- Used the `abs()` function to check if the height difference between left and right subtrees exceeds 1, indicating imbalance.
- Employed the `max()` function to determine the height of the current node as the maximum height of its children plus one.

####  **Challenges & Overcoming Them**:
- Understanding the use of DFS in a recursive manner for tree traversal.
- Realizing the importance of returning both the height and balance status at each node for efficient computation.

#### **Key Takeaways**:
- The `abs()` function is crucial in this context for easily determining the absolute difference in height between two subtrees, simplifying the balance check.
- The `max()` function helps in calculating the height of the current node by identifying the taller subtree. The height of a node is based on the height of its tallest child.
- The clever use of returning a tuple (height, balance status) at each step streamlines the process and avoids unnecessary computations.

#### **Additional Notes**:
- This problem is a good example of using recursion to simplify complex tree-based computations.
- It demonstrates the importance of considering each node's properties (height and balance) in relation to its subtree for problem-solving in binary trees.

### [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Detecting if a singly-linked list has a cycle.
- **Input/Output**:
  - Input: The head of a singly-linked list (`head`).
  - Output: `True` if there's a cycle in the list, `False` otherwise.
- **Data Structures Used**:
  - Singly-Linked List.
- **Algorithms Used**:
  - Fast and Slow Pointer Technique.
- **Time Complexity**:
  - O(n) - In the worst case, the fast pointer traverses the entire list.
- **Space Complexity**:
  - O(1) - No additional space is used, pointers only.

####  **Solution Approach**:
- Utilized two pointers, `slow` and `fast`, both initially pointing at the head of the list.
- `slow` moves one step at a time, while `fast` moves two steps.
- The loop continues as long as `fast` and `fast.next` are not null, which prevents null reference errors when accessing `fast.next.next`.
- If `slow` and `fast` meet at any point, it indicates a cycle in the list.

####  **Challenges & Overcoming Them**:
- Understanding the significance of moving `fast` two steps and `slow` one step and how it helps in detecting a cycle.
- Ensuring that the loop condition checks for `fast` and `fast.next` to avoid null reference exceptions.

#### **Key Takeaways**:
- The Fast and Slow Pointer Technique is an efficient way to detect cycles in a linked list.
- Careful consideration of loop conditions is crucial to avoid errors, especially in pointer manipulation problems.

#### **Additional Notes**:
- This problem is a classic example of a pointer algorithm in linked lists and demonstrates an important technique in the detection of cycles.
- The approach is widely applicable in various problems involving linked lists, particularly in cycle detection and related challenges.

### [Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/)

#### **Problem Overview**:
- **Difficulty**: Easy
- **Key Problem Aspects**:
  - Implementing a queue using standard stack operations (push to back, peek/pop from front, size, and is empty).
- **Input/Output**:
  - Various queue operations including `push`, `pop`, `peek`, and `empty`.
- **Data Structures Used**:
  - List in Python (as a stack).
- **Algorithms Used**:
  - Stack-based approach to mimic queue operations.
- **Time Complexity**:
  - Push: O(1) - Appending to a list is a constant time operation.
  - Pop: O(n) - Popping from the front of a list involves shifting all elements, which is O(n).
  - Peek: O(1) - Accessing the first element is constant time.
  - Empty: O(1) - Checking if the list is empty is constant time.
- **Space Complexity**:
  - O(n) - The space complexity is proportional to the number of elements in the queue.

####  **Solution Approach**:
- Implemented a queue using a list, with methods for `push`, `pop`, `peek`, and `empty`.
- The `push` method appends elements to the end of the list.
- The `pop` and `peek` methods operate on the front of the list, returning and accessing the first element, respectively.
- The `empty` method checks if the list (queue) is empty, returning a boolean value.

####  **Challenges & Overcoming Them**:
- Ensuring that the queue operations adhere to the First-In-First-Out (FIFO) principle using only stack operations.
- Efficiently implementing the `pop` operation, which is inherently less efficient in a list used as a stack.

#### **Key Takeaways**:
- The use of the `empty` method in other methods (`pop` and `peek`) to check if the queue is empty before performing operations, which enhances code readability and safety.
- Understanding the trade-offs in implementing a queue with a list, especially in terms of the time complexity of different operations.

#### **Additional Notes**:
- While the list in Python is used as a stack here, it's important to note that the `pop(0)` operation is not efficient for large lists due to the need to shift all elements.
- This implementation serves as a good exercise in understanding the underlying mechanics of different data structures and their operations.
