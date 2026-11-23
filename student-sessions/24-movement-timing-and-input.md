<!-- SESSION NAV START -->
[← Previous: Session 23: Hello Pygame: Write the Game Loop](./23-hello-pygame-write-the-game-loop.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 25: Images, Text, Sound, and Collisions →](./25-images-text-sound-and-collisions.md)
<!-- SESSION NAV END -->

# Session 24: Movement, Timing, and Input

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Animate and control objects consistently using Rects, timing, and keyboard/mouse input.

### Pen-and-paper prediction
Draw the starting position of an object and predict where it will be after one update and after ten updates. For keyboard movement, draw the expected path for each key. Then run the program and compare your prediction with the result.


**You need from earlier lessons:** Session 23's working pygame loop.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson24.py`.

**Run it:**
```text
python lesson24.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`Clock`, `tick(60)`, `Rect`, `get_pressed`, `KEYDOWN`, `mouse position`, `constants`

## Timing
## Timing

A **frame** is one picture of the game.

If a computer draws pictures very quickly, the game can run at different speeds on different computers.

Use a clock:

```python
clock = pygame.time.Clock()
```

At the bottom of the game loop:

```python
clock.tick(60)
```

This asks pygame to keep the loop near 60 frames per second.

For today, think of it as:

> "Try not to run the loop faster than about 60 times each second."

You do not need to learn delta time yet.

## Rect
## Rect

A `Rect` is a rectangle that stores **position and size**.

```python
player = pygame.Rect(100, 100, 40, 40)
```

That means:

- left = 100
- top = 100
- width = 40
- height = 40

You can draw it:

```python
pygame.draw.rect(screen, "blue", player)
```

And move it:

```python
player.x += 4
```

On paper, draw a rectangle and label `left`, `right`, `top`, and `bottom`. This will make the later boundary code easier to understand.

## Bouncing
```python
vx = 4
vy = 3

ball.x += vx
ball.y += vy

if ball.left < 0 or ball.right > WIDTH:
    vx = -vx
if ball.top < 0 or ball.bottom > HEIGHT:
    vy = -vy
```

## Held keys
```python
keys = pygame.key.get_pressed()

if keys[pygame.K_LEFT]:
    player.x -= 5
if keys[pygame.K_RIGHT]:
    player.x += 5
```

## Single keypress
Use the event loop:
```python
if event.type == pygame.KEYDOWN:
    if event.key == pygame.K_SPACE:
        print("Jump!")
```

## Mouse
```python
mouse_x, mouse_y = pygame.mouse.get_pos()
```
and:
```python
if event.type == pygame.MOUSEBUTTONDOWN:
    print(event.pos)
```

## Constants
```python
WIDTH = 800
HEIGHT = 600
SPEED = 5
```

## Checkpoint: What should I see?

The ball should move and bounce. The player should move only while the chosen key is held and should remain inside the window.

## Your Core Challenge: Build a bouncing ball, then a player square controlled by arrows or WASD.
Do **one project at a time**.

### Part A — bouncing square

Start with:

```python
ball = pygame.Rect(100, 100, 40, 40)
vx = 4
vy = 3
```

Inside the update part of the loop:

```python
ball.x += vx
ball.y += vy
```

Then add the horizontal wall check and vertical wall check from the lesson.

**Checkpoint:** the square moves and bounces.

### Part B — player controls

After Part A works, make a second `Rect`:

```python
player = pygame.Rect(100, 500, 50, 30)
```

Use held-key input:

```python
keys = pygame.key.get_pressed()

if keys[pygame.K_LEFT]:
    player.x -= 5
if keys[pygame.K_RIGHT]:
    player.x += 5
```

Keep the player inside the window.

**Minimum success:** either Part A and Part B work in one program, or you can demonstrate each part separately. Do not add mouse controls until both work.

## Stretch Challenge: Build a paddle.

## Bonus Challenge
Create two-player Pong controls.

## Boundary check
Keep the player inside the screen.

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
This program is meant to keep the player inside an 800×600 window:
```python
player.x += 20

if player.x > 800:
    player.x = 800
```
Suppose `player.width` is 50. The player can still move partly off-screen. Fix the boundary so the player's right edge stays inside the window.
## Finish by Thinking: Why do we use `clock.tick(60)`? What is the difference between held-key input and a `KEYDOWN` event?

## If you get stuck

**Try this lesson-specific recovery first:**

If movement speed changes unexpectedly, keep `clock.tick(60)` in the loop and change the speed number rather than adding random delays. If a Rect boundary is confusing, draw the rectangle on paper and label left/right/top/bottom.

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

## Timing, Rects, and input

A game loop can run at different speeds on different computers. `pygame.time.Clock` and `clock.tick(60)` help keep the loop near 60 frames per second.

A `pygame.Rect` stores a rectangle's position and size. Its properties such as `x`, `y`, `left`, and `right` make movement and collision work easier.

`pygame.key.get_pressed()` is useful for movement while a key is held. A `KEYDOWN` event represents a particular key-press event. Mouse functions and events provide mouse position and clicks.

---

[Check your answers and hints](../answers/24-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 23: Hello Pygame: Write the Game Loop](./23-hello-pygame-write-the-game-loop.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 25: Images, Text, Sound, and Collisions →](./25-images-text-sound-and-collisions.md)
<!-- SESSION NAV END -->
