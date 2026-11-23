# Session 11: Turtle Project and Checkpoint

**Part of:** Module 2 — Building Blocks
**Using:** turtle
**Today's mission:** Apply the first ten sessions in a creative project and demonstrate core skills.


## Before you start

**Create this file:** `lesson11.py` in your course practice folder.

If you are using VS Code, open the course practice folder first. If you are using another Python editor, create the file there.

**Run it:** run `lesson11.py` with Python.

If the previous lesson left a Turtle window open, close that window before running this lesson.

**Paper first:** before each drawing change, sketch or predict the turtle's path on paper.

**Expected result:** the lesson's first complete example should run without you adding any missing code. If it does not, stop and use the troubleshooting section before starting the challenge.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`planning`, `decomposition`, `testing`, `comments`, `checkpoint`


## Combining your programming tools

You now have several building blocks: sequences, loops, variables, functions, lists, conditionals, and recursion. A project does not need all of them. Choose the ones that make your drawing interesting.

Before coding, decide what you want to draw, what repeats, which values should be easy to change, and whether a function or other concept will make the program clearer. A short program you understand is more valuable than a long program you cannot explain.
### Plan on paper first
Before opening the editor, sketch your final drawing. Mark where the main shapes go, which parts repeat, and which numbers you may want to change. Circle any part that could become a function. Keep the sketch beside you while you code.

## Start Here: Quick solo quiz

On paper, write one short example of each:

- sequence
- loop
- variable
- function
- list
- conditional
- recursion

If you cannot think of one, look back at the matching lesson before starting the project.


## Project briefing
## Project briefing

You can choose one of these three projects. Start with **A** if you want the easiest path.

### A — Pattern Poster (easiest)

Draw a repeating pattern using a loop, variable, and function.

### B — Village Scene

Draw three houses using a function with a size parameter. Add trees or clouds if you want.

### C — Magic Garden (harder)

Draw a garden that uses randomness and at least one conditional.

Each project has a small minimum version. You can add your own ideas only after the minimum version works.

## Planning
A good plan names small parts:
- background
- repeated shape
- colors
- movement/position
- function names
- special effects

Add comments only when they explain *why* you chose something, not when they simply repeat what the code already says.

## Build It Step by Step
## Build It Step by Step

Use this checklist for your chosen project.

1. Create a new file called `lesson11_project.py`.
2. Copy one complete drawing program from an earlier lesson.
3. Run it before changing anything.
4. Add **one loop** and run it.
5. Add **one variable** and run it.
6. Put a repeated drawing into **one function** and run it.
7. Add the project's required extra idea:
   - A: none — your loop is enough.
   - B: a parameter such as `size`.
   - C: a list or conditional.
8. Run after every step.
9. Add decoration only after the minimum version works.

### Checkpoint

Put a tick beside each requirement in the code:

- [ ] sequence of instructions
- [ ] loop
- [ ] variable
- [ ] function
- [ ] one extra idea from the list above

**Minimum success:** all five boxes can be pointed to in your code.

## Core checkpoint
A project must demonstrate:
- a sequence
- a loop
- a variable
- a function
- at least one of: list, conditional, recursion

## Checkpoint: What should I see?

Your project must open, draw something, and include the required programming ideas listed in the checkpoint. You should be able to point to where each idea is used.

## Your Core Challenge: Finish a shareable artwork or interactive helper.

## Stretch Challenge: Add a second technique from an earlier session.

## Bonus Challenge
Make the artwork different each time it runs.

## Debugging checklist
- Does the program run?
- Is the error message readable?
- What did I expect?
- What happened?
- What changed most recently?
- Can I test a smaller version?

## Show What You Made
## Show What You Made

### Solo option

You do not need an audience.

1. Run the project.
2. Take a screenshot.
3. Write two sentences explaining what it does.
4. Write one sentence about the programming idea you are most proud of.

If another person is available, you may show them instead, but this is optional.

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
A project function is meant to draw a square, but the program has a small bug:
```python
import turtle

def draw_square(size):
    for i in range(4):
        turtle.forward(size)
        turtle.right(80)

draw_square(100)
```
Run it. The result should be a square. Find the incorrect value and fix it. Then choose a different size.
## Finish by Thinking: Which programming idea is easiest for you now? Which needs more practice?

## If you get stuck

**Try this lesson-specific recovery first:**

If the project feels too large, return to the minimum checkpoint. You only need one working artwork plus the required programming ideas; stretch features can wait.

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

[Check your answers and hints](../answers/11-answers.md)
