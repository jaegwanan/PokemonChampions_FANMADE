# PokemonChampions_FANMADE(Console C++)

## 프로젝트 소개

Pokemon Champions의 대전 시스템을 참고하여 제작하는 콘솔 기반 턴제 포켓몬 배틀 시뮬레이터입니다.

본 프로젝트는 C++ 객체지향 설계, 파일 시스템 기반 데이터 관리, AI 시스템, 턴제 전투 로직 구현을 목표로 합니다.

학습 및 포트폴리오 목적으로 개발되며, 상업적 이용을 목적으로 하지 않습니다. (문제 시 바로 내리도록 하겠습니다.)

---

# 개발 목표

* 객체지향 설계를 활용한 포켓몬 배틀 시스템 구현
* 콘솔 환경에서 UI 시스템 구현
* 데이터 기반 포켓몬 및 기술 관리
* NPC AI 구현
* 노력치, 성격, 기술 배치 등 육성 시스템 반영
* 추후 온라인 대전 기능 확장 가능하도록 설계

---

# 주요 기능

## 1. 대전 시스템

### 기본 배틀

* 1 vs 1 포켓몬 배틀 (더블배틀은 추후 추가 예정)
* 턴 기반 전투
* 속도에 따른 행동 순서 결정
* 기술 사용
* 포켓몬 교체
* 기절(Faint) 처리
* 승패 판정
* TOD

### 기술 시스템

* 물리 기술
* 특수 기술
* 변화 기술
* PP 관리
* 명중률 판정
* 우선도(Priority) 적용

### 타입 상성

* 타입별 상성 적용
* 효과 굉장함
* 효과 별로
* 효과 없음

### 상태 이상

* 화상(Burn)
* 독(Poison)
* 마비(Paralysis)
* 수면(Sleep)
* 얼음(Freeze)
* 혼란(Confusion)
---

## 2. 육성 시스템

### 레벨 시스템

* 레벨은 모두 고정

### 노력치(EV)

* HP
* 공격
* 방어
* 특수공격
* 특수방어
* 스피드

### 성격(Nature)

* 능력치 증가
* 능력치 감소

예시

* 고집 (공격↑ 특공↓)
* 겁쟁이 (스피드↑ 공격↓)
* 조심 (특공↑ 공격↓)

### 기술 배치

* 최대 4개 기술 장착
* 기술 교체
* 기술 습득

---

## 3. AI 시스템  
- 최대한 구현 예정 -
* 가장 높은 기대 데미지 계산
* 타입 상성 고려
* 포켓몬 교체 판단
* 상태이상 활용
* 마무리 기술 선택
* 공격 우선도 판단

---

## 4. UI 시스템

### 콘솔 UI

* 전투 화면
* 포켓몬 정보 표시
* 트레이너 정보 표시
* 기술 선택 창
* 메시지 출력 창

### 체력 바

* HP Bar

### ASCII Sprite

* 포켓몬 도트 출력
* 트레이너 도트 출력

### 애니메이션(가능하면)

* 공격 애니메이션
* 데미지 연출
* 상태이상 연출 

---

## 5. 데이터 시스템

파일 기반 데이터 관리

### Pokemon Data

* 종족값
* 타입
* 진화 정보

### Move Data

* 기술 정보
* 위력
* 명중률
* PP

### Nature Data

* 성격 정보

### Type Chart

* 타입 상성 정보

---

# 데이터 구조

```txt
assets/
│
├── pokemon.csv
├── moves.csv
├── learnsets.csv
├── natures.csv
├── typechart.csv
│
└── sprites/
    ├── pikachu.txt
    ├── charizard.txt
    └── ...
```

---

# 프로젝트 구조

```txt
src/
│
├── core/
│   ├── GameManager
│   ├── SceneManager
│   └── InputManager
│
├── pokemon/
│   ├── Pokemon
│   ├── PokemonSpecies
│   ├── Nature
│   ├── EV
│   └── IV
│
├── move/
│   ├── Move
│   └── MoveData
│
├── trainer/
│   ├── Trainer
│   ├── Player
│   └── NPCTrainer
│
├── battle/
│   ├── Battle
│   ├── DamageCalculator
│   └── BattleAction
│
├── ai/
│   └── BattleAI
│
├── ui/
│   ├── UIManager
│   ├── BattleUI
│   └── ConsoleRenderer
│
├── data/
│   ├── DataManager
│   ├── CsvReader
│   └── TypeChart
│
└── save/
    └── SaveManager
```

---

# 개발 로드맵

## Phase 1 - 기반 구조

* [ ] 클래스 설계
* [ ] UML 클래스 다이어그램 작성
* [ ] CSV 로더 구현
* [ ] 포켓몬 데이터 로딩

## Phase 2 - 배틀 시스템

* [ ] Pokemon 클래스 구현
* [ ] Move 클래스 구현
* [ ] DamageCalculator 구현
* [ ] Battle 시스템 구현

## Phase 3 - UI

* [ ] UIManager 구현
* [ ] 전투 화면 구현
* [ ] HP Bar 구현
* [ ] ASCII Sprite 출력

## Phase 4 - 육성 시스템

* [ ] 노력치 구현
* [ ] 성격 구현
* [ ] 레벨업 구현

## Phase 5 - AI

* [ ] 랜덤 AI
* [ ] 타입 상성 고려 AI
* [ ] 교체 AI

## Phase 6 - 확장 기능

* [ ] 저장 시스템
* [ ] 팀 편성 기능
* [ ] 랭킹 시스템
* [ ] 온라인 대전

```

---

## 개발 환경

- Language : C++17 이상
- IDE : Visual Studio 2022
- Version Control : Git / GitHub
- Data Storage : CSV File System
- Platform : Windows Console

---

## 참고

본 프로젝트는 Pokémon Champions의 전투 시스템에서 영감을 받은 비상업적 학습 프로젝트입니다.

All Pokémon-related trademarks and copyrights belong to Nintendo, Game Freak, and The Pokémon Company.
```
