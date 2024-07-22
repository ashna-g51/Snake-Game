# Snake-Game
Snake Game using ATMega32 and 8x8 LED Matrix

Components used:
1. ATMega32
2. MAXI7219 8x8 LED Matrix
3. XY Joystick Module

Algorithm
Used Assembly C to code multiple functions, to mimic the logic of the game.
1. move (): This function makes the snake appear on the other end of the display when it comes
to the end of the sides
2. moveSnake(): Moving the snake. All the bits of the snake follow the bit which is in front of
itself.
3. updateDir(): Update the direction of the head of the snake when the user changes the
direction.
4. IsSnakeDead(): Checking whether the snake is dead or not. Compared all bits locations.
If they were the same (overlapped) assumed that the snake is dead.
5. IsFeedEaten(): Checking whether the snake ate the feed or not. Compared all bits
locations with the feeds locations. If they were the same (overlapped) assumed that snake ate
the feed.
6. snakeGrows(): If the snake ate the feed, we extended the length of the snake by 1.
7. joyStickDirectChange(): Used ADC and interrupt in this function to check whether the
user used the joystick or not.
8. random_dot(): Generated a random dot (feed) to the display by using a random
generator sub-function. Also, checked whether the location of the feed and the snake overlapped or not. If it did, generated another dot. 
