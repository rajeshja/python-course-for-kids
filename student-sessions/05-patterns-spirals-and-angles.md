<!-- SESSION NAV START -->
[← Previous: Session 4: Variables: Giving Things Names](./04-variables-giving-things-names.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 6: Functions: Your Own Commands →](./06-functions-your-own-commands.md)
<!-- SESSION NAV END -->

# Session 5: Patterns, Spirals, and Angles

**Part of:** Module 1 — Turtle Basics
**Using:** turtle
**Today's mission:** Combine loops and changing variables to create patterns.


## Before you start

**Create this file:** `lesson05.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson05.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`changing variable`, `nested loop`, `spiral`, `pattern`, `angle`


## How patterns grow

A variable can change inside a loop. In a spiral, for example, `size = size + 5` makes each new line longer.

A **nested loop** is a loop inside another loop. In the square-circle example, the inner loop draws one square and the outer loop repeats that square while turning the turtle.

Changing small numbers can create very different artwork. There is no single correct pattern. Experiment with the repeat count, size change, turn angle, and colours and observe what happens.
### Pen-and-paper planning
Sketch your pattern before coding it. Mark the first few lines, the direction of rotation, and how the size changes. You can change the sketch as you experiment; it is a plan, not a test you can fail.

## Start Here: Compare two nearly identical spirals

Look at two spiral drawings (or draw two quick spirals on paper). Circle the tiny numerical change you think could make one spiral grow differently.

## Learn the Idea: Variables can change inside loops:
```python
size = 10

for i in range(30):
    turtle.forward(size)
    turtle.right(90)
    size = size + 5
```
The loop repeats, while the size grows each time.

## Try It square spiral
You predict what happens if `size = size + 2`, `+5`, or `+10`.

## Circle of squares
A repeated shape can also rotate:
```python
import turtle

for i in range(36):
    for j in range(4):
        turtle.forward(50)
        turtle.right(90)
    turtle.right(10)
```
Notice that the inner loop draws one square and the outer loop repeats/rotates it.

## Rainbow spiral
You can cycle through a fixed sequence of colors manually. When you have many values to manage, a list can make that easier.

## Checkpoint: What should I see?

You should see the pattern change as the size or turning amount changes. Your paper sketch should look roughly like the computer's path.

## Your Core Challenge: Invent a personal pattern. It must contain:
Do not invent the whole pattern from nothing. Start with the square spiral below.

```python
import turtle

size = 20

for i in range(20):
    turtle.forward(size)
    turtle.right(90)
    size = size + 5

turtle.done()
```

### Build your own version

Change **one thing at a time**:

1. Run the starter unchanged.
2. Change the starting `size`.
3. Run it.
4. Change `size = size + 5` to `size = size + 2`.
5. Run it.
6. Change `right(90)` to `right(60)`.
7. Run it.
8. Change the repeat count.
9. Run it.
10. Give your pattern a name.

**Minimum success:** your program creates a repeated pattern and you can point to the number that controls its growth.

### Plan first

Before each major change, draw 4–6 turns on paper. Predict whether the pattern will grow, shrink, turn more tightly, or spread out.

## Stretch Challenge: Make a pattern where both size and turning angle change.

## Bonus Challenge
Create a “mandala” by repeating a small pattern around a circle.

## Gallery
## Gallery

If you want to save your work as a picture:

1. Run the program.
2. Make sure the Turtle window shows your finished pattern.
3. Use your computer's screenshot tool.
4. Save the screenshot with a useful name such as `my-pattern.png`.

You do not need to upload or share the picture to finish the lesson.

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
This spiral is supposed to grow, but it keeps the same size:
```python
import turtle

size = 10
for i in range(20):
    for j in range(4):
        turtle.forward(size)
        turtle.right(90)
    turtle.right(18)
```
Run it and describe the problem. Fix the program so the square gets larger after each turn. Choose your own growth amount.
## Finish by Thinking: What does changing a number inside a loop allow the computer to do?

## If you get stuck

**Try this lesson-specific recovery first:**

If a pattern becomes enormous, reduce the starting size or the amount added each loop. If the turns look wrong, draw one turn on paper before changing the angle.

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

[Check your answers and hints](../answers/05-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 4: Variables: Giving Things Names](./04-variables-giving-things-names.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 6: Functions: Your Own Commands →](./06-functions-your-own-commands.md)
<!-- SESSION NAV END -->
