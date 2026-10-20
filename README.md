# DeathGuider

[English](README.md) · [Korean](README.ko.md) · [Japanese](README.ja.md)

An O2CUBE team game. My work connects prisoner management, facilities and battle preparation.

**C# · Unity · O2CUBE** · Contribution fork

A portfolio documentation fork of the **O2CUBE team project**. Original project: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider). The original repository and its credits remain authoritative. This fork documents **Young-Sang Lee (YSL-RyuDo)'s contributions**, not sole authorship of the game.

The fork uses `0.23Ver` as its default branch because the original `main` contains an early snapshot. Upstream branches and development history are preserved; no pull request or change was sent to the original repository.

[Explore the case](https://ysl-ryudo.github.io/en/work/deathguider/) · [Portfolio](https://ysl-ryudo.github.io/en/)

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider) (Public repository)

## System responsibilities

| Area | Implementation |
|---|---|
| Management | Prisoner/bus lists and storage data |
| Progression | Days, training, recovery, erosion and facilities |
| Preparation | Unit/equipment selection with an empty-party entry guard |

## Development videos

- [DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## My contribution: management systems

- Bus/prisoner management, prisoner lists, storage and their UI/data flow.
- Day progression and management-state updates.
- Training, recovery, erosion and facility-related systems, including research/smithing work.
- Battle preparation: selecting available units/equipment, preventing invalid empty-party entry, and connecting management state to preparation UI.

These responsibilities are supported by authored commits and the `Assets/Script/MainScene/` code. Combat AI, procedural maps and all other teammates' systems are not included in this contribution claim.

## Evidence / 근거 / 根拠

- [Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)
- [Research & smithing / 연구소·대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)
- [Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)
- [Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## Inspecting the project

Open with the Unity version in [ProjectVersion.txt](ProjectSettings/ProjectVersion.txt). Start by inspecting the management scenes and `Assets/Script/MainScene/Lobby Test/` on `0.23Ver`. This documentation update does not certify a new build or playtest. Fork ownership does not transfer authorship or rights in the team's code/assets. Existing source history and credits are preserved.
