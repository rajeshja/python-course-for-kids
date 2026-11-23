# Session 26: Debugging Like a Pro

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Use VS Code's debugger and a repeatable process to find bugs.

### Use paper to trace the bug
Before changing code, make a small table of the important variables and write what you expect them to contain at each step. Then use breakpoints to check your prediction. This turns debugging into a testable investigation.


**You need from earlier lessons:** Session 23's loop and Session 25's catch-game concepts. You do not need to know the debugger yet.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson26.py`.

**Run it:**
```text
python lesson26.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`traceback`, `breakpoint`, `F5`, `step over`, `step into`, `Variables`, `Watch`, `print debugging`


## The debugger lets you pause time
## The debugger lets you pause time

A debugger lets you stop your program while it is running so you can inspect what is happening.

A **breakpoint** is a stop sign on a line of code.

Start with the simplest possible experiment.

Create:

```python
number = 10
number = number + 5
print(number)
```

Put a breakpoint on the `print(number)` line.

Start the debugger with **F5**.

When the program stops, look at the **Variables** panel. You should see `number` is `15`.

This is the main idea:

> Predict a value → pause → inspect the value → compare it with your prediction.

If F5 does not work, first run the program normally with the Run button. Then return to the breakpoint experiment.

## Debugging process
## Debugging process

Use this order. Do not jump straight to advanced debugger features.

1. Reproduce the problem.
2. Write what you expected.
3. Write what actually happened.
4. Read the traceback.
5. Add a `print()` if you need to inspect a value.
6. Predict the value at a breakpoint.
7. Set one breakpoint.
8. Inspect **Variables**.
9. Use **Step over** to run one line.
10. Fix one thing and test again.

**Step into** and **Watch** are optional until you are comfortable with breakpoints.

## Breakpoints
Click beside a line or use the debugger controls. Start with F5.

At a collision:
```python
if fruit_rect.colliderect(player_rect):
    score += 1
```
Set a breakpoint and inspect:
- player_rect
- fruit_rect
- score

## Step over vs step into
In simple language:
- Step over: run this line and stay in the current code.
- Step into: enter a function call.

## Watch
Watch an important variable such as `score` or `lives`.

## Checkpoint: What should I see?

You should be able to pause at a breakpoint, inspect a variable, step through one or two lines, and explain what changed.

## Your Core Challenge: Complete the Bug Museum exercises. Fix each bug, run the program again, and record what the bug was and how you fixed it.
Do the Bug Museum in this order:

1. Run one bug without changing it.
2. Write the symptom.
3. Identify the line that gives you the clue.
4. Fix it.
5. Run it again.
6. Only then move to the next bug.

For each bug, record:

```text
Symptom:
What I expected:
Clue:
Fix:
What I learned:
```

**Minimum success:** fix three bugs and explain the cause of each.

You do not need to finish all five bugs to complete the lesson.

## Stretch Challenge: Debug your own catch game with one breakpoint.

## Bonus Challenge
Write a bug for a partner. Give only the symptom.

## Bug Hunt

Before you change any bug, use the same seven steps:

1. **Predict:** What do you think will happen?
2. **Run:** Run the broken code.
3. **Look:** What message or symptom do you see?
4. **Find:** Which line is the clue?
5. **Fix:** Change one thing.
6. **Run again:** Did the symptom disappear?
7. **Explain:** What was wrong?

Do one bug at a time. You do not need to solve all five at once.

## Bug Museum
Find and fix all five bugs. For each one, write down the symptom, the cause, and the fix.

**Bug 1 — movement:**
```python
if pygame.K_LEFT:
    player.x -= 5
```

**Bug 2 — collision:**
```python
player_rect = pygame.Rect(100, 100, 50, 50)
fruit_rect = pygame.Rect(400, 100, 50, 50)
# The fruit is drawn at (200, 100), but fruit_rect was never updated.
```
Change the rectangle so it matches the fruit's real position.

**Bug 3 — score resets:**
```python
while running:
    score = 0
    # game code...
```
Move the assignment to the correct place.

**Bug 4 — flicker:**
```python
while running:
    pygame.draw.circle(screen, "red", (200, 200), 30)
    pygame.display.flip()
```
What important drawing step is missing before the new frame?

**Bug 5 — game closes:**
```python
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = True
```
Fix the quit logic.
## Finish by Thinking: Describe one situation where a breakpoint is more useful than repeatedly adding random changes.

## If you get stuck

**Try this lesson-specific recovery first:**

If F5 does not start the debugger, first run the program normally. Then set one breakpoint and start debugging. You can always return to `print()` if the debugger feels too complicated.

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

[Check your answers and hints](../answers/26-answers.md)
