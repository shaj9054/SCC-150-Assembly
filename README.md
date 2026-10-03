# MIPS Bitmap Drawing Coursework

An assembly-language exercise exploring user input, branching, loops, subroutines and memory-mapped graphics. The source offers a menu for clearing a bitmap display and drawing a five-line musical stave.

## Implemented routines

- Console prompts and integer input using MIPS syscall conventions.
- Colour-selection branches for yellow, green, red, pink and orange.
- A loop that writes colour words to consecutive display-memory locations.
- Stave drawing with a user-supplied starting row, five horizontal lines and a reusable `line` subroutine.

## Source file

The assembly is stored in `CourseWork`, without a filename extension. It contains `.data` and `.text` sections and a `main` entry label.

## Running environment

Use a MIPS teaching simulator with compatible syscalls and a bitmap-display tool. The code assumes a display base address of `0x10040000`, four bytes per pixel, 512 pixels per row and a 524,288-byte display region, corresponding to 512 × 256 pixels.

Open `CourseWork` in the simulator, or copy it to a local `.asm` file if the tool requires an extension. Configure the bitmap display to match those assumptions before assembling and running.

## Menu and input

| Option | Current behaviour |
| --- | --- |
| 1: cls | Select a colour and attempt to fill the display. |
| 2: stave | Use the second input as the starting row and draw five lines. |
| 3: note | Branches to an unfinished routine. |
| 4: exit | Listed in the menu, but has no dedicated dispatch branch. |

## Current limitations

The note routine is unfinished. Several `addi` operands exceed the instruction's 16-bit immediate range, so the source may not assemble without changes in a strict simulator. Strings and input validation also need refinement. This repository is an academic source snapshot, not a completed music-notation application.

## Project context

University coursework for **SCC-150** at Lancaster University. Language: **MIPS assembly**. Repository owner: **Mohammed Shajalal Sarwar**. Some repositories include supplied coursework support code; original source attributions are retained.
