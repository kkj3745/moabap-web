# 모아밥 · 같이밥 체험 (웹)

저장해 둔 맛집을 모아 친구들과 함께 정하는 앱 **모아밥**의 같이밥 흐름을 웹에서 체험하는 프로토타입입니다.
날짜·음식·거리를 고르면 AI 추천 후보 5곳이 나오고, 투표까지 해 볼 수 있습니다. (후보와 투표 수는 샘플 데이터)

- 데모: https://kkj3745.github.io/moabap-web/
- 단일 `index.html` (빌드 도구 없음). 파일을 열기만 하면 동작합니다.
- 이용 기록: Amplitude + GA4 (`index.html` 상단 `CONFIG`에 키를 넣었을 때만 전송, 비어 있으면 콘솔에만 기록)
- 이벤트: invite_opened, conditions_started, conditions_submitted, candidates_generated, candidates_viewed, vote_cast, vote_completed, feedback_submitted
- URL 옵션: `?room=방ID&src=유입경로&host=이름&name=모임이름`
- 개인정보처리방침: https://kkj3745.github.io/moabap-privacy/

## 라이선스
코드는 MIT입니다. `photos/`의 음식 사진은 MIT 대상이 아니며 재사용을 허락하지 않습니다.
