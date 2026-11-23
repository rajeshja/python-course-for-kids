# Answer Key: Session 18: Classes and Objects

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

A class is a blueprint; an object is one instance made from it.

### Question 2

Classes help when many similar objects share structure and behaviour.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Run the tiny `Dog` class first.

### Hint 2

Think of `self` as 'this particular object'.

### Worked example / minimal reference

Use the complete `Ball` class and create three objects with different positions or speeds. Do not start with a large game.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Inside `describe()`, the attribute is `self.size`, not `size`. Change the line to `print("Ball size:", self.size)`.

---

[Back to the lesson](../student-sessions/18-classes-and-objects.md)
