# Answer Key: Session 23: Hello Pygame: Write the Game Loop

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

Setup, event processing, update, drawing, and display refresh.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Build the window first, then the event loop, then drawing.

### Hint 2

Remember to call `pygame.display.flip()` after drawing.

### Worked example / minimal reference

The complete loop in Try It Step by Step is the minimal reference implementation.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

The program needs `pygame.display.flip()` after drawing and before the next loop iteration. It shows the newly drawn frame.

---

[Back to the lesson](../student-sessions/23-hello-pygame-write-the-game-loop.md)
