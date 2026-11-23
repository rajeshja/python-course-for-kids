# Answer Key: Session 15: Keyboard and Mouse Control

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

Use held-key input for continuous movement; use a key-down event for an action triggered by a key press.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

First make left/right movement work.

### Hint 2

Use the supplied `basket.png` or `alien.png` asset and check the `images` folder.

### Worked example / minimal reference

The complete paddle program is the minimal reference: movement plus left/right boundary checks.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Pygame Zero's `keyboard.left` is a value you check, not a function you call. Use `if keyboard.left:`.

---

[Back to the lesson](../student-sessions/15-keyboard-and-mouse-control.md)
