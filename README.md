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

## **Snapshots**
Menu: <img width="1202" height="939" alt="menu" src="https://github.com/user-attachments/assets/89b62e0e-fde9-4eca-9405-444e3291a328" />
Sonic speed: <img width="1202" height="939" alt="sonic ability" src="https://github.com/user-attachments/assets/6345b3c8-66e4-4110-8cac-4e3d96e0e4a0" />
Tails Flying: <img width="1202" height="939" alt="flying" src="https://github.com/user-attachments/assets/144b9a89-0df5-43d0-a7e9-2c9c4f684a4d" />
Knuckles Punch: <img width="1202" height="939" alt="knuckles" src="https://github.com/user-attachments/assets/ac853b68-b45a-43fc-b4cd-3b0bd6da3b42" />
Level 2, low friction ice level: <img width="1202" height="939" alt="level 2" src="https://github.com/user-attachments/assets/50cc0e68-3b85-42a2-9f78-6a9dc08584c0" />
level 3, low gravity space level: <img width="1202" height="939" alt="level 3" src="https://github.com/user-attachments/assets/11520c96-ce9b-4513-925b-ff2d4d43e76f" />
Boss level: <img width="1202" height="939" alt="boos level " src="https://github.com/user-attachments/assets/2d9333a8-19c2-45a8-aa57-85946fc32364" />
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
