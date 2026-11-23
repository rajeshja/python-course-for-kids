# Session 8: Randomness and Lists

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Use lists and random choices to create variation.


## Before you start

**Create this file:** `lesson08.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson08.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`import`, `random`, `randint`, `choice`, `list`, `index`, `append`


## Lists and randomness

A **list** stores several values together: `colors = ["red", "blue", "green"]`. Python numbers list positions from 0, so `colors[0]` is `"red"`. `append()` adds an item.

The `random` module lets a program make different choices. `random.choice(colors)` picks one item from the list. `random.randint(20, 100)` chooses a whole number in that range.

A list holds many values, an index identifies a position, and randomness lets the program vary its behaviour. These three ideas work especially well together in drawings and games.
### Pen-and-paper prediction
For list exercises, write the list and number its positions starting at 0. For random programs, write down a few possible results before you run the program. You cannot predict the exact random choice, but you can predict what kinds of results are possible.

## Start Here: Think: “How could the computer choose a different star size every time?”

## Randomness
```python
import random

size = random.randint(20, 80)
color = random.choice(["red", "blue", "purple"])
```
Notice that randomness lets the program choose from possibilities.

## Lists
## Lists: a shelf with several labelled places

A **list** stores several values together.

Start with something familiar:

```python
shopping = ["apples", "bread", "milk"]
print(shopping)
```

The first item is at position `0`:

```python
print(shopping[0])  # apples
print(shopping[1])  # bread
```

Why does counting start at 0? Think of the number as the **number of steps from the beginning**. The first item is zero steps from the beginning.

You can add an item:

```python
shopping.append("juice")
```

For now, only learn these three list actions:

- create a list with `[ ]`;
- get an item with `[number]`;
- add an item with `.append()`.

## Try It random stars
```python
import turtle
import random

colors = ["white", "yellow", "lightblue"]

for i in range(50):
    x = random.randint(-300, 300)
    y = random.randint(-200, 200)
    size = random.randint(5, 20)

    turtle.penup()
    turtle.goto(x, y)
    turtle.pendown()
    turtle.color(random.choice(colors))
    turtle.dot(size)
```

## Important concept
The *rules* are fixed even when the result changes. The computer is still following instructions.

## Checkpoint: What should I see?

Running the star example should produce stars at different positions or sizes. Running it again may produce a different arrangement.

## Your Core Challenge: Create a starry sky with random positions, colors, and sizes.
Start with the complete program below:

```python
import turtle
import random

colors = ["white", "yellow", "cyan"]

for i in range(20):
    x = random.randint(-250, 250)
    y = random.randint(-180, 180)
    size = random.randint(5, 15)

    turtle.penup()
    turtle.goto(x, y)
    turtle.pendown()

    turtle.dot(size, random.choice(colors))

turtle.done()
```

### Build it step by step

1. Run the starter unchanged.
2. Draw on paper where you think the 20 stars might appear.
3. Run it again. Notice that the arrangement can change.
4. Change `20` to `30`.
5. Change the size range.
6. Add one more color to the list.

**Minimum success:** a sky containing stars at random positions and at least two colors.

`random.choice(colors)` means "choose one item from this list at random." The computer is still following rules; it is choosing one allowed value.

## Stretch Challenge: Use a list of colors to draw a striped design.

## Bonus Challenge
Create a random “alien garden” where each flower has a random color and size.


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
This program tries to choose the fifth color from a list of five colors:
```python
import random

colors = ["red", "blue", "green", "yellow", "purple"]
print(colors[5])
```
Run it. Fix the index so the program prints the fifth color. Then try choosing a random color with `random.choice(colors)`.
## Finish by Thinking: What is a list? What is `random.choice()` useful for?

## If you get stuck

**Try this lesson-specific recovery first:**

If a list index error appears, remember that the first item is number 0. If stars look identical, check that the random value is used when each star is created.

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

[Check your answers and hints](../answers/08-answers.md)
