# 이미지/자산 점검 보고서

## [확인된 원인]
- 업로드된 저장소는 Git 브랜치 루트 아래에 다시 `main/` 폴더가 있어 플러그인이 기대하는 Raw 경로와 1단계 어긋나 있었습니다.
- 주인공/NPC/기본 동료 이미지도 `characters/allies/...` 아래에 추가 중첩되어 있었습니다.
- 이 패치 준비본에서는 저장소 루트에 `assets/`, `game/`이 오도록 평탄화하고, 캐릭터 파일을 기대 경로에도 복사했습니다.

## [이미지 크기]
- 몬스터 파일: 약 1254×1254, 1.4~2.0MB. 웹 로딩에 다소 무겁지만, 파일이 아예 표시되지 않는 직접 원인은 경로 불일치 쪽이 더 명확합니다.
- VFX: 96×96, 수 KB 수준으로 크기 문제와 무관합니다.

## [경로 수정 후에도 실제로 없는 기본 자산: 24개]
- `npc_major_01` (character) → `assets/characters/npc_major/npc_major_01.png`
- `npc_major_02` (character) → `assets/characters/npc_major/npc_major_02.png`
- `npc_major_03` (character) → `assets/characters/npc_major/npc_major_03.png`
- `forest_sea_01` (background) → `assets/backgrounds/forest_sea/forest_sea_01.webp`
- `forest_sea_02` (background) → `assets/backgrounds/forest_sea/forest_sea_02.webp`
- `forest_sea_03` (background) → `assets/backgrounds/forest_sea/forest_sea_03.webp`
- `sky_archipelago_01` (background) → `assets/backgrounds/sky_archipelago/sky_archipelago_01.webp`
- `sky_archipelago_02` (background) → `assets/backgrounds/sky_archipelago/sky_archipelago_02.webp`
- `sky_archipelago_03` (background) → `assets/backgrounds/sky_archipelago/sky_archipelago_03.webp`
- `labyrinth_01` (background) → `assets/backgrounds/labyrinth/labyrinth_01.webp`
- `labyrinth_02` (background) → `assets/backgrounds/labyrinth/labyrinth_02.webp`
- `labyrinth_03` (background) → `assets/backgrounds/labyrinth/labyrinth_03.webp`
- `forest_city_exterior` (background) → `assets/backgrounds/cities/forest_city_exterior.webp`
- `forest_city_interior` (background) → `assets/backgrounds/cities/forest_city_interior.webp`
- `sky_city_exterior` (background) → `assets/backgrounds/cities/sky_city_exterior.webp`
- `sky_city_interior` (background) → `assets/backgrounds/cities/sky_city_interior.webp`
- `labyrinth_city_exterior` (background) → `assets/backgrounds/cities/labyrinth_city_exterior.webp`
- `labyrinth_city_interior` (background) → `assets/backgrounds/cities/labyrinth_city_interior.webp`
- `event_sunset_meeting` (event) → `assets/events/event_sunset_meeting.webp`
- `event_ancient_guardian` (event) → `assets/events/event_ancient_guardian.webp`
- `event_sky_islands` (event) → `assets/events/event_sky_islands.webp`
- `status_scroll_frame` (ui) → `assets/ui/status_scroll_frame.png`
- `event_frame` (ui) → `assets/ui/event_frame.png`
- `wood_panel` (ui) → `assets/ui/wood_panel.png`