<!-- SESSION NAV START -->
[← Previous: Session 27: Sprites, Classes, and Code Organization](./27-sprites-classes-and-code-organization.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 29: Pygame Showcase and Next Steps →](./29-pygame-showcase-and-next-steps.md)
<!-- SESSION NAV END -->

# Session 28: Project Workshop: Port or Create

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Apply plain pygame skills to a complete project.

### Plan on paper before coding
Complete your one-page game plan and draw at least one screen. Show the player, important objects, controls, and one example of winning or losing. Use the drawing to decide what to build first.


**You need from earlier lessons:** Sessions 23–27. The state-machine starter in this lesson is the minimum path, so you do not have to port a whole earlier game.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson28.py`.

**Run it:**
```text
python lesson28.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`project planning`, `game loop`, `game states`, `prototype`, `high score`

## Choose a project
## Choose a project

Use the supplied state-machine starter above as the foundation.

### Option A — easiest: Catch Game

Add your Session 25 catch-game idea inside the `playing` state.

### Option B — Dodger

Move a player rectangle left and right while objects fall.

### Option C — Your own game

Only choose this if you can describe the game in one sentence and draw its minimum version on paper.

Do not start from a blank file. Start from the working state example.

## One-page plan
Include:
- title
- goal
- controls
- rules
- win condition
- lose condition
- core mechanic
- screen sketch
- must-have features
- nice-to-have features
- stretch features
- development steps

## Build order
## Build order

Complete one checkpoint at a time:

1. [ ] title state works
2. [ ] Space changes to playing
3. [ ] player appears
4. [ ] player moves
5. [ ] one game object appears
6. [ ] the main interaction works
7. [ ] score or feedback appears
8. [ ] game-over state works
9. [ ] quit works

Run after every checkpoint.

**Minimum success:** the title → playing → game-over path works, even if the game is very simple.

## Game states
## Game states

A **game state** is the current mode of the game.

Use three simple states:

```python
state = "title"
```

The three states are:

- `title` — waiting to start;
- `playing` — the game is active;
- `game_over` — the game has finished.

Here is a complete tiny state example:

```python
import pygame

pygame.init()
screen = pygame.display.set_mode((800, 600))
clock = pygame.time.Clock()

state = "title"
running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

        if state == "title" and event.type == pygame.KEYDOWN:
            if event.key == pygame.K_SPACE:
                state = "playing"

    screen.fill("navy")

    if state == "title":
        pygame.draw.circle(screen, "yellow", (400, 300), 50)
    elif state == "playing":
        pygame.draw.rect(screen, "green", (350, 250, 100, 100))
    elif state == "game_over":
        pygame.draw.line(screen, "red", (300, 250), (500, 350), 8)

    pygame.display.flip()
    clock.tick(60)

pygame.quit()
```

Run this complete example before changing it.

**Expected result:** you see the title picture. Press Space and the playing picture appears.

## Optional high score
If the group is ready, save a single high score to a text file. Treat file persistence as optional.

## Optional: Peer play-test

If someone is available, let them play. Otherwise use the Solo testing steps in the Core Challenge.

If someone else is playing, let them describe anything confusing before you explain it. If you are alone, write down one thing that felt confusing while you tested the game.

## Checkpoint: What should I see?

The starter project should reach its title state, start playing when the chosen key is pressed, and reach game over. You then add your own game idea one small piece at a time.

## Your Core Challenge: Finish a playable game with a working loop, input, and interaction.
Use the state-machine starter.

### Required

- title state
- playing state
- one player control
- one game interaction
- one visible result
- game-over state
- quit button

### Solo testing

Test your game yourself:

1. Start it.
2. Try the controls.
3. Try to trigger the main interaction.
4. Try to reach game over.
5. Quit.
6. Write down anything surprising.

**Minimum success:** a tiny game that can be started, played, finished, and closed.

Do not add file saving yet. High scores are an optional future lesson.

## Stretch Challenge: Add a second game state or a simple difficulty increase.

## Bonus Challenge
Add a high score or second level.

## Backup
Make a copy of the project folder before major changes.

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
A game should show the title screen until the player presses Space, but this code switches immediately:
```python
game_state = "title"

if game_state == "title":
    game_state = "playing"

print(game_state)
```
Find the logic problem. Rewrite it so the state changes only when a Space-key event is received.
## Finish by Thinking: What is the smallest playable version of your game? Is it working yet?

## If you get stuck

**Try this lesson-specific recovery first:**

If the project becomes too large, go back to the starter and get the title → playing → game-over path working first. Add only one game feature per checkpoint.

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

## Game states and prototypes

A game can have states such as `title`, `playing`, and `game_over`. A simple variable can record the current state, and `if`/`elif` chooses what the game should do in that state.

Build a **prototype** first: a small working version proving that the main idea works. Add the player, central interaction, and win/lose rule before optional polish. A finished small game is better than an ambitious game that never becomes playable.

---

[Check your answers and hints](../answers/28-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 27: Sprites, Classes, and Code Organization](./27-sprites-classes-and-code-organization.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 29: Pygame Showcase and Next Steps →](./29-pygame-showcase-and-next-steps.md)
<!-- SESSION NAV END -->
