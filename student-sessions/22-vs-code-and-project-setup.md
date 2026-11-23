<!-- SESSION NAV START -->
[← Previous: Session 21: Showcase and Celebration](./21-showcase-and-celebration.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 23: Hello Pygame: Write the Game Loop →](./23-hello-pygame-write-the-game-loop.md)
<!-- SESSION NAV END -->

# Session 22: VS Code and Project Setup

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Become comfortable with VS Code, a project folder, the terminal, and pygame installation.

### Plan your project folder on paper
Draw a simple box for your project folder and write the files you expect to create inside it. This gives you a map of your project before you start adding code.


## Before you start — one-time VS Code setup

This lesson is the setup lesson for Sessions 22–29. Follow it in order. You do **not** need to understand every term yet.

### 1. Install Python

Install Python on your computer using the Python installer supplied with the course or your normal trusted software source.

When the installer offers an option to add Python to your PATH, turn that option on.

Open a new terminal and test:

```text
python --version
```

You should see a Python version number. If `python` is not recognized, stop here and use the **Python not found** recovery box later in this lesson.

### 2. Install VS Code

Open VS Code and install the **Python** extension from the Extensions view.

### 3. Create the course project folder

Create a folder named:

```text
pygame-games
```

In VS Code choose **File → Open Folder** and select `pygame-games`.

### 4. Choose the Python interpreter

Open the Command Palette and choose:

```text
Python: Select Interpreter
```

Choose the Python installation you just tested.

An **interpreter** is the program that reads your Python code and runs it. VS Code and the terminal need to use the same interpreter.

### 5. Open the terminal

In VS Code choose **Terminal → New Terminal**.

Test Python again:

```text
python --version
```

### 6. Install pygame

In that same terminal run:

```text
python -m pip install pygame
```

`pip` is Python's package installer. `python -m pip` tells the Python interpreter you selected to run pip, which helps avoid installing pygame into a different Python by accident.

You should see a successful installation message.

### 7. Test pygame

Create:

```text
test_pygame.py
```

Put this in it:

```python
import pygame

print("Pygame is installed!")
print("Pygame version:", pygame.version.ver)
```

Save it and run:

```text
python test_pygame.py
```

You should see the two messages in the terminal.

**Do not continue until this test works.**

### If something goes wrong

- **`python` is not recognized:** close and reopen VS Code after installing Python. If it still fails, check that Python was added to PATH.
- **`No module named pygame`:** run `python -m pip install pygame` in the VS Code terminal, then check the selected interpreter again.
- **VS Code shows one Python but the terminal uses another:** run `python --version` in the terminal, then use **Python: Select Interpreter** to choose that same installation.

### After setup

Sessions 23–29 use:

```text
python your_file_name.py
```

from the VS Code terminal.

**Expected result:** `test_pygame.py` prints the installation message without an error.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`VS Code`, `Python extension`, `interpreter`, `terminal`, `pip`, `project folder`

## Scavenger hunt
Find:
- Explorer
- editor
- terminal
- Run button
- Problems panel
- Command Palette

Change the font size or theme. Then write down one shortcut you would teach someone else.

## Open a project
Create:
```text
pygame-games/
```
Open the **folder**, not just a single file.

## Interpreter
Use Command Palette → `Python: Select Interpreter`. Notice that VS Code must use the same Python where pygame is installed.

## Terminal
Run:
```text
python --version
```
Then:
```text
python -m pip install pygame
```

Test:
```python
import pygame
print("Pygame is ready!")
```

Run:
```text
python test_pygame.py
```

## Deliberate bug
Remove a colon:
```python
if True
    print("hello")
```
Use the Problems panel and traceback.

## Checkpoint: What should I see?

`test_pygame.py` should print `Pygame is installed!` and a pygame version number with no error.

## Your Core Challenge: Open a Session 5 Turtle program in VS Code and run it. Then create and run the pygame import test.

## Stretch Challenge: Write down the steps for selecting the interpreter so another person could follow them.

## Bonus Challenge
Explore a keyboard shortcut and document it.

## Common problem
If `pygame` is not found, check the selected interpreter before reinstalling anything.

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
The following code should run after you install pygame, but it has a syntax bug:
```python
import pygame

if True
    print("Pygame is installed")
```
Run it. Find the error, fix it, and run the test again.
## Finish by Thinking: Why is opening the whole project folder useful? What does the Python interpreter setting control?

## If you get stuck

**Try this lesson-specific recovery first:**

If `pygame` cannot be imported, run `python -m pip install pygame` in the VS Code terminal and check **Python: Select Interpreter**. If Python itself is not found, fix Python before pygame.

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

## What VS Code, Python, and pygame each do

VS Code is the **editor** where you write and organize code. Python is the language and interpreter that runs the code. The terminal is where you can type commands. A Python extension adds helpful editing and debugging features.

The **project folder** contains your game and its assets. Opening the whole folder helps VS Code understand the project structure. The **Python interpreter** is the Python environment VS Code uses to run your program.

Installing `pygame` makes that package available to the Python environment. If VS Code cannot import a package that appears installed, check that the editor and terminal are using the same environment.

---

[Check your answers and hints](../answers/22-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 21: Showcase and Celebration](./21-showcase-and-celebration.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 23: Hello Pygame: Write the Game Loop →](./23-hello-pygame-write-the-game-loop.md)
<!-- SESSION NAV END -->
