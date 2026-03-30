# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**
Multithreading is a fundamental concept in operating systems that allows multiple tasks to execute concurrently within a single process. Through this assignment, I learned how threads are created using the Runnable interface and executed using the start() method. I also understood how threads transition between different states such as New, Runnable, Running, Waiting, and Terminated.

One of the most important concepts I learned is how Round-Robin scheduling distributes CPU time fairly among processes. The use of Thread.sleep() helped simulate real execution delays, while Thread.join() ensured proper synchronization between threads. I also realized how lightweight threads are compared to processes, making them efficient for simulations like this one. Overall, this assignment improved my understanding of concurrency and CPU scheduling in a practical way.

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**The most challenging part of this assignment was understanding how the scheduler manages multiple threads using the Round-Robin algorithm. At first, it was difficult to track how processes move between execution and the ready queue. Additionally, implementing new features such as priority and waiting time required modifying the existing code without breaking its functionality.

Another challenge was ensuring that all threads executed correctly while maintaining synchronization using join(). Understanding how context switching works internally also required careful analysis of the code. This challenge is directly related to process scheduling concepts discussed in Chapter 2 of the textbook.

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**To overcome these challenges, I carefully analyzed the provided starter code and broke it down into smaller parts. I focused on understanding each method, especially the run() method and the scheduler loop. I also used debugging techniques such as printing intermediate outputs to track process behavior.

Reading the textbook and revisiting lecture slides helped me understand key concepts like scheduling and thread lifecycle. Additionally, testing the program after each modification ensured that errors were identified early. This step-by-step approach made it easier to implement features correctly.

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**Multithreading concepts are widely used in real-world applications such as web browsers, operating systems, and mobile applications. For example, web browsers use multiple threads to load web pages, handle user input, and run scripts simultaneously. This improves performance and user experience.

Similarly, mobile apps use threads to perform background tasks such as downloading data while keeping the user interface responsive. In this assignment, the use of threads to simulate CPU scheduling reflects how operating systems manage multiple processes efficiently. This shows how theoretical concepts can be applied to real-world systems.

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

consider myself at an intermediate level in multithreading. I understand the basic concepts such as thread creation, scheduling, and lifecycle. However, I still need more practice with advanced topics like synchronization and concurrency issues.

### Feedback on the assignment This assignment was very helpful in understanding how theoretical concepts are applied in real systems. It was slightly challenging but provided valuable hands-on experience. I would recommend adding more examples related to real-world applications.

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
