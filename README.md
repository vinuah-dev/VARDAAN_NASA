# NASA Space Mission Game

A 3D, single-player space-mission game where the player takes the role of a newly selected astronaut and prepares for space missions inside an interactive NASA-inspired facility.

> **Status:** In development. Mission 1 and Mission 2 are the current implementation scope. This README describes the project vision; it does not claim that every listed feature is already implemented.

## Game Overview

The player explores a 3D mission-preparation facility, interacts with researchers and equipment, completes objectives, and progresses through missions.

### Mission 1 — Rocket Assembly
Set in the first-floor rocket assembly laboratory.

- Inspect the rocket and identify missing or damaged components.
- Earn coins through temporary mini-game stations.
- Purchase components from the vending machine.
- Manage components in the inventory.
- Install compatible components into the correct rocket sockets.
- Review rocket condition, assembly, durability, weight, and launch readiness.
- Complete mission validation.

### Mission 2 — Launch and Orbit Planning
Set on the second-floor launch control balcony.

- Select a suitable launch date.
- Review weather, wind, visibility, and launch risk.
- Configure the launch trajectory and review accuracy and deviation.
- Plan orbital boosts, timing, strength, and expected orbit count.
- Validate the launch plan and review the mission summary.

### Future Roadmap
Future missions are planned but are not part of the current full implementation scope.

- **Mission 3:** In-space operations, tasks, and research.
- **Mission 4:** Destination landing, exploration, and research.
- **Mission 5:** Return-to-Earth preparation and completion.

## Core Systems

- Game root and game-state coordination
- Stage and mission management
- Objective and progress tracking
- Player interaction
- Dialogue and NPC behaviour
- Cutscenes and transitions
- Rocket assembly and component data
- Inventory, shop, coins, and rewards
- Mini-game integration
- Launch date and weather data
- Trajectory and orbit planning
- Mission validation
- Reusable UI
- Save and load

## Design Principles

- **Single-player:** No multiplayer, accounts, or online dependency.
- **Modular:** Keep systems independent and reusable.
- **Data-driven:** Keep mission, objective, component, item, reward, and planning data separate from gameplay logic.
- **Replaceable assets:** Use placeholders with clear replacement points for models, icons, animations, sound, UI art, and mini-games.
- **Centralized validation:** Mission completion should be validated by gameplay systems, not UI button handlers.
- **Persistence:** Save mission progress and important gameplay state.
- **Safe failure:** Missing optional assets or data should use fallbacks and should not block gameplay.
- **Preserve existing functionality:** Extend the existing project rather than unnecessarily replacing its player controller, camera, input, scenes, or working systems.

## Development Status

| Area | Intended scope |
|---|---|
| Core architecture | Modular foundation |
| Mission 1 | Rocket assembly gameplay |
| Mission 2 | Launch and orbit planning |
| Mini-games | Replaceable placeholders until final games are integrated |
| Art and animation | Replaceable placeholders until final assets are supplied |
| Missions 3–5 | Future hooks / locked entries only |

Update this table as features are implemented and tested.

## Getting Started

The exact setup and run commands depend on the game engine and project configuration.

1. Clone this repository.
2. Open the project using its configured game engine and version.
3. Allow the editor to import or build project assets.
4. Open the configured main scene or project entry point.
5. Run the project using the engine's normal play/run command.

Add the exact engine version, dependencies, setup commands, and build instructions here once confirmed for this repository.

## Controls

The initial target is keyboard and mouse. Fill in the actual bindings once finalized.

| Action | Input |
|---|---|
| Move | To be configured |
| Look / Camera | To be configured |
| Interact | To be configured |
| Open mission / inventory UI | To be configured |

## Testing Checklist

Mark an item complete only after testing it in the project.

- [ ] Existing project launches successfully.
- [ ] Player movement, camera, and input still work.
- [ ] Player can interact with NPCs and mission objects.
- [ ] Mission and objective progress updates correctly.
- [ ] Mission 1 works from briefing through rocket validation.
- [ ] Mini-game placeholders award rewards correctly.
- [ ] Purchases update coins and inventory correctly.
- [ ] Compatible components install successfully.
- [ ] Incompatible components are rejected without changing inventory or rocket stats.
- [ ] Rocket status updates after component installation.
- [ ] Mission 2 date, weather, trajectory, and orbit planning work.
- [ ] Invalid plans show useful feedback.
- [ ] Save/load restores required progress.
- [ ] Missing optional assets do not block gameplay.
- [ ] Existing project functionality remains intact.

## Suggested Logical Structure

Adapt these categories to the existing engine and repository conventions; do not restructure a working project just to match this example.

```text
Core/
Player/
NPC/
Missions/
  Mission1_RocketAssembly/
  Mission2_LaunchPlanning/
  FutureMissions/
Systems/
UI/
Data/
```

## Development Guidelines

1. Inspect the existing implementation before adding or replacing systems.
2. Reuse existing project conventions and working functionality.
3. Keep mission logic separate from UI presentation.
4. Prefer configurable data and replaceable references over hard-coded content.
5. Test affected mission flows and relevant existing functionality.
6. Document setup steps, controls, and asset integration points.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
