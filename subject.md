# TP BONUS : THE GAME

## README

Write two small C console games.

## AUTHORS

* SidoShiro
* Felix Léon

## Mails

Use: [ASM][BONUS]

marc.sidorenko@epita.fr
felix.leon@epita.fr

## COPYRIGHT

This subject is our own creation and is not associated with any other
intellectual content. This subject is public and free to use. Therefore it is
not allowed to sell this intellectual content.

# Summary

Hello!

Soon it's holidays, and for most of you the exchange semester. This subject is
written in English as a little training before your fantastic trip.

You have to make a game, choosing one of these (or doing both of them):
  * Tetris-like game
  * 2048-like game

# Rules of submission

You need to follow this architecture of submission, in our school git.

```
game_bonus/
|
|__________AUTHORS
|
|__________README
|
|__________TODO
|
|__________Makefile
|
|__________src_tetris/
|          |
|          |_______*.c   // Meaning all your .c files
|
|__________src_twothousantfortyeight/
|          |
|          |_______*.c   // ... same
|
|__________include/
           |
           |_______*.h  // Meaning all your .h files
```

Here a **begining** of a Makefile in order to have a good start.

```Makefile
CC = gcc
CFLAGS = -std=c99 -pedantic -Wextra -Wall -Werror -Iinclude
SRC_TETRIS = # put the tetris .c files here
SRC_TTFE = # put the twothousantfortyeight .c files here

all: # put here tetris or/and twothousandfortyeight

tetris:
          $(CC) $(CFLAGS) $(SRC) -o tetris

twothousandfortyeight:
          $(CC) $(CFLAGS) $(SRC) -o twothousandfortyeight

clean:
          $(RM) *.o tetris twothousantfortyeight
```

> /!\ You can choose to do *tetris* or/and *2048* (of course if you do the two games correctly your grade will be the best

# The Two Games

## Tetris

Make a console mode tetris game. The game should take place in a 20x10 array of
blocks. Border should be printed by a special ascii symbol of your choice.

> Fill carefully your README: explain how to *make*, *execute* and *play* the game.

**Core Features**

* Handle collisions
* Have at least the square of 4 blocks
* Handle lose
* Handle the line removal if a full line of blocks is completed

**Advance Features**

* 5 types of piece
  * square of 4 blocks
  * bar of 4 blocks
  * T of 4 blocks
  * L of 5 blocks
  * S of 4 blocks

```
square:

  ##
  ##

bar:

####

T:

 #
###

S:

 ##
##
```

* Handle score - write in README the points computation used
* Handle piece rotation
* Handle randomness of piece spawning

**Advance+ Features**

* Main Menu (Play, See Scores, Exit)
* Score board, may write a file tetris.score in the current directory of the binary
* Add more pieces
* Colors

## 2048


