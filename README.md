# Minesweeper NoJS
### HTML+CSS Minesweeper game without JavaScript
This is not "program" but only layout.

You can play it on GitHub Pages:
https://valent-in.github.io/mines-no-js/

This game was written in July 2018 as learning project.

It is not "true" Minesweeper!
Not all functions from original game implemented due to CSS limitations:

* Only 5600 different placement patterns can be generated by it's "randomizer".
* Only one board (8x8) is available.
* Lack of right mouse click.
* No timer and leaderboard.


### Gameplay
> The objective of the game is to clear a rectangular board containing hidden "mines" or bombs without detonating any of them, with help from clues about the number of neighboring mines in each field. (From Wikipedia)

#### Player must meet one of this conditions to win game:
* All free fields are opened.
* All 10 flags are set correctly.

#### Fail conditions:
* Opened field with mine.
* All 10 flags are set but some are in wrong places.

Flags can be set on top left corner of every field (default mode). Alternatively mode can be switched to "open only" or "flags only".

### Underhood
This is completely static page (not server-generated). 

Most of internal mechanisms built on CSS counters. Arithmetic operations not allowed for counters, so all "calculations" are performing by "simple counting".
CSS property :indeterminate is used for user input expansion (creating 2 mines by single click, auto-open emty areas).
HTML element Form allows resetting game without page reload.

Documents in folder "generators" were used for creation of some parts of HTML and CSS. Generated parts of HTML are marked in comments. Generated CSS files are marked in names. 

Source of ideas (greatly explained):
https://css-tricks.com/roman-empire-made-pure-css-connect-4-possible/
