# DeathGuider

<!-- portfolio-languages -->
[![English (current)](https://ysl-ryudo.github.io/assets/diagrams/language-en-current.svg)](README.md) [![한국어](https://ysl-ryudo.github.io/assets/diagrams/language-ko.svg)](README.ko.md) [![日本語](https://ysl-ryudo.github.io/assets/diagrams/language-ja.svg)](README.ja.md)
<!-- /portfolio-languages -->

An O2CUBE team game. My work connects prisoner management, facilities and battle preparation.

O2CUBE team project. Original repository: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider).

| Project | Details |
|---|---|
| Status | Contribution fork |
| Stack | C#, Unity, O2CUBE |

[Explore the case](https://ysl-ryudo.github.io/en/work/deathguider/), [Portfolio](https://ysl-ryudo.github.io/en/)

[![DeathGuider](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

[DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## Inside the game

[![Recruitment connects generated prisoner candidates, daily limits and the roster.](https://ysl-ryudo.github.io/assets/gameplay/deathguider-recruitment.webp)](https://ysl-ryudo.github.io/assets/gameplay/deathguider-recruitment.webp)

Recruitment connects generated prisoner candidates, daily limits and the roster.

[![The management flow connects party slots, equipment selection and dungeon entry.](https://ysl-ryudo.github.io/assets/gameplay/deathguider-party.webp)](https://ysl-ryudo.github.io/assets/gameplay/deathguider-party.webp)

The management flow connects party slots, equipment selection and dungeon entry.

## What I built across the game

I worked on unit recruitment and storage, training, recovery and erosion, research and smithing, and party/equipment preparation before exploration.

[![My implementation flow](https://ysl-ryudo.github.io/assets/diagrams/deathguider-flow-en.svg)](https://ysl-ryudo.github.io/assets/diagrams/deathguider-flow-en.svg)

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

## Evidence / 근거 / 根拠

[Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

[Research & smithing / 연구소, 대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)

[Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)

[Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## Implementation and design

A management game needs prisoner state, facilities, day progression and battle preparation to agree. The preparation screen also needs to reject an empty party before entering battle.

My contribution covers bus/prisoner and storage management, training/recovery/erosion, research and smithing, and unit/equipment selection for battle preparation. Authored commits identify these changes within the shared project.

## How the code works and why it is structured this way

### Facility progression uses persistent unit state

**Implementation**

My management-system commit changes training completion to inspect unit data and its activity status, apply the relevant stat changes, then reset the activity status. Related changes cover recovery, erosion and storage. Battle preparation is another contribution, connecting selected units and equipment to entry into battle.

**Design rationale**

A facility panel is a view; the unit's activity and stats need to persist beyond that view. Reading unit state makes the progression rule follow the game data rather than only the currently populated training slots. Resetting the activity also represents a state transition that later UI and gameplay must observe.

**Alternatives and the current tradeoff**

Driving progression from occupied facility slots is local and easy to follow, but can couple game rules to slot representation. Reading the unit activity data follows the persistent entity instead. A typed state model could make transitions clearer than numeric status codes, but would require migrating existing consumers and saved values.

**Tradeoffs and verification**

Scanning unit data requires owner and activity filters. Numeric activity codes make the rules harder to read, and facility progress must stay aligned with the game's date-advance events.

[DeathGuider ee560502](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [DeathGuider 5593c51c](https://github.com/YSL-RyuDo/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## Inspecting the project

Open with the Unity version in [ProjectVersion.txt](ProjectSettings/ProjectVersion.txt). Start by inspecting the management scenes and `Assets/Script/MainScene/Lobby Test/` on `0.23Ver`.

## Related repositories

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider), Public repository
