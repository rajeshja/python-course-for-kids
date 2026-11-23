# Answer Key: Session 8: Randomness and Lists

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

A list stores several values together.

### Question 2

`random.choice()` selects one item from a sequence such as a list.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Create a small list first and print one item from it.

### Hint 2

Remember that the first list position is 0.

### Worked example / minimal reference

Use the supplied starry-sky program as the reference. It creates random positions and sizes and chooses a color from a list.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

A five-item list has indexes 0 through 4, so the fifth color is `colors[4]`. `random.choice(colors)` can choose any item from the list.

---

[Back to the lesson](../student-sessions/08-randomness-and-lists.md)
