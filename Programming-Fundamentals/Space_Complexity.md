## What is Space Complexity?

- Before learning the definition, think about this.
- Suppose you write two Java programs.

- **Program A**
  .int sum = a + b;
- Memory Used:
  . Variable a
  . Variable b
  . Variable sum

- **Program B**
  int[] arr = new int[1000000];
- Memory Used:
  . Array of 1,000,000 integers
- Obviously,
  . Program B uses much more memory.
- That memory consumption is measured using Space Complexity.

- **Definition**
  . Space Complexity is the amount of memory an algorithm requires to  
   execute as the input size grows.
  . Just like Time Complexity measures execution time,
  . Space Complexity measures memory usage.

Example 2
int[] arr = new int[n];
. If -> n = 10, Memory: 10 integers
. If -> n = 100, Memory: 100 integers
. If -> n = 1,000,000, Memory: 1,000,000 integers

- The memory increases as n increases.
- Therefore, Space Complexity = O(n)
