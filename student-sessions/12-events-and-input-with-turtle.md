<!-- SESSION NAV START -->
[← Previous: Session 11: Turtle Project and Checkpoint](./11-turtle-project-and-checkpoint.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 13: Hello Pygame Zero →](./13-hello-pygame-zero.md)
<!-- SESSION NAV END -->

# Session 12: Events and Input with Turtle

**Part of:** Module 3 — Making It Interactive
**Using:** turtle
**Today's mission:** Learn that a program can wait for an event and react to it.


## Before you start

**Create this file:** `lesson12.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson12.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`event`, `handler`, `onkey`, `listen`, `onscreenclick`, `ontimer`

## Key phrase
**“I write the function; the computer decides when to call it.”**


## Events: waiting for something to happen

An event-driven program can wait for a key press, mouse click, or timer. An **event handler** is a function connected to an event. The function runs when that event occurs.

`onkey(function, key)` connects a key to a function. `onscreenclick(function)` connects mouse clicks. `ontimer(function, delay)` schedules a function. `listen()` enables keyboard listening and `mainloop()` keeps the event-driven program running.

The important difference from earlier programs is that the event decides when the handler runs.
### Pen-and-paper planning
Draw a simple map of your interactive program. Write an event such as **left key pressed** or **mouse clicked** and draw an arrow to the action that should happen. This is a quick way to plan event-driven code.

## Start Here: Think About Events
How can a program react when something happens later, such as a key press or mouse click? Compare that with a normal program that simply runs from top to bottom.

## Keyboard events
## Keyboard events

Start with keyboard input only.

A keyboard event means:

> "A key was pressed."

Use this complete starter:

```python
import turtle

turtle.shape("turtle")

def move_up():
    turtle.setheading(90)
    turtle.forward(20)

def move_down():
    turtle.setheading(270)
    turtle.forward(20)

turtle.onkey(move_up, "Up")
turtle.onkey(move_down, "Down")
turtle.listen()
turtle.mainloop()
```

Notice that we write `move_up`, **not** `move_up()`.

That means:

> "When the Up key is pressed, Turtle should call this function."

Run it. Press the Up and Down arrow keys.

Only after this works should you add mouse controls.

## Mouse events
```python
def draw_dot(x, y):
    turtle.goto(x, y)
    turtle.dot(20, "red")

turtle.onscreenclick(draw_dot)
```

## Timer
## Optional stretch: Timer

A timer can ask a function to run later. This is more advanced than keyboard input.

Try this only after the drawing app works:

```python
def say_hello():
    print("Hello!")

turtle.ontimer(say_hello, 2000)
```

The number `2000` means about 2000 milliseconds, or 2 seconds.

You do not need `ontimer()` for today's Core Challenge.

## Try It
Build:
1. arrow-key turtle
2. mouse drawing
3. number keys that change color
4. timed creeping turtle

## Checkpoint: What should I see?

Pressing the chosen key should cause the Turtle to move or change. Clicking the window should cause the mouse action. The program should remain running until you close it.

## Your Core Challenge: Make a drawing app with at least two controls: keyboard movement and mouse drawing.
Build the drawing app in two checkpoints.

### Checkpoint 1 — keyboard

Start from the working keyboard example above.

Add one more key that turns the Turtle left or right.

Run it.

### Checkpoint 2 — mouse

Add a click handler:

```python
def draw_dot(x, y):
    turtle.goto(x, y)
    turtle.dot(10)
```

Connect it to clicks:

```python
turtle.onscreenclick(draw_dot)
```

Run it.

### Minimum success

- arrow keys move the Turtle;
- clicking the window draws a dot;
- the program keeps running until you close it.

### Stretch

Only after the minimum works, add color keys or a size control.

## Stretch Challenge: Add color keys and a size control.

## Bonus Challenge
Add a “clear” key using `turtle.clear()`.


## Bug Hunt

Before you change the code, do the seven steps below. Write your answers on paper.

1. **Predict:** What do you think will happen?
2. **Run:** Run the broken program exactly as it is.
3. **Look:** What message or unexpected result do you see?
4. **Find:** Which line gives you the biggest clue?
5. **Fix:** Change one thing.
6. **Run again:** Does the program now behave as expected?
7. **Explain:** In one sentence, what was wrong and why did your fix work?

Do not skip the first run. The error message is a clue, not a failure.
The up-arrow key is supposed to move the turtle, but nothing happens:
```python
import turtle

def go_up():
    turtle.setheading(90)
    turtle.forward(20)

turtle.listen()
turtle.onkey(go_up(), "Up")
turtle.mainloop()
```
Find the mistake in the event registration. Fix it, run the program, and press the Up arrow.
## Finish by Thinking: What is an event handler? Who decides when it runs?

## If you get stuck

**Try this lesson-specific recovery first:**

If a key does nothing, check that the program calls `listen()` and that the key name is spelled correctly. Remember: an event handler is the function name, without parentheses.

Then use the general routine:

1. Read the error message slowly.
2. Look at the line mentioned in the message.
3. Check spelling, brackets, quotes, colons, and indentation.
4. Compare what you expected with what actually happened.
5. Change **one thing** and try again.
6. Write down: **“I expected ____. It did ____. I tried ____.”**
7. Use the answer key's hints in order.

## Your final check

Before you finish, make sure your program runs and that you can explain the main idea of today's lesson in your own words.

---

[Check your answers and hints](../answers/12-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 11: Turtle Project and Checkpoint](./11-turtle-project-and-checkpoint.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 13: Hello Pygame Zero →](./13-hello-pygame-zero.md)
<!-- SESSION NAV END -->
