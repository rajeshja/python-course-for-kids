# Session 1: Meet the Turtle

**Part of:** Module 1 — Turtle Basics
**Using:** turtle
**Today's mission:** Understand that a program is a list of instructions run in order.


## Before you start

**Create this file:** `lesson01.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson01.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`sequence`, `turtle`, `forward()`, `backward()`, `left()`, `right()`, `angles`, `comments`


## What the Turtle commands mean

A **turtle** is a drawing robot. Your program tells it what to do one instruction at a time.

| Command | Meaning |
|---|---|
| `forward(100)` | Move forward 100 steps, drawing a line. |
| `backward(100)` | Move backward 100 steps, drawing a line. |
| `left(90)` | Turn 90 degrees left. The turtle does not move. |
| `right(90)` | Turn 90 degrees right. The turtle does not move. |

The number in parentheses is an **argument**. `forward(50)` moves 50 steps; `right(45)` turns 45 degrees. The turtle remembers its position and direction, so each instruction starts from the result of the previous one.

These are not the only Turtle commands. Other useful commands include `goto()`, `color()`, `penup()`, and `circle()`. You do not need to memorize every command: learn a few, then look up or ask about a command when your project needs it.
### Pen-and-paper prediction
Before you run a Turtle program, draw a tiny arrow showing where the turtle starts and where you think it will finish. Mark its direction after each turn. Then run the program and compare your drawing with the result. Your prediction does not have to be right—the useful part is making a prediction before you test it.

## Start Here: Human Robot (5–10 min)
You can do this activity by yourself.

### Solo Human Robot

Pretend that **you are the robot**.

Write these instructions on paper:

1. Take 5 steps forward.
2. Turn right.
3. Take 3 steps forward.
4. Turn left.
5. Take 2 steps forward.

Now draw the path on paper.

The important idea is that a computer follows instructions in order. It does not guess what you meant.

### First Python file

Create `lesson01.py`.

Type this complete program:

```python
import turtle

turtle.forward(100)
turtle.right(90)
turtle.forward(50)

turtle.done()
```

`import turtle` means **bring Python's Turtle drawing tool into this program**.

Save the file and run it.

**You should see:** a Turtle window with a long line followed by a shorter line after a right turn.

Do not change anything yet. First make sure this exact program works.

## Learn the Idea: Programs are instructions (10 min)
Notice that Python executes instructions from top to bottom. A turtle is useful because the result is visible immediately.

Start with:
```python
import turtle

turtle.forward(100)
turtle.right(90)
turtle.forward(100)
```
Predict before running. Notice that `right(90)` means turn 90 degrees, not move 90 pixels.

Comments are notes for people reading your code. Try this:
```python
# Draw the first side
turtle.forward(100)
```
A comment is a note for humans; Python does not execute it.

## Try It (15 min)
Build a square one instruction at a time:
```python
import turtle

turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
```
Try to predict the final direction of the turtle.

Next, try:
```python
import turtle

turtle.forward(120)
turtle.left(90)
turtle.forward(60)
turtle.right(90)
turtle.forward(120)
```

Change one number at a time. Try repeating a command yourself. If you can predict what the repeated commands will do, you are already thinking like a programmer.

## Checkpoint: What should I see?

You should see the Turtle window open and the example drawing a line or simple shape. The turtle should move exactly as the commands say.

## Your Core Challenge: Draw your initial
Your goal is to draw **one letter from your first name**.

Do not start by guessing commands. Plan it on paper first.

### Step 1 — Draw the letter on paper

Use a simple block-style letter made from straight lines.

For example, for a letter shaped like `L`, draw:

```text
|
|
|____
```

Mark the starting point with a dot and number the line segments in the order you want the Turtle to draw them.

### Step 2 — Turn the first segment into code

Start with:

```python
import turtle

turtle.forward(80)
```

Run it.

### Step 3 — Add one turn and one segment

Add a turn and another movement. Run it again.

### Step 4 — Finish the letter

Keep adding one segment at a time.

**Minimum success:** one complete letter made from straight lines.

If your letter needs the Turtle to move without drawing, use `turtle.penup()`, move, then `turtle.pendown()`.

You do not need perfect artwork. The goal is to make your plan become instructions.

## Stretch Challenge: House
Draw a simple house using straight lines only. Try to plan the instructions on paper first.

## Bonus Challenge
Add a chimney, door, or window using only the same commands.


## Show What You Made
Look at your drawing and write one sentence explaining an instruction that was important.

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
Try this broken program:
```python
import turtle

turtle.forward(100)
turtle.rigth(90)
turtle.forward(100)
```
Run it. Find the line Python complains about, identify the typo, fix it, and run the program again. Then change the turn to `left(90)` and predict what will change.
## Finish by Thinking: 1. What does `forward(50)` tell the turtle to do?
2. Why does the order of instructions matter?
3. What does `#` do in Python?

## If you get stuck

**Try this lesson-specific recovery first:**

If the Turtle window does not appear, make sure you ran the `.py` file with Python. If the turtle disappears, use `turtle.home()` to bring it back to the centre.

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

[Check your answers and hints](../answers/01-answers.md)
