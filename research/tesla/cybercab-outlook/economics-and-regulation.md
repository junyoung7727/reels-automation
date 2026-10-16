# 사이버캡 사업 전망: 차 한 대의 값, 규제의 무게, 주가에 들어 있는 몫

- 조사일: 2026-10-05
- 질문 A: 운행 중인 로보택시 한 대는 1년에 얼마를 버는가. 그 값으로 시장의 매출 기대를 차량 대수로 바꾸면 몇 대인가.
- 질문 B: 규제 완화는 사이버캡에 얼마나, 언제 중요한가.
- 질문 C: 지금 Tesla 시가총액 중 얼마가 로보택시 성공을 전제로 하고, 그 값을 정당화하려면 어떤 차량 대수와 이익이 필요한가.
- 이 문서는 조사 기록이다. 대본이 아니다. 같은 폴더의 `scaling.md`, `stakeholders.md`, `precedents.md`와 `../cybercab-investment-thesis.md`에 이미 있는 내용은 되풀이하지 않고 가리키기만 했다.

## 읽는 법

| 표시 | 뜻 |
|---|---|
| 원문 확인(직접 읽음) | 원문 파일을 내려받아 본문 텍스트를 직접 검색하고 읽었다(SEC 공시, 하원 위원회 문서, 법안 XML, Alphabet 실적 발표 녹취 PDF). |
| 원문 확인†(요약 도구로 읽음) | 적힌 URL을 열었지만 페이지를 요약해 주는 도구를 거쳤다. 숫자를 대본에 쓰기 전에 사람이 해당 문장을 한 번 더 봐야 한다. |
| 검색 요약만 | 검색 결과 요약에만 나온 내용이다. 페이지가 열리지 않았거나(403, 연결 끊김) 열지 않았다. 확인된 사실로 쓰면 안 된다. |
| 계산 | 위 숫자로 작업자가 계산한 값이다. 출처가 말한 숫자가 아니다. |
| 선행 조사 | 같은 폴더의 기존 문서에서 이미 확인 수준과 함께 기록한 값이다. 이번에 다시 열지 않았다. |

사실, 남의 해석, 작업자의 계산은 절마다 따로 묶었다.

---

# 질문 A. 로보택시 한 대는 1년에 얼마를 버는가

## A-1. Waymo 실적 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 주간 유료 탑승 "~500,000 paid public rides per week, ~4 million autonomous miles per week", 차량 "~4,000 vehicles (September 2026, Waymo-reported)", 미국 15개 대도시권 | 2026-09-24 기준 집계 | https://thechargeport.com/robotaxi-tracker | 원문 확인†(2차 집계 사이트) |
| 주간 유료 탑승 50만 건 이상(2026-03-26), 차량 약 3,000대(2026-03), 3,871대(2026-06-17 리콜 신고서) | 2026-03 ~ 06 | `scaling.md` 1-2, 1-3 | 선행 조사 |
| 2026년 2분기에도 주간 탑승은 약 50만 건으로 제자리였다. 가동 차량 약 3,600대, "about 20 trips per vehicle per day", 이론상 상한 "around 40 trips per day". 차량 추가 속도 월 265~300대 | 2026-08 무렵 | https://futuresearch.ai/waymo-financial-forecast/ | 원문 확인†(2차, 예측 업체의 추정) |
| 2025년 연간 탑승 1,500만 건, 2024년 450만 건. 2025년 말 하루 57,100건, 차량 "roughly 2,500 Jaguar I-PACEs", 대당 "about twenty-five trips per day", 하루 약 16시간 운행 | 2026-02-12 | https://om.co/2026/02/12/is-waymo-worth-126-billion/ | 원문 확인†(2차, 칼럼) |
| 평균 요금: San Francisco $19.69(Obi, 2025-11-27~2026-01-01, 약 94,000건), Uber $17.47 | 2026-01-27 | `scaling.md` 6장(TechCrunch) | 선행 조사 |
| 평균 요금 "roughly eighteen dollars per trip" | 2026-02-12 | 위 om.co | 원문 확인†(2차) |
| 연환산 매출: 2025년 "$350 million"(Bloomberg 인용) | 2026-02-12 | 위 om.co | 원문 확인†(Bloomberg 원문은 열지 않음) |
| 연환산 매출 추정: 2024년 말 $125M → 2025년 말 약 $284M → 2026년 2월 $355M | 2026-02 | https://sacra.com/research/waymo-at-355m-year/ | 검색 요약만(연결 끊김) |
| Alphabet 공시: "In Other Bets, revenues were $382 million, and operating loss was $1.8 billion as we continue to expand Waymo's business and invest in key Other Bets." Waymo 단독 매출·탑승 건수는 이 발표에 없다 | 2026-07-22 (2분기) | https://s206.q4cdn.com/479360582/files/doc_events/2026/Jul/22/2026_Q2_Earnings_Transcript.pdf | 원문 확인(직접 읽음) |
| 캘리포니아 2026년 2분기: 총 주행 약 2,814만 마일 중 승객 탑승 약 1,658만 마일(58.9%), 탑승 1건당 약 3.93마일 | 2026 2분기 | `../cybercab-investment-thesis.md`(CPUC 원본 ZIP 합산) | 선행 조사 |
| 차량 원가: I-PACE "$75,000 for the car and $100,000 for the sensor stack and compute hardware"(Dolgov 발언이라고 인용), 차세대(Zeekr) "maybe $75,000 total" | 2026-02-12 | 위 om.co | 원문 확인†(2차. 원 발언은 열지 않음) |
| 차량 원가 다른 추정: I-PACE 장착 후 "$150,000 to $200,000", Ojai 기본 차량 "around $32,000", 센서 42% 감소. 2026년 8월 대기 중인 Ojai 약 950대 | 2026-08 무렵 | 위 futuresearch | 원문 확인†(2차 추정) |
| Ojai(6세대)를 일반 승객에게 열었다: "Waymo introduced its newest vehicle, Ojai, to public riders." | 2026-07-22 | 위 Alphabet 녹취 | 원문 확인(직접 읽음) |
| 도시별 수익성: JMP 보고서를 인용한 X 게시물 "Waymo has 63% cash contribution margins ... accounting for their depreciation, contribution margins are just slightly positive", 가동률 35% | 2024-08 | https://x.com/aleximm/status/1828938865517965809 | 검색 요약만(2024년 자료, 2차 인용) |

찾지 못한 것:
- Waymo 단독 매출·손익의 공식 숫자. Alphabet은 Other Bets 합계만 낸다.
- 2026년 기준으로 "어느 도시가 차량 단위 영업흑자"라고 Waymo나 증권사가 밝힌 자료. 2024년 JMP 추정(샌프란시스코, 감가 전 63%, 감가 후 소폭 흑자)이 유일하고 검색 요약만이다.
- 차고지·운영비 추정의 2026년 수치. Morgan Stanley의 마일당 총비용 $1.43(Waymo)만 있다(`scaling.md` 5장).
- YipitData, Bernstein, The Information의 Waymo 매출 추정 원문.

## A-2. Tesla 로보택시 실적 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 요금: 출시 때 정액 $4.20(2025-06-22), 이후 정액 $6.90, 2025-07부터 거리 기반 | 2025 | https://www.notateslaapp.com/news/3757/tesla-increases-robotaxi-base-fare-drastically-increasing-short | 원문 확인† |
| 요금 변경: 기본 $1.00 + 마일당 $1.00 → 기본 $3.25 + 마일당 $1.00 (Austin). 2마일 $3.00 → $5.25, 5마일 $6.00 → $8.25 | 2026-03-07 무렵 | 위와 같음 | 원문 확인† |
| Austin "$3.00 base + $1.40 per mile" | 2026-03-12 | https://robotaxiprice.com/tesla-robotaxi-price/ | 원문 확인†(2차 집계). 불일치: 위 행의 "$3.25 + $1.00"과 며칠 차이로 다르다. 어느 쪽이 그 뒤 요금인지 확인하지 못했다 |
| Bay Area 하루 평균 요금 $8.31~$14.59(Obi), 출시 뒤 41% 상승 | 2026-03-01 ~ 04-14 | 위 robotaxiprice, https://www.automotiveworld.com/news/obi-tesla-robotaxi-prices-up-41-in-san-francisco/ | 원문 확인†(집계), 41%는 검색 요약만 |
| Dallas 같은 2.25마일: Tesla $6.15, Waymo $13.93 (한 건의 사례) | 2026-04 | 위 robotaxiprice | 원문 확인†(2차) |
| 사이버캡 요금: 같은 경로에서 사이버캡 $7.77, Model Y 로보택시 $12.10 (약 35% 저렴). Tesla가 공표한 사이버캡 요금표는 없다 | 2026-09-05 | 위 robotaxiprice (Not a Tesla App 인용) | 원문 확인†(2차. 한 건의 사례) |
| 누적 유료 주행: 2026년 1분기 말 약 180만 마일, 2분기 말 약 250만 마일 (도표 판독) | 2026-03-31, 06-30 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026049213/exhibit991.htm | 원문 확인†(1차. 이번에도 "2.5 million miles (from chart)"로 읽힘) |
| 무감독 주행 "more than 380,000 miles driven across six cities with zero notable safety incidents" | 2026-07-22 (2분기 발표) | https://www.fool.com/earnings/call-transcripts/2026/08/05/tesla-tsla-q2-2026-earnings-call-transcript/ | 원문 확인† |
| 차량 수: Texas 인가 42대(2026-05-28), 57대(06-30), 두 지역 합계 약 200대(2026-02), Texas 등록 589대(2026-10-02, Model Y 420 + 사이버캡 169) | 각 날짜 | `scaling.md` 4장, `stakeholders.md` 5-1 | 선행 조사 |
| Bay Area: CPUC 자료 기준 "Tesla has registered 1,655 vehicles and 798 drivers for its Bay Area service" (2025-08에는 28대·128명) | 2025-12-21 | https://www.webpronews.com/tesla-expands-robotaxi-fleet-to-1655-vehicles-in-bay-area-push/ | 원문 확인†(2차) |
| Tesla가 공시한 로보택시 매출: 없다. 2025년 10-K는 "Our Robotaxi business currently operates with Model Y vehicles but, in time, will include Cybercab"라고만 적는다 | 2026-01 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026003952/tsla-20251231.htm | 원문 확인(직접 읽음) |
| 비용 목표: 마일당 $0.30 미만(Tesla, 2024-10). 제3자 추정: Morgan Stanley Tesla $0.81, Waymo $1.43, 사람 운전 $1.71. Goldman: 사이버캡 원가 $20,000~$30,000이면 마일당 $0.05~$0.30 유리 | 2024 ~ 2026 | `scaling.md` 5·6장 | 선행 조사 |
| 사이버캡 제조 원가 추정: ARK $18,000, Tesla 목표가 $25,000~$30,000 | 2026 | https://robotaxidepot.com/cybercab-cost/ 등 | 검색 요약만 |

찾지 못한 것: Tesla의 탑승 건수, 실제 동시 운행 대수, 로보택시 매출, 실제 마일당 비용, 사이버캡 생산 라인의 투자액.

## A-3. 시장이 기대하는 숫자 (사실과 남의 전망)

| 내용 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| Visible Alpha 로보택시 매출 중앙값: 2027년 "$1 billion", 2030년 "$25 billion ... (primarily from the mobility service itself)" | 2026-09-21 | https://www.fool.com/investing/2026/09/21/teslas-free-cash-flow-went-negative-it-still-has-a/ | 원문 확인† |
| Visible Alpha 표(Cybercab/Robotaxi 매출, 단위 $M). 평균: 2026년 183, 2027년 1,843, 2028년 6,998, 2029년 22,276, 2030년 42,436. 중앙값: 87, 1,205, 2,285, 25,748, 34,776. "20% of revenue in 2030 and about 30% of gross profit" | 2026-05-27 | https://www.fool.com/investing/2026/05/27/tesla-stock-gets-wall-street-upgrade-on-robotaxi-p/ | 원문 확인† |
| S&P Visible Alpha(분석가 3명): 사이버캡 매출 2026년 $1B, 2030년 $75B, 차량 매출의 약 45% | 날짜 미확인 | https://www.spglobal.com/market-intelligence/en/news-insights/research/teslas-robotaxis-could-drive-45-of-automotive-sales-by-2030 | 검색 요약만 |
| Goldman Sachs: 미국 로보택시 시장 전체가 2030년 $19B, 2035년 $48B. 세계 차량은 "roughly 7,000 vehicles last year to about 1 million in 2030", 세계 시장 2035년 약 $415B | 날짜 미확인(2026) | https://www.goldmansachs.com/insights/articles/robotaxis-to-become-a-400-billion-dollar-market-in-2035 | 검색 요약만(403) |
| Goldman "26.9천 대(2027), 473.5천 대(2030)" | 날짜 미확인 | https://www.goldmansachs.com/pdfs/insights/goldman-sachs-research/robotaxi/report.pdf | 검색 요약만(403). **Tesla만의 숫자인지, 어느 지역인지 이번에도 확인하지 못했다.** 같은 보고서의 "세계 100만 대"와 함께 나오므로 Tesla 전망이라고 쓰면 안 된다 |
| Goldman(Delaney): Tesla 로보택시 2027년 매출 약 $115M, 가격 가정 마일당 $2.50 | 날짜 미확인 | 검색 요약 | 검색 요약만(인용된 기사 본문에서는 확인되지 않았다) |
| Morgan Stanley(2024년 Jonas 틀): Tesla Mobility 2030년 157,500대, 매출 $17B, 주당 $61(목표가 $310의 약 20%) | 2024년 | https://www.tesla-mag.com/en/analysis-of-teslas-robotaxis-by-morgan-stanley/ | 원문 확인†(2차. 2024년 자료) |
| Morgan Stanley(Percoco): 2026년 말 1,000대, 2035년 100만 대 | 2025-12-17 | `scaling.md` 5장 | 선행 조사 |
| Musk: "Robotaxi likely will not see material revenue until at least 2027." | 2026-07 | `scaling.md` 5장 | 선행 조사 |

Tesla의 크기 (비교용):

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 2025년 총매출 $94,827M, 자동차 매출 $69,526M, 자동차 매출원가 $57,165M, 총이익 $17,094M | 2025 회계연도 | https://www.sec.gov/Archives/edgar/data/1318605/000162828026003952/tsla-20251231.htm | 원문 확인(직접 읽음) |
| 자동차 매출총이익 $12,361M (17.8%) | | 69,526 − 57,165 | 계산 (규제 크레딧 $1,993M 포함) |
| 분기 총매출: 2025년 3분기 $28,095M, 4분기 $24,901M, 2026년 1분기 $22,387M, 2분기 $28,236M. 자동차 매출: $21,205M, $17,693M, $16,234M, $20,516M | 2026-07-22 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026049213/exhibit991.htm | 원문 확인† |
| 최근 4개 분기 총매출 $103,619M, 자동차 매출 $75,648M | | 위 숫자의 합 | 계산 |

## A-4. 이미 넣은 돈 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 2025년 설비투자 "Capital expenditures amounted to $8.53 billion in 2025 compared to $11.34 billion in 2024" | 2026-01 | 위 10-K | 원문 확인(직접 읽음) |
| 2026년 전망(연초): "we currently expect our capital expenditures to exceed $20 billion in 2026 driven by our AI initiatives ... the expansion and ramp of our manufacturing and R&D production lines and facilities, and growth in our fleet of company-operated AI-enabled assets" | 2026-01 | 위 10-K | 원문 확인(직접 읽음) |
| 2026년 전망(상향): "more than $25 billion". 최대 $30B의 신규 차입 한도 확보 | 2026-07-22 | 위 2분기 녹취(Fool) | 원문 확인† |
| 분기 설비투자: 2025년 3분기 $2,248M, 4분기 $2,393M, 2026년 1분기 $2,493M, 2분기 $5,789M | 2026-07-22 | 위 exhibit991 | 원문 확인† |
| 2026년 상반기 설비투자 $8,282M | | 2,493 + 5,789 | 계산 |
| 불일치: Motley Fool 9월 기사는 2분기 설비투자를 "$3.3 billion"으로 적는다. Tesla 공시 요약은 $5,789M이다. 공시 쪽을 따랐다 | 2026-09-21 | 위 Fool 9월 기사 | 원문 확인† |
| CFO: 설비투자는 앞으로 2~3년 더 는다. 용도는 로보택시 차량 확대, Optimus 생산, 반도체 공장, 태양광, AI 연산 | 2026-07 | https://www.nasdaq.com/articles/tesla-reaffirms-massive-capital-spending-2026-robotaxis-and-artificial-intelligence | 검색 요약만 |
| 사이버캡 설치 능력 ">125,000", 상태 "Production" | 2026 2분기 | 위 exhibit991 | 원문 확인† |

찾지 못한 것: 설비투자 중 사이버캡 라인이나 로보택시 차량에 쓴 금액. Tesla는 나눠 밝히지 않는다.

## A-5. 작업자의 계산

모든 값은 위 표의 숫자로 계산했다. 가정은 줄마다 적었다.

**(i) Waymo의 실제 가동과 요금으로 본 한 대의 연 매출**

- 하루 탑승: 500,000 ÷ 7 = 71,429건.
- 대당 하루 탑승: ÷ 3,000대 = 23.8건, ÷ 3,600대 = 19.8건, ÷ 3,871대 = 18.5건, ÷ 4,000대 = 17.9건. 탑승 숫자(2026-03 이후 "50만 건 이상"이 반복됨)와 차량 수의 날짜가 달라 범위로 읽어야 한다.
- 연 매출 총액: 500,000 × 52 × $19.69 = $512M. $18이면 $468M. Sacra 추정 $355M(2026-02)은 건당 약 $14.4에 해당한다(355M ÷ (475,000 × 52)).
- 대당 연 매출:

| 차량 수 가정 | 건당 $19.69 | 건당 $18 | 건당 $14.4 |
|---|---:|---:|---:|
| 3,000대 | $170,600 | $156,000 | $124,800 |
| 3,871대 | $132,300 | $120,900 | $96,700 |
| 4,000대 | $128,000 | $117,000 | $93,600 |

- 정리: Waymo 한 대는 연 **약 $10만~$13만**(3,871~4,000대 기준)을 번다. $19.69는 요금이 가장 높은 San Francisco의 값이라 위쪽 끝은 과대일 수 있다.
- 유료 거리: 18.5건 × 3.93마일 = 하루 약 73마일. 건당 $19.69 ÷ 3.93마일 = 유료 마일당 약 $5.0. 요금은 San Francisco, 거리는 캘리포니아 전체라 짝이 정확하지 않다.
- Other Bets 매출 $382M(분기)은 Waymo 외 사업을 포함하므로 Waymo 매출의 상한일 뿐이다. 전부 Waymo라고 쳐도 연 $1.53B, 4,000대로 나누면 대당 $382,000이 되는데 이는 탑승 건수와 맞지 않는다(건당 $59). 그래서 계산에 쓰지 않았다.

**(ii) Tesla가 실제로 보인 유료 거리와 요금으로 본 한 대의 연 매출**

- 2분기 유료 거리: 2.5M − 1.8M = 약 70만 마일(도표 판독, 오차 ±10만 마일 가능). 91일로 나누면 하루 약 7,700마일. 이 숫자는 운전자가 탄 Bay Area 차량을 포함한 전체 네트워크다.
- 대당 하루 유료 거리는 분모에 따라 크게 달라진다. 57대(6월 말 Texas)만으로 나누면 135마일, 약 200대(2월 추정, 두 지역)면 38마일, Bay Area 등록 1,655대면 4.6마일. 57대 가정은 Bay Area 주행을 Texas 차에 얹은 것이라 상한이다.
- 요금: Austin "$3.00 + $1.40/마일" 기준 5마일 탑승은 $10, 유료 마일당 $2.00. 사이버캡은 한 사례에서 35% 쌌다(마일당 약 $1.30).
- 대당 연 매출: 38마일 × $2.00 × 365 = **약 $27,700**. 상한(135마일)은 $98,600. 사이버캡 요금($1.30)이면 $18,000.
- 전체 네트워크 매출로 보면 2분기 70만 마일 × $2.00 = 약 $1.4M, 연환산 약 $5.6M이다. Musk의 "2027년 전에는 의미 있는 매출이 없다"와 맞는다.
- 한계: Tesla가 운행 대수를 밝히지 않아 이 값은 자릿수 정도만 믿을 수 있다.

**(iii) 섞은 경우: Tesla 요금 × Waymo 가동**

- 하루 유료 73마일 × $2.00 × 365 = $53,300. 사이버캡 요금($1.30)이면 $34,600.
- 참고: `../cybercab-investment-thesis.md`의 가정(하루 유료 150마일, $1.20, 330일)은 $59,400이다.

**기대 매출을 차량 대수로 바꾸면** (연평균 운행 대수)

| 대당 연 매출 가정 | 2027년 $1.0B (9월 중앙값) | 2027년 $1.84B (5월 평균) | 2030년 $25B (9월 중앙값) | 2030년 $42.4B (5월 평균) |
|---|---:|---:|---:|---:|
| $130,000 (Waymo 실제, 위쪽) | 7,700대 | 14,200대 | 192,000대 | 326,000대 |
| $100,000 (Waymo 실제, 아래쪽) | 10,000대 | 18,400대 | 250,000대 | 424,000대 |
| $53,000 (Tesla 요금 × Waymo 가동) | 18,900대 | 34,800대 | 472,000대 | 801,000대 |
| $34,600 (사이버캡 요금 × Waymo 가동) | 28,900대 | 53,300대 | 723,000대 | 1,226,000대 |
| $27,700 (Tesla 관측치) | 36,100대 | 66,500대 | 903,000대 | 1,532,000대 |

- 2026-10-02 Texas 인가 대수는 589대다. 2027년 $1B에는 연평균 7,700~36,000대가 필요하므로 지금의 13~61배다.
- Waymo는 4,000대로 연 $0.4~0.5B를 번다. Tesla의 2027년 기대 $1B는 지금 Waymo의 두 배다.
- 2030년 $25B는 Goldman이 본 미국 시장 전체($19B, 검색 요약만)보다 크다. 두 숫자가 같은 범위를 재는지 확인하지 못했다. Visible Alpha 숫자에 해외나 고객 소유 차량의 수수료가 들어 있을 수 있다.
- 차량 투자: 192,000~472,000대 × $27,500(목표가 중간) = $5.3B~$13.0B. 차고지와 충전은 빼고 차값만이다.

## 질문 A에 대한 답

- **답**: 실제로 굴러가는 로보택시 한 대는 Waymo 기준으로 연 약 $10만~$13만을 번다(하루 18~20건, 건당 $14~$20). Tesla가 지금 받는 요금(유료 마일당 약 $2.0)으로 같은 가동을 내면 약 $5만 3천, 사이버캡 요금이면 약 $3만 5천이다. Tesla가 실제로 보인 값은 자릿수로 약 $3만이다. 이 값으로 나누면 2027년 기대 매출 $1B는 연평균 약 8천~3만 6천 대, 2030년 $25B는 약 19만~90만 대다. Tesla가 Waymo보다 싸게 받는 한, 같은 매출에는 Waymo의 2~4배 차량이 필요하다.
- **범위**: 매출(손님이 낸 운임)만 본 것이다. 이익은 질문 C에서 다룬다. Waymo 숫자는 회사 발표의 반올림 값과 2차 집계의 조합이고, 요금은 San Francisco 표본이다. Tesla 숫자는 도표 판독과 추적 사이트에 기댄다.
- **남은 빈칸**: Waymo 단독 매출과 도시별 손익, Tesla의 운행 대수·탑승 건수·매출, Visible Alpha 숫자의 범위(직영 운임인지 수수료 포함인지, 분석가 수), Goldman의 26.9천/473.5천 대가 무엇을 세는지, 사이버캡 라인 투자액.

---

# 질문 B. 규제 완화는 사이버캡에 얼마나, 언제 중요한가

## B-1. 주별 상황 (사실)

| 주 | 인구 (2025-07-01) | Tesla의 현재 상태 | 운전대 없는 차에 대한 주법 | 확인 |
|---|---:|---|---|---|
| Texas | 31,709,821 | Austin·Dallas·Houston에서 Model Y 무감독 운행, 사이버캡은 Austin만. DMV 인가는 회사의 자기인증 | 인가 요건에 "연방법에 맞는 자율주행 시스템"이 들어 있다(`stakeholders.md` 4-1). 2021년 H.B. 3026이 운전대·페달 없는 설계를 허용했다는 설명은 검색 요약만 | 선행 조사 + 검색 요약만 |
| Florida | 23,462,518 | Miami(2026-07-03), Orlando·Tampa(07-21)에서 Model Y 무감독 운행 | 주·연방법을 지킬 수 있고 보험 $1M이 있으면 무인 운행 허용(검색 요약만) | https://thechargeport.com/robotaxi-tracker 원문 확인†, 법 내용은 검색 요약만 |
| Nevada | 3,282,188 | 2026-08-20 Clark County 최대 5,000대 인가. 승객 운행은 아직 시작하지 않았다 | 확인하지 못함 | 위 tracker 원문 확인†, `stakeholders.md` 4-3 |
| Arizona | 7,623,818 | TNC 허가(무인 불가, 2025-11). Phoenix에 Model Y 약 60대 대기, 긴급대응 계획 제출 | 주·연방 차량법을 지키면 된다는 설명(검색 요약만) | 검색 요약만 |
| Georgia | 11,302,748 | Tesla 운행 계획을 찾지 못함 | 주법: 연방이나 주가 면제를 주지 않았다면 제조 시점에 FMVSS 적합 인증을 받은 차여야 한다(검색 요약만) | 검색 요약만 |
| California | 39,355,309 | 무인 시험·배치 허가 없음. 가진 것은 CPUC 전세 운송(TCP) 허가와 DMV의 운전자 탑승 시험 허가. CPUC: "Tesla is not operating an autonomous vehicle service." "the person who is sitting in the driver's seat, that is the driver. That is not a safety driver." | 별도 허가 단계가 필요하다(DMV 무인 시험 → 배치, CPUC 여객 허가) | https://electrek.co/2026/03/25/california-regulator-confirms-tesla-not-operating-autonomous-vehicle-service/ 원문 확인† |
| California (계속) | | 2025년 캘리포니아 자율주행 시험 주행 0마일(6년 연속). DMV는 Tesla가 추가 허가를 신청하지 않았다고 확인. 2026-10-03 CNBC: "Tesla still hasn't obtained permits to run its vehicles on public roads without humans at the wheel." | | 앞의 두 문장은 검색 요약만(automotiveworld, 연결 끊김). CNBC 문장은 `stakeholders.md` 4-3 |
| New York | 20,002,427 | 계획을 찾지 못함 | 시험 법이 차 안의 사람을 요구한다 | 검색 요약만 |
| Massachusetts | 7,154,084 | 계획을 찾지 못함 | 사람 운전자 동승을 명시적으로 요구하는 6개 주 가운데 하나 | 검색 요약만 |
| Illinois | 12,719,141 | 계획을 찾지 못함 | 불분명 | 검색 요약만 |
| Washington DC | 약 70만(이번에 확인하지 않음) | 계획을 찾지 못함 | 상업 운행 금지, 시험에도 안전 운전자 필요. 2026년 허용 법안 발의 | 검색 요약만 |

- 인구는 Census Vintage 2025 추정(미국 전체 3억 4,180만)이다. 확인 수준은 검색 요약만이다.
- 계산: Tesla가 무감독 운행을 하거나 인가를 받은 Texas + Florida + Nevada는 5,845만 명, 미국의 17.1%. Arizona와 Georgia를 더하면 7,737만 명, 22.6%. California + New York + Massachusetts + Illinois는 7,923만 명, 23.2%.
- 호출 시장의 주별 비중: 찾지 못했다. Uber 2025년 10-K는 "We generate a significant percentage of our Gross Bookings from trips in large metropolitan areas and trips to and from airports"와 "In 2025, we generated 15% of our Mobility Gross Bookings from trips that either started or were completed at an airport"만 적는다(원문 확인, 직접 읽음, https://www.sec.gov/Archives/edgar/data/1543151/000154315126000015/uber-20251231.htm ). 2024년 공시에는 "Mobility Gross Bookings의 20%가 Chicago, Los Angeles, New York City, São Paulo, London 다섯 대도시권에서 나왔다"는 문장이 있었다(검색 요약만). 2025년 10-K 본문에서는 이 문장을 찾지 못했다.
- 해석(작업자): Uber가 꼽은 미국 3대 도시권(Chicago, Los Angeles, New York)은 모두 Tesla가 무인 운행을 할 수 없는 주에 있다. 주 규제가 막는 것은 인구의 4분의 1이지만 호출 수요로는 그보다 클 가능성이 높다. 숫자로는 확인하지 못했다.
- 해석(작업자): 확인한 주법들은 운전대를 직접 요구하지 않고 "연방 기준 적합 또는 면제"에 기댄다. 그래서 운전대 없는 차의 운명은 주가 아니라 연방(NHTSA의 자기인증 감사, AQ26002)에서 갈린다. Texas·Georgia 조문의 해당 부분은 이번에 원문으로 읽지 않았다.

캘리포니아 일정에 관해 찾지 못한 것: Tesla의 무인 시험 허가 신청, DMV가 밝힌 처리 기간, Tesla가 밝힌 캘리포니아 무인 운행 목표일. 선행 주자의 소요 기간도 이번에 원문으로 확인하지 못했다.

## B-2. 연방: 상한과 Model Y라는 우회로 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| Part 555 면제는 제조사당 12개월에 2,500대까지다(49 U.S.C. § 30113(d)). Zoox 면제도 12개월당 2,500대, 기간 2026-07-31~2028-07-31, 신청에서 승인까지 약 11개월 | 2026-07-31 | `precedents.md` 2-1 | 선행 조사 |
| Tesla는 Part 555 면제를 신청하지 않았다. 사이버캡이 모든 FMVSS에 맞는다고 자기인증했다. Moravy는 상한이 적용되느냐는 질문에 "No"라고 답했다 | 2026-04, 2026-09 | https://electrek.co/2026/04/23/tesla-cybercab-production-starts-no-nhtsa-2500-vehicle-cap/ | 원문 확인† |
| NHTSA는 그 자기인증을 감사 중이다(AQ26002, 2026-09-03 개시, Special Order 2026-09-10, 답변 기한 연장) | 2026-09 ~ 10 | `precedents.md` 1장 | 선행 조사 |
| Model Y는 운전대가 있어 면제가 필요 없다. Tesla는 이미 Austin, Dallas, Houston, Miami, Orlando, Tampa에서 Model Y로 무감독 운행을 한다 | 2026-09-24 기준 | https://thechargeport.com/robotaxi-tracker | 원문 확인†(2차 집계) |
| Texas 등록: Model Y 420대, 사이버캡 169대 | 2026-10-02 | `scaling.md` 4장 | 선행 조사 |
| 10-K: "Our Robotaxi business currently operates with Model Y vehicles but, in time, will include Cybercab" | 2026-01 | 위 Tesla 10-K | 원문 확인(직접 읽음) |
| 사이버캡 효율 약 165 Wh/mi, Model Y RWD 약 240 Wh/mi, 배터리 50 kWh 미만, 2인승 | 2026-05-22 | https://electrek.co/2026/05/22/tesla-cybercab-most-efficient-ev-ever-165-wh-mi/ | 검색 요약만(403) |
| Musk: "90% of miles driven are with one or two people". 사이버캡을 장래 생산의 다수로 만들겠다는 취지 | 2026-04 | 위 electrek 4월 기사 | 원문 확인† |
| Waymo 캘리포니아 탑승당 승객 약 1.4명 | 2023-08 ~ 2025-12 | `scaling.md` 6장(findingspress) | 선행 조사 |
| Waymo 탑승의 71%가 1명, 15%가 2명, "90%가 2명 이하"(CPUC 자료 분석이라고 인용) | 날짜 미확인 | https://www.notebookcheck.net/Tesla-was-right-about-Cybercab-design-as-per-new-Waymo-robotaxi-data.1174205.0.html | 검색 요약만(403). 71 + 15 = 86이라 90%와 맞지 않는다 |
| BofA: Waymo 로보택시 한 대 $150,000, Model Y $40,000 | 2026-03-05 | https://finance.yahoo.com/news/bofa-bullish-on-tesla-calls-it-the-current-leader-in-autonomy-and-soon-robotaxis-164643460.html | 원문 확인† |
| 사이버캡 목표가 $25,000~$30,000 | 2026-09-03 | `scaling.md` 4-2 | 선행 조사 |
| Cantor: "Management previously said that once production ramps, it expects Cybercab to ultimately be the largest volume vehicle in its lineup" | 2026-10-02 | `stakeholders.md` 5-2 | 선행 조사 |

작업자의 계산: Model Y로 대신하면 얼마나 손해인가

- 전기료: (240 − 165) Wh/mi × $0.16/kWh = 마일당 $0.012.
- 차값: $40,000 − $27,500 = $12,500. 30만 마일을 탄다고 가정하면 마일당 $0.042. 30만 마일은 작업자 가정이다.
- 합계 마일당 약 $0.05~$0.06. Goldman이 말한 "경쟁 차량 대비 $0.05~$0.30 유리"의 아래쪽 끝과 같다.
- 하루 총 124마일(유료 73마일 ÷ 58.9%)을 달리는 차라면 연 45,000마일 × $0.055 = 대당 연 약 $2,500. 대당 매출 $53,000의 약 5%다.
- 좌석: Model Y는 5인승이라 3명 이상 탑승(Waymo 자료로 10~14%)도 받는다. 사이버캡은 받지 못한다.

## B-3. 언제 풀리나 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| NHTSA 최종 규칙 목표일: 제안 문서에 없다. DOT 2026년 규제 의제 해설도 8개 개정 작업(10개 표준)을 나열할 뿐 날짜를 적지 않았다. 새로 오른 것은 FMVSS 111(RIN 2127-AN05), 126(2127-AN03), 201·208(2127-AN04) | 2026-07-09 | https://environmentalhealthsafetybrief.sidley.com/2026/07/09/the-department-of-transportations-2026-regulatory-agenda-acceleration-of-autonomous-vehicle-rulemaking-and-future-action-on-fuel-economy/ | 원문 확인†(로펌 해설. reginfo.gov 원문은 열지 않음) |
| ADS 성능 기준 제정(RIN 2127-AM99)은 사전 단계다. 해설: "not at all clear that those standards will be finalized in the current Administration" | 2026-07-09 | 위와 같음 | 원문 확인† |
| FMVSS 135(브레이크) 제안 의견 마감 2026-08-26. 제안에서 확정까지 전례 11~40개월 | | `precedents.md` 4-1, 4-2 | 선행 조사 |
| **H.R. 7389는 2026-05-21 위원회를 48 대 1로 통과했다**: "Ordered to be Reported (Amended) by the Yeas and Nays: 48 - 1." 그 뒤 조치는 없다(상태 자료 갱신일 2026-08-20) | 2026-05-21 | https://www.govinfo.gov/bulkdata/BILLSTATUS/119/hr/BILLSTATUS-119hr7389.xml | 원문 확인(직접 읽음) |
| **그런데 위원회가 채택한 대체안(Amendment in the Nature of a Substitute)에는 2,500 → 90,000 조항이 없다.** 발의본 8조 "General exemptions"가 대체안 목차에 없고, 본문에 "30113", "2,500", "90,000"이 한 번도 나오지 않는다 | 2026-05-19 등록 | https://docs.house.gov/meetings/IF/IF00/20260521/119327/BILLS-119-7389-G000558-Amdt-1.pdf | 원문 확인(직접 읽음, PDF 본문 검색) |
| Latta 의원이 SELF DRIVE Act 전체를 대체안에 붙이는 수정안(LATTA_021)을 냈다가 철회했다. 속기록: "with that commitment, I will withdraw the amendment." 위원장: "We do want to move this, that is for sure." | 2026-05-21 | https://docs.house.gov/meetings/IF/IF00/20260521/119327/HMKP-119-IF00-Transcript-20260521.pdf | 원문 확인(직접 읽음) |
| Latta: "When this bill passed out of the subcommittee, we had a commitment that we were going to start to work on this issue this summer". Pallone: "my understanding is exactly that commitment has already been made, both to you and to Mrs. Dingell." | 2026-05-21 | 위 속기록 | 원문 확인(직접 읽음) |
| Dingell: "I wish all our bipartisan work around autonomous vehicles had been included in this package" | 2026-05-21 | 위 속기록 | 원문 확인(직접 읽음) |
| Latta 수정안의 내용: 탑승자가 안전 정지를 명령할 수단이 있으면 FMVSS가 수동 조작 장치를 요구할 수 없다. 연방 선점 조항 포함. 대수 상한 숫자는 없다 | 2026-05-20 | https://docs.house.gov/meetings/IF/IF00/20260521/119327/BILLS-119-7389-A000370-Amdt-8.pdf | 원문 확인(직접 읽음) |
| **H.R. 7390(SELF DRIVE Act)은 소위원회 통과(12 대 11, 2026-02-10) 뒤 진전이 없다**(상태 자료 갱신일 2026-09-19) | 2026-09-19 | https://www.govinfo.gov/bulkdata/BILLSTATUS/119/hr/BILLSTATUS-119hr7390.xml | 원문 확인(직접 읽음) |
| H.R. 7389는 하원 교통위의 육상교통 재승인 법안(BUILD America 250 Act, H.R. 8870)에 묶여 갈 예정이다 | 2026-05 | https://members.asashop.org/press-releases/Details/u-s-house-energy-and-commerce-committee-passes-motor-vehicle-modernization-act-of-2026-334376 | 원문 확인† |
| 육상교통 프로그램은 2026-09-30 만료 대신 2026-12-11까지 연장됐다(H.R. 6500). H.R. 8870은 위원회 통과(62 대 2, 2026-05-22) 뒤 본회의에 오르지 않았다. Graves 위원장: "Passing a multi-year surface transportation reauthorization bill before the end of this Congress remains a top priority for me." | 2026-09-02 | https://www.masstransitmag.com/management/article/55403068/surface-transportation-programs-extended-to-december-2026 | 원문 확인† |
| 상원: Cruz 위원장이 재승인 법안에 "AV title"을 넣고 싶다고 했다(2026-06). 상원 법안 문안은 찾지 못했다 | 2026-06 | `precedents.md` 4-3 | 선행 조사 |
| 전례: 2017년 SELF DRIVE Act는 하원을 통과했지만 상원에서 멈췄고 AV START Act는 상원 본회의에 오르지 못했다. Latta 본인 발언: "Since ... we passed this legislation in 2017, 340,000 Americans have died on the highways" | 2017 ~ 2018 | `precedents.md` 4-3, 위 속기록 | 선행 조사 + 원문 확인(직접 읽음) |

- `precedents.md` 4-3의 "2,500 → 90,000대 조항은 H.R. 7389에 있다"는 **발의본에만 해당한다.** 위원회를 통과한 판본에는 없다. 그 문서의 마지막 행("전체 위원회 통과 여부: 찾지 못함")도 이번에 확인됐다.
- 해석(작업자): 2026-10-05 현재 상·하원 어느 쪽에서도 상한을 올리는 문안이 위원회를 통과한 상태가 아니다. 남은 길은 (1) 약속대로 별도의 자율주행 법안을 위원회에서 다시 다루는 것, (2) 12월 11일 전후의 재승인 법안 협상에서 상원의 "AV title"에 넣는 것이다. 119대 의회는 2027-01-03에 끝나고 그때까지 처리되지 않은 법안은 폐기된다. 2026-11-03 중간선거 뒤 회기는 약 5주다.
- 기준율(작업자): 자율주행 승용차 연방 법안은 2017년부터 2026년까지 9년 동안 한 번도 법이 되지 못했다. 가장 멀리 간 것이 2017년 하원 통과다. 이번에는 하원 본회의에도 가지 못했다.
- 중간선거의 영향을 다룬 분석은 찾지 못했다.

## B-4. 미국 밖 (사실)

| 지역 | 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|---|
| 유럽 | Musk: "Hopefully soon in Europe too". 출시 도시·날짜·승인 경로는 없다. EU 6개국이 FSD (Supervised)를 승인했고 운전대 없는 차의 승인은 "an even steeper climb" | 2026-09-08 | https://www.notateslaapp.com/news/4665/musk-tesla-cybercab-hopefully-coming-soon-to-europe | 원문 확인† |
| 유엔 | UNECE WP.29가 2026-06-24 자율주행 시스템 세계 기술 규정(ADS GTR)을 채택했다 | 2026-06-24 | https://www.connectedautomateddriving.eu/blog/unece-adopts-first-ever-global-rules-allowing-fully-autonomous-vehicles/ | 검색 요약만. 발효일("7월 말")도 검색 요약만 |
| 중국 | Beijing·Shanghai에서 사이버캡을 전시만 했다. 로보택시 상업 허가도 무감독 주행 승인도 없다. 현지 소프트웨어는 레벨 2로 분류된다. CFO가 1분기 발표에서 "targeting that approval by the end of Q3 2026"이라고 했다(무엇의 승인인지 기사 요약으로는 불분명) | 2026-09-17 | https://www.techtimes.com/articles/327677/20260917/tesla-brings-driverless-cybercab-china-no-chinese-permit-operate.htm | 원문 확인† |
| 일본·홍콩·호주 | 2026-09-09 홍콩에서 시작한 전시 순회(Tokyo, Osaka, Nagoya, 호주 7개 도시, 12월까지). 판매·시승·운행은 없다 | 2026-09 | https://teslant.com/en/news/tesla-cybercab-asia-pacific-tour-no-europe-2026-09 | 검색 요약만 |
| 한국 | FSD V14-Lite 배포 대상에 한국이 있다는 요약뿐이다. 로보택시 계획은 찾지 못했다 | 2026 | https://www.notateslaapp.com/news/4031/everything-tesla-announced-during-its-q1-2026-earnings-call-summaryrecap | 검색 요약만 |
| 중동 | Musk가 로보택시가 언젠가 사우디에 갈 것이라고 했다(시점 없음). 경쟁사: WeRide·Uber가 Abu Dhabi·Dubai·Riyadh에 1,200대 이상(2027년) | 날짜 미확인 | https://www.teslarati.com/tesla-robotaxi-saudi-arabia-elon-musk/ | 검색 요약만 |

Tesla 2분기 실적 발표 녹취 요약에는 해외 로보택시 일정이 없었다(원문 확인†). 날짜가 붙은 해외 사이버캡 승인 계획은 어디에서도 찾지 못했다.

## B-5. 작업자의 계산: 상한은 언제 걸리고 무엇이 걸려 있나

전제: 상한이 "걸린다"는 것은 NHTSA가 자기인증을 인정하지 않아 Tesla가 Part 555 면제로 가는 경우다. 지금은 상한이 적용되고 있지 않다.

- 상한 아래 누적 사이버캡: 연 2,500대. 2027~2030년 4년이면 최대 10,000대. 면제는 2년 단위이고 Zoox는 승인에 11개월이 걸렸으므로 실제로는 더 적을 수 있다.
- 지금 속도: 등록 기준 32일에 124대는 연 1,414대, 최근 2주(14일에 111대)는 연 2,894대다. **최근 속도가 이미 연 2,500대 선이다.** 속도가 더 오르면 2027년부터 상한이 묶는다.
- 전례 속도(`scaling.md` 시나리오 1·2)로는 2030년 말 사이버캡이 약 6,200~12,500대다. 이 경로라면 상한(누적 10,000대)은 2029~2030년에야 묶거나 거의 묶지 않는다.
- 시장 기대 경로(2030년 연평균 19만~47만 대)라면 상한은 첫해부터 묶는다. 필요한 차의 2~5%만 사이버캡으로 채울 수 있다.
- 대수 차이: "상한 유지"면 2030년까지 사이버캡 최대 약 1만 대. "상한 없음"이면 공장이 정한다. 설치 능력 연 12만 5천 대 이상, Cybertruck 전례를 적용하면 4년 누적 8만~15만 6천 대(`scaling.md` 시나리오 3).
- 매출 차이: Model Y가 같은 서비스를 할 수 있으므로 매출에 걸린 것은 직접적으로는 거의 없다. 걸린 것은 비용이다. 2030년 $25B를 마일당 $2.00로 벌면 유료 125억 마일, 총 주행 약 212억 마일(÷ 58.9%). 여기에 마일당 $0.055를 곱하면 **연 약 $1.2B의 추가 비용**이다. 차값으로는 19만~47만 대 × $12,500 = $2.4B~$5.9B가 더 든다.
- 따로 걸린 것: 사이버캡 전용 라인(설치 능력 12만 5천 대 이상)이 연 2,500대만 만들게 되는 경우의 유휴 설비. 투자액을 찾지 못해 금액으로 적지 못했다.

## 질문 B에 대한 답

- **답**: 연방 규제는 로보택시 사업 전체가 아니라 사이버캡이라는 차의 운명을 정한다. Tesla는 이미 6개 도시에서 운전대 있는 Model Y로 무감독 운행을 하고 있고, Model Y로 대신할 때 드는 손해는 마일당 약 5~6센트, 대당 연 약 $2,500(매출의 약 5%)이다. 2030년 기대 매출 $25B 규모에서는 연 약 $1.2B다. 상한이 적용되면 2030년까지 사이버캡은 최대 약 1만 대이고, 지금의 배치 속도(최근 2주 연 2,900대꼴)가 이미 그 선에 닿아 있어 2027년부터 묶일 수 있다. 사업 전체를 좌우하는 규제는 따로 있다. 하나는 주 단위 무인 운행 허가다. California, New York, Illinois, Massachusetts는 인구의 23%이고 Uber의 미국 3대 도시권을 포함하는데 Tesla는 California에 무인 허가를 신청하지도 않았다. 다른 하나는 자기인증 감사가 Model Y 운행까지 번지느냐인데 이번 조사에서 그런 조짐은 찾지 못했다.
- **시기**: 입법으로 2026년 안에 풀릴 근거는 약하다. 상한을 9만 대로 올리는 조항은 5월 위원회 통과 판본에서 빠졌고 SELF DRIVE 수정안은 철회됐다. 남은 창은 12월 11일 전후의 재승인 법안과 2027-01-03 회기 종료다. 규칙 개정은 목표일이 없고 전례로는 2027~2029년이다. 가장 빠른 변수는 NHTSA가 Tesla의 답변에 내릴 판단이다.
- **범위**: 주법 조문(Texas 외)은 원문으로 읽지 않았다. Model Y 대체 비용은 차값 $40,000, 수명 30만 마일, 전기료 $0.16/kWh라는 가정에 기댄다.
- **남은 빈칸**: 주별 호출 시장 비중, California 무인 허가의 현실적 일정, 연장된 Special Order 답변 기한과 Tesla의 답, 상원 AV 문안, 사이버캡 라인 투자액, 날짜가 붙은 해외 승인 계획.

---

# 질문 C. 주가에는 로보택시가 얼마나 들어 있나

## C-1. 지금의 값과 실적 (사실)

| 사실 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| 종가 $370.59, 하루 +4.65%. S&P 500 +0.74%, Nasdaq +1.19%. 3분기 인도 486,532대. 시가총액 "$1.5 trillion". 2026년 들어 대형 기술주 7개 중 유일한 마이너스 | 2026-10-02 | https://www.fool.com/coverage/stock-market-today/2026/10/02/stock-market-today-oct-2-tesla-rises-on-q3-delivery-beat/ | 원문 확인† |
| 시가총액 $1.46T, 발행 주식 3.95B | 2026-10-02 | https://stockanalysis.com/stocks/tsla/market-cap/ | 검색 요약만 |
| 희석 주식 수(분기 가중평균) 3,540M | 2026 2분기 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026049213/exhibit991.htm | 원문 확인† |
| 분기 영업이익: $1,624M, $1,409M, $941M, $398M (2025년 3분기 ~ 2026년 2분기). GAAP 순이익: $1,373M, $840M, $477M, $1,114M. GAAP 희석 EPS: $0.39, $0.24, $0.13, $0.32. 비GAAP EPS: $0.50, $0.50, $0.41, $0.33 | 2026-07-22 | 위 exhibit991 | 원문 확인† |
| 분기 잉여현금흐름: $3,990M, $1,420M, $1,444M, −$1,092M. 2분기 자동차 매출총이익률 16.9%, 총이익률 16.8%. 현금·단기투자 $43,524M | 2026-07-22 | 위 exhibit991 | 원문 확인† |
| 순현금 $34.2B(현금 $43.5B − 부채 $9.3B) | 2026-09-21 | https://www.fool.com/investing/2026/09/21/teslas-free-cash-flow-went-negative-it-still-has-a/ | 원문 확인† |
| 최근 4개 분기 합계: 매출 $103,619M, 영업이익 $4,278M, 순이익 $3,806M, 희석 EPS $1.08, 잉여현금흐름 $5,762M. P/E 384.57, 선행 P/E 201.25 | 2026-10-05 조회 | https://stockanalysis.com/stocks/tsla/financials/?p=ttm | 원문 확인†(2차 집계) |
| 컨센서스 EPS: 2026년 $1.75~$1.77, 2027년 $2.16~$2.20. 2027년 값은 90일 전 $2.52였다. 선행 P/E 157.86(2026-09-13) | 2026-09 | https://www.gurufocus.com/term/forward-pe-ratio/TSLA 등 | 검색 요약만 |
| 2분기 영업이익률 1.4%, 조정 EBITDA 약 $3.27B | 2026-08-13 | https://www.investing.com/analysis/teslas-robotaxi-reality-check-time-to-deliver-200685781 | 원문 확인†(2차) |

계산과 불일치:
- 분기 합으로 다시 계산하면 영업이익 $4,372M(1,624 + 1,409 + 941 + 398), 순이익 $3,804M, EPS $1.08, 잉여현금흐름 $5,762M이다. 영업이익만 집계 사이트($4,278M)와 약 $94M 다르다. 이유는 확인하지 못했다.
- 시가총액은 세는 주식 수에 따라 다르다. 희석 주식 3,540M × $370.59 = $1.312T. 집계 사이트는 3.95B주로 $1.46T라고 적는다. 차이 약 4억 주의 정체는 확인하지 못했다. 아래 계산은 주당 값으로 하고, 총액이 필요하면 3,540M주를 썼다.
- 후행 P/E: $370.59 ÷ $1.08 = 343배. 2026년 컨센서스 기준 $370.59 ÷ $1.76 = 약 211배, 2027년 기준 ÷ $2.18 = 약 170배(EPS가 검색 요약만이므로 참고값).

## C-2. 증권사의 부문별 합산 (남의 평가)

| 기관 | 날짜 | 목표가 | 부문별 배분 | 출처 URL | 확인 |
|---|---|---|---|---|---|
| Morgan Stanley (Percoco) | 2026-09-03 직전 | $400, Equal-weight | Tesla Mobility(로보택시) 주당 $120, Network Services(FSD) $144. 나머지 부문은 기사에 없다 | `stakeholders.md` 5-2 (finance.biggo.com) | 선행 조사(2차 매체) |
| Morgan Stanley | 2025-12-08 | $425 | 자동차 본업 $55, Network Services/FSD $145, Optimus $60. 강세 $860, 약세 $145 | `stakeholders.md` 5-2 | 선행 조사 |
| Morgan Stanley (Jonas, 옛 틀) | 2024년 | $310 | Tesla Mobility $61(약 20%). 2030년 157,500대, 매출 $17B | https://www.tesla-mag.com/en/analysis-of-teslas-robotaxis-by-morgan-stanley/ | 원문 확인†(2차) |
| Bank of America (Perry) | 2026-03-05 | $460 | 로보택시(국내·해외) $844B, 전체 $1.625T의 52%. 자동차 21%, FSD 19%, 에너지 6%, Optimus 2% | https://finance.yahoo.com/news/bofa-bullish-on-tesla-calls-it-the-current-leader-in-autonomy-and-soon-robotaxis-164643460.html | 원문 확인† |
| Bank of America (이전 판) | 날짜 미확인 | $471 | 로보택시 45%, FSD 17%, 자동차 12%, 에너지 6%, Optimus 19% | https://eletric-vehicles.com/tesla/bofa-estimates-tesla-robotaxi-accounts-for-45-of-company-value/ | 검색 요약만(403) |
| William Blair (Dorsheimer) | 2025-12-18 | 없음 | 자동차는 "about $30 to $40 per share", 에너지는 그와 비슷하거나 조금 위, 자율주행(로보택시와 Optimus)이 70% 이상. 당시 주가 약 $480 | https://finance.yahoo.com/news/teslas-car-business-is-only-worth-30-a-share-analyst-warns-182354067.html | 원문 확인† |
| Piper Sandler (Potter) | 2026년 | $500 → $450 | 17개 제품군(차량, 에너지, 충전, 보험, FSD, 로보택시)의 20년 DCF 합이 주당 약 $400, Optimus에 $100. "At $400/share, we think investors can buy Optimus for free". 로보택시만의 값은 기사에 없다 | https://www.tikr.com/blog/tesla-stock-piper-sandler-says-optimus-is-free-at-445-heres-where-the-stock-could-go | 원문 확인†($450 하향은 검색 요약만) |
| Goldman Sachs | 2026-09-07 | $360 (상방 약 $500, 하방 약 $150) | 부문별 배분은 찾지 못했다 | `scaling.md` 5장 | 선행 조사 |
| Wedbush (Ives) | 2026-09 | $600 | 로보택시가 "$1 trillion of value alone"을 만들 수 있다는 발언. 부문별 표는 찾지 못했다 | `stakeholders.md` 5-2 | 선행 조사 |
| Wells Fargo (Langan) | 2026-07-15 | $130, Underweight | 부문별 배분 없음. "if today's profit cannot justify the price, the next question is what can." 당시 주가 약 $396 | https://finance.yahoo.com/markets/stocks/articles/wells-fargo-raised-tesla-stock-142312325.html | 원문 확인† |
| UBS (Spak) | 2026-09-24 | $385 | 배분을 찾지 못했다 | 검색 요약 | 검색 요약만 |
| Barclays (Levy) | 2026-09-21 | $370 | 배분을 찾지 못했다 | 검색 요약 | 검색 요약만 |
| Guggenheim (Jewsikow) | 2026 | $175, Sell | 배분 없음 | 검색 요약 | 검색 요약만 |
| GLJ Research | 2026 | $24.86, Sell | 배분 없음 | 검색 요약 | 검색 요약만 |
| ARK | 2024-06 모형 | 2029년 $2,600 | 기업가치의 약 90%가 로보택시 | `stakeholders.md` 5-2 | 선행 조사(검색 요약만) |

- "로보택시" 값의 범위: BofA는 "domestic & international"이라고만 적었다. Morgan Stanley는 Tesla Mobility(차량 호출)와 Network Services(FSD 구독 등)를 나눈다. 어느 쪽이 고객 소유 차량의 수수료를 로보택시에 넣는지는 2차 기사로 확인하지 못했다. Visible Alpha 2030년 중앙값은 "primarily from the mobility service itself"라고 적혀 있다.
- Bernstein의 2026년 부문별 값은 찾지 못했다.

## C-3. 로보택시를 뺀 사업의 값 (작업자의 계산)

가정: 지금 이익은 사실상 전부 자동차·에너지·서비스에서 나온다. 로보택시 매출은 연환산 수백만 달러 수준이기 때문이다(A-5).

| 방식 | 계산 | 주당 | $370.59 중 비중 |
|---|---|---:|---:|
| 최근 4개 분기 순이익 × 10배 (Toyota 선행 P/E 10.0, 검색 요약만) + 순현금 | $3.80B × 10 + $34.2B = $72B | $20 | 5% |
| 순이익 × 20배 + 순현금 | $3.80B × 20 + $34.2B = $110B | $31 | 8% |
| 순이익 × 30배 + 순현금 | $3.80B × 30 + $34.2B = $148B | $42 | 11% |
| William Blair: 자동차 $30~$40 + 에너지 같은 크기 | | $60~$80 | 16~22% |
| Morgan Stanley(2025-12): 자동차 본업 | | $55 (에너지 별도) | 15% |
| BofA(2026-03): 자동차 21% + 에너지 6% | $460 × 27% | $124 (목표가 기준) | 목표가의 27% |

- 정리: 지금 버는 사업은 평범한 배수로 주당 $20~$40, 증권사가 후하게 쳐도 $60~$125다. **주가 $370.59의 66~95%, 주당 약 $245~$350는 아직 이익이 없는 사업(FSD, 로보택시, Optimus)에 붙은 값이다.**
- 한계: 순이익에는 규제 크레딧과 이자 수익이 들어 있고 AI 투자 비용이 빠져 있지 않다. 에너지 부문의 성장에 높은 배수를 주면 비중은 달라진다.

## C-4. 로보택시의 이익 쪽 (사실과 남의 가정)

| 내용 | 날짜 | 출처 URL | 확인 |
|---|---|---|---|
| Morgan Stanley 마일당 총비용: Tesla $0.81, Waymo $1.43, 사람 운전 $1.71 | 2026-04-11 보도 | `scaling.md` 5장 | 선행 조사 |
| Tesla 목표 마일당 $0.30 미만, ARK 2030년 $0.16~$0.20 | 2024 ~ 2026 | `scaling.md` 5·6장 | 선행 조사(ARK는 검색 요약만) |
| BofA: $20짜리 사람 운전 호출에서 약 절반($9.60)이 운전자 몫이고 "this cost goes away with robotaxis" | 2026-03-05 | 위 BofA 기사 | 원문 확인† |
| Morgan Stanley(2024년 틀): 차량 원가 $45,000, 수명 7년 | 2024 | 검색 요약 | 검색 요약만 |
| "per-vehicle profits of $25,000–$40,000 annually", 수수료율 30%, 규모가 커지면 매출총이익률 40~60%라는 추정들 | 날짜 미확인 | 검색 요약(출처 섞임) | 검색 요약만 |
| Waymo의 실제: Other Bets 분기 영업손실 $1.8B(매출 $382M) | 2026 2분기 | 위 Alphabet 녹취 | 원문 확인(직접 읽음) |
| Other Bets 연간 영업손실: 2023년 $4.10B, 2024년 $4.44B, 2025년 $7.52B | 각 연도 | `scaling.md` 1-4 | 선행 조사(검색 요약만) |
| Waymo 기업가치 $126B(2026-02 투자 유치) | 2026-02 | `scaling.md` 1-4 | 선행 조사 |
| Uber: 시가총액 $147B, 기업가치 $154B, EV/EBITDA 15.1배 | 2026년 중반 | https://multiples.vc/public-comps/uber-valuation-multiples | 검색 요약만 |
| Tesla EV/EBITDA 100.22배, 비교 기업 중앙값 5.88배 | 2026년 | 위 tikr 기사 | 원문 확인†(2차) |

작업자의 계산: 비용에서 거꾸로 본 이익률

- 요금은 유료 마일에만 붙고 비용은 달린 모든 마일에 든다. 유료 비중 58.9%(Waymo 캘리포니아)를 쓰면 총 주행 마일당 매출은 $2.00 × 0.589 = $1.18이다.
- Morgan Stanley 비용($0.81)이면 영업이익률 (1.18 − 0.81) ÷ 1.18 = **31%**.
- Tesla 목표 비용($0.30)이면 75%.
- 사이버캡 요금($1.30)이면 총 마일당 매출 $0.77로 Morgan Stanley 비용 $0.81보다 낮다. **지금 사이버캡 요금은 제3자 추정 비용으로는 적자다.** 비용이 목표대로 내려가야 성립한다.
- 참고: Waymo 기업가치 $126B ÷ 약 4,000대 = 대당 약 $3,150만. 투자자는 지금 차가 아니라 미래의 차 수십만 대에 값을 치렀다.

## C-5. 작업자의 계산: 주가가 요구하는 차량 대수

여기부터는 전부 작업자의 가정과 산수다. 시장이 실제로 이렇게 계산한다는 증거가 아니다. 증권사의 배분 비율을 현재 주가에 그대로 곱한 것도 가정이다.

**(i) 현재 주가에 들어 있는 로보택시 값 (증권사 틀을 빌려)**

| 틀 | 로보택시 비중 | $370.59 기준 주당 | 총액 (3,540M주) |
|---|---:|---:|---:|
| Morgan Stanley (2026-09): $120 ÷ $400 | 30% | $111 | $393B |
| BofA (2026-03): $844B ÷ $1,625B | 52% | $193 | $682B |
| William Blair (2025-12): 자율주행 70% 이상, Optimus 포함 | 70% 이상 | $259 이상 | $918B 이상 |

중심값으로 $500B(주당 약 $141)를 쓴다. 범위는 $390B~$680B다.

**(ii) 그 값을 벌려면 몇 대가 언제까지 필요한가**

식: 현재 값 = 운행 대수 × 대당 세후 이익 × 이익 배수 ÷ (1 + 할인율)^햇수

가정:
- 할인율 연 10%. 이익 배수 25배(성장하는 플랫폼 기업 수준으로 잡은 값. Uber는 EV/EBITDA 약 15배). 세율 21%.
- 2030년 말까지는 4.25년(1.1^4.25 = 1.50), 2035년 말까지는 9.25년(1.1^9.25 = 2.41).
- 대당 세후 이익:
  - 보수: 매출 $53,000(Tesla 요금 × Waymo 가동) × 영업이익률 20% × 0.79 = **$8,400**
  - 중심: 매출 $100,000(Waymo 실제 아래쪽) × 30%(Morgan Stanley 비용에서 계산한 값) × 0.79 = **$23,700**
  - 낙관: 매출 $130,000 × 50% × 0.79 = **$51,400**

필요한 연 세후 이익: $500B × 1.50 ÷ 25 = $30.0B (2030년), $500B × 2.41 ÷ 25 = $48.3B (2035년).

| 대당 세후 이익 | 2030년 말에 필요한 대수 | 2035년 말에 필요한 대수 |
|---|---:|---:|
| 보수 $8,400 | 357만 대 | 575만 대 |
| 중심 $23,700 | 127만 대 | 204만 대 |
| 낙관 $51,400 | 58만 대 | 94만 대 |

- 로보택시 값을 $390B(Morgan Stanley)로 잡으면 위 숫자에 0.78, $680B(BofA)면 1.36을 곱한다. 중심 가정의 2030년 대수는 99만~172만 대다.
- 비교: 2026-10-02 Texas 인가 대수 589대. Waymo 약 4,000대. Musk 보상안의 목표 100만 대. Morgan Stanley의 2035년 전망 100만 대.
- 낙관 가정에서 2035년 94만 대는 Morgan Stanley와 보상안의 100만 대와 거의 같다. 즉 **지금 주가의 로보택시 몫은 "2035년 무렵 100만 대가 대당 $13만을 벌고 절반을 영업이익으로 남긴다"와 맞먹는다.**
- 교차 확인: Visible Alpha 2030년 중앙값 $25B에 이익률 30%, 세율 21%를 적용하면 세후 $5.9B, 25배면 2030년 값 $148B, 현재 값 $99B(주당 $28)다. 2030년 기대 매출만으로는 로보택시 몫($390B~$680B)의 15~25%만 설명된다. 나머지는 2030년 이후의 성장이나 더 높은 배수에 기댄다.

**(iii) Waymo의 가장 빠른 속도(연 2.34배)로 자란다면**

- 출발: Texas 인가 589대(2026-10-02). 등록 대수이고 실제 운행 대수는 더 적을 수 있다. Florida와 Bay Area 차량은 빠져 있다.
- 2030년 말: 589 × 2.34^4.25 = 589 × 37.1 = 약 21,900대. 중심 이익으로 연 $0.52B, 25배면 $13.0B, 현재 값 $8.6B, **주당 약 $2.4**. 낙관 이익이면 주당 약 $5.
- 2035년 말: 589 × 2.34^9.25 = 589 × 2,600 = 약 153만 대. 중심 이익으로 연 $36.3B, 25배면 $907B, 현재 값 $376B, **주당 약 $106**.
- 읽는 법: Waymo의 최고 속도를 9년 내내 이어 가면 Morgan Stanley 틀의 로보택시 몫(주당 $111)에 거의 닿는다. 4년만 보면 100분의 2다. Waymo가 이 속도를 유지한 기간은 13개월이었고 그 전 6년은 600~700대에 머물렀다(`scaling.md` 1-5).

이 계산이 틀리는 조건:
- 고객 소유 차량이 네트워크에 들어오면 Tesla는 차를 사지 않고 수수료를 받는다. 대당 이익은 줄지만 대수는 훨씬 빨리 늘 수 있다. 이 계산은 직영만 가정했다.
- 배수 25배와 할인율 10%는 작업자가 고른 값이다. 배수를 40배로 잡으면 필요한 대수는 0.63배가 된다. 할인율을 12%로 올리면 2035년 대수는 1.18배가 된다.
- 증권사 배분은 목표가를 나눈 것이지 시장 가격을 나눈 것이 아니다.

## C-6. 로보택시 소식과 주가 (사실)

| 날짜 | 사건 | Tesla | 시장·동종 | 출처 URL | 확인 |
|---|---|---|---|---|---|
| 2024-10-11 | We, Robot 행사 다음 날 | 약 −9% | 찾지 못함 | https://www.cnbc.com/2024/10/11/tesla-tsla-stock-drops-in-premarket-after-cybercab-robotaxi-reveal.html | 검색 요약만 |
| 2025-06-23 | Austin 로보택시 출시 뒤 첫 거래일 | 약 +8.2%, 시가총액 약 $100B 증가 | 찾지 못함 | https://www.cnbc.com/2025/06/23/tesla-stock-robotaxi-austin.html | 검색 요약만(403) |
| 2026-01-22 ~ 23 | Austin 무감독 운행 시작 발표 | 종가 기준 4% 이상 상승 | 선물만 언급(S&P 500 선물 −0.10%) | https://finance.yahoo.com/news/tesla-stock-pops-as-elon-musk-posts-video-claiming-no-safety-monitor-in-austin-robotaxi-191059641.html | 원문 확인†(거래일이 22일인지 23일인지 불분명) |
| 2026-09-03 | 사이버캡 행사 당일(행사 전) | 약 +7% | 찾지 못함 | https://uk.finance.yahoo.com/news/tesla-stock-soars-ahead-cybercab-212924792.html | 검색 요약만 |
| 2026-09-04 | 행사 다음 날, NHTSA 감사 개시 | −5.92%, 종가 $354.08 | S&P 500 −0.38%, Nasdaq −0.29%, GM +0.83%, Rivian −1.07% | https://finance.yahoo.com/markets/stocks/articles/stock-market-today-sept-4-211745990.html | 원문 확인† |
| 2026-09-08 | "Uber Falls 4% on Tesla Cybercab Threat" | Tesla +4%(제목) | | `stakeholders.md` 4-3 (247wallst) | 선행 조사 |
| 2026-09-15 ~ 16 | Special Order 공개 | 약 −1% | 기사에 없음 | https://finance.yahoo.com/markets/stocks/articles/tsla-edges-lower-regulator-asks-205735157.html | 원문 확인† |
| 2026-10-02 | 3분기 인도 대수 발표(로보택시 소식 아님) | +4.65% | S&P 500 +0.74%, Nasdaq +1.19% | 위 Fool 10-02 기사 | 원문 확인† |

- 시장 대비로 확인된 것은 2026-09-04 하나다. Tesla −5.92%, S&P 500 −0.38%이므로 약 5.5%포인트가 Tesla만의 움직임이다. $354.08 ÷ (1 − 0.0592) = 전일 종가 약 $376.4, 주당 약 $22 하락, 3,540M주 기준 약 $79B다(계산).
- 해석(작업자): 행사 전날 7% 오르고 다음 날 6% 내렸으므로 이틀을 합치면 거의 제자리다. Special Order 공개에는 1%만 움직였다. 로보택시 "출시" 소식에는 8% 안팎으로 크게 반응했고 규제 소식에는 작게 반응했다. 사례가 여섯 개뿐이라 통계로 쓸 수는 없다.

## 질문 C에 대한 답

- **답**: 2026-10-02 종가 $370.59에서 지금 이익을 내는 사업(자동차, 에너지, 서비스)이 평범한 배수로 설명하는 몫은 주당 약 $20~$40, 증권사가 후하게 쳐도 $60~$125다. 나머지 66~95%는 아직 이익이 없는 FSD·로보택시·Optimus의 값이다. 그중 로보택시만 떼면 증권사 틀에 따라 주당 $111(Morgan Stanley, 30%)에서 $193(BofA, 52%), 총액 약 $390B~$680B다. 이 값을 벌려면 작업자 가정(할인율 10%, 이익의 25배)으로 중심 경우 2030년 말 약 127만 대 또는 2035년 말 약 204만 대가, 낙관 경우 2035년 말 약 94만 대가 운행돼야 한다. 지금은 589대다. Waymo의 최고 속도(연 2.34배)로 자라면 2030년 로보택시 몫은 주당 약 $2~$5이고, 그 속도를 2035년까지 9년 이어야 주당 약 $106에 닿는다. 시장 컨센서스의 2030년 매출 $25B도 같은 가정으로는 주당 약 $28이다. 즉 지금 주가의 로보택시 몫은 2030년이 아니라 2035년 무렵 100만 대 규모의 고수익 서비스에 값을 치른 것이다.
- **범위**: 부문별 배분은 증권사 목표가의 구성을 현재 주가에 비례로 옮긴 것이다. 필요한 대수는 할인율·배수·이익률 가정에 크게 움직인다. 직영 차량만 가정했다.
- **남은 빈칸**: 증권사 보고서 원문(모두 2차 기사로만 봤다), Morgan Stanley의 2026년 Mobility 가정(대수, 마일당 매출, 이익률, 할인율), Goldman·UBS·Barclays·Bernstein의 부문별 값, 컨센서스 EPS의 1차 출처, 발행 주식 3.95B와 희석 3.54B의 차이, 로보택시 소식 당일의 시장 지수(2024-10-11, 2025-06-23, 2026-09-03), 고객 소유 차량 네트워크의 수수료 구조.

---

## 이번 조사에서 선행 문서와 달라진 점

- `precedents.md` 4-3: 2,500 → 90,000대 조항은 H.R. 7389 발의본에만 있다. 2026-05-21 위원회를 통과한 대체안에는 없다. SELF DRIVE 수정안은 같은 날 철회됐다.
- `scaling.md` 5장: Goldman의 "26.9천/473.5천 대"는 이번에도 원문을 열지 못했다. Tesla의 전망이라고 쓰면 안 된다.
- `stakeholders.md` 5-2: BofA의 로보택시 비중은 2026-03-05 기준 52%($844B ÷ $1.625T)로 확인됐다. 45%는 그 이전 판으로 보이며 검색 요약만이다.
- `../cybercab-investment-thesis.md`: Fool 기사가 적은 2분기 설비투자 "$3.3 billion"은 Tesla 공시($5,789M)와 다르다.
