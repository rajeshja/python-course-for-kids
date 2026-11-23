# Answer Key: Session 2: Colors, Pens, and Coordinates

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

`(100, -50)` means 100 units right and 50 units down from the Turtle origin.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Check whether the pen is up or down before each movement.

### Hint 2

Build the flag as four sides of a rectangle; move between shapes with `penup()`.

### Worked example / minimal reference

Use the complete flag program in the Core Challenge. Run it unchanged, then change one size or color.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

The turtle stays in pen-up mode. Add `turtle.pendown()` after the first `goto()` and before the first `forward()` so the forward moves draw. `penup()` is useful when you want to reposition without drawing.

---

[Back to the lesson](../student-sessions/02-colors-pens-and-coordinates.md)
