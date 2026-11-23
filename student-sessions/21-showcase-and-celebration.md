# Session 21: Showcase and Celebration

**Part of:** Module 4 — Structure and Final Project
**Using:** pygame-zero
**Today's mission:** Share a finished game and reflect on the programming journey.


**You need from earlier lessons:** Your working project from Sessions 19–20. A solo student can complete this lesson.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson21.py`.

**Run it:** from the project folder, run:

```text
pgzrun lesson21.py
```

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`presentation`, `feedback`, `reflection`, `iteration`


## Explaining your work is part of programming

A showcase is an opportunity to explain your design, your code, and a bug you solved. Try to explain the idea rather than simply reading code aloud.

When giving feedback, be specific: say what was clear, what was confusing, and what you think could improve. Finished projects do not need to be perfect. Programming is iterative: you build, test, learn, and improve.
### Plan your explanation on paper
Before presenting, jot down three things: what the player does, one interesting piece of code, and one bug you solved. A tiny sketch of your game screen can also help you explain your design.

## Start Here: Prepare a 30-second introduction:
“My game is called ____. You ____. The hardest part was ____.”

## Final polish
Before the fair, check:
- game instructions visible
- controls clear
- game-over/win behavior
- sound not too loud
- no obvious error on launch
- project saved in the correct folder

## Game fair
## Game fair — optional group activity

If other people are available, you can demonstrate your game to them.

### Solo option

You can complete the course without a game fair:

1. Run your game.
2. Test the controls.
3. Test the win/lose condition.
4. Take a screenshot or short recording.
5. Write the three reflection answers.
6. Compare your project with the rubric.

You do not need another player, a shared folder, or a live presentation.

## Reflection
- My favorite concept was...
- The hardest bug was...
- I learned that programming...
- Next I want to make...

## Final rubric
## Checkpoint: What should I see?

Your project should launch, the controls should work, the main action should work, and the quit path should work. If you are working alone, the self-check below is enough.

## Final self-check

Give yourself one point for each statement that is true:

- [ ] My game launches.
- [ ] I can explain the controls.
- [ ] The main game action works.
- [ ] The game can be won, lost, or otherwise finished.
- [ ] I fixed at least one bug.
- [ ] I can point to a loop in my code.
- [ ] I can point to a function.
- [ ] I can explain one variable.
- [ ] I can explain one `if` statement.
- [ ] I can explain what I would improve next.

**8–10 points:** you are ready for the optional plain-pygame module.

**5–7 points:** replay the lessons whose ideas you cannot explain yet.

**0–4 points:** return to the Turtle projects and rebuild one small project before moving on.

## Celebration
Certificates and a shared folder/page of projects.

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
Before showing a game to anyone, test this common mistake:
```python
score = 0

def add_point():
    score = score + 1

add_point()
print(score)
```
Run it. Find the bug and fix it. This is a good reminder that a game should be tested before its showcase.
## Finish by Thinking: What is one thing you can build now that you could not build before this course?

## If you get stuck

**Try this lesson-specific recovery first:**

If you are alone, use the Solo option: record a short demo or simply run the final checklist and write the reflection answers. No partner is required.

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

[Check your answers and hints](../answers/21-answers.md)
