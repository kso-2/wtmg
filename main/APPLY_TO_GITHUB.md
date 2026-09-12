# 적용 안내

이 ZIP은 `wtmg` GitHub 저장소에 올리기 위한 **패치 준비본**입니다.

## [바로 적용 가능한 항목]
1. 저장소 구조를 `assets/`, `game/` 루트 구조로 수정
2. 주인공 / 중립 NPC / 기본 동료의 잘못 중첩된 경로를 호환 경로에 복사
3. `game/manifest.json` 추가
4. `game/skills/skills.json`을 명확한 5e식 효과 설명으로 확장
5. `game/traits/traits.json` 추가
6. 누락 이미지 목록과 무료 소스 후보 문서화

GitHub 저장소에서 기존 루트의 `main/` 폴더 안 내용물을 루트로 이동시키거나,
이 ZIP의 내용으로 저장소 루트를 구성하세요.

정상 예:
`https://raw.githubusercontent.com/kso-2/wtmg/main/assets/monsters/beasts/beast_01.webp`
`https://raw.githubusercontent.com/kso-2/wtmg/main/game/manifest.json`

## [예정 항목]
전투 UI, 상태창 UI, 서술형 캐릭터 메이킹 완료 처리는 플러그인/앱 소스가 필요합니다.
자세한 구현 명세는 `PLANNED/` 폴더에 있습니다.
