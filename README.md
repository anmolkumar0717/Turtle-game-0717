# Turtle Race Game

This is a simple game where turtles race across the screen using the Python `turtle` module. The turtles' movements are randomized using the `random` module to determine the winner.

## How to Play

1. Clone or download this repository.
2. Make sure you have Python installed on your system.
3. Run the `Turtle_game-0717.py` script:

    ```bash
    python turtle_race.py
    ```

4. Watch the turtles race across the screen!
5. The turtle that reaches the finish line first is declared the winner.

## Rules

- Each turtle starts at the left side of the screen and races towards the right side.
- The turtles move forward a random distance at each step.
- The first turtle to reach the right side of the screen is declared the winner.

## Features

- Randomized Movement: Each turtle's movement is determined randomly, making each race unpredictable.
- Multiple Turtles: You can customize the number of turtles racing.
- Animated Display: The race is displayed visually with the turtles moving across the screen.

## Code Example

Here's a simple example of how the game is implemented:

```python
import turtle
import random

# Set up the screen
screen = turtle.Screen()
screen.setup(width=600, height=400)

# Create turtles
num_turtles = 5
turtles = []

for i in range(num_turtles):
    turtles.append(turtle.Turtle())

# Race loop
while True:
    for turtle in turtles:
        turtle.forward(random.randint(1, 10))

        if turtle.xcor() >= 300:
            print(f"Turtle {turtles.index(turtle) + 1} wins!")
            screen.bye()
            break
