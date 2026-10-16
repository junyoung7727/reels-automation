# 사이버캡이라는 제품: 2026년에 실제로 나온 차

조사일: 2026-10-05. 질문은 하나다. "2026년에 출고된 사이버캡은 정확히 어떤 차인가. 하드웨어는 무엇이고, 무엇이 실제로 새롭고, 2024년 약속 중 무엇이 지켜졌고, 어떤 하드웨어 선택이 무인 운행을 돕거나 막는가."

제조 공정(기가캐스팅, 언박스드 조립, 도장 공정 없음, 10초 목표)은 `production/reel-04/sources.md`에 이미 있어 다시 조사하지 않았다. 원격 조작 사고와 충전 기지 허가는 `../cybercab-outlook/stakeholders.md` 5-3과 `binding-constraint.md` 4장에 있는 것을 "기존 조사"로 끌어다 썼다.

## 읽는 법

확인 수준:

- **원문 확인(직접 읽음)**: 문서를 받아 쪽마다 직접 읽었다. 이번에는 Tesla의 사이버캡 긴급대응 문서(PDF, v1.2, 2026-09-03, 본문 28쪽) 한 건뿐이다.
- **원문 확인†(요약 도구로 읽음)**: 해당 URL을 열어 요약 도구(WebFetch)가 뽑아 준 내용이다. 인용문은 자막에 쓰기 전에 원문과 글자 그대로 대조해야 한다.
- **검색 요약만**: 원문을 열지 못하고 다른 문서(주로 위키백과)의 인용으로만 본 것이다. 괄호에 경유한 문서를 적었다.
- **기존 조사**: 같은 저장소의 다른 조사 파일에 적힌 사실. 확인 수준은 그 파일을 따른다.

구분 열: **발표**(회사·임원이 말한 것), **목표**(앞으로 하겠다는 것), **실제**(인증 서류·운행 문서·현장 관찰로 확인된 것), **해석**(남의 평가).

**이번 조사의 제약.** 검색 도구의 세션 한도(200회)가 이미 소진돼 **검색을 한 번도 하지 못했다.** 알고 있는 URL, 위키백과 참고문헌 목록, 매체의 주제별 목록 페이지를 따라가며 원문을 열었다. 그래서 "찾지 못했다"는 "없다"가 아니라 "이 경로로는 닿지 못했다"는 뜻이다. MotorTrend, Car and Driver, Wired, The Verge, Reuters, PCMag, CNBC, tesla.com 본문은 열리지 않았다(차단 또는 403).

---

## 1. 제원: 2024년 발표와 2026년 출고 차

### 1-1. 2024년 10월 "We, Robot"과 직후에 한 약속

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 가격 "available to purchase for less than $30,000". 생산은 2026년 시작, Musk는 자기가 일정에 낙관적이라며 "before 2027"로 고쳐 말했다 | 2024-10-10 | https://www.carscoops.com/2024/10/tesla-cybercab-is-a-robotaxi-youll-be-able-to-buy-for-less-than-30000/ | 원문 확인† | 발표·목표 |
| 무선 유도 충전, 충전구 없음. 버터플라이 문 2개, 운전대·페달 없음, 큰 화면 | 2024-10-11 | https://tech.yahoo.com/teslas-cybercab-robotaxi-yet-still-072131923.html (Mashable) | 원문 확인† | 발표 |
| CNBC 영상 제목: "Tesla CEO Elon Musk: The Cybercab has no plug, uses inductive charging" | 2024-10-10 | https://www.cnbc.com/video/2024/10/10/tesla-ceo-elon-musk-the-robotaxi-has-no-plug.html | 검색 요약만 (위키백과 참고문헌 제목) | 발표 |
| Musk: "It will cost on the order of -- cost roughly 25K, so it is a 25K car." / "we're aiming for at least 2 million units a year of Cybercab" / "I do feel confident of Cybercab reaching volume production in '26" | 2024-10-23 (3분기 실적 발표) | https://www.fool.com/earnings/call-transcripts/2024/10/23/tesla-tsla-q3-2024-earnings-call-transcript/ | 원문 확인† | 발표·목표 |
| 무선 충전 효율: Tesla 공식 계정 "Efficiency is well above 90%". 시연 영상의 출력은 충전량 35%에서 19kW, 다른 영상에서 25kW | 2024-10-19 | https://www.teslarati.com/tesla-wireless-charging-efficiency-above-90/ | 원문 확인† | 발표 |
| 수석 엔지니어 Eric Earley: "We're gonna be delivering a car that has roughly half the parts of Model 3 today." / "You really just have what looks like a bench seat, easy to clean automatically." / "82% of miles driven today are with two or fewer passengers." 트렁크에는 기내용 가방 2개와 위탁 가방 2개가 함께 들어간다고 설명 | 2024-12-06 | https://www.teslarati.com/tesla-lead-engineer-cybercab-half-parts-model-3/ | 원문 확인† | 발표 |
| Tesla IR 책임자가 Deutsche Bank에 한 말(은행 보고서의 표현): "Tesla believes it would be reasonable to assume some type of teleoperator would be needed at least initially for safety/redundancy purposes." | 2024-12-09 | https://www.teslarati.com/tesla-plan-cybercab-safety-measure/ | 원문 확인† | 발표 |
| AI5(당시 HW5): HW4보다 10배 강력, 복잡한 환경에서 최대 800W(HW3 100W, HW4 160W). 출시는 2026-01 예정이라고 했다 | 2024-06-13 (주주총회) | https://en.wikipedia.org/wiki/Tesla_Autopilot_hardware (autoevolution 2024-06-14, SemiAnalysis 2023-06-27 인용) | 검색 요약만 (위키백과 경유) | 발표·목표 |

2024년 행사에서 Musk가 말했다고 널리 알려진 것 중 **이번에 원문으로 확인하지 못한 것**: 운영비 "마일당 20센트", 청소 로봇 팔 시연, 사이버캡에 AI5를 넣는다는 발언. Not a Tesla App(2026-09-04)이 "probably going to be around 20 cents a mile"을 Musk의 과거 발언으로 옮겼지만 원 발언 시점은 확인하지 못했다.

### 1-2. 2026년 출고 차의 제원

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| EPA 인증 서류(5-21 제출, 5-26 인증): 배터리 47.6kWh(146Ah, 326V), 전륜 단일 모터 "AC 3-Phase Permanent Magnet" 163kW(219마력), 공차중량 3,113lb(1,412kg), 총중량 3,730lb, 적재 약 617lb, 미조정 복합 주행거리 418.2마일, 고속 375.4마일, 조정 뒤 약 293마일, 165Wh/mi. 최고속도·치수·타이어는 서류에 없다 | 2026-06-15 | https://electrek.co/2026/06/15/tesla-cybercab-epa-specs-curb-weight-battery-motor-power/ | 원문 확인† (EPA 서류 자체는 열지 못함) | 실제 |
| 같은 서류의 다른 판독: 배터리 비에너지 154Wh/kg, 인증상 "Useful Life Rating" 150,000마일. 위키백과는 Car and Driver를 인용해 145Wh/kg, 255.2V로 적었다. **수치가 서로 다르다** | 2026-06-16 | https://evwire.com/p/tesla-cybercab-epa-certification-specs-revealed , https://en.wikipedia.org/wiki/Tesla_Cybercab | 원문 확인† | 실제 (불일치) |
| 차량 공학 부사장 Lars Moravy가 165Wh/mi를 인증 수치라고 확인. Electrek의 비교(EPA): Lucid Air Pure RWD 230, Model 3 RWD 240, Model Y RWD 240, Ioniq 6 SE RWD 241 Wh/mi | 2026-05-22 | https://electrek.co/2026/05/22/tesla-cybercab-most-efficient-ev-ever-165-wh-mi/ | 원문 확인† | 실제 |
| 4680 셀, 88S6P 구성 | 2026 | https://en.wikipedia.org/wiki/Tesla_Cybercab | 원문 확인† (위키백과) | 실제 (2차) |
| 출시 행사 발표: 공기저항계수 0.20 미만. 구동 장치 "18% smaller while being 25% lighter and more efficient". 히트펌프(Super Manifold V3) "38% more efficient than other thermal systems". 앞좌석 다리 공간 43.4인치. 트렁크 20.2 cu ft(572L), 적재 220lb. 화면 21인치. 카메라 9개, 천장 레이더, 유압 없는 브레이크, Starlink V5 안테나 | 2026-09-04 | https://www.notateslaapp.com/news/4650/tesla-cybercab-event-highlights-everything-tesla-showed-off | 원문 확인† | 발표 |
| 화면 크기는 출처마다 다르다. 21인치(위 기사, Basenor 09-08), 22인치(Not a Tesla App 09-04 다른 기사), 24인치(디자인 책임자 von Holzhausen, 2026-02-23 인터뷰 "A 24-inch screen anchors the cabin") | 2026 | https://www.notateslaapp.com/news/4651/cybercab-joins-teslas-robotaxi-fleet-with-cheaper-fares , https://www.cardesignnews.com/designers/designing-the-future-from-first-principles-von-holzhausen-on-the-tesla-cybercab/2612995 | 원문 확인† | 불일치 |
| 폭 69인치(위키백과: 초대 Roadster를 포함해 어느 Tesla보다 좁다). 승하차 높이 16.5인치. 전장·전고·축거는 찾지 못했다 | 2026-09 | https://teslanorth.com/2026/09/09/tesla-cybercab-cost-per-mile/ , https://www.basenor.com/blogs/news/tesla-cybercab-is-live-your-robotaxi-questions-answered | 원문 확인† (2차) | 실제 (2차) |
| 좌석 2개. 운전대·가속·브레이크 페달 "not typically equipped". 사이드미러 없음, 글러브박스 없음. 좌석은 전동이고 두 좌석이 함께 앞뒤로 움직인다 | 2026-09-03 | https://digitalassets.tesla.com/tesla-contents/image/upload/cybercab-first-responder-interaction-plan.pdf (5, 22쪽) | 원문 확인(직접 읽음) | 실제 |
| 브레이크: 유압 없는 전기기계식. "an actuator on each brake caliper [is] triggered with an electrical signal". The Drive: "a completely electric brake-by-wire system, which is still (almost) unheard of in 2026". 공급사는 Brembo Sensify일 것이라는 추측(미확인). 올해 Chery Exeed EX7이 "first mass-produced"를 먼저 주장했다 | 2026-09-04 | https://www.thedrive.com/news/tesla-cybercab-isnt-just-missing-a-steering-wheel-it-doesnt-even-have-brake-lines , 위 Not a Tesla App 4650 | 원문 확인† | 실제 / 해석 |
| 조향: "Steer-by-wire and brake-by-wire systems"라는 한 줄뿐. 조향 액추에이터 수, 이중화 구성은 어느 자료에도 없다 | 2026-09-04 | https://www.notateslaapp.com/news/4651/cybercab-joins-teslas-robotaxi-fleet-with-cheaper-fares | 원문 확인† | 실제 (근거 얇음) |
| 저전압 계통은 48V. 점프 스타트도 48V 전원만 된다("12V and 16V won't work"). "cutting the cables of the low voltage battery alone doesn't necessarily disable the low voltage system due to system redundancies". 고전압 차단용 First Responder Loop가 2개(후드 아래, B필러 안쪽). 에어백 제어기(RCM)는 약 10초짜리 예비 전원이 있다 | 2026-09-03 | 위 Tesla PDF (15~17, 28쪽) | 원문 확인(직접 읽음) | 실제 |
| 문: B필러의 버튼 또는 화면으로 연다. 승객을 태울 때 자동으로 열 수 있다. 전동 스트럿과 예압 스프링. 안쪽 손잡이는 2단이고 2단째가 기계식 비상 해제다. 전원 없이 열면 "The door will be heavy and will not remain open. The window may crack or break if still rolled up." 문 경로에 장애물이 있으면 열리지 않고, 길게 눌러 무시할 수 있다 | 2026-09-03 | 위 Tesla PDF (18~20쪽) | 원문 확인(직접 읽음) | 실제 |
| 트렁크: 해치식. 화면의 버튼이나 트렁크 손잡이 아래 스위치로 연다 | 2026-09-03 | 위 Tesla PDF (21쪽) | 원문 확인(직접 읽음) | 실제 |
| 바퀴: 금색 휠 커버는 클립으로 끼운 덮개다. 벗기면 검은 휠과 러그 너트가 나온다. 견인은 네 바퀴를 모두 띄워야 한다 | 2026-09-03 | 위 Tesla PDF (23~25쪽) | 원문 확인(직접 읽음) | 실제 |
| 충전: 뒤쪽 숨은 NACS 포트로 DC 급속 충전만 된다. 차 안에 충전기(OBC)가 없어 AC 충전이 안 된다. Kyle Conner(Out of Spec): "It does not support AC charging...for fleet only, there's no OBC - which is kind of cool for cost / durability optimization." | 2026-09-05 | https://www.notateslaapp.com/news/4653/tesla-cybercab-doesnt-support-ac-charging | 원문 확인† | 실제 |
| 무선 충전은 지금 쓰이지 않는다. Austin St. Elmo 기지 허가 신청서: 1단계 V4 Supercharger 48기, 2단계 무선 충전기 80기. 완공 시점 없음 | 2026-08-19 | https://evwire.com/p/tesla-cybercab-wireless-chargers-austin-robotaxi-hub | 원문 확인† | 목표 |
| 현장 영상: 공용 Supercharger로 보이는 곳에서 직원 한 명이 걸어다니며 로보택시 10대(사이버캡 1대, Model Y 9대)에 케이블을 꽂는다. "A Tesla employee is walking around and plugging each of them in." | 2026-10-02 촬영 | https://teslanorth.com/2026/10/04/cybercab-driverless-supercharger-charging/ | 원문 확인† (X 영상을 옮긴 기사) | 실제 |
| 모터: Musk가 X에서 희토류를 쓰지 않는다고 확인. EPA 서류는 영구자석 모터라고 적었다. Electrek은 페라이트나 알니코 자석일 것으로 추측했고(미확인) "Real benefit is packaging"이라고 평가했다 | 2026-09-04 | https://electrek.co/2026/09/04/teslas-new-rare-earth-free-ev-motor-is-a-big-deal-but-not-that-big-a-deal/ | 원문 확인† | 발표 / 해석 |
| 설계 수명 500,000마일 | 2026-09-05 | https://www.basenor.com/blogs/news/tesla-cybercab-is-live-your-robotaxi-questions-answered | 원문 확인† (액세서리 판매업체 블로그, 신뢰도 낮음) | 발표 (2차) |
| 가격: Basenor는 "$25,000"이라고 적었고 Electrek은 "a vehicle Tesla is trying to build for $30,000"이라고 썼다. Tesla는 2026년에 소비자 가격을 발표하지 않았고 차는 Tesla가 소유·운영한다. 외부 사업자에게는 관심 등록만 받는다 | 2026-09 | 위 Basenor, https://electrek.co/2026/08/10/tesla-first-cybercab-starlink-integration/ , 위 Tesla PDF 11쪽("All Robotaxi vehicles are owned and operated by Tesla at this time") | 원문 확인† / 원문 확인(직접 읽음) | 2024년 숫자의 반복. **실제 원가는 미공개** |
| 접근성: 버튼의 점자, 음성 조작, 휠체어 높이에 맞춘 좌석 | 2026-09-03 | https://en.wikipedia.org/wiki/Tesla_Cybercab (Basenor 인용) | 원문 확인† (위키백과) | 발표 (2차) |

### 1-3. 약속과 출고 차를 나란히

| 항목 | 2024년 발표 | 2026년 출고 | 판정 |
|---|---|---|---|
| 운전대·페달·미러 | 없음 | 없음. 단 시험용 차에는 운전대와 페달을 단다 | 지켜짐 |
| 좌석·문 | 2인승, 버터플라이 문 | 같음. 자동 개폐 | 지켜짐 |
| 부품 수 | Model 3의 약 절반 | von Holzhausen(2026-02) "That meant halving part count". 독립 분해 자료는 찾지 못했다 | 회사 발표만 있음 |
| 충전 | 충전구 없음, 무선만 | 숨은 NACS 포트로 DC 급속 충전, 사람이 꽂는다. 무선은 허가 단계 | **지켜지지 않음** |
| 가격 | 3만 달러 미만, 약 2만 5천 달러 | 판매하지 않음. 원가 미공개 | 판단 불가 |
| 대량 생산 | 2026년 | 설치 능력은 있으나 운행 등록 169대(기존 조사) | 부분적 |
| 자율주행 컴퓨터 | AI5가 2026-01 출시 예정이었다(사이버캡 탑재 발언은 이번에 원문 미확인) | AI4 계열(메모리 증설판으로 보도) | 2장 참조 |
| 청소 | "easy to clean automatically" | Tesla 문서가 "cleaning station"을 언급하지만 방식은 공개되지 않았다 | 확인 불가 |
| 효율 | 수치 약속을 찾지 못했다 | 165Wh/mi 인증 | 실제 |

---

## 2. 센서와 컴퓨터

### 2-1. 센서

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 주행 센서는 카메라뿐이다. 라이다·주행용 레이더 없음 | 2026-09-05 | https://cleantechnica.com/2026/09/05/10-facts-about-the-tesla-cybercab/ | 원문 확인† | 실제 |
| "Nine cameras"와 "ceiling-mounted radar sensor". 천장 레이더는 주행용이 아니라 좌석에 어른, 카시트, 빈자리 중 무엇이 있는지 가려 에어백을 조절한다. 요약 도구가 9개를 "cabin"의 것으로 옮겨 **9개가 차 전체 수인지 불분명하다** | 2026-09-04 | https://www.notateslaapp.com/news/4650/tesla-cybercab-event-highlights-everything-tesla-showed-off | 원문 확인† | 발표 (모호) |
| Tesla 문서: "Cybercab has cameras on the front fender." B필러에 카메라가 있다(구조대원이 신분증을 보여 주는 곳). "equipped with a camera suite and sound detection technology"로 긴급차량의 경광등과 사이렌을 감지한다. 외부 마이크는 양쪽 B필러, 외부 스피커는 차 바닥 | 2026-09-03 | 위 Tesla PDF (3, 8, 10쪽) | 원문 확인(직접 읽음) | 실제 |
| 문서의 그림에서 본 것: 앞 번호판 아래 범퍼에 렌즈 하나, 뒤 라이트바 가운데에 렌즈 하나, 실내 천장 앞쪽에 장치 하나. 그림을 눈으로 본 것이고 문서가 글로 밝힌 것은 아니다 | 2026-09-03 | 위 Tesla PDF (3, 5, 24쪽 그림) | 원문 확인(직접 읽음), **작업자의 관찰** | 실제 (약함) |
| GPS 2개("dual GPS for better position tracking") | 2026-07-11 | https://www.notateslaapp.com/news/4422/tesla-to-start-fully-autonomous-cybercab-employee-rides-soon | 원문 확인† | 실제 (2차) |
| 카메라 세척: 앞유리 와이퍼는 그림에 있다. 펜더·B필러·후방 카메라의 세척 노즐이나 열선은 어느 자료에도 없다. Elluswamy는 1분기 발표에서 소비자 차에 대해 "If the camera is not able to see things clearly because of residue buildup or what have you, then the FSD won't be available for those cars."라고 했다 | 2026-04-23 | https://evwire.com/p/tesla-tsla-q1-2026-earnings-call-full-transcript | 원문 확인† | 실제 (사이버캡 세척 장치는 **모름**) |
| 비: Elluswamy "Tesla Robotaxis work equally well in the rain"(2026-09-07 X). 10-03 폭우 주행 영상. Tesla 문서의 운행 조건은 "light and moderate precipitation such as rain, fog, and snow"까지이고 폭우·침수·눈길·빙판은 "not intended for use in such situations at this time" | 2026-09~10 | https://www.basenor.com/blogs/news/tesla-cybercab-operates-in-heavy-rain-what-it-means-for-the-robotaxi-rollout , 위 Tesla PDF 11쪽 | 원문 확인† / 원문 확인(직접 읽음) | 발표 / 실제 |
| 밤: 운행은 23시까지다. Musk는 이유를 "grey kittens on grey tarmac in the dark"라고 했고 카메라가 "very well in the dark when AI is doing the photon count analysis"라고 했다. 열화상 카메라 추가는 거부했다 | 2026-10-03 | https://www.notateslaapp.com/news/4766/tesla-fsds-main-issue-with-nighttime-driving-is-avoiding-pets | 원문 확인† | 발표 |

**카메라 배치가 Model Y와 다른가.** 확인하지 못했다. Electrek의 Fred Lambert는 출시 전 글에서 "the same cameras, same FSD, same problems, smaller box"라고 썼다(https://electrek.co/2026/08/28/tesla-cybercab-launch-predictions/, 원문 확인†, 의견). 위치·높이가 Model Y와 얼마나 다른지 잰 자료는 찾지 못했다.

Musk가 2분기 발표(2026-07-22)에서 든 이유는 카메라가 아니라 **차대**였다. "because it is a new vehicle chassis, we need to accumulate driving data that is specific to the Cybercab"(기존 조사, `binding-constraint.md` 40행). Fool 판본에는 "we actually have to accumulate miles with Cybercab that are retrofitted with steering wheels and brakes ... to calibrate to the Cybercab chassis"가 이어진다(https://www.fool.com/earnings/call-transcripts/2026/08/05/tesla-tsla-q2-2026-earnings-call-transcript/, 원문 확인†, 녹취 오타 있음). "카메라 위치가 달라서 새 데이터가 필요하다"는 문장은 Tesla가 한 말이 아니다.

### 2-2. 자율주행 컴퓨터

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 사이버캡의 FSD 컴퓨터는 소비자용 Model 3·Y의 것보다 메모리가 많다(표준 AI4는 칩 2개 × 16GB = 32GB). 기사는 세 가지 가능성을 열어 뒀다: 시제 AI4+, AI4 보드 2장, 초기 AI5. 출처는 "very reliable"이라고만 했다 | 2026-07-07 | https://www.notateslaapp.com/news/4409/exclusive-tesla-cybercab-includes-more-powerful-fsd-hardware | 원문 확인† (익명 출처) | 실제 (미확정) |
| 출시 행사 보도: "similar autopilot computer to HW4 with some iterative updates" | 2026-09-03 | https://www.statesman.com/business/article/tesla-cybercab-austin-launch-live-updates-22414898.php | 검색 요약만 (위키백과 경유, 원문은 열리지 않음) | 실제 (2차) |
| Tesla가 JPMorgan에 한 설명: 지금의 HW4(AI4)로 v15와 무감독 FSD를 돌릴 수 있다. AI4.5는 연산 약 10% 증가, 메모리 2배. AI5는 2027년 중반으로 미뤄졌다 | 2026-08-20 | https://electrek.co/2026/08/20/tesla-jpmorgan-fremont-fsd-v15-hw4-optimus-2027/ | 원문 확인† | 발표 |
| Musk: "We are planning an AI4 upgrade to use newer generation RAM. So it'll go from 16 gigabytes to I think 32 gigabytes per SOC, so a total of 64 GB." / "probably a 10% increase in compute ... AI4+ probably goes into production middle of next year." / "Samsung is doing the modifications for us" | 2026-04-23 (1분기 발표) | https://evwire.com/p/tesla-tsla-q1-2026-earnings-call-full-transcript | 원문 확인† | 목표 |
| Musk(X): "AI4 is enough to achieve much better than human safety for FSD." AI5의 용도를 묻자 "Optimus and our supercomputer clusters." AI5 설계 완료(tape-out)를 알리며 TSMC와 Samsung에 감사했다 | 2026-04-15 | https://www.teslarati.com/tesla-finalizes-ai5-chip-design-elon-musk-makes-bold-claim-capability/ | 원문 확인† | 발표 |
| 석 달 전 Musk(X): "AI4 by itself will achieve self-driving safety levels very far above human. AI5 will make the cars almost perfect and greatly enhance Optimus. AI6 will be for Optimus and data centers." 기사는 AI5 추론 성능을 AI4의 40~50배로 적었다 | 2026-01-19 | https://www.notateslaapp.com/news/3515/musk-targets-9-month-chip-cycle-for-tesla-talks-ai5-ai6-and-space-based-ai | 원문 확인† | 발표 |
| Musk(2분기 발표): "We have an upgraded AI chip that's ... moderate improvement over AI4, probably reaches production around the middle of next year. And then there's also AI5, which hopefully is in volume production around the middle of next year." | 2026-07-22 | 위 Fool 2분기 녹취록 | 원문 확인† | 목표 |
| HW4 칩은 Samsung 7nm(화성). 소비전력 최대 160W. 카메라 8개 구성 | 2021~2023 | https://en.wikipedia.org/wiki/Tesla_Autopilot_hardware (Korea Economic Daily 2021-09-23, SemiAnalysis 2023-06-27 인용) | 검색 요약만 (위키백과 경유) | 실제 (2차) |
| AI6: Samsung과 165억 달러 공급 계약(2025-07). Musk 2026-01: 차량용이 아니라 Optimus와 데이터센터용 | 2025-07-28, 2026-01 | 위 위키백과 (Reuters 2025-07-28 인용), 위 Not a Tesla App 3515 | 검색 요약만 / 원문 확인† | 발표 |
| HW3 전례: Tesla는 여러 해 동안 HW3로 충분하다고 했다가 지금은 HW3 차에 "FSD v14 Lite"만 준다. Musk는 2분기 발표에서 HW4 미만 차의 교체가 "make sense"하다고 했다 | 2026-08-20, 2026-07-22 | 위 Electrek 08-20, 위 Fool 녹취록 | 원문 확인† | 실제 / 해석 |

정리하면 **출고된 사이버캡은 AI5가 아니라 AI4 계열로 달린다.** AI5의 대량 생산은 2027년 중반이 목표이고, 차에 들어가는지는 Musk의 말이 석 달 사이에 달라졌다(1월 "will make the cars almost perfect", 4월 "Optimus and our supercomputer clusters"). 연산 이중화(칩 2개가 서로를 대신하는지)는 2026년 자료에서 찾지 못했다. AI5의 공정(몇 나노), 사이버캡 컴퓨터의 소비전력도 찾지 못했다.

---

## 3. 원격 운영과 통신

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| Tesla 직원이 원격으로 할 수 있는 일(문서에 적힌 것): 문·후드·트렁크 잠금 해제, 창문 내리기, 차 안팎 스피커와 마이크로 양방향 통화, 자율주행 모드 해제와 재개, "remotely moves the vehicle" | 2026-09-03 | 위 Tesla PDF (7~10쪽) | 원문 확인(직접 읽음) | 실제 |
| "If Cybercab Robotaxi experiences connectivity or hardware issues, the hazard lights flash rapidly and the vehicle attempts to pull over at the nearest safe stopping location." | 2026-09-03 | 위 Tesla PDF (6쪽) | 원문 확인(직접 읽음) | 실제 |
| 자율주행 모드가 꺼지면 Tesla 직원이 사건을 검토하고 직접 다시 켜기 전에는 재개되지 않는다. 안전벨트를 풀거나 문을 열어 두면 주행을 멈추고 주차한다 | 2026-09-03 | 위 Tesla PDF (7, 13쪽) | 원문 확인(직접 읽음) | 실제 |
| 원격 운영자는 시속 10마일 이하에서 차를 직접 몰 수 있다. 원격 조작 중 사고 3건(Model Y) | 2026-05~07 | 기존 조사 `../cybercab-outlook/stakeholders.md` 5-3 | 기존 조사 | 실제 |
| 화면에 숨은 수동 주행 모드: 터치스크린의 가상 조이스틱으로 차를 움직인다. 승객이 우연히 발견했다("I have a feeling I wasn't supposed to see this."). 속도 제한과 사용 권한은 알려지지 않았다. 구조대원은 Tesla의 승인을 받아 "onboard vehicle controls"로 차를 옮길 수 있다 | 2026-09-08 | https://electrek.co/2026/09/08/tesla-cybercab-hidden-virtual-joystick-manual-driving/ , 위 Tesla PDF 10, 26쪽 | 원문 확인† / 원문 확인(직접 읽음) | 실제 |
| Starlink V5 안테나를 지붕(해치)에 매립. 09-08에 Giga Texas 출고장에서 다수 확인. V5 제원(Basenor): 375Mbps 이상, 306×384mm, 1.1kg, 평균 35~50W | 2026-08-10, 09-08 | https://electrek.co/2026/08/10/tesla-first-cybercab-starlink-integration/ , https://teslanorth.com/2026/09/08/tesla-cybercab-starlink-giga-texas/ , https://www.basenor.com/blogs/news/starlink-v5-in-cybercab-6-details-that-matter | 원문 확인† | 실제 |
| Elluswamy: Starlink는 "for navigation, customer service, and fleet management"이고 안전한 자율주행에 필요한 것은 아니다. Musk: "for a robotaxi situation, you need to have coverage everywhere." / "So we don't have robotaxis missing in action." | 2026-07-21~22 | https://www.teslarati.com/tesla-starlink-elon-musk-ai-cars/ , 위 Fool 2분기 녹취록 | 원문 확인† | 발표 |
| Electrek의 평가: 운행 도시는 모두 통신망이 좋은 도심이라 위성 안테나는 "redundant hardware"이고 비용·무게·월 요금을 더한다 | 2026-08-10 | 위 Electrek 08-10 | 원문 확인† | 해석 |

셀룰러 모뎀의 사양, 통신사, 원격 주행 때의 지연 시간, 원격 인원수는 찾지 못했다.

---

## 4. 다른 로보택시와 비교

| 항목 | 사이버캡 | Tesla Model Y 로보택시 | Waymo Ojai (Zeekr, 6세대) | Zoox |
|---|---|---|---|---|
| 주행 센서 | 카메라(9개로 보도), 외부 마이크 | 카메라 8개(HW4 구성) | 카메라 13개 이상, 라이다 4, 레이더 6, 외부 음향 수신기 | 카메라·라이다·레이더(개수는 이번에 확인 못 함) |
| 센서 세척 | 앞유리 와이퍼. 그 밖은 모름 | 모름 | 와이퍼 10개(센서용 소형 포함) | 모름 |
| 컴퓨터 | AI4 계열, 메모리 증설판으로 보도 | AI4(칩 2개 × 16GB) | 비공개 | 비공개 |
| 수동 조작 장치 | 없음(시험차만 있음) | 있음 | 위키백과 요약은 운전대가 없다고 했으나 "운전석은 승객이 못 쓴다"는 서술과 맞지 않는다. **미확인** | 없음 |
| 승객 | 2 | 4 | 4 | 4(기억, 미확인) |
| 배터리 | 47.6kWh | 이번에 확인 안 함 | 93kWh, 800V | 133kWh(기억, 미확인) |
| 효율 | 165Wh/mi(인증) | 240Wh/mi(Model Y RWD 18인치 EPA) | 공식 수치 없음 | 모름 |
| 충전 | DC 급속(NACS), 사람이 꽂음. 무선은 계획 | NACS AC·DC | 모름 | 모름 |
| 차 값 | Tesla 목표 2만 5천~3만 달러. 실제 원가 미공개 | 이번에 확인 안 함 | Waymo 차량 일반 추정 "over $120,000"(Morgan Stanley), "$150,000", "above $100,000" | 모름 |
| 이중화 | 48V 저전압 "system redundancies", 차단 루프 2개. 조향·제동·연산 이중화는 공개 자료 없음 | 모름 | "three complementary sensing modalities" | 양방향 대칭 차체, 시속 75마일 |
| 운행 규모 | 등록 169대(2026-10-02, 기존 조사) | Texas 약 420대 등록 | Waymo 전체 3,000대, 주 50만 건(2026-03) | 약 50대(2026-01) |

출처: Waymo 6세대 https://waymo.com/blog/2024/08/meet-the-6th-generation-waymo-driver (2024-08-19, 원문 확인†). Ojai https://en.wikipedia.org/wiki/Waymo_Ojai (원문 확인†, 위키백과). Waymo 비용·규모 https://en.wikipedia.org/wiki/Waymo (원문 확인†, 위키백과). Zoox https://en.wikipedia.org/wiki/Zoox_(company) (원문 확인†, 양방향·시속 75마일·약 50대만 확인. 4인승과 133kWh는 2020년 공개 제원에 대한 작업자의 기억이고 이번에 원문을 열지 못했다). Model Y 대수는 https://www.basenor.com/blogs/news/tesla-cybercab-fleet-hits-158-in-texas-your-questions-answered (원문 확인†, 신뢰도 낮음). Model Y 효율은 위 Electrek 05-22.

이 표는 빈칸이 많다. 경쟁사 원가, 컴퓨터, 이중화 구성은 회사들이 공개하지 않았거나 이번 경로로 닿지 못했다.

---

## 5. 전문가의 평가

| 평가 | 날짜 | 출처 | 확인 | 누구 |
|---|---|---|---|---|
| "Calling the Cybercab the 'most efficient EV ever' is technically accurate, but it's a bit like comparing a motorcycle's fuel economy to a sedan's." 운전대 축, 페달, 다인승 충돌 구조가 없는 2인승이라는 이유다 | 2026-05-22 | 위 Electrek 05-22 | 원문 확인† | Fred Lambert (Tesla에 비판적인 매체 편집장) |
| 브레이크: "still (almost) unheard of in 2026". 장점으로 원가, 바퀴별 제동 제어, 회생제동과의 결합을 들었다 | 2026-09-04 | 위 The Drive | 원문 확인† | Andrew P. Collins (자동차 기자) |
| 충전기 없는 설계: "kind of cool for cost / durability optimization" | 2026-09-05 | 위 Not a Tesla App 4653 | 원문 확인† | Kyle Conner (Out of Spec Reviews, 충전 전문 리뷰어) |
| 희토류 없는 모터: "a big deal, but not THAT big a deal". 모터는 이미 입력의 90% 이상을 회전력으로 바꾸므로 효율 개선 폭은 작고 실익은 포장 크기라고 봤다 | 2026-09-04 | 위 Electrek 09-04 | 원문 확인† | Jameson Dow |
| "The bottleneck is FSD. ... no amount of hardware coming off the line in Austin changes that." | 2026-07-06 | https://electrek.co/2026/07/06/tesla-cybercab-production-before-autonomy/ | 원문 확인† | Fred Lambert |
| 원격 조작 의존에 대해: "Eventually you will lose connection at exactly the worst time. With a million cars, it's going to happen every day." | 2026-05-26 | 기존 조사 `stakeholders.md` 5-3 | 기존 조사 | Philip Koopman (자율주행 안전 연구자) |
| 설계자 본인의 설명: "A standard hinged door isn't optimal for ingress and egress in a shared autonomous environment." / "If you examine ride-share data, roughly 90-95% of trips involve a single occupant." / "The best version of something cannot be a conversion of something else." | 2026-02-23 | 위 Car Design News | 원문 확인† | Franz von Holzhausen, Eric Earley (당사자) |

**찾지 못한 것.** Sandy Munro(Munro Live)의 분해나 논평, SAE·Autoline의 기술 기사, 전 Tesla 엔지니어의 평가. 검색을 못 했고 MotorTrend(09-04 첫인상, 09-08 시승)와 Car and Driver는 열리지 않았다. 사이버캡은 일반에 팔지 않으므로 독립 분해가 아직 없을 가능성이 높지만 확인한 것은 아니다. 위 평가자 대부분은 기자이고 차량 구조 전문가의 독립 평가는 이 문서에 없다.

---

## 6. 2026-09-03 이후 운행에서 나온 문제

| 사실 | 날짜 | 출처 | 확인 | 하드웨어·제품 문제인가 |
|---|---|---|---|---|
| 호텔 주차장에서 못 나감. 한 차로가 공사로 막혔는데 열린 차로를 못 보고 네 번 왕복한 뒤 출발지에서 "도착"을 선언했다. "it couldn't see the other open lane" | 2026-09-15 | https://futurism.com/advanced-transport/cybercab-trapped-hotel-lot | 원문 확인† (승객 X 글을 옮긴 기사) | 인식·경로 소프트웨어. 카메라 한계인지는 알 수 없다 |
| 10분 거리가 70분. 고속도로(MoPac, US-183)를 못 타고 평면 철도 건널목을 못 건너 우회했다. Tesla 문서의 운행 조건은 "freeways, highways"를 포함한다 | 2026-09-14 | https://electrek.co/2026/09/14/tesla-cybercab-70-minute-austin-detour/ , 위 Tesla PDF 11쪽 | 원문 확인† / 원문 확인(직접 읽음) | 소프트웨어·운영 제한. Model Y도 같다 |
| 대기 1시간 이상, 같은 구간 요금이 Model Y($12.04)보다 비쌌다($15.24). 출시 직후에는 반대로 35% 쌌다($7.77 대 $12.10) | 2026-09-04, 09-07 | https://www.teslaoracle.com/2026/09/07/high-demand-for-tesla-cybercab-makes-it-more-expensive-than-uber-and-the-model-y-robotaxi/ , 위 Not a Tesla App 4651 | 원문 확인† | 대수 부족. 제품 문제 아님 |
| 트렁크: 타기 전에 트렁크를 열었으면 도착 때 자동으로 다시 열린다. 기사는 분실 사례를 적지 않았다 | 2026-09-27 | https://teslanorth.com/2026/09/28/tesla-robotaxi-trunk-auto-opens-after-rides-to-stop-lost-bags/ | 원문 확인† | 예방 기능. 문제 보고는 아님 |
| 충전: 직원이 걸어다니며 케이블을 꽂는다 | 2026-10-02 | 위 teslanorth 10-04 | 원문 확인† | **제품 설계와 직접 관련** (무선 충전 미가동) |
| 밤: 운행은 23시까지. 24시간 운행은 10월 목표 | 2026-10-04 | https://www.notateslaapp.com/news/4768/tesla-extends-robotaxi-hours-in-austin-adds-111-cybercabs | 원문 확인† | 카메라 저조도 성능과 관련될 수 있으나 Tesla는 소프트웨어 문제로 설명한다 |
| CNBC가 첫 달을 "rocky"라고 평가. 긴 대기, 틀린 승하차 지점. Austin 소방 간부가 자율주행차 긴급대응 지침을 요구 | 2026-10-03 | https://teslanorth.com/2026/10/04/elon-musk-touts-careful-cybercab-rollout-austin-fleet-169/ (CNBC 원문은 403) | 원문 확인† (2차) | 운영 |
| NHTSA 감사(AQ26002): 운전대·페달·미러 없는 차의 FMVSS 자기인증 과정을 조사 | 2026-09-03~ | 기존 조사 `../cybercab-outlook/precedents.md` | 기존 조사 | 제품 설계와 직접 관련 |

**찾지 못한 것.** 문 고장, 문에 끼임, 창문 파손, 충전 포트 고장, 승차감 불만, 청소 상태 불만, 2인승이라 호출을 포기했다는 수요 자료. 보고가 없다는 뜻이 아니라 이번 경로로 닿지 못했다는 뜻이다. MotorTrend 시승기(09-08)가 승차감을 다뤘을 가능성이 높지만 열리지 않았다.

---

## 7. 작업자의 계산

입력은 모두 위 표의 숫자다.

| 계산 | 식 | 결과 |
|---|---|---|
| 효율을 mi/kWh로 | 1000 ÷ 165 | 6.06 mi/kWh |
| Model Y RWD 대비 전력 소비 | 165 ÷ 240 | 69%, 즉 31% 적다 |
| Model 3 Standard Range 대비 무게 | 3,113 − 3,862 lb | 749lb(340kg) 가볍다, 19% |
| Waymo Ojai 대비 배터리 | 47.6 ÷ 93 | 51% |
| 조정 주행거리 검산 | 418.2 × 0.7 | 292.7마일. 보도된 "약 293마일"과 맞는다. EPA 표준 보정 계수 0.7을 쓴 값으로 보이고 최종 라벨 수치인지는 확인하지 못했다 |
| 165Wh/mi로 달릴 때 배터리 전체 주행거리 | 47.6 ÷ 0.165 | 288마일 |
| 배터리 무게 | 47.6kWh ÷ 145~154Wh/kg | 309~328kg, 공차중량의 22~23% |
| 무선 25kW로 10→80% | 47.6 × 0.7 ÷ 25 | 약 1.3시간(충전 곡선 무시). 25kW는 2024년 시연 수치이고 양산 패드의 출력은 모른다 |
| 무선 효율 "90% 이상"의 손실 | 33.3kWh ÷ 0.9 − 33.3 | 10→80% 한 번에 최대 약 3.7kWh 손실 |
| 마일당 전기료(가정: kWh당 0.15달러) | 0.165 × 0.15, 0.240 × 0.15 | 사이버캡 2.5센트, Model Y 3.6센트. 차이 1.1센트. 전기 요금은 작업자의 가정이다 |
| 승객 적재 여유 | 617lb − 트렁크 220lb | 승객 2명에게 397lb(180kg). 트렁크를 가득 채웠을 때 |

마지막 줄은 서류상 수치의 뺄셈일 뿐이다. 실제 운행에서 무게 제한이 걸렸다는 보고는 찾지 못했다.

전기료 차이(마일당 약 1센트)는 Tesla가 말하는 운영비 목표(마일당 20~30센트)에 견주면 작다. 효율 165Wh/mi가 경제성에 주는 큰 효과는 전기료보다 **배터리를 절반 크기로 줄여 차 값과 무게를 낮춘 것**이다. 이것은 작업자의 해석이다.

---

## 질문에 대한 답

### (a) 실제로 인상적이고 근거가 탄탄한 기술 사실

1. **165Wh/mi 인증 효율.** EPA 인증 서류에 있고 Tesla 부사장이 확인했다. 같은 기준에서 Model 3·Y(240)보다 31%, Lucid Air Pure(230)보다 28% 적게 쓴다. 근거 수준은 높다(서류 자체는 2차로 봤다). 단서: 2인승이고 운전 장치가 없어 일반 승용차와 같은 조건의 비교가 아니다.
2. **47.6kWh 배터리로 조정 주행거리 약 293마일, 공차중량 1,412kg.** Model 3 기본형보다 340kg 가볍다. Waymo Ojai 배터리(93kWh)의 절반이다. 근거 수준 높음.
3. **유압 없는 브레이크.** 바퀴마다 전기 액추에이터가 있고 브레이크액, 배관, 마스터 실린더가 없다. 2026년 양산차에서 드물다. Tesla 발표와 The Drive가 독립적으로 전했다. 근거 수준 중간(구조는 확인, 이중화는 미공개).
4. **48V 저전압 구조와 전원 이중화.** Tesla 긴급대응 문서에 직접 적혀 있다. 저전압 배터리 선을 잘라도 "system redundancies" 때문에 꺼지지 않을 수 있다고 구조대에 경고한다. 근거 수준 높음(1차 문서를 직접 읽음). 무엇이 몇 개 겹쳐 있는지는 모른다.
5. **차 안에 충전기가 없는 DC 전용 설계.** 부품을 덜어 원가와 고장 요인을 줄인 선택이다. 근거 수준 중간(리뷰어 관찰과 Tesla 전문 매체).
6. **희토류를 쓰지 않는 163kW 전륜 모터, "18% smaller, 25% lighter".** Musk와 Tesla 발표다. 비교 대상이 불분명하고 자석 재료는 미확인이다. 근거 수준 낮음~중간.
7. **공기저항계수 0.20 미만.** Tesla 발표뿐이다. 독립 측정은 없다. 근거 수준 낮음.
8. **자동문과 무인 운영용 장치들.** 장애물 감지, 2단 기계식 비상 해제, 외부 마이크와 바닥 스피커, B필러 카메라로 신분 확인, 안전벨트를 풀면 정차. 1차 문서에 적혀 있다. 근거 수준 높음.

"부품 수가 Model 3의 절반"은 회사 발표만 있고 독립 확인이 없어 넣지 않았다.

### (b) 지금 투입을 제약하는 제품 선택

| 제품 선택 | 제약의 내용 | 근거의 강도 |
|---|---|---|
| 무선 충전을 전제로 설계했으나 가동되지 않는다 | 사람이 케이블을 꽂는다. AC 충전이 안 돼 Supercharger급 DC 기지가 있어야 한다. Austin 전용 기지의 무선 패드 80기는 허가 단계다 | **강함.** 설계(충전기 없음), 허가 서류, 현장 영상이 일치한다. 다만 169대 규모에서 이것이 병목이라는 증거는 없다. 수천 대부터의 문제다 |
| 새 차대 | Musk 본인이 사이버캡 전용 주행 데이터를 운전대 단 시험차로 쌓아야 한다고 했다 | **중간.** 발언은 분명하다. 얼마나 필요한지, 지금 얼마나 쌓였는지는 없다. "카메라 위치 때문"이라는 설명은 Tesla가 한 적이 없고 배치 차이도 확인하지 못했다 |
| 운전대·페달 없음 | NHTSA 감사를 받고 있다. 안전요원이 탈 수 없어(2인승에서 한 자리를 쓰면 승객은 1명) 새 도시를 Model Y로 먼저 열어야 한다. 차를 옮길 때는 원격 조작이나 화면 조이스틱에 의존한다 | **중간~강함.** 규제는 기존 조사에 있다. 안전요원 문제는 Not a Tesla App이 짚었다 |
| 카메라만 쓰는 센서 구성 | 밤 운행이 23시에 끝나고, 폭우·눈길은 운행 조건 밖이며, 주차장 공사 구간에서 열린 차로를 못 봤다 | **약함~중간.** 사건은 있지만 원인이 센서인지 소프트웨어인지 가를 자료가 없다. Tesla는 소프트웨어 문제로 설명한다 |
| AI4 계열 컴퓨터 | Tesla는 충분하다고 한다. HW3 때도 같은 말을 했다가 물러났다. AI5는 2027년 중반이고 차에 들어갈지 말이 엇갈린다 | **판단 불가.** 부족하다는 직접 증거는 없다. 전례만 있다 |
| 2인승 | 3명 이상은 Model Y가 받는다. 수요를 얼마나 놓치는지 자료가 없다. 출시 첫 달에는 오히려 대기가 1시간을 넘었다 | **약함.** 지금은 수요가 아니라 대수가 모자란다 |
| 원격 연결 의존 | 연결이 끊기면 차가 길가에 선다. 자율주행 모드가 한번 꺼지면 사람이 검토해 다시 켜야 한다 | **중간.** 1차 문서에 적힌 동작이다. 빈도 자료는 없다 |

종합하면 제품 하드웨어 가운데 **지금 169대라는 숫자를 직접 설명하는 것은 없다.** 가장 근거가 강한 제약인 충전은 규모가 커질 때의 문제이고, 새 차대의 데이터 축적은 소프트웨어 검증과 같은 방향의 제약이다. 앞선 조사의 결론(한계는 주행 소프트웨어의 신뢰도)을 뒤집을 하드웨어 증거는 찾지 못했다. 반대로 하드웨어가 준비됐다는 것도 독립적으로 검증된 것은 효율과 무게 정도이고, 안전에 중요한 이중화는 공개 자료가 없다.

### (c) 아직 모르는 것

- **조향·제동·연산의 이중화 구성.** 액추에이터 수, 독립 전원 수, 칩 2개가 서로 대신하는지. Tesla가 공개하지 않았고 NHTSA 감사 답변(09-30 기한)도 공개되지 않았다.
- **카메라의 정확한 수, 위치, 해상도, 세척 장치**, 그리고 Model Y와의 차이.
- **사이버캡 컴퓨터의 정체.** AI4, AI4+, 보드 2장 중 무엇인지. 소비전력.
- **AI5의 공정과 차량 탑재 여부.** TSMC와 Samsung이 함께 언급됐을 뿐이다.
- **실제 제조 원가.** 2만 5천~3만 달러는 2024년 목표의 반복이다.
- **무선 충전 양산품의 출력·효율·가동 시점.** 25kW와 "90% 이상"은 2024년 시연 수치다.
- **청소 방식과 인력.** 로봇 청소가 쓰이는지.
- **최고속도, 전장·전고·축거, 타이어 규격.**
- **원격 운영 인원과 개입 빈도, 통신 사양.**
- **문·창문·충전 포트의 현장 고장률, 승차감 평가, 2인승이 수요에 주는 영향.**
- **독립 분해 분석.** Munro 등의 평가가 있는지조차 확인하지 못했다.

### 검증하지 못한 것과 주의할 점

- 검색을 하지 못해 조사 범위가 알려진 URL과 그 연결에 한정됐다. 위 "찾지 못했다"는 모두 이 조건에서의 결과다.
- 직접 읽은 원문은 Tesla 긴급대응 문서 하나다. 나머지 인용문은 요약 도구를 거쳤으므로 자막에 쓰기 전에 원문과 대조해야 한다.
- 수치 불일치가 남아 있다: 화면 21·22·24인치, 배터리 비에너지 145·154Wh/kg, 전압 326V·255.2V.
- "카메라 9개"는 차 전체 수인지 불분명하다.
- Basenor(액세서리 판매업체 블로그), TeslaNorth, Tesla Oracle은 X 게시물을 옮긴 2차 자료다. 500,000마일 수명, 2만 5천 달러, Model Y 420대는 이 수준의 근거다.
- Zoox의 4인승·133kWh는 작업자의 기억(2020년 공개 제원)이고 이번에 원문을 열지 못했다. Waymo Ojai의 운전대 유무는 위키백과 요약이 스스로 엇갈렸다.
- 2분기 실적 발표 녹취록(Fool)은 오타가 많다("AI will initially go into Optimus"는 AI5를 가리키는 것으로 보이나 확정하지 못했다).
