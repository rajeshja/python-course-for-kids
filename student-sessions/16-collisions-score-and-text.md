<!-- SESSION NAV START -->
[← Previous: Session 15: Keyboard and Mouse Control](./15-keyboard-and-mouse-control.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 17: Images, Sound, and Polish →](./17-images-sound-and-polish.md)
<!-- SESSION NAV END -->

# Session 16: Collisions, Score, and Text

**Part of:** Module 3 — Making It Interactive
**Using:** pygame-zero
**Today's mission:** Build a complete first mini-game using collision detection and game state.

### Plan the game on paper
Sketch the player, falling objects, score, lives, and Game Over screen. Mark one example of a collision and one example of a miss. Then use the sketch as your checklist while building the game.


**You need from earlier lessons:** Session 15's keyboard controls and Session 14's Actor movement.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson16.py`.

**Run it:** from the project folder, run:

```text
pgzrun lesson16.py
```

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`collision`, `colliderect`, `collidepoint`, `score`, `lives`, `game over`, `scheduled spawning`

## Mission
Build **Catch the Falling Objects**.

## Game design
Player at bottom. Objects fall from the top. Catching an object increases score. Missing one costs a life. When lives reach zero, show Game Over.

## Starter
## Starter

This lesson builds the catch game in checkpoints. The starter uses the supplied course images.

Copy these files into your Pygame Zero project's `images` folder:

- `basket.png`
- `apple.png`

Then create `lesson16.py` with this **first checkpoint**:

```python
WIDTH = 800
HEIGHT = 600

player = Actor("basket")
player.pos = (400, 550)

fruit = Actor("apple")
fruit.pos = (400, 100)

score = 0
lives = 3
game_over = False

def update():
    if game_over:
        return

    if keyboard.left:
        player.x -= 6
    if keyboard.right:
        player.x += 6

    fruit.y += 4

def draw():
    screen.clear()
    player.draw()
    fruit.draw()
    screen.draw.text(f"Score: {score}", (20, 20), fontsize=40)
    screen.draw.text(f"Lives: {lives}", (20, 60), fontsize=40)
```

Run it.

**Checkpoint:** the basket moves, the apple falls, and score/lives are visible.

### Why `global` sometimes appears in game examples

When a function needs to change a variable created outside that function, Python normally treats a new assignment inside the function as a new local variable. The word `global` tells Python:

> "Use the same variable that was created outside this function."

You will see `global` in the optional full solution below. We are not using it until the moment it is needed.

## Scheduled spawning
## Build the game one checkpoint at a time

Do **not** add every feature at once.

### Checkpoint 1 — movement

Get the basket moving left and right.

### Checkpoint 2 — falling

Make the fruit move downward.

### Checkpoint 3 — catching

Add:

```python
if fruit.colliderect(player):
    score += 1
    reset_fruit()
```

Now test by deliberately moving the basket under the fruit.

### Checkpoint 4 — missing

If the fruit goes below the bottom of the screen:

```python
if fruit.top > HEIGHT:
    lives -= 1
    reset_fruit()
```

### Checkpoint 5 — game over

When lives reach zero, set `game_over = True` and show a message.

### Optional — scheduled spawning

Only after the single-fruit version works, try `clock.schedule_interval()` to create several falling objects. You do not need multiple objects to complete the lesson.

### Complete reference version

If you have completed the checkpoints but want to compare your whole program with a working version, use this:

```python
import random

WIDTH = 800
HEIGHT = 600

player = Actor("basket")
player.pos = (400, 550)

fruit = Actor("apple")
fruit.pos = (400, 100)

score = 0
lives = 3
game_over = False

def reset_fruit():
    fruit.x = random.randint(40, WIDTH - 40)
    fruit.y = 0

def update():
    global score, lives, game_over

    if game_over:
        return

    if keyboard.left:
        player.x -= 6
    if keyboard.right:
        player.x += 6

    if player.left < 0:
        player.left = 0
    if player.right > WIDTH:
        player.right = WIDTH

    fruit.y += 4

    if fruit.colliderect(player):
        score += 1
        reset_fruit()

    if fruit.top > HEIGHT:
        lives -= 1
        reset_fruit()

        if lives <= 0:
            game_over = True

def draw():
    screen.clear()
    player.draw()
    fruit.draw()

    screen.draw.text(f"Score: {score}", (20, 20), fontsize=40)
    screen.draw.text(f"Lives: {lives}", (20, 60), fontsize=40)

    if game_over:
        screen.draw.text(
            "GAME OVER",
            center=(WIDTH / 2, HEIGHT / 2),
            fontsize=70
        )
```

Here `global` is needed because `update()` changes `score`, `lives`, and `game_over`, which were created outside the function. You do not need to memorise this rule yet; notice how it fixes the scope problem in the Bug Hunt.

## Checkpoint: What should I see?

The player should move, an object should fall, catching it should increase the score, misses should reduce lives, and game over should be visible when lives reach zero.

## Your Core Challenge: Complete the game with player, falling object, score, lives, and game over.
Your Core Challenge is now a checklist, not a single giant task.

Complete these in order:

- [ ] basket moves
- [ ] apple falls
- [ ] catching the apple adds 1 to the score
- [ ] the apple returns to the top
- [ ] missing the apple removes 1 life
- [ ] game over appears at 0 lives
- [ ] close the game normally

Run after every tick.

**Minimum success:** one falling apple, a moving basket, a score, lives, and a working game-over condition.

Do not add multiple apples or scheduled spawning until all seven boxes work.

## Stretch Challenge: Make objects fall faster as score increases.

## Bonus Challenge
Add several object types: good objects increase score, bad objects cost a life.

## Optional: Peer play-test

If someone is available, let them try the game without explaining the controls. If you are working alone, test the game yourself using the checklist in the Core Challenge.

Each player gives:
- two things they liked
- one suggestion


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
The player should gain a point when touching the coin:
```python
def update():
    if player.colliderect(coin):
        score += 1

def draw():
    screen.draw.text(str(score), (10, 10))
```
Find the bug that stops the score from working. Fix it and make sure `score` starts at `0`.
## Finish by Thinking: What does collision detection tell the program?

## If you get stuck

**Try this lesson-specific recovery first:**

Build one system at a time. If scoring fails, temporarily print the score. If the player or object is missing, get movement working before adding collision or lives.

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

## Collision, score, and game state

**Collision detection** checks whether game objects touch or overlap. The result can be used in an `if` statement to decide what happens next.

A score or number of lives is simply stored in a variable. For example, `score += 1` increases the score. A game-over condition can be another `if` statement.

The important pattern is: **detect something → make a decision → change the game state → show the result**.

---

[Check your answers and hints](../answers/16-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 15: Keyboard and Mouse Control](./15-keyboard-and-mouse-control.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 17: Images, Sound, and Polish →](./17-images-sound-and-polish.md)
<!-- SESSION NAV END -->
