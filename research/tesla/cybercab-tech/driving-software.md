# 테슬라 무감독 주행 소프트웨어는 왜 아직 한계인가

- 작성일: 2026-10-05
- 질문: 테슬라의 무감독 주행 소프트웨어가 대수와 운행 조건을 묶는 이유는 넷 중 무엇인가.
  - **Ha** 데이터·학습 연산 문제다. 학습을 늘리고 다음 판이 나오면 풀린다.
  - **Hb** 카메라만 쓰는 방식에 인식 한계(밤, 역광, 날씨, 작은 물체)가 있고 데이터만으로는 안 풀린다.
  - **Hc** 차에 실린 컴퓨터(AI4)가 필요한 모델에 비해 작아서 AI5를 기다린다.
  - **Hd** 주행 능력보다 운영·원격 지원 설계의 문제다.
- 앞선 조사: [병목 증거](../cybercab-outlook/binding-constraint.md), [종합 분석](../cybercab-outlook/analysis.md) 6절. 거기서 내린 결론(지금 묶는 것은 무감독 주행의 신뢰도와 테슬라의 속도 조절)은 되풀이하지 않고, 그 신뢰도가 **왜** 모자란지를 가른다.

## 읽는 법

확인 표시는 세 가지다.

- **원문 확인(직접 읽음)**: 문서 원문을 내려받아 글자 그대로 읽었다.
- **원문 확인†(요약 도구로 읽음)**: 해당 주소를 열었지만 요약 도구가 뽑아 준 내용으로 읽었다. 인용문의 글자 하나하나까지 보증하지 못한다.
- **검색 요약만**: 검색 결과에 나온 요약만 봤다. 주소를 열지 못했다.
- **기억(미확인)**: 2025년 이전 사실을 작업자의 기억으로 적었고 이번에 원문을 열지 못했다. 근거로 세지 않는다.

조사의 한계: 이번 세션의 검색 한도가 첫 여섯 번의 검색 뒤에 소진됐다. 나머지는 이미 알고 있던 주소와 그 페이지가 건 주소를 직접 열어 확인했다. 그래서 검색으로만 찾을 수 있는 자료(Missy Cummings·Brad Templeton의 분석, Bloomberg 기사, 학술 논문, Musk와 Elluswamy의 X 원문)는 대부분 빠졌다. "찾지 못했다"는 말은 "없다"가 아니라 "이번에 찾을 수단이 없었다"는 뜻이다.

사실, 남의 해석, 작업자의 판단을 절마다 나눠 적었다.

---

## 1. FSD는 2026년에 어떻게 작동하나 (테슬라의 설명)

### 1-1. 구조

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| FSD는 카메라 영상, 차량 운동 정보, 내비게이션 지도, 소리를 받아 조향·가속 명령을 내는 하나의 종단간(end-to-end) 신경망이다. Elluswamy는 이를 "the only scalable path to solving real-world robotics"라고 했다 | 2025-10 (ICCV 2025 발표) | https://www.humanoidsdaily.com/feed/tesla-ai-chief-details-unified-world-simulator-for-fsd-and-optimus , https://www.itiger.com/news/1146546403 | 원문 확인† (2차 매체. 발표 영상·X 원문은 못 봄) |
| 같은 발표: 신경망 기반 "world simulator"로 새 모델을 닫힌 고리로 평가하고, 과거 위험 장면을 바꿔 다시 돌리고, 드문 상황을 만들어 내고, 대규모 강화 학습에 쓴다. 차량 fleet가 하루에 사람 운전 500년치에 해당하는 데이터를 낸다는 주장 | 2025-10 | 위와 같음 | 원문 확인† |
| 같은 발표: "블랙박스" 비판에 대한 답으로 중간 토큰, 생성형 Gaussian splatting(3차원 이해의 시각화), 자연어 설명을 든다 | 2025-10 | https://www.itiger.com/news/1146546403 | 원문 확인† |
| 입력 규모(카메라 7대 × 초당 36장 × 5메가픽셀 × 30초, 입력 토큰 약 20억 개 → 출력 2개)라는 수치 | 2025-10 | (Elluswamy의 X 글) | 기억(미확인). 근거로 세지 않는다 |
| 테슬라 FSD는 "relies exclusively on vision-based cameras and the related FSD software"(NHTSA의 서술). 2021년 중반에 레이더를 빼고 카메라만 쓰는 방식으로 옮겼다 | 2026-03-18 | https://static.nhtsa.gov/odi/inv/2026/INOA-EA26002-10023.pdf | 원문 확인(직접 읽음) |
| 사이버캡은 카메라만 쓴다. 컴퓨터는 "a modified version of Hardware 4"이고 "not available to consumer cars" | 2026-09 | https://en.wikipedia.org/wiki/Tesla_Cybercab | 원문 확인† (위키백과) |

### 1-2. 판별 변화

| 판 | 무엇이 바뀌었나 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|---|
| v12 | 사람이 쓴 규칙 코드를 신경망으로 바꿨다("over 300,000 lines of explicit C++ code" 제거). 2024-04에 이름이 "Beta"에서 "Supervised"로 | 2023-08 시연, 2024-04 | https://en.wikipedia.org/wiki/Tesla_Autopilot | 원문 확인† |
| v13 | AI4 카메라의 원래 해상도 입력, AI4 전용 신경망. "Reduced photon-to-control latency", 주차 출발·후진 통합 | 2024-11 (v13.2) | 위와 같음 | 원문 확인† |
| v14 | 2025-10 AI4용 공개(v14.1.3). 강화 학습, 자가 주차 등. 2026-06 HW3용 v14 Lite. Tesla는 2026-04에 v14.3을 "last piece of the puzzle"이라고 불렀다 | 2025-10 ~ 2026-06 | 위 위키백과, https://electrek.co/2026/08/20/tesla-jpmorgan-fremont-fsd-v15-hw4-optimus-2027/ | 원문 확인† |
| v15 | 매개변수 약 10억 → 약 100억(10배). Musk: "a complete overhaul of the software architecture". 일곱 개의 개선 갈래를 병렬로 진행 | 2026-04-22 ~ | https://www.notateslaapp.com/news/4035/tesla-confirms-fsd-v15-will-run-on-hardware-4-shares-release-date , https://www.notateslaapp.com/news/4679/tesla-ai-chief-talks-about-whats-coming-in-fsd-v15 | 원문 확인† |
| v15 | 10배 모델은 **원래 v14에 넣으려던 것이 v15로 밀렸다** | 2026-04-23 보도 | 위 notateslaapp 4035 | 원문 확인† |
| v15 | 맥락 길이 약 10초 → 30초 | 2026 | (검색 결과 요약) | 검색 요약만 |
| v15 | Elluswamy(2분기 실적 발표): "The currently operating robotaxi fleet is already running early versions of the v15 FSD software ... we had planned roughly about seven major improvement tracks ... The early v15 builds that are running on robotaxi have already -- 40% of those tracks merged together" | 2026-07-22 | https://www.fool.com/earnings/call-transcripts/2026/08/05/tesla-tsla-q2-2026-earnings-call-transcript/ , https://www.investing.com/news/transcripts/earnings-call-transcript-tesla-q2-2026-revenue-beats-eps-misses-as-stock-falls-93CH-4807216 | 원문 확인† (두 녹취록이 같은 문장) |
| v15 | Elluswamy(X): "Even earlier prediction of hazards, even faster reaction time and overall significantly better safety and collision avoidance coming as part of the next big upgrade (v15)." | 2026-09-11 보도 | 위 notateslaapp 4679 | 원문 확인† |
| v15 | 고객용 배포 목표: 2026년 말 또는 2027년 초. AI4 전용이고 HW3용 "v15 Lite"는 없다 | 2026-04-22, 2026-09-11 | 위 4035, 4679 | 원문 확인† |

로보택시용 판과 고객용 판의 차이: 로보택시 fleet는 v15의 초기판(일곱 갈래 중 40%)을 쓰고 고객 차는 v14.3.x를 쓴다(위 출처). 그 밖의 차이(지도, 원격 지원 연결, 승하차 로직)는 테슬라가 설명한 자료를 찾지 못했다.

### 1-3. 학습 연산

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| "more than doubled onsite compute in Texas (in terms of MW of compute) during the first half of 2026". Cortex 1과 Cortex 2가 차량·로봇 자율 개발을 맡는다 | 2026-07-22 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026049213/exhibit991.htm | 원문 확인† (1차 자료) |
| Cortex 2가 가동돼 학습 작업을 돌리고 있다 | 2026-04-22 | https://www.notateslaapp.com/news/4031/everything-tesla-announced-during-its-q1-2026-earnings-call-summaryrecap | 원문 확인† |
| Dojo: Bloomberg가 2025-08에 프로젝트 해체를 보도. 2026-01에 AI5 칩 기반으로 재개("Dojo 3") | 2025-08, 2026-01 | https://en.wikipedia.org/wiki/Tesla_Dojo | 원문 확인† (위키백과) |
| 2024년에 학습 연산을 400% 늘렸다 | 2025-01 | https://en.wikipedia.org/wiki/Tesla_Autopilot | 원문 확인† |
| FSD 누적 주행 100억 마일, 그중 시내 37억 마일 | 2026-05 | 위와 같음 | 원문 확인† |
| Musk는 2026-01에 무감독에 필요한 데이터를 100억 마일이라고 말했다(Electrek의 서술) | 2026-01 | https://electrek.co/2026/04/22/tesla-elon-musk-unsupervised-fsd-consumer-cars-q4-delay-again/ | 원문 확인† |
| Cortex의 H100 환산 대수, 전력(MW) 절대값 | | | 찾지 못했다. 2분기 자료는 "두 배 이상"이라는 비율만 준다 |

작업자의 판단: 100억 마일은 2026-05에 넘었다. Musk가 직접 든 데이터 기준이 채워진 뒤에도 운행 조건은 풀리지 않았다. "데이터 양이 모자라서"라는 가장 단순한 형태의 Ha는 이것으로 약해진다. 남는 Ha는 "더 큰 모델(v15)을 학습해 내놓아야 한다"는 형태다.

---

## 2. 판별 신뢰도 증거

### 2-1. 고객 차의 개입 빈도 (공동체 집계)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| FSD Community Tracker의 "치명적 개입 1회당 마일"(전체 / 시내): v12.3.x 177 / 121, v12.5.x 273 / 129, v13.2.x 444 / 217, v14.1.x 9,263 / 4,109, v14.2.x 1,642 / 696, v14.3.x 1,750 / 853 | 2026-06-01 (07-01 수정) | https://blog.dominik-roth.eu/posts/fsd-14.html | 원문 확인† (개인 분석가의 글. 표의 신뢰구간 열은 요약 도구가 깨뜨려 옮기지 않았다) |
| 같은 글: v14.1의 급등은 초기 이용자 소수의 표본 때문이고 v14.2의 하락은 평균 회귀다. v14.x 기록의 76%는 치명적 개입 0건. 시험자 387명 중 v13과 v14를 모두 가진 사람은 17명 | 같음 | 같음 | 원문 확인† |
| 같은 글: Waymo가 안전 운전자를 뺄 때의 수준을 치명적 개입 1회당 약 48,000마일로 놓으면 현재 fleet(1,950마일)과 **24.6배 차이**. 추세를 이으면 교차 시점은 2031년 무렵(90% 구간은 2020년대 후반~2030년대 중반). Texas·Nevada·Florida는 2027~2029년 | 같음 | 같음 | 원문 확인† |
| tracker 원 사이트 | | https://teslafsdtracker.com/ | 열었지만 숫자가 읽히지 않았다 |

남의 해석: Dominik Roth는 "FSD가 무너졌다"는 2026-03 무렵의 해석을 통계적 착시라고 본다. 반대로 한 증권 분석가는 지표가 "sharply deteriorating"이라고 했다(검색 요약만, https://www.sahmcapital.com/news/content/teslas-fsd-safety-metrics-sharply-deteriorating-says-analyst-2026-03-09 는 404).

작업자의 판단: 이 집계는 자원자 표본이고 "치명적"의 판정이 운전자 주관이다. 쓸 수 있는 것은 방향뿐이다. v13에서 v14로 약 4배 나아졌고, 무감독에 필요한 수준과는 아직 한 자릿수 배가 아니라 수십 배 차이라는 것. 로보택시는 고객 차와 다른 판(v15 초기판)을 지오펜스 안에서 쓰므로 이 숫자를 로보택시에 그대로 옮길 수 없다.

### 2-2. 로보택시 사고 보고 (NHTSA 상시 일반 명령)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 2025-07~11: 약 50만 마일에 9건. 약 55,000마일당 1건. 모두 안전요원이 탄 상태 | 2026-01-29 | https://electrek.co/2026/02/05/teslas-own-robotaxi-data-confirms-crash-rate-3x-worse-than-humans-even-with-monitor/ | 원문 확인† |
| 2026-01 중순까지 약 80만 마일에 14건. 57,000마일당 1건. 새 5건: 시속 17마일 고정물, 4마일 대형 트럭, 0마일 버스(정지 중), 2마일 후진 중 고정물, 1마일 후진 중 기둥·나무 | 2026-02-17 | https://electrek.co/2026/02/17/tesla-robotaxi-adds-5-more-crashes-austin-month-4x-worse-than-humans/ | 원문 확인† |
| 2025-07~2026-03 17건: 재산 피해만 13건, 입원 1건. 가장 흔한 유형은 서 있거나 느린 로보택시를 다른 차가 들이받은 것. 2025-09 개를 침(개는 달아남), 2025-09 비보호 좌회전 중 주차장 쇠사슬 | 2026-05-15, 05-26 | https://techcrunch.com/2026/05/15/tesla-reveals-two-robotaxi-crashes-involving-teleoperators/ , https://www.techtimes.com/articles/317224/20260526/tesla-robotaxi-crashes-blamed-human-teleoperators-backup-system-failed-twice-nhtsa-data.htm | 원문 확인† |
| 원격 조작자가 몰다 낸 사고: 2025-07 Austin(연석을 넘어 철제 울타리, 요원 입원), 2026-01 Austin(시속 약 9마일, 공사 차단물). 두 건 모두 자동 주행이 멈춘 뒤 원격으로 넘어갔다 | 같음 | 같음 | 원문 확인† |
| 2026-06 중순 누계 18건(최근 건은 정지 중 추돌당함). 같은 자료의 Waymo 약 697건 | 2026-06-16 | https://electrek.co/2026/06/16/tesla-robotaxi-clean-crash-record-barely-running/ | 원문 확인† |
| Elluswamy: "We have driven more than 380,000 miles of unsupervised robotaxi now across six cities in two different states. We have had zero notable incidents." | 2026-07-22 | 위 Fool 녹취록 | 원문 확인† |
| 무감독 누적 100만 마일. 6주 동안 62만 마일 추가 | 2026-09-03 | https://electrek.co/2026/09/03/tesla-announces-1-million-unsupervised-miles-driven-by-robotaxi/ | 원문 확인† |
| Waymo: 무인 2억 7,130만 마일(2026-06까지). 백만 마일당 중상 이상 0.01(기준 0.21, −95%), 부상 보고 0.67(기준 3.77, −82%), 에어백 전개 0.29(기준 1.62, −82%) | 2026-06 | https://waymo.com/safety/impact/ | 원문 확인† (회사 자료. 동료 심사 논문 Kusano 등에 기반한다고 적혀 있다) |
| Swiss Re 연구: 2,530만 마일에서 재산 피해 청구 −88%, 신체 상해 청구 −92%(Waymo 9건·2건 대 예상 78건·26건). ADAS를 단 2018~2021년식 차와 견줘도 −86%, −90% | 2024-12-19 | https://waymo.com/blog/2024/12/new-swiss-re-study-waymo | 원문 확인† |
| IIHS 연구: Waymo의 전체 사고율이 사람보다 68% 낮고 부상·사망 사고율은 81% 낮다. 경찰 신고 대상 사고의 8%가 Waymo 과실 | 2026-07 | https://en.wikipedia.org/wiki/Waymo | 원문 확인† (위키백과) |

비교할 때의 주의:

- 테슬라의 분모(마일)는 실적 자료의 도표를 읽은 추정이다. 테슬라는 월별 마일을 내지 않는다.
- 2026-01까지의 사고는 모두 안전요원이 탄 상태였다. 요원이 막은 사고는 집계에 없다.
- 테슬라는 2026-05까지 사고 서술을 전부 가렸다.
- 사람 기준이 출처마다 다르다(경찰 신고 사고 50만 마일당 1건, 미신고 포함 20만 마일당 1건, 테슬라 자체 보고서의 경미한 충돌 22만 9천 마일당 1건).
- 상시 일반 명령은 사고를 마일로 나누지 않는다. Waymo의 697건은 2억 마일대의 분모에서 나온 것이다.
- Philip Koopman의 일반적 비판: 안전 연구는 "changing software, remote-operator roles, empty-vehicle miles that reduce 'injury crashes,' selective reporting"을 자주 빼먹고, 드문 사망 사고는 훨씬 많은 마일이 있어야 잰다(https://philkoopman.substack.com/p/podcast-limitations-of-robotaxi-safety , 원문 확인†).

작업자의 계산(판단): 사건이 0건일 때 95% 신뢰로 "기준보다 낮다"고 말하려면 대략 3 ÷ 기준 빈도만큼의 마일이 필요하다. Waymo가 쓰는 사람 기준으로 부상 사고는 약 80만 마일, 에어백 전개는 약 185만 마일, **중상 이상은 약 1,400만 마일**이다. 테슬라의 무감독 누적은 100만 마일이다. 최근 속도(6주에 62만 마일, 주 약 10만 마일)가 그대로면 1,400만 마일까지 약 2년 반이 걸린다. 기준값은 Waymo 운행 도시의 것이어서 Austin에 그대로 맞지 않는다. 뜻하는 바는 하나다. **신뢰도를 입증하는 속도는 무감독 마일에 묶이고, 무감독 마일은 대수와 운행 시간에 묶인다.** 테슬라가 "생산 목표를 무감독 마일 증가에 맞췄다"고 한 것과 같은 구조다.

### 2-3. 고객 차 FSD에 대한 NHTSA 조사

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| EA26002(PE24031에서 격상). 주제 "FSD Collisions in Reduced Roadway Visibility Conditions". 대상 3,203,754대. 충돌 9건, 사망 1건 | 2026-03-18 | https://static.nhtsa.gov/odi/inv/2026/INOA-EA26002-10023.pdf | 원문 확인(직접 읽음) |
| 같은 문서: "the system did not detect common roadway conditions that impaired camera visibility and/or provide alerts when camera performance had deteriorated until immediately before the crash occurred ... In each of these crashes, FSD also lost track of or never detected a lead vehicle in its path." 조건은 "glare and airborne obscurants" | 같음 | 같음 | 원문 확인(직접 읽음) |
| 같은 문서: 테슬라의 사후 분석으로는 열화 감지 갱신판이 9건 중 3건에 영향을 줄 수 있었다. 테슬라의 내부 자료·표지 한계로 "under-reporting"이 있었을 수 있다 | 같음 | 같음 | 원문 확인(직접 읽음) |
| PE25012. 주제 "Traffic safety violations while Full Self Driving ('FSD') is engaged". 대상 2,882,566대. 사건 58건, 충돌 14건, 부상 23명. 두 유형: 빨간 신호에 교차로 진입(충돌한 상시 보고 6건), 반대 차로로 차로 변경. Maryland Joppa의 같은 교차로에서 반복 | 2025-10-07 | https://static.nhtsa.gov/odi/inv/2025/INOA-PE25012-19171.pdf | 원문 확인(직접 읽음) |

작업자의 판단: EA26002는 Hb를 직접 뒷받침하는 유일한 1차 자료다. 역광과 공기 중 차폐물에서 카메라가 앞차를 놓쳤고 시스템이 자기 열화를 알아차리지 못했다. 다만 대상은 2016년식부터의 고객 차(HW3 포함)이고 사고는 2023~2024년 판에서 났다. v15와 AI4 카메라에 같은 약점이 남아 있는지는 이 문서로 알 수 없다. PE25012는 인식이 아니라 신호·차로 의미 해석과 계획의 문제다.

### 2-4. 로보택시·사이버캡에서 보고된 실패의 분류

| 실패 | 날짜 | 조건 | 분류 | 출처 URL | 확인 |
|---|---|---|---|---|---|
| 좌회전 망설임 끝에 반대 차로 잠깐 진입 | 2025-06 | 낮 | 계획 | https://electrek.co/2025/06/25/whoopsie-uh-oh-oh-my-heres-all-the-gaffes-and-goofs-by-tesla-robotaxi-so-far/ | 원문 확인† |
| 지는 해를 향해 달리다 이유 없는 급제동 | 2025-06 | 해 질 녘 | 인식(역광) | 같음 | 원문 확인† |
| 교차로·좌회전 차로에 서서 하차, 주차장 연석 접촉, 주차된 차에 접근해 요원이 개입 | 2025-06 | 낮 | 계획(승하차·저속 기동) | 같음 | 원문 확인† |
| 경찰차 옆에서 과한 제동 | 2025-06 | 낮 | 계획 | 같음 | 원문 확인† |
| 개를 침 | 2025-09 | 불명 | 인식 또는 반응(불명) | 위 TechCrunch 05-15 | 원문 확인† |
| 후진 중 고정물·기둥 접촉(시속 1~2마일) | 2025-12 ~ 2026-01 | 불명 | 인식(근거리 사각) 또는 계획 | 위 Electrek 02-17 | 원문 확인† |
| 자동 주행이 멈춤 → 원격 조작자가 몰다 울타리·차단물 충돌 3건 | 2025-07, 2026-01, 2026-05 | 저속 | 계획(멈춤) + 원격 운영 | 위 TechTimes, 앞선 조사 | 원문 확인† |
| 플라스틱 말뚝 앞에서 여러 번 서다가 밀고 지나감. 말뚝은 2024-02부터 있었다 | 2026-08 | 낮, 시야 좋음 | 계획(인식은 됐다) | https://electrek.co/2026/08/18/tesla-robotaxi-rams-through-bollards-austin/ | 원문 확인† |
| Dallas: 목적지 3마일 앞에서 하차, 하차 지점을 계속 지나침, 길 한가운데서 멈춤. 지원 담당이 "end of shift"라며 돕지 못함. 한 번은 원격 수동 개입 | 2026-08-17 ~ 21 | 불명 | 경로·지오펜스 + 원격 운영 | https://electrek.co/2026/08/24/tesla-robotaxi-failing-fans-texas/ | 원문 확인† |
| 2.3마일에 66분 걸리는 경로 | 2026-08-22 | | 경로 | 같음 | 원문 확인† |
| 사이버캡: 공사로 한 차로가 막힌 호텔 주차장에서 네 번 오가다 출발 지점에 내려 줌 | 2026-09 | | 계획(열린 차로를 찾지 못함) | https://futurism.com/advanced-transport/cybercab-trapped-hotel-lot | 원문 확인† |
| 사이버캡: 고속도로와 평면 철도 건널목을 피해 10분 거리를 70분에 감 | 2026-09 | | 운행 조건 제한(경로) | https://electrek.co/2026/09/14/tesla-cybercab-70-minute-austin-detour/ | 원문 확인† |
| 사이버캡 첫 달: 긴 대기, 틀린 승하차 지점, 문·트렁크 오작동. 큰 충돌 보고 없음 | 2026-10-04 | | 경로·운영 | https://teslanorth.com/2026/10/04/elon-musk-touts-careful-cybercab-rollout-austin-fleet-169/ | 원문 확인† |

세어 보면: 표의 13줄 가운데 인식이 원인으로 분명한 것은 1줄(역광 급제동), 인식일 수 있는 것이 2줄(개, 후진 접촉)이다. 나머지는 계획·경로·원격 운영이다. **이 표는 공개된 실패의 표이지 테슬라가 막아 둔 실패의 표가 아니다.** 밤 11시 이후, 비, 고속도로, 철도 건널목은 운행하지 않으므로 거기서 날 실패는 관찰되지 않는다. 그래서 이 분류만으로 Hb를 기각할 수 없다.

찾지 못한 것: 긴급 차량·공사 구간·철도 건널목에서의 로보택시 사고 보고. 사이버캡의 상시 일반 명령 보고(보고 지연이 있어 9월분은 아직 나오지 않았을 수 있다). 원격 개입 횟수.

---

## 3. 운행 조건이 풀린 속도

### 3-1. 테슬라

| 조건 | 상태와 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 차 안의 사람 | 2025-06-22 조수석 안전요원 → 2026-01-22 Austin 일부 차량에서 제거(처음에는 뒤따르는 차에 요원) → 2026-04-18 Dallas·Houston 출시일부터 무감독 → 2026-07 Florida 세 도시 | 앞선 조사, https://electrek.co/2026/01/22/tesla-didnt-remove-the-robotaxi-safety-monitor-it-just-moved-them-to-a-trailing-car/ | 원문 확인† |
| 차 안의 사람(2026-04) | Austin 약 80대 중 무감독은 4~12대, 나머지 대부분은 "safety monitors in the driver's seat" | https://electrek.co/2026/04/18/tesla-robotaxi-launches-dallas-houston-small-geofences/ | 원문 확인† |
| 차 안의 사람(사이버캡) | Tesla North는 "Tesla began paid Austin rides in September with safety monitors and a small fleet", "has not promised a schedule for removing monitors"라고 썼다. 사이버캡에는 운전대가 없고 테슬라는 무감독이라고 부른다. **두 서술이 어긋난다. 풀지 못했다** | https://teslanorth.com/2026/10/04/elon-musk-touts-careful-cybercab-rollout-austin-fleet-169/ | 원문 확인† |
| 운행 시간 | 2025-06 출시: 자정~오전 6시 미운행(오전 6시~자정, 요원 탑승) → 2026-01 Electrek "not operating at night" → 2026-08~09 여섯 도시 오전 6시~오후 10시 → 2026-10-03 Austin 오후 11시까지 | 위 Electrek 2025-06-25, https://www.teslarati.com/tesla-robotaxi-24-7-service/ , https://www.notateslaapp.com/news/4768/tesla-extends-robotaxi-hours-in-austin-adds-111-cybercabs | 원문 확인† |
| 날씨 | 2025-06 "No operation in bad weather" → 2026-02 "Shuts down entirely during rain" → 2026-04 "still shuts down during rain". 그 뒤의 상태는 찾지 못했다 | 위 Electrek 2025-06-25, https://electrek.co/2026/02/16/tesla-robotaxi-status-check-8-months-in/ , 위 Electrek 04-18 | 원문 확인† |
| 고속도로 | 2026-09: 사이버캡과 Model Y 로보택시 모두 Austin에서 고속도로(MoPac, US-183)를 타지 않는다. 일반 도로 시속 35마일 | 위 Electrek 09-14 | 원문 확인† |
| 고속도로(과거) | 2025-09 무렵 운전석에 안전요원을 앉히고 고속도로 운행을 시작했다 | | 기억(미확인) |
| 철도 건널목 | 평면 건널목을 피하고 다리로만 건넌다 | 위 Electrek 09-14 | 원문 확인† |
| 지오펜스 | Austin 약 20~30제곱마일(2025-06) → 약 245(2026-04) → 264(2026-08). Dallas 31 → 81(2026-08). Houston 25, Miami 31, Orlando 26, Tampa 24 | https://www.notateslaapp.com/news/4632/tesla-expands-robotaxi-geofences-in-dallas-and-austin , 위 Electrek 04-18 | 원문 확인† |
| 무감독 구역(2026-02) | 무감독 운행은 South Congress와 Lamar를 따라가는 좁은 구간에 한정 | 위 Electrek 02-16 | 원문 확인† |
| 원격 운전 | 시속 10마일 이하에서 원격 조작자가 직접 몬다 | 위 TechCrunch 05-15 | 원문 확인† |
| 대수 | 무감독 한 자릿수(2026-01) → 25(04월 말) → 14(06월) → Texas 등록 476대(Model Y 409, 사이버캡 67, 09-22) → 사이버캡 169(10-04) | https://electrek.co/2026/04/30/tesla-robotaxi-unsupervised-finally-signs-ramping-up/ , 위 Electrek 06-16, https://electrek.co/2026/09/22/tesla-robotaxi-active-fleet-austin-crashes-8-vehicles/ | 원문 확인† |
| 실제 운행 대수 | 목격 집계로 최근 7일 8대(09-22). 9월 초 출시 직후에는 100대 이상 | 위 Electrek 09-22 | 원문 확인† (목격 집계. 방법의 한계가 크다) |
| 공항 | 찾지 못했다 | | |

읽는 법(판단):

1. 풀린 것은 "차 안의 사람"(7개월)과 "지오펜스"(14개월에 약 10배)다. 풀리지 않은 것은 "심야", "비", "고속도로", "철도 건널목"이다.
2. 운행 시간은 **요원을 뺀 뒤에 오히려 줄었다**(자정 → 오후 10시)가 한 시간 늘었다. 요원이 있으면 자정까지 달리던 차가 요원이 없으면 10시에 멈춘다. 운영 인력이나 수요가 원인이라면 요원이 탈 때도 같아야 한다. 주행 신뢰도에 대한 테슬라 자신의 평가가 원인이라는 쪽이다.
3. 10월의 Austin은 해가 오후 7시쯤 진다. 오후 11시까지 운행한다는 것은 **어두운 뒤 약 네 시간을 이미 무감독으로 달린다**는 뜻이다. "카메라는 밤에 못 본다"는 강한 형태의 Hb는 이것과 맞지 않는다. 남는 Hb는 "가로등과 차량이 적은 심야의 저대비 물체"라는 좁은 형태다. (일몰 시각은 작업자의 일반 지식이다.)

### 3-2. Waymo (한 단계에 걸린 시간의 참고)

| 단계 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 일반인 대상 완전 무인 서비스(Phoenix) | 2020-10-08 | https://waymo.com/blog/2020/10/waymo-is-opening-its-fully-driverless | 앞선 조사(원문 확인) |
| 공항: Phoenix Sky Harbor 2022-11-01, San Jose 2025-12-01, San Francisco 2026-01-29(대기 명단) | 각 날짜 | https://en.wikipedia.org/wiki/Waymo | 원문 확인† |
| 고속도로: 2025-11 일부 승객에게 개방. **무인 서비스 개시 뒤 약 5년** | 2025-11 | 같음 | 원문 확인† |
| 고속도로 중단: 닫힌 고속도로 공사 구간에 들어가 속도를 낸 사건이 2026-04-11부터 13건. 05-19 고속도로 운행 중단, 06-17 리콜 공표. 위키백과는 05~07월 중단이라고 적는다 | 2026-04 ~ 07 | https://philkoopman.substack.com/p/a-third-strike-for-waymo-on-failed , 위 위키백과 | 원문 확인† |
| 2026년의 다른 리콜: 침수 구역에 빠른 속도로 진입, 정차한 통학 버스 추월(2025-12-08 소프트웨어 리콜) | 2025-12 ~ 2026-06 | 같음 | 원문 확인† |
| 눈 오는 도시: Denver 정식 서비스 2026-09-01. 겨울 운행 실적은 아직 없다 | 2026-09-01 | https://techcrunch.com/2026/09/01/waymo-accelerates-robotaxi-expansion-with-launches-in-denver-san-diego-and-tampa/ , 위 위키백과 | 원문 확인† |
| 규모: 14개 도시, 4,000대 이상(Ojai 약 300대), 주 50만 건 이상 | 2026-09-01 | 위 TechCrunch | 원문 확인† |
| Austin에서 24시간, 90제곱마일, 무인 100대 이상 | 2026-02 | 위 Electrek 02-16 | 원문 확인† (Electrek의 서술) |
| Waymo가 각 도시에서 24시간 운행을 시작한 날짜 | | | 찾지 못했다 |

남의 해석: Koopman은 Waymo가 세 영역(침수, 통학 버스, 공사 구간)에서 "operational mitigations"로 때우다 거듭 실패했다고 본다.

작업자의 판단: Waymo의 2026년 리콜 세 건은 모두 라이다와 레이더를 단 차에서 났고 원인은 감지가 아니라 **상황의 의미 해석**(닫힌 구간, 통학 버스의 정지 신호, 물의 깊이)이다. 센서를 더 달아도 남는 꼬리가 있다는 뜻이다. 또 무인 서비스에서 고속도로 승객 개방까지 5년이 걸렸고 6개월 만에 두 달을 멈췄다. 고속도로는 "다음 판 하나"로 열리는 종류의 조건이 아니었다.

---

## 4. Waymo의 방식과 카메라 전용 방식의 현황

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 6세대 Waymo Driver: "With 13 cameras, 4 lidar, 6 radar, and an array of external audio receivers (EARs) ... optimized for greater performance at a significantly reduced cost". 최대 500미터, 낮과 밤 | 2024-08-19 | https://waymo.com/blog/2024/08/meet-the-6th-generation-waymo-driver | 원문 확인† |
| Waymo Foundation Model: 빠른 계통(카메라·라이다·레이더를 합치는 Sensor Fusion Encoder)과 느린 계통(Driving VLM. "leverages Gemini's extensive world knowledge to better understand rare, novel, and complex semantic scenarios")이 World Decoder로 들어간다. Simulator와 Critic이 딸린다. 교사 모델을 학생 모델로 줄여 차에 싣는다 | 2025-12-09 | https://waymo.com/blog/2025/12/demonstrably-safe-ai-for-autonomous-driving | 원문 확인† |
| EMMA: Gemini 같은 다중 모달 언어 모델 위에서 카메라 원시 자료를 주행 궤적·물체·도로 그래프로 바로 바꾸는 연구 모델 | 2024-10-30 (v3 2025-09-23) | https://arxiv.org/abs/2410.23262 | 원문 확인† (초록) |
| 원격 지원: "RA does not continuously monitor a vehicle". 차가 요청하면 조언하고 차가 받아들이거나 거부한다. 원격 운전은 쓰지 않는다. 동시 근무 "approximately 70" 명, 차량 3,000대(약 1:43), 주 400만 마일 이상 | 2026-02-17 | https://waymo.com/blog/shorts/advice-not-control-the-role-of-remote-assistance/ | 원문 확인† |
| 차량 비용: Morgan Stanley 추정 $120,000 이상(2024-10), $100,000 이상(2025-06) | | 위 위키백과 | 원문 확인† |
| Rivian은 라이다가 대당 "a few hundred dollars"라고 했다 | 2026-09 | https://electrek.co/2026/10/03/tesla-robotaxi-pets-night-musk-lidar/ | 원문 확인† (Electrek의 서술) |
| Waymo의 Srikanth Thirumalai: "Simply improving a driver-assist system (L2) for full autonomy is a false summit. True L4 maturity can only be safely achieved by a purpose-built system, validated on closed courses and hardened by the uncompromising experience of driving without a human in the car." 카메라만으로는 안 된다는 주장과 "You can't build trust with a black box"도 함께 | 2026-08 | https://electrek.co/2026/08/27/waymo-tesla-self-driving-false-summit/ | 원문 확인† (Electrek의 인용. Waymo 블로그 원문은 못 찾음) |
| Waymo가 2026-08에 카메라 화면이 "close to useless"인 캄캄한 길을 달리는 시연을 냈다 | 2026-08 | 위 Electrek 10-03 | 원문 확인† (Electrek의 서술) |
| XPeng 로보택시: 라이다 없이 카메라와 4D 밀리미터파 레이더. 자체 Turing 칩. 2026-05 양산 시작, 2026년 하반기 시범 운행, "fully driverless operation in early 2027" 계획 | 2026-05 | https://en.wikipedia.org/wiki/XPeng | 원문 확인† (위키백과, Reuters 인용) |
| Wayve, comma, Mobileye의 카메라 전용 계통이 무인 상업 운행을 한다는 자료 | | | 찾지 못했다(검색 한도). "없다"고 쓰지 않는다 |

작업자의 판단: 2026-10 기준으로 카메라만으로 사람 없이 유료 승객을 태우는 곳은 확인한 범위에서 테슬라뿐이다. XPeng은 레이더를 쓰고 아직 무인이 아니다. 그래서 "카메라만으로 된다"는 독립된 선례도, "안 된다"는 독립된 반증도 없다. 테슬라 자신이 유일한 실험이다. Waymo도 느린 계통에서는 카메라 중심의 언어 모델을 쓴다. 두 회사의 차이는 모델 구조보다 **감지 계층의 중복**(라이다·레이더)과 **원격 지원의 방식**(조언 대 직접 운전)에 있다.

---

## 5. 차에 실린 컴퓨터

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| AI4(HW4): 2023-01부터. 삼성 7nm. Musk "three to eight times more powerful than HW3". 메모리는 출처에 따라 16GB(위키백과, notateslaapp) 또는 합계 32GB(Electrek) | 2023 ~ | https://en.wikipedia.org/wiki/Tesla_Autopilot_hardware , https://electrek.co/2026/04/23/tesla-hw4-plus-upgrade-will-hw4-follow-hw3/ | 원문 확인† (수치가 서로 다르다) |
| AI4+(AI4.1): 칩당 메모리 16GB → 32GB(합계 64GB), 연산·메모리 대역폭 약 10% 증가. 2027년 생산. 2026-04-22 발표 | 2026-04-22 | 위 Electrek 04-23, 위 위키백과 | 원문 확인† |
| Not a Tesla App: AI4+는 "preparation for larger robotaxi models and longer context windows". 사이버캡에는 AI5가 아니라 메모리를 늘린 AI4 계열이 들어간 것으로 보인다 | 2026-08-20 | https://notateslaapp.com/news/4594/tesla-is-holding-back-model-y-robotaxis-reveals-new-fsd-v15-details | 원문 확인† (매체의 추정이 섞여 있다) |
| 1분기 실적 발표: v15는 지금의 AI4에서 돈다. Musk는 소프트웨어를 "designed to squeeze every ounce of performance out of the existing Hardware 4 units"라고 했다. 방법은 큰 모델을 줄이는 "distillation" | 2026-04-22 | 위 notateslaapp 4035 | 원문 확인† |
| Musk: "AI4 is enough to achieve much better than human safety for FSD" | 2026 | 위 위키백과 Autopilot hardware | 원문 확인† (위키백과) |
| AI5는 당분간 차에 넣지 않는다. Optimus와 데이터센터에 먼저 쓴다. 차의 교체는 "Several years away; only needed when AI4 becomes outdated" | 2026-04-22 | 위 notateslaapp 4031, 위 Electrek 04-23, 위 위키백과 | 원문 확인† (세 출처가 일치) |
| Musk(2분기): "We have an upgraded AI4 chip that's a moderate improvement over AI4, probably reaches production around the middle of next year. We'll say AI5, which hopefully is in volume production around the middle of next year." | 2026-07-22 | 위 Investing.com 녹취록 | 원문 확인† |
| AI5 일정의 이력: 2024-06 발표 때 2025년 하반기 → 2026년 말 → Musk(2025-11) "AI5 will not be available in sufficient volume to switch over Tesla production lines until mid 2027" | 2024-06 ~ 2025-11 | https://electrek.co/2025/11/20/tesla-delays-next-gen-ai5-chip-mid-2027-cybercab/ | 원문 확인† |
| AI5 성능 주장: AI4의 "10x"(Electrek), "5x the compute power"(notateslaapp 4035), 단일 칩이 Nvidia H100과 비슷(notateslaapp 3519) | 2025-11 ~ 2026-04 | 위 출처, https://www.notateslaapp.com/news/3519/teslas-ai5-to-enter-production-in-2h-2026-rivals-nvidias-30k-chip-in-performance | 원문 확인† (출처마다 배수가 다르다) |
| Musk의 "40x" 발언 | 2025 | | 기억(미확인). 이번에 연 자료에는 40배가 나오지 않았다 |
| HW3: Musk "simply does not have the capability". 메모리 대역폭이 HW4의 8분의 1. 약 400만 대를 "micro-factories"에서 교체하거나 AI4 차로 할인 교환 | 2026-04-22 | 위 Electrek 04-23, 위 Electrek 04-22, 위 notateslaapp 4031 | 원문 확인† |
| Musk: "At some point the AI4 hardware is going to get like so old that it's like, okay, the only reason to keep the factory open is for AI4" | 2026-04 | 위 Electrek 04-23 | 원문 확인† |
| 남의 해석(Electrek): AI4가 HW3의 길을 갈 수 있다. HW3도 충분하다고 했다가 뒤집혔다 | 2026-04-23 | 위 Electrek 04-23 | 원문 확인† |

작업자의 판단:

- "AI5를 기다린다"는 형태의 Hc는 **테슬라의 행동과 맞지 않는다.** 테슬라는 AI5를 차에 넣을 계획을 미뤘고, 로보택시는 AI4 계열에서 v15 초기판으로 이미 달린다. AI5가 병목이라고 믿는 회사라면 AI5를 로봇과 데이터센터에 먼저 돌리지 않는다. 다만 이것은 테슬라의 믿음에 대한 증거이지 그 믿음이 옳다는 증거는 아니다. HW3 때 같은 믿음이 틀렸다.
- "메모리가 모자란다"는 약한 형태의 Hc는 **지지된다.** 10배 모델이 v14에서 v15로 한 판 밀렸고, 메모리를 두 배로 늘린 AI4+를 따로 만들었고, 사이버캡에는 고객 차에 없는 개조 컴퓨터가 들어갔다. 큰 모델을 줄여서 싣는다고 회사가 직접 말했다.
- 이미 만든 차에 대한 뜻: 로보택시 쪽은 문제가 작다. 사이버캡은 새로 만드는 차이고 메모리가 큰 컴퓨터를 쓴다. 문제는 고객 차다. 표준 AI4를 단 수백만 대가 줄인 v15로 무감독 수준에 닿는지가 열려 있다. 앞선 분석 7-2절의 "고객 소유 차로 차이를 메운다"는 길이 여기에 달려 있다.

---

## 6. 테슬라가 말한 일정과 지킨 정도 (2024~2026)

| 말한 날 | 말한 것 | 목표 | 실제 | 출처 URL | 확인 |
|---|---|---|---|---|---|
| 2025-01 | "We're going to be launching unsupervised Full Self-Driving as a paid service in Austin in June." | 2025-06 | 2025-06-22 시작. 조수석에 안전요원 | https://en.wikipedia.org/wiki/List_of_predictions_for_autonomous_Tesla_vehicles_by_Elon_Musk | 원문 확인† |
| 2025-07 | "autonomous ride hailing in probably half the population of the U.S. by the end of the year" | 2025-12 | 두 지역 | 같음 | 원문 확인† |
| 2025-07 | "[FSD] will be available for unsupervised personal use by the end of this year in certain geographies." | 2025-12 | 미달 | 같음 | 원문 확인† |
| 2025-09 | "[Robotaxi] Should be no safety driver by end of year." | 2025-12 | 2026-01-22 일부 차량(뒤따르는 차에 요원) | 같음 | 원문 확인† |
| 2025-10 | Austin에 "500 or more" | 2025-12 | 2026-02에 약 42대 | 위 Electrek 02-16 | 원문 확인† |
| 2025-12-09 | "There will be Tesla Robotaxis operating in Austin with no one in them, in about three weeks." | 2025-12 말 | 2026-01-22(약 6주 뒤) | https://electrek.co/2025/12/09/tesla-ceo-elon-musk-claims-driverless-robotaxis-coming-to-austin-in-3-weeks/ | 원문 확인† |
| 2026-01 | 일곱 도시를 2026년 상반기에 | 2026-06 | Dallas·Houston 04-18. Florida 세 도시는 07월. Phoenix·Las Vegas는 미출시 | https://electrek.co/2026/04/22/tesla-seems-to-say-robotaxi-launch-will-be-pushed-back-in-5-US-cities/ | 원문 확인† |
| 2026-01 | "Fully autonomous vehicles in probably somewhere between a quarter and half of the United States by the end of the year." | 2026-12 | 진행 중 | 위 위키백과 목록 | 원문 확인† |
| 2026-04-22 | 고객 차 무감독: "I'm just guessing here, but probably in the fourth quarter." | 2026 4분기 | 진행 중 | 위 Electrek 04-22 | 원문 확인† |
| 2026-04-22 | v15는 2026년 말 또는 2027년 초 | | 로보택시에 초기판(07월 기준 40%) | 위 notateslaapp 4035 | 원문 확인† |
| 2026-05-18 | 무감독 FSD가 "widespread in the US by the end of this year" | 2026-12 | 진행 중 | https://electrek.co/2026/05/18/musk-unsupervised-fsd-widespread-us-end-of-year-smart-mobility-summit/ | 원문 확인† |
| 2026-08-20 | 대수 확대가 2026년 말부터 2027년 초에 걸쳐 빨라진다(JPMorgan에 한 설명) | | 진행 중 | 위 Electrek 08-20 | 원문 확인† |
| 2026-09-04 | Elluswamy, 24시간 운행: "next month or so. the next tech to merge on the v15 plan will enable it." | 2026-10 무렵 | 10-03에 오후 11시까지로 한 시간 연장 | https://www.notateslaapp.com/news/4682/tesla-robotaxis-to-get-fsd-v15-start-running-247-next-month | 원문 확인† |
| 2026-10-03 | Musk: "The main thing we're trying to solve is making sure that we don't run over pets when they're hard to see at night. Literally trying to avoid grey kittens on grey tarmac in the dark." 열화상은 필요 없고 카메라가 "very well in the dark when AI is doing the photon count analysis" | | | https://electrek.co/2026/10/03/tesla-robotaxi-pets-night-musk-lidar/ , https://www.notateslaapp.com/news/4766/tesla-fsds-main-issue-with-nighttime-driving-is-avoiding-pets | 원문 확인† (X 원문은 못 봄) |
| | 고속도로 무감독 승객 운행, 원격 조작자 제거의 일정 | | 테슬라가 말한 날짜를 찾지 못했다 | | |

지킨 정도의 요약(판단): 2025~2026년에 날짜를 박은 약속 가운데 형태까지 그대로 지킨 것은 생산 개시 하나였다. "무감독"류의 약속은 대개 **1~7개월 늦었고 처음에는 좁은 형태로** 왔다(요원을 뒤차로, 2~3대로, 좁은 구간으로). 테슬라가 "다음 달쯤"이라고 한 것은 6주~3개월로, "올해 안"이라고 한 것은 이듬해 상반기로 읽는 편이 지난 기록에 맞다.

---

## 7. 가설을 가르는 표

"가르지 못함"은 그 관찰이 여러 가설과 똑같이 맞는다는 뜻이다.

| # | 관찰 | 지지 | 반박 | 가르지 못함 |
|---|---|---|---|---|
| 1 | Musk가 심야를 닫는 이유로 어두운 길의 저대비 동물 인식을 들었다(10-03) | Hb(인식이 원인이라고 회사가 말함) | Hd(운영이 원인이면 이렇게 말할 까닭이 없다) | Ha 대 Hb. 테슬라는 같은 문제를 소프트웨어("photon count analysis")로 푼다고 한다 |
| 2 | 해가 진 뒤 오후 11시까지는 이미 무감독으로 달린다 | Ha(밤 자체는 열려 있고 한 시간씩 늘린다) | Hb의 강한 형태(카메라는 밤에 못 쓴다) | Hb의 좁은 형태(심야의 저대비 물체) |
| 3 | 운행 시간이 요원이 탈 때는 자정까지였고 요원을 빼자 오후 10시로 줄었다 | Ha·Hb(주행 신뢰도에 대한 자체 평가) | Hd(인력·수요가 원인이면 요원이 탈 때도 같아야 한다) | Ha 대 Hb |
| 4 | 비가 오면 멈춘다(2025-06 ~ 2026-04, 14개월 동안 그대로) | Hb(세 번의 큰 판올림 v13→v14→v15 초기판을 거쳐도 안 풀렸다) | | 2026-04 뒤의 상태를 모른다. Waymo의 비 운행 실적과 직접 견주지 못했다 |
| 5 | EA26002: 역광·차폐물에서 "FSD also lost track of or never detected a lead vehicle", 열화를 스스로 알아차리지 못함 | Hb | | 고객 차의 2023~2024년 판이다. v15·AI4 카메라에 남아 있는지 모른다 |
| 6 | 공개된 로보택시 실패의 대부분이 계획·경로·승하차·멈춤이다(말뚝, 주차장, 건널목 우회, 원격 사고) | Ha(학습으로 줄일 종류), Hd(멈춘 차를 사람이 빼야 한다) | Hb가 **유일한** 원인이라는 설명 | Hb. 닫아 둔 조건의 실패는 보이지 않는다 |
| 7 | 말뚝을 보고 여러 번 선 뒤 밀고 지나감(낮, 시야 좋음) | Ha(계획) | Hb(이 건은 인식 문제가 아니다) | |
| 8 | Waymo도 2026년에 공사 구간·통학 버스·침수로 리콜했고 고속도로를 두 달 멈췄다. 라이다·레이더가 있어도 | "남은 꼬리는 의미 해석"이라는 Ha 쪽 설명 | "센서만 더 달면 풀린다"는 Hb의 따름정리 | |
| 9 | Waymo는 같은 Austin에서 24시간 운행한다 | Hb(센서 차이가 심야 차이와 겹친다) | | 원인이 센서인지, 6년 먼저 시작한 검증 마일인지 가르지 못한다 |
| 10 | 카메라 전용으로 무인 유료 운행을 하는 다른 회사를 확인하지 못했다 | | | 전부. 선례도 반증도 없다(검색 한도로 범위가 좁았다) |
| 11 | 누적 100억 마일을 넘긴 뒤(2026-05)에도 조건이 그대로다 | | Ha의 단순한 형태(데이터 양) | Ha의 "더 큰 모델" 형태 |
| 12 | 공동체 집계: v13 → v14.3에서 치명적 개입 간격 약 4배. 무감독 수준과는 약 25배 차이, 추세상 2031년 무렵 | Ha(나아진다) | Ha의 "다음 판이면 된다"(한 판에 4배로는 25배를 못 메운다) | 로보택시 판과 지오펜스에는 그대로 못 옮긴다 |
| 13 | Dallas·Houston·Florida는 출시일부터 무감독 | Ha(능력이 도시를 넘어 옮겨 간다) | | 낮, 맑은 날, 일반 도로 안에서의 일이다. Hb가 말하는 조건 밖 |
| 14 | 10배 모델이 v14에서 v15로 밀렸다. 메모리 두 배의 AI4+를 만들었다. 사이버캡은 개조 HW4 | Hc의 약한 형태(메모리) | | |
| 15 | 테슬라가 AI5를 차가 아니라 Optimus·데이터센터에 먼저 쓴다. v15는 AI4에서 돈다고 확정. 로보택시가 AI4 계열에서 v15 초기판으로 달린다 | | Hc의 강한 형태(AI5 대기) | 테슬라의 판단이 옳은지는 별개다(HW3 전례) |
| 16 | 테슬라는 시속 10마일 이하 원격 운전을 쓰고 그 중 사고 3건. Waymo는 조언만, 70명이 3,000대 | Hd(설계 차이가 실제로 있다) | | 인원·개입 횟수가 비공개라 Hd의 크기를 잴 수 없다 |
| 17 | 지원 담당이 "end of shift"라 돕지 못함. 등록 476대에 목격 운행 8대(09-22) | Hd | | 목격 집계의 한계. 의도적 속도 조절로도 설명된다 |
| 18 | 테슬라가 24시간 운행을 원격 인력이 아니라 v15의 특정 기술 병합에 걸었다 | Ha | Hd | Hb. 그 병합으로 실제로 열리는지 아직 모른다 |
| 19 | 무감독 100만 마일로는 중상 사고율이 사람보다 낮다는 것을 통계로 보일 수 없다(약 1,400만 마일 필요, 작업자 계산) | "검증 마일이 속도를 묶는다"(Ha의 변형) | "다음 판이 나오면 바로 열린다" | |

---

## 질문에 대한 답

**답.** 넷 중 하나로 떨어지지 않는다. 증거가 가리키는 모양은 이렇다.

1. **운행 조건마다 묶는 것이 다르다.**
   - 대수와 지오펜스, 도시: 묶는 것은 드물게 나오는 계획·의미 해석 실패의 빈도와 그것을 입증할 무감독 마일이다. Ha 쪽이고, 풀리는 중이다(요원 제거 7개월, 지오펜스 14개월에 약 10배, 새 도시는 출시일부터 무감독).
   - 심야와 비: Hb의 좁은 형태가 가장 잘 맞는다. 회사가 인식을 이유로 들었고(관찰 1), 비 중단은 14개월 동안 세 번의 판올림에도 그대로였으며(관찰 4), 1차 자료가 역광·차폐물에서 앞차를 놓친 것을 적었다(관찰 5). 그러나 밤 운행 자체는 이미 네 시간쯤 하고 있어(관찰 2) "카메라는 안 된다"는 강한 형태는 맞지 않는다.
   - 고속도로와 철도 건널목: 가를 증거가 없다. 테슬라는 이유도 일정도 말하지 않았다. 실수의 대가가 큰 곳을 닫아 둔 것이고 이는 Ha(신뢰도 미달)와 Hb 모두와 맞는다.
2. **Hc는 강한 형태로는 반박되고 약한 형태로는 지지된다.** 테슬라는 AI5를 기다리지 않는다(관찰 15). 그러나 메모리가 모델 크기를 묶어 왔다(관찰 14). 로보택시에는 메모리 큰 컴퓨터를 넣어 피해 갔고, 부담은 표준 AI4를 단 고객 차에 남는다.
3. **Hd는 원인이 아니라 결과에 가깝다.** 원격 운전 설계의 차이는 실제이고(관찰 16) 대수가 늘면 병목이 될 수 있다. 그러나 테슬라는 조건을 여는 열쇠를 인력이 아니라 소프트웨어 병합에 걸었고(관찰 18), 요원이 탈 때는 자정까지 달렸다(관찰 3). 차가 덜 멈추면 원격 인력도 덜 든다.

작업자의 확신 정도(판단이고, 숫자는 느낌을 드러내려는 것이다):

| 진술 | 확신 |
|---|---|
| Hd가 주된 원인이 아니다 | 높음(열에 여덟) |
| "AI5가 와야 풀린다"가 아니다(로보택시 fleet에 한해) | 중간 이상(열에 일곱). 테슬라의 믿음이 틀릴 수 있다 |
| 대수·도시를 묶는 것은 Ha 쪽이다 | 중간(열에 여섯) |
| 심야·비는 다음 판만으로는 완전히 안 열린다(Hb의 좁은 형태가 남는다) | 낮음~중간(열에 넷). 가장 불확실하고 가장 중요하다 |

Ha와 Hb를 깔끔하게 가르지 못하는 까닭: 가를 자료는 조건별(낮·밤, 맑음·비) 개입 빈도인데 테슬라가 공개하지 않는다. 그리고 닫아 둔 조건에서는 실패가 관찰되지 않는다.

**가장 이르게 열릴 수 있는 시점(판단).**

| 조건 | 테슬라가 말한 것 | 가장 이른 시점 | 작업자의 중심 예상 | 근거 |
|---|---|---|---|---|
| 24시간 운행(한 도시의 일부 차량) | 2026-10 무렵 | 2026년 4분기 | 2026-12 ~ 2027년 1분기. 연말까지 열릴 가능성은 반반 | 10-03에 한 시간을 실제로 늘렸다. "약 3주"가 6주가 된 전례. 처음에는 좁은 형태로 올 것 |
| 비 오는 날 운행 | 없음 | 알 수 없음 | 24시간보다 늦다 | 14개월 동안 그대로. 일정을 말한 적이 없다 |
| 고속도로 무감독 승객 운행 | 없음 | 2027년 상반기 | 2027년 하반기 이후 | Waymo는 무인 개시 뒤 5년이 걸렸고 열고 6개월 만에 두 달 멈췄다. 테슬라는 날짜를 말하지 않았다 |
| 대수 10배(등록 약 590대 → 약 6천 대) | "2026년 말~2027년 초에 빨라진다" | 2027년 말 | 2028년 | 중상 사고율을 입증할 마일(약 1,400만)이 지금 속도로 2년 반. 대수가 늘면 줄어든다. 앞선 분석의 2030년 말 5천~2만 5천 대와 어긋나지 않는다 |

**앞으로 6개월 안에 판단을 바꿀 관찰.**

| 관찰 | 바뀌는 판단 |
|---|---|
| 24시간 운행이 Austin 전역에서 열리고 석 달 동안 야간 동물·보행자 사고 보고가 없다 | 심야에 대한 Hb가 크게 약해진다. Ha 쪽으로 |
| 24시간 운행이 2027년 1분기를 넘겨도 안 열리거나, 가로등이 있는 구간·일부 차량에만 열린다 | Hb의 좁은 형태가 강해진다 |
| 비 오는 날 무감독 운행을 시작한다 | Hb가 가장 크게 약해진다. 14개월 묵은 제한이 풀리는 것이다 |
| 테슬라가 사이버캡에 카메라 밖의 감지 장치(레이더, 열화상, 조명)를 더한다 | Hb가 사실상 확정된다 |
| 상시 일반 명령 보고에 사이버캡의 야간·역광 사고가 나온다 | Hb 쪽으로 |
| v15 완성판이 표준 AI4 Model Y 로보택시에는 안 가고 메모리 큰 차에만 간다. 또는 고객용 v15가 "줄인 판"으로 나오거나 미뤄진다 | Hc의 약한 형태가 강해진다. 고객 소유 차 경로의 가치가 내려간다 |
| 테슬라가 AI5를 차에 넣는 일정을 당긴다 | Hc의 강한 형태가 되살아난다 |
| 공동체 집계에서 v15가 큰 표본으로 치명적 개입 1회당 1만 마일을 넘는다 | Ha가 강해진다 |
| 테슬라가 원격 인력 수나 개입 횟수를 공개한다. 또는 등록 대수와 실제 운행 대수의 차이가 좁혀진다 | Hd의 크기를 처음으로 잴 수 있다 |
| 무감독 주간 마일이 지금(주 약 10만)의 서너 배로 오른다 | 대수 10배의 시점이 당겨진다 |

**범위.** 이 답은 Texas와 Florida의 테슬라 직영 로보택시(Model Y와 사이버캡)에 대한 것이다. 고객 차의 무감독 FSD는 5절에서 컴퓨터 문제만 다뤘다. California는 규제가 따로 묶는다(앞선 조사).

**남은 공백.**

- Musk와 Elluswamy의 X 원문을 직접 보지 못했다. 인용은 모두 2차 매체를 거쳤다.
- 조건별 개입 빈도, 원격 개입 횟수, 원격 인력 수. 테슬라가 공개하지 않는다. Ha와 Hb, Hd를 가를 핵심 자료다.
- 사이버캡에 지금 차 안 요원이 타는지. Tesla North의 서술과 "무감독"이라는 회사 표현이 어긋난다.
- 비 오는 날 운행의 2026-04 이후 상태. 운행 시간이 자정에서 오후 10시로 줄어든 날짜.
- 테슬라의 고속도로 운행 이력(2025년에 요원을 운전석에 앉히고 했다는 것은 기억이다).
- Cortex의 H100 환산 대수와 전력. AI5의 "40x" 발언. Elluswamy 발표의 입력 규모 수치.
- FSD Community Tracker 원자료. Dominik Roth의 글 하나에 기댔다.
- Missy Cummings, Brad Templeton, Bloomberg, 학술 논문의 독립 분석. Waymo 블로그의 "false summit" 원문과 야간 시연 원문. Wayve·comma·Mobileye의 현황. 검색 한도 때문에 찾지 못했다.
- Waymo가 도시별로 24시간 운행과 비 운행을 시작한 날짜. 관찰 9의 비교가 그만큼 약하다.
- 목격 집계의 "실제 운행 8대"(09-22)와 그 뒤 사이버캡 등록 급증(169대) 사이의 관계.
