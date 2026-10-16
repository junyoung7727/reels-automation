# Grok과 xAI는 사이버캡에서 무엇을 하고, 테슬라와 어떻게 묶여 있나

조사일: 2026-10-05. 작성: 조사 작업자(Claude).

질문: "Grok은 지금 테슬라 차와 사이버캡·로보택시 서비스에서 실제로 무엇을 하나. 운전 자체에 역할이 있나. 테슬라와 xAI는 돈과 기술로 어떻게 묶여 있고 누가 이득을 보나."

## 0. 읽기 전에

### 확인 방식 표기

| 표기 | 뜻 |
|---|---|
| 원문 확인(직접 읽음) | SEC EDGAR에서 원문 파일을 내려받아 해당 문단을 직접 읽었다 |
| 원문 확인†(요약 도구로 읽음) | 원문 페이지를 열었지만 요약 모델을 거쳐 읽었다. 인용문의 글자 단위 정확성은 보장되지 않는다 |
| 검색 요약만 | 검색 결과 요약에만 나왔고 원문을 열지 못했다 |
| 미확인(기억) | 2025년 이전 사건을 작업자 기억으로 적었다. 원문을 열지 못했다(주로 CNBC 403) |

### 이번 조사의 한계

- 세션의 웹 검색 한도(200회)가 조사 초반에 소진되어 검색은 4회만 성공했다. 이후에는 이미 아는 주소와 SEC EDGAR 전문 검색(공식 도구)만 썼다. 애널리스트 의견, 한국 출시 여부, 경쟁사 최신 상황은 그래서 얇다.
- `tesla.com`(Grok 지원 문서, 개인정보 고지, 사용 설명서)은 403으로 열리지 않았다. 웹 아카이브도 도구에서 막혀 있다. 테슬라 Grok 지원 문서의 내용은 2차 자료로만 확인했다.
- X 게시물 원문(@robotaxi, @Tesla, 머스크, 엘루스와미)은 직접 열지 못했다. 게시물을 인용한 매체로 확인했다.

### 이름 정리

xAI(X.AI Corp., 2023-03 설립) → 2025-03 X와 합쳐 X.AI Holdings → 2026-02-02 SpaceX의 100% 자회사 → 2026-07 "SpaceXAI"로 개명(개명은 Wikipedia† 기준). 테슬라 공시에서는 2026년 1분기부터 상대방이 "xAI"가 아니라 "SpaceX"로 적힌다. 아래에서는 시점에 맞는 이름을 쓴다.

---

## 1. 제품: Grok이 차 안에서 하는 일

### 1-1. 사실

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| Grok이 소프트웨어 2025.26으로 테슬라 차에 들어왔다. AMD Ryzen 프로세서 필요. "Requires Premium Connectivity or a Wi-Fi connection." | 2025-07-12 | https://www.notateslaapp.com/software-updates/version/2025.26/release-notes | 원문 확인†(요약 도구로 읽음) | 실제(배포됨) |
| 출시 당시 릴리스 노트: "Grok is currently in Beta and does not issue commands to your car - existing voice commands remain unchanged." | 2025-07-12 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 실제 |
| 릴리스 노트: "Conversations are anonymous to Tesla and not associated with your vehicle." 성격 선택지는 "Storyteller"부터 "Unhinged"까지 | 2025-07-12 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 발표(테슬라 설명) |
| 테슬라 3분기 자료: "deploying Grok (an AI companion) for vehicles in North America" | 2025-10-22 | https://www.sec.gov/Archives/edgar/data/1318605/000162828025045861/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 테슬라 4분기 자료: "Grok (an AI companion) which now supports navigation commands (allowing users to find, add and edit navigation destinations hands-free)" | 2026-01-28 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026003837/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 2026년 봄 업데이트(4월): "Customers can launch Grok by saying “Hey Grok,” and set location-based reminders." | 2026-04-22 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026026551/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 2026년 여름 릴리스(7월): "additional Grok functionality such as making phone calls, searching and playing music and adjusting climate controls" | 2026-07-22 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026049213/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 음성 처리는 차 안이 아니라 클라우드 서버에서 한다. 테슬라 개인정보 고지: "uses Grok, an intelligent AI-powered assistant built by SpaceXAI" | 2026-09-09 | https://autos.yahoo.com/ev-and-future-tech/articles/grok-tesla-robotaxis-fine-print-161200621.html (The Auto Wire, Eve Nowell) | 원문 확인†(요약 도구로 읽음). 테슬라 고지 원문은 못 열었다 | 실제(2차 자료가 고지를 인용) |
| 테슬라 CFO: "Even today, if you look at Tesla, Inc. vehicles, we are using Grok in there." | 2026-01-28 | https://www.fool.com/earnings/call-transcripts/2026/01/28/tesla-tsla-q4-2025-earnings-call-transcript/ | 원문 확인†(요약 도구로 읽음) | 실제 |

정리하면 차량용 Grok의 권한은 1년 사이에 이렇게 넓어졌다: 대화만(2025-07) → 내비게이션 목적지(2025년 4분기) → 호출어·알림(2026-04) → 전화·음악·공조(2026-07). 모두 운전석 주변 기능이다.

### 1-2. 사이버캡·로보택시 안의 Grok (2026-09 출시)

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 사이버캡 유료 운행이 오스틴에서 시작됐다(9-03 행사, 9-04 유료 탑승) | 2026-09-04 | https://en.wikipedia.org/wiki/Tesla_Cybercab | 원문 확인†(요약 도구로 읽음) | 실제 |
| 텍사스 로보택시 약 420대 중 사이버캡은 약 45대 | 2026-09 | https://en.wikipedia.org/wiki/Tesla_Robotaxi | 원문 확인†(요약 도구로 읽음). 1차 출처 미확인 | 실제(추정치) |
| 테슬라 로보택시 계정: "Talk to Grok to control your Cybercab". 시연 영상에는 공조, 유튜브, 음악, 목적지 수정(휴대폰 알림 경유)이 나온다 | 2026-09-06 | https://teslanorth.com/2026/09/06/tesla-cybercab-talk-to-grok/ (원 게시물 https://x.com/robotaxi/status/2096428461166588208) | 원문 확인†(요약 도구로 읽음). X 원문은 못 열었다 | 발표 |
| 현장 탑승기(이틀간 약 6회 탑승): Grok은 남은 거리·도착 시각을 정확히 답했고 목소리 선택이 됐다 | 2026-09-09 | https://www.roadtoautonomy.com/tesla-cybercab-launch-day-field-report/ (David Moss) | 원문 확인†(요약 도구로 읽음) | 실제(제3자 관찰) |
| 같은 탑승기: 목적지를 말로 바꾸지 못한다. "A voice request to reroute to a coffee shop produced a push notification to the phone rather than a reroute" | 2026-09-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 실제(제3자 관찰) |
| 같은 탑승기: 앱에서 목적지를 바꾸면 즉시 반영됐다. "the vehicle repriced to $15.02, updated the arrival time, and began a lane change within seconds" | 2026-09-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 실제(제3자 관찰) |
| 같은 탑승기: Grok은 탑승객 계정이 아니라 테슬라 계정으로 돈다. 탑승객의 기억·개인화가 없고, NSFW·이야기 모드가 빠졌으며, "Grok cannot start the ride, yet" | 2026-09-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 실제(제3자 관찰) |
| 비상 정차는 Grok이 아니라 점자가 새겨진 물리 버튼(emergency pullover button)으로 한다 | 2026-09-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 실제(제3자 관찰) |
| The Auto Wire: "Grok isn't rerouting the car. It's handing you off to the app that reroutes the car. The assistant controls the cabin. It does not control the driving stack." | 2026-09-09 | https://autos.yahoo.com/ev-and-future-tech/articles/grok-tesla-robotaxis-fine-print-161200621.html | 원문 확인†(요약 도구로 읽음) | 남의 해석(기자) |
| 개인정보: 테슬라(실내 카메라·마이크)와 SpaceXAI(대화)가 따로 수집한다. 조기 이용 지역 탑승객은 "additional collection by default, including exterior camera analytics, cabin camera analytics and sound detection data" | 2026-09-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음). 테슬라 고지 원문 미확인 | 실제(2차 자료) |

### 1-3. 옵티머스

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 머스크: 로봇이 많아지면 "an orchestra conductor"가 필요하고 Grok이 그 역할을 한다는 취지 | 2026-01-28 | https://www.fool.com/earnings/call-transcripts/2026/01/28/tesla-tsla-q4-2025-earnings-call-transcript/ | 원문 확인†(요약 도구로 읽음). 문장 전체는 확보하지 못했다 | 주장(전망) |
| 테슬라가 Grok을 옵티머스의 "the brains"(대화 부분)로 넣고 있다는 보도 | 2025-09 무렵 | https://www.notateslaapp.com/news/3106/tesla-shareholders-to-vote-on-proposal-for-investment-in-xai | 원문 확인†(요약 도구로 읽음) | 주장(매체 서술, 1차 근거 미확인) |

---

## 2. 운전: Grok이 운전 판단에 들어가나

### 2-1. 사실

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 테슬라가 FSD v14.3을 설명한 문단에 Grok·xAI가 없다. 강화학습 단계, 비전 인코더, AI 컴파일러·런타임만 언급한다 | 2026-04-22 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026026551/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 테슬라 2026년 2분기 10-Q 전문에서 "Grok"은 0회 나온다. "xAI"는 소송 문단과 투자 문단에만 나온다 | 2026-07-23 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026049270/tsla-20260630.htm | 원문 확인(직접 읽음) | 실제 |
| 엘루스와미: "Some elements of reasoning such as navigation route changes during construction, parking options have already shipped in 14.2." Grok 언급 없음 | 2026-01-09 | https://www.notateslaapp.com/news/3498/tesla-sets-10-billion-mile-goal-for-unsupervised-fsd-ashok-confirms-reasoning-is-here | 원문 확인†(요약 도구로 읽음) | 실제(FSD 자체 기능) |
| 머스크(2025년 3분기 실적 발표): "With reasoning, it's literally going to think about which parking spot to pick. It'll drop you off at the entrance of the store, then go find a parking spot." Grok 언급 없음 | 2025-10-22 | https://www.teslarati.com/tesla-ai-head-says-future-fsd-feature-already-partially-shipped/ | 원문 확인†(요약 도구로 읽음) | 주장(전망) |
| Grok으로 FSD에 말로 지시하는 기능("Take a left at the stop sign", 특정 진입로 지정)에 대해 엘루스와미: "Working on it." 머스크: "in about 3 months or so" | 2026-07-08 | https://teslahubs.com/blogs/tips/tesla-vp-confirms-grok-fsd-integration-is-coming-soon | 원문 확인†(요약 도구로 읽음). X 원문 미확인 | 주장(개발 중) |
| 테슬라: "FSD Supervised w/ Grok is a lot like having your own Robotaxi". 예시는 "Hey Grok, take me to the ATM", "Hey Grok, take me home". HW4는 FSD v14.3.7 | 2026-09-14 | https://teslanorth.com/2026/09/14/tesla-fsd-grok-own-robotaxi/ (원 게시물 https://x.com/Tesla/status/2099634149363728628) | 원문 확인†(요약 도구로 읽음) | 발표(목적지 전달 수준) |
| 머스크: "Grok will be, I think, very helpful in maximizing the efficiency of the management of a large autonomous fleet." | 2026-01-28 | https://www.fool.com/earnings/call-transcripts/2026/01/28/tesla-tsla-q4-2025-earnings-call-transcript/ | 원문 확인†(요약 도구로 읽음) | 주장(전망, 운전이 아니라 배차·관리) |
| 주주 제안서(제안자 Stephen Hawk)의 문구: Grok은 "already integrated into Tesla vehicles to enhance user experience, vehicle functionality, and autonomous driving capabilities". 이사회는 이 안건에 권고를 내지 않았다 | 2025-09-17 | https://www.sec.gov/Archives/edgar/data/1318605/000110465925090866/tm252289-12_def14a.htm | 원문 확인(직접 읽음) | 주장(주주 개인의 문구, 회사 확인 아님) |
| 테슬라 특별위원회의 표현은 조건부다: xAI의 능력이 "may potentially lead to further advancements in autonomous decision-making and real-world adaptability, which could benefit Tesla's vehicles and robotics offerings" | 2025-09-17 | 같은 곳(부록 A) | 원문 확인(직접 읽음) | 주장(가능성) |
| "머스크가 Grok 음성 명령을 2026-09까지 FSD 계획 계층에 통합한다고 확인했다", "엘루스와미가 Grok이 supervisor 역할로 간다고 확인했다" | 2026-03 무렵 | https://tahaabbasi.com/blog/taha-abbasi-grok-controlling-tesla-fsd-natural-language-ai-driving-march-2026 , https://letsdatascience.com/news/tesla-integrates-voice-intent-into-fsd-driving-decisions-c2b6055d | 검색 요약만(두 페이지 모두 열리지 않았다) | 주장(미검증) |

### 2-2. 구분

- **Grok이 목적지를 내비게이션에 넘긴다**: 고객 차에서는 확인된다(2025년 4분기부터). 그 뒤의 차선·속도·주차 판단은 FSD가 한다.
- **Grok이 운전 판단에 영향을 준다**: 확인되지 않는다. 개발 중이라는 발언(2026-07)만 있고, 테슬라 공시와 FSD 설명에는 없다.
- 사이버캡에서는 첫 단계인 목적지 전달조차 Grok이 직접 하지 않고 휴대폰 앱으로 넘긴다.

---

## 3. 회사와 돈: 2023–2026 시간표

| 날짜 | 사실 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 2023-03-09 | xAI 설립(네바다). 머스크는 2023-03부터 xAI CEO | https://www.sec.gov/Archives/edgar/data/1318605/000110465926053166/tm2611837d1_10ka.htm (머스크 약력), https://en.wikipedia.org/wiki/SpaceXAI | 원문 확인(직접 읽음) / 설립일은 원문 확인† | 실제 |
| 2023-12~2024-06 | 테슬라 몫 엔비디아 칩이 X·xAI로 돌려졌다(CNBC 2024-06-04 보도). 기억으로는 H100 12,000개, 5억 달러 이상이며 머스크는 테슬라에 칩을 켤 곳이 없었다고 답했다 | https://www.cnbc.com/2024/06/04/elon-musk-told-nvidia-to-ship-ai-chips-reserved-for-tesla-to-x-xai.html , https://en.wikipedia.org/wiki/SpaceXAI | 기간·사실은 원문 확인†(Wikipedia). 수량·금액은 미확인(기억, CNBC 403) | 실제(보도), 세부는 미검증 |
| 2024-01-15 | 머스크: 의결권 약 25% 없이는 AI·로봇을 테슬라 밖에서 만들겠다는 X 게시물. 테슬라 위임장도 "his repeated public statements that voting influence at Tesla is critically important to him if he is tasked with developing AI products for Tesla"라고 적는다 | https://www.sec.gov/Archives/edgar/data/1318605/000110465925090866/tm252289-12_def14a.htm | 위임장 문구는 원문 확인(직접 읽음). X 게시물 문구는 미확인(기억) | 실제 |
| 2024-05-24, 06-10, 06-13 | 테슬라 주주가 델라웨어 형평법원에 대표소송 3건을 냈다. 주제는 "Elon Musk and others, X Corp. (formerly Twitter) and xAI" | https://www.sec.gov/Archives/edgar/data/1318605/000162828026049270/tsla-20260630.htm | 원문 확인(직접 읽음) | 실제 |
| 2024년 | xAI가 테슬라에 낸 돈 약 1억 9,830만 달러, 그중 메가팩 1억 9,100만 달러 | https://www.sec.gov/Archives/edgar/data/1318605/000110465925090866/tm252289-12_def14a.htm | 원문 확인(직접 읽음) | 실제 |
| 2025-03-28 | xAI와 X가 X.AI Holdings 아래로 합쳐졌다(xAI 800억, X 330억 달러 평가) | 테슬라 10-K/A(위) / 평가액은 https://en.wikipedia.org/wiki/SpaceXAI | 합병은 원문 확인(직접 읽음), 평가액은 원문 확인† | 실제 |
| 2025-07-12 | Grok 차량 탑재(1장) | 1장 참조 | | 실제 |
| 2025-10-28 | 덴홀름 의장: "We haven’t invested in it" — xAI는 테슬라의 실세계 AI와 "a completely different kind of technology"를 만든다는 이유 | https://www.sec.gov/Archives/edgar/data/1318605/000110465925103255/tm252289d43_defa14a.htm (테슬라가 제출한 Bloomberg 기사) | 원문 확인(직접 읽음) | 실제(발언) |
| 2025-11-06 | 주주총회 안건 7(xAI 투자 승인, 권고적): 찬성 1,058,999,435 / 반대 916,321,296 / 기권 473,073,200 / 브로커 무투표 302,456,274. 회사 표현: "this was not approved under the bylaw standard", "the Board will examine next steps" | https://www.sec.gov/Archives/edgar/data/1318605/000110465925108507/tm2530590d1_8k.htm | 원문 확인(직접 읽음) | 실제 |
| 2026-01-16 | 테슬라가 xAI 시리즈 E 우선주 약 20억 달러 매입 계약. "on market terms consistent with those previously agreed to by other investors". 함께 맺은 것은 "a framework for evaluating potential AI collaborations" | https://www.sec.gov/Archives/edgar/data/1318605/000162828026003837/exhibit991.htm | 원문 확인(직접 읽음) | 실제 |
| 2026-01 | xAI 시리즈 E: 200억 달러 모집, 기업가치 약 2,300억 달러. xAI는 월 10억 달러를 쓴다는 보도 | https://electrek.co/2026/01/28/tesla-invests-2-billion-in-elon-musk-xai-cash-furnace/ | 원문 확인†(요약 도구로 읽음) | 실제(보도) |
| 2026-02-02 | SpaceX가 xAI Holdings를 인수(전액 주식, xAI 2,500억·SpaceX 1조 달러 평가) | 테슬라 10-K/A(인수 사실) / https://en.wikipedia.org/wiki/SpaceXAI (평가액) | 인수는 원문 확인(직접 읽음), 평가액은 원문 확인† | 실제 |
| 2026-03-12 | 테슬라가 20억 달러를 납입하고 SpaceX A종 보통주를 받았다(주식 분할 전 380만 주, 2026-05-01 기준 18,990,195주, 지분 1% 미만) | https://www.sec.gov/Archives/edgar/data/1181412/000162828026042639/spaceexplorationtechnologi.htm , 테슬라 10-Q(위) | 원문 확인(직접 읽음) | 실제 |
| 2026-03 | 테슬라·SpaceX가 반도체 공장 "Terafab" 협업 발표(인텔 참여 예정). SpaceX: "neither Tesla nor Intel are obligated to remain a part of the project" | SpaceX 424B4(위) | 원문 확인(직접 읽음) | 발표(확정 계약 없음) |
| 2026-04-13 | 델라웨어 법원이 xAI 관련 대표소송을 기각. 원고는 2026-05 델라웨어 대법원에 항소 | 테슬라 10-Q(위) | 원문 확인(직접 읽음) | 실제 |
| 2026-06-12 | SpaceX 상장 투자설명서(424B4). 공모가 주당 135달러 | SpaceX 424B4(위) | 원문 확인(직접 읽음) | 실제 |
| 2026-06-30 | 테슬라가 보유한 SpaceX 지분 공정가치 30억 700만 달러(시장성 결여 할인 2억 3,800만 달러 반영). 2분기 평가이익 10억 달러 | 테슬라 10-Q(위) | 원문 확인(직접 읽음) | 실제 |

### 3-1. 관계회사 거래 원문

테슬라 10-K/A(2026-04-30), 직접 읽음:

> "xAI is party to certain commercial, consulting and support agreements with Tesla. Under these agreements, Tesla incurred expenses of approximately $4.0 million in 2025 and $0.2 million through February 2026. Tesla also recognized revenue of approximately $430.1 million in 2025 and approximately $78.1 million through February 2026, primarily for the sale of our Megapack products."

테슬라 10-K(2026-01-29) 주석 15, 직접 읽음:

> "During the year ended December 31, 2025, we recognized $430 million of revenues and $285 million of cost of revenues from xAI for its purchase of our Megapack products in the ordinary course of business."

테슬라 10-Q(2026-07-23) 주석 13, 직접 읽음:

> "In the three and six months ended June 30, 2026, we recognized $318 million and $405 million of revenues, respectively, and $242 million and $307 million of cost of revenues, respectively, from SpaceX for its purchase of our Megapack products in the ordinary course of business."

SpaceX 424B4(2026-06-12), 직접 읽음:

> "Under these agreements, xAI obtained goods and services of $191 million in 2024, $506 million in 2025, and $303 million from January 1, 2026 through April 30, 2026 ($269 million of which relates to purchases of Megapacks in April 2026), and xAI recognized revenue of $2 million in 2025 and $1 million from January 1, 2026 through April 30, 2026 from Tesla."

> "Certain of these projects, including Macrohard and Terafab, are in the very early stages, as a result of which we and Tesla have not finalized a variety of details relating to our collaboration, including, but not limited to, financial terms, intellectual property rights, and the ultimate term of our collaboration."

### 3-2. 돈의 흐름 정리

| 방향 | 항목 | 금액 | 기간 | 출처 |
|---|---|---|---|---|
| xAI → 테슬라 | 메가팩 구매 | 1억 9,100만 달러 | 2024 | 테슬라 위임장 |
| xAI → 테슬라 | 메가팩 매출(테슬라 인식 기준) | 4억 3,010만 달러(원가 2억 8,500만 달러) | 2025 | 테슬라 10-K, 10-K/A |
| SpaceX(xAI 포함) → 테슬라 | 메가팩 매출 | 4억 500만 달러(원가 3억 700만 달러) | 2026 상반기 | 테슬라 10-Q |
| SpaceX → 테슬라 | 차량 구매(주로 사이버트럭) | 1억 4,330만 달러(SpaceX 기재는 정가 1억 3,100만 달러) | 2025 | 테슬라 10-K/A, SpaceX 424B4 |
| 테슬라 → xAI | 상업·컨설팅·지원 계약 비용 | 400만 달러(xAI가 인식한 매출은 200만 달러) | 2025 | 테슬라 10-K/A, SpaceX 424B4 |
| 테슬라 → xAI | 같은 항목 | 20만 달러(1~2월), xAI 매출 기준 100만 달러(1~4월) | 2026 | 같은 곳 |
| 테슬라 → SpaceX | 상업·라이선스·지원 계약 비용 | 1,140만 달러 | 2025 | 테슬라 10-K/A |
| 테슬라 → X | 광고 | 330만 달러 | 2025 | 테슬라 10-K/A |
| 테슬라 → xAI(→SpaceX) | 지분 투자 | 20억 달러 | 2026-03-12 | 테슬라 10-Q, SpaceX 424B4 |

주의: 같은 2025년 메가팩 거래를 테슬라는 매출 4억 3,010만 달러로, SpaceX는 구매 5억 600만 달러로 적는다. 테슬라의 2026년 1분기 SpaceX향 메가팩 매출은 8,700만 달러인데 SpaceX는 1분기 구매를 3,400만 달러로 적는다. 인식 시점 차이로 보이지만 어느 공시도 차이를 설명하지 않는다.

### 3-3. Macrohard, 칩, Terafab

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| SpaceX: "Together with Tesla, we are also developing Macrohard, an agentic AI platform". Macrohard는 "cost efficient, next-generation Tesla processors"에서도 돌 것으로 기대 | 2026-06-12 | SpaceX 424B4 | 원문 확인(직접 읽음) | 발표(초기 단계) |
| 테슬라 쪽 이름은 "Digital Optimus": "We are working on automating digital workloads, building an intelligence layer". 테슬라 자료에는 "Macrohard"라는 단어가 없다(EDGAR 전문 검색 0건) | 2026-04-22 | 테슬라 1분기 자료 | 원문 확인(직접 읽음) | 발표 |
| Terafab이 만들 칩 두 종류: 하나는 "to be used primarily in Tesla’s Optimus robots and vehicles", 하나는 SpaceX 궤도 컴퓨팅용 | 2026-06-12 | SpaceX 424B4 | 원문 확인(직접 읽음) | 발표 |
| 테슬라: "Our partnership with SpaceX aims to build the largest chip fab ever". 시작은 기가 텍사스의 "Tesla-owned Research Fab" | 2026-04-22 | 테슬라 1분기 자료 | 원문 확인(직접 읽음) | 발표 |
| 테슬라 2분기 자료는 오스틴 반도체 공장을 "still in its early stages"라고 적는다. 2026년 설비투자 전망은 250억 달러 초과 | 2026-07-22~23 | 테슬라 2분기 자료, 10-Q | 원문 확인(직접 읽음) | 실제(초기) |
| AI5·AI6 칩 생산 계획은 각각 2027년, 2028년. AI5 설계 완료는 2026-04 | 2026-01-28, 04-22 | 테슬라 4분기·1분기 자료 | 원문 확인(직접 읽음) | 발표 |
| 머스크: "I think Tesla, Inc. needs to build a TerraFab... a very big fab that includes logic, memory, and packaging." | 2026-01-28 | Motley Fool 녹취 | 원문 확인†(요약 도구로 읽음) | 주장 |

---

## 4. 지배구조와 소송

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 대표소송 3건(2024-05~06 제기)은 2026-04-13 기각, 2026-05 항소. 테슬라 공시는 사건명을 적지 않는다. "Cleveland Bakers and Teamsters Pension Fund v. Musk"가 그중 하나라는 점은 원문으로 확인하지 못했다 | 2026-07-23 | 테슬라 10-Q | 원문 확인(직접 읽음), 사건명은 미확인 | 실제 |
| 소송의 주장: 머스크가 "AI resources, talent, and opportunities"를 테슬라에서 xAI로 돌렸고, xAI 지분을 테슬라로 넘기라는 청구 | 2026-01-28 | https://electrek.co/2026/01/28/tesla-invests-2-billion-in-elon-musk-xai-cash-furnace/ | 원문 확인†(요약 도구로 읽음). 소장 미확인 | 주장(원고) |
| 기관투자자 서한(AFT, 네바다 주 재무관 등): "Mr. Musk’s reported uses of Tesla resources, including both engineering employees detailed to Twitter and the reallocation of chips intended for Tesla to xAI" | 2025-10-02 | https://www.sec.gov/Archives/edgar/data/1318605/000121465925014509/j102251px14a6g.htm | 원문 확인(직접 읽음) | 남의 해석(반대 주주) |
| 같은 서한: 보상안은 "no formal commitment to focus his time, attention, and Tesla’s own resources on Tesla" | 2025-10-02 | 같은 곳 | 원문 확인(직접 읽음) | 남의 해석 |
| CNBC 진행자 발언: ISS·Glass Lewis가 xAI 지분 투자를 두고 "this shouldn’t happen, that this would be a conflict"라고 본다. 두 자문사의 보고서 원문은 확인하지 못했다 | 2025-10-27 | https://www.sec.gov/Archives/edgar/data/1318605/000110465925102658/tm252289d42_defa14a.htm | 원문 확인(직접 읽음, 테슬라가 제출한 방송 녹취) | 남의 해석(전언) |
| 덴홀름: 주주가 찬성하면 "in the same way that we do other related-party-type transactions"로 감사위원회가 본다 | 2025-10-27 | 같은 곳 | 원문 확인(직접 읽음) | 발표 |
| 2025 CEO 보상안 위임장에서 특별위원회는 xAI를 유출 위험으로 적는다: "Mr. Musk’s other ventures, including SpaceX, xAI, Neuralink Corporation and TBC, which may start to seem more attractive" | 2025-09-17 | 테슬라 위임장 | 원문 확인(직접 읽음) | 실제(이사회 서술) |
| 같은 위임장 부록: 다른 회사들은 "may not fit squarely within Tesla’s mission and, therefore, should not be built using Tesla’s resources" | 2025-09-17 | 같은 곳 | 원문 확인(직접 읽음) | 주장(이사회 입장) |
| 테슬라 10-K 위험 요인: 머스크는 "does not devote his full time and attention to Tesla" | 2026-01-29 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026003952/tsla-20251231.htm | 원문 확인(직접 읽음) | 실제 |
| 이사 아이라 에런프라이스는 테슬라와 SpaceX 이사를 겸한다 | 2026-06-12 | SpaceX 424B4 | 원문 확인(직접 읽음) | 실제 |
| 보상안(안건 4)은 찬성 1,892,235,822 / 반대 564,940,908로 통과 | 2025-11-06 | 테슬라 8-K | 원문 확인(직접 읽음) | 실제 |

---

## 5. 경쟁사 대비

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| Waymo Foundation Model은 "Think Fast and Think Slow" 두 갈래다. 느린 쪽인 Driving VLM은 "Trained using Gemini, it leverages Gemini’s extensive world knowledge" | 2025-12-09 | https://waymo.com/blog/2025/12/demonstrably-safe-ai-for-autonomous-driving | 원문 확인†(요약 도구로 읽음) | 발표(Waymo 설명) |
| 큰 Teacher 모델은 차에 그대로 싣지 않고 작은 Student 모델로 증류해 싣는다. 별도의 차내 검증 계층이 있다 | 2025-12-09 | 같은 곳 | 원문 확인†(요약 도구로 읽음) | 발표 |
| EMMA는 "powered by Gemini"인 종단간 주행 모델이며 연구 논문이다. 한계로 라이다·레이더 미사용, 긴 영상 처리 불가를 직접 적었다 | 2024-10-30 | https://waymo.com/blog/2024/10/introducing-emma/ | 원문 확인†(요약 도구로 읽음) | 실제(연구) |
| Waymo가 Gemini 기반 차내 도우미를 시험했고 공조·조명·음악은 다루지만 경로 변경과 운전 평가는 못 하게 막았다는 보도(TechCrunch, 2025-12) | 2025-12 | 주소 확인 실패(404) | 미확인(기억) | 보도, 미검증 |
| Amazon/Zoox, Baidu Apollo Go의 차내 LLM | | | 조사하지 못했다 | |

---

## 6. 애널리스트

| 사실 | 날짜 | 출처 | 확인 | 구분 |
|---|---|---|---|---|
| 실적 발표에서 xAI 투자와 협업 방식을 물은 사람은 Morgan Stanley 애널리스트(Andrew)다. 의견이 아니라 질문이다 | 2026-01-28 | Motley Fool 녹취 | 원문 확인†(요약 도구로 읽음) | 실제 |
| Electrek(Fred Lambert)은 투자를 "cash furnace"에 넣는 순환 거래로 평가: 주주가 xAI로의 자원 유출을 문제 삼아 소송 중인데 테슬라가 그 회사에 20억 달러를 넣었다 | 2026-01-28 | https://electrek.co/2026/01/28/tesla-invests-2-billion-in-elon-musk-xai-cash-furnace/ | 원문 확인†(요약 도구로 읽음) | 남의 해석(매체) |
| Motley Fool: 찬성 논리는 수직 통합과 모델 접근, 반대 논리는 머스크가 양쪽을 지배해 테슬라가 유리한 대우를 받는지 검증할 수 없다는 점 | 2026-03-20 | https://www.fool.com/investing/2026/03/20/is-xai-good-news-for-tesla-investors/ | 원문 확인†(요약 도구로 읽음) | 남의 해석(매체) |
| 월터 아이작슨: 테슬라와 xAI가 "merge eventually"할 것으로 본다 | 2025-09 무렵 | https://www.notateslaapp.com/news/3106/tesla-shareholders-to-vote-on-proposal-for-investment-in-xai | 원문 확인†(요약 도구로 읽음) | 남의 해석(전기 작가) |
| Wedbush(Dan Ives), Morgan Stanley의 "embodied AI" 논지에서 Grok·xAI에 붙인 가치 | | | 찾지 못했다(검색 한도 소진) | |

---

## 7. 작업자의 판단

아래는 사실이 아니라 위 자료를 읽고 내린 판단이다.

1. **Grok은 사이버캡의 병목과 무관하다.** 사이버캡을 묶는 것은 주행 소프트웨어의 신뢰도인데, Grok이 그 소프트웨어의 일부라는 근거를 테슬라 공시·자료·발언 어디에서도 찾지 못했다. 사이버캡에서 Grok은 공조·미디어·질문 응답을 맡는 차내 도우미다.
2. **테슬라의 홍보 문구는 실제 권한보다 넓게 읽힌다.** "Talk to Grok to control your Cybercab"의 control은 실내 기능이고, "FSD Supervised w/ Grok"은 목적지를 말로 넣는 것이다. 주주 제안서의 "autonomous driving capabilities"는 주주 개인의 문구이며 회사가 확인하지 않았다.
3. **Grok 사용료는 사실상 없다.** xAI가 테슬라에서 올린 매출은 2025년 200만 달러다. 테슬라 차 수백만 대에 들어간 도우미의 대가로 보기에는 작다. 테슬라가 싸게 쓰고 있다는 뜻일 수도, xAI가 사용자 접점과 음성 데이터를 대가로 받는다는 뜻일 수도 있다. 계약 조건은 공개되지 않았다.
4. **현금 기준으로는 테슬라에서 머스크의 다른 회사로 나간 돈이 더 많다.** 2024년부터 2026년 상반기까지 테슬라가 받은 메가팩 매출은 약 10억 2,600만 달러(1억 9,100만 + 4억 3,010만 + 4억 500만), 차량 1억 4,330만 달러다. 나간 돈은 지분 20억 달러와 소액 비용 약 2,000만 달러다. 다만 성격이 다르다. 받은 돈은 원가가 있는 제품 매출이고(2025년~2026년 상반기 메가팩 매출총이익 약 2억 4,300만 달러), 나간 20억 달러는 2026-06-30 기준 30억 달러로 평가되는 지분으로 남아 있다.
5. **2026년 2분기 테슬라 순이익의 대부분은 이 지분의 평가이익이다.** GAAP 순이익 11억 1,400만 달러 중 SpaceX 지분 평가이익이 세후 7억 6,300만 달러로 약 68%다(테슬라 2분기 자료의 비GAAP 조정표, 직접 읽음. 비율은 작업자 계산).
6. **"LLM 회사와 묶인 로보택시 회사"는 드물지 않다. 묶인 방식이 다르다.** Waymo와 Google은 같은 모회사 안에 있고 Gemini가 주행 모델의 학습에 쓰인다고 Waymo가 직접 설명한다. 테슬라와 xAI는 지배주주만 같은 별개 회사이고, 운전 쪽 기술 연결은 공개된 것이 없으며, 거래는 관계회사 거래로 감사위원회 심사를 받는다.
7. **Terafab과 Macrohard가 Grok보다 큰 연결 고리가 될 수 있지만 아직 계약이 아니다.** SpaceX 스스로 금전 조건, 지식재산권, 기간을 정하지 않았다고 적었다.

---

## 8. 질문에 대한 답

### (가) 지금 사이버캡 탑승객에게 Grok이 실제로 하는 일

공조, 음악, 유튜브를 말로 조작하고, 남은 거리와 도착 시각 같은 질문에 답한다. 목소리를 고를 수 있다. 목적지를 바꿔 달라고 하면 차를 돌리지 않고 탑승객 휴대폰에 알림을 보내 앱에서 바꾸게 한다. 탑승을 시작시키지 못하고, 탑승객 개인 계정과 연결되지 않으며, 비상 정차는 물리 버튼이다. 근거는 테슬라 계정의 시연(2026-09-06)과 제3자 탑승기 한 편(2026-09-09)이다. 처리 장소는 클라우드이고 대화는 SpaceXAI가 따로 수집한다.

### (나) 운전에 검증된 역할이 있나

없다. 테슬라의 10-Q, 분기 자료의 FSD 설명, 엘루스와미의 "reasoning" 발언 어디에도 Grok이 없다. 고객 차에서 Grok은 목적지를 내비게이션에 넘기고, 운전은 FSD가 한다. 말로 주행을 지시하는 기능은 2026-07에 "Working on it."이라는 답이 전부이고 출시를 확인하지 못했다. 머스크가 말한 Grok의 역할은 운전이 아니라 대규모 차량·로봇의 관리("management of a large autonomous fleet")이며 전망이다.

### (다) 돈과 자원의 흐름

- xAI·SpaceX → 테슬라: 메가팩 2024년 1억 9,100만, 2025년 4억 3,010만, 2026년 상반기 4억 500만 달러. 차량 2025년 1억 4,330만 달러.
- 테슬라 → xAI·SpaceX·X: 지분 20억 달러(2026-03-12), xAI 계약 비용 2025년 400만 달러, SpaceX 계약 비용 1,140만 달러, X 광고 330만 달러.
- Grok 사용료: xAI가 테슬라에서 인식한 매출은 2025년 200만 달러뿐이다.
- 순방향: 2024년~2026년 상반기 합계로 현금은 테슬라에서 약 8억 5,000만 달러 더 나갔다(나간 돈 약 20억 2,000만, 들어온 매출 약 11억 7,000만 달러. 작업자 계산). 대신 테슬라는 2026-06-30 기준 30억 달러로 평가되는 SpaceX 지분(1% 미만)을 가졌고 평가이익 10억 달러를 잡았다.
- 금액으로 잡히지 않는 것: 2023-12~2024-06의 엔비디아 칩 전용, xAI로 옮긴 엔지니어, 머스크의 시간. 소송은 이를 다투었으나 2026-04-13 기각됐고 항소 중이다.
- 누가 이득인가: 테슬라 에너지 사업은 큰 고객을 얻었고 지분 평가이익을 얻었다. xAI는 전력 설비, 20억 달러, 차량이라는 배포 경로를 얻었다. 운전 기술 면에서 테슬라가 xAI에서 얻은 것은 확인되지 않는다.

### (라) 놀라운 사실 다섯 가지

1. xAI 투자 안건은 찬성(10억 5,900만)이 반대(9억 1,600만)보다 많았지만 기권 4억 7,300만이 반대로 계산되어 부결됐다. 이사회는 두 달 열흘 뒤 20억 달러 투자 계약을 맺었다(8-K, 분기 자료).
2. 의장은 2025-10-28에 xAI가 "a completely different kind of technology"를 만들기 때문에 투자하지 않았다고 말했다. 석 달 뒤 테슬라는 투자했다(테슬라 제출 DEFA14A).
3. 테슬라는 xAI 우선주를 사기로 했는데 납입 전에 SpaceX가 xAI를 인수해, 실제로 받은 것은 SpaceX 보통주다. 석 달 반 뒤 장부가는 30억 달러가 됐고 2026년 2분기 GAAP 순이익의 약 68%가 이 평가이익이다(10-Q, 2분기 자료).
4. 테슬라 차 전체에 깔린 Grok에 대해 xAI가 테슬라에서 올린 매출은 2025년 200만 달러다. 같은 해 xAI는 테슬라 메가팩을 4억 3,000만~5억 600만 달러어치 샀다(SpaceX 424B4, 테슬라 10-K/A).
5. 사이버캡의 Grok은 목적지를 직접 바꾸지 못하고 휴대폰 앱으로 넘긴다. 테슬라의 문구는 "Talk to Grok to control your Cybercab"이다(Road to Autonomy 탑승기, teslanorth).

### (마) 확인하지 못한 것

- 한국에서 차량용 Grok이 제공되는지, 한국어를 지원하는지.
- X Premium·SuperGrok 구독이 필요한지. 릴리스 노트는 Premium Connectivity 또는 Wi-Fi만 요구한다.
- Grok 이용량 수치. 찾지 못했다.
- 테슬라 Grok 지원 문서, 개인정보 고지, 사이버캡 설명서의 원문(tesla.com 403).
- X 게시물 원문 전부.
- Grok–FSD 음성 지시 기능이 2026-10-05 현재 출시됐는지. 2026-09-14 게시물은 목적지 지정 수준으로 보인다.
- 테슬라와 xAI의 Grok 라이선스 조건, 2026-01 프레임워크 계약 전문.
- 엔비디아 칩 전용의 수량과 금액(CNBC 원문 403), xAI로 옮긴 테슬라 엔지니어 수.
- "Cleveland Bakers v. Musk"라는 사건명과 기각 결정문.
- ISS·Glass Lewis 보고서 원문.
- Wedbush·Morgan Stanley가 Grok·xAI에 붙인 가치.
- Waymo 차내 Gemini 도우미의 현재 상태, Zoox·Baidu의 사례.
- 2026년 2분기 실적 발표 녹취(주소 404). 3분기 실적은 아직 발표 전이다.
- 테슬라가 2026년 2분기에 주식 19억 5,000만 달러로 인수한 "AI hardware company"가 어디인지, 머스크 계열과 관계가 있는지(10-Q는 이름을 밝히지 않는다).
- xAI가 테슬라 AI5·AI6 칩을 실제로 쓰는지. SpaceX는 Macrohard가 테슬라 프로세서에서 돌 것으로 "기대"한다고만 적었다.

### 고쳐 읽을 것

- Drive Tesla Canada는 주주 안건이 "최대 50억 달러" 승인이었다고 적었지만, 위임장의 안건 문구는 금액을 정하지 않았다("in an amount and form deemed appropriate by the Board").
- 검색 요약에 나온 "Grok이 FSD 계획 계층에 통합된다고 머스크가 확인"은 원문을 열지 못했다. 사실로 쓰지 않는다.
