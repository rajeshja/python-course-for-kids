# Session 15: Keyboard and Mouse Control

**Part of:** Module 3 — Making It Interactive
**Using:** pygame-zero
**Today's mission:** Let the player control objects using keyboard and mouse input.


**You need from earlier lessons:** Session 14's Actor movement.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson15.py`.

**Run it:** from the project folder, run:

```text
pgzrun lesson15.py
```

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`keyboard.left`, `keyboard.right`, `on_key_down`, `on_mouse_down`, `on_mouse_move`, `boundaries`


## Keyboard and mouse input

For movement, `keyboard.left` or `keyboard.right` is useful because it stays true while the key is held. A key-down handler is better for an action that should happen once when a key is pressed, such as a jump or shot.

Mouse events can tell your program that the player clicked and can provide the mouse position. This is the same event idea from Turtle: connect an event to a function, then let the event cause that function to run.
### Pen-and-paper planning
Draw the game screen and mark where the player should move when each key is pressed. For mouse input, draw a few click positions and predict what the program should do at each one.

## Start Here: Compare “hold the key” and “tap the key.” Which should control movement? Which might control a jump or shot?

## Held keys
```python
player = Actor("alien")
player.pos = (400, 300)
speed = 5

def update():
    if keyboard.left:
        player.x -= speed
    if keyboard.right:
        player.x += speed
```

Keep the Actor on screen:
```python
if player.left < 0:
    player.left = 0
if player.right > WIDTH:
    player.right = WIDTH
```

## Single key press
```python
def on_key_down(key):
    if key == keys.SPACE:
        print("Jump!")
```

## Mouse
```python
def on_mouse_down(pos):
    player.pos = pos

def on_mouse_move(pos):
    player.pos = pos
```

## Try It
## Try It

Use the supplied `alien.png` image for the first two experiments.

Copy the image from `resources/pygame-zero/images/` into your project's `images` folder.

### Experiment 1 — held key

```python
player = Actor("alien")
player.pos = (400, 300)

def update():
    if keyboard.left:
        player.x -= 5
    if keyboard.right:
        player.x += 5

def draw():
    screen.clear()
    player.draw()
```

Run it and hold the arrow keys.

### Experiment 2 — mouse

Add:

```python
def on_mouse_move(pos):
    player.pos = pos
```

Run it and move the mouse.

Notice that the mouse version makes the Actor jump to the mouse position. That is useful for a cursor-controlled game, but you do not need to use it in the Core Challenge.

## Checkpoint: What should I see?

Holding the left/right control should move the paddle smoothly. It should stop at the screen edges.

## Your Core Challenge: Make a paddle that moves with left/right and cannot leave the screen.
Start from this complete program:

```python
WIDTH = 800
HEIGHT = 600

paddle = Actor("basket")
paddle.pos = (400, 550)

def update():
    if keyboard.left:
        paddle.x -= 6
    if keyboard.right:
        paddle.x += 6

    if paddle.left < 0:
        paddle.left = 0
    if paddle.right > WIDTH:
        paddle.right = WIDTH

def draw():
    screen.clear()
    paddle.draw()
```

Copy `basket.png` from `resources/pygame-zero/images/` into your project's `images` folder.

### Build it

1. Run the starter.
2. Hold left and right.
3. Draw the screen edges on paper.
4. Test what happens when the paddle reaches an edge.
5. Add the boundary lines if they are missing.
6. Only then add A/D controls.

**Minimum success:** the paddle moves left and right and never leaves the window.

## Stretch Challenge: Support both arrow keys and A/D.

## Bonus Challenge
Click to launch an object.

## Debugging prompts
If movement is too fast, reduce `speed`. If it moves off-screen, check boundary code. If `on_key_down` never runs, check its exact name and indentation.

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
The paddle should move while the left arrow is held:
```python
def update():
    if keyboard.left():
        paddle.x -= 5
```
What is wrong with the keyboard check? Fix it.
## Finish by Thinking: When would you use `keyboard.left` instead of `on_key_down(key)`?

## If you get stuck

**Try this lesson-specific recovery first:**

If movement is too fast, reduce the speed number. If it moves outside the window, compare the Actor's `left` and `right` values with `WIDTH`.

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

[Check your answers and hints](../answers/15-answers.md)
