# Hexagonal Chess

The game description file in this directory describes several variants of Hexagonal Chess (i.e., chess played on a board made up of hexagonal spaces.) Specifically, those variants are:
* Glinski Chess
* Brusky Chess
* De Vasa Chess
* Empty Palace Chess
* McCooey Chess
* Mini Hexchess
* Shafran Chess
* Starchess

Each variant has associated rules that can be viewed through the Ludii General Game System ("the app").

## How to Play
Currently, the following steps are needed to run play Hexagonal Chess using the '.lud' file in this directory:
* From https://ludii.games/download.php, download the Ludii player (Ludii.jar, currently at v0.9.3) to an empty directory.
* The Ludii User Guide and the Ludii Language Reference can optionally be downloaded from the same website.
* On a computer with Java (v8 or higher), start the play by running the command
      java -jar Ludii.jar
* From within the player, select the menu item File, then Load Game from File. 
* The Ludii General Game System supports playing games online with other players, but this appears
  to be limited to those games already integrated into the system. The online play of games loaded from files
  is not supported.

## Bugs
Ludii system (v0.9.3) bugs to report:
* Changing the name of a game loaded from a File to match the filename can trigger the error message:
      The game could not be compiled, but no specific error was identified."..
* The definition of StepForwardToEmpty in section A.6.1 of the Ludii Language Reference
  doesn't match the implementation in rules/play/moves/StepForwardToEmpty.def.
* Whitespace sensitivity. Adding a newline between the keyword "rulesets" and its
  following open brace can trigger the error mesage:
      Could not expand. Check that bracket pairs '(..)' and '{..}' match.

## Feature Requests
Ludii system (v0.9.3) feature requests:
* **Relative direction enums for hexagonal boards.**
  Relative direction enums for hexagon and rhombus board shapes.
* **Flexible rhombus Cell orientation and board layout.**
  Ability to specify orientation of Cells for rhombus boards, and other aspects of the layout.
  Currently all Cells are horizontally oriented, and there is only one layout available,
  with the first row starting at the far left and pointing to the SE,
  while the hexagon board type supports both horizontal and vertical hexagon cells.
* **Three-colour uniform colouring for boards with horizontally oriented hexagonal Cells.**
  When hexagon Cells are horizontally oriented, Phase0, Phase1, and Phase2 do not form a 3-colour uniform tiling,
  as they do when hexagonal Cells are vertically oriented.
* **Optional whitespace between argument label and argument.**  The Ludii language seems to not constrain a game
  file's use of whitespace. However, whitespace introduced between an argument label (e.g., if: ifAfterwards: to: size:
  stack:) and the argument triggers a syntax error, without identifying the source of the error.
* **A means of unit testing.** For example, a means of supporting tests with a setup that creates a games, then a means
  of making assertions about available moves and outcomes, etc.
* **Option attribute (e.g., "hidden") to remove an option from the Options menu.**
    For example, if one option specifies removal of board spaces, and another constrols piece
    starting locations, then some combinations could be incompatible. Making incompatible combinations
    available could be confusing for the end user.
* **Improved compilation error messages.**
    Currently, it seems that the following two unhelpful error messages are output upon the catching of an Exception
    that was thrown from a large code block that has many different modes of failure:
        The game could not be compiled, but no specific error was identified.
        Syntax error: Could not create "game" ludeme from description.
        Could not expand. Check that bracket pairs '(..)' and '{..}' match.
