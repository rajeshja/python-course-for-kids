# Session 29: Pygame Showcase and Next Steps

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Share a finished plain-Pygame project and understand where to go next.

### Prepare on paper
Before the showcase, write three short notes: what your game does, one bug you solved, and one thing you would improve next. A quick screen sketch can help you explain how the game works.


**You need from earlier lessons:** Your working Session 28 project.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson29.py`.

**Run it:**
```text
python lesson29.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`showcase`, `debugger`, `comparison`, `reflection`, `next steps`

## Checkpoint: What should I see?

Your final project should launch, play, and quit. You should also be able to complete the independent skills test and explain one bug you fixed.

## Final checks
Verify:
- the game launches
- the game can be played
- the quit path works
- controls are visible
- no missing assets
- the project folder is saved
- one backup exists

## Game fair
## Game fair — optional

If other people are available, show them your game.

### Solo alternative

You can finish this lesson alone:

1. Record a 30–60 second demo, or take screenshots.
2. Run the final self-test below.
3. Write the reflection answers.
4. Write one thing you would improve next.

No shared folder, website, or audience is required.

## Comparison
Discuss:
- Pygame Zero hides the game loop; pygame exposes it.
- Pygame Zero gives `draw()` and `update()`; pygame lets you decide how to organize the loop.
- Both use the same underlying ideas: events, state, drawing, movement, collision, images, and sound.

## Reflection
Write down your answers before checking the answer key:
- What did Pygame Zero make easier?
- What does plain pygame make possible?
- Which debugging tool helped you most?
- What would you change if you had two more sessions?
- What will you build next?

## Final extension rubric
## Final independent skills test

Try these without copying a previous solution:

1. Create a Python file and run it.
2. Use a variable to store a number.
3. Write a loop that repeats something five times.
4. Write a function and call it.
5. Use an `if` statement to make a decision.
6. Draw one shape with pygame.
7. Keep a pygame window open and close it cleanly.
8. Move a rectangle with the keyboard.
9. Detect whether two rectangles overlap.
10. Find and fix one small bug using a traceback or `print()`.

If you can complete **8 out of 10**, you have a strong foundation for your next project.

If fewer than 8 work, return to the matching earlier lesson and rebuild that one skill.

## Celebration
Award extension certificates and collect projects into a shared folder/page.

## Next steps
## Next steps

Pick **one** concrete next project instead of trying to learn everything at once.

Good choices:

- add a second level to your game;
- add a new enemy;
- make a simple Pong game;
- make a maze;
- make a reaction-time game;
- draw a simulation.

If you want to explore another Python library, first find a beginner project for that library and learn only the pieces you need.

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
Your final game should be tested before the showcase. Here is a small bug to find:
```python
score = 0

for i in range(5):
    score += 1
    score = 0

print(score)
```
Predict the output, run it, then fix the program so the final score is `5`. Explain why the original version kept losing the score.
## Finish by Thinking: Write one sentence completing:
**“I used to think programming was ____. Now I think programming is ____.”**

## If you get stuck

**Try this lesson-specific recovery first:**

If the showcase is not available, use the solo checklist and record your own demo. For the next step, choose one concrete project instead of trying to learn every Python library at once.

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

## What you learned about Pygame Zero and pygame

Pygame Zero gives you helpful structures such as `draw()`, `update()`, and `Actor`. Plain pygame exposes more of the machinery: you write the loop, handle events, update state, draw, and refresh the display yourself.

The underlying programming ideas are the same: events, state, movement, drawing, collision, images, sound, loops, conditions, functions, and classes. The big step is that you can now use those ideas with more than one tool.

---

[Check your answers and hints](../answers/29-answers.md)
