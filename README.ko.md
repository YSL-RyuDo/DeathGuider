# DeathGuider

<!-- portfolio-languages -->
[![English](https://ysl-ryudo.github.io/assets/diagrams/language-en.svg)](README.md) [![한국어 (현재 언어)](https://ysl-ryudo.github.io/assets/diagrams/language-ko-current.svg)](README.ko.md) [![日本語](https://ysl-ryudo.github.io/assets/diagrams/language-ja.svg)](README.ja.md)
<!-- /portfolio-languages -->

오투큐브 공동 제작 게임. 수감자 관리와 시설 운영, 전투 준비를 연결하는 시스템을 담당했습니다.

O2CUBE 팀 프로젝트. 원본 저장소: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider).

| 프로젝트 정보 | 내용 |
|---|---|
| 개발 상태 | 담당 작업을 정리한 포크 |
| 사용 기술 | C#, Unity, O2CUBE |

[개발 사례 보기](https://ysl-ryudo.github.io/ko/work/deathguider/), [Portfolio](https://ysl-ryudo.github.io/ko/)

[![DeathGuider](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

[DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## 게임에서 보는 구현

[![수감자 후보 생성과 일일 수락 제한, 보유 명단을 연결한 모집 화면.](https://ysl-ryudo.github.io/assets/gameplay/deathguider-recruitment.webp)](https://ysl-ryudo.github.io/assets/gameplay/deathguider-recruitment.webp)

수감자 후보 생성과 일일 수락 제한, 보유 명단을 연결한 모집 화면.

[![파티 슬롯과 장비 선택, 던전 입장을 연결한 관리 화면.](https://ysl-ryudo.github.io/assets/gameplay/deathguider-party.webp)](https://ysl-ryudo.github.io/assets/gameplay/deathguider-party.webp)

파티 슬롯과 장비 선택, 던전 입장을 연결한 관리 화면.

## 게임 전체에서 맡은 구현

유닛 모집과 보관, 훈련과 회복 및 침식, 연구와 장비 제작, 탐사 전 파티와 장비 준비를 담당했습니다.

[![담당 구현 흐름](https://ysl-ryudo.github.io/assets/diagrams/deathguider-flow-ko.svg)](https://ysl-ryudo.github.io/assets/diagrams/deathguider-flow-ko.svg)

### 모집과 유닛 보관

무작위 수감자 모집과 버스 UI, 유닛 보관과 선택을 작업했습니다. 모집한 유닛을 경영 화면과 이후의 파티 준비에 연결하는 시스템입니다.

[BusRandomPrisoner.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Bus/BusRandomPrisoner.cs), [내 변경 fc21ab5](https://github.com/YSL-RyuDo/DeathGuider/commit/fc21ab5eb4e66a8c14ed5de5e9a261ffbb7242f6), [StorageUI.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Floor/StorageUI.cs), [내 변경 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### 훈련, 회복과 침식

훈련과 회복, 침식 처리를 구현하고 수정했습니다. 시설 진행은 유닛의 활동 데이터를 읽습니다. 화면 슬롯의 점유만으로 진행을 계산하던 구조를 바꾼 내용은 아래에서 설명합니다.

[GYMSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/GYM/GYMSystem.cs), [내 변경 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [HealthSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Health/HealthSystem.cs), [내 변경 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [ErosionSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Erosion/ErosionSystem.cs), [내 변경 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### 연구와 제작

경영 흐름의 연구소와 제작 시스템을 작업했습니다. 개발 선택과 자원 및 상태 처리를 전투 전에 사용할 장비와 연결했습니다.

[LaboratorySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Laboratory/LaboratorySystem.cs), [내 변경 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2), [SmithSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Smith/SmithSystem.cs), [내 변경 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2)

### 파티와 장비 준비

전투 유닛과 장비 선택, 비어 있는 파티의 전투 진입을 막는 처리를 작업했습니다. 제가 맡은 경영 흐름을 팀의 탐사와 전투 시스템에 연결하는 경계입니다.

[BattleReadySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/BattleReadySystem.cs), [내 변경 f8015e0](https://github.com/YSL-RyuDo/DeathGuider/commit/f8015e039aa7e33d9e8355f3d09cd90c786a04c8)

## Evidence / 근거 / 根拠

[Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

[Research & smithing / 연구소, 대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)

[Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)

[Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 구현과 설계

수감자 상태, 시설, 날짜 진행과 전투 준비가 서로 연결되어야 하는 경영 게임입니다. 전투 준비 단계에서는 빈 파티가 입장하지 못하도록 막아야 합니다.

버스, 수감자, 보관 관리, 훈련, 회복, 침식, 연구소, 대장장이, 전투 준비의 인원, 장비 선택을 담당했습니다. 공동 프로젝트 안에서 작성 커밋으로 해당 변경을 구분합니다.

## 코드의 동작과 구현 방식을 택한 이유

### 시설 화면과 유닛 상태를 연결하는 방식

**구현 흐름**

제 경영 시스템 커밋에서는 훈련 완료 처리가 유닛 데이터의 활동 상태를 확인하고 해당 능력치를 변경한 뒤 활동 상태를 초기화하도록 수정했습니다. 회복, 침식, 보관 관련 변경도 함께 포함됩니다. 별도 전투 준비 작업에서는 선택한 인원과 장비를 전투 입장에 연결했습니다.

**이 구조가 필요한 이유**

시설 패널은 화면이고 유닛의 활동과 능력치는 화면 밖에서도 유지되어야 하는 게임 데이터입니다. 유닛 상태를 읽으면 훈련 슬롯의 현재 표시만이 아니라 게임 데이터에 따라 진행 규칙을 적용할 수 있습니다. 활동 상태 초기화도 단순 표시 변경이 아니라 이후 UI와 게임 진행이 함께 따라야 하는 상태 전환입니다.

**대안과 현재 구현의 절충**

시설 슬롯에서 진행을 계산하면 해당 화면에서 추적하기 쉽지만 규칙이 슬롯 표현에 결합될 수 있습니다. 유닛의 활동 데이터를 읽으면 유지되는 게임 객체를 기준으로 처리합니다. 숫자 상태 대신 타입으로 상태를 표현하면 전이를 더 명확히 할 수 있지만 기존 참조 코드와 저장값의 이관이 필요합니다.

**장단점과 검증 범위**

유닛 데이터를 순회할 때 소유자와 활동 상태를 걸러야 합니다. 숫자로 표현한 활동 코드는 규칙을 읽기 어렵게 만들며, 시설 진행 시점을 게임의 날짜 변경 이벤트와 맞춰야 합니다.

[DeathGuider ee560502](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [DeathGuider 5593c51c](https://github.com/YSL-RyuDo/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 프로젝트 확인

[ProjectVersion.txt](ProjectSettings/ProjectVersion.txt)의 Unity 버전을 사용하세요. `0.23Ver`의 경영 씬과 `Assets/Script/MainScene/Lobby Test/`부터 살펴볼 수 있습니다.

## 관련 저장소

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider), 공개 저장소
