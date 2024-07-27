# TIC-TAC-TOE-using-FPGA SPARTAN 6A Board
-----

**Dislamer** : In this project the the implementation of Tic-Tac-Toe is tried but due to some issues faced; hardware implementation was not possible; but the results got during simulation can be seen.

-----

### Introduction
This project involves the implementation of a Tic-Tac-Toe game using the Spartan6-XC6SLX9 TQ144FPGA board. The goal was to design, simulate, and implement the game on an FPGA, showcasing the use of Verilog for digital design and the capabilities of FPGA for real-time applications.

### Project Structure
The project is organized into several key components, each detailed below:

### 1. Verilog Code
The primary Verilog code is structured around the main module tictactoe, which handles the game logic, input/output management, and interaction between player and computer moves.

### Main Module: tictactoe
- Inputs:
  - clock: System clock for synchronization.
  - reset: Reset signal to restart the game.
  - play: Signal for player to make a move.
  - pc: Signal for the computer to make a move.
  - computer_position, player_position: 4-bit inputs representing the positions chosen by the computer and player.
- Outputs:
  - pos1 to pos9: 2-bit outputs representing the state of each position on the board (00: empty, 01: player, 10: computer).
  - who: 2-bit output indicating the winner (00: no winner, 01: player, 10: computer).

### Submodules
- position_registers: Manages the state of the board positions.
- winner_detector: Determines the winner by analyzing the board state.
- position_decoder: Decodes the position inputs for both player and computer moves.
- illegal_move_detector: Checks for and prevents illegal moves.
  
### 2. Module Creation and Interfacing
The modules were created and interfaced using Verilog. The design follows a modular approach, making it easier to test and debug individual components before integrating them into the main system.

### 4. RTL and Technology Schematic
The RTL (Register-Transfer Level) schematic provides a visual representation of the design at the register level, showing how data flows between registers and logic gates. The technology schematic maps the design onto the FPGA's physical resources.

### 5. UCF File
The UCF (User Constraints File) maps the design's logical signals to the FPGA's physical pins, ensuring correct interfacing with the hardware.

### 6. Configuration of Target Device
The project was successfully implemented on the Spartan6-XC6SLX9 TQ144FPGA board, with the configuration process confirming successful programming of the device.
