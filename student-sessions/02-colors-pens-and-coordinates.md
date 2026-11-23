# Session 2: Colors, Pens, and Coordinates

**Part of:** Module 1 — Turtle Basics
**Using:** turtle
**Today's mission:** Control how and where the turtle draws.


## Before you start

**Create this file:** `lesson02.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson02.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`color()`, `pensize()`, `penup()`, `pendown()`, `goto()`, `speed()`, `bgcolor()`, `begin_fill()`, `end_fill()`, `x/y coordinates`


## What the new Turtle commands mean

`color()` changes the pen colour. `pensize()` changes line thickness. `penup()` lifts the pen so movement does not draw; `pendown()` puts it down again. `goto(x, y)` moves to a particular coordinate. `speed()` changes animation speed and `bgcolor()` changes the background. `begin_fill()` and `end_fill()` surround the commands that make a shape you want filled.

Turtle normally starts at `(0, 0)`, the centre. Positive x goes right and negative x goes left. Positive y goes up and negative y goes down. So `(100, -50)` means 100 right and 50 down.

Turtle also has other commands such as `circle()`, `dot()`, `write()`, `setheading()`, and `home()`. You will meet new commands when they become useful.
### Pen-and-paper prediction
Use a sheet of paper as a mini Turtle screen. Draw the center `(0, 0)`, mark a few coordinates, and sketch the path you expect the turtle to take before you run the code. This is especially useful when using `goto()`, `penup()`, and `pendown()`.

## Start Here: (5–10 min)
Before running the next example, predict where `(0, 0)` should be if the screen is a map. In Turtle, the origin is normally at the center of the window.

## Learn the Idea: (10 min)
Show:
```python
import turtle

turtle.bgcolor("skyblue")
turtle.color("red")
turtle.pensize(5)
turtle.speed(5)

turtle.goto(100, 50)
turtle.goto(-100, 50)
```
Explain x: left/right and y: down/up. In Turtle, positive y is upward.

To move without drawing:
```python
turtle.penup()
turtle.goto(-100, -50)
turtle.pendown()
```

Filled shapes:
```python
turtle.color("red")
turtle.begin_fill()
for _ in range(4):
    turtle.forward(80)
    turtle.right(90)
turtle.end_fill()
```

## Try It
Use a printed coordinate grid. Call out coordinates and have you predict which quadrant they belong to. Then place the turtle at several points with `goto()`.

Make a traffic light:
```python
import turtle

turtle.speed(0)
turtle.bgcolor("gray")

for y, color in [(80, "red"), (0, "yellow"), (-80, "green")]:
    turtle.penup()
    turtle.goto(0, y)
    turtle.pendown()
    turtle.color(color)
    turtle.begin_fill()
    turtle.circle(30)
    turtle.end_fill()
```
For a simpler version, use the provided code and change only one value at a time.

## Checkpoint: What should I see?

You should see the pen change the drawing, and `goto()` should move the turtle without drawing when the pen is up.

## Your Core Challenge: Recreate a simple flag using rectangles/lines and `goto()`. Focus on precise positioning rather than perfect artwork.
### Minimum path: draw a simple flag

Turtle does not have a built-in `rectangle()` command. You can make a rectangle by drawing four sides.

Start with this complete program:

```python
import turtle

turtle.speed(5)

# Flag pole
turtle.goto(0, 0)
turtle.pendown()
turtle.forward(20)
turtle.right(90)
turtle.forward(120)
turtle.penup()

# Move to the flag's starting corner
turtle.goto(20, 0)
turtle.pendown()

# Draw a rectangle
turtle.forward(100)
turtle.right(90)
turtle.forward(60)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
turtle.forward(60)

turtle.done()
```

### Build it yourself

1. Copy and run the program.
2. On paper, draw the rectangle and label its four sides.
3. Change `100` to `80`. Run it.
4. Change `60` to `40`. Run it.
5. Add `turtle.color("blue")` before the rectangle.
6. Draw a second small shape inside the flag.

**Minimum success:** a rectangle-shaped flag with a pole.

### Stretch: traffic light

Use **three circles**, not a list. Put each circle at a different `y` coordinate.

This avoids using lists before they are taught in Session 8.

## Stretch Challenge: Make a traffic light with a dark housing and three colored lights.

## Bonus Challenge
Create a simple target with concentric circles placed at a chosen coordinate.

## Change-this experiments
- What happens if x changes but y stays the same?
- What happens if `penup()` is removed?
- What happens if `pensize(1)` becomes `pensize(10)`?
- What happens if the background changes?


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
The turtle should draw a line after moving to a new position, but it does not:
```python
import turtle

turtle.penup()
turtle.goto(100, 50)
turtle.forward(80)
turtle.goto(-100, 50)
turtle.forward(80)
```
Run it. Find the problem and fix the program so the two `forward()` commands draw lines. Try the fixed version and explain why `penup()` is useful before `goto()`.
## Finish by Thinking: Explain what `(100, -50)` means in Turtle.

## If you get stuck

**Try this lesson-specific recovery first:**

If a line appears when you only wanted to move, check whether the pen is down. If a line is missing, check `penup()`/`pendown()` and the order of your `goto()` commands.

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

[Check your answers and hints](../answers/02-answers.md)
