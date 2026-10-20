# DeathGuider

[English](README.md), [Korean](README.ko.md), [Japanese](README.ja.md)

오투큐브 공동 제작 게임. 수감자 관리와 시설 운영, 전투 준비를 연결하는 시스템을 담당했습니다.

**O2CUBE 팀 프로젝트**의 포트폴리오 문서용 포크입니다. 원본: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider). 원본 저장소와 기존 크레딧을 존중하며 **이영상(YSL-RyuDo)이 맡은 부분**을 설명합니다. 게임 전체의 단독 제작을 주장하지 않습니다.

원본 main이 초기 상태여서 이 포크는 `0.23Ver`를 기본 브랜치로 사용합니다. 원본 브랜치와 개발 이력을 보존했고 원본 저장소에 변경이나 PR을 보내지 않았습니다.

| 프로젝트 정보 | 내용 |
|---|---|
| 개발 상태 | 담당 작업을 정리한 포크 |
| 사용 기술 | C#, Unity, O2CUBE |

[개발 사례 보기](https://ysl-ryudo.github.io/ko/work/deathguider/), [Portfolio](https://ysl-ryudo.github.io/ko/)

[![DeathGuider](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

[DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## 내 기여: 경영 시스템

버스, 수감자 관리, 수감자 목록, 보관과 UI, 데이터 흐름.

날짜 진행과 경영 상태 갱신.

훈련, 회복, 침식과 시설 시스템, 연구소, 대장장이 관련 작업.

전투 준비: 이용 가능한 인원, 장비 선택, 빈 파티 입장 방지와 경영 데이터의 준비 UI 연결.

작성한 커밋과 `Assets/Script/MainScene/` 코드로 확인되는 담당 범위입니다. 전투 AI, 절차적 맵과 다른 팀원의 시스템을 제 기여로 포함하지 않습니다.

## Evidence / 근거 / 根拠

[Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

[Research & smithing / 연구소, 대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)

[Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)

[Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 구현과 설계

수감자 상태, 시설, 날짜 진행과 전투 준비가 서로 연결되어야 하는 경영 게임입니다. 전투 준비 단계에서는 빈 파티가 입장하지 못하도록 막아야 합니다.

버스, 수감자, 보관 관리, 훈련, 회복, 침식, 연구소, 대장장이, 전투 준비의 인원, 장비 선택을 담당했습니다. 공동 프로젝트 안에서 작성 커밋으로 해당 변경을 구분합니다.

| 영역 | 구현 |
|---|---|
| 경영 | 수감자, 버스 목록과 보관함 데이터 |
| 진행 | 날짜, 훈련, 회복, 침식, 시설 |
| 전투 준비 | 유닛, 장비 선택과 빈 파티 입장 방지 |

## 코드의 동작과 구현 방식을 택한 이유

확인한 구현이 어떤 제약을 다루며 어떤 장단점이 생기는지 설명합니다. 설계 효과에 대한 설명은 코드 분석이며, 비교한 모든 대안을 당시 직접 구현했다는 뜻은 아닙니다. 기여 링크는 공동 프로젝트 안의 담당 변경을 가리키고 소스 링크는 기존 접근 권한을 유지합니다.

### 시설 화면과 유닛 상태를 연결하는 방식

**구현 흐름**

제 경영 시스템 커밋에서는 훈련 완료 처리가 유닛 데이터의 활동 상태를 확인하고 해당 능력치를 변경한 뒤 활동 상태를 초기화하도록 수정했습니다. 회복, 침식, 보관 관련 변경도 함께 포함됩니다. 별도 전투 준비 작업에서는 선택한 인원과 장비를 전투 입장에 연결했습니다.

**이 구조가 필요한 이유**

시설 패널은 화면이고 유닛의 활동과 능력치는 화면 밖에서도 유지되어야 하는 게임 데이터입니다. 유닛 상태를 읽으면 훈련 슬롯의 현재 표시만이 아니라 게임 데이터에 따라 진행 규칙을 적용할 수 있습니다. 활동 상태 초기화도 단순 표시 변경이 아니라 이후 UI와 게임 진행이 함께 따라야 하는 상태 전환입니다.

**대안과 현재 구현의 절충**

시설 슬롯에서 진행을 계산하면 해당 화면에서 추적하기 쉽지만 규칙이 슬롯 표현에 결합될 수 있습니다. 유닛의 활동 데이터를 읽으면 유지되는 게임 객체를 기준으로 처리합니다. 숫자 상태 대신 타입으로 상태를 표현하면 전이를 더 명확히 할 수 있지만 기존 참조 코드와 저장값의 이관이 필요합니다.

**장단점과 검증 범위**

유닛 데이터를 넓게 순회할수록 소유자와 적용 대상 조건을 주의해야 하고, 숫자로 표현한 활동 코드는 규칙을 읽기 어렵게 만듭니다. 이는 검토할 지점이며 기존 구현이 완성된 범용 상태 머신이라는 뜻은 아닙니다. 공동 DateSystem은 팀원의 작성 코드이고 제 담당은 시설과 진행의 연동입니다.

[DeathGuider ee560502](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [DeathGuider 5593c51c](https://github.com/YSL-RyuDo/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 프로젝트 확인

[ProjectVersion.txt](ProjectSettings/ProjectVersion.txt)의 Unity 버전을 사용하세요. `0.23Ver`의 경영 씬과 `Assets/Script/MainScene/Lobby Test/`부터 살펴볼 수 있습니다. 이번 문서 작업은 새 빌드, 플레이 검증을 뜻하지 않습니다. 포크 소유가 팀 코드, 에셋의 저작자나 권리를 이전하지 않습니다. 기존 개발 이력과 크레딧을 유지합니다.

## 관련 저장소

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider), 공개 저장소
