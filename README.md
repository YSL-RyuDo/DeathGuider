# DeathGuider

[English](README.md), [Korean](README.ko.md), [Japanese](README.ja.md)

An O2CUBE team game. My work connects prisoner management, facilities and battle preparation.

A portfolio documentation fork of the **O2CUBE team project**. Original project: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider). The original repository and its credits remain authoritative. This fork documents **Young-Sang Lee (YSL-RyuDo)'s contributions**, not sole authorship of the game.

The fork uses `0.23Ver` as its default branch because the original `main` contains an early snapshot. Upstream branches and development history are preserved; no pull request or change was sent to the original repository.

| Project | Details |
|---|---|
| Status | Contribution fork |
| Stack | C#, Unity, O2CUBE |

[Explore the case](https://ysl-ryudo.github.io/en/work/deathguider/), [Portfolio](https://ysl-ryudo.github.io/en/)

[![DeathGuider](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

[DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## What I built across the game

My work is concentrated in management systems and battle preparation within a shared game. The fork preserves the upstream project. I do not attribute the whole exploration, combat AI, date system or other members' scenes to myself.

**Player flow**

Recruit units → allocate facilities and resources → train, recover and develop equipment → prepare a party → enter exploration

Source links pin the inspected revision; contribution links identify my non-merge changes. Shared-file links do not imply sole authorship. Private source requires repository access.

### Recruitment and unit storage

Worked on randomized prisoner recruitment, bus-facing UI and unit storage/selection. These systems connect available units to the management screen and later party preparation.

[BusRandomPrisoner.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Bus/BusRandomPrisoner.cs), [My change fc21ab5](https://github.com/YSL-RyuDo/DeathGuider/commit/fc21ab5eb4e66a8c14ed5de5e9a261ffbb7242f6), [StorageUI.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Floor/StorageUI.cs), [My change ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### Training, recovery and erosion

Implemented and changed gym, health and erosion processing. Facility progression reads unit activity data; the detailed design note traces the move away from deriving progression only from occupied UI slots.

[GYMSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/GYM/GYMSystem.cs), [My change ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [HealthSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Health/HealthSystem.cs), [My change ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [ErosionSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Erosion/ErosionSystem.cs), [My change ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### Research and smithing

Worked on laboratory and smithing systems as part of the management loop. Their state and resource handling connects development choices to the equipment available before a battle.

[LaboratorySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Laboratory/LaboratorySystem.cs), [My change 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2), [SmithSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Smith/SmithSystem.cs), [My change 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2)

### Party and equipment preparation

Worked on selecting battle units and equipment and preventing an empty party from entering battle. This is the boundary between my management work and the team's exploration/gameplay systems.

[BattleReadySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/BattleReadySystem.cs), [My change f8015e0](https://github.com/YSL-RyuDo/DeathGuider/commit/f8015e039aa7e33d9e8355f3d09cd90c786a04c8)

## My contribution: management systems

Bus/prisoner management, prisoner lists, storage and their UI/data flow.

Day progression and management-state updates.

Training, recovery, erosion and facility-related systems, including research/smithing work.

Battle preparation: selecting available units/equipment, preventing invalid empty-party entry, and connecting management state to preparation UI.

These responsibilities are supported by authored commits and the `Assets/Script/MainScene/` code. Combat AI, procedural maps and all other teammates' systems are not included in this contribution claim.

## Evidence / 근거 / 根拠

[Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

[Research & smithing / 연구소, 대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)

[Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)

[Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## Implementation and design

A management game needs prisoner state, facilities, day progression and battle preparation to agree. The preparation screen also needs to reject an empty party before entering battle.

My contribution covers bus/prisoner and storage management, training/recovery/erosion, research and smithing, and unit/equipment selection for battle preparation. Authored commits identify these changes within the shared project.

## How the code works and why it is structured this way

These notes connect the inspected implementation to the constraints it addresses and its tradeoffs. Explanations of design consequences are code analysis, not a claim that every alternative was prototyped. Contribution links identify my changes within team projects; source links retain their original access permissions.

### Facility progression uses persistent unit state

**Implementation**

My management-system commit changes training completion to inspect unit data and its activity status, apply the relevant stat changes, then reset the activity status. Related changes cover recovery, erosion and storage. Battle preparation is another contribution, connecting selected units and equipment to entry into battle.

**Design rationale**

A facility panel is a view; the unit's activity and stats need to persist beyond that view. Reading unit state makes the progression rule follow the game data rather than only the currently populated training slots. Resetting the activity also represents a state transition that later UI and gameplay must observe.

**Alternatives and the current tradeoff**

Driving progression from occupied facility slots is local and easy to follow, but can couple game rules to slot representation. Reading the unit activity data follows the persistent entity instead. A typed state model could make transitions clearer than numeric status codes, but would require migrating existing consumers and saved values.

**Tradeoffs and verification**

A wider unit-data iteration needs careful ownership and eligibility checks, and numeric activity codes make rules harder to read. These are review points, not a claim that the legacy implementation is a finished generic state machine. The shared DateSystem was authored by a teammate; my contribution is facility/progression integration, not ownership of that entire system.

[DeathGuider ee560502](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [DeathGuider 5593c51c](https://github.com/YSL-RyuDo/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## Inspecting the project

Open with the Unity version in [ProjectVersion.txt](ProjectSettings/ProjectVersion.txt). Start by inspecting the management scenes and `Assets/Script/MainScene/Lobby Test/` on `0.23Ver`. This documentation update does not certify a new build or playtest. Fork ownership does not transfer authorship or rights in the team's code/assets. Existing source history and credits are preserved.

## Related repositories

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider), Public repository
