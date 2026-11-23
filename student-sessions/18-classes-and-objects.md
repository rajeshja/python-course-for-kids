<!-- SESSION NAV START -->
[← Previous: Session 17: Images, Sound, and Polish](./17-images-sound-and-polish.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 19: Plan Your Game →](./19-plan-your-game.md)
<!-- SESSION NAV END -->

# Session 18: Classes and Objects

**Part of:** Module 4 — Structure and Final Project
**Using:** pygame-zero
**Today's mission:** Use classes to organize many similar game objects.


**You need from earlier lessons:** Session 14's Actor idea. You do not need to understand the whole catch game before learning the class example.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson18.py`.

**Run it:** In Mu, select **Pygame Zero** mode and click **Play**.

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`class`, `object`, `attribute`, `method`, `__init__`, `self`, `instance`


## Classes and objects

A **class** is a blueprint for objects. An **object** is one particular thing made from that blueprint. A class can describe both data and actions.

```python
class Enemy:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def move(self):
        self.x += 3
```

`self` means the particular object currently using the method. Classes become useful when many objects have the same structure and behaviour, such as many enemies.
### Pen-and-paper planning
Draw one example object and label the information it needs, such as position or speed. Then draw a second object of the same kind. Circle the information they share and the information that can be different. This is a useful way to see why a class can be helpful.

## Start Here: You have already used `Actor`. Notice that `Actor` is an object made from a class: a blueprint.

## Learn the Idea: A class describes what an object has and can do:
## Learn the Idea: a class is a blueprint

A **class** is a blueprint. An **object** is one thing made from that blueprint.

Before using a game, start with a tiny example:

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def say_hello(self):
        print("Hi, I am", self.name)

dog1 = Dog("Milo")
dog2 = Dog("Luna")

dog1.say_hello()
dog2.say_hello()
```

Here:

- `Dog` is the blueprint.
- `dog1` and `dog2` are objects.
- `name` is information each dog remembers.
- `say_hello()` is something each dog can do.
- `self` means **this particular object**.
- `__init__` runs when a new object is created.

Run this before looking at the game example.

You do not need to memorise the special names. Copy the pattern and change one thing at a time.

## Refactor
## Move from the tiny example to a game object

Now use the same idea for a ball.

```python
class Ball:
    def __init__(self, x, y, speed):
        self.x = x
        self.y = y
        self.speed = speed

    def move(self):
        self.x += self.speed
```

Create one:

```python
ball = Ball(100, 100, 4)
ball.move()
print(ball.x)
```

Run this before connecting the class to Pygame Zero.

The important idea is:

> Each Ball object remembers its own position and speed.

## Enemy
Create a simple `Enemy` class with behavior different from a Ball.

## Checkpoint: What should I see?

Creating one `Ball` object should give you one working ball. Creating three objects should give you three balls without copying the whole class.

## Your Core Challenge: Create a `Ball` class and at least three objects.
Use the Ball class from the previous section.

### Step 1

Create one Ball object and make it move.

### Step 2

Create a second Ball with a different starting position.

### Step 3

Create a third Ball.

### Step 4

Use a loop to move all three.

```python
balls = [
    Ball(100, 100, 3),
    Ball(300, 200, 5),
    Ball(500, 150, -4)
]

for ball in balls:
    ball.move()
```

If you connect the class to Pygame Zero, use the complete game example from the lesson rather than inventing the screen code.

**Minimum success:** three objects made from one class, each with its own position or speed.

## Stretch Challenge: Give each ball a different size or direction.

## Bonus Challenge
Create an `Enemy` with its own movement rule.

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
This class is meant to create a ball with a size, but creating the object causes an error:
```python
class Ball:
    def __init__(self, size):
        self.size = size

    def describe(self):
        print("Ball size:", size)

ball = Ball(50)
ball.describe()
```
Find the bug and fix it so the program prints `Ball size: 50`.
## Finish by Thinking: What is a class? What is an object? Why is a class useful when you have many similar things?

## If you get stuck

**Try this lesson-specific recovery first:**

If `self` or `__init__` looks confusing, go back to the tiny `Dog` example in this lesson. First make one object work; only then create three.

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

[Check your answers and hints](../answers/18-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 17: Images, Sound, and Polish](./17-images-sound-and-polish.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 19: Plan Your Game →](./19-plan-your-game.md)
<!-- SESSION NAV END -->
