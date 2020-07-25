# Hexagonal Chess

The game description files in this directory describes several variants of Hexagonal Chess (i.e., chess played on a board made up of hexagonal spaces.) Specifically, those variants are:
* Glinski Chess (the most popular version) 
* Brusky Chess
* De Vasa Chess
* McCooey Chess
* Mini Hexchess
* Shafran Chess
* Starchess
* Wellisch Chess (a 3-player variant)

Most of the variants above are playable with Ludii v0.9.4, except for Wellisch Chess, which I've updated to v1.0.0. (Ludii v1.0.0 was released on 2020-07-24, and has changed the board coordinates used in the last couple updates.)

Each of these variants has associated rules that can be viewed through the Ludii General Game System ("the app").

## How to Play
Currently, the following steps are needed to run play the variations of hexagonal chess found in this directory:
* From https://ludii.games/download.php, download the Ludii player (Ludii.jar, currently at v1.0.0) to an empty directory.
* The Ludii User Guide and the Ludii Language Reference can optionally be downloaded from the same website. There is also a tutorial available.
* On a computer with Java (v8 or higher), start the play by running the command
      java -jar Ludii.jar
* If your computer does not hava Java (v8 or higher) installed, there is a link on the same download page to a website (https://www.java.com/en/download/) where you can install Java.
* From within the player, select the menu item File, then Load Game from File. 
* The Ludii General Game System supports playing games online with other players, but this appears
  to be limited to those games already integrated into the system. The online play of games loaded from files
  is not supported.

## Ludii Potential Feature Improvements
Ludii system (v1.0.0) feature requests:
* **Relative direction enums for hexagonal boards.**
  Relative direction enums for hexagon and rhombus board shapes.
* **Optional whitespace between argument label and argument.**  The Ludii language seems to not constrain a game
  file's use of whitespace. However, whitespace introduced between an argument label (e.g., if: ifAfterwards: to: size:
  stack:) and the argument triggers a syntax error, without identifying the source of the error.
* **A means of unit testing.** For example, a means of supporting tests with a setup that creates a games, then a means
  of making assertions about available moves and outcomes, etc.
* **Improved compilation error messages.**
    Some error messages aren't very helpful in determining the source of the error, particularly this one:
        Syntax error: Could not create "game" ludeme from description.
