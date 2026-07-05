# Lesson 1: Time Complexity & Big O Notation

**What is Time Complexity?**

- Time Complexity is a way to measure how the amount of work performed by an algorithm grows as the input size increases.
- It does **not** measure the actual execution time in seconds.
- Different computers have different processors and speeds, so instead of measuring time, we measure the number of operations an algorithm performs.

## What is Big O Notation?

- Big O Notation is a mathematical way to describe the growth rate of an algorithm.
- It tells us how the work performed by an algorithm increases as the input size (n) becomes
  very large.
- Big O focuses on the **growth pattern**, not the exact number of operations.

## Why Do We Study Time Complexity?

- When solving a problem, there can be multiple correct solutions.
  Example:
  . Algorithm A performs 100 operations.
  . Algorithm B performs 10,000 operations.
  . Both produce the correct answer, but Algorithm A is more efficient.
  . Time Complexity helps us compare algorithms based on efficiency..

# O(1) - Constant Time

- The amount of work remains constant regardless of the input size.
- Whether the input contains:
  . 10 elements
  . 100 elements
  . 1,000,000 elements
- The algorithm still performs the same amount of work.
- Example:
  . java
  . int first = arr[0];
  . Explanation:
  . Accessing the first element always requires only one operation.
  . Time Complexity: O(1)

## O(n) - Linear Time

- The amount of work increases linearly with the size of the input.
- If the input doubles, the work approximately doubles.
- Example:
  for(int i = 0; i < n; i++){
  System.out.println(arr[i]);
  }
- Explanation:
  . The loop executes once for every element.
- If there are:
  . 10 elements → 10 iterations
  . 100 elements → 100 iterations
  . 1000 elements → 1000 iterations
  . Time Complexity: O(n)

## O(n²) - Quadratic Time

- The amount of work grows as the square of the input size.
- Usually occurs when one loop is nested inside another.
- Example:
  for(int i = 0; i < n; i++){
  for(int j = 0; j < n; j++){
  System.out.println(i + " " + j);
  }
  }
- Explanation:
  . Outer Loop → n times
  . Inner Loop → n times
  . Total Work: n × n
- Time Complexity: O(n²)

## Why Do We Ignore Constants?

- Example: O(2n), O(10n), O(100n)
- These algorithms perform different numbers of operations.
- However, they all grow linearly.
- Big O measures the growth pattern of an algorithm, not the exact number of operations.
- Therefore,
  O(2n) -> O(n)
  O(100n) -> O(n)
- Rule: Ignore constant factors because they do not change the growth pattern.

## Why Do We Ignore Smaller Terms?

- **Example:** O(n² + n)
- As the input size becomes very large,
- n² grows much faster than n.
  **Example:**
  n = 1000
  n² = 1,000,000
  n = 1,000
- The contribution of n becomes very small compared to n².
- Therefore,
  O(n² + n) -> O(n²)
- Rule: Always keep the fastest-growing term.

## O(log n)

- The input size is reduced by half in every step.
- Instead of checking every element,
- the algorithm repeatedly removes half of the remaining search space.
  . Example: 16 -> 8 -> 4 -> 2 -> 1
- This requires only 4 steps.
- Rule:
  . Whenever an algorithm eliminates half of the remaining data in every step,
  . its complexity is usually O(log n).

## Important Big O Rules

**Rule 1**

- Big O measures the growth of work, not the execution time.

**Rule 2**

- Ignore constant factors.
- Example:
  O(5n) -> O(n)

**Rule 3**

- Ignore smaller-growing terms.
- Example: O(n² + n) -> O(n²)

**Rule 4**

- Sequential loops → Add
  n + n -> O(n)

**Rule 5**

- Nested loops → Multiply
  n × n -> O(n²)

**Rule 6**

- If the problem size is reduced by half in every step,
- the complexity is generally O(log n).

Interview Tip

## Whenever you calculate Time Complexity, ask yourself:

- How many times does the loop execute?
- Are the loops sequential or nested?
- Is the input reduced by half in every step?
- Which term grows the fastest?
- Ignore constants and smaller terms.

## Summary

- O(1) -> Constant amount of work.
- O(n) -> Work grows linearly.
- O(n²) -> Nested loops.
- Work grows quadratically -> O(log n)
- Input is divided by 2 in every step.

## Key Takeaways

• Big O measures growth, not exact execution time.
• Ignore constants.
• Ignore smaller terms.
• Sequential loops → Add.
• Nested loops → Multiply.
• Dividing the input by half repeatedly usually indicates O(log n).
• Always analyze how the work grows as the input size increases.
