# Session 25: Images, Text, Sound, and Collisions

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Rebuild the catch game in plain pygame with assets, text, sound, and collisions.

### Plan the screen on paper
Sketch the game screen and mark the rectangles or positions of the important objects. Draw one example where two objects overlap and one where they do not. This gives you a visual prediction for your collision code.


**You need from earlier lessons:** Session 23's loop and Session 24's movement/input. Course assets are supplied in `../resources/pygame/`.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson25.py`.

**Run it:**
```text
python lesson25.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`image.load`, `convert_alpha`, `transform.scale`, `blit`, `Font`, `render`, `mixer`, `colliderect`, `assets`


## Images, text, sound, and collisions in pygame
## Images, text, sound, and collisions in pygame

This lesson has several new ideas, so learn them one at a time.

### `blit()` — put a picture on the screen

Think of `blit()` as:

> "Put this picture here."

```python
screen.blit(player_image, player_rect)
```

### `convert_alpha()`

`convert_alpha()` prepares an image so transparent parts can be drawn correctly. You can copy this line without learning the technical details yet.

### Text

A font turns words into an image that pygame can draw:

```python
font = pygame.font.Font(None, 40)
score_text = font.render("Score: 0", True, "white")
screen.blit(score_text, (20, 20))
```

### Sound

A sound effect is a short sound played for an event:

```python
catch_sound = pygame.mixer.Sound("assets/catch.wav")
catch_sound.play()
```

Background music is handled separately:

```python
pygame.mixer.music.load("assets/background.wav")
pygame.mixer.music.play(-1)
```

### Collision

`colliderect()` asks:

> "Do these two rectangles overlap?"

```python
if fruit_rect.colliderect(player_rect):
    print("Caught!")
```

Test each idea separately before combining them.

## Project structure
## Project structure

The course supplies the assets you need. Copy these files from `resources/pygame/assets/` into an `assets` folder beside `main.py`:

```text
catch-game/
├── main.py
└── assets/
    ├── basket.png
    ├── apple.png
    ├── catch.wav
    ├── miss.wav
    └── background.wav
```

The files are deliberately simple. You do not need to download anything.

**Checkpoint:** before writing the game code, confirm that all five files are visible in the `assets` folder.

## Images
```python
player_image = pygame.image.load("assets/basket.png").convert_alpha()
player_image = pygame.transform.scale(player_image, (80, 50))
player_rect = player_image.get_rect(center=(400, 550))
```

Draw with:
```python
screen.blit(player_image, player_rect)
```

## Text
```python
font = pygame.font.Font(None, 40)
score_text = font.render(f"Score: {score}", True, "white")
screen.blit(score_text, (20, 20))
```

## Sound
```python
catch_sound = pygame.mixer.Sound("assets/catch.wav")
catch_sound.play()
```

Music:
```python
pygame.mixer.music.load("assets/background.wav")
pygame.mixer.music.play(-1)
```

## Collision
```python
if fruit_rect.colliderect(player_rect):
    score += 1
```

## Build It Step by Step
## Build It Step by Step

Use `main.py` in the supplied `catch-game` structure.

### Checkpoint 1 — window and player

Open a window and draw the basket image.

### Checkpoint 2 — falling fruit

Add one apple rectangle and move it downward.

### Checkpoint 3 — collision

When the apple overlaps the basket, print `Caught!`.

### Checkpoint 4 — score

Replace the print with:

```python
score += 1
```

Draw the score on the screen.

### Checkpoint 5 — sound

Play `catch.wav` when the apple is caught.

### Checkpoint 6 — miss

When the apple moves below the window, move it back to the top and play `miss.wav`.

Run after every checkpoint.

**Minimum success:** a basket catches one falling apple, the score changes, and the catch sound plays.

## Checkpoint: What should I see?

The starter catch game should show the image, score text, and collision response. A missing asset should be caught by the troubleshooting steps instead of guessed at.

## Your Core Challenge: Complete the catch game.
Start with the checkpointed catch game above.

Finish these in order:

- [ ] basket is visible
- [ ] apple falls
- [ ] basket moves
- [ ] collision is detected
- [ ] score increases
- [ ] caught apple returns to the top
- [ ] miss sound works
- [ ] game quits normally

**Minimum success:** the player can catch falling apples and see the score change.

Lives and restart are stretch features. You do not need them for the minimum game.

## Stretch Challenge: Add lives and a restart key.

## Bonus Challenge
Add two types of falling objects.

## Common bug
`FileNotFoundError` usually means the working directory or path is wrong. Opening the project folder in VS Code is important.

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
The player and coin look like they overlap, but this collision test never fires:
```python
if player.colliderect(coin_image):
    score += 1
```
Assume `player` and `coin_image` are Surfaces, not Rects. Find what the collision test needs instead.
## Finish by Thinking: What does `blit()` do? What does `Rect.colliderect()` tell you?

## If you get stuck

**Try this lesson-specific recovery first:**

If an image does not load, verify the folder and filename. If sound does not play, check that pygame was initialized and the sound file is in `assets/`. If collision seems wrong, draw both rectangles on paper.

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

[Check your answers and hints](../answers/25-answers.md)
