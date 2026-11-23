# Answer Key: Session 12: Events and Input with Turtle

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

An event handler is a function connected to an event.

### Question 2

The event causes the handler to run.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Check that `listen()` is called.

### Hint 2

Event handlers are given without parentheses, such as `onkey(move_up, "Up")`.

### Worked example / minimal reference

Use the complete keyboard example first, then add `onscreenclick()` for mouse drawing. Timers are optional.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

Register the function itself, not the result of calling it. Use `turtle.onkey(go_up, "Up")`, without parentheses after `go_up`.

---

[Back to the lesson](../student-sessions/12-events-and-input-with-turtle.md)
