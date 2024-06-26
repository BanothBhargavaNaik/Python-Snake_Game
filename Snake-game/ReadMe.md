

![Designer (11)](https://github.com/BanothBhargavaNaik/Python-Snake_Game/assets/52111190/1222e297-d5d4-4bf4-98d3-862f1cc90f5b)


# Snake Game Documentation

This document provides a comprehensive guide to the Snake game written in Python using Turtle graphics.

## Requirements

This requirements.txt file specifies the Python version required for your game and any additional libraries needed, ensuring that users can easily install the dependencies by running 

- pip install -r requirements.txt.

## Gameplay

The Snake game is a classic arcade game where you control a snake that grows longer by eating food. Avoid hitting the walls or your own body, or the game ends. Use the arrow keys to change the direction of the snake.


## Game Variables (`snake_game.py`)

- `WIDTH`: Width of the game screen (pixels)
- `HEIGHT`: Height of the game screen (pixels)
- `DELAY`: Delay between game updates (milliseconds)
- `FOOD_SIZE`: Size of the food item (pixels)
- `SNAKE_SIZE`: Size of each snake segment (pixels)
- `DIRECTIONS`: List of valid directions (`up`, `down`, `left`, `right`)
- `SNAKE_STEP`: Movement amount per update (pixels)
- `snake`: List containing the coordinates of each snake segment (`x, y`)
- `snake_direction`: Current direction of the snake (`up`, `down`, `left`, `right`)
- `food_pos`: Coordinates of the food item (`x, y`)
- `score`: Current game score
- `high_score`: Highest score achieved

## Functions

- `init_screen()`: Initializes the game screen, sets the window title, and sets up the background image (optional).
- `update_high_score()`: Updates the high score file if the current score is higher.
- `set_snake_direction(direction)`: Changes the snake's direction if a valid key is pressed.
- `food_collision(food)`: Checks if the snake collides with the food and updates the score and food position.
- `check_collision(new_head)`: Checks if the snake collides with the walls or itself.
- `game_over()`: Handles game over events, displays a message, and removes event handlers.
- `start_new_game(x, y)`: Resets the game state and restarts the game loop.
- `get_distance(pos1, pos2)`: Calculates the distance between two points.
- `get_random_food_pos()`: Generates random coordinates for the food item within the game area.
- `reset_game()`: Resets the snake position, direction, score, and food position.

## Game Loop

The `game_loop` function continuously updates the game state. It performs the following actions:

1. Clears the previous screen.
2. Updates the snake's position based on the current direction.
3. Checks for collisions with walls or the snake itself.
4. Checks for food collision and updates score and food position.
5. Draws the snake and food items on the screen.
6. Updates the screen title with the current score and high score.
7. Schedules the next game update based on the `DELAY` value.

## User Interaction

The game uses the arrow keys to control the snake's direction:

- Up arrow: Moves the snake upwards.
- Down arrow: Moves the snake downwards.
- Left arrow: Moves the snake leftwards.
- Right arrow: Moves the snake rightwards.

## Running the Game

1. Save the code as a Python file (e.g., `snake_game.py`).
2. Open a terminal or command prompt and navigate to the directory where you saved the file.
3. Run the script using the command `python snake_game.py`.
4. This will launch the Snake game. Use the arrow keys to control the snake and try to achieve a high score!

## Customization

You can customize the game by adjusting the following:

- Change the values of constants like `WIDTH`, `HEIGHT`, `DELAY`, `FOOD_SIZE`, and `SNAKE_SIZE` in the code.
- Create a custom background image using an image editor and set the path in the `init_screen` function.
- (Optional) Implement a configuration file to store these settings for easier modification.
