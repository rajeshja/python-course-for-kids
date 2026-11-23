<!-- SESSION NAV START -->
[← Previous: Session 13: Hello Pygame Zero](./13-hello-pygame-zero.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 15: Keyboard and Mouse Control →](./15-keyboard-and-mouse-control.md)
<!-- SESSION NAV END -->

# Session 14: Animation with update() and Actors

**Part of:** Module 3 — Making It Interactive
**Using:** pygame-zero
**Today's mission:** Make objects move by changing values every frame.


**You need from earlier lessons:** Session 13's Pygame Zero setup and `draw()`/`update()` idea.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson14.py`.

**Run it:** from the project folder, run:

```text
pgzrun lesson14.py
```

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`animation`, `frame`, `update()`, `speed`, `Actor`, `x`, `y`


## Animation: change, then draw again

Animation is repeated change. `update()` changes positions, scores, or other game state. `draw()` displays the current state. If an object's x position changes a little on every update, it appears to move.

An `Actor` is a Pygame Zero object that can represent a player, enemy, or item. It has useful properties such as `x`, `y`, and `pos`, and can be drawn with `.draw()`.

A useful rule is: **update = change what is happening; draw = show what is happening.**
### Pen-and-paper prediction
Draw three tiny snapshots of the screen: **before**, **after one update**, and **after several updates**. Mark how you think the Actor will move. Then run the program and compare the snapshots with what actually happens.

## Start Here: Make a tiny paper flipbook

Draw three quick pictures of a ball in different positions. Flip the pages quickly. Notice how many still pictures can look like movement.

## Learn the Idea: update()
## Learn the Idea: `update()`

Pygame Zero calls `update()` again and again while the game is running.

Start with an Actor so the object remembers its own position:

```python
ball = Actor("ball")
ball.pos = (100, 300)

def update():
    ball.x += 2

def draw():
    screen.fill("black")
    ball.draw()
```

Each update moves the ball 2 pixels to the right. Then `draw()` shows the new position.

**You do not need `global` for this example.**

If the ball disappears off the right side, that is expected. The next section teaches bouncing.

## Prefer Actor attributes
## Prefer Actor attributes

An **Actor** is a game object that can have a picture and a position.

The Actor keeps its own position, so we do not need a separate `global x` variable.

Copy this complete program:

```python
ball = Actor("ball")
ball.pos = (400, 300)

speed_x = 4
speed_y = 3

def update():
    ball.x += speed_x
    ball.y += speed_y

def draw():
    screen.clear()
    ball.draw()
```

Put `ball.png` from `resources/pygame-zero/images/` into your project's `images` folder first.

Run it.

**You should see:** the ball move across the screen.

The next step will add the wall checks that make it bounce.

## Bouncing
## Bouncing

Start with the moving ball above. Add one wall check at a time.

```python
if ball.left < 0 or ball.right > WIDTH:
    speed_x = -speed_x
```

Run it and test the left and right walls.

Then add:

```python
if ball.top < 0 or ball.bottom > HEIGHT:
    speed_y = -speed_y
```

Run it again.

You can think of `left`, `right`, `top`, and `bottom` as the four edges of the Actor's picture.

### Why not use `global`?

You may see examples that use `global speed_x`. We are deliberately avoiding that in the main path. If you later need to change a variable created outside `update()`, the word `global` tells Python to use that outside variable. It is not needed for the basic Actor movement example above.

For today's lesson, focus on the Actor's position and the bounce rule.

## Multiple actors
## Optional: multiple Actors

Once one ball works, you can make another:

```python
ball2 = Actor("ball")
ball2.pos = (200, 200)
```

Then give it its own speed.

Do not use this list-comprehension example yet:

```python
balls = [Actor("ball") for i in range(5)]
```

It combines lists and loops in one line. Those ideas are already known from earlier lessons, but you do not need to combine them to finish today's Core Challenge.

## Checkpoint: What should I see?

The object should move every frame. In the completed example it should bounce back when it reaches each edge.

## Your Core Challenge: Make one object bounce off all four walls.

## Stretch Challenge: Make several balls with different speeds.

## Bonus Challenge
Increase the speed whenever the ball hits a wall.

## Key comparison
Turtle: `forward(10)` moves immediately.
Pygame Zero: change a position in `update()`; `draw()` shows the new position.

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
The ball should move every frame, but it stays still:
```python
ball_x = 100

def update():
    ball_x = ball_x + 5

def draw():
    screen.draw.filled_circle((ball_x, 100), 20, "red")
```
Find the problem. Fix the program so `ball_x` can change inside `update()`.
## Finish by Thinking: What is the job of `update()`? What is the job of `draw()`?

## If you get stuck

**Try this lesson-specific recovery first:**

If the object moves but does not bounce, check which edge property you compare and reverse the matching speed. Prefer the Actor's own `x` and `y` attributes instead of adding `global` variables.

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

[Check your answers and hints](../answers/14-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 13: Hello Pygame Zero](./13-hello-pygame-zero.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 15: Keyboard and Mouse Control →](./15-keyboard-and-mouse-control.md)
<!-- SESSION NAV END -->
