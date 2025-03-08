### **1. Data Structures & Algorithms**

1. **Explain the difference between an array and a linked list.**
   - **Array**: A contiguous block of memory that holds a fixed-size collection of elements. Elements can be accessed by their index in constant time (O(1)), but resizing the array can be costly.
   - **Linked List**: A linear data structure where each element (node) contains data and a reference (link) to the next node. It allows efficient insertions and deletions (O(1)) but has O(n) access time due to sequential searching.

2. **What is the time complexity of QuickSort, MergeSort, and Bubble Sort?**
   - **QuickSort**: Average case O(n log n), Worst case O(n^2)
   - **MergeSort**: Always O(n log n)
   - **Bubble Sort**: Worst case O(n^2), Best case O(n) if the list is already sorted.

3. **How does a hash table work, and what are collision resolution techniques?**
   - A hash table uses a hash function to map keys to indices in an array. If two keys map to the same index (a collision), techniques like:
     - **Chaining**: Store multiple elements at the same index in a linked list.
     - **Open Addressing**: Search for the next available slot in the array (linear probing, quadratic probing, etc.)

4. **What is the difference between BFS and DFS?**
   - **BFS (Breadth-First Search)**: Explores all nodes at the present depth level before moving on to nodes at the next depth level. It uses a queue and is useful for finding the shortest path in an unweighted graph.
   - **DFS (Depth-First Search)**: Explores as far down a branch as possible before backtracking. It uses a stack or recursion and is useful for pathfinding and topological sorting.

5. **How would you detect a cycle in a directed graph?**
   - Use **Depth-First Search (DFS)**. While performing DFS, if a node is encountered that is already in the current recursion stack (marked as “in progress”), a cycle is detected.

6. **Can you explain dynamic programming with an example?**
   - Dynamic programming (DP) is an optimization technique for solving problems by breaking them into simpler subproblems and storing the results to avoid redundant calculations.
     Example: Fibonacci Sequence – Instead of recalculating the same Fibonacci number repeatedly, store results in a table.
     
     ```
     fib(n) = fib(n-1) + fib(n-2)
     ```

---

### **2. Database Management Systems (DBMS)**

1. **What are the differences between SQL and NoSQL databases?**
   - **SQL**: Structured data, uses relational tables, and enforces a schema (e.g., MySQL, PostgreSQL).
   - **NoSQL**: Unstructured or semi-structured data, flexible schema, and designed for scalability (e.g., MongoDB, Cassandra).

2. **Explain normalization and denormalization.**
   - **Normalization**: Process of organizing data to minimize redundancy (1NF, 2NF, 3NF).
   - **Denormalization**: Process of intentionally introducing redundancy to optimize read performance.

3. **What is an index in a database? How does it improve performance?**
   - An **index** is a data structure that improves the speed of data retrieval operations on a database. It works like a book's index, allowing the system to quickly find the location of a specific record.

4. **Explain ACID properties in a database transaction.**
   - **Atomicity**: The transaction is fully completed or not executed at all.
   - **Consistency**: The database remains in a valid state before and after the transaction.
   - **Isolation**: Transactions do not interfere with each other.
   - **Durability**: Once committed, the transaction is permanent even if the system crashes.

5. **How does a JOIN operation work? Can you give an example of INNER and LEFT JOIN?**
   - **INNER JOIN**: Returns records that have matching values in both tables.
     Example: `SELECT * FROM customers INNER JOIN orders ON customers.id = orders.customer_id;`
   - **LEFT JOIN**: Returns all records from the left table and matched records from the right table. If no match, NULL is returned.
     Example: `SELECT * FROM customers LEFT JOIN orders ON customers.id = orders.customer_id;`

---

### **3. Operating Systems (OS)**

1. **What is the difference between process and thread?**
   - **Process**: An independent program running in its own memory space.
   - **Thread**: A lightweight process that shares the same memory space with other threads within the same process.

2. **Explain deadlock and how to prevent it.**
   - **Deadlock** occurs when two or more processes are blocked indefinitely, waiting for each other to release resources. Prevention methods include:
     - **Resource allocation graphs**
     - **Lock ordering**
     - **Timeouts**

3. **What are paging and segmentation in memory management?**
   - **Paging**: Divides memory into fixed-size pages, reducing fragmentation.
   - **Segmentation**: Divides memory into variable-sized segments based on logical divisions (e.g., code, data).

4. **What is the role of a scheduler in an operating system?**
   - The **scheduler** manages the execution of processes by assigning CPU time. It determines which process should run next based on scheduling algorithms.

5. **What are system calls, and can you give an example?**
   - **System calls** are the interface between user programs and the kernel. They request services such as file handling, process management, etc.
     Example: `fork()` in UNIX to create a new process.

---

### **4. Computer Networks**

1. **Explain the OSI Model and the functions of each layer.**
   - **Application**: End-user interaction.
   - **Presentation**: Data formatting and encryption.
   - **Session**: Establishment and management of communication sessions.
   - **Transport**: Reliable data transfer (e.g., TCP, UDP).
   - **Network**: Routing and addressing (e.g., IP).
   - **Data Link**: Error detection and correction, framing.
   - **Physical**: Transmission of raw bits over a physical medium.

2. **What is the difference between TCP and UDP?**
   - **TCP**: Connection-oriented, reliable, ensures data is received in order.
   - **UDP**: Connectionless, faster but unreliable, no guarantee of delivery.

3. **How does DNS work?**
   - **DNS** (Domain Name System) translates human-readable domain names (e.g., www.example.com) into IP addresses that computers can understand.

4. **What is the difference between IPv4 and IPv6?**
   - **IPv4**: 32-bit address, 4.3 billion unique addresses.
   - **IPv6**: 128-bit address, allowing for a vast number of unique addresses (3.4×10^38).

5. **What is a subnet mask, and why is it important?**
   - A **subnet mask** determines which portion of an IP address represents the network and which represents the host. It is essential for routing and network segmentation.

---

### **5. Machine Learning & Artificial Intelligence**

1. **Explain the difference between supervised, unsupervised, and reinforcement learning.**
   - **Supervised Learning**: The model is trained with labeled data (e.g., classification).
   - **Unsupervised Learning**: The model finds patterns in unlabeled data (e.g., clustering).
   - **Reinforcement Learning**: The agent learns by interacting with the environment and receiving feedback through rewards or penalties.

2. **What is overfitting in ML? How can you prevent it?**
   - **Overfitting** occurs when a model learns noise and details in the training data, leading to poor generalization. Prevent it by:
     - Using more training data.
     - Applying regularization techniques (L1, L2).
     - Using cross-validation.

3. **What are precision, recall, and F1-score in classification problems?**
   - **Precision**: The proportion of true positive results among all positive predictions.
   - **Recall**: The proportion of true positive results among all actual positives.
   - **F1-score**: The harmonic mean of precision and recall.

4. **Explain the working of a decision tree.**
   - A **decision tree** splits data based on feature values. It creates branches for decisions and leaves for outcomes, using algorithms like ID3 or C4.5 to choose the best feature to split at each node.

5. **What is the difference between CNN and RNN?**
   - **CNN (Convolutional Neural Networks)**: Primarily used for image processing, they focus on spatial hierarchies.
   - **RNN (Recurrent Neural Networks)**: Used for sequential data (e.g., text or time series) and have memory to maintain information over time.

6. **How does backpropagation work in neural networks?**
   - Backpropagation is a process of updating weights in a neural network by propagating the error back through the network, using the gradient descent algorithm to minimize the error.

---

### **6. Programming & Problem-Solving**

1. **Write a Python function to check if a string is a palindrome.**
   ```python
   def is_palindrome(s):
       return s == s[::-1]
   ```

2. **How would you implement a stack using a queue?**
  

### **6. Programming & Problem-Solving**

1. **Write a Python function to check if a string is a palindrome.**

   ```python
   def is_palindrome(s):
       return s == s[::-1]
   
   # Test
   print(is_palindrome("racecar"))  # True
   print(is_palindrome("hello"))    # False
   ```

2. **How would you implement a stack using a queue?**
   - A stack follows Last In First Out (LIFO) principle, and a queue follows First In First Out (FIFO).
   - We can implement a stack using two queues:
   
   ```python
   from collections import deque

   class StackUsingQueues:
       def __init__(self):
           self.queue1 = deque()
           self.queue2 = deque()

       def push(self, x):
           self.queue1.append(x)

       def pop(self):
           if len(self.queue1) == 0:
               return None
           # Move all elements except the last to queue2
           while len(self.queue1) > 1:
               self.queue2.append(self.queue1.popleft())
           # Pop the last element
           top = self.queue1.popleft()
           # Swap queues
           self.queue1, self.queue2 = self.queue2, self.queue1
           return top

   # Test
   stack = StackUsingQueues()
   stack.push(1)
   stack.push(2)
   print(stack.pop())  # 2
   print(stack.pop())  # 1
   ```

3. **What are lambda functions in Python?**
   - **Lambda functions** are small anonymous functions defined using the `lambda` keyword. They can have any number of arguments but only one expression.
   
   Example:
   ```python
   square = lambda x: x ** 2
   print(square(4))  # 16
   ```

4. **Explain object-oriented programming concepts (OOP): Inheritance, Polymorphism, Encapsulation.**
   - **Inheritance**: The ability of a class to inherit properties and methods from another class. It promotes code reusability.
     Example: A `Dog` class can inherit from an `Animal` class.
   - **Polymorphism**: The ability of different classes to implement methods in their own way while sharing the same name. It allows the same method to behave differently based on the object calling it.
     Example: A `Dog` and a `Cat` class both have a `speak()` method, but each class defines it differently.
   - **Encapsulation**: The bundling of data (attributes) and methods that operate on that data into a single unit (class). It also hides the internal state and requires all interactions to be performed through methods.
     Example: Using getter and setter methods to access private attributes.

5. **What are RESTful APIs, and how do they work?**
   - **RESTful APIs** (Representational State Transfer) are a set of rules for creating web services. They allow different applications to communicate with each other over HTTP by using standard HTTP methods like `GET`, `POST`, `PUT`, `DELETE`.
   - RESTful APIs are stateless, meaning each request from a client must contain all the information needed to understand the request. They use URLs to specify resources (e.g., `/users/123`) and usually respond in formats like JSON or XML.
   
   Example:
   - **GET**: Fetch data (e.g., retrieve user details).
   - **POST**: Submit data (e.g., create a new user).
   - **PUT**: Update existing data.
   - **DELETE**: Remove data.

---

### **7. Probability & Statistics**

1. **What is the difference between mean, median, and mode?**
   - **Mean**: The average of a set of numbers, calculated as the sum of all values divided by the number of values.
   - **Median**: The middle value when the data is ordered. If the number of values is even, the median is the average of the two middle values.
   - **Mode**: The value that appears most frequently in the data set.

2. **Explain Bayes' Theorem with an example.**
   - Bayes' Theorem describes the probability of an event, based on prior knowledge of conditions related to the event.
   
   Formula:
   \[
   P(A|B) = \frac{P(B|A)P(A)}{P(B)}
   \]
   Where:
   - \(P(A|B)\) is the probability of event A given event B.
   - \(P(B|A)\) is the probability of event B given event A.
   - \(P(A)\) is the probability of event A.
   - \(P(B)\) is the probability of event B.
   
   **Example**: If 1% of people have a certain disease, and a test for the disease is 99% accurate, what’s the probability that someone with a positive test result actually has the disease?
   Use Bayes' Theorem to calculate the probability, considering both true positives and false positives.

3. **What is the Central Limit Theorem?**
   - The **Central Limit Theorem (CLT)** states that the distribution of the sample mean will tend to be normal (Gaussian), regardless of the shape of the original population distribution, as long as the sample size is large enough (typically n > 30).
   - This theorem is important because it allows us to make inferences about population parameters even when the underlying distribution is not normal.

4. **How would you evaluate the performance of a machine learning model?**
   - **Accuracy**: Percentage of correct predictions.
   - **Precision**: Proportion of true positive predictions to the total predicted positives.
   - **Recall**: Proportion of true positive predictions to the total actual positives.
   - **F1-score**: Harmonic mean of precision and recall.
   - **Confusion Matrix**: A table showing the actual vs predicted values, including True Positives (TP), True Negatives (TN), False Positives (FP), and False Negatives (FN).
   - **ROC Curve and AUC**: For classification problems, the Receiver Operating Characteristic curve and its area under the curve (AUC) can evaluate model performance.

---

Let me know if you need further clarification on any of these answers!
