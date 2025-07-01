# Brick Breaker FPGA Game

This project is a Brick Breaker game implemented on an FPGA using C and a VGA display, controlled by push-buttons and displaying the score on a 7-segment display.

## Features

- VGA Graphics for Brick Breaker game
- Controls using FPGA push buttons (KEY0-KEY3)
- Score display using 7-segment display
- Ball, paddle, and bricks rendered in real-time
- Collision detection and response

## Hardware Used

- FPGA DE1-SoC Board
- VGA output (0xC8000000)
- Push Buttons (KEY_BASE: 0xFF200050)
- 7-Segment Display (HEX_BASE: 0xFF200020)

## Controls

- KEY0: Reset Game
- KEY1: Start Ball Movement
- KEY2: Move Paddle Left
- KEY3: Move Paddle Right

## How it Works

- Paddle is controlled using KEY2 and KEY3.
- Ball bounces on walls, paddle, and breaks bricks on collision.
- When all bricks are broken, the player wins.
- On missing the paddle, the game resets.

## Build and Run

1. Use ARM toolchain to compile:
   ```bash
   arm-eabi-gcc -Wall -gdwarf-2 -O1 -mno-unaligned-access -mfloat-abi=softfp -mcpu=cortex-a9 -o brick_breaker.elf brick_breaker.c
   ```

2. Load the `.elf` file onto the FPGA using your DE1-SoC loader or simulator.

## Demo

Demo images are provided in the repository. Use a connected VGA monitor and observe the 7-segment display for scores.
---![image](https://github.com/user-attachments/assets/8b37493c-2fc4-400e-9898-085fd2b85af6)
![image](https://github.com/user-attachments/assets/8de8aa93-057c-4e18-8b45-6a6c211cd8cd)
![image](https://github.com/user-attachments/assets/9e3d4ebc-e484-4d8f-a971-e61ab0490cf5)
![image](https://github.com/user-attachments/assets/1c2bccd6-2a74-4cd1-bd63-af4a696195b7)




Created for educational purposes using FPGA, C, and embedded programming techniques by Amitesh Raj.
