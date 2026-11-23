# Answer Key: Session 24: Movement, Timing, and Input

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

`clock.tick(60)` helps keep the loop near 60 frames per second.

### Question 2

Held-key input checks current key state; `KEYDOWN` represents a key-press event.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Draw a Rect on paper and label its four edges.

### Hint 2

Keep `clock.tick(60)` in the loop and change speed values rather than adding delays.

### Worked example / minimal reference

Use Part A for bouncing and Part B for player movement. They are intentionally separate checkpoints.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Use the player's width when calculating the boundary, for example `if player.right > 800: player.right = 800`. The right edge, not the center x-coordinate, must stay within the screen.

---

[Back to the lesson](../student-sessions/24-movement-timing-and-input.md)
