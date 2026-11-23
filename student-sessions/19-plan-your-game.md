<!-- SESSION NAV START -->
[← Previous: Session 18: Classes and Objects](./18-classes-and-objects.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 20: Build and Debug Workshop →](./20-build-and-debug-workshop.md)
<!-- SESSION NAV END -->

# Session 19: Plan Your Game

**Part of:** Module 4 — Structure and Final Project
**Using:** pygame-zero
**Today's mission:** Design a realistic game before building it.


**You need from earlier lessons:** Sessions 14–18. Choose the starter closest to your game instead of starting from a blank file.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson19.py`.

**Run it:** In Mu, select **Pygame Zero** mode and click **Play**.

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`game goal`, `rules`, `win/lose condition`, `core mechanic`, `scope`, `prototype`, `must-have`


## Plan the smallest fun game

The **core mechanic** is the main action the player repeats: catch, avoid, match, explore, and so on. Start with the smallest version that is still a game.

Separate features into must-have, nice-to-have, and stretch ideas. Build the basic loop, player control, main interaction, win/lose rule, and feedback before adding polish. This makes the project much more likely to be finished.
### Use pen and paper
Do not start by coding. Draw the game screen, sketch the player and important objects, and show what happens during one round of play. Write the controls beside the drawing. Your sketch can be messy—the goal is to make your idea clear before you build it.

## Start Here: Describe a favorite game in one sentence. Then think: “What is the smallest version of that game that would still be fun?”

## Game design
## Game design

Three words help you keep a game small:

- **Core mechanic:** the main action the player repeats.
- **Prototype:** the smallest working version that proves the core mechanic.
- **Scope:** how much you promise to build.

Example:

> "Space shooter" is too big.

Make it:

> "Move a ship left and right and catch falling stars."

The prototype only needs the ship, stars, movement, and one way to score.

## One-page plan
## One-page plan

Fill this in on paper before coding:

```text
Game title:
Player does:
Controls:
Things that move:
How I score:
How I lose:
How I know I won:
One thing I will NOT build yet:
```

### Worked example

```text
Game title: Star Catch
Player does: moves a basket
Controls: left and right arrows
Things that move: one falling star
How I score: catch the star
How I lose: miss three stars
How I know I won: reach 10 points
One thing I will NOT build yet: levels
```

This example is intentionally small. Copy its structure, then make your own version.

## Scope rule
If the game cannot be explained in one minute, it may be too large for three sessions.

## Prototype
Start with only:
- one player
- one object
- one interaction

Do not add menus, ten enemy types, or complicated stories before the core mechanic works.

## Checkpoint: What should I see?

Your plan should describe a tiny game that can be made from the skills you already have. The prototype should have one working core action before any polish.

## Your Core Challenge: Write your plan, then build the first working prototype.
Build only the prototype.

### Step 1
Finish the one-page plan.

### Step 2
Choose one existing starter from Sessions 14–18 that is closest to your idea.

### Step 3
Make the player move.

### Step 4
Add **one** object.

### Step 5
Add the core interaction.

### Step 6
Add one visible result, such as a score.

### Step 7
Run the game and test the one core mechanic.

**Minimum success:** the core mechanic works once from start to finish.

Only after that should you add a second object, sound, extra screen, or other polish.

## Stretch Challenge: Add one nice-to-have feature only after the core works.

## Bonus Challenge
Create a second level on paper, but do not let it delay the first playable version.

## Debugging mindset
Plan small tests:
“First I will make the player move.”
“Then I will make one object appear.”
“Then I will make them interact.”

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
This prototype is supposed to increase the score when the player catches the star, but the score never changes:
```python
score = 0

def update():
    if player.colliderect(star):
        score = score + 1
```
Find the problem in the code structure. Then write down one way to fix it in a small Pygame Zero game.
## Finish by Thinking: What is your game's core mechanic? What is one feature you deliberately left out to keep the project finishable?

## If you get stuck

**Try this lesson-specific recovery first:**

If your game plan has more than one main mechanic, remove features until one action is fun and testable. The prototype is the smallest working version, not the finished game.

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

[Check your answers and hints](../answers/19-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 18: Classes and Objects](./18-classes-and-objects.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 20: Build and Debug Workshop →](./20-build-and-debug-workshop.md)
<!-- SESSION NAV END -->
