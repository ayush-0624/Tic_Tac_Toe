﻿![](tic-tac-toe.png)

![](Output.png)


- **Initializing Game Components**

We start by importing the pygame library and the time library .Then we initialize all the global variables that we will use in our Tic Tac Toe game. Here, the TTT is the main 3×3 Tic Tac Toe board and at first, it will have 9 None values. The height and width of the canvas where we will play the game is 400×400.

- **Initializing Pygame window**

We use the pygame to create a new window where we’ll play our Tic Tac Toe game. So we initialize the [pygame](https://www.pygame.org/) with pg.init() method and the window display is set with a width of 400 and a height of 500. We have reserved 100-pixel space for displaying the status of the game.

The pg.display.set\_mode() initializes the display and we reference it with the screen variable. This screen variable will be used whenever we want to draw something on the display.

The pg.display.set\_caption method is used to set a name that will appear at the top of the display window.

- **Load and transform images**

The Python project uses many images like the opening image that will display when the game starts or resets. The X and O images that we will draw when the user clicks on the grid. We load all the images and resize them so that they will fit easily in our window.

- **Define the functions**
- Now we create a function that will start the game. We will also use this function when we want to restart the game. In pygame, the blit() function is used on the surface to draw an image on top of another image.

- So we draw the opening image and after drawing, we always need to update the display with **pg.display.update().** When the opening image is drawn, we wait for 1 second using time.sleep(1) and fill the screen with white colour.

- Next, we draw 2 vertical and horizontal lines on the white background to make the 3×3 grid. In the end, we call the draw\_status() function

- The **draw\_status()** function draws a black rectangle where we update the status of the game showing which player’s turn is it and whether the game ends or draws.

- The **check\_win()** function checks the Tic Tac Toe board to see all the marks of ‘X’ and ‘O’. It calculates whether a player has won the game or not. They can either win when the player has marked 3 consecutive marks in a row, column or diagonally. This function is called every time when we draw a mark ‘X’ or ‘O’ on the board.

- The **drawXO(row, col)** function takes the row and column where the mouse is clicked and then it draws the ‘X’ or ‘O’ mark. We calculate the x and y coordinates of the starting point from where we’ll draw the png image of the mark.

- The **userClick()** function is triggered every time the user presses the mouse button. When the user clicks the mouse, we first take the x and y coordinates of where the mouse is clicked on the display window and then if that place is not occupied we draw the ‘XO’ on the canvas. We also check if the player wins or not after drawing ‘XO’ on the board.
- The last function is the **reset\_game()**. This will restart the game and we also reset all the variables to the beginning of the game.

- **Run the tic tac toe game forever**

- To start the game, we will call the **game\_opening()** function. Then, we run an infinite loop and continuously check for any event made by the user. If the user presses mouse button, the MOUSEBUTTONDOWN event will be captured and then we will trigger the **userClick()** function. Then if the user wins or the game draws, we reset the game by calling **reset\_game()** function. We update the display in each iteration and we have set the frames per second to 30.





