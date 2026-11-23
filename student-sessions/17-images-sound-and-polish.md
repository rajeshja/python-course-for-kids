<!-- SESSION NAV START -->
[← Previous: Session 16: Collisions, Score, and Text](./16-collisions-score-and-text.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 18: Classes and Objects →](./18-classes-and-objects.md)
<!-- SESSION NAV END -->

# Session 17: Images, Sound, and Polish

**Part of:** Module 3 — Making It Interactive
**Using:** pygame-zero
**Today's mission:** Use images and sound to make a game feel finished.

### Pen-and-paper planning
Make a quick screen sketch showing where your images, text, and other visual elements should appear. Mark anything that should change during the game. This helps you decide what needs to be drawn or updated.


**You need from earlier lessons:** Session 16's working catch game. Course assets are supplied in `../resources/pygame-zero/`.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson17.py`.

**Run it:** from the project folder, run:

```text
pgzrun lesson17.py
```

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`images folder`, `sounds folder`, `Actor image`, `sound effect`, `music`, `angle`, `image swapping`, `attribution`

## Images
## Images

Pygame Zero looks for pictures in a folder named `images`.

The course supplies:

- `basket.png`
- `basket_left.png`
- `basket_right.png`
- `apple.png`
- `alien.png`
- `ball.png`

Copy only the files you need from `resources/pygame-zero/images/` into your project's `images` folder.

For example:

```python
player = Actor("basket")
fruit = Actor("apple")
```

Do not write `.png` inside `Actor()`.

If Python says an image is missing, check the spelling and folder before changing the code.

## Sound
## Sound

The course supplies three simple WAV files in `resources/pygame-zero/sounds/`:

- `catch.wav`
- `miss.wav`
- `background.wav`

Copy them into your project's `sounds` folder.

Then:

```python
sounds.catch.play()
```

plays the catch sound.

For background music:

```python
music.play("background")
```

Pygame Zero uses the name without the `.wav` extension for music.

Test one sound at a time before adding music.

## Rotation
```python
player.angle = 10
```

## Image swapping
```python
if player.x < WIDTH / 2:
    player.image = "basket_left"
else:
    player.image = "basket_right"
```

## Try It
Replace placeholder shapes in the catch game. Add a catch sound, a miss sound, and background music.

## Responsible assets
Use your own drawings or assets whose licence permits use. Keep an attribution note for anything that requires credit.

## Checkpoint: What should I see?

The supplied image and sound assets should load without missing-file errors. The game should show the image and play the chosen sound at the correct event.

## Your Core Challenge: Create a polished version of the catch game with images and at least two sounds.
Start from your **working Session 16 catch game**.

Do not rebuild the game from scratch.

### Checkpoint 1 — images

Replace the simple drawing with `basket.png` and `apple.png`.

Run it.

### Checkpoint 2 — catch sound

Add `sounds.catch.play()` when the apple is caught.

Run it.

### Checkpoint 3 — miss sound

Add `sounds.miss.play()` when the apple reaches the bottom.

Run it.

### Checkpoint 4 — optional music

Only after the first three work, add:

```python
music.play("background")
```

### Minimum success

- supplied images load;
- catching an apple plays one sound;
- missing an apple plays another sound.

The sounds and pictures are supplied with the course, so you do not need to find files on the internet.

## Stretch Challenge: Add a title screen or changing background.

## Bonus Challenge
Make the player change image when moving left/right.


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
A Pygame Zero image is not appearing:
```python
player = Actor("player")

def draw():
    screen.clear()
    player.draw()
```
Assume the file is actually named `hero.png`. Find the bug and fix the code. Then think of one other reason an asset might fail to load.
## Finish by Thinking: Where does Pygame Zero look for images? Why should we keep track of asset licences?

## If you get stuck

**Try this lesson-specific recovery first:**

If an image is missing, the filename in the code must exactly match the file in `images/`. If sound is missing, check `sounds/` and the exact filename. Use the supplied assets rather than downloading random files.

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

## Images, sounds, and assets

A game can use pictures and sounds instead of only shapes. Pygame Zero normally expects images in an `images` folder and sounds in a `sounds` folder inside the project. An `Actor` can use an image by name, and sounds can be played when appropriate.

Keeping assets in the expected folders prevents many file-not-found problems. Also remember that other people's images, music, and sounds may have usage restrictions. Check that you are allowed to use an asset and keep track of its source or licence.

---

[Check your answers and hints](../answers/17-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 16: Collisions, Score, and Text](./16-collisions-score-and-text.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 18: Classes and Objects →](./18-classes-and-objects.md)
<!-- SESSION NAV END -->
