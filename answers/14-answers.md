# Answer Key: Session 14: Animation with update() and Actors

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

`update()` changes game state; `draw()` displays it.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Make one Actor move before adding bouncing.

### Hint 2

Check `left`, `right`, `top`, and `bottom` against the window edges.

### Worked example / minimal reference

Use the complete Actor example with `ball.x` and `ball.y`. It deliberately avoids `global` in the main path.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

`ball_x` is defined outside `update()`, so assigning to it inside the function creates a local variable. Add `global ball_x` inside `update()` for this simple example, or use an object/attribute for a larger game.

---

[Back to the lesson](../student-sessions/14-animation-with-update-and-actors.md)
