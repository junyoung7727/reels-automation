# 서클(CRCL) 주가가 움직인 날과 까닭 — 조사 초안

조사일: 2026-10-16(한국 시각). 미국장 마지막 종가는 2026-10-15.
조사자: 하위 에이전트(웹 검색과 WebFetch). 아직 대본에 쓸 확정 사실이 아니다.

**확인 범위 표기**
- 원문을 직접 읽음: 이번 조사에는 없다. 모든 웹 자료는 WebFetch(요약 모델)를 거쳤다.
- 요약 도구를 거쳐 읽음: WebFetch로 그 페이지를 열어 요약을 받음. 따옴표 안 문장은 요약 도구가 "verbatim"이라고 돌려준 것이라 원문과 한두 낱말이 다를 수 있다. 더빙에 쓰기 전에 원문을 한 번 더 연다.
- 검색 요약만 봄: 검색 결과의 요약만 봤고 페이지를 열지 못했다(403, ECONNRESET 등).
- 로컬 데이터: `data/crcl_daily.csv`, `data/coin_daily.csv`, `data/irx_daily.csv`(야후 일봉)에서 계산.

**같은 날 CRCL·COIN 종가 변화(로컬 데이터로 계산)**

| 날 | CRCL 종가 | CRCL | COIN | 찾은 까닭(아래 번호) |
|---|---|---|---|---|
| 2025-06-23 | 263.45 | +9.6% | -0.3% | 사상 최고 종가(장중 298.99) M2 |
| 2025-06-24 | 222.65 | -15.5% | +12.1% | M3 |
| 2025-11-12 | 86.30 | -12.2% | -0.0% | M4 |
| 2026-01-15 | 76.60 | -9.7% | -6.5% | M5 |
| 2026-01-30 | 63.93 | -5.4% | -2.2% | M6(1월 미끄럼) |
| 2026-02-05 | 50.23 | -8.8% | -13.3% | M7 |
| 2026-02-25 | 83.14 | +35.5% | +13.5% | M8 |
| 2026-03-24 | 101.17 | -20.1% | -9.8% | M9 |
| 2026-05-04 | 119.53 | +19.9% | +6.1% | M10 |
| 2026-05-11 | 131.76 | +15.9% | +7.7% | M11 |
| 2026-06-03 | 90.13 | -10.6% | -6.2% | M12 |
| 2026-06-05 | 80.28 | -11.3% | -7.1% | M13 |
| 2026-06-30 | 62.63 | -17.5% | -3.6% | M14 |
| 2026-08-19 | 78.59 | +9.6% | +9.6% | M17 |
| 2026-08-31 | 95.55 | +9.7% | +5.3% | M18(까닭 못 찾음) |
| 2026-09-03 | 103.23 | +16.5% | +10.1% | M19 |
| 2026-09-15 | 86.30 | -11.4% | -10.1% | M20 |
| 2026-10-14 | 79.55 | -5.6% | -4.9% | M22 |
| 2026-10-15 | 86.97 | +9.3% | +6.3% | M23 |

로컬 데이터의 다른 값: 2026년 최고 종가 132.84(2026-03-18), 2026년 최저 종가 50.23(2026-02-05). 2025-06-23 최고 종가 263.45 → 2026-10-15 86.97은 -67.0%. 2025-12-31 종가 79.30이라 2026-10-15 기준 올해 +9.7%. 2026-08-05와 08-06의 종가가 63.28로 같다(데이터 오류일 수 있음, 실적 발표일과 겹침).

---

## 1. 날짜별 움직임과 까닭

**M1. 상장.** 2025-06-05 공모가 31달러, 첫 종가 83.23(로컬 데이터). 공모가는 여러 보도에 같다.
- 출처: https://www.tipranks.com/news/cathie-wood-dumps-circle-crcl-stock-during-meteoric-rise — 검색 요약만 봄.

**M2. 2025-06-23 최고점.** 장중 298달러대, 완전희석 시가총액 770억 달러 넘음, 종가 263.45.
- "the stock price of stablecoin issuer Circle hit $298 during trading on Monday, and its market value exceeded $77 billion on a fully diluted basis" (PANews가 The Block을 인용, 2025-06-24)
- 출처: https://www.mexc.com/news/18019 계열 PANews 재게시 — 검색 요약만 봄. 같은 날 앞선 보도는 시가총액 약 580억 달러(기본 주식 수 기준)로 적었다. 숫자는 기준(기본/완전희석)에 따라 다르다.

**M3. 2025-06-24 -15.5%.** 단일한 공식 까닭은 없다. 보도에 나온 것: 캐시 우드의 ARK가 6월 23일 최고점 무렵 약 30만 7천 주를 팔았다. 같은 사흘 동안 코인베이스는 약 15% 올랐고, "투자자가 코인베이스로 갈아탔을 수 있다"는 추정이 있다. 코인베이스는 이날 룩셈부르크에서 MiCA 인가를 받았다는 보도도 있다.
- "its investors may have rotated into Coinbase" — CNBC 기사 재게시(NBC Miami, 2025-06-26), 추정으로 쓰인 문장. https://www.nbcmiami.com/news/business/money-report/circle-resumes-its-post-ipo-rally-after-pullback-stablecoin-issuer-boosts-coinbase/3646172/ — 요약 도구를 거쳐 읽음.
- ARK 매도: https://www.tipranks.com/news/cathie-wood-dumps-circle-crcl-stock-during-meteoric-rise — 검색 요약만 봄.
- 같은 기사: 코인베이스는 USDC 준비금 이자의 절반을 받고 자기 플랫폼에 있는 USDC의 이자는 전부 받는다. 연준 인사 두 명이 7월 인하를 지지할 수 있다고 말해 서클 이익에 불리할 수 있다는 맥락도 적혀 있다.
- 판정: 매도 주체(ARK)와 코인베이스로의 이동은 보도된 사실, "그래서 떨어졌다"는 추정.

**M4. 2025-11-12 -12.2%(3분기 실적).** 실적은 예상보다 좋았으나(조정 EPS 0.64달러, 매출 약 7.4억 달러) 금리 하락 걱정이 앞섰다. 준비금 수익률이 96bp 내려 4.15%. 연간 영업비용 전망을 2천만 달러 올렸다.
- CFO 제러미 폭스긴: "In many ways, we think falling rates are good for our business in the near term." / "Falling rates lead to greater economic activity, more risk-taking, and increased investment."
- 출처: https://finance.yahoo.com/news/circle-stock-plunges-as-concerns-over-falling-interest-rates-overshadow-strong-revenue-earnings-growth-174402233.html (2025-11-13, Ines Ferré) — 요약 도구를 거쳐 읽음.
- 모틀리풀: 장중 최대 -11.4%, "expected operating expenses were raised by $20 million, while other revenues saw a $15 million increase." https://www.fool.com/investing/2025/11/12/why-circle-internet-stock-fell-11-this-morning — 요약 도구를 거쳐 읽음.
- 같은 날 블룸버그 영상 제목 "Declining Rates Are Catalyst for Growth, Circle CEO Says" https://www.bloomberg.com/news/videos/2025-11-12/declining-rates-are-catalyst-for-growth-circle-ceo-says-video — 제목만 봄.
- 같은 날 COIN은 -0.0%(로컬 데이터): 서클만의 악재였다는 근거.

**M5. 2026-01-15 -9.7%.** 1월 14일 코인베이스 CEO 브라이언 암스트롱이 상원 시장구조법(CLARITY) 초안 지지를 철회했다. 까닭 넷 가운데 하나가 그 초안이 "kill rewards on stablecoins"(스테이블코인 보상을 없앤다)였다. 몇 시간 뒤 상원 은행위원장 팀 스콧이 심사(markup)를 미뤘다. 다음 날 서클은 10% 가까이 빠졌다.
- 출처: https://www.theblock.co/news/regulation/2026-01-14-coinbase-pulled-support-what-happened-385704 (2026-01-14) — 요약 도구를 거쳐 읽음. 스콧: "everyone remains at the table working in good faith."
- 서클 하락 보도: https://financefeeds.com/us-crypto-equities-retreat-as-senate-delays-landmark-market-structure-vote/ 등 — 검색 요약만 봄("tumbled nearly 10%", 종가 76.60은 로컬 데이터와 같음).
- "rather have no bill than a bad bill"이라는 말은 확인하지 못했다(위 기사에 없음).

**M6. 2026-01 미끄럼(01-30 종가 63.93).** 한 가지 까닭으로 묶은 보도는 못 찾았다. 그 달에 있었던 일:
- 1월 15일 CLARITY 심사 연기(M5), 1월 20일 -7.5%(까닭 못 찾음).
- 1월 22일 다보스에서 앨러 "totally absurd" 발언(E3).
- 1월 27일 테더가 미국용 스테이블코인 USAT 출시(D1). 1월 27일 CRCL -1.3%, 이튿날 +4.1%(로컬 데이터)라 출시일에 큰 반응은 없었다.
- 1월 29~30일 -7.3%, -5.4%, 비트코인 하락 국면(M7)과 겹친다.
- 판정: 1월 하락을 USAT 탓으로 쓸 근거는 없다.

**M7. 2026-02-05 종가 50.23(사상 최저 종가).** 비트코인이 6만 8천 달러 아래로, 2024년 10월 이후 최저. 넉 달 전 최고점 12만 6천 달러에서 46% 하락. 같은 날 COIN은 -13.3%로 CRCL(-8.8%)보다 더 빠졌다.
- "Fell below $68,000, its lowest level since October 2024... down 46% from its all-time high of $126,000"; 서클 주가 "around $52, down from a high of $263"
- 출처: https://fortune.com/2026/02/05/crypto-market-in-free-fall-as-bitcoin-plunges/ (2026-02-05 2:20 PM ET) — 요약 도구를 거쳐 읽음. 오프체인 랩스의 Beto Aparicio: "encourages investors to delay returning to risk-on assets"(2월 셧다운 가능성, 긴축 쪽 연준 의장 지명).

**M8. 2026-02-25 +35.5%(4분기 실적).** 매출과 EPS가 예상을 넘었다. 매출 7.7억 달러(+77%), 희석 EPS 0.43달러(예상 0.16), USDC 유통량 753억 달러(+72%). 거래량 6,140만 주(3개월 평균의 약 5배). 같은 날 COIN +13.5%.
- 출처: https://finance.yahoo.com/news/stock-market-today-feb-25-223511077.html — 요약 도구를 거쳐 읽음. "The stock rallied after Q4 2025 results topped revenue and EPS expectations."
- EPS·유통량: https://coin360.com/news/circle-q4-2025-earnings-usdc-75b-revenue-stock-surge — 검색 요약만 봄.
- 2월 5일 바닥에서 3월 중순 약 129달러까지 약 160% 올랐다는 보도: https://www.bitget.com/news/detail/12560605286633 — 검색 요약만 봄.

**M9. 2026-03-24 -20.1%(상장 뒤 최대 하루 낙폭이라는 보도).** 상원 CLARITY 새 초안이 "이자와 경제적으로 같은" 보상과 가만히 들고 있는 잔고에 주는 보상을 막는다는 보도. 같은 날 COIN -9.8%. 같은 날 아침 테더가 4대 회계법인 감사를 받기로 했다는 발표도 있었다.
- CoinDesk(2026-03-24): 2월 초 이후 약 170% 오른 랠리를 지웠다. USDC는 코인베이스 매출의 약 20%.
  - 미즈호 Dan Dolev: "Clarity Act could potentially ban yield payments for simply holding a stablecoin"
  - 키록 Amir Hajian: "It pulls the rug on the pass-through model that has been driving stablecoin adoption,"
  - 클리어스트리트 Owen Lau: "the actual situation doesn't appear to be as bad as the headline indicates."
  - 비트와이즈 Ryan Rasmussen: "There will be workarounds,"
  - https://www.coindesk.com/markets/2026/03/24/circle-stock-plunges-18-as-a-new-draft-of-the-clarity-act-threatens-stablecoin-rewards — 요약 도구를 거쳐 읽음.
- 테더 감사: https://decrypt.co/362215/circle-stock-dives-tether-big-four-audit-crypto-bill-threatens-stablecoin-yield — 검색 요약만 봄.
- 반론: 번스타인은 목표가 190달러 유지(준비금 이자를 버는 일과 유통 파트너에 주는 일은 막지 않는다), ARK가 폭락 중 약 1,600만 달러어치 매수 — 검색 요약만 봄(같은 Decrypt·Cointelegraph 묶음).

**M10. 2026-05-04 +19.9%.** 금요일(5월 1일) 틸리스·올스브룩스 상원의원의 수익 타협안. 가만히 들고 있는 것만으로 주는 이자·수익은 막고, 활동에 붙는 보상은 남긴다. COIN +6.1%.
- 타협안 문구: "covered parties"가 미국 고객에게 스테이블코인을 들고 있다는 것만으로 이자나 수익을 주지 못하고, "economically or functionally equivalent to the payment of interest or yield on an interest-bearing bank deposit"인 수익도 막는다.
- 틸리스(X): "Our compromise prohibits stablecoin rewards from resembling interest on bank deposits."
- 은행 단체: "It is imperative that Congress get this right."
- 출처: https://www.theblock.co/post/399973/crypto-stocks-rally-circle-jumps (2026-05-04) — 요약 도구를 거쳐 읽음.

**M11. 2026-05-11 +15.9%(1분기 실적).** 매출·준비금 수입 6.94억 달러(+20%), 순이익 5,500만 달러(-15%), USDC 770억 달러(+28%), 온체인 거래량 21.5조 달러(+263%). Arc 토큰 사전판매 2.22억 달러, 완전희석 가치 30억 달러. ARK가 약 550만 달러어치 매수.
- 출처: https://www.theblock.co/post/400850/ark-invest-buys-circle-shares-stock-jumps — 검색 요약만 봄. 회사 발표문 https://app.edgar.tools/filing/1876042/0001876042-26-000148/final_05x11q1epr30.htm — 검색 요약만 봄.
- 한 집계 사이트는 매출 "flat", EPS 0.21로 적어 회사 발표와 어긋난다(회사 발표를 따른다).

**M12. 2026-06-03 -10.6%.** 비자·마스터카드·스트라이프가 경쟁 스테이블코인 플랫폼을 내놓으려 하고 코인베이스도 참여를 검토한다는 CoinDesk 보도(익명 소식통, 세부 없음).
- 모틀리풀: "Circle's stock price fell by nearly 11% across that trading session." / "This would be a serious competitor to Circle's USDC." / "I wouldn't sell out of Circle solely on this report"
- 출처: https://www.fool.com/investing/2026/06/03/why-circle-internet-group-stock-tumbled-today/ — 요약 도구를 거쳐 읽음.
- 같은 무렵 스트래티지가 2022년 이후 처음 비트코인을 팔았고(6월 1일 발표, 32개, 250만 달러), 비트코인이 7만 달러 아래로: https://www.cnbc.com/2026/06/01/strategy-shares-fall-after-selling-2point5-million-in-bitcoin-its-first-sale-since-2022.html — 검색 요약만 봄.

**M13. 2026-06-05 -11.3%.** 그날만의 까닭을 쓴 보도는 못 찾았다. 모틀리풀의 6월 정리는 "6월 첫 주 서클은 비트코인을 따라 더 빠르게 내렸다"고 쓴다. 6월 비트코인은 약 -20%로 2026년 최악의 달이었다는 보도(검색 요약만 봄).
- 출처: https://www.fool.com/investing/2026/07/07/how-circle-internet-group-stock-lost-45-last-month/ — 요약 도구를 거쳐 읽음. 서클 주가 6월 한 달 -44.6%(S&P 글로벌 자료).

**M14. 2026-06-30 -17.5%(종가 62.63).** 독립 회사 오픈 스탠더드가 달러 스테이블코인 **오픈 USD(OUSD)** 공개. 창립 파트너 스트라이프·코인베이스·마스터카드·비자·블랙록 등 140곳 넘음. 기업은 수수료 없이 발행·환매하고, 준비금 이자는 관리 수수료를 뺀 뒤 참여 파트너에게 돌아간다. 이끄는 사람은 스트라이프가 2024년에 산 브리지의 공동창업자 잭 에이브럼스. 서클은 넉 달 만의 최저, 5월 중순보다 55% 낮음.
- 에이브럼스: "Existing stablecoins have great strengths, but to use them at scale, businesses need something that's open, low-cost"
- 출처: https://www.coindesk.com/business/2026/06/30/circle-slides-8-as-stripe-coinbase-and-blackrock-back-rival-stablecoin-network (2026-06-30) — 요약 도구를 거쳐 읽음.
- 윌리엄 블레어(Andrew Jeffrey, Adib Choudhury): 아웃퍼폼 유지, "We see competitive concerns as overblown," / OUSD는 "a solution searching for a problem." 테더 아르도이노: "Welcome OUSD. Player 2 has entered the game." https://theblock.co/news/markets/2026-06-30-circle-shares-sink-16-open-usd-reveal-analysts-say-fears-overblown-406758 — 요약 도구를 거쳐 읽음.
- 모틀리풀은 6월 말 17.6% 급락의 까닭을 둘로 든다: OUSD와 러셀 지수 다섯 곳에서 빠진 것(패시브 매도). 러셀 제외는 이 한 곳에서만 봤다 — 요약 도구를 거쳐 읽음(M13 같은 기사).
- 같은 날 COIN은 -3.6%. 코인베이스는 서클의 최대 유통 파트너이면서 OUSD의 창립 파트너다.

**M15. 2026-07 미즈호 하향과 OCC 인가.** 서클이 OCC의 국가 디지털 통화 은행 인가 소식에 장전 13% 오른 다음 날, 미즈호가 언더퍼폼으로 내리고 목표가 85→50달러.
- "The new banking license doesn't fix the bigger problem: USDC's market share has been shrinking." / "If Coinbase throws its weight behind OUSD, that could give Coinbase more leverage in those negotiations"
- 출처: https://www.tikr.com/blog/mizuho-downgrades-circle-nyse-crcl-stock-open-usd-consortium-threatens-stablecoin-business-model (2026-07-16 갱신) — 요약 도구를 거쳐 읽음. 하향 날짜(7월 14일)는 검색 요약만 봄. 7월 14일 2026년 장중 최저 59.29달러라는 트레이딩뷰 글은 검색 요약만 봄(로컬 데이터의 2026 최저 종가는 50.23, 2월).

**M16. 2026-08-03 모건스탠리 하향, 08-05 2분기 실적.**
- 모건스탠리 James Faucette: 비중축소로 하향, 목표가 106→38달러. "USDC contraction exposes reserve income sensitivity." USDC 공급 전망을 2027년 약 33%, 2028년 약 44% 낮춤. 토큰화 MMF·예금과 OUSD를 위협으로 듦. 주가 -6%, 올해 약 -30%. https://www.coindesk.com/markets/2026/08/03/circle-internet-slides-after-morgan-stanley-downgrade-cut-in-price-target — 요약 도구를 거쳐 읽음.
- 2분기 실적(2026-08-05, SEC 공시): USDC 기말 733억 달러(+19%), 평균 765억 달러(+25%), 매출·준비금 수입 7.01억 달러(+7%), 준비금 수입 6.68억 달러(+5%), 준비금 수익률 3.5%(-66bp), 순이익 4,800만 달러, 희석 EPS 0.18달러, 조정 EBITDA 1.43억 달러. 기타 매출 전망 1.5~1.7억 → 3.1~3.3억 달러로 올림. 1분기 말 770억 → 2분기 말 733억으로 유통량이 줄었다.
  - 앨러: "Our quarterly financial results reflect the current rate environment and a crypto market that has slowed"
  - https://www.sec.gov/Archives/edgar/data/1876042/000187604226000246/augustepr-circle_q22026f.htm — 요약 도구를 거쳐 읽음.
- 같은 실적 통화(8월 5일)에서 코인베이스 계약이 기존 조건대로 갱신됐다고 밝힘(E7). 계약은 3년 자동 갱신이라 2029년까지(검색 요약만 봄).
- 실적 날 주가: 발표 직후 약 7% 올랐다가 되돌렸다는 보도 https://crypto.news/circle-stock-reverses-7-rally-after-mixed-q2-results/ — 검색 요약만 봄. 로컬 데이터 종가는 +0.0%.

**M17. 2026-08-19 +9.6%.** 트럼프 대통령이 백악관에서 암호화폐 기업 대표와 SEC 의장 폴 앳킨스, CFTC 의장 마이크 셀릭을 만난 날. 전날 SEC가 일부 암호화폐 기업의 증권 등록 요건을 면제하는 규칙안을 냈다. 비트코인 7만 달러 돌파와 국채 금리 하락도 함께 꼽힘. 같은 날 COIN도 +9.6%.
- "The big catalyst, however, would be the passing of the Clarity Act, currently stalled in the Senate."
- 출처: https://www.fool.com/investing/2026/08/19/why-is-circle-internet-group-stock-up-today/ — 요약 도구를 거쳐 읽음. 그날 앨러의 2분기 실적 AMA도 있었다(검색 요약만 봄).

**M18. 2026-08-31 +9.7%.** 그날의 까닭을 쓴 보도를 찾지 못했다. 8월 한 달 CRCL은 60.35(08-03)에서 95.55(08-31)로 올랐다(로컬 데이터). 8월 27일 WSJ의 "은행들이 자체 스테이블코인을 검토" 보도에 -4%였다(https://ca.finance.yahoo.com/news/circle-internet-stock-falls-banks-154610532.html — 요약 도구를 거쳐 읽음. JP모건 대변인: "has no plans to issue a stablecoin but would evaluate all options depending on customer demand").

**M19. 2026-09-03 +16.5%(종가 103.23, 100달러 회복).** 비트코인이 8만 달러를 넘었고(+3%대), 연준 월러 이사가 이번 달 동결을 지지할 수 있다고 말해 9월 인상 확률이 내려갔으며, 달러지수가 99 아래로. 같은 날 COIN +10.1%, 로빈후드도 약 15%.
- 출처: https://www.tipranks.com/news/crypto-stocks-robinhood-hood-and-are-rallying-on-thursday-heres-why (2026-09-03) — 요약 도구를 거쳐 읽음.
- 전날(9월 2일) 서클 사장 히스 타버트가 하원 금융위 증언: 달러 스테이블코인은 "dollar statecraft in its most practical form." 9월 1일 골드만삭스·BoA·씨티·도이체·UBS 등 21개 금융사가 2027년 상반기 출시 목표의 달러 스테이블코인 회사를 만들기로 했고 그날 CRCL 약 -6%(로컬 데이터 09-01 -6.4%). https://www.tikr.com/blog/circle-stock-jumped-16-and-reclaimed-100-as-crypto-rallied-and-washington-weighed-in-heres-where-crcl-could-go — 요약 도구를 거쳐 읽음.

**M20. 2026-09-15 -11.4%.** 상원이 CLARITY Act 토론 개시(클로처) 표결에서 49 대 50으로 60표에 못 미쳤다. 공화당 4명(콜린스, 홀리, 모런, 틸리스)이 반대, 쿤스 불참, 나머지 민주당 46명 반대. 틸리스는 재심의 동의를 내려고 반대표를 던졌다. 같은 날 COIN -10.1%. 쟁점은 공직자의 암호화폐 보유에 관한 윤리 조항과 스테이블코인 수익.
- 표결: https://www.orrick.com/en/Insights/2026/10/The-CLARITY-Act-Stalls-in-the-Senate-Whats-Next-for-Digital-Asset-Regulation (2026-10-02) — 요약 도구를 거쳐 읽음. 반대한 사람 명단은 검색 요약만 봄(https://homecryptoinvest.com/news/clarity-act-senate-vote-result.html 등).
- 코인베이스와 서클이 각각 약 10% 하락: https://cointelegraph.com/news/crypto-stocks-rebound-after-clarity-selloff-as-us-regulators-move-ahead (2026-09-18) — 요약 도구를 거쳐 읽음.
- CNBC 기사(2026-09-15) https://www.cnbc.com/2026/09/15/senate-cloture-vote-on-clarity-act-fails-dealing-regulatory-setback-to-crypto-industry.html — 403, 열지 못함.
- 같은 무렵 Arc 메인넷 출시(9월 15~16일, E8).
- 어긋나는 보도: 블록노미는 "9월 초 서클이 분기 실적을 못 맞춰 11.6% 내린 86.10달러"라고 쓰는데, 2분기 실적은 8월 5일이었다. 이 문장은 믿지 않는다.

**M21. 2026-09-16 -6.8%와 연준 인상.** 연준이 9월 16일 0.25%p 올려 3.75~4.00%(2023년 이후 첫 인상). 워시 의장: "our predominant focus is on the price stability side of our mandate."
- https://www.mufgresearch.com/rates/september-2026-fomc-recap/ — 요약 도구를 거쳐 읽음. 연준 공식 성명은 직접 보지 못했다.
- 블록노미는 이날 -6.8%를 CLARITY 좌절로 설명한다: https://blockonomi.com/circle-crcl-stock-slides-7-as-clarity-act-fails-yet-analysts-maintain-optimistic-outlook/ — 요약 도구를 거쳐 읽음.
- 해석(작업자): 금리가 오르면 서클의 준비금 수입은 늘어야 하는데, 인상일에 주가는 내렸다. 시장이 이 주식을 "금리 수혜주"보다 "암호화폐 위험자산"으로 다룬다는 신호로 읽힌다. 이 해석을 쓴 보도는 찾지 못했다.

**M22. 2026-10-14 -5.6%.** 9월 CPI가 전년 대비 3.7%(예상 3.6%, 8월 3.4%)로 뜨거워 10월 인상 베팅이 늘었다. 비트코인 8만 1천 달러 아래, 코스피 8% 급락과 서킷브레이커(10월 15일 아시아장). 같은 날 COIN -4.9%.
- 기로투스 CEO Vikram Subburaj: "Stronger U.S. inflation data has renewed concerns that interest rates will stay higher for longer,"
- STS Digital: "With the next FOMC a coin flip, this uncertainty is damaging liquidity and dampening risk appetite"
- CME 페드워치 10월 인상 확률이 약 22%→약 47%로 뛰었다가 26%로 내려옴.
- 출처: https://www.coindesk.com/markets/2026/10/15/bitcoin-is-back-below-usd81-000-as-fed-rate-uncertainty-weighs (2026-10-14 11:57 PM EDT) — 요약 도구를 거쳐 읽음. 이 기사 본문은 서클을 다루지 않는다. 서클 하락과 CPI를 잇는 것은 같은 날 일어났다는 것뿐이다.

**M23. 2026-10-15 75.27 출발, 86.97 마감(+9.3%).** 까닭을 밝힌 보도를 찾지 못했다. 토큰포스트는 서클 장중 +7.10%로 암호화폐 관련주 가운데 1위(블록 +3.80%, 스트래티지 +3.79%, 코인베이스 +3.29%)라고만 썼다. 같은 날 나온 관련 소식: 유럽은행감독청(EBA)이 USDC를 MiCA의 첫 "significant" 전자화폐 토큰으로 지정(10월 14일 발표, 11월 12일부터 EBA가 감독). StocksToTrade는 CFTC 규칙 소식과 낙관론을 들지만 CFTC 사전공고는 10월 5일에 나왔다.
- https://tokenpost.com/news/investing/32835 (2026-10-15 6:52 PM EDT) — 요약 도구를 거쳐 읽음.
- EBA 지정: https://crypto.news/circles-usdc-becomes-first-stablecoin-under-eu-rules/ 등 — 검색 요약만 봄.
- 판정: 10월 15일 반등의 까닭은 미확인.

---

## 2. (a) 2026년 8~10월 애널리스트 의견

| 날 | 회사(애널리스트) | 의견 | 목표가 | 확인 범위와 출처 |
|---|---|---|---|---|
| 2026-06-30 | 윌리엄 블레어(Andrew Jeffrey) | 아웃퍼폼 유지 | 없음 | 요약 도구, The Block(M14) |
| 2026-07 초 | 골드만삭스(James Yaro) | 중립 유지 | 111→96 | 요약 도구, https://www.tikr.com/blog/goldman-cut-circle-to-96-while-bernstein-says-buy-whos-right-on-crcl-stock-in-2026 |
| 2026-07-14 무렵 | 미즈호 | 중립→언더퍼폼 | 85→50 | 요약 도구, TIKR(M15) |
| 2026-07 말 | 번스타인(Gautam Chhugani) | 아웃퍼폼 유지 | 190→140 | 검색 요약만 봄 |
| 2026-08-03 | 모건스탠리(James Faucette) | 비중유지→비중축소 | 106→38 | 요약 도구, CoinDesk(M16) |
| 2026-08-04 | JP모건(Ken Worthington) | 매수 | 120 | 검색 요약만 봄(구글 파이낸스 목록). 2월에 100→90으로 내렸다는 MarketBeat 항목, 5월에 155로 올렸다는 항목도 있어 서로 맞지 않는다 |
| 2026-08-17 | 시포트 리서치 | — | 100 | 요약 도구, dailypolitical(MarketBeat 계열) |
| 2026-08-24 | 서스퀘하나 | 중립 | 69→92 | 같은 곳 |
| 2026-08-25 | 울프 리서치 | 언더퍼폼 | 50→65 | 같은 곳 |
| 2026-08-25 / 09-09 / 09-16 | 골드만삭스 | 중립 81달러(8/25), "underperform" 재확인(9/9), Hold 92달러(9/16) | — | 목록마다 다르다. 9/9의 "underperform"은 7월 중립과 맞지 않아 오기일 수 있다 |
| 2026-09-08 | KBW | 신규 Market Perform | 105 | 요약 도구, dailypolitical |
| 2026-09-17 | TD 코웬(Bryan Bergin) | 매수 | 87→92 | 요약 도구, 블록노미와 dailypolitical 두 곳 일치 |
| 2026-09-21 | 번스타인(Chhugani) | 매수 유지 | 140 | 검색 요약만 봄. 같은 날 SEC 혁신 면제에 대해 서클을 "a direct beneficiary of the new rules"라 했다는 Investing.com 기사는 요약 도구를 거쳐 읽음 |
| 2026-04-27 | 씨티(Peter Christiansen) | 매수 | 243 | 검색 요약만 봄. 그 시점 주가(약 100~120달러)에 비해 지나치게 높아 확인 필요. 10월 9일 "Citi remains a Buy"라는 팁랭크스 항목도 검색 요약만 봄 |
| 2025-07 | 컴패스 포인트 | 매도 | 205→130 | 검색 요약만 봄. 2026년 의견은 찾지 못함 |
| 2026-10-03/08/11 | 월스트리트 젠, 와이스 레이팅 | 계량 평가 하향("strong sell", "sell (d)") | — | 증권사 의견이 아님 |

컨센서스(출처마다 다름): 팁랭크스 "Moderate Buy" 매수 13·보유 6·매도 3, 평균 101.53달러(블록노미, 2026-09-17, 요약 도구) / TIKR 23명 평균 103.55달러(2026-09-03 무렵, 요약 도구) / StockAnalysis 29명 평균 약 107달러, 야후 1년 목표 106.98달러 최저 37달러(검색 요약만 봄). 다음 실적 발표는 2026-11-04(검색 요약만 봄).

내부자 매도: 최근 90일 485,657주, 약 3,921만 달러. 이사 패트릭 네빌 8월 3일 5만 주(평균 59.55달러, 보유분의 96%), 니킬 찬독 10월 8일 26,668주(79.59달러). 모두 10b5-1 계획(dailypolitical, 요약 도구).

---

## 3. (b) 고점에서 67% 빠진 까닭: 서로 다른 설명

**근거가 숫자로 있는 것**

B1. **상장 직후 거품.** 공모가 31달러가 장중 298.99달러(약 9.6배)까지, 완전희석 시가총액 770억 달러 넘음(M2). 7월 후행 PER 175배(바차트, 검색 요약만 봄). 2026년 고점(3월 132.84)도 2025년 고점의 절반이다. 이 설명은 "떨어졌다"보다 "처음 값이 지나치게 높았다"에 가깝다.

B2. **금리가 실제로는 내려 있었다.** "2026년에 금리가 올랐는데 왜 떨어졌나"라는 전제는 절반만 맞다.
- 13주 국채 금리: 2025-06 약 4.23% → 2026-01 약 3.52%(최저) → 2026-10 약 4.0%(로컬 IRX 데이터). 2026년 상승폭은 약 0.5%p이고, 2025년 상장 때보다 아직 낮거나 비슷하다.
- 서클 준비금 수익률: 2025년 3분기 4.15%(-96bp), 2026년 2분기 3.5%(-66bp, SOFR 하락)(M4, M16).
- 연준 인상은 2026-09-16 한 번(3.75~4.00%, M21). 3분기 실적(11월 4일)에야 반영된다.
- 금리 민감도 추정: 100bp 인하마다 매출 6.18억 달러(전체의 23%) 감소(드래건플라이 Omar Kanji, 2025-08), 25bp마다 2027년 매출 약 9%·EBITDA 11% 감소(번스타인) — 둘 다 검색 요약만 봄.

B3. **번 돈의 절반 이상이 코인베이스로 간다.** 2025년 코인베이스에 약 14억 달러, 매출·준비금 수입의 약 51%. 유통·거래 비용 전체는 16.6억 달러, 1달러 벌면 약 60센트(크립토슬레이트, 4pillars, 페이먼트 엑스퍼트 — 검색 요약만 봄. 10-K 원문은 보지 못했다). 2026년 8월 계약이 같은 조건으로 갱신돼 이 구조는 2029년까지 간다(M16).

B4. **USDC가 덜 자랐다.** 2025년 말 753억 → 2026년 3월 말 770억 → 6월 말 733억 달러(회사 발표). 모건스탠리가 2027·2028년 USDC 전망을 33%·44% 낮춤(M16). 회사 가이던스는 연 40% 성장을 유지.

B5. **경쟁자가 서클의 수익 모델을 정면으로 겨눴다.** 6월 30일 OUSD(이자를 파트너에게 돌려줌, 140곳 넘음) 공개일 -17.5%. 6월 3일 소문 -10.6%. 9월 1일 21개 은행 컨소시엄 -6.4%. 8월 27일 은행 자체 코인 보도 -4%. 반면 1월 27일 테더 USAT 출시일은 -1.3%(로컬 데이터)였고, 5월 말 앨러는 USAT 유통량을 2천만 달러로 말했다(E5).

B6. **규제의 수익 금지 싸움이 날마다 값을 흔들었다.** 1월 15일 -9.7%(암스트롱 철회), 3월 24일 -20.1%(보상 금지 초안), 5월 4일 +19.9%(타협안), 9월 15일 -11.4%(클로처 49:50 실패). 한 법안의 소식만으로 하루 ±20%가 오갔다.

B7. **비트코인과 같이 움직인다.** 비트코인 12.6만 → 6.8만 달러(2026-02-05, -46%), 그날 CRCL 사상 최저 종가 50.23. 6월 비트코인 약 -20%, CRCL 6월 -44.6%. 큰 날 대부분에서 COIN과 같은 방향(위 표). 금리 인상 베팅이 커진 10월 14일에도 CRCL은 내렸다(M22).

B8. **물량.** 2025년 8월 1천만 주 추가 매각(서클 200만, 기존 주주 800만, 앨러 포함), 8월 13일 JP모건이 1,150만 주 보호예수 조기 해제, 2025-12-02 180일 보호예수 만료(검색 요약만 봄). 최근 90일 내부자 3,921만 달러 매도(요약 도구).

**논평에 가까운 것(숫자로 인과가 확인되지 않음)**

B9. "서클은 사실상 금리에 건 펀드라 금리 인하 사이클이 끝이다" — 2025년 하반기 기사들의 논조. 2026년 금리가 오르는 동안에도 반등이 없었다는 점에서 이 설명만으로는 부족하다.
B10. "ARK 같은 큰손이 팔아서" — 2025년 6월 매도는 사실이나 2026년 3월·5월에는 ARK가 샀다(M9, M11). 하락의 주된 까닭으로 쓸 근거 없음.
B11. "코인베이스로 갈아탔다" — 2025년 6월 CNBC가 추정으로 쓴 말(M3).
B12. "러셀 지수 제외로 패시브 매도" — 모틀리풀 한 곳(M14).
B13. "Arc 토큰이 주주 가치를 나눠 간다" — 관련 보도는 찾았지만 주가 하락과 잇는 숫자는 찾지 못했다.

---

## 4. (c) CLARITY Act와 수익·보상 금지 싸움(2026년 10월 현재)

- 하원 통과: 2025-07-17, 294 대 134(검색 요약만 봄, 엘리너 테럿 X 글).
- 2026-01-14 코인베이스 지지 철회, 상원 은행위 심사 연기(M5).
- 2026-03-24 "이자와 경제적으로 같은" 보상과 가만히 들고 있는 잔고의 보상을 막는 초안(M9).
- 2026-05-01 틸리스·올스브룩스 타협안: 들고 있는 것만으로 주는 이자·수익 금지, 활동에 붙는 보상 허용(M10). 은행 단체는 부족하다고 반발. 미국은행협회는 "stop payment stablecoins from becoming deposit substitutes"(검색 요약만 봄), BoA 모이니핸은 수익이 허용되면 최대 6조 달러가 은행을 떠날 수 있다고 주장(검색 요약만 봄).
- 2026-08: 상원이 표결 없이 휴회(ABA 뱅킹 저널, 검색 요약만 봄). 9월 14일 트럼프가 윤리 조항에 동의했다는 CNBC 보도(검색 요약만 봄).
- 2026-09-15 클로처 49 대 50 실패(M20). 틸리스 재심의 동의로 되살릴 길은 남음.
- 오릭(2026-10-02): "passage during this Congress is now widely viewed as unlikely." / "A durable framework ultimately requires Congressional action." — 요약 도구를 거쳐 읽음.
- 규제기관이 법 없이 움직임: SEC 'Regulation Crypto Assets' 제안(8월 18일, 의견 마감 10월 20일), CFTC 규칙 OIRA 제출(9월 17일), CFTC 소매 레버리지 거래 사전공고(10월 5일, 연방관보 10월 13일). 오릭 기사와 검색 요약.
- 11월 3일 중간선거 뒤 레임덕 회기에서 다시 다룰지는 확인된 바 없다. 10월 15일 백악관 디지털자산 고문 패트릭 윗이 떠났다는 보도가 있다(https://en.cryptonomist.ch/2026/10/15/white-house-crypto-leadership-witt-exit — 검색 요약만 봄).
- 2025년 GENIUS Act는 이미 발행사가 직접 이자를 주는 것을 막는다. 싸움은 코인베이스 같은 플랫폼이 주는 "보상"을 어디까지 허용하느냐다(The Block, M10).

---

## 5. (d) 테더: USAT, 2025년 이익, 인원

**D1. USAT 미국 출시: 2026-01-27.** 발행은 앵커리지 디지털 뱅크(N.A.), 준비금 관리는 캔터 피츠제럴드. 첫 단계 거래소: 바이빗, 크립토닷컴, 크라켄, OKX, 문페이. CEO는 백악관 암호화폐위원회 사무국장 출신 보 하인스. 계획은 2025-09-12에 처음 발표.
- 아르도이노: "USA₮ offers institutions an additional option: a dollar-backed token made in America,"
- 하인스: "Our focus is stability, transparency, and responsible governance,"
- https://tether.io/news/tether-announces-the-launch-of-usat-the-federally-regulated-dollar-backed-stablecoin-made-in-america/ — 요약 도구를 거쳐 읽음.
- 2026-07-29 셀로 체인 추가(이더리움 다음 두 번째) — 검색 요약만 봄.
- 5월 28일 앨러의 평가: 유통 2천만 달러, "basically zero transaction volume"(E5).
- 2026년 10월 현재 USAT 유통량: 찾지 못함.

**D2. 2025년 순이익: 100억 달러 넘음**(2026-01-30 발표, BDO 이탈리아의 4분기 확인서. 감사가 아님). USDT 유통 1,860억 달러 넘음(1년 새 +500억), 미 국채 직접 1,220억 달러(역레포 포함 1,410억), 금 174억, 비트코인 84억, 초과 준비금 63억 달러.
- 아르도이노: "Tether enters 2026 with one of the strongest balance sheets of any global company"
- https://www.coindesk.com/business/2026/01/30/tether-s-gold-holdings-top-usd17-billion-as-net-profits-surpassed-usd10-billion-for-2025 — 요약 도구를 거쳐 읽음.
- 2026년 1분기 순이익 약 10.4억 달러, 초과 준비금 82.3억 달러(BDO) — 검색 요약만 봄(https://news.bitcoin.com/paolo-ardoino-drives-1-04b-profit-for-tether-as-reserves-climb-to-8-23b-in-q1/).
- 테더는 준비금 이자를 USDT 보유자에게 주지 않는다(포천의 설명, 아르도이노의 말 아님).

**D3. 인원: 출처마다 다르다.**
- 포천(2026-01-27): "fewer than 200 employees"(기자의 설명, 아르도이노 인용 아님). https://fortune.com/article/tether-ceo-paolo-ardoino-crypto-firm-stabelcoins-howard-lutnick-usdt-cantor-fitzgerald/ — 요약 도구를 거쳐 읽음.
- 아르도이노, 팟캐스트 When Shift Happens 143회(2025-10-16 방송): 2년 전 40명 → "250 and 300", 스테이블코인 핵심 팀은 "around 100 people", 2024년 이익 "$13.7 billion". 이것은 중국어 번역(테크플로)을 다시 영어로 옮긴 Odaily 재게시에서 읽은 것이라 원문 낱말이 아니다. https://www.odaily.news/en/post/5207014 — 요약 도구를 거쳐 읽음. 원래 영상에서 받아써야 더빙에 쓸 수 있다.
- "직원 1인당 1억 달러"는 진행자의 질문에 나온 숫자이고, 아르도이노는 "Frankly, I don't think much about this kind of data."(번역 재게시)라고 답했다.
- 같은 말: 2025년 이익 100억 달러 ÷ 200~300명이면 1인당 약 3,300만~5,000만 달러(작업자 계산, 인원이 불확실).

---

## 6. (e) 제러미 앨러의 말(영어 원문, 날짜, 출처)

더빙 후보로 짧은 줄에 ★. 모두 요약 도구가 돌려준 문장이라 쓰기 전에 원문 대조가 필요하다.

E1. ★ "We welcome continued innovation and competition in the space" / "Stablecoins represent one of the largest market opportunities in the world" — X 글, OUSD 공개 직후(2026-06-30 또는 07-01). CoinDesk(M14) — 요약 도구를 거쳐 읽음.

E2. ★ USDC는 "the most trusted, widely adopted, institutional-ready stablecoin in the world." — 같은 X 글. The Block(M14) — 요약 도구를 거쳐 읽음. 같은 글에서 파트너에게 준비금 수입을 거의 다 돌려주는 모델이 "starving an infrastructure"할 수 있다고 썼다는 보도 — 검색 요약만 봄(cryptobriefing 기사 열기 실패).

E3. ★ 수익 붙은 스테이블코인이 뱅크런을 부른다는 걱정은 "totally absurd" — 2026-01-22 다보스 세계경제포럼 패널. 같은 자리: "They help with stickiness, they help with customer traction" / "around $11 trillion of dollar money market funds that grew in various different circumstances" / "Meanwhile, lending is already shifting away from banks toward private credit and capital markets." / "there is no other alternative other than stablecoins to do that right now."(AI 에이전트 결제에 대해)
- https://cointelegraph.com/news/stablecoin-yields-no-bank-runs-circle-ceo-davos-2026 — 요약 도구를 거쳐 읽음.
- "Rewards around financial products exist in every balance that you have with a credit card that you use."는 다른 매체의 인용으로 검색 요약만 봄.

E4. ★ "USDC is fundamentally the only real choice that you have." — 2026-05-28 번스타인 전략결정 콘퍼런스. TIKR(골드만 기사) — 요약 도구를 거쳐 읽음.

E5. ★ 테더를 두고 "a macro hedge fund" / "unless they completely change from being essentially a macro hedge fund that connected to a stablecoin network" / USAT은 "basically zero transaction volume", "$20 million in circulation" / "I have not seen that anywhere in the institutional market, but it is an experiment for sure" — 같은 콘퍼런스(2026-05-28). https://thecoinformer.com/news/circle-ceo-slams-tether-us-stablecoin-says-usat-has-zero-volume (2026-05-30) — 요약 도구를 거쳐 읽음.

E6. 금리: "High rates, while, in theory, generate more revenue for us, they really slow down the velocity of money in the economy" / 올해 추가 인하는 "welcome" — 로이터 인터뷰, 2026-02-25 무렵(4분기 실적). **검색 요약만 봄**(재게시 페이지 403). 원문 확인 전에는 쓰지 않는다. 금리에 대한 앨러의 확인된 말은 E7의 첫 줄뿐이다.

E7. 2026-08-05 2분기 실적(SEC 공시와 통화 녹취):
- "Our quarterly financial results reflect the current rate environment and a crypto market that has slowed" (공시, 요약 도구)
- ★ "Our network is not theoretical or aspirational." (통화, OUSD 관련 맥락)
- "Approximately 70% of the companies that have expressed interest are already participants on our network."
- "our agreement with Coinbase has renewed on its existing terms"
- ★ "Circle enters this moment from a position of extraordinary strength."
- Arc: "the birth of a new operating system layer for economic activity in the world"
- CLARITY: "the CLARITY Act is very actively being discussed and kind of final issues are being worked on"
- https://www.fool.com/earnings/call-transcripts/2026/08/12/circle-crcl-q2-2026-earnings-call-transcript/ — 요약 도구를 거쳐 읽음.

E8. Arc 출시(2026-09-16 CoinDesk): ★ "This is, I believe, the most consequential major platform launch in our history" / 체인을 쓰려면 그 토큰을 들어야 한다는 생각에 ★ "That would be crazy," — https://www.coindesk.com/business/2026/09/15/circle-debuts-arc-blockchain-which-jeremy-allaire-calls-more-consequential-than-usdc — 요약 도구를 거쳐 읽음.

E9. 표결 전 X 글(2026-09-14): ★ "It's time for CLARITY." ... "YES." — https://x.com/jerallaire/status/2099344350798901371 — 검색 요약만 봄. 이튿날 49:50으로 실패했으니, 앞뒤로 붙이면 반전이 된다.

E10. 표결 실패 뒤 CNBC 스쿼크박스 인터뷰(2026-09-16) https://www.cnbc.com/video/2026/09/16/clarity-act-fails-to-pass-in-senate-circle-ceo-jeremy-allaire-on-whats-next-for-crypto-regulation.html — 영상이라 내용을 보지 못했다.

E11. 오래된 말(테더): 2020년 "unregulated offshore USD shadow banking solution for China and Asia" — https://decrypt.co/15878/circle-ceo-slams-tether-as-shadow-banking-solution-for-china — 검색 요약만 봄.

---

## 7. 확인하지 못한 것

- 2026-08-31(+9.7%)과 2026-10-15(+9.3%) 반등의 까닭. 1월 20일(-7.5%)의 까닭.
- 2026-06-05(-11.3%)를 그날 하나의 사건으로 설명한 보도(비트코인 하락이라는 월간 정리뿐).
- 러셀 지수 제외(한 곳만).
- JP모건·씨티의 2026년 9~10월 목표가. 씨티 243달러(4월)와 골드만 "underperform"(9/9)은 의심스럽다. 컴패스 포인트의 2026년 의견.
- 2025년 10-K 원문의 유통비용 숫자(2차 보도만).
- 앨러의 금리 발언(E6) 원문, OUSD에 대한 X 글 전문, CNBC 인터뷰 내용.
- 아르도이노의 인원 발언 영어 원문(번역 재게시만). 2026년 10월 현재 USAT 유통량.
- CNBC 9월 15일 기사(403), 폴 헤이스팅스 정리(연결 끊김) 원문.
- 연준 9월 16일 인상의 공식 성명과 표결.
