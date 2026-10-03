# Rubik's Cube (C# / Windows Forms)

A desktop Rubik's Cube you can turn, scramble and reset, drawn as an unfolded 2D cube. Built as a second-year university group project.

## What it does

- Shows all six faces (Front, Right, Back, Left, Up, Down) as a grid of coloured tiles.
- Twelve arrow buttons turn the cube: each of the three rows can move left or right, and each of the three columns can move up or down.
- **Scramble** applies a random-length sequence of turns.
- **Reset** returns the cube to its solved state.
- A start screen with **Start**, **Credits** and **End**.

## How it works

Each face tile is a `Button` whose background colour is its sticker colour. The tiles are grouped into six strips of twelve:

- `fr1`–`fr3`: the three horizontal rows that wrap around the Front, Right, Back and Left faces.
- `fc1`–`fc3`: the three vertical columns that wrap around the Front, Down, Back and Up faces.

A turn shifts the colours along one strip by three tiles, using three hidden buttons as temporary storage for the tiles that wrap around. After each turn the tiles shared between a row strip and a column strip are re-linked so the two views stay in sync.

The logic is in [`Form1.cs`](Rubix%20Cube%20C%20sharp/Form1.cs); the start screen is [`Form2.cs`](Rubix%20Cube%20C%20sharp/Form2.cs).

## Run it

Requirements: Windows, Visual Studio 2019 or later, .NET Framework 4.7.2.

1. Clone the repository.
2. Open `Rubix Cube C sharp.sln` in Visual Studio.
3. Press **F5**.

## Known limitations

- Turning an outer row or column moves the strip but does not rotate the face attached to it, so the cube does not yet behave exactly like a physical one.
- There is no solver or move counter.

## Team

- Muhammad Qasim ([@Globeeeee](https://github.com/Globeeeee))
- Imran ([@imu-002](https://github.com/imu-002))
