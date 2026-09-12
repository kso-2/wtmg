# SionTRPGViewer v1.6.1 이미지 자산 점검 결과

## 소스/APK 기준
- helperfix source의 `server.js` `DEFAULT_ASSETS` 기준 자산 수: **64개**
  - character 23 / monster 20 / background 15 / event 3 / ui 3
- APK/소스는 위 게임 아트 전체를 내장하지 않고 원격 `asset_base`를 사용합니다.
- 기대 원격 루트: `https://raw.githubusercontent.com/kso-2/wtmg/main/assets/`

## 기존 wtmg.zip에서 발견한 문제
1. Git 저장소 루트 아래에 `main/assets/...`가 있어 앱이 요청하는 `assets/...`와 한 단계 어긋나 있습니다.
2. 캐릭터 20개는 추가로 `characters/allies/` 아래에 잘못 중첩되어 있었습니다.
3. 아래 24개는 저장소에 원본 파일 자체가 없었습니다.

### 실제 파일 부재 24개
- `npc_major_01` → `assets/characters/npc_major/npc_major_01.png`
- `npc_major_02` → `assets/characters/npc_major/npc_major_02.png`
- `npc_major_03` → `assets/characters/npc_major/npc_major_03.png`
- `forest_sea_01` → `assets/backgrounds/forest_sea/forest_sea_01.webp`
- `forest_sea_02` → `assets/backgrounds/forest_sea/forest_sea_02.webp`
- `forest_sea_03` → `assets/backgrounds/forest_sea/forest_sea_03.webp`
- `sky_archipelago_01` → `assets/backgrounds/sky_archipelago/sky_archipelago_01.webp`
- `sky_archipelago_02` → `assets/backgrounds/sky_archipelago/sky_archipelago_02.webp`
- `sky_archipelago_03` → `assets/backgrounds/sky_archipelago/sky_archipelago_03.webp`
- `labyrinth_01` → `assets/backgrounds/labyrinth/labyrinth_01.webp`
- `labyrinth_02` → `assets/backgrounds/labyrinth/labyrinth_02.webp`
- `labyrinth_03` → `assets/backgrounds/labyrinth/labyrinth_03.webp`
- `forest_city_exterior` → `assets/backgrounds/cities/forest_city_exterior.webp`
- `forest_city_interior` → `assets/backgrounds/cities/forest_city_interior.webp`
- `sky_city_exterior` → `assets/backgrounds/cities/sky_city_exterior.webp`
- `sky_city_interior` → `assets/backgrounds/cities/sky_city_interior.webp`
- `labyrinth_city_exterior` → `assets/backgrounds/cities/labyrinth_city_exterior.webp`
- `labyrinth_city_interior` → `assets/backgrounds/cities/labyrinth_city_interior.webp`
- `event_sunset_meeting` → `assets/events/event_sunset_meeting.webp`
- `event_ancient_guardian` → `assets/events/event_ancient_guardian.webp`
- `event_sky_islands` → `assets/events/event_sky_islands.webp`
- `status_scroll_frame` → `assets/ui/status_scroll_frame.png`
- `event_frame` → `assets/ui/event_frame.png`
- `wood_panel` → `assets/ui/wood_panel.png`

## 이 패키지에서 한 처리
- 기존에 존재하던 자산은 helperfix 소스가 요구하는 정확한 경로로 재배치했습니다.
- 원본 파일이 없던 24개는 **즉시 동작 테스트가 가능한 기능성 fallback**을 만들었습니다.
- 중요 NPC 3장은 사용자가 올린 저장소의 캐릭터 일러스트를 정사각형 초상화로 크롭했습니다.
- 배경/이벤트 CG는 사용자가 올린 `status_bg.webp`를 기반으로 색보정·안개·구도·실내 프레임 등을 가공했습니다.
- UI 3장은 제3자 비트맵을 복제하지 않고 단순 프레임/패널을 새로 구성했습니다.

> 이 fallback 24개는 “경로와 렌더링 검증용 즉시 사용본”입니다. 출시용 최종 아트는 아래 CC0 후보로 교체하는 것을 권장합니다. 사용자가 제공한 원본 일러스트의 라이선스는 이 작업에서 독립적으로 검증하지 않았습니다.
