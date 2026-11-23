# Session 23: Hello Pygame: Write the Game Loop

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Recreate what Pygame Zero did behind the scenes by writing the game loop.

### Sketch the game loop
On paper, draw a circle or arrows showing the repeating cycle: **events → update → draw → repeat**. Keep this beside you while you write the loop. When the program behaves strangely, use the sketch to ask which part of the cycle might be responsible.


**You need from earlier lessons:** Session 22's successful `test_pygame.py` installation test.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson23.py`.

**Run it:**
```text
python lesson23.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`pygame.init`, `display.set_mode`, `while`, `event.get`, `QUIT`, `draw`, `flip`, `quit`

## Learn the Idea: Pygame Zero gave you a loop and window system automatically. Plain pygame asks us to write them.

Canonical template:
```python
import pygame

pygame.init()

WIDTH = 800
HEIGHT = 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("My Pygame")

running = True

while running:
    # 1. Events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # 2. Update
    # change game values here

    # 3. Draw
    screen.fill("skyblue")
    pygame.draw.circle(screen, "red", (400, 300), 50)

    # 4. Show the finished frame
    pygame.display.flip()

pygame.quit()
```

## Five areas
1. setup
2. event processing
3. update
4. drawing
5. display refresh

## Try It Step by Step
## Try It Step by Step

Do not write the whole loop from memory. Build it in pieces.

### Step 1 — open a window

```python
import pygame

pygame.init()

screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("My Game")

pygame.quit()
```

This opens and immediately closes the window. That is expected.

### Step 2 — keep the window open

Add:

```python
running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
```

An **event** is something that happened, such as clicking the close button.

### Step 3 — draw

Inside the loop, before `pygame.display.flip()`:

```python
screen.fill("skyblue")
pygame.draw.circle(screen, "red", (400, 300), 50)
```

### Step 4 — show the finished frame

Add:

```python
pygame.display.flip()
```

`flip()` means "show the finished picture on the window."

### Complete program

```python
import pygame

pygame.init()

screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("My Game")

running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    screen.fill("skyblue")
    pygame.draw.circle(screen, "red", (400, 300), 50)

    pygame.display.flip()

pygame.quit()
```

Run this complete version before changing it.

## Comparison
Pygame Zero `draw()` ≈ drawing section in the loop.
Pygame Zero `update()` ≈ update section.
Pygame Zero automatic event handling ≈ `pygame.event.get()`.


## Checkpoint: What should I see?

A pygame window should open, show the requested shapes, and close cleanly when you click the close button.

## Your Core Challenge: Create a working scene with at least three shapes and a clean quit path.
Start with the complete loop above.

### Build the scene

1. Run the starter unchanged.
2. On paper, sketch your scene.
3. Change the circle's position.
4. Add one rectangle with `pygame.draw.rect`.
5. Run it.
6. Add one line with `pygame.draw.line`.
7. Run it.
8. Add one more shape if you want.

**Minimum success:** a window with at least three shapes and a working close button.

Do not add movement yet. Movement is the next lesson.

## Stretch Challenge: Change the background color when a key is pressed.

## Bonus Challenge
Create a small animated element by changing one coordinate each loop.

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
This game loop draws a circle but never shows the finished frame:
```python
import pygame
pygame.init()
screen = pygame.display.set_mode((800, 600))
running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    screen.fill("skyblue")
    pygame.draw.circle(screen, "red", (400, 300), 50)

pygame.quit()
```
Run it. Find the missing step that makes the drawing appear. Add it in the right place.
## Finish by Thinking: What are the five conceptual parts of the pygame loop?

## If you get stuck

**Try this lesson-specific recovery first:**

If the window opens and immediately closes, check that the event loop is running. If shapes do not appear, check that drawing commands occur before `pygame.display.flip()`.

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

## The plain pygame game loop

Pygame makes you responsible for the main loop. Think of it as five jobs: **setup, event processing, update, drawing, display refresh**.

Event processing handles things such as quitting the window and key presses. Update changes the game state. Drawing puts the current state on the screen. `pygame.display.flip()` shows the newly drawn frame.

Pygame Zero hid much of this machinery. Plain pygame exposes it, giving you more control but also more responsibility.

---

[Check your answers and hints](../answers/23-answers.md)
