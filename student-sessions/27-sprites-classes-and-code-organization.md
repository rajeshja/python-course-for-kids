<!-- SESSION NAV START -->
[← Previous: Session 26: Debugging Like a Pro](./26-debugging-like-a-pro.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 28: Project Workshop: Port or Create →](./28-project-workshop-port-or-create.md)
<!-- SESSION NAV END -->

# Session 27: Sprites, Classes, and Code Organization

**Part of:** Module 5 — Level Up with Plain Pygame in VS Code (Optional Extension)
**Using:** pygame
**Today's mission:** Organize a larger pygame project using classes, sprites, groups, and multiple files.

### Plan the structure on paper
Draw boxes for `main.py`, `settings.py`, and any other files you plan to use. Inside each box, write what that file is responsible for. For classes, sketch one Player or Enemy object and label its important data.


**You need from earlier lessons:** Session 18's class/objects idea and Session 23's pygame loop.

## Before you start

**Continue in the `pygame-games` folder from Session 22.**

**Create this file:** `lesson27.py`.

**Run it:**
```text
python lesson27.py
```

Copy the complete starter program and run it before changing anything.

**Expected result:** the first checkpoint below should work before you begin the Core Challenge.

**Paper first:** sketch the window, objects, controls, or state changes you expect to see.

## How to use this lesson

Read a little, then try the code. **Predict → Run → Change → Observe.** Before you press Run, make a guess about what will happen. After it runs, change one small thing and run it again. You do not have to understand everything immediately. If you are stuck, write down what you expected, what actually happened, and what you tried. Then use the answer key for a hint.

## Concepts introduced

`Sprite`, `Group`, `Player`, `Enemy`, `class`, `inheritance`, `super()`, `module`, `import`, `multi-file project`


## Sprites, Groups, and multiple files
## Sprites, Groups, and multiple files

This lesson has several layers. Learn them in order.

1. A normal class.
2. One `pygame.sprite.Sprite`.
3. One `Group`.
4. Multiple sprites.
5. Multiple files.
6. Collision helpers.

Do not refactor your whole game yet.

## Bridge
Reuse the Session 18 idea: a class is a blueprint. Now pygame provides a `Sprite` class that can help organize game objects.

## Player class
## Player class

A `pygame.sprite.Sprite` is a special kind of class designed to work with pygame's sprite tools.

Start with this complete example:

```python
import pygame

class Player(pygame.sprite.Sprite):
    def __init__(self, x, y):
        super().__init__()

        self.image = pygame.Surface((50, 50))
        self.image.fill("blue")

        self.rect = self.image.get_rect(topleft=(x, y))

player = Player(100, 100)
```

### What is `super().__init__()`?

For now, think of it as:

> "Run the setup that the parent Sprite class provides."

You do not need to write your own version of it.

The important Sprite rule for this lesson is:

> A drawable Sprite needs an `image` and a `rect`.

Run a one-player version before adding groups.

## Group
## Group

A `Group` is a collection of sprites.

```python
player = Player(100, 100)
players = pygame.sprite.Group(player)
```

Later, if you have several enemies, one group can contain all of them.

`players.update()` asks the sprites in the group to update.

`players.draw(screen)` asks pygame to draw the sprites. This works because each Sprite has an `image` and a `rect`.

Do not add enemies until the single-player version works.

## Enemy
Create an Enemy class with its own update behavior.

## Collision helpers
## Collision helpers

Once you have a player and an enemy group, pygame can check collisions for you:

```python
hits = pygame.sprite.spritecollide(player, enemies, True)
```

The last `True` means:

> "Remove an enemy from the group when it is hit."

Try `False` instead to see the difference.

Do not worry about every detail of the function yet. The important idea is that pygame can check a group of sprites for you.

## Multi-file structure
## Multi-file structure

Only split the project after the single-file version works.

Start with:

```text
my-game/
├── main.py
└── player.py
```

In `player.py`:

```python
import pygame

class Player(pygame.sprite.Sprite):
    def __init__(self, x, y):
        super().__init__()
        self.image = pygame.Surface((50, 50))
        self.image.fill("blue")
        self.rect = self.image.get_rect(topleft=(x, y))
```

In `main.py`:

```python
import pygame
from player import Player
```

`from player import Player` means:

> "Open `player.py` and let this file use the `Player` class."

Keep both files in the same folder.

## Checkpoint: What should I see?

One `Player` sprite should update and draw correctly before you add groups, enemies, or extra files.

## Your Core Challenge: Refactor the catch game so the player and falling objects use classes.
Do not refactor the whole catch game at once.

### Minimum path

1. Make a `Player` Sprite with a blue square.
2. Run it.
3. Make one `Fruit` Sprite.
4. Run it.
5. Put the player in a Group.
6. Add one enemy group only after the single sprites work.
7. Move the class definitions into separate files only after the one-file version works.
8. Use `pygame.sprite.spritecollide()` last.

**Minimum success:** one Player Sprite and one Fruit Sprite work in a pygame loop.

The goal is to understand the organization. You do not need a large finished game in this lesson.

## Stretch Challenge: Move settings into `settings.py`.

## Bonus Challenge
Create a second enemy class.

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
This class should remember the player's starting position:
```python
class Player:
    def __init__(x, y):
        self.x = x
        self.y = y

player = Player(100, 200)
```
Run it. Find the missing parameter and fix the constructor.
## Finish by Thinking: Why might a game use a Group instead of managing every enemy with a separate variable?

## If you get stuck

**Try this lesson-specific recovery first:**

If `Group.draw()` fails, check that every Sprite has both an `image` and a `rect`. If an import fails, check the filename and the `from player import Player` line.

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

[Check your answers and hints](../answers/27-answers.md)

<!-- SESSION NAV START -->
[← Previous: Session 26: Debugging Like a Pro](./26-debugging-like-a-pro.md) &nbsp;&nbsp;|&nbsp;&nbsp; [Next: Session 28: Project Workshop: Port or Create →](./28-project-workshop-port-or-create.md)
<!-- SESSION NAV END -->
