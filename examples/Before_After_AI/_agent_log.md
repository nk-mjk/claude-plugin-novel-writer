# 에이전트 실행 로그 — Before/After AI (풀 파이프라인 실측)

> novel-writer 풀 파이프라인 1회 통짜 완주 실측. 각 Agent 호출의 usage·agentId 기록.

- novel-writer:story-arc | 담당: story-bible 설계 | 토큰 26818 | 도구 2회 | 210초 | a697bd754f9d87c3b | 완료
- novel-writer:episode-writer | 담당: 1화 작은 편의 | 토큰 31838 | 도구 2회 | 144초 | a74504d39985cd15a | 완료
- novel-writer:episode-writer | 담당: 2화 표준이 된 지름길 | 토큰 32430 | 도구 3회 | 150초 | abc11790c32857eeb | 완료
- novel-writer:episode-writer | 담당: 3화 진짜가 흔들리다 | 토큰 32728 | 도구 4회 | 152초 | a5de78759986119cb | 완료
- novel-writer:episode-writer | 담당: 4화 판단을 넘기다 | 토큰 33267 | 도구 3회 | 165초 | a0764278d5454110e | 완료
- novel-writer:episode-writer | 담당: 5화 돌이킬 수 없는 자리 | 토큰 32285 | 도구 2회 | 143초 | af4784319624f17e1 | 완료
- [실측·병렬 동시성] ep03 작가가 집필 시점 ep02.md 미생성 확인(5개 동시 실행 증거). story-bible이 유일한 공유 레일로 작동 → 격리 경계 재확인. 인접 화 디테일(2화 오류=정확한 얼굴/틀린 숫자 vs 3화 소품=어긋난 날짜) 정합은 Phase3 검수에서 조정.
- novel-writer:character-actor | 담당: 3화 강선생 recast(폐업 장면) | 토큰 12507 | 도구 0회 | 15초 | a953283750f3b1ca3 | 완료
- [실측·연기패스 recast] 카드를 이미 충실히 따른 핵심 장면은 recast 효과가 '미세 심화'(말버릇 "사람이 말이야" 삽입·호흡·어깨 동작 애틋화). 평면적 대사일수록 효과 큼 명제 재확인.
- novel-writer:character-actor | 담당: 4화 핑퐁 T1 세라 | 토큰 11104 | 도구 0회 | 8초 | a7c155fbd37ee2556 | 완료
- novel-writer:character-actor | 담당: 4화 핑퐁 T2 도윤 | 토큰 11178 | 도구 0회 | 10초 | a61bf282bb8bcb3ff | 완료
- novel-writer:character-actor | 담당: 4화 핑퐁 T3 세라(펀치라인) | 토큰 11383 | 도구 0회 | 9초 | af080cb7d16fcba1f | 완료
- novel-writer:character-actor | 담당: 4화 핑퐁 T4 도윤(회피정점) | 토큰 11206 | 도구 0회 | 8초 | a354c248d913b77dd | 완료
- [실측·연기패스 react 핑퐁] 4턴 순차 중계 작동. 비유·논리가 두 입을 오가며 누적/전이(도윤 "자동화·내 일" → 세라 "뭘 넘기는지" 정면 충돌). recast(미세)보다 react(누적)가 장면 긴장 ↑ = story-bible 노트 재확인. ★호칭 함정: character-actor가 나이차(34vs29)로 "선배" 자생성 → 초고 "도윤 씨"로 감독이 교체 통일. 워커는 장면 밖 호칭규칙을 모름 → 감독 중계 필수.
- novel-writer:flow-checker | 담당: 흐름·연속성 검수(전체) | 토큰 71160 | 도구 7회 | 204초 | ad2e2e2a6c29640c8 | 완료
- novel-writer:fact-checker | 담당: 사실·세계관 검수(전체) | 토큰 70690 | 도구 7회 | 204초 | a98ba1cc61facd863 | 완료
- [실측·검수] 두 검수자 독립 작업이 동일 핵심결함에 합치 → ep02(숫자)↔ep03(날짜) 오류 정체 불일치(병렬 집필 취약점, 사전 예측 적중). 부가: ep04 도윤 반말 "너"(연기패스 핑퐁이 생성한 레지스터 이탈) + 세라 마지막말 ep04↔ep05 불일치. ★연기패스가 만든 오류를 검수가 잡음 = 복원형 안전망 작동. 세라 퇴사 대사의 미래 톤은 위반 아님 판정(가치관발 막연한 두려움, 카드 범위 내).
