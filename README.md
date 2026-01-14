# Sonic Classic Heroes
A classic Sonic-inspired platformer built with C++ and SFML, featuring team-based mechanics with Sonic, Tails, and Knuckles.

**Team Project** - Developed collaboratively by Muhammad Saad and Muntazir, demonstrating advanced object-oriented programming principles.

## About
Navigate through multiple challenging levels including Labyrinth Zone, Ice Cap Zone, Death Egg Zone, and face off against a final boss. Control three unique characters, each with distinct abilities and gameplay mechanics.

## Team Contributions

### Muhammad Saad - Player Systems & Mechanics
* **Player Mechanics**: Implemented complete player movement system including jump physics, momentum, and character-specific controls
* **Collision System**: Developed hitbox detection and collision resolution for players, enemies, and environment interactions
* **Special Abilities**: Designed and implemented unique abilities for Sonic (spin dash), Tails (flight), and Knuckles (glide/climb + block breaking)
* **Physics Engine**: Created gravity, acceleration, and velocity systems for realistic platforming feel
* **Power-up System**: Implemented heart (health) collection and star (special ability activation) generation and mechanics
* **Destructible Environment**: Developed block-breaking system for Knuckles' unique terrain interaction
* All systems built using OOP principles with proper encapsulation and inheritance

### Muntazir - Game Systems & Level Design
* **Enemy AI**: Developed behavior patterns for all enemy types including patrol routes, attack logic, and boss mechanics
* **Game Flow**: Implemented state management system (menu, gameplay, leaderboard transitions)
* **Level Design**: Created four complete levels with varied layouts, enemy placement, destructible blocks, and difficulty progression
* **UI Systems**: Built menu system with navigation, pause functionality, and scoreboard display
* **Audio & Visuals**: Integrated animation systems, sound effects, and background music
* **Save System**: Implemented game state persistence and leaderboard tracking
* All features structured using OOP design patterns and modular architecture

## Object-Oriented Design
This project demonstrates key OOP principles through collaborative implementation:

### Factory Pattern
Dual factory systems for runtime object creation:
* **PlayerFactory** - Dynamic character creation (Sonic, Tails, Knuckles)
* **EnemyFactory** - Enemy spawning and level population

### Inheritance & Polymorphism
* **Entity Hierarchy**: `Entity` → `DynamicEntity` → `Player` / `Enemy`
* **Player Classes**: `Player` base extended by `Sonic`, `Tails`, `Knuckles` with unique abilities
* **Enemy Categories**:
  * Crawlers: `CrabMeat`, `MotoBug`
  * Flyers: `BatBrain`, `BeeBot`, `Boss`
* **Level System**: Abstract `Level` base with four unique implementations

### Encapsulation
* State management with clean transitions (MENU, PLAYING, LEADERBOARD)
* Resource management with proper memory cleanup
* Private camera system with controlled scrolling

### Composition
* Modular subsystems: `Menu`, `Scoreboard`, `Level`
* Independent managers: `SoundManager`, `ProjectileManager`, `Animation`
* Decoupled save/load system

## Features
* Three playable characters with unique abilities:
  * **Sonic**: Speed boost and spin dash
  * **Tails**: Flight ability for vertical exploration
  * **Knuckles**: Glide/climb and break through destructible blocks
* Four distinct levels with progressive difficulty
* Multiple enemy types with varied AI behaviors
* Power-up system with hearts (health) and stars (special ability activation)
* Destructible environment mechanics
* Save/load system with full game state persistence
* Scoring system with persistent leaderboard
* 180-second time challenge
* Volume control and audio management
* Smooth camera following

## Technologies
* **C++17** - Modern C++ with manual memory management
* **SFML 2.5+** - Graphics, audio, and input handling
* **CMake** - Cross-platform build system

## Building the Project

### Prerequisites
* CMake 3.10+
* C++17 compatible compiler
* SFML 2.5+

### Linux/macOS
```bash
mkdir build && cd build
cmake ..
make
./SonicClassicHeroes
```

### Windows
```bash
mkdir build && cd build
cmake .. -G "Visual Studio 16 2019"
cmake --build . --config Release
.\Release\SonicClassicHeroes.exe
```

## Controls
* **Arrow Keys** - Move
* **Space** - Jump
* **Shift** - Special ability (requires star power-up)
* **Tab** - Switch character
* **F5** - Quick save
* **ESC** - Pause/Menu

## Project Structure
```
OPP_Project_SonicClassicHeroes/
├── Data/                          # Assets and save files
├── Src/
│   └── Src.cpp                    # Entry point
├── classes/
│   ├── entities/
│   │   ├── Entity.cpp/h
│   │   └── dynamicEntity/
│   │       ├── DynamicEntity.cpp/h
│   │       ├── enemy/
│   │       │   ├── Enemy.cpp/h
│   │       │   ├── crawlers/      # CrabMeat, MotoBug
│   │       │   ├── flyers/        # BatBrain, BeeBot, Boss
│   │       │   ├── Projectile.cpp/h
│   │       │   └── ProjectileManager.cpp/h
│   │       └── player/            # Player, Sonic, Tails, Knuckles
│   ├── factories/                 # PlayerFactory, EnemyFactory
│   └── game/                      # Game loop, levels, menu, scoreboard
├── CMakeLists.txt
└── README.md
```

## Development Timeline
Completed in 2 weeks as part of OOP coursework, with both developers contributing equally to design decisions and implementation.

## License
This is an educational project created for OOP coursework.

## Acknowledgments
* Inspired by SEGA's Sonic the Hedgehog series
* SFML library for graphics and audio

**Note:** This is a fan project for educational purposes and is not affiliated with or endorsed by SEGA.
