# Answer Key: Session 28: Project Workshop: Port or Create

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

The smallest playable version has the main loop, player control, and central interaction and can actually be played.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Start from the supplied title/playing/game-over state example.

### Hint 2

Do not add a new feature until the previous checkpoint works.

### Worked example / minimal reference

The state-machine program is the complete reference starter. Put your own tiny game inside its `playing` state.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

The code changes state simply because the program is in the title state. The state change should happen inside the Space-key event handler, for example `if event.type == pygame.KEYDOWN and event.key == pygame.K_SPACE: game_state = "playing"`.

---

[Back to the lesson](../student-sessions/28-project-workshop-port-or-create.md)
