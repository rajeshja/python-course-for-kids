# Session 13: Hello Pygame Zero

**Part of:** Module 3 — Making It Interactive
**Using:** pygame-zero
**Today's mission:** See that the Python concepts remain the same while the drawing system changes.

### Pen-and-paper prediction
Before running a Pygame Zero drawing, sketch the screen as a rectangle. Mark where you expect the shapes to appear and remember that `(0, 0)` is the top-left corner. Then compare your sketch with the real screen.


## Before you start — Pygame Zero setup

This is a new tool, so do the setup once before continuing with Sessions 13–21.

**Create a project folder:** `pygame-zero-course`.

Inside it, create a file called `lesson13.py`.

Install Pygame Zero in the Python environment you will use for the course. In a terminal, run:

```text
pip install pgzero
```

If `pip` is not recognized, do not guess. Go to **Session 22 → Common setup problems** for the Python/terminal recovery steps, then return here.

**Run the file:** in the same terminal, from the folder containing the file, run:

```text
pgzrun lesson13.py
```

If your computer is configured so that the Pygame Zero run button works, you may use that instead.

For Sessions 14–21, keep using this same project folder. Create a new file for each lesson using the filename shown in that lesson.

**Expected result:** a game window opens. If it does not, fix the setup before changing the lesson code.

**Paper first:** sketch the game window and where you expect each object to appear.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`Pygame Zero`, `WIDTH`, `HEIGHT`, `draw()`, `screen.fill`, `filled_circle`, `filled_rect`, `text`, `top-left origin`

## The starter
Create `lesson13.py` in the Pygame Zero project folder.

Start with this complete program:

```python
WIDTH = 800
HEIGHT = 600
TITLE = "My First Pygame Zero"

def draw():
    screen.fill("navy")
    screen.draw.circle((400, 300), 60, "yellow")

```

Run it with:

```text
pgzrun lesson13.py
```

**You should see:** a navy window with a yellow circle in the middle.

### Where the supplied pictures live

The course includes simple images in `resources/pygame-zero/images/`. Copy those files into an `images` folder in your Pygame Zero project when a later lesson asks for them.

You do not need any images for this first lesson.

## Learn the Idea: draw()
Pygame Zero repeatedly calls `draw()` to repaint the screen.

```python
def draw():
    screen.fill("skyblue")
    screen.draw.filled_circle((400, 300), 50, "red")
    screen.draw.filled_rect(Rect((100, 100, 150, 80)), "green")
    screen.draw.text("Hello!", center=(400, 100), fontsize=50, color="white")
```

Important coordinate difference:
- Turtle: `(0,0)` is center; y increases upward.
- Pygame Zero: `(0,0)` is top-left; y increases downward.

## Translation activity
## Translation activity

Turtle and Pygame Zero both draw pictures, but they use different commands.

Do this in small steps:

1. Draw one circle.
2. Run it.
3. Add one rectangle.
4. Run it.
5. Add one line.
6. Run it.

Do not try to translate a whole Turtle picture at once.

**Paper first:** sketch where the three shapes should go.

## Functions inside draw()
```python
def draw_house(x, y):
    screen.draw.filled_rect(Rect((x, y, 100, 80)), "orange")
    # add roof lines

def draw():
    screen.fill("skyblue")
    draw_house(100, 400)
    draw_house(300, 400)
```

## Deliberate surprise: flickering stars
If random positions are generated inside `draw()`, stars jump every frame:
```python
def draw():
    for i in range(50):
        x = random.randint(0, WIDTH)
        y = random.randint(0, HEIGHT)
        screen.draw.filled_circle((x, y), 3, "white")
```
Think about why. This prepares you for Session 14: `draw()` is called repeatedly.

## Checkpoint: What should I see?

A Pygame Zero window should open and your `draw()` function should draw the example scene without flickering.

## Your Core Challenge: Draw a night sky with stars. Create the star positions once in a list *outside* `draw()` to stop flicker.

## Stretch Challenge: Add a moon and a house using a reusable function.

## Bonus Challenge
Translate one of your Session 11 artworks.

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
This Pygame Zero program is meant to draw a red circle, but the circle never appears:
```python
def draw():
    screen.fill("skyblue")
    screen.draw.filled_circle((200, 150), 30, "red")

screen.draw.filled_circle((200, 150), 30, "red")
```
Find the problem. Move the drawing command to the correct place and run the program.
## Finish by Thinking: What belongs in `draw()`? Name one thing that changed from Turtle and one thing that stayed the same.

## If you get stuck

**Try this lesson-specific recovery first:**

If `pgzrun` is not recognized, return to the Pygame Zero setup in this lesson. If an `Actor` or image is missing, check the exact filename and the `images` folder.

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

## Pygame Zero: drawing on a game screen

Pygame Zero is a beginner-friendly layer over pygame. It supplies helpful structures so you can start making games without writing all the setup yourself.

`draw()` describes what should appear on screen. `screen.fill()` fills the background; `screen.draw.circle()` and `screen.draw.line()` draw shapes; `screen.draw.text()` displays text.

Pygame Zero normally uses `(0, 0)` at the **top-left**. x increases to the right and y increases downward. This is different from Turtle. Pygame Zero repeatedly calls `draw()` while the game is running. A separate `update()` function can be used to change the game state, such as moving a player.

---

[Check your answers and hints](../answers/13-answers.md)
