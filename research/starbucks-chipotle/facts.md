# 스타벅스의 치폴레 인수설과 부인(2026-10): 사실과 판단 재료

조사 시각 2026-10-13(화) 00:00~00:20 KST = 미국 동부 10-12(월) 11:00~11:20, **미국 장 마감 전**. 조사만 했다. 대본과 제작물은 건드리지 않았다. 받은 시세는 `data/`(cmg.csv, sbux.csv, mcd.csv, vz.csv: 나스닥 API, 2018-01-02~2026-10-09 일별, 액면분할 반영·배당 미반영), 계산식은 `scripts/calc.py`에 있다.

**전제 확인: 사건은 실제로 있었다.** FT 보도(10-08), 스타벅스의 부인(10-12), 두 주식의 움직임을 CNBC·NBC·포춘·CBS·세마포 원문과 받은 시세로 확인했다. 받은 줄거리와 다른 곳이 여덟 군데 있다(11절).

확인 범위 표기: **[원문]** 기사·보도자료 본문을 직접 읽음 / **[요약도구]** 요약 도구를 거쳐 읽음 / **[재인용]** 다른 매체가 옮긴 것을 읽음(원 기사는 못 읽음) / **[데이터]** 받은 시세·컨센서스로 작업자가 계산 / **[자막]** 유튜브 자동 자막을 읽음(받아쓰기 오류 가능) / **[검색요약]** 검색 요약만 봄 / **[기억]** 작업자의 기억, 미확인. 뒤의 넷은 게시 전에 원문으로 확인한다.

시각 환산: 미국 동부(서머타임) + 13시간 = 한국. 미국 장은 한국 22:30~05:00.

## 한눈에

1. **10-08(목)** FT: 스타벅스가 최근 몇 달 자문사와 치폴레 인수 제안을 준비해 왔다. 성사되면 외식업 사상 최대 인수(지금 기록은 2014년 버거킹의 팀호턴스 114억 달러). 치폴레 시가총액은 약 390억~410억 달러.
2. 그날 치폴레는 장중 +8.5%(33.40달러), 종가 **+6.21%(32.68달러)**, 거래량 7,204만 주(직전 한 달 평균의 5배). 스타벅스는 장중 -6.7%(87.35달러)까지 갔다가 종가 -0.40%(93.21달러).
3. **10-09(금)** 치폴레 -3.34%(31.59달러): 하루 만에 오른 것의 절반 이상을 반납. 스타벅스 -2.64%(90.75달러).
4. **10-12(월) 09:01 ET(한국 22:01)** CNBC: 스타벅스 대변인이 짐 크레이머에게 **"Starbucks is not buying Chipotle."** NBC에는 이메일로 "we want to be clear we are not buying Chipotle". CNBC 방송은 크레이머가 주말에 니콜 본인과 이야기했다고 전했다.
5. 10-12 11:16 ET(한국 00:16, **마감 전**) 치폴레 **30.28달러(-4.15%)**, 스타벅스 92.13달러(+1.52%), S&P500 ETF 보합. **치폴레는 FT 보도 전날 종가 30.77달러보다 1.6% 아래다. 인수 웃돈은 0이고, 그 밑이다.**
6. 치폴레는 사상 최고 종가 68.55달러(2024-06-18)에서 **-56%**, 니콜이 떠난다고 발표하기 전날(2024-08-12, 55.87달러)에서 **-46%**. 같은 기간 스타벅스는 +20%.
7. 니콜 재임 중 치폴레 주가: 스타벅스 발표 자료는 "nearly 800%". 받은 시세로는 취임일 종가 6.40 → 55.87달러, **8.7배**.
8. 치폴레 동일매장 매출: 2025년 **-1.7%**(상장 뒤 첫 연간 감소라는 보도), 2025년에 가이던스를 세 번 낮춤. 2026년은 1분기 +0.5%, 2분기 +2.2%로 돌아섰고 7월에 가이던스를 올렸다. 그런데 주가는 8월 살모넬라(할라페뇨)로 하루 -9.7%, 9월 한 달 -16%.
9. 값: 올해 예상 이익의 **약 27배**, 내년 예상 이익의 약 22배(11:16 ET 가격). 맥도날드 18배, 스타벅스 36배. 치폴레의 5년 중간값은 51배(구루포커스, 재인용). 증권사 평균 목표가 약 44달러.
10. **다음 날짜: 치폴레 3분기 실적 10-28(수) 16:10 ET = 한국 10-29(목) 05:10**, 설명회 05:30. 회사가 준 3분기 동일매장 매출 가이던스는 약 +1%. 스타벅스는 10-29(목) 장 마감 뒤, 설명회 한국 10-30(금) 05:15.
11. 한국: 치폴레 아시아 1호점이 2026-09-02 강남역 10번 출구 근처에 열렸다. SPC(상미당홀딩스) 계열 빅바이트컴퍼니 51%, 치폴레 49%의 합작.

## 1. 시간표

| 날짜(미 동부) | 한국 시각 | 일 | 확인 |
|---|---|---|---|
| 2026-09-14(월) 저녁 | 09-15 아침 | 치폴레가 전 KFC CEO 사비르 사미를 이사로 선임 | [재인용] 세마포 09-15 |
| 09-15(화) 12:27 | 09-16 01:27 | 세마포 "Chipotle tries to get ahead of a potential activist problem" | [원문] F1 |
| 09-15(화) 장중 | | 치폴레 -5.94%(34.83달러). 확인된 회사 뉴스 없음 | [데이터], [원문] 24/7 월스트리트 |
| 09-28(월) | | 베타빌의 "uncooked" 알림으로 인수설. 장중 33.60달러(+7.2%), 종가 31.85달러(+1.66%), 거래량 3,144만 주. 인수자 이름 없음 | [데이터], [원문] parameter.io F3 |
| 09-28 주 ~ 10-02 | | 세마포(로한 고스와미): 치폴레가 인수 방어를 위해 은행을 고용 | [재인용] F2 |
| 10-05(월) | | 치폴레 -4.67%(30.85달러). 9월 말 인수설로 오른 것 소멸 | [데이터], [원문] 24/7 월스트리트 |
| 10-06(화) 08:11 | 10-06 21:11 | 세마포 "A Starbucks-Chipotle tie-up might be crazy enough to work" | [원문] F4 |
| 10-07(수) | | 치폴레 종가 30.77달러(FT 보도 전 마지막 종가) | [데이터] |
| **10-08(목)** 장중 | 10-09 새벽 | **FT 보도.** 정확한 게재 시각은 확인 못 함 | [재인용] F5 |
| 10-08(목) | | 스타벅스 "루머에 논평하지 않는다" 성명. 치폴레 무응답 | [원문] F6 |
| 10-09(금) | | 포춘: "두 주식이 보도 전 수준으로 돌아왔다" | [원문] F10 |
| 주말(10-10~11) | | 크레이머가 니콜과 이야기(CNBC 방송의 말) | [자막] F8 |
| **10-12(월) 09:01** | **10-12 22:01** | CNBC: 스타벅스 대변인이 크레이머에게 부인. 10:22 갱신 | [원문] F7 |
| 10-12 09:24 | 22:24 | NBC: 스타벅스 대변인이 이메일로 부인 | [요약도구] F7 |
| 10-12 11:16 | 10-13 00:16 | 치폴레 30.28달러 -4.15%, 스타벅스 92.13달러 +1.52% (**마감 전**) | [데이터] 나스닥 실시간 |

### 보도와 발언

- **F1.** 세마포 2026-09-15(로한 고스와미의 "View"): 치폴레가 이사회를 보강해 "potential activist scrutiny"에 대한 걱정을 누그러뜨리려 한다. 그때까지 외식업 경력이 있는 이사는 의장 스콧 모 한 명뿐이었다. 외식업 임원과 행동주의 방어 자문가들이 "치폴레가 행동주의 투자자를 맞게 될 것"이라고 사적으로 말했다. 까닭은 "the collapse in the company's multiple". 치폴레는 논평 요청에 답하지 않았다. **행동주의 투자자의 이름은 없다. "올 것 같다"는 관측이지 들어왔다는 보도가 아니다.** 소비자들이 치폴레류를 "slop bowls"라고 비웃는다는 대목도 있다. [원문] https://semafor.com/article/09/15/2026/chipotle-tries-to-get-ahead-of-a-potential-activist-problem
- **F2.** "치폴레가 자문사를 고용했다"의 출처: 세마포 10-06 기사가 스스로 "Semafor reported last week that Chipotle had tapped bankers to fend off a potential takeover"라고 적었다. 그 지난주 보도 자체는 찾지 못했다(세마포 사이트맵에 치폴레 기사는 09-15와 10-06뿐. 뉴스레터나 X 글로 보인다). Digg의 10-02 요약에 따르면 고스와미가 X에 인수 제안 가능성은 "highly doubtful"이지만 치폴레가 "potential activist or unwanted takeover"에 대비해 자문사를 고용한 것으로 안다고 썼다. [재인용] https://www.semafor.com/article/10/06/2026/a-starbucks-chipotle-tie-up-might-be-crazy-enough-to-work , https://digg.com/world-business/zag7dk3z . CNBC는 "Earlier in October, Semafor reported"라고 적었다(F7). **고용된 은행·자문사의 이름은 어느 보도에도 없다.**
- **F3.** 09-28 인수설: 베타빌(Betaville)의 "uncooked" 알림이 출처, 인수자 이름 없음, 치폴레 무응답. [원문, 2차 매체] https://parameter.io/chipotle-cmg-stock-jumps-4-amid-acquisition-rumors/ (이 매체는 "4% 상승"이라 적었으나 받은 시세의 종가는 +1.66%, 장중 고가 기준 +7.2%)
- **F4.** 세마포 10-06: 치폴레와 가까운 사람들은 "인수 제안을 받지 않았다"고 했다. 그런데 자꾸 나오는 가설이 스타벅스-치폴레 결합이다. 얌브랜드(KFC·피자헛·타코벨)처럼 따로 운영하고 부동산과 뒷단을 합치는 꼴. 니콜은 얌에서 10년 넘게 일했다. 걸림돌: 스타벅스는 낮은 배수로 다시 매겨질 것이고 신주를 찍어야 할 것. 스타벅스는 논평 거절, 치폴레 무응답. **FT보다 이틀 먼저 스타벅스의 이름을 꺼낸 것은 세마포다.** [원문] 위 URL
- **F5.** FT 2026-10-08(목): 스타벅스가 최근 몇 달 자문사들과 치폴레 인수 제안을 준비해 왔다. 사정을 아는 사람들 인용. 제안의 상태와 정식 제안 여부는 확인되지 않음. 초기 단계이고 규모 때문에 성사되지 않을 수 있다. 치폴레 시가총액 410억 달러. 니콜이 치폴레를 다시 이끄는 안이 들어 있다(SBS Biz·연합의 옮김). **FT 원문은 유료라 읽지 못했다.** [재인용] PYMNTS https://www.pymnts.com/?p=4290504 , CBS https://www.cbsnews.com/news/chipotle-stock-starbucks-takeover-ceo-brian-niccol/ , SBS Biz https://biz.sbs.co.kr/amp/article/20000339100 . 자문사 이름은 보도되지 않았다. 인베스팅닷컴이 옮긴 씨티 노트 기사 하나만 FT 보도를 "수요일"이라 적었다(다른 매체는 전부 목요일).
- **F6.** 스타벅스의 첫 반응(10-08): "As a matter of policy, we don't comment on rumors and speculation. Our team is laser focused on executing our Back to Starbucks strategy. We have strong momentum and confidence in our long-term growth potential. We look forward to sharing our Q4 results, including FY27 guidance, later this month." [원문] PYMNTS(위), CBS(위), NRN https://www.nrn.com/mergers-acquisitions/starbucks-is-reportedly-eyeing-a-chipotle-acquisition (세 매체 문구 일치)
- **F7.** **부인(10-12).**
  - CNBC 09:01 ET 게재, 10:22 갱신: "Starbucks is not buying Chipotle," a Starbucks spokesperson told CNBC's Jim Cramer. 부인문은 이 한 문장이다. CNBC 기사에는 대변인의 이름이 없다. [원문] https://www.cnbc.com/2026/10/12/starbucks-denies-chipotle-takeover.html
  - NBC 09:24 ET(스티브 코팩): 대변인이 NBC에 이메일로 "we want to be clear we are not buying Chipotle", 회사는 "laser focused on executing our Back to Starbucks strategy". [요약도구] https://www.nbcnews.com/business/consumer/starbucks-not-buying-chipotle-rcna602968
  - 인베스팅닷컴은 같은 문장을 "CNBC와 블룸버그 뉴스에 따르면"으로 옮겼다. [요약도구] https://www.investing.com/news/stock-market-news/not-buying-chipotle-starbucks-squashes-blockbuster-acquisition-speculation-4944539
- **F8.** CNBC 방송(10-12, "Market Open" 묶음 영상 00:35~01:34): 진행자 "CNBC Mad Money host Jim Cramer chatted with the Starbucks CEO Brian Niccol over the weekend". 크레이머(데이비드 파버와): "Can confirm that Starbucks is not going to buy Chipotle. They're not interested…", "let's just put that to bed, move on". 니콜의 말을 옮기며 "our turn is real and the numbers are real and we don't want to derail anything". [자막] https://www.youtube.com/watch?v=BucZl6rytG0 . **니콜 본인이 카메라 앞에서 한 말은 찾지 못했다.** 크레이머가 옮긴 말이고 자동 자막이라 게시 전에 귀로 확인해야 한다.
- **F9.** 치폴레 쪽의 말: 없다. CNBC, NBC, CBS, 포춘, PYMNTS, 세마포 모두 "응답하지 않았다". 치폴레 뉴스룸의 10월 보도자료는 10-05 채소 오케스트라 건이 마지막이다. [원문] https://newsroom.chipotle.com/press-releases
- **F10.** 포춘 10-09(필 와바): 치폴레는 목요일 장중 8%까지 올랐다가 "roughly where they were before the article"로 돌아왔다. 시장은 성사 가능성이 낮다고 결론 냈다. 시가총액 약 400억 달러에 통상의 웃돈 20%를 얹으면 500억 달러, 스타벅스 기업가치의 절반. 윌리엄 블레어가 본 절감액은 연 약 3억 달러. 니콜은 다른 브랜드를 합쳐 본 경험이 거의 없다. [원문] https://fortune.com/2026/10/09/chipotle-starbucks-niccol-stock/
- **F11.** 행동주의 투자자: **이름이 보도된 곳을 찾지 못했다.** 댄 로브의 서드포인트가 2025년 4분기에 치폴레 약 475만 주(약 1억 7,480만 달러)를 샀다는 13F 보도는 있으나 요구를 내걸었다는 보도는 없다. [검색요약] https://finviz.com/news/320584/billionaire-investor-bets-on-chipotle-while-stock-trades-near-52-week-low . 치폴레는 2025년 연간 실적 자료의 위험 문구에 "the potential impact of activist shareholder actions or tactics"를 적어 두었다. [원문] F30의 자료. 과거: 2016년 빌 애크먼의 퍼싱스퀘어가 9.9%를 사고 치폴레가 골드만삭스·모건스탠리 등을 고용했다. [원문] NRN 2016-10-28 https://www.nrn.com/mergers-acquisitions/chipotle-girds-for-battle-with-activist

## 2. 주가

출처는 전부 나스닥 API 일별 종가 [데이터]. 치폴레는 2024-06-26에 50대 1 액면분할을 했고(분할 날짜는 [기억]) 아래 값은 분할 반영 값이다.

### 보도 전후(달러)

| 날짜 | CMG 종가 | 등락 | 거래량 | SBUX 종가 | 등락 | S&P500 ETF |
|---|---|---|---|---|---|---|
| 09-14 | 37.03 | +2.29% | 991만 | 99.07 | +0.33% | |
| 09-15 | 34.83 | **-5.94%** | 1,999만 | 96.58 | -2.51% | -0.46% |
| 09-25 | 31.33 | -2.12% | 1,334만 | 94.86 | | |
| 09-28 | 31.85 | +1.66%(고가 33.60) | 3,144만 | 95.27 | +0.43% | -0.74% |
| 10-02 | 32.36 | +0.12% | 1,508만 | 94.71 | -0.18% | |
| 10-05 | 30.85 | **-4.67%** | 2,362만 | 94.43 | -0.30% | +0.67% |
| 10-06 | 30.90 | +0.16% | 1,776만 | 96.11 | +1.78% | |
| 10-07 | **30.77** | -0.42% | 1,294만 | 93.58 | -2.63% | -0.24% |
| **10-08** | **32.68** | **+6.21%**(고가 33.40, 저가 30.46) | **7,204만** | 93.21 | -0.40%(저가 **87.35**) | -0.42% |
| 10-09 | 31.59 | -3.34% | 2,009만 | 90.75 | -2.64% | +0.60% |
| 10-12 11:16 ET | 30.28 | -4.15%(장중 30.05~31.17) | 981만(진행 중) | 92.13 | +1.52% | -0.02% |

- **F12.** 10-08 치폴레: 장중 고가 33.40달러는 전날 종가 대비 +8.5%. 종가 +6.21%. 거래량 7,204만 주는 09-01~10-07 평균 1,429만 주의 5.0배. 스타벅스는 장중 저가 87.35달러(-6.7%)에서 93.21달러로 되돌아와 -0.40%. [데이터]. 블룸버그는 장중 +8.6%, -6.7%로 보도(스타벅스는 1년여 만의 가장 큰 장중 하락). [재인용] TIKR https://www.tikr.com/blog/chipotle-stock-jumped-6-on-a-starbucks-takeover-report-its-q3-guide-counted-one-food-scare-and-left-out-another
- **F13.** 그날 시장: S&P500 ETF(SPY)는 10-08 -0.42%, 10-09 +0.60%, 10-12 장중 보합. 10-12 같은 시각 맥도날드 -0.25%, 얌브랜드 +0.49%. 치폴레의 움직임은 치폴레만의 것이다. [데이터]
- **F14.** **인수 웃돈이 얼마나 남았나.** FT 전 종가 30.77 → 10-08 종가 32.68(+1.91달러) → 10-09 31.59(남은 것 +0.82달러) → 10-12 11:16 ET 30.28(**-0.49달러, -1.6%**). 베타빌 인수설 전 종가(09-25) 31.33달러와 견줘도 -3.4%. **웃돈은 남아 있지 않고, 인수설이 나오기 전보다 싸다.** [데이터]
- **F15.** 10-12 시세는 마감 전 값이다(11:16 ET). 장중 범위 치폴레 30.05~31.17, 스타벅스 90.71~92.27. 종가는 한국 10-13 05:00 뒤에 다시 받아야 한다. 매체가 본 시각의 값: CNBC "nearly 4%" 하락·스타벅스 +1%, 벤징가 09:50 ET -4.02%(30.33달러), 24/7 월스트리트 30.55달러(-3%), 야후·쿼츠 개장 전 -2% 넘게.

### 긴 흐름

- **F16.** 치폴레 사상 최고: 종가 **68.55달러(2024-06-18)**, 장중 69.26달러(같은 날). 분할 전 값으로 약 3,428달러. [데이터] 10-09 종가는 여기서 -53.9%, 10-12 11:16 ET는 -55.8%.
- **F17.** **2024-08-13(니콜 이직 발표일)**: 치폴레 55.87 → 51.68달러 **-7.50%**, 스타벅스 77.03 → 95.90달러 **+24.50%**. 그날 SPY +1.64%. [데이터]
- **F18.** 그 뒤:

  | 기준 | CMG | SBUX |
  |---|---|---|
  | 2024-08-12 종가 → 2026-10-09 종가 | 55.87 → 31.59, **-43.5%** | 77.03 → 90.75, **+17.8%** |
  | 2024-08-12 종가 → 10-12 11:16 ET | -45.8% | +19.6% |
  | 2024-08-13 종가 → 2026-10-09 종가 | -38.9% | -5.4% |
  | 니콜 스타벅스 취임 전 종가(2024-09-06, 91.15) → 10-09 | | -0.4% |

  NRN은 10-07 종가 기준으로 치폴레 -45%, 스타벅스 +21.5%라 적었다. [원문] NRN(F6). CBS와 로이터는 "약 50%", "거의 절반". 세마포는 스타벅스 주가가 니콜 취임 뒤 "flat"이라 적었다(F4). **스타벅스가 오른 것은 거의 전부 발표 당일 하루의 +24.5%다.** [데이터]
- **F19.** 치폴레 연간: 2024년 +31.8%(45.74 → 60.30), **2025년 -38.6%**(60.30 → 37.00), 2026년 10-09까지 **-14.6%**(37.00 → 31.59), 10-12 11:16 ET까지 -18.2%. 스타벅스: 2024년 -5.0%, 2025년 -7.7%, 2026년 10-09까지 +7.8%. [데이터]
- **F20.** 치폴레의 바닥들: 2025-11-11 장중 29.75달러, **2026-06-04 장중 28.035달러(52주 최저)**. 52주 최고는 2025-10-15의 42.815달러. 지금 가격은 52주 최저에서 8% 위다. [데이터]
- **F21.** 치폴레 월말 종가: 2024-12 60.30 / 2025-03 50.21 / 06 56.15 / 07 42.88 / 09 39.19 / 10 31.69 / 12 37.00 / 2026-01 38.87 / 03 32.01 / 06 34.00 / 07 37.22 / 08 38.03 / 09 31.95. [데이터] 2026년 9월 한 달 -16.0%.
- **F22.** 실적 다음 날 등락: 2025-07-24 -13.3%, **2025-10-30 -18.2%**, 2026-02-04 +1.9%, 2026-04-30 +3.0%, **2026-07-30 +12.5%**. 살모넬라 날 2026-08-04 **-9.72%**. [데이터]

## 3. 브라이언 니콜

- **F23.** 치폴레 재임: 2018년 3월~2024년 8월. 타코벨 CEO에서 옮겼다. 선임 발표 다음 날(2018-02-14) 치폴레는 5.03 → 5.80달러, **+15.4%**. [데이터]. 취임일을 03-05로, 선임 발표를 02-13 장 마감 뒤로 적은 것은 [기억]이다.
- **F24.** 재임 중 주가:
  - 출처 있는 숫자: 스타벅스가 2024년 8월 선임 자료에서 "매출 거의 두 배, 이익 거의 7배, 주가 거의 800%"라고 했다. [재인용] PYMNTS(F5). 세마포 "a near 800% share price surge"(F4). 포춘 "연 매출을 100억 달러로 두 배"(F10).
  - 계산값: 2018-03-05 종가 6.40 → 2024-08-12 종가 55.87달러, **8.73배(+773%)**. 선임 발표 전 종가(2018-02-13, 5.03달러)에서는 11.1배. [데이터]
- **F25.** 그 전 사건: 2015년 대장균 사태. 치폴레 주가는 2015-10-13 757달러(분할 전) → 2016년 2월 초 475달러(-37%). 2015년 4분기 동일매장 매출 -14.6%(2006년 상장 뒤 첫 감소). 2016년 1분기 -29.7%, 3분기 -21.9%. [검색요약] CNN머니 2016-02-02 https://money.cnn.com/2016/02/02/investing/chipotle-earnings-e-coli/ , [원문] NRN 2016-10-28(F11). 니콜이 오기 직전 종가 5.03달러는 분할 전 약 251달러다. [데이터]
- **F26.** 스타벅스가 준 보수: 2024-08-14 발표. 합계 약 **1억 1,300만 달러**: 사인온 보너스 1,000만, 지분 7,500만, 2025회계연도부터 해마다 최대 2,300만 달러어치. 연봉 160만, 현금 보너스 360만~720만 달러. 시애틀 본사로 이사하지 않아도 되고 캘리포니아 뉴포트비치에 작은 사무실을 회사 돈으로 차려 주며 회사 비행기로 통근한다. [원문] 포춘 2024-08-14 https://fortune.com/2024/08/14/starbucks-ceo-brian-niccol-113-million-payday-remote-work . 공시된 보수는 2024회계연도 9,600만, 2025회계연도 3,100만 달러. [검색요약] 블룸버그 2026-01-27
- **F27.** 스타벅스에서의 성과("Back to Starbucks", 취임 이틀째인 2024년 9월에 내건 구호):

  | 분기 | 세계 동일매장 매출 | 북미·미국 | 영업이익률(조정) | 확인 |
  |---|---|---|---|---|
  | FY26 1분기(2025-12 끝) | +4%(거래 +3%) | +4% | 10.1%(-180bp) | [원문] |
  | FY26 2분기(2026-03 끝) | +6.2%(거래 +3.8%) | 북미 +7.1% | | [원문] |
  | **FY26 3분기(2026-06-28 끝)** | **+7.9%**(거래 +4.2%, 객단가 +3.5%) | 미국 +7.9%, 북미 +8.1% | **14.4%(+430bp)** | [요약도구] |

  3분기 조정 EPS 0.85달러(+70%), 매출 93억 달러(-1.4%, 중국 사업 구조 변경 영향). 보도자료 제목이 "네 분기 연속 동일매장 성장, 두 분기 연속 이익률 확대". 2026회계연도 가이던스: 미국 동일매장 6.0%를 조금 웃돎, 조정 EPS 2.55~2.65달러. [요약도구] https://investor.starbucks.com/news/financial-releases/news-details/2026/Starbucks-Reports-Q3-Fiscal-Year-2026-Results/default.aspx , [원문] 1·2분기 자료(같은 사이트). 쿼츠는 조정 영업이익률 14.4%가 2년 전의 16.7%보다 낮다고 짚었다. [요약도구] 야후(쿼츠) https://finance.yahoo.com/markets/stocks/articles/starbucks-denies-chipotle-acquisition-sending-132658555.html
- **F28.** 중국: 스타벅스는 중국 사업의 과반을 보위캐피털에 넘겼고(2026년 4월 완료, 지분 40% 유지) 처분 이익 5억 3,630만 달러를 냈다. [요약도구] 위 3분기 자료. 포춘은 이를 "복잡함을 덜어낸 것"으로 보고, 치폴레 인수는 그 반대라고 했다(F10).
- **F29.** 2026-09-10 니콜이 직원들에게 "Starbucks is back. Our business has made the turn"이라는 메모를 보냈고 CNBC에 나와 "the shine is back on Starbucks"라고 했다. 진행자: 취임일 대비 주가 약 +10%, 선임 발표일 대비 +30%. [자막] https://www.youtube.com/watch?v=kJxONRGhEPs . **그 한 달 뒤 인수설이 나왔다.** 인수설에 대한 니콜 본인의 공개 발언은 없다(F8의 크레이머 전언뿐).

## 4. 치폴레의 지금

- **F30.** 동일매장 매출(회사 보도자료):

  | 분기 | 동일매장 매출 | 거래 건수 | 그때의 연간 가이던스 | 확인 |
  |---|---|---|---|---|
  | 2024년 연간 | +7.4% | +5.3% | 2025년: "low to mid-single digit" 성장 | [원문] |
  | 2025 1분기(04-23 발표) | -0.4% | -2.3% | "low single digit" 성장으로 **1차 하향** | [원문] |
  | 2025 2분기(07-23) | **-4.0%** | -4.9% | "About flat"으로 **2차 하향** | [원문] |
  | 2025 3분기(10-29) | +0.3% | -0.8% | "low-single digit" 감소로 **3차 하향** | [원문] |
  | 2025 4분기(2026-02-03) | -2.5% | -3.2% | 2026년: "about flat" | [원문] |
  | **2025년 연간** | **-1.7%** | -2.9% | | [원문] |
  | 2026 1분기(04-29) | +0.5% | +0.6% | "about flat" 유지 | [원문] |
  | **2026 2분기(07-29)** | **+2.2%** | +1.0% | "low single digit" 성장으로 **상향** | [요약도구] |

  원문: https://ir.chipotle.com/2025-02-04-CHIPOTLE-ANNOUNCES-FOURTH-QUARTER-AND-FULL-YEAR-2024-RESULTS , https://ir.chipotle.com/2025-04-23-CHIPOTLE-ANNOUNCES-FIRST-QUARTER-2025-RESULTS , https://ir.chipotle.com/2025-07-23-CHIPOTLE-ANNOUNCES-SECOND-QUARTER-2025-RESULTS , https://ir.chipotle.com/2025-10-29-CHIPOTLE-ANNOUNCES-THIRD-QUARTER-2025-RESULTS , https://ir.chipotle.com/2026-02-03-CHIPOTLE-ANNOUNCES-FOURTH-QUARTER-AND-FULL-YEAR-2025-RESULTS , https://newsroom.chipotle.com/2026-04-29-CHIPOTLE-ANNOUNCES-FIRST-QUARTER-2026-RESULTS , 2분기는 SEC 8-K https://www.sec.gov/Archives/edgar/data/0001058090/000105809026000063/cmg-20260729xex991.htm
- **F31.** 2025년 -1.7%는 2016년 뒤 첫 연간 감소(QSR, 재인용: https://news.piratesandprincesses.net/p/starbucks-explored-buying-chipotle). 세마포는 "for the first time in decades"라고 적었다(F1). 두 표현이 다르다. 2016년에 크게 줄었으므로 QSR 쪽이 맞아 보인다(작업자의 해석).
- **F32.** 2026년 2분기(06-30 끝): 매출 33억 달러(+9.3%), 조정 EPS 0.33달러(전년과 같음), 영업이익률 15.7%(전년 18.2%), 매장 이익률 25.2%(전년 27.4%), 디지털 비중 38.3%, 새 매장 100곳. 보트라이트: "Our positive results reflect the momentum we're building as our Recipe for Growth strategy continues to take shape". [요약도구] 위 8-K
- **F33.** 이익이 눌리는 까닭(회사 자료의 말): 2025년 4분기와 연간 자료가 "inflation, primarily in beef and chicken"과 "the impact from tariffs enacted in 2025", 임금 상승, 거래 감소를 적었다. 2026년 1분기 자료는 "inflation, primarily in beef and freight". 1분기 영업이익률 12.9%(전년 16.7%), 조정 EPS 0.24달러(-17.2%). [원문] F30의 자료
- **F34.** 2025년에 왜 빠졌나: 2025-10-29 3분기 발표에서 가이던스를 세 번째로 낮추고 다음 날 -18.2%(블룸버그 제목 "Falls Most Since 2012"). 보트라이트는 25~35세의 지출이 크게 줄었고 모든 소득층에서 방문 빈도가 줄었다고 했다. [검색요약] TIKR https://www.tikr.com/blog/chipotle-nyse-cmg-stock-tanks-19-on-lower-forecast-and-sluggish-consumer-spending , [데이터]. 2026-02 발표에서는 핵심 고객의 약 60%가 가구 소득 10만 달러 이상이라고 했다. [검색요약] 모틀리풀 녹취
- **F35.** 2026년 여름 식품 안전 두 건:
  - 사이클로스포라(상추 관련, 업계 전반): 치폴레 메뉴에 든 재료는 아니었다고 보트라이트가 말했다. 3분기 가이던스 약 +1%에 약 200bp의 역풍으로 반영. CDC가 09-11에 종료 선언.
  - 살모넬라(할라페뇨): 08-04에 치폴레가 할라페뇨를 뺐고 주가 -9.72%. 미네소타 환자 84명 가운데 75명이 치폴레에서 먹었다고 답했다. 회사는 다음 날 공시에서 "our guidance did not include a financial impact from these matters". **3분기 가이던스 +1%에 살모넬라는 들어 있지 않다.** [원문, 2차 매체] TIKR(F12의 URL), 24/7 월스트리트 2026-09-15 https://247wallst.com/investing/2026/09/15/chipotle-falls-5-profit-taking-after-a-strong-month-or-the-salmonella-headline-again/ , [데이터]
- **F36.** CFO 애덤 라이머(07-29 설명회): 새 매장 생산성 "in the 80% range", 2년 차 현금 수익률 "around 60%", 북미만 7,000곳 이상 가능. 매장은 06-30 기준 4,200곳 넘음. 보트라이트: "we have taken share in each month of 2026". [재인용] TIKR(F12의 URL)
- **F37.** 자사주: 치폴레는 2025년에 24억 달러어치를 평균 **42.54달러**에, 2026년 1분기에 7억 80만 달러어치를 36.14달러에, 2분기에 6억 3,070만 달러어치를 **32.55달러**에 샀다. 06-11에 13억 달러를 더 승인해 06-30 기준 17억 달러가 남았다. **지금 주가(30.28)는 회사가 최근 1년 반 동안 산 어느 분기의 평균가보다 낮다.** [원문] F30의 자료, [요약도구] 2분기 8-K. 씨티: 치폴레는 빚이 없고 현금을 번다(F45).
- **F38.** 시가총액: 나스닥 382억 9천만 달러(10-12 장중), 24/7 월스트리트 381억 4천만 달러(얌브랜드 396억, 맥도날드 1,652억, 스타벅스 1,044억 달러). [데이터], [원문] https://247wallst.com/investing/2026/10/12/chipotle-slides-3-as-starbucks-rules-out-acquisition-starbucks-stock-rises-while-mcdonalds-stock-slips/ . **치폴레의 시가총액이 타코벨·KFC의 얌브랜드보다 작아졌다.**
- **F39.** PER(10-12 11:16 ET 가격, 나스닥이 싣는 잭스 컨센서스로 계산):

  | | 가격 | 올해 예상 EPS | 배수 | 내년 예상 EPS | 배수 |
  |---|---|---|---|---|---|
  | 치폴레 | 30.28 | 2026년 1.14 | **26.6배** | 2027년 1.36 | **22.3배** |
  | 스타벅스 | 92.13 | 2026-09 회계 2.59 | 35.6배 | 2027-09 회계 3.16 | 29.2배 |
  | 맥도날드 | 234.64 | 2026년 12.85 | 18.3배 | 2027년 13.70 | 17.1배 |

  [데이터] https://api.nasdaq.com/api/analyst/CMG/earnings-forecast (애널리스트 15명). 지난 네 분기 조정 EPS 합(0.29+0.25+0.24+0.33 = 1.11달러) 기준으로는 27.3배. 2025년 조정 EPS는 1.17달러였고 2026년 예상 1.14달러는 그보다 적다: **올해 이익은 줄어드는 해다.**
  - 다른 출처: TIKR은 10-08 기준 앞으로 12개월 이익의 약 26배(2025년 말 약 32배), 맥도날드 약 18배, 스타벅스 약 32배. 앞으로 12개월 EPS 예상은 2025년 말 약 1.16 → 약 1.27달러로 올랐는데 주가는 37.00 → 32.68달러로 내렸다. [원문, 2차 매체] TIKR(F12의 URL)
  - 과거와 견줌: 구루포커스의 5년 PER 중간값 51.35배, 09-28 기준 29.76배. [재인용] parameter.io(F3). 구루포커스 원 페이지는 못 봤다.
- **F40.** 목표가: 평균 43.76달러(06-30의 42.88달러에서 조금 오름), 매수·비중확대 의견 24곳(26곳에서 줄어듦). 나스닥 1년 목표가 44.00달러. 씨티 매수·45달러. [원문, 2차 매체] TIKR, [데이터] 나스닥, [원문, 2차 매체] https://www.tradingpedia.com/2026/10/09/citi-sees-logic-in-potential-starbucks-chipotle-deal/ . 평균 목표가는 지금 가격보다 약 45% 위다(계산값).
- **F41.** 3분기 컨센서스: EPS 약 0.29달러(전년과 같음), 4분기 0.28달러. [데이터] 나스닥
- **F42.** **다음 실적 발표.**
  - 치폴레 3분기: **2026-10-28(수)** 자료 약 16:10 ET = **한국 10-29(목) 05:10**, 설명회 16:30 ET = 한국 05:30. [원문] https://newsroom.chipotle.com/2026-09-01-CHIPOTLE-MEXICAN-GRILL-TO-ANNOUNCE-THIRD-QUARTER-2026-RESULTS-ON-OCTOBER-28,-2026
  - 스타벅스 4분기·연간: **2026-10-29(목)** 장 마감 뒤, 설명회 13:15 PT = 16:15 ET = **한국 10-30(금) 05:15**. 2027회계연도 가이던스를 같이 낸다. [원문] https://investor.starbucks.com/news/financial-releases/news-details/2026/Starbucks-Announces-Q4-and-Full-Fiscal-Year-2026-Results-Conference-Call/default.aspx (10-08 발표: FT 보도와 같은 날이다)
- **F43.** 보트라이트의 전략 이름은 "Recipe for Growth"(2026-02-03 발표). 2024-11-11에 정식 CEO가 됐다. [원문] F30의 자료, 치폴레 뉴스룸 목록

## 5. 애널리스트들이 이번 건에 한 말

- **F44.** 규모: 지금까지 가장 큰 외식업 인수는 2014년 버거킹의 팀호턴스 **114억 달러**(멜리어스 리서치를 인용한 CBS, NRN). NRN은 물가를 반영하면 약 160억 달러라고 했다. 윌리엄 블레어는 웃돈을 얹으면 **500억 달러** 가까이로 봤다(QSR 재인용). 114억의 네 배가 넘는다. 스타벅스 시가총액은 약 1,070억 달러(로이터·LSEG 재인용)라 500억은 그 절반. [원문] CBS, NRN, 포춘
- **F45.** 씨티 존 타워(매수, 목표가 45달러): 말이 되는 근거는 경영진("The clear anchor to why this would make any sense is management"), 스타벅스의 해외 라이선스망, 치폴레의 무차입. 그러나 투자자 대부분은 성사를 기대하지 않는다. 규모와 금리 때문에 스타벅스 주주에게 희석. 치폴레가 스타벅스의 노조 문제에 노출될 수 있다. [원문] 포춘(F10), [원문, 2차 매체] tradingpedia(F40)
- **F46.** TD 코웬 앤드루 찰스: "a low-probability outcome at this stage". 400억 달러 인수는 Back to Starbucks와 "inconsistent". [원문] CBS(F5)
- **F47.** BTIG 피트 살레: 인수는 자금 조달, 통합, 조직, 시스템, 인사에 경영진의 시간을 크게 잡아먹을 수 있다. [원문] 포춘(F10)
- **F48.** RBC 로건 라이히: "The strategic rationale … isn't apparent to us given limited overlap between the businesses". [원문] NRN(F6)
- **F49.** 윌리엄 블레어 샤론 잭피아: 스타벅스 재팬을 팔아 돈을 댈 수 있다. 그런 인수는 경영진이 스타벅스의 성장에 자신이 덜하다는 신호일 수 있다. 연 절감액 약 3억 달러. [원문] NRN, 포춘
- **F50.** 멜리어스 제이컵 에이킨-필립스: "It's not like Starbucks has a grill". [재인용] 블룸버그 → piratesandprincesses(F31의 URL). 시포트 리서치: 시너지가 까닭이 아니라면 "니콜이 지금 경영진과 무엇을 다르게 할 것인가"가 물음이다. [원문] CBS
- **F51.** 블룸버그 인텔리전스 마이클 헤일런(10-08 블룸버그TV): 니콜은 치폴레를 잘 알고 매출을 두 번째로 되살릴 적임자다. "Scott Boatwright, the current CEO, has not done a very good job replacing Brian Niccol". 그러나 시너지는 많지 않고 스타벅스 경영진에 부담. [자막] https://www.youtube.com/watch?v=ApNx2JacfcI
- **F52.** 24/7 월스트리트 10-12: 강세 논리는 "스타벅스만 한 회사가 들여다봤다는 것 자체가 눌린 주가에 반영 안 된 값이 있다는 뜻", 약세 논리는 "웃돈이 빠졌고 아직 오지 않은 방문객 회복에 기대 서 있다". 치폴레는 매장을 전부 직영해 방문객이 줄면 이익이 바로 준다(맥도날드·얌은 가맹 수수료를 받는다). [원문] F38의 URL

## 6. 한국과 닿는 점

- **F53.** 치폴레 아시아 1호점 "치폴레 강남점"이 **2026-09-02** 문을 열었다. 강남역 10번 출구 근처, 96석, 옆이 쉐이크쉑. 운영은 합작법인 에스앤씨레스토랑홀딩스(상미당홀딩스 계열 빅바이트컴퍼니 **51%**, 치폴레 본사 **49%**). 한국과 싱가포르 사업을 맡는다. 전부 직영. 연내 2·3호점, 2027년 상반기 싱가포르. 치폴레가 현지 기업과 합작으로 새 지역에 나간 것은 처음. 메뉴는 12,800원부터. [원문] 머니투데이 2026-09-02 https://www.mt.co.kr/living/2026/09/02/2026090111210726646 , 비즈워치 2026-09-01 https://news.bizwatch.co.kr/article/consumer/2026/09/01/0013 (가격은 [검색요약])
- **F54.** 09-01 강남점 기자간담회에 스콧 보트라이트 CEO가 와서 허희수 상미당홀딩스 CVO와 악수했다. 보트라이트: "(치폴레 한국은) 아시아 전역에서 치폴레가 어떻게 성장할 지에 대한 기준점이 될 것". [원문] 비즈워치, 머니투데이(사진 있음). **실물: 보트라이트가 서울에 온 사진이 한국 기사에 있다.**
- **F55.** 한국어 기사: SBS Biz(연합) 2026-10-09 07:36 "FT '스타벅스, 치폴레 인수 검토…성사시 외식부문 역대 최대'"(시가총액 390억 달러, 약 52조 원. 합치면 매출 500억 달러 가까이, 스타벅스 4만 1천 점포). [원문] F5의 URL. **부인을 다룬 한국어 기사는 조사 시각에 검색되지 않았다.**
- **F56.** 스타벅스코리아는 미국 본사 소유가 아니다(이마트가 최대주주). [기억] 확인하지 않았으니 쓰려면 다시 찾는다.

## 7. 판단의 재료: 인수설이 꺼진 치폴레, 지금 사도 되나

### 사는 쪽의 근거

1. **인수 웃돈이 없다.** 지금 값은 FT 보도 전날보다 1.6% 싸고 9월 말 인수설 전보다 3.4% 싸다(F14). 인수설을 보고 산 값이 아니다.
2. **값이 내려와 있다.** 사상 최고에서 -56%, 52주 최저(28.035달러)에서 8% 위(F16, F20). 올해 이익의 27배, 내년 이익의 22배. 5년 중간값 51배의 절반(F39).
3. **장사는 돌아서는 중이다.** 동일매장 매출이 -4.0%(2025년 2분기)에서 +2.2%(2026년 2분기)로, 거래 건수도 두 분기 연속 늘었고 7월에 가이던스를 올렸다(F30).
4. **회사가 자기 주식을 더 비싸게 사 왔다.** 2분기 평균 32.55달러, 남은 한도 17억 달러. 빚이 없다(F37).
5. **누군가 들여다봤다.** FT 보도가 맞다면 스타벅스가 몇 달을 검토했고, 회사는 은행을 고용했고, 행동주의 투자자가 올 거라는 관측이 있다(F1, F2, F5). 주가가 더 빠지면 다시 표적이 된다.
6. 증권사 평균 목표가 약 44달러(+45%)(F40).

### 안 사는 쪽의 근거

1. **부인 뒤 살 사람이 한 명 줄었다.** 500억 달러를 낼 수 있는 외식 회사는 손에 꼽는다. 행동주의 투자자는 이름조차 없다(F11).
2. **올해 이익은 줄어든다.** 2026년 예상 EPS 1.14달러는 2025년의 1.17달러보다 적다. 매장 이익률이 27.4% → 25.2%로 내려왔다. 쇠고기·운임·관세·임금(F32, F33, F39).
3. **3분기 가이던스가 낮고 구멍이 있다.** 동일매장 +1%인데 살모넬라의 영향은 넣지 않았다. 3분기는 전년 비교도 가장 어렵다(F35).
4. **맥도날드보다 여전히 비싸다.** 치폴레 27배, 맥도날드 18배(F39). "싸졌다"는 치폴레의 과거와 견준 말이다.
5. **인수설이 없던 9월에도 한 달 -16%였다.** 09-15 -5.9%, 10-05 -4.7%는 뉴스 없이 빠진 날이다(1절 표). 지금 블룸버그 인텔리전스는 CEO를 공개적으로 낮게 평가한다(F51).
6. 직영이라 방문객이 줄면 이익이 그대로 준다(F52).

### 전례: 인수설이 꺼진 뒤

- **F57.** **파파존스(PZZA)**: 2025-10-13~14 아폴로의 인수 제안 보도로 +9.7%, +6.7%(41.59 → 48.68달러). 2025-11-04 "아폴로가 제안을 거뒀다"는 보도에 -10.0%, 다음 날 -5.1%(48.29 → 41.26달러). **인수설 전 가격(41.59)으로 이틀 만에 돌아갔고, 그 뒤 계속 내려 2026-10-09 종가는 19.75달러다(-59%).** [데이터] 나스닥 API, [원문, 제목과 첫 문장] 시킹알파 2025-11-04 https://seekingalpha.com/news/4514763-papa-johns-falls-on-report-apollo-has-withdrawn-takeover-offer . 부인이 아니라 철회 보도라는 점이 다르다. 그 뒤 하락의 까닭(실적)은 조사하지 않았다.
- **F58.** **도미노피자 엔터프라이즈(호주, DMP)**: 2025년 10월 말 호주 파이낸셜리뷰가 베인캐피털의 최대 40억 호주달러 인수 검토를 보도하자 장중 +23%(19호주달러). 회사가 "제안도 접촉도 없었다"고 공시하자 대부분 반납. 종가는 매체마다 다르다(로이터·인사이드리테일 16.02호주달러 +3.7%, 블룸버그 오후 16.53호주달러). [검색요약] https://insideretail.com.au/business/dominos-refutes-report-of-4bn-takeover-offer-from-bain-capital-202510 . 야후 시세로는 그 뒤 한 달 동안 올라 11-28 21.38호주달러, 2026-04-30 16.47, 2026-10-12 21.90호주달러. [데이터] 야후 차트 API(날짜 하루 어긋날 수 있음). **부인 뒤에도 오른 사례다.** 까닭은 조사하지 않았다.
- 두 전례는 방향이 반대다. 공통점은 하나: **부인·철회 직후 주가는 인수설 전 가격 근처로 돌아간다. 그 다음은 장사가 정한다.** (작업자의 해석)

### 판단을 가를 날짜와 숫자

- **10-28(한국 10-29 05:10) 3분기 실적.** 동일매장 매출이 가이던스 +1%를 넘는가(TIKR은 사이클로스포라 영향을 빼면 바탕은 3% 근처라는 CFO의 확인을 인용, F35), 살모넬라의 영향이 얼마였나, 연간 가이던스 "low single digit"을 지키는가, 매장 이익률 25.2%에서 더 내려가는가.
- 틀리는 경우의 선: 52주 최저 28.035달러(2026-06-04). 지금에서 -7.4%.
- 위쪽의 선: FT 보도일 종가 32.68달러, 회사의 2분기 자사주 평균가 32.55달러, 평균 목표가 약 44달러.

## 8. 쓸 수 있는 말(대독 후보)

| # | 누가 | 말(원문) | 날짜 | 출처 | 확인 |
|---|---|---|---|---|---|
| Q1 | 스타벅스 대변인 → CNBC 짐 크레이머 | "Starbucks is not buying Chipotle." | 2026-10-12 | CNBC(F7) | [원문] |
| Q2 | 스타벅스 대변인 → NBC(이메일) | "we want to be clear we are not buying Chipotle" | 2026-10-12 | NBC(F7) | [요약도구] |
| Q3 | 스타벅스 대변인(첫 반응) | "As a matter of policy, we don't comment on rumors and speculation." | 2026-10-08 | CBS, PYMNTS, NRN | [원문] |
| Q4 | 짐 크레이머(CNBC 방송) | "Can confirm that Starbucks is not going to buy Chipotle." / "let's just put that to bed, move on" | 2026-10-12 | 유튜브 BucZl6rytG0 00:54~01:13 | [자막] |
| Q5 | 짐 크레이머가 옮긴 니콜의 말 | "our turn is real and the numbers are real and we don't want to derail anything" | 2026-10-12 | 같은 영상 01:26~01:33 | [자막] 전언 |
| Q6 | 브라이언 니콜(직원 메모) | "Starbucks is back. Our business has made the turn." | 2026-09-10 | CNBC 유튜브 kJxONRGhEPs 00:13 | [자막] |
| Q7 | 브라이언 니콜(CNBC) | "the shine is back on Starbucks" | 2026-09-10 | 같은 영상 00:59 | [자막] |
| Q8 | 브라이언 니콜(세마포 대담, 치폴레로 옮길 때를 돌아보며) | "if I didn't take that chance on Chipotle I think I would have been watching from the sidelines" | 2026-03-19 게시 | 유튜브 N8MajsPAEpk 15:10 | [자막] |
| Q9 | 스콧 보트라이트(실적 자료) | "Our positive results reflect the momentum we're building as our Recipe for Growth strategy continues to take shape" | 2026-07-29 | SEC 8-K | [요약도구] |
| Q10 | 스콧 보트라이트(설명회) | "we have taken share in each month of 2026" | 2026-07-29 | TIKR 재인용 | [재인용] |
| Q11 | 스콧 보트라이트(서울) | "(치폴레 한국은) 아시아 전역에서 치폴레가 어떻게 성장할 지에 대한 기준점이 될 것" | 2026-09-01 | 비즈워치 | [원문] 한국어로 옮겨진 말 |
| Q12 | 씨티 존 타워 | "The clear anchor to why this would make any sense is management" | 2026-10-08 | 포춘 | [원문] |
| Q13 | 멜리어스 제이컵 에이킨-필립스 | "It's not like Starbucks has a grill" | 2026-10-08 | 블룸버그 재인용 | [재인용] |
| Q14 | TD 코웬 앤드루 찰스 | "a low-probability outcome at this stage" | 2026-10-08 | CBS | [원문] |
| Q15 | 블룸버그 인텔리전스 마이클 헤일런 | "Scott Boatwright, the current CEO, has not done a very good job replacing Brian Niccol" | 2026-10-08 | 블룸버그TV 유튜브 ApNx2JacfcI 00:36 | [자막] |
| Q16 | 세마포 로한 고스와미(글) | "There have been weirder marriages." | 2026-10-06 | 세마포 | [원문] |
| Q17 | 치폴레 공시 | "our guidance did not include a financial impact from these matters" | 2026-08-05 | TIKR 재인용 | [재인용] |

기사 제목 후보: CNBC "Starbucks says it is not buying Chipotle after takeover speculation"(10-12), 포춘 "Why buying Chipotle would be a mistake for Starbucks, even with Brian Niccol in charge"(10-09), 세마포 "A Starbucks-Chipotle tie-up might be crazy enough to work"(10-06), 24/7 월스트리트 "Chipotle Slides 3% as Starbucks Rules Out Acquisition…"(10-12).

## 9. 화면의 실물 후보(목록만, 내려받지 않았다)

### 위키미디어 커먼스

| 무엇 | 파일 페이지 | 라이선스 | 메모 |
|---|---|---|---|
| 브라이언 니콜 | https://commons.wikimedia.org/wiki/File:Brian_Niccol_(uncropped).jpg | CC BY 2.0(Phi Delta Theta) | 5374×3583, 2023-06-15. 치폴레 CEO 시절 |
| 브라이언 니콜(얼굴) | https://commons.wikimedia.org/wiki/File:Brian_Niccol.jpg | CC BY 2.0 | 325×429로 작다 |
| 스콧 보트라이트 | https://commons.wikimedia.org/wiki/File:Scott_Boatwright,_CEO_of_Chipotle_and_Joe_DiRosa,_Founder_of_Tartare_at_the_CREATE._The_Event_for_Emerging_Restaurateurs.jpg | CC BY 4.0(Punkrock347) | 800×1061, 2026-07-24. 두 사람이 같이 찍힘 |
| 치폴레 매장 | https://commons.wikimedia.org/wiki/File:Chipotle,_Valdosta.jpg | CC BY-SA 4.0(Michael Rivera) | 5184×3456, 2021 |
| 치폴레 매장 | https://commons.wikimedia.org/wiki/File:Chipotle_Mexican_Grill,_Mobile.jpg | CC BY-SA 4.0 | 5184×3456, 2018 |
| 부리토 | https://commons.wikimedia.org/wiki/File:Burrito,_Chipotle_Mexican_Grill,_Rue_de_Montfaucon,_Paris_001.jpg (002, 003도) | CC BY 2.0(Guilhem Vellut) | 5472×3648, 2016 |
| 부리토 볼 | https://commons.wikimedia.org/wiki/File:Chipotle_burrito_bowl_-_October_2024_-_Sarah_Stierch.jpg | CC BY 4.0(Missvain) | 4032×3024 |
| 부리토 볼 | https://commons.wikimedia.org/wiki/File:Burrito_bowl_from_Chipotle_Mexican_Grill_2026-08-08_1.jpeg | CC BY-SA 4.0 | 2160×2053, 2026-08 |
| 스타벅스 리저브 로스터리(시애틀) | https://commons.wikimedia.org/wiki/File:Starbucks_Reserve_Roastery_01.jpg , https://commons.wikimedia.org/wiki/File:Starbucks_Reserve_Roastery_and_Tasting_Room,_Seattle,_2023.jpg | CC BY-SA 4.0 | 외관·내부 여러 장(interior 03, 04) |
| 스타벅스 본사(스타벅스 센터) | https://commons.wikimedia.org/wiki/File:Seattle_-_Starbucks_Center_from_the_water_01.jpg | CC BY-SA 3.0(Joe Mabel) | 4288×2848 |
| 스타벅스 본사 | https://commons.wikimedia.org/wiki/File:Starbucks_Headquarters_Seattle.jpg | 퍼블릭 도메인 | 1164×1552 |

라이선스는 커먼스 API의 표기를 읽은 것이다. 파일 페이지를 열어 다시 확인한다. "스타벅스 일반 매장 외관"은 이 검색어로는 못 찾았다(다른 검색어로 다시 찾을 것).

### 유튜브

| 영상 | 올린 날 | 길이 | 쓸 만한 구간 |
|---|---|---|---|
| CNBC Television "Market Open: Stocks Mixed, Starbucks Won't Buy Chipotle, Tech CEO Warns on AI • 10/12/26" https://www.youtube.com/watch?v=BucZl6rytG0 | 2026-10-12 | 3:51 | **00:35~01:34**: 진행자의 부인 소식, 크레이머와 파버의 스튜디오 장면(Q4, Q5) |
| Bloomberg Television "Chipotle Jumps on Report Starbucks Explored a Takeover" https://www.youtube.com/watch?v=ApNx2JacfcI | 2026-10-08 | 1:36 | 00:00~00:45: FT 보도 소개, 헤일런의 말(Q15) |
| Bloomberg Television "Chipotle Jumps on Report of Potential Starbucks Takeover \| Closing Bell" https://www.youtube.com/watch?v=nJ8rGzaCGJQ | 2026-10-08 | 6:49 | 04:00 앞뒤: 치폴레 주가 화면과 "이 규모의 거래는 뜨지 못할 수도" |
| TODAY "Starbucks Reportedly Exploring Bid to Takeover Chipotle" https://www.youtube.com/watch?v=xtVlXKBA11Y | 2026-10-09 | 2:38 | 지상파 뉴스 화면. 구간은 보지 않았다 |
| Bloomberg Podcasts "Chipotle Jumps on Report Starbucks Has Explored Takeover" https://www.youtube.com/watch?v=mrJzF3Fom0w | 2026-10-08 | 6:27 | 보지 않았다 |
| CBS Philadelphia "Starbucks is exploring possible Chipotle takeover, report says" https://www.youtube.com/watch?v=_bRwXVArdn0 | 2026-10 | 0:24 | 짧은 뉴스 단신 |
| CNBC Television "'The shine is back on Starbucks,' says CEO Brian Niccol" https://www.youtube.com/watch?v=kJxONRGhEPs | 2026-09-10 | 4:45 | 00:09~01:05: 메모 소개와 니콜의 얼굴·말(Q6, Q7). **인수설 한 달 전의 니콜** |
| CNBC Television "Starbucks CEO Brian Niccol on Q3 earnings" https://www.youtube.com/watch?v=nLSvBJLXKcE | 2026-07-30 | 3:00 | 보지 않았다 |
| Semafor "Starbucks CEO Brian Niccol on Leading Through Turnarounds \| The CEO Signal" https://www.youtube.com/watch?v=N8MajsPAEpk | 2026-03-19 | 47:13 | 14:50~16:10: 타코벨에서 치폴레로 옮긴 결정(Q8). 15:58 진행자가 치폴레 주가 차트를 말함 |
| WSJ "Starbucks CEO Breaks Down the Company's Biggest Problem and How to Fix It" https://www.youtube.com/watch?v=Mp_6X8Gbbe4 | 2025-02-20 | 8:18 | 니콜이 매장에서 말하는 장면. 구간은 보지 않았다 |
| CNBC Television "Not everyone is onboard with Brian Niccol at Starbucks, says Jim Cramer" https://www.youtube.com/watch?v=3k-jybXWePA | 2024-10-01 | 1:49 | 옛 자료 |
| CNBC Television "Squawk Pod: SpaceX aims for telecom, Starbucks eyes Chipotle - 10/09/26" https://www.youtube.com/watch?v=N1pS-PRtXcY | 2026-10-09 | 37:00 | 소리만 |

- 크레이머의 발언만 따로 올린 CNBC 영상은 조사 시각에 없었다(CNBC Television 채널 최근 150개 목록에서 확인). 위 "Market Open" 묶음 영상이 유일하다.
- 보트라이트의 방송 인터뷰는 유튜브 검색으로 못 찾았다. 그의 얼굴은 커먼스 사진과 한국 기자간담회 사진(F54)이 있다.
- 다른 실물: CNBC 기사 화면(F7), 포춘 기사 화면(F10), 세마포 두 기사 화면(F1, F4), 치폴레 보도자료, 받은 주가 데이터(`data/cmg.csv`, `sbux.csv`: 10-08의 긴 양봉과 7,204만 주 거래량 막대가 그림이 된다), 강남점 사진(머니투데이·비즈워치).

## 10. 지난 시리즈 편 채점용: 버라이즌

- **F59.** 버라이즌(VZ): 10-08 종가 46.35 → 10-09 종가 **41.65달러**(-10.1%, 거래량 9,517만 주). **10-12 11:16 ET(한국 10-13 00:16, 마감 전) 42.32달러, +1.61%**(장중 41.87~42.78). 금요일 저가 40.81달러 아래로는 내려가지 않았다. [데이터] 나스닥
- **F60.** 실적 발표일: **10-26(월) 그대로다.** 자료 07:00 ET, 설명회 08:30 ET. 버라이즌이 09-28에 낸 공지와 회사 행사 페이지. 팁랭크스(10-20), 넥스트어닝스데이트(10-28)의 날짜는 추정치다. [검색요약] https://www.verizon.com/about/news/verizon-q3-2026-earnings-report-date
- **F61.** 10-09 뒤의 새 소식: **통신사가 스페이스X에 망을 빌려준다는 발표는 찾지 못했다.** 10-12까지의 보도는 스페이스X의 그레인 800MHz 인수(10-08 발표, WSJ가 약 80억 달러로 보도, FCC 승인 필요)와 그 반응뿐이다. [검색요약] 확장 검색 한 번. 10-12자 기사로는 트레이딩키의 스페이스X 주가 전망이 잡혔으나 열어 보지 않았다.

## 11. 받은 줄거리와 다른 점

1. **"세마포가 치폴레가 자문사를 고용했다고 보도"**: 세마포의 09-15 기사는 이사 선임과 "행동주의 투자자가 올 것"이라는 관측이었다. 자문사(은행) 고용 보도는 9월 28일 주에 따로 나왔고(원 보도는 못 찾음), 고용의 목적은 세마포 스스로의 표현으로 "잠재적 인수를 막기 위해"다. **행동주의 투자자는 이름이 없고 실제로 들어왔다는 보도도 없다.**
2. **인수설의 순서**: 09-28 베타빌 인수설(인수자 미상) → 세마포의 은행 고용 보도 → 10-06 세마포가 스타벅스를 가설로 처음 거론("치폴레는 제안을 받지 않았다") → 10-08 FT. FT가 처음이 아니다.
3. **"치폴레 급등, 스타벅스 하락"**: 10-08 스타벅스의 종가는 -0.40%로 거의 보합이었다(장중 -6.7%에서 회복). 종가로 크게 빠진 날은 다음 날 10-09(-2.64%)다.
4. **"부인 → 치폴레 하락"**: 치폴레는 부인 전인 10-09에 이미 -3.34%로 오른 것의 절반 넘게 반납했다. 포춘은 10-09에 "보도 전 수준으로 돌아왔다"고 썼다. 10-12에는 보도 전 가격 아래로 내려갔다.
5. **부인한 사람**: 스타벅스 대변인이 크레이머에게 한 말이고, CNBC 방송에 따르면 크레이머는 주말에 니콜 본인과도 이야기했다. NBC에는 대변인이 이메일로 따로 확인했다. 문구가 둘이다(Q1, Q2).
6. **스타벅스의 첫 반응은 부인이 아니었다**: 10-08에는 "루머에 논평하지 않는다"였다. 나흘 뒤에 딱 잘랐다.
7. **"니콜이 떠난 뒤 반 토막"**: 발표 전날 종가 기준 -43.5%(10-09), -45.8%(10-12 장중)다. "거의 절반"은 맞고 "절반 넘게"는 아니다. 사상 최고가(니콜 재임 중인 2024-06) 기준으로는 -56%.
8. **치폴레의 2026년은 실적만 보면 회복 중이다**: 동일매장 매출이 두 분기 연속 늘었고 7월에 가이던스를 올려 하루 +12.5%였다. 주가가 다시 꺾인 것은 8월 살모넬라와 9월의 까닭 모를 하락 때문이다.

## 확인하지 못한 것

- **10-12 종가.** 조사 끝 시각이 11:16 ET다. 한국 05:00 뒤에 `https://api.nasdaq.com/api/quote/CMG/historical`로 다시 받는다.
- FT 원문(유료)과 게재 시각. 인수 자문사의 이름. FT가 말한 "니콜이 치폴레를 다시 이끄는 안"의 정확한 문구(SBS Biz의 옮김만 봄).
- 세마포의 9월 말 "은행 고용" 원 보도와 고스와미의 X 글 원문, 날짜.
- 크레이머 방송 발언의 정확한 문구(자동 자막뿐). 니콜 본인의 공개 발언.
- NBC 기사, 스타벅스 3분기 자료, 치폴레 2분기 8-K는 요약 도구를 거쳐 읽었다(SEC가 직접 접속을 막았다).
- 니콜의 치폴레 취임일(2018-03-05)과 선임 발표일(2018-02-13), 스타벅스 취임일(2024-09-09), 치폴레 액면분할일(2024-06-26), 스타벅스코리아의 지분 구조는 기억이다.
- 니콜의 2025회계연도 보수 3,100만 달러(검색 요약). 서드포인트의 지분과 지금도 들고 있는지(검색 요약, 2025년 4분기 13F).
- 2015년 대장균 사태의 숫자(검색 요약).
- 구루포커스의 5년 PER 중간값 51.35배(재인용). 스타벅스의 2025회계연도 4분기 동일매장 매출(자료 페이지에서 숫자를 못 뽑았다).
- 보트라이트의 2분기 설명회 발언은 TIKR의 재인용이다. 녹취 원문은 열지 못했다.
- 09-15(-5.9%)와 10-05(-4.7%) 하락의 까닭: 24/7 월스트리트는 "확인된 뉴스 없음"이라 했다. 다른 설명은 찾지 못했다.
- 도미노피자 엔터프라이즈의 날짜별 값(야후 시세, 날짜 어긋남 가능)과 부인 뒤 오른 까닭. 파파존스가 그 뒤 -59% 된 까닭.
- 부인을 다룬 한국어 기사(조사 시각에 없음). 강남점 메뉴 가격과 2호점 위치.
- 버라이즌·스페이스X의 10-10~12 새 소식은 검색 요약 한 번으로만 봤다.
