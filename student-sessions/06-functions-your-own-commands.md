# Session 6: Functions: Your Own Commands

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Package code into a reusable named block.


## Before you start

**Create this file:** `lesson06.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson06.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`function`, `def`, `call`, `reusable`, `block`


## Functions: your own commands

A function is a named block of instructions. `def draw_house():` **defines** the function; `draw_house()` **calls** it and makes it run. Defining a function does not run its body immediately.

Functions prevent repeated code and give a complicated action a useful name. You can call the same function many times. A function can contain the Turtle commands you already know. Later lessons will show how a function can accept information. For now, focus on making a reusable command.
### Pen-and-paper planning
Before writing a function, sketch the small action it should perform. If you plan to use the function several times, draw where each copy should appear. This helps you decide which Turtle commands belong inside the function.

## Start Here: Imagine inventing a command called `draw_house()`. What should happen when you type it?

## Learn the Idea: A function is a new command we invent:
```python
def draw_house():
    turtle.forward(100)
    turtle.right(90)
    # ...
```
Then call it:
```python
draw_house()
```
Remember: defining describes the recipe; calling actually runs it.

## Try It
Turn an existing house into `draw_house()`.

After the house works, you can create another complete function for a tree. You do not need a placeholder or `pass` for today's challenge.

## Build a street
Call the same function several times. You can move the turtle between calls while each function uses the same instructions:
```python
draw_house()
turtle.penup()
turtle.goto(150, 0)
turtle.pendown()
draw_house()
```

## Checkpoint: What should I see?

Calling `draw_house()` should draw the same house each time. Moving the function call should move the place where the house is drawn.

## Your Core Challenge: Create `draw_house()` and call it at least three times.
You are going to **turn an existing working drawing into a function**. You do not have to invent the house.

Start with this complete program:

```python
import turtle

def draw_house():
    # square
    for i in range(4):
        turtle.forward(60)
        turtle.right(90)

    # roof
    turtle.left(45)
    turtle.forward(42)
    turtle.left(90)
    turtle.forward(42)
    turtle.left(45)

# Test the command once
draw_house()

turtle.done()
```

### Step by step

1. Copy the complete program.
2. Run it. Make sure one house appears.
3. Notice that the drawing commands are indented inside `draw_house()`.
4. Add `draw_house()` a second time.
5. If the second house needs a new position, use `penup()`, move, and `pendown()` between the calls.
6. Add a third call.

**Minimum success:** the same function draws three houses.

A **definition** creates the command. A **call** runs the command.

## Stretch Challenge: Add `draw_tree()` and `draw_cloud()` and make a scene.

## Bonus Challenge
Create a tiny “stamp collection” of three reusable shapes.


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
A function is defined below, but the program does not run:
```python
import turtle

draw_house()

def draw_house():
    turtle.forward(80)
    turtle.right(90)
    turtle.forward(60)
```
Run it. Find the problem and fix the program. Then call `draw_house()` twice.
## Finish by Thinking: What is the difference between defining and calling a function?

## If you get stuck

**Try this lesson-specific recovery first:**

If Python says a function is not defined, check the spelling and make sure the `def` block appears before the call.

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

[Check your answers and hints](../answers/06-answers.md)
