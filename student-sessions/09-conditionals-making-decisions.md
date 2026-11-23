<!-- SESSION NAV START -->
[← Previous: Session 8: Randomness and Lists](./08-randomness-and-lists.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 10: Fractals and Recursion →](./10-fractals-and-recursion.md)
<!-- SESSION NAV END -->

# Session 9: Conditionals: Making Decisions

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Make a program choose what to do based on conditions.


## Before you start

**Create this file:** `lesson09.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson09.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`if`, `elif`, `else`, `comparison`, `boolean`, `and`, `or`


## Conditionals: making decisions

An `if` statement asks whether a condition is true. If it is, the indented block runs. `else` gives an alternative. `elif` lets you test another condition.

Common comparisons are `==` equal, `!=` not equal, `<`, `>`, `<=`, and `>=`. Be careful: `=` assigns a value, while `==` compares two values.

You can combine conditions with `and` and `or`. Conditions are the bridge between what the program knows and what it decides to do.
### Pen-and-paper prediction
Make a two-column table before running your code: **condition** and **what should happen**. Try values that make the condition true and values that make it false. Then test each case.

## Start Here: Play a human decision game: “If I say red, clap; otherwise stand still.”
You can do this alone.

Write these two rules on paper:

- If the card says **red**, clap.
- Otherwise, do nothing.

Now imagine showing the computer a value called `color`.

The programming version is:

```python
color = "red"

if color == "red":
    print("Clap!")
else:
    print("Stand still.")
```

`if` asks a question. If the answer is true, Python runs the indented block. Otherwise it runs the `else` block.

Start with `if` and `else` today. `and` and `or` are optional until the basic idea feels comfortable.

## Learn the Idea: ```python
if score > 10:
    print("Great job!")
else:
    print("Keep trying!")
```
Explain the colon and indentation.

Comparisons:
`<`, `>`, `<=`, `>=`, `==`, `!=`

Multiple choices:
```python
if x < 0:
    color = "red"
elif x > 0:
    color = "blue"
else:
    color = "white"
```

Combining conditions:
```python
if x > 0 and y > 0:
    print("top right")
```

## Try It boundary-aware turtle
Use a turtle whose x/y position is checked. If it gets too far right, turn around.

## Position-dependent color
Draw on the left in red and right in blue.

## Guess-the-number bridge
```python
import random

secret = random.randint(1, 10)
guess = int(input("Guess 1–10: "))

if guess == secret:
    print("You got it!")
elif guess < secret:
    print("Too low!")
else:
    print("Too high!")
```

## Checkpoint: What should I see?

The program should make a different choice when its condition is true versus false. A checkerboard should alternate predictably, not randomly.

## Your Core Challenge: Make a checkerboard where the color depends on whether a square is in an even/odd position.
First learn the even/odd rule.

A number is **even** if it can be divided into pairs with nothing left over:

- 0, 2, 4, 6 are even.
- 1, 3, 5, 7 are odd.

Python can test this with `% 2`:

```python
number = 4

if number % 2 == 0:
    print("even")
else:
    print("odd")
```

`%` means "remainder after division."

### Build the checkerboard

Use a row and column number. The simple rule is:

```python
if (row + column) % 2 == 0:
    color = "black"
else:
    color = "white"
```

Your job is to use this rule while drawing the squares.

### Minimum path

1. Draw one square.
2. Draw a row of four squares.
3. Add the even/odd rule.
4. Draw four rows.
5. Run it and compare the result with your paper checkerboard.

Do not add `and` or `or` until this works.

## Stretch Challenge: Create three zones with three colors.


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
Fix the three bugs in this program. It should print `You can enter!` when `age` is 10 or more.
```python
age = 12

if age >= 10
print("You can enter!")
```
First predict what is wrong. Then run it, fix it, and run it again.
## Finish by Thinking: What question does an `if` statement answer? What is the difference between `=` and `==`?

## If you get stuck

**Try this lesson-specific recovery first:**

If every checkerboard square has the same color, first test a tiny condition with one square and print the values you are comparing. Do not add `and` or `or` until the basic `if` works.

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

[Check your answers and hints](../answers/09-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 8: Randomness and Lists](./08-randomness-and-lists.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 10: Fractals and Recursion →](./10-fractals-and-recursion.md)
<!-- SESSION NAV END -->
