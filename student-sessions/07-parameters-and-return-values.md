<!-- SESSION NAV START -->
[← Previous: Session 6: Functions: Your Own Commands](./06-functions-your-own-commands.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 8: Randomness and Lists →](./08-randomness-and-lists.md)
<!-- SESSION NAV END -->

# Session 7: Parameters and Return Values

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Make functions flexible by giving them inputs and returning results.


## Before you start

**Create this file:** `lesson07.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson07.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`parameter`, `argument`, `default value`, `return`, `local variable`


## Parameters and return values

A **parameter** is an input name in a function definition. In `draw_square(size)`, `size` is the parameter. `draw_square(50)` supplies 50 as the argument. Parameters let one function work with many different values.

A function can also calculate something and send it back with `return`.

```python
def double(number):
    return number * 2
```

`double(7)` produces 14, which can be stored in another variable. Think of a function as a small machine: information can go in, instructions run, and a result can come out.
### Pen-and-paper prediction
For a function with parameters, make a small table: write the arguments you will give it and predict what it will draw or return. Check your predictions by running the code.

## Start Here: Compare `draw_house()` with a wish for `draw_house(50)` and `draw_house(120)`. Why would inputs make a function more useful?

## Learn the Idea: parameters
```python
def draw_square(size):
    for i in range(4):
        turtle.forward(size)
        turtle.right(90)
```
Call it:
```python
draw_square(50)
draw_square(100)
```
The number supplied is an argument.

Multiple parameters:
```python
def draw_star(size, color):
    turtle.color(color)
    for i in range(5):
        turtle.forward(size)
        turtle.right(144)
```

Optional: default values:
```python
def draw_star(size=50, color="gold"):
    ...
```

## Optional: Return values
A function can give a result back. This is useful later, but it is not needed for today's village challenge:
```python
def double(x):
    return x * 2

answer = double(7)
print(answer)
```
Use “machine that takes something in and gives something back” as the mental model.

## Try It
Upgrade yesterday's house/tree functions so they accept a size.

## Regular polygon
```python
def draw_polygon(sides, size):
    angle = 360 / sides
    for i in range(sides):
        turtle.forward(size)
        turtle.right(angle)
```

## Checkpoint: What should I see?

Calling the same function with different parameter values should produce differently sized results. A small `double(7)` example should produce the number 14.

## Your Core Challenge: Build a village with at least three differently sized buildings.
Start from the working `draw_house(size)` example in **Try It**.

### Step 1 — make size a parameter

Your function should look like:

```python
def draw_house(size):
    # use size in the drawing
    ...
```

A **parameter** is a named input that a function receives.

### Step 2 — call it with different arguments

An **argument** is the value you give the function:

```python
draw_house(50)
draw_house(80)
draw_house(110)
```

The three arguments make three different-sized houses.

### Step 3 — build the village

1. Draw the first house.
2. Move the Turtle to a new starting position.
3. Draw the second house.
4. Move again.
5. Draw the third house.
6. Check that the three sizes are visibly different.

**Minimum success:** three working houses with three different sizes.

### Return values — optional

After the village works, try:

```python
def double(number):
    return number * 2

answer = double(7)
print(answer)
```

`return` sends a value back to the code that called the function. You do not need this for the village.

## Stretch Challenge: Add color parameters.

## Bonus Challenge
Write a function that returns the turning angle for a polygon:
```python
def polygon_angle(sides):
    return 360 / sides
```

## Local/global intuition
## Optional: a first look at where values live

You do **not** need the words "local" and "global" for today's Core Challenge.

For now, remember one simple rule:

> A variable created inside a function normally belongs to that function.

For example:

```python
def make_number():
    number = 7
    return number

answer = make_number()
print(answer)
```

The function creates `number`, then `return` sends the value `7` back out.

Do not worry about changing variables outside a function yet. That becomes useful later when building games, and it will be explained when you need it.

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
This function is supposed to give the caller the area, but it does not:
```python
def rectangle_area(width, height):
    area = width * height
    print(area)

answer = rectangle_area(5, 4)
print(answer + 10)
```
Run it. The final line should print `30`. Find the bug and fix it without changing the final `print()` line.
## Finish by Thinking: What is a parameter? What does `return` do?

## If you get stuck

**Try this lesson-specific recovery first:**

If a parameter error appears, compare the number of values inside the parentheses with the number of parameters after `def`. For `return`, remember that it sends a value back to the line that called the function.

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

[Check your answers and hints](../answers/07-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 6: Functions: Your Own Commands](./06-functions-your-own-commands.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 8: Randomness and Lists →](./08-randomness-and-lists.md)
<!-- SESSION NAV END -->
