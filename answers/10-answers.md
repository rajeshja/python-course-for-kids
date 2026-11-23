# Answer Key: Session 10: Fractals and Recursion

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

The base case tells recursion when to stop.

### Question 2

The recursive call must move toward the base case or it may never stop.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Start with recursion depth 1.

### Hint 2

Never remove the base case. The recursive call must reduce the depth.

### Worked example / minimal reference

Use the complete `branch(length, depth)` example. Run depth 1, then 2, then 3. The Sierpinski example is optional.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

The function needs a base case, such as `if n == 0: return`, and the recursive call should use `count_down(n - 1)`.

---

[Back to the lesson](../student-sessions/10-fractals-and-recursion.md)
