# 적용 방법

1. ZIP을 풉니다.
2. GitHub 저장소 `kso-2/wtmg`의 **루트**에 `assets/`와 `game/`을 그대로 올립니다.
3. 저장소 루트가 `assets/`, `game/`으로 시작해야 합니다. `main/assets/`처럼 한 폴더 더 감싸면 안 됩니다.
4. 아래 주소를 브라우저에서 테스트합니다.
   - `https://raw.githubusercontent.com/kso-2/wtmg/main/game/manifest.json`
   - `https://raw.githubusercontent.com/kso-2/wtmg/main/assets/backgrounds/forest_sea/forest_sea_01.webp`
   - `https://raw.githubusercontent.com/kso-2/wtmg/main/assets/characters/protagonists/protagonist_f_01.webp`
   - `https://raw.githubusercontent.com/kso-2/wtmg/main/assets/ui/wood_panel.png`
5. 네 주소가 200으로 열리면 현재 helperfix 소스의 자산 경로와 일치합니다.

## 권장
기존 `main/` 폴더를 남겨도 새 경로가 있으면 로딩은 되지만, 혼동을 피하려면 검증 후 구형 `main/assets` 중복 폴더를 정리하세요.
