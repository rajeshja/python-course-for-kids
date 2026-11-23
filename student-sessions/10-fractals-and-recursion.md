<!-- SESSION NAV START -->
[← Previous: Session 9: Conditionals: Making Decisions](./09-conditionals-making-decisions.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 11: Turtle Project and Checkpoint →](./11-turtle-project-and-checkpoint.md)
<!-- SESSION NAV END -->

# Session 10: Fractals and Recursion

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Understand recursion and use it to draw self-similar patterns.


## Before you start

**Create this file:** `lesson10.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson10.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`recursion`, `base case`, `recursive call`, `depth`, `self-similarity`, `fractal`


## Recursion and the rule for stopping
Recursion means **a function uses itself to make a smaller version of the same job**.

The safest way to learn it is to build the idea in tiny steps.

### Step 1 — one branch

Draw one branch by hand on paper.

### Step 2 — a smaller branch

Draw the same branch again, but shorter.

### Step 3 — the computer's rule

A recursive function needs two parts:

1. a **base case** — when to stop;
2. a **recursive call** — make a smaller version.

Example:

```python
import turtle

def branch(length, depth):
    if depth == 0:
        return

    turtle.forward(length)

    turtle.left(30)
    branch(length * 0.7, depth - 1)

    turtle.right(60)
    branch(length * 0.7, depth - 1)

    turtle.left(30)
    turtle.backward(length)

branch(100, 1)
turtle.done()
```

With `depth = 1`, the function calls itself only for the smaller branches.

Try `depth = 2`.

Then try `depth = 3`.

**Important:** never remove the `if depth == 0` stopping rule.

## Start Here: paper tree
Draw one branch, then from its tip draw two smaller branches. Apply the same rule again. The picture starts repeating itself.

## Learn the Idea: A recursive function is a function that calls itself. It must have a **base case**: a rule that says when to stop.

```python
import turtle

def branch(length, depth):
    if depth == 0:
        return

    turtle.forward(length)

    turtle.left(30)
    branch(length * 0.7, depth - 1)

    turtle.right(60)
    branch(length * 0.7, depth - 1)

    turtle.left(30)
    turtle.backward(length)

branch(100, 4)
```

Explain the call as a smaller version of the same recipe. `depth` gets smaller until it reaches 0.

## Visual trace
Draw nested boxes:
`branch(100,4)` → `branch(70,3)` → `branch(49,2)` → `branch(34,1)` → stop.

## Guided experiments
Change:
- branch angle
- shrinking factor
- starting length
- depth 1, 2, 3, 4

Then use:
```python
turtle.tracer(0)
branch(100, 5)
turtle.update()
```
Notice that this makes Turtle draw quickly; do not dwell on implementation details.

## Koch curve
For the Koch curve, use this rule: one segment becomes four smaller segments, with the middle two angled.

```python
def koch(length, depth):
    if depth == 0:
        turtle.forward(length)
        return

    length = length / 3
    koch(length, depth - 1)
    turtle.left(60)
    koch(length, depth - 1)
    turtle.right(120)
    koch(length, depth - 1)
    turtle.left(60)
    koch(length, depth - 1)
```

A snowflake is three Koch curves joined by 120-degree turns.

## Stretch: Sierpinski triangle

This is **stretch material**. You do not need it to complete the lesson.

If you want to try it, use this complete starter. It includes the triangle-drawing function so you are not asked to invent a missing function:

```python
import turtle

def draw_triangle(size):
    for i in range(3):
        turtle.forward(size)
        turtle.left(120)

def sierpinski(size, depth):
    if depth == 0:
        draw_triangle(size)
        return

    half = size / 2

    sierpinski(half, depth - 1)

    turtle.forward(half)
    sierpinski(half, depth - 1)

    turtle.backward(half)
    turtle.left(60)
    turtle.forward(half)
    turtle.right(60)
    sierpinski(half, depth - 1)

    turtle.left(60)
    turtle.backward(half)
    turtle.right(60)

sierpinski(200, 2)
turtle.done()
```

If this feels difficult, return to `branch()` and finish the Core Challenge instead.

## Checkpoint: What should I see?

At depth 1 you should see a small, understandable version of the recursive pattern. Increasing the depth should add more branches without changing the basic rule.

## Your Core Challenge: Create one fractal and write one sentence describing its rule.
Your minimum fractal is the guided `branch()` program above.

### Step 1
Run it with `depth = 1`.

### Step 2
Draw the result on paper.

### Step 3
Change only `depth` to `2`.

### Step 4
Predict what will happen at `depth = 3`.

### Step 5
Run it and compare your prediction.

### Step 6
Write one sentence:

> "My fractal works by __________________."

**Minimum success:** a working recursive branch and a one-sentence explanation.

You do not need to invent a new recursive algorithm today. Understanding the stopping rule and seeing depth change the picture is the goal.

## Stretch Challenge: Make a random tree using `random` from Session 8.

## Bonus Challenge
Invent a fractal rule of your own.

## Gallery
Save or print your favorite fractal with its rule sentence.

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
This recursive function never gets closer to stopping:
```python
def count_down(n):
    print(n)
    count_down(n)

count_down(3)
```
Run it and observe the error. Add a base case and make the recursive call move toward it. Your fixed version should print `3`, `2`, `1` and then stop.
## Finish by Thinking: What is the base case? Why must the recursive call move toward it?

## If you get stuck

**Try this lesson-specific recovery first:**

If recursion never stops, stop the program and check the base case. The recursive call must move toward the stopping point. Start again with depth 1.

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

[Check your answers and hints](../answers/10-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 9: Conditionals: Making Decisions](./09-conditionals-making-decisions.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 11: Turtle Project and Checkpoint →](./11-turtle-project-and-checkpoint.md)
<!-- SESSION NAV END -->
