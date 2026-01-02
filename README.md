# Atari Breakout Clone (x86 Assembly – NASM, DOSBox)

A fully working **Atari Breakout clone** written in **x86 Assembly using NASM**, targeting **DOS .COM format** and designed to run inside **DOSBox**.

This project demonstrates low-level game development concepts including graphics rendering, keyboard handling, collision detection, timing, sound (PC speaker), and score management using BIOS and DOS interrupts.

## Inspiration

This project is **inspired by** the following repository:

https://github.com/nav1s/Atari-Breakout

The implementation, structure, and logic are written independently and use **NASM**, not TASM or MASM.

## Key Features

- Classic Breakout gameplay
- Paddle and ball physics
- Brick collision and destruction
- **Live score display during gameplay**
- Final score display on Game Over and Victory screens
- Multiple lives system (starts with 3 lives)
- PC Speaker sound effects
- Pause and restart functionality
- Cheat and speed control keys
- Written **purely in NASM**
- Runs as a **.COM program** in DOSBox

## Controls

### Paddle Movement
- **Left Arrow** → Move paddle left
- **Right Arrow** → Move paddle right

### Game Controls
- **ENTER** → Start the game
- **ESC** → Pause game (press again to resume)
- **SPACE** → Restart game (on Game Over or Victory)
- **ESC (from menu)** → Exit program

### Speed & Special Keys
- **F** → Increase ball speed
- **S** → Decrease ball speed
- **Down Arrow** → Fastest ball mode
- **Z** → Cheat mode (destroys bricks automatically)

## Scoring System

- Each destroyed brick increases the score
- Score is calculated and displayed live at the bottom of the screen
- Final score is shown on:
  - Game Over screen
  - Victory screen
- Score supports up to **three digits**

## Game Rules

- Destroy all bricks to win
- Missing the paddle costs one life
- Game ends when all lives are lost
- Total bricks: **32**

## Requirements

- **DOSBox**
- **NASM assembler**
- Any x86 host system capable of running DOSBox

## Build Instructions

Assemble the game using NASM:

```bash
nasm -f bin breakout.asm -o breakout.com
