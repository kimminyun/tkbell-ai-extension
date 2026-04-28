# 띵커벨 AI 문제 생성기 (Chrome 확장)

띵커벨 편집기에서 학년·교과·단원에 맞는 문제를 AI로 자동 생성합니다.

## 선생님용 설치 방법

> **사용 조건**: 학교 내부망 PC에서만 동작합니다 (백엔드 서버가 교내 IP에 있음).

1. 받으신 `install.reg` 파일을 더블클릭합니다.
2. "이 변경 내용을 추가하시겠습니까?" → **예** 클릭.
   - 관리자 권한이 필요할 수 있습니다 (UAC 창이 뜨면 "예").
3. **Chrome을 완전히 종료한 뒤 다시 실행**합니다.
   - 작업 표시줄/시스템 트레이의 Chrome도 모두 닫혀야 합니다.
4. `chrome://extensions/` 주소로 이동해서 "띵커벨 AI 문제 생성기"가 보이면 설치 완료.
5. 띵커벨 에디터(`https://www.tkbell.co.kr/user/editor/editorQuiz.do`)로 이동.
6. 화면 우측 하단의 **🤖 AI 문제 생성** 버튼을 클릭해서 사용합니다.

## 자동 업데이트

레지스트리 정책으로 강제 설치되어 있어서, 새 버전이 올라오면 Chrome 재시작 시 자동으로 갱신됩니다.

## 문제가 있을 때

- 확장이 안 보이면: Chrome 완전 재시작 후에도 안 나오면 PC 재부팅.
- "🤖 AI 문제 생성" 버튼이 안 보이면: 띵커벨 편집기 페이지인지 확인 (URL에 `editorQuiz.do` 포함).
- 문제 생성이 안 되면: 학교 와이파이/유선망에 연결되어 있는지 확인.

## 제거 방법

`chrome://extensions/`에서 직접 제거가 안 됩니다(정책 강제 설치). 제거하려면:

1. 시작 → "regedit" 실행 (관리자 권한)
2. `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome\ExtensionInstallForcelist` 및
   `HKEY_CURRENT_USER\SOFTWARE\Policies\Google\Chrome\ExtensionInstallForcelist` 항목에서
   `dpogcbgnkacojlbbnkmnkcddaamnmmon`이 포함된 값을 삭제.
3. Chrome 재시작.
