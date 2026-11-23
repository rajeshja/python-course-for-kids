# Answer Key: Session 16: Collisions, Score, and Text

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

Collision detection tells the program whether game objects are touching or overlapping.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Build movement before collision, collision before score, score before lives.

### Hint 2

Use the supplied basket and apple images; do not search for missing assets.

### Worked example / minimal reference

The lesson's five checkpoints are the rescue implementation. Get each one running before moving to the next.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

`score` must exist before it is used. Add `score = 0` outside `update()`. Because `update()` changes it, a simple version also needs `global score` inside `update()`, or the score can be stored as an attribute such as `game.score`.

---

[Back to the lesson](../student-sessions/16-collisions-score-and-text.md)
