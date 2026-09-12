# [예정 항목] 서술형 캐릭터 메이킹 완료 처리

## 판정
마지막 운명 선택 이후 화면이 완료되지 않는 것은 정상 동작으로 보기 어렵습니다.

v1.6.1 API 구조상:
1. `start_character_creation`은 생성 규칙/선택지를 시작하는 역할입니다.
2. 실제 캐릭터 저장 완료는 `build_character_from_description` 또는 `roll_character_creation`이 담당합니다.
3. 따라서 마지막 서술형/타로 선택이 끝났다면 클라이언트가 최종 선택값을 모아 `build_character_from_description`을 호출해야 합니다.

## 수정 권장
마지막 선택 직후:
- 모든 필수 선택 검증
- 완성 요약 화면 표시
- `캐릭터 생성 완료` 버튼 활성화
- 버튼 클릭 시 `build_character_from_description`
- 성공 응답 후 `get_character_state`로 저장 결과 검증
- 실패 시 선택 화면을 유지하고 오류 메시지 표시

자동 완료를 원하면 마지막 선택 직후 바로 build 호출할 수도 있으나,
사용자가 능력치/배경/직업을 최종 확인할 수 있도록 명시적인 완료 버튼을 두는 방식을 권장합니다.
