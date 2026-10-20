# DeathGuider — Team Contribution Portfolio

[English](README.md) · [Korean](README.ko.md) · [Japanese](README.ja.md)

**C# · Unity · O2CUBE** · 담당 작업을 정리한 포크

[개발 사례 보기](https://ysl-ryudo.github.io/ko/work/deathguider/) · [Portfolio](https://ysl-ryudo.github.io/ko/)


**O2CUBE 팀 프로젝트**의 포트폴리오 문서용 포크입니다. 원본: [vliza321/DeathGuider](https://github.com/vliza321/DeathGuider). 원본 저장소와 기존 크레딧을 존중하며 **이영상(YSL-RyuDo)이 맡은 부분**을 설명합니다. 게임 전체의 단독 제작을 주장하지 않습니다.

원본 main이 초기 상태여서 이 포크는 `0.23Ver`를 기본 브랜치로 사용합니다. 원본 브랜치와 개발 이력을 보존했고 원본 저장소에 변경이나 PR을 보내지 않았습니다.

## 해결하려던 문제

수감자 상태, 시설, 날짜 진행과 전투 준비가 서로 연결되어야 하는 경영 게임입니다. 전투 준비 단계에서는 빈 파티가 입장하지 못하도록 막아야 합니다.

## 내 구현과 설계

버스·수감자·보관 관리, 훈련·회복·침식, 연구소·대장장이, 전투 준비의 인원·장비 선택을 담당했습니다. 공동 프로젝트 안에서 작성 커밋으로 해당 변경을 구분합니다.

### 구현 개요 · 개념 흐름도

```mermaid
flowchart LR
    N0["Prisoner / storage"] --> N1
    N1["Facilities / day"] --> N2
    N2["Units / equipment"] --> N3
    N3["Battle preparation"]
```

### 개발 시연 영상

[![DeathGuider — DeathGuider demo](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

- [DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

촬영 당시의 프로젝트 시연입니다. 게임 안에서 제가 맡은 작업은 아래 기여 항목으로 구분합니다.

## 내 기여: 경영 시스템

- 버스·수감자 관리, 수감자 목록·보관과 UI·데이터 흐름.
- 날짜 진행과 경영 상태 갱신.
- 훈련·회복·침식과 시설 시스템, 연구소·대장장이 관련 작업.
- 전투 준비: 이용 가능한 인원·장비 선택, 빈 파티 입장 방지와 경영 데이터의 준비 UI 연결.

작성한 커밋과 `Assets/Script/MainScene/` 코드로 확인되는 담당 범위입니다. 전투 AI·절차적 맵과 다른 팀원의 시스템을 제 기여로 포함하지 않습니다.

## Evidence / 근거 / 根拠

- [Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)
- [Research & smithing / 연구소·대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)
- [Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)
- [Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 프로젝트 확인

[ProjectVersion.txt](ProjectSettings/ProjectVersion.txt)의 Unity 버전을 사용하세요. `0.23Ver`의 경영 씬과 `Assets/Script/MainScene/Lobby Test/`부터 살펴볼 수 있습니다. 이번 문서 작업은 새 빌드·플레이 검증을 뜻하지 않습니다. 포크 소유가 팀 코드·에셋의 저작자나 권리를 이전하지 않습니다. 기존 개발 이력과 크레딧을 유지합니다.

## 구현을 확인하는 방법

0.23Ver의 기여 커밋 4개와 MainScene 경영 스크립트부터 살펴보세요. 전투 AI와 절차적 맵 생성은 이 담당 범위에 포함하지 않습니다.
