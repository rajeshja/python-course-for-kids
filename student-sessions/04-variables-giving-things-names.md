# Session 4: Variables: Giving Things Names

**Part of:** Module 1 — Turtle Basics
**Using:** turtle
**Today's mission:** Store values so they can be reused and changed.


## Before you start

**Create this file:** `lesson04.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson04.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`variable`, `assignment`, `value`, `arithmetic`, `input()`


## Variables: names for values

A variable gives a value a name. Think of it as a labelled box.

```python
size = 80
color = "blue"
```

The `=` means **assign**: put the value on the right into the name on the left. A variable can hold numbers or text. You can use the same idea to name many kinds of values, including lists and objects.

Variables can change: `size = size + 10` takes the old value, adds 10, and stores the new value. `input()` asks the user for text; `int()` can turn number-shaped text into a number. The important idea is that naming a value lets you reuse and change it in one place.
### Pen-and-paper prediction
Write the starting values of your variables on paper. If a loop changes a variable, make a tiny table showing its value after each repetition. Predict the drawing before you run it.

## Start Here: Show the same number `80` in four places in a drawing. Think: “If we want every 80 to become 120, how many places must we edit?”

## Learn the Idea: A variable is a named box containing a value:
```python
size = 80
angle = 90
color = "purple"
```
Use it:
```python
turtle.color(color)
turtle.forward(size)
turtle.right(angle)
```
Changing the box changes every place that uses it.

Explain assignment as “put this value into this named box.” A variable name should describe the value.

## Try It
```python
import turtle

size = 80
angle = 90
color = "blue"

turtle.color(color)

for i in range(4):
    turtle.forward(size)
    turtle.right(angle)
```
You change one variable at a time and predict the effect.

Arithmetic:
```python
size = 50
bigger = size * 2
```

## Input
### Optional: asking the player for a number

You do **not** need `input()` for today's Core Challenge. It is an extra example.

`input()` asks the person running the program to type something. What they type arrives as **text**.

For example:

```python
name = input("What is your name? ")
print("Hello", name)
```

If you ask for a number:

```python
age_text = input("How old are you? ")
age = int(age_text)
```

`int()` converts number-shaped text such as `"11"` into the number `11`.

You can see why the conversion is needed:

```python
age_text = "11"
print(age_text + "1")   # 111
```

The first value is text, so Python joins the two pieces of text.

```python
age = int("11")
print(age + 1)          # 12
```

The second value is a number.

If this feels like too much, skip this section and return to the variables examples.

## Checkpoint: What should I see?

You should be able to change `size`, `color`, or `angle` near the top and see the drawing change without editing every drawing command.

## Your Core Challenge: Create a program with variables for size, color, and angle. Change only the variables to create different shapes.

## Stretch Challenge: Make the shape grow:
```python
size = 20

for i in range(8):
    for j in range(4):
        turtle.forward(size)
        turtle.right(90)
    size = size + 10
```

## Bonus Challenge
Ask the user for a size and draw the shape at that size.


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
This program is supposed to store the square size in a variable:
```python
import turtle

size == 100

turtle.forward(size)
```
Run it. Find the mistake and fix it so `size` receives the value `100`. Then change `size` to `200` and observe the result.
## Finish by Thinking: What is a variable useful for? Why is changing one variable better than changing the same number everywhere?

## If you get stuck

**Try this lesson-specific recovery first:**

If a variable change does nothing, check that the drawing uses the variable name rather than the old number.

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

[Check your answers and hints](../answers/04-answers.md)
