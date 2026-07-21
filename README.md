# Moglix Online Assignment

## Problem
Given a string `s` containing only the characters `'('` and `')'`, return the length of the **longest valid (well-formed) parentheses substring**.

---

## Language

**Java**

---

## Approach (Stack)

### Intuition

- Use a **stack to store indices** instead of characters.
- Push `-1` initially as a **base index**.
- Traverse the string:
  - If the current character is `'('`, push its index onto the stack.
  - If the current character is `')'`:
    - Pop the top element.
    - If the stack becomes empty, push the current index as the new base.
    - Otherwise, calculate the length of the current valid substring using:
      ```text
      currentIndex - stack.peek()
      ```
    - Update the maximum length.

### Algorithm

1. Initialize a stack and push `-1`.
2. Iterate through the string.
3. For `'('`, push its index.
4. For `')'`:
   - Pop the stack.
   - If the stack becomes empty, push the current index.
   - Otherwise, update the maximum valid length.
5. Return the maximum length.

---

## Time Complexity

- **O(n)**

Each character is pushed and popped from the stack at most once.

---

## Space Complexity

- **O(n)**

The stack may store all indices in the worst case.

---

## Author
Akash Yadav
- **GitHub:** https://github.com/Akash72914
- **LinkedIn:** https://www.linkedin.com/in/akash-ydv
