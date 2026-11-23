# Answer Key: Session 25: Images, Text, Sound, and Collisions

Try the questions yourself first. Use this page only when you want to check your thinking.

### Question 1

`blit()` draws an image onto the screen.

### Question 2

`colliderect()` checks whether two rectangles overlap and returns true or false.


## Core Challenge Rescue Path

Try the challenge yourself before reading these.

### Hint 1

Check the supplied `assets/` folder first.

### Hint 2

Test `blit()`, collision, text, and sound separately.

### Worked example / minimal reference

The six checkpoints form the complete minimal catch-game build. Finish them in order rather than porting the whole Pygame Zero game.

If your program is still broken, create a **fresh file**, copy the complete starter or checkpoint program from the lesson, and run it unchanged. Then compare your version with the known-good version one checkpoint at a time. This gives you a working reference without requiring you to guess which missing line to invent.

### Bug Hunt

`colliderect()` is a method of `pygame.Rect`. Give both objects Rects and compare those, for example `if player_rect.colliderect(coin_rect):`.

---

[Back to the lesson](../student-sessions/25-images-text-sound-and-collisions.md)
