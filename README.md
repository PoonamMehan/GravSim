# GravSim

A small **gravity simulation** written in C++ using [raylib](https://www.raylib.com/) for graphics. Two bodies (circles) move under Newtonian gravity; forces are computed with an inverse-square law and positions updated each frame. The window shows the two bodies and a line between them.

## What the project does

- Simulates two bodies with position, velocity, acceleration, and mass.
- Applies Newtonian gravity: \( F = G \, m_1 m_2 / r^2 \), with a fixed timestep.
- Renders in a raylib window: one body as an orange circle, the other as a red circle, with a green line connecting them.
- Runs in a loop until you close the window.

## Setup

### Prerequisites

1. **raylib** — On Windows, raylib must be available so the compiler can find headers and the library. The makefile expects:
   - Include path: `C:\raylib\include`
   - Library path: `C:\raylib\lib`
   - You can [download raylib](https://github.com/raysan5/raylib/releases) (e.g. Windows MinGW build) and unpack it so that `raylib.h` is in `C:\raylib\include` and `libraylib.a` (or the appropriate lib) is in `C:\raylib\lib`.
   - Alternatively, run the provided script to fetch raylib into `./lib`, then adjust the makefile’s `CXXFLAGS` and `LDFLAGS` to use `./lib` instead of `C:\raylib` if needed:
     ```powershell
     .\setup-raylib.ps1
     ```
2. **Chocolatey** (Windows package manager, if you don’t have it):
   ```powershell
   Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
   ```
3. **Make** and **MinGW** (C++ compiler and build tools):
   ```powershell
   choco install make
   choco install mingw
   ```

### Build and run

1. Clone the repo and go to the project root:
   ```powershell
   git clone https://github.com/PoonamMehan/GravSim.git
   ```
2. Build:
   ```powershell
   make
   ```
3. Run the simulation:
   ```powershell
   .\bin\game.exe
   ```

To remove build artifacts: `make clean`.

## How to contribute

Coming soon...
