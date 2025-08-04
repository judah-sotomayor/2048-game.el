# 2048-game.el #
**All credit to ZCK's original implementation: https://hg.sr.ht/~zck/game-2048**

I have enhanced it with a persistent game history file, allowing you to continue your attempts at reaching 2048 on separate days.

### Installing 2048-game.el ###
Original install instructions can be found in zck's repo.
To add to Doom emacs, use the following:

packages.el:
``` emacs-lisp
(package! 2048-game
  :recipe (:host github :repo "judah-sotomayor/2048-game.el"))
```

config.el:
``` emacs-lisp
(use-package! 2048-game)
```

### Playing ###

* The goal is to create a tile with value 2048.
* Start the game by typing `M-x 2048-game`, and pressing enter.
* You can move the tiles around with the arrow keys, p/n/b/f, or C-p/C-n/C-b/C-f.
* Whenever the board moves, all tiles slide as far to that direction as they can go. If a tile collides with another tile of the same value, the tiles combine into a  tile with double the initial value, and you gain the new tile's value as your score.
