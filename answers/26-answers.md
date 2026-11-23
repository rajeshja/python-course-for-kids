# Answer Key: Session 26: Debugging Like a Pro

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

A breakpoint is useful when you need to pause at a specific line and inspect values or execution flow.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Start with `print()` if the debugger feels confusing.

### Hint 2

Set one breakpoint and inspect one variable.

### Worked example / minimal reference

The `number = 10` → `number = number + 5` debugger example is the minimal reference for breakpoints and Variables.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Bug 1: check a held key with `pygame.key.get_pressed()` or compare the event key to `pygame.K_LEFT`; `pygame.K_LEFT` by itself is just a constant. Bug 2: make `fruit_rect` match the fruit's actual position. Bug 3: set `score = 0` before the main loop so it is not reset every frame. Bug 4: clear the screen before drawing the new frame, for example `screen.fill(...)`. Bug 5: set `running = False` when `pygame.QUIT` happens.

---

[Back to the lesson](../student-sessions/26-debugging-like-a-pro.md)
