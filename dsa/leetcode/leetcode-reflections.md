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
