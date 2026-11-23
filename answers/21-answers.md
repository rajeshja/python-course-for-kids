# Answer Key: Session 21: Showcase and Celebration

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

Answers vary.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Use the solo checklist if no one else is available.

### Hint 2

Test launch, controls, game action, win/lose, and quit.

### Worked example / minimal reference

The final self-check is the minimum reference; you do not need a game fair or shared folder.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

The function tries to assign to `score` without accessing the outer variable. For this simple example, add `global score` inside `add_point()`, or pass the score into a function and return the new value. A clean alternative is `def add_point(score): return score + 1`.

---

[Back to the lesson](../student-sessions/21-showcase-and-celebration.md)
