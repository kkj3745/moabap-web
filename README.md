# 모아밥 · 같이밥 체험 (웹)

저장해 둔 맛집을 모아 친구들과 함께 정하는 앱 **모아밥**의 같이밥 흐름을 웹에서 체험하는 프로토타입입니다.
날짜·음식·거리를 고르면 AI 추천 후보 5곳이 나오고, 투표까지 해 볼 수 있습니다. (후보와 투표 수는 샘플 데이터)

- 데모: https://kkj3745.github.io/moabap-web/
- `index.html`: 데스크톱 웹(홈·저장·모아맵·같이밥·상세), `m.html`: 모바일 간단 체험. 화면 너비로 자동 이동합니다. 빌드 도구 없이 파일만 열면 동작합니다.
- 이용 기록: Amplitude + GA4 (`index.html` 상단 `CONFIG`에 키를 넣었을 때만 전송, 비어 있으면 콘솔에만 기록)
- 이벤트: place_saved(링크로 맛집 저장·체험), place_save_failed, invite_opened, group_link_opened(초대 링크), experience_started, conditions_started, conditions_submitted, candidates_generated, reco_card_clicked, vote_cast, group_vote_completed, reservation_completed(체험·simulated:true), install_button_clicked, outbound_clicked, feedback_submitted
- A/B(방문자별 무작위 배정, 모든 이벤트에 속성으로 포함): reason_variant(추천 이유 문구 유무), chip_variant(카드에 시간 칩 노출 vs 상세에서만), mylist_variant(내 저장 포함 가능 vs 불가)
- 예약은 실제로 이루어지지 않는 체험용입니다. 식당과 투표 수는 샘플 데이터입니다.
- URL 옵션: `?room=방ID&src=유입경로&host=이름&name=모임이름` (테스트용: `&v_reason=with|without&v_chip=chip|detail&v_mylist=on|off`로 변형 고정, 이 경우 forced_variant=true라 집계에서 제외`
- 개인정보처리방침: https://kkj3745.github.io/moabap-privacy/

## 라이선스
코드는 MIT입니다. `photos/`의 음식 사진은 MIT 대상이 아니며 재사용을 허락하지 않습니다.
