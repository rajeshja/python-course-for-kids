<!-- SESSION NAV START -->
[← Previous: Session 19: Plan Your Game](./19-plan-your-game.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 21: Showcase and Celebration →](./21-showcase-and-celebration.md)
<!-- SESSION NAV END -->

# Session 20: Build and Debug Workshop

**Part of:** Module 4 — Structure and Final Project
**Using:** pygame-zero
**Today's mission:** Develop a game in small steps and use a repeatable debugging process.


**You need from earlier lessons:** Session 19's one-page plan and prototype. Keep working in the same Pygame Zero project.

## Before you start

**Continue in the Pygame Zero project from Session 13.**

**Create this file:** `lesson20.py`.

**Run it:** In Mu, select **Pygame Zero** mode and click **Play**.

Do not start by inventing a new project. Copy the complete starter program in this lesson first and make sure it runs.

**Expected result:** you should see the result described in the first checkpoint before you start the Core Challenge.

**Paper first:** sketch the screen and predict where objects will be before you press Run.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`debugging`, `traceback`, `print`, `version`, `peer play-test`


## Debugging: investigate instead of guessing

A bug is a problem in a program. Debugging means finding its cause. A useful process is: reproduce the problem, describe expected versus actual behaviour, make a guess, check the relevant code or values, change one thing, run again, and retest.

Error messages often contain useful clues. A line number tells you where Python noticed the problem, although the cause can sometimes be just before that line. If the program runs but behaves incorrectly, inspect the values, conditions, positions, and order of operations.

Changing many things at once makes debugging harder because you cannot tell which change mattered.
### Use paper while debugging
When something goes wrong, write down **what I expected** and **what actually happened**. For movement bugs, sketch the expected path. For score or lives bugs, write the expected values after each step. These notes can make the bug much easier to find.

## Start Here: Bug Hunt
Start with the broken program below. Predict what will go wrong before you run it, then run it and fix the problem.

## Debugging process
Use this debugging routine:
1. Reproduce the problem.
2. State what you expected.
3. State what actually happened.
4. Read the error from the bottom up.
5. Check the most recent change.
6. Add a `print()` if useful.
7. Change one thing.
8. Test again.

If you need help, you can say:
> “I expected ____. It did ____. I tried ____.”

## Build workshop
## Build workshop

Work in the same Pygame Zero project as Sessions 19–21.

Use this cycle:

1. Choose one tiny feature.
2. Predict what should happen.
3. Add only that feature.
4. Run the game.
5. Test the feature.
6. If it fails, use the Bug Hunt routine.
7. Save a working copy before starting the next feature.

### Show one real traceback

Deliberately introduce a tiny error such as:

```python
print("hello"
```

Run it.

Look at the last part of the traceback. Python should tell you that it reached the end of the line while it was still expecting something.

Fix the missing `)` and run again.

This is what "read the error" means: use the message as a clue.

## Version safety
Save versions such as:
`game_v1.py`, `game_v2.py`, or use copied project folders. A working older version is better than losing everything.

## Optional: Peer play-test

If someone is available, let them try one feature. If you are working alone, test the feature yourself three times and write down anything surprising.

Halfway through:
- player gives two likes
- player gives one useful suggestion
- developer watches without defending the design

## Checkpoint: What should I see?

The sample bug should produce a traceback first. After the fix, the same program should run successfully.

## Your Core Challenge: A playable game with its core loop working.

## Stretch Challenge: One carefully chosen extra feature.

## Bonus Challenge
Improve instructions, feedback, sound, or visual polish.

## A useful debugging questions
- “What line changes the value?”
- “Can we print the value just before the bug?”
- “What is the smallest version that shows the problem?”
- “What changed immediately before it broke?”

## Bug Hunt
## Bug Hunt

Use the same Pygame Zero technology as your project.

```python
WIDTH = 800

def draw():
    screen.draw.text("Hello", (20, 20)
```

Do the seven-step Bug Hunt routine.

**Expected result:** the first run gives you a syntax error. After adding the missing `)`, the program should open and show `Hello`.

## Finish by Thinking: Describe one bug you solved using the eight-step debugging process.

## If you get stuck

**Try this lesson-specific recovery first:**

If the traceback looks scary, find the last line first. It usually tells you the type of error and the line where Python noticed it. Fix one clue at a time.

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

[Check your answers and hints](../answers/20-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 19: Plan Your Game](./19-plan-your-game.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 21: Showcase and Celebration →](./21-showcase-and-celebration.md)
<!-- SESSION NAV END -->
