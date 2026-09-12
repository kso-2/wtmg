# SionTRPGViewer v1.6.1 VFX Ready Pack

## 추천 적용 방식
이 압축의 `assets/`와 `game/` 폴더를 GitHub 저장소 `kso-2/wtmg`의 루트에 그대로 병합하세요.

최종 구조 예시:
- assets/effects/slash/effect.webp
- assets/effects/pierce/effect.webp
- ...
- assets/effects/poison/effect.webp
- game/effects/effects.json

## 왜 이 구성을 선택했나
- 13종 전체를 PVFX Foundry 계열로 통일해 픽셀 스타일과 96x96 기준을 맞춤.
- PVFX Foundry 배포 ZIP 내부에 CC0 1.0 라이선스가 명확히 포함됨.
- 현재 TRPGViewer가 기대하는 `assets/effects/<id>/effect.webp` 구조에 바로 맞춤.
- 모든 애니메이션은 20 FPS(프레임당 50ms)의 lossless animated WebP로 변환.
- `pierce`는 Magical Projectile을 은백색으로 변환해 물리 찌르기 계열로 사용.
- `wind_slash`는 Crescent Slash를 청록/백색으로 변환해 바람 속성을 구분.
- `blunt`는 Landing Dust를 사용해 전기 속성과 혼동되는 타격광을 피함.

## 선별 매핑
| ID | 한국어 | 원본 PVFX | 처리 |
|---|---|---|---|
| slash | 베기 | crescent-slash | 원본 |
| pierce | 찌르기 | magical-projectile | 은백색 변환 |
| blunt | 때리기 | landing-dust | 원본 |
| fire | 불 | ember-jet | 원본 |
| ice | 얼음 | frost-nova | 원본 |
| wind_slash | 바람칼날 | crescent-slash | 청록/백색 변환 |
| lightning | 번개 | electric-impact | 원본 |
| rockfall | 낙석 | earth-rupture | 원본 |
| light | 빛 | solar-shrapnel | 원본 |
| dark | 어둠 | void-implosion | 원본 |
| roots | 나무뿌리 | rootscript | 원본 |
| explosion | 폭발 | warm-explosion | 원본 |
| poison | 독 | acid-splash | 원본 |

## GitHub 적용 후 확인
예:
`https://raw.githubusercontent.com/kso-2/wtmg/main/assets/effects/fire/effect.webp`

이 주소가 브라우저에서 열리면 자산 경로는 정상입니다.

`game/effects/effects.json`도 함께 올리면 v1.6.1의 원격 문서 로더가 해당 정의를 가져올 수 있습니다.
현재 `game/manifest.json`이 없어도 내장 manifest fallback이 `effects/effects.json` 경로를 알고 있으므로 이 효과 패키지 적용에는 필수는 아닙니다.

## 라이선스
선별 및 변환에 사용한 PVFX Foundry sprite sheets는 업로드된 배포본의 `LICENSE.txt` 기준 CC0 1.0 Universal 범위입니다.
원문은 `LICENSES/PVFX_FOUNDRY_CC0_LICENSE.txt`에 동봉했습니다.

## 제외한 업로드 팩
- `vfx_free_pack.zip`
- `Everything.zip`

두 압축에는 확인 가능한 라이선스 문서가 함께 들어 있지 않았기 때문에, 이번 배포용 압축에는 포함하지 않았습니다.
