# SkillForge
### An Interactive Skill RPG Platform

**Forge your skills, shape your journey.**

SkillForge is an academic minor project concept for a 2.5D Windows desktop game that combines interactive puzzle challenges with player progression, skill unlocking, and persistent progress.

> **Project status: Work in Progress.** Requirements and system/database design are being prepared before full prototype implementation. A runnable release is not available yet.

## Overview

Players will explore an ancient-futuristic environment, access challenge chambers, interact with a puzzle system, and progress through a game-style skill-development experience. The project is being developed as a Windows desktop prototype using Unity and C#.

## Planned Features

- **Interactive HUB:** A central environment for accessing the player profile, Forge, Skill Tree, challenges, information, and settings.
- **Puzzle Challenges:** A challenge chamber built around a three-ring puzzle system involving physical alignment, energy flow, and core synchronization.
- **Player Progression:** Player level and XP tracking, with progression updates following valid challenge completion.
- **Skill Unlocking:** A progression structure for unlocking approved skills and abilities.
- **Forge Vision:** An in-game analysis feature intended to display challenge formation and stability information without directly revealing puzzle solutions.
- **Persistent Progress:** Local saving and loading of player progression and settings.
- **Settings and Feedback:** Interface/audio settings, hints, notifications, and system feedback.

*These are planned design features, not claims that the features are already implemented or tested.*

## Technology Stack

| Area | Technology |
|---|---|
| Game engine | Unity 6.3 LTS |
| Programming language | C# |
| Target platform | Windows Desktop |
| Local database | SQLite |
| Documentation and diagrams | Draw.io |

## System Design

The planned prototype uses two Unity scenes:

- **`MainScene`:** Opening sequence, Hall/HUB, login/sign-up flow, UI-driven progression, Forge, Skill Tree, settings, and other HUB interactions.
- **`ChallengeScene`:** Interactive challenge chamber and puzzle gameplay.

Routine HUB navigation and interface-driven progression are intended to remain within `MainScene`. Scene transitions are reserved for entering and returning from the challenge experience.

The planned data architecture separates runtime player state from persistence responsibilities:

- **PlayerManager:** Runtime player information such as level, XP, inventory, and skill/ability progression.
- **SaveManager:** Saving, loading, and auto-saving persistent player data.
- Other managers are intended to have focused responsibilities rather than duplicate ownership of the same data.

## Database Design

The database is planned for **SQLite local storage**. The conceptual ERD includes these core entities:

- **`PLAYER`:** Player identity and progression, including level, XP, and play time.
- **`CHALLENGE`:** Challenge definitions.
- **`INVENTORY`:** Player inventory records.
- **`SKILL_ABILITY`:** Available skills and abilities.
- **`SETTINGS`:** Persisted interface and audio settings.

Many-to-many player relationships are resolved at database level through junction tables:

- **`CHALLENGE_PROGRESS`:** Player-specific challenge completion and reward-claimed state.
- **`PLAYER_SKILL`:** Player-specific skill unlock state.

The design aims to stay aligned with the approved project scope without adding unnecessary systems such as multiplayer, a virtual-currency economy, or cloud services.

## Development Status

- [x] Initial project concept and scope
- [x] Requirement analysis documentation
- [x] Level 0 and Level 1 Data Flow Diagrams (DFD)
- [x] Conceptual Entity Relationship Diagram (ERD)
- [x] Initial SQLite database design
- [ ] Unity prototype implementation
- [ ] Challenge gameplay implementation
- [ ] Database integration and save/load testing
- [ ] Testing and Windows build

This checklist reflects the current planning/documentation stage and should be updated as implementation progresses.

## Running the Project

This public repository currently serves as a **project overview and documentation showcase**. It does not currently contain a runnable build or the complete Unity source code. Setup and execution instructions will be added if and when the Unity project is published to this repository.

## Project Goals

- Practice requirement analysis and technical documentation
- Model system data flows using DFDs and ERDs
- Design a relational database using SQLite
- Apply C# and Unity game-architecture concepts
- Plan player progression and persistent data management
- Structure a small Windows desktop game prototype

## Author

**Vasim Shah**  
GitHub: [@vasim-shah21](https://github.com/vasim-shah21)

---

*SkillForge is an academic minor project and is currently under development.*
