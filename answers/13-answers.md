# Answer Key: Session 13: Hello Pygame Zero

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

`draw()` contains instructions describing what should appear on screen.

### Question 2

Pygame Zero uses a top-left origin, unlike Turtle's usual centred origin; both still execute Python instructions to create visible results.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

If `pgzrun` is not recognized, return to the setup steps.

### Hint 2

Run the exact starter before changing it.

### Worked example / minimal reference

The complete `lesson13.py` starter is the reference: it opens a window and draws a yellow circle.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Pygame Zero redraws the screen through `draw()`. The final `screen.draw...` line should be inside `draw()`; the standalone line outside the function should be removed.

---

[Back to the lesson](../student-sessions/13-hello-pygame-zero.md)
