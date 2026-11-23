# Session 3: Loops: Let the Computer Repeat

**Part of:** Module 1 — Turtle Basics
**Using:** turtle
**Today's mission:** Replace repeated instructions with a for loop.


## Before you start

**Create this file:** `lesson03.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson03.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`for`, `range()`, `loop`, `iteration`, `indentation`, `polygon`


## What a `for` loop means
A `for` loop is a **repeat button**.

```python
for i in range(4):
    turtle.forward(50)
    turtle.right(90)
```

Read this as:

> "Repeat the two indented instructions 4 times."

`range(4)` means four repeats. The first value is 0, but you do not need to use that number yet.

### Indentation

The spaces before `turtle.forward()` and `turtle.right()` tell Python that both instructions belong to the loop.

Think of indentation as a **box**:

```text
for ...:
    ┌─ repeat these lines
    │
    └─ until the repeat count is finished
```

If a line is not indented, it is outside the loop.

## Start Here: Display four copies of:
```python
turtle.forward(100)
turtle.right(90)
```
Think: “What if I wanted 100 copies?”

## Learn the Idea: A loop tells Python to repeat a block:
```python
for i in range(4):
    turtle.forward(100)
    turtle.right(90)
```
Explain `i` as a counter that changes automatically. The indented lines belong to the loop.

Predict `range(4)`, `range(1)`, and `range(6)` before running.

## Try It
Start with the square. Then change only the repeat count and turning angle:
```python
import turtle

for i in range(3):
    turtle.forward(100)
    turtle.right(120)
```
This makes a triangle.

Try 4, 5, 6, and 8 sides. Think about notice that the turn must change as the number of sides changes.

## Polygon rule
For a regular polygon:
**turn angle = 360 ÷ number of sides**

Examples:
- triangle: 120°
- square: 90°
- pentagon: 72°
- hexagon: 60°

## Checkpoint: What should I see?

You should see each polygon complete cleanly. If a line is missing, check indentation inside the loop.

## Your Core Challenge: Write a program that asks for no input but draws a triangle, square, pentagon, and hexagon.
Build the four shapes directly with loops. Do not use functions yet; functions are taught in Session 6.

### Triangle

```python
for i in range(3):
    turtle.forward(60)
    turtle.right(120)
```

Run it.

### Square

Move the Turtle without drawing:

```python
turtle.penup()
turtle.goto(150, 0)
turtle.pendown()
```

Then repeat four sides:

```python
for i in range(4):
    turtle.forward(60)
    turtle.right(90)
```

### Add the pentagon

1. Move to another position with `penup()`, `goto()`, `pendown()`.
2. Repeat 5 sides.
3. Use `72` degrees for each turn.

### Add the hexagon

1. Move again.
2. Repeat 6 sides.
3. Use `60` degrees for each turn.

**Minimum success:** four closed shapes: triangle, square, pentagon, hexagon.

The rule is:

> turn angle = `360 / number_of_sides`

You can calculate the angle on paper before writing it.

## Stretch Challenge: Make a polygon using variables:
```python
sides = 6
size = 80
angle = 360 / sides

for i in range(sides):
    turtle.forward(size)
    turtle.right(angle)
```

## Bonus Challenge star
Experiment with `right(144)` and `range(5)` to draw a five-pointed star.


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
This loop is meant to draw a square, but its indentation is broken:
```python
import turtle

for i in range(4):
turtle.forward(100)
    turtle.right(90)
```
Run it. Fix the indentation so both turtle commands belong to the loop. Then run it again and check that a square appears.
## Finish by Thinking: What does `range(5)` tell Python? Why is indentation important?

## If you get stuck

**Try this lesson-specific recovery first:**

If only the first side is drawn, check indentation: the commands that repeat must be indented under `for`.

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

[Check your answers and hints](../answers/03-answers.md)
