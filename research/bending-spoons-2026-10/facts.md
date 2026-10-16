# 벤딩스푼스(Nasdaq: BSP) 사실 정리 — 2026-10-16 01시경(KST) 기준

조사: 2026-10-16 (KST 00:10~). 미국은 10-15(수→목) 장중이다. **10-15 종가는 아직 없다**(조사 시각 = 미 동부 10-15 11시대).

확인 수준 표기
- [원문 직접]: SEC 원문(6-K, 424B4, 13G) 또는 원자료(JSON)를 직접 읽음
- [기사]: 기사 본문을 읽음
- [검색 요약만]: 검색 결과 요약·제목만 봄. 대본에 쓰기 전에 원문 확인 필요
- (계산): 작업자가 원자료로 계산. 식을 같이 적음

원자료 위치: `data/` (아래 각 항목에 파일명). SEC 원문 텍스트는 `data/sec/*.txt`.

---

## 1. 상장(IPO)

| 번호 | 사실 | 날짜 | 출처 | 수준 |
|---|---|---|---|---|
| F1 | 공모가 **29달러**(희망 범위 26~28달러 위). 공모 주식 57,971,015주(회사 신주 34,398,640 + 기존 주주 23,572,375). 초과배정 옵션 회사 5,244,026주 + 주주 3,451,626주 | 2026-06-30 가격결정, 07-01 상장 | 424B4 표지·"The offering" `data/sec/20260701_424b4.htm.txt`; 가격 범위는 https://www.investing.com/news/stock-market-news/bending-spoons-prices-ipo-at-29-per-share-on-nasdaq-432SI-4769553 | 주식 수 [원문 직접], 29달러·범위 [검색 요약만]+TechCrunch [기사] |
| F2 | 공모 총액 **16.8억 달러**(57.97M×29 = 16.81억, 기본 물량 기준). 회사가 받은 순수입 **11.0억 달러**(수수료 뺀 값) | 07-01 / 08-13 발표 | TechCrunch https://techcrunch.com/2026/07/01/bending-spoons-defies-saas-slump-surges-40-on-first-day-of-trading/ ; Q2 실적 6-K `data/sec/20260813_ex99-1.htm.txt` | [기사], 순수입 [원문 직접] |
| F3 | 상장 후 주식 수: 보통주 324,978,625(초과배정 전부 행사 시 330,222,651) + A주 310,240,685 = **약 6.35억 주(행사 시 6.40억 주)**. A주는 1주 5표(이중 의결권). 임원·이사 13명이 의결권 약 63% | 424B4 | 424B4 | [원문 직접] |
| F4 | 첫날(07-01) 시가 **31.00**, 고가 **43.98**, 저가 30.70, 종가 **40.50**(공모가 대비 +39.7%), 거래량 1,737만 주 | 2026-07-01 | Yahoo 일봉 `data/bsp_daily_2026-07-01_2026-10-14.csv`, TechCrunch | [원문 직접]+[기사] |
| F5 | 첫날 종가 기준 시가총액 **257억 달러**(TechCrunch). 공모가 기준 기업가치 약 184억 달러(29×6.35억 = 184.2억, 계산 일치). 마지막 비상장 가치는 110억 달러 | 07-01 | TechCrunch(위) | [기사] (계산) |
| F6 | 보호예수(lock-up): 상장 설명서 날짜 뒤 **180일**. 2026-06-30 기준이면 **2026-12-27 전후** 풀림 | 424B4 | 424B4 "Lock-up agreements" | 180일은 [원문 직접], 날짜는 (계산) |
| F7 | 상장 시점 큰 주주: Baillie Gifford 49,503,716주(보통주의 15.2%, 7/31 기준 13G), Durable Capital 23,586,614주(7.3%, 13G), Galileo Quattordici 11.6%(상장 전) | 07-09, 08-03 제출 | `data/sec/13g_20260709.xml.txt`, `13g_20260803.xml.txt`, 424B4 | [원문 직접] |
| F8 | **424B4(상장 설명서) 본문에 "Berkshire" 단어가 없다.** 버크셔의 상장 때 6억 달러 매입은 10-14 보도자료에서 처음 확인됨. 7월에 이를 보도한 기사는 찾지 못함 | 10-14 | 424B4 전문 검색(0건); 10-14 EX-99.1 | 설명서 [원문 직접]; "7월 보도 없음"은 검색으로 못 찾았다는 뜻일 뿐 |

## 2. 버크셔 해서웨이

| 번호 | 사실 | 날짜 | 출처 | 수준 |
|---|---|---|---|---|
| F9 | 버크셔가 **신주 1,000만 주를 주당 33.00달러**, 총 **3.3억 달러**에 사는 사모 배정(private placement). 돈의 쓰임: "일반 목적과 **새 인수**". 마감 예정 **2026년 4분기**(아직 안 끝남) | 2026-10-14 | 6-K https://www.sec.gov/Archives/edgar/data/2004711/000200471126000018/bsp-20261014x6k.htm ; EX-99.1 `data/sec/20261014_ex99-1.htm.txt` | [원문 직접] |
| F10 | 보도자료: 상장 때 버크셔가 **6억 달러** 투자, 이번까지 합쳐 지분 **4%** | 10-14 | EX-99.1 | [원문 직접] |
| F11 | 33달러는 전날(10-13) 종가 **37.86달러보다 12.8% 싸다**(1−33/37.86). 10-14 종가 53.46 기준으로는 38% 싸다(1−33/53.46). 같은 지적: Yahoo(약 13% 아래), GuruFocus/TradingView | 10-14 | Yahoo 일봉; https://finance.yahoo.com/markets/article/bending-spoons-stock-soars-on-new-berkshire-hathaway-investment-151759397.html ; https://www.tradingview.com/news/gurufocus:f185a4aed094b:0-bending-spoons-stocks-jump-nearly-42-although-berkshire-s-33-entry-discounts-yest/ | 원문 직접 (`계산`; 로컬 자료·배포 제외), [기사] |
| F12 | 발표 시각: 미 동부 **10-14 오전 9시 10~15분경(장 시작 전)**. 8:20에 38.04 → 9:15에 최고 50.99 → 9:30 시가 50.29, **첫 5분 안에 장중 최고 58.56** | 10-14 | Yahoo 5분봉(장전 포함) `data/yahoo_bsp_5d_5m_prepost_20261016.json` | [원문 직접] |
| F13 | 버크셔 몫 계산: 6억/29 = 약 **2,069만 주** + 1,000만 주 = 약 3,069만 주, 평균 단가 약 **30.30달러**, 10-14 종가 기준 평가액 약 **16.4억 달러**(투입 9.3억) | — | (계산). 상장 때 산 값이 29달러라는 것은 Business Model Analyst 등 2차 자료의 가정. 회사 자료는 금액(6억)만 밝힘 | (계산) |
| F14 | 버크셔 쪽 말은 **없다**. 보도자료·6-K 모두 버크셔 발언 없음(Yahoo도 같은 지적). 인용은 회사 측 두 사람뿐 | 10-14 | EX-99.1, Yahoo 기사 | [원문 직접] |
| F15 | 6-K: 버크셔에 **"관례적인 등록 권리(registration rights)"**를 준다(나중에 등록해 팔 수 있는 길). 별도 보유 기간 약속은 6-K에 없음. 미등록 주식이라 등록 전에는 Rule 144(보통 6개월 보유)가 걸린다는 해석은 2차 자료 | 10-14 | 6-K 본문; https://businessmodelanalyst.com/bending-spoons-berkshire-private-placement-discount/ | 6-K [원문 직접], 6개월 해석 [기사] |
| F16 | 버크셔 지도부: **그렉 에이블이 2026-01-01부터 CEO**, 워런 버핏은 **이사회 의장으로 남음**(2025-05 이사회 결정). 토드 콤스는 2025-12 JP모건으로 떠남(2026-01 이동). 테드 웨슐러는 남아 있음 | 2025-05 / 2025-12-08 | CNBC(10-14 기사 본문: "CEO Greg Abel took the helm from … Warren Buffett at the start of the year"), Axios https://www.axios.com/2025/12/08/warren-buffett-berkshire-jpmorgan | CNBC 기사 (`curl로 본문 확인`; 로컬 자료·배포 제외), 의장·콤스·웨슐러 [검색 요약만] |
| F17 | Reuters(LSEG 자료): 버크셔는 이 지분으로 **여섯 번째로 큰 주주** | 10-14 | Reuters를 실은 BusinessDay https://www.businessday.co.za/world/international-companies/2026-10-14-berkshire-boosts-bending-spoons-stake-with-330m-investment/ | [기사] |

## 3. 주가의 길

일봉 원자료: `data/bsp_daily_2026-07-01_2026-10-14.csv`, 갱신본 `data/yahoo_bsp_chart_20261016.json`, Nasdaq `data/nasdaq_bsp_hist_20261016.json`.

| 날짜 | 시가 | 고가 | 저가 | 종가 | 거래량 | 메모 |
|---|---|---|---|---|---|---|
| 07-01 | 31.00 | 43.98 | 30.70 | 40.50 | 17.37M | 상장 첫날 |
| 07-13 | 33.36 | 33.66 | 30.97 | **31.78** | 3.56M | 종가 최저 |
| 07-14 | 31.47 | 33.38 | **30.11** | 32.50 | 2.73M | 장중 최저 |
| 08-04 | 36.84 | 38.00 | 34.82 | 37.45 | 2.21M | 에어테이블 인수 발표 |
| 08-11 | 52.99 | **58.94** | 51.87 | 53.44 | 4.47M | 10-14까지의 장중 최고 |
| 08-13 | 46.83 | 46.91 | 39.10 | 40.92 | 4.64M | 2분기 실적(−16.5%) |
| 10-02 | 32.78 | 33.18 | 31.91 | 32.03 | 2.24M | 10월 바닥권 |
| 10-06 | 32.53 | 34.03 | 32.14 | 33.07 | 2.26M | |
| 10-07 | 33.07 | 42.27 | 32.76 | **41.07** | 8.80M | **+24.2%** |
| 10-13 | 36.99 | 38.50 | 36.41 | 37.86 | 1.66M | 버크셔 발표 전날 |
| 10-14 | 50.29 | 58.56 | 49.21 | **53.46** | 19.63M | **+41.2%**, 버크셔 |
| 10-15(장중) | 52.00 | 59.50 | 49.51 | 58.73(11:15 ET) | 3.38M(11:15) | **장중, 종가 아님** |

| 번호 | 사실 | 출처 | 수준 |
|---|---|---|---|
| F18 | 10-07 +24.2%(33.07→41.07). **뚜렷한 재료 없음.** Yahoo Finance(Michael B. Kelley): "closed up 24% on Oct. 7 without an obvious catalyst". 5분봉을 보면 한 번에 뛴 게 아니라 **하루 종일 조금씩 오르다가 마지막 30분(15:30~16:00)에 거래가 몰리며 39→41**. 회사 공시(SEC)는 10-02와 10-14 사이에 없다 | Yahoo 기사(위 F11 링크); `data/yahoo_bsp_2026-10-07_5m.json`; `data/sec_submissions_20261016.json` | 기사 [기사], 5분봉·공시 목록 [원문 직접] |
| F19 | 10-07 원인 추정들(근거 약함): QuiverQuant(AI 작성 표시) "미로 인수 자금 조달 마감(10-02 텀론B 추가 12.5억 달러+3.95억 유로)과 무디스·S&P 신용등급 상향(Ba3, BB-)에 대한 늦은 반응, 모멘텀" | https://www.quiverquant.com/news/Why+Bending+Spoons+(BSP)+Stock+Is+Up+Today | 기사 (`AI 생성 글`; 로컬 자료·배포 제외) |
| F20 | 공매도 잔고(Nasdaq/FINRA): 07-15 854만 → 07-31 1,446만 → 09-15 1,501만 → **09-30 2,014만 주**(평균 거래량으로 갚는 데 6.8일). 10-07 직전 공매도가 급증해 있었다 | `data/nasdaq_bsp_short_interest_20261016.json` | [원문 직접] |
| F21 | 자유롭게 거래되는 주식은 사실상 공모 물량뿐(나머지는 12월 말까지 보호예수, F6). 공모 물량 5,797만(초과배정 포함 6,667만) 대비 공매도 2,014만 = **약 30~35%**. 전체 보통주(3.3억) 대비로는 약 6%, Benzinga는 "short float 5.3%"(다른 분모) | (계산), Benzinga 시세 페이지 https://www.benzinga.com/quote/BSP/sentiment | (계산), Benzinga [검색 요약만] |
| F22 | 10-14 종가 **53.46**(+41.2%), 장중 최고 58.56(+54.7%), 거래량 약 1,963만 주(3개월 평균의 수 배). Bloomberg "장중 최대 55%" | Yahoo/Nasdaq JSON; Yahoo 기사; Bloomberg 제목 | [원문 직접], Bloomberg [검색 요약만] |
| F23 | 10-15 장중(미 동부 11:15): **58.73달러, +9.86%**, 장중 고가 **59.50** = 8-11의 58.94를 넘는 **상장 후 장중 최고**. 장전 거래는 52~53달러로 약세 출발, 시가 52.00, 저가 49.51 | `data/nasdaq_bsp_info_20261016.json`(11:15 ET), Yahoo JSON(11:08 ET) | [원문 직접] — **장중 값이라 종가로 쓰면 안 됨** |
| F24 | 나스닥 종합지수: 10-14 **−1.88%**(26,692.87, "뜨거운 물가 지표에 금리 인상 걱정" 보도), 10-15 장중 −0.36%(11:08 ET). 지수가 빠지는 날 BSP는 +41% | `data/yahoo_ixic_20261016.json`; Yahoo 기사 제목 "Nasdaq ends sharply lower as hot inflation data stirs rate-hike worries" | 지수 [원문 직접], 원인 [검색 요약만] |
| F25 | 공모가 29달러 대비: 10-14 종가 +84%, 10-15 장중 58.73이면 약 +103%(2배) | (계산) | (계산) |
| F26 | 10-09 블룸버그 인터뷰(10-07 이틀 뒤): 페라리 "Valuations in SaaS were unreasonably high and had been for probably a decade." 소프트웨어 값이 떨어진 지금이 인수 기회라는 말. AI가 코드의 90% 이상을 쓴다고 함 | Bloomberg https://www.bloomberg.com/news/articles/2026-10-09/bending-spoons-ceo-sees-buying-opportunities-in-saaspocalypse (차단), Briefs https://www.briefs.co/news/bending-spoons-says-the-saas-slump-is-a-buying-window-turboc/ , 영상 https://www.youtube.com/watch?v=FWKAnmR2Z1g | 인용문 기사 (`Briefs 본문, 출처는 블룸버그로 보임`; 로컬 자료·배포 제외), 90%는 [검색 요약만] |

## 4. 사업 숫자

| 번호 | 사실 | 출처 | 수준 |
|---|---|---|---|
| F27 | 매출: 2023년 3.87억 → 2025년 **13.1억 달러**(연평균 84%). 2025 영업이익 2.78억(이익률 21%), 조정 영업이익 6.13억. **2025 순이익 −20만 달러(사실상 0)**, 2024 순이익 8,900만, 2023 1.61억 | 424B4(창업자 편지·요약 재무) | [원문 직접] |
| F28 | 2025 유기 성장률(인수 효과 뺀 성장) 13% | 424B4 | [원문 직접] |
| F29 | **2026년 2분기**: 매출 **7.04억 달러(+126%)**, 영업이익 2.40억(+139%, 이익률 34%), 조정 영업이익 3.81억(이익률 54%), 순이익 1.77억, 희석 EPS 0.28, 조정 EPS 0.46. **유기 성장률 3%**(트랙티브·위트랜스퍼가 끌고, 레미니·스플라이스 매출은 줄었다) | Q2 6-K EX-99.1 (2026-08-13) `data/sec/20260813_ex99-1.htm.txt` | [원문 직접] |
| F30 | 2분기 이자비용 **1.09억 달러**(1년 전 3,570만). 상반기 2.02억. 2분기 구조조정 비용 5,000만 달러(AOL·이벤트브라이트·트랙티브·비메오 퇴직 패키지) | Q2 EX-99.1, EX-99.2 | [원문 직접] |
| F31 | 6/30 순부채 **40.9억 달러**(장기부채 48.8억 − 현금 7.93억), 레버리지 2.4배 → 회사식 조정 EBITDA(인수 회사 1년치를 다 넣고 예상 비용 절감까지 넣은 값) 약 17억 달러(40.9/2.4) | Q2 EX-99.1 | [원문 직접], EBITDA는 (계산) |
| F32 | 상반기 영업현금흐름 2.54억, 인수에 쓴 현금 22.9억, 새로 빌린 돈 25.7억 | Q2 EX-99.2 | [원문 직접] |
| F33 | 2026 전망(8-12 보유 회사만, 에어테이블·미로 빠짐): 매출 27.8~28.2억(+114%), 조정 영업이익 14.6~15.1억(+142%). 3분기 매출 7.33~7.45억 | Q2 EX-99.1 | [원문 직접] |
| F34 | 상장 뒤 빚: 7월 유로 텀론·리볼버 합계 14.9억 유로(SACE 보증 5억 유로 포함), 9-25 텀론B 추가 12.5억 달러+3.95억 유로(미로 인수용). 그 주에 무디스 B1→Ba3, S&P B+→BB- 상향 | 6-K 07-28, 10-02 | [원문 직접] |
| F35 | 인수: "50건이 넘는 인수"(424B4). 상장 뒤 **에어테이블**(EV 12.85억, 지분가치 약 22.5억, 08-04 발표, 09-04 완료), **미로**(EV 13.55억, 지분가치 17.9억, 09-10 발표, 4분기 마감 예정, 미로 주주 일부가 2.95억 달러를 BSP 신주에 재투자), 트랙티브(EV 7.59억, 2026-05) | 424B4; 6-K 08-04, 09-04, 09-10; Q2 EX-99.1 | [원문 직접] |
| F36 | 사람: 2025년 지원서 약 80만 건, 채용 286명(0.04% 미만). 2분기 신규 채용의 절반 이상이 이탈리아 밖. 월간 사용자 5억 명 이상, 유료 고객 900만 이상(2026-03). 총 직원 수는 원문에서 못 찾음(위키백과 1,743명(2025)은 [검색 요약만]) | 424B4, Q2 EX-99.1 | [원문 직접] |
| F37 | "처음엔 시드 자본 약 4만 달러, 첫 인수에 1만 달러를 냈다. 13년 뒤 수십억 달러짜리 인수를 한다"(창업자 편지, 루카 페라리 서명) | 424B4 | [원문 직접] |

### 가치평가(같은 기준으로 견줌)

기준: 주식 수 6.405억(보통주 3.302억 + A주 3.102억, 초과배정 행사 가정 — Q2의 순수입 11.0억 달러가 회사 몫 3,964만 주×29달러에서 수수료를 뺀 값과 맞아 행사된 것으로 추정). 순부채는 6/30의 40.9억(상장 자금·에어테이블은 반영 안 됨). 조정 영업이익은 회사의 2026 전망 가운데값 14.85억.

| 주가 | 시가총액 | (시총+순부채)/2026 조정영업이익 | 주가/(2분기 조정EPS×4=1.84) | 주가/최근 4분기 순이익(EPS 약 0.39) |
|---|---|---|---|---|
| 29(공모가) | 185.7억 | 15.3배 | 15.8배 | 약 74배 |
| 33(버크셔) | 211.4억 | 17.0배 | 17.9배 | 약 84배 |
| 53.46(10-14 종가) | 342.4억 | **25.8배** | **29.1배** | 약 136배 |

- 최근 4분기 순이익 = 2025 순이익(−0.2백만) − 2025 상반기(−47.0백만) + 2026 상반기(204.4백만) = 2.51억 달러. (계산)
- 보도된 시총: Yahoo "약 330억 달러", Motley Fool 339.6억(초과배정 빼고 6.352억 주로 계산하면 53.46×6.352 = 339.6억과 일치). (계산)
- **조정 영업이익은 인수 무형자산 상각·구조조정 비용·주식보상을 뺀 값**이다. 2분기 순이익(1.77억)과 조정 영업이익(3.81억)의 차이가 크다. 같은 기준끼리만 견줄 것.

### 애널리스트

| 번호 | 사실 | 출처 | 수준 |
|---|---|---|---|
| F38 | 7-27 첫 커버리지(당시 34.06달러): 골드만 매수 43, 미즈호 아웃퍼폼 45, JP모건 중립 35, BofA 중립 37("2028년까지 90억 달러 인수를 이미 반영"), 제프리스 보유 38(인수 걱정), 에버코어 인라인 36. 번스타인 아웃퍼폼 40 | https://www.investing.com/news/stock-market-news/bending-spoons-draws-mixed-analyst-coverage-at-ipo-average-target-implies-14-upside-93CH-4814763 | 표 [기사], BofA 문구·번스타인 [검색 요약만] |
| F39 | 이후: 미즈호 목표 72.28로 상향(8-11, 주가 51.43), JP모건 35→38·에버코어 36→40(8-14), 웰스파고 45→48(9-1). 10-14 미즈호 "목표 유지" 기사 있음(본문 못 읽음) | Investing.com, Benzinga 목표가 페이지 | [검색 요약만] |
| F40 | 10-14 종가 53.46은 미즈호를 뺀 모든 목표가(35~48) 위다 | (F38·F39와 비교) | (계산), 목표가가 검색 요약 수준이라 확인 필요 |

## 5. 사고 나서 자르기(인수 뒤 감원·가격 인상)

| 번호 | 회사 | 사실 | 날짜 | 출처 | 수준 |
|---|---|---|---|---|---|
| F41 | 에버노트 | 미국·칠레 직원 대부분 해고, 유럽으로 옮김(7-05 통보). 몇 명인지 회사는 안 밝힘. 앞서 2월에 약 129명 감원 보도 | 2023-07 | The Verge 제목(캡처 있음) https://www.theverge.com/2023/7/9/23789012/evernote-layoff-us-staff-bending-spoons-note-taking-app ; Engadget | [검색 요약만]+캡처 |
| F42 | 에버노트 | 무료 사용자 노트 50개로 제한 | 2023-11-29 | TechCrunch https://techcrunch.com/2023/11/29/its-official-evernote-will-restrict-free-users-to-50-notes/ | 제목만 [검색 요약만] |
| F43 | 에버노트 | ZDNet(David Berlind, 14년 구독자): 연 **25달러 → 37(2018) → 74(2023) → 138(2024) → 250달러(2025-12 통지)**. "what was once $25 was now 900% more expensive." 새 요금: 100달러에 저장 1GB | 2026-03-25 | https://www.zdnet.com/article/why-i-left-evernote-for-notion/ | 기사 (`curl로 본문`; 로컬 자료·배포 제외) |
| F44 | 필믹 | 원래 팀 22명 전원 11월에 나감(회사 대변인) | 2023-12-04 | https://techcrunch.com/2023/12/04/bending-spoons-lays-off-entire-staff-of-flimic/ | [기사] |
| F45 | 위트랜스퍼 | 인수 뒤 직원 **75% 감원 계획**(직원 350명 넘음). 페라리 직접 발언(아래 인용) | 2024-09-08 | https://techcrunch.com/2024/09/08/bending-spoons-plans-to-lay-off-75-of-wetransfer-staff-after-acquisition/ | [기사] |
| F46 | 위트랜스퍼 | 무료 요금제 월 10회 전송으로 제한 | 2024-12-18 | TechCrunch(캡처 있음) | 제목만 |
| F47 | 브라이트코브 | 2.33억 달러에 인수(2025-02 완료) 뒤 **198명 감원**, 미국 직원의 약 3분의 2 | 2025-03-19 | https://www.boston.com/news/business/2025/03/19/boston-based-streaming-company-brightcove-to-lay-off-198-workers/ | [기사] |
| F48 | 코무트 | 직원 약 150명, 인수 뒤 대규모 감원 예상(숫자 없음). 위키백과는 "4분의 3 감원" | 2025-03-21 | https://www.bikeradar.com/news/komoot-acquisition | [기사], 4분의 3은 [검색 요약만] |
| F49 | 비메오 | 13.8억 달러 인수 뒤 1-20 감원 통보. 회사는 인원 비공개. 뉴욕주 WARN: 뉴욕 사무소 **547명 중 132명**(4-20 효력). "비디오 팀 전체" 등 "대부분"은 전 직원 게시글 근거 | 2026-01-20~23 | Verge/Engadget/Gizmodo 제목(캡처 있음); WARN 수치는 검색 요약 | [검색 요약만] |
| F50 | AOL | 레스턴 사무소 108명 감원 | 2026-02-20 | https://virginiabusiness.com/aol-to-lay-off-108-tied-to-reston-office/ (403) | 제목만 |
| F51 | 이벤트브라이트 | 약 5억 달러 인수(3-10 완료) 뒤 "인수 전 팀의 큰 부분" 감원, 인원 비공개 | 2026-04-13 | Reuters 보도 인용(IQ Magazine, heise 제목) | [검색 요약만] |
| F52 | 트랙티브 | 9억 달러(7.7억 유로, 이연 1.19억 포함) 인수(5-18 완료), 직원 약 300명 중 약 160명 감원 보도(회사 미확인) | 2026-06-30 | https://www.trendingtopics.eu/bending-spoons-pays-e770m-for-tractive-then-cuts-50-of-jobs-before-ipo/ | [기사] |
| F53 | 하베스트 | 요금 체계 변경으로 일부 갱신 요금 최대 **1,500%** 인상. 영국 고객 월 130달러 → **2,110달러**, "daylight robbery". 미국 고객 연 2,800 → 23,000달러 | 2026-08-20 | BBC https://www.bbc.com/news/articles/clyq011414eo | [기사] |
| F54 | **에어테이블** | 09-04 인수 완료 뒤 "인수 전 팀의 큰 부분(a large portion)"과 결별, 주말까지 떠남. 인원 비공개(대변인 "not able to share"). 인수 전 직원 약 800명 | 2026-10-12~13 | Business Insider(Yahoo UK 전재) https://uk.finance.yahoo.com/news/airtables-owner-laying-off-large-211016844.html ; Hoodline https://hoodline.com/2026/10/airtable-guts-pre-acquisition-staff-weeks-after-1-3b-san-francisco-sale/ | [기사] |
| F55 | 에어테이블 | 벤딩스푼스 제품 책임자 Federico Simionato의 X 글이 반발을 삼: "deep belief that small teams ship more and better", "To everyone leaving: thank you. If you're hiring, these are excellent people and worth a call" | 2026-10-12~13 | 위 BI 기사; Fast Company 제목 https://www.fastcompany.com/91622894/bending-spoons-product-lead-sparks-fury-with-x-post-on-airtable-layoffs | 기사 (`BI`; 로컬 자료·배포 제외), Fast Company는 제목만 |
| F56 | 주가와의 시점 | 에어테이블 감원 보도(10-12~13) **바로 다음 날(10-14)** 버크셔 추가 투자 발표 | — | (날짜 대조) | (계산) |

### 더빙에 쓸 수 있는 짧은 인용(원문 확인된 것만)

| 번호 | 누가 | 원문 | 뜻 | 출처 | 수준 |
|---|---|---|---|---|---|
| Q1 | 루카 페라리(CEO) | "We acquire businesses with the intention of owning and operating them for the long term, and Miro will be no exception." | 우리는 오래 갖고 운영하려고 산다. 미로도 예외가 아니다 | 6-K 2026-09-10 EX-99.1 https://www.sec.gov/Archives/edgar/data/2004711/000200471126000015/bsp-20260910x6k.htm | [원문 직접] |
| Q2 | 루카 페라리 | "the vision we developed is of a smaller, more sharply focused WeTransfer organization" | 우리가 그린 위트랜스퍼는 더 작고 더 날카로운 조직이다(=75% 감원 설명) | TechCrunch 2024-09-08 | [기사] |
| Q3 | 루카 페라리 | "Valuations in SaaS were unreasonably high and had been for probably a decade." | 소프트웨어 값은 10년 가까이 터무니없이 비쌌다 | 블룸버그 10-09 인터뷰(Briefs 전재) | [기사] |
| Q4 | 루카 페라리 | "For decades now, Berkshire Hathaway has been among the finest and most respected capital allocators in the world, and is a longstanding inspiration for Bending Spoons." | 버크셔는 오래전부터 우리의 본보기였다 | 10-14 EX-99.1 | [원문 직접] |
| Q5 | 프란체스코 파타르넬로(인수 책임, 공동창업) | "Bending Spoons continuously evaluates M&A opportunities, and our pipeline remains strong." | 살 회사 목록은 여전히 두껍다 | 10-14 EX-99.1 | [원문 직접] |
| Q6 | 회사 소개문 | "has never sold a material business" | 중요한 사업을 판 적이 한 번도 없다 | 10-14 EX-99.1, 424B4 "Divestitures" | [원문 직접] |
| Q7 | 페데리코 시미오나토(제품 책임) | "deep belief that small teams ship more and better" | 작은 팀이 더 많이, 더 잘 만든다(에어테이블 감원 때) | BI 2026-10-12 | [기사] |

## 6. 화면에 쓸 실물

| 무엇 | URL | 보이는 것 | 상태 |
|---|---|---|---|
| 나스닥 타종 영상 | https://www.nasdaq.com/videos/bending-spoons-rings-nasdaq-stock-market-opening-bell | 07-01 타종, 마켓사이트 | 포스터·타워 사진 `production/reel-41/references/photos/` 있음 |
| CNN 타종 영상 | https://edition.cnn.com/2026/07/01/business/video/spending-spoons-nasdaq-ipo-ferrari-live-070104pseg1-cnni-business-fast | 페라리 생방송 | 링크만 |
| Getty 상장일 사진(CNBC 대표 이미지) | https://image.cnbcfm.com/api/v1/image/108329449-1782925310551-gettyimages-2283612305-BENDING_SPOONS_IPO.jpeg | 마켓사이트의 공동창업자 마테오 다니엘리(가운데) | 링크만 |
| Quartz 대표 이미지(Getty) | https://assets.qz.com/media/GettyImages-2283602127.jpg | 10-09 SaaSpocalypse 기사 사진(내용 미확인) | 링크만 |
| 블룸버그 10-09 인터뷰 | https://www.youtube.com/watch?v=FWKAnmR2Z1g | 페라리 "SaaSpocalypse" 인터뷰 | 접촉 시트 `references/video/sheets/FWKAnmR2Z1g.jpg` |
| 블룸버그 10-14 | https://www.youtube.com/watch?v=4GkPqYAXSds | "Bending Spoons Stock Soars on Berkshire's Increased Stake" | 시트 있음 |
| 블룸버그 상장일 | https://www.youtube.com/watch?v=auV52do1eCs | "AOL Owner Bending Spoons Jumps After $1.68 Billion IPO" | 시트 있음 |
| 폭스비즈니스 | https://www.youtube.com/watch?v=Qr5GBykX910 | CEO가 인수 공식 설명 | 시트 있음 |
| CNBC | https://www.youtube.com/watch?v=xGbvIX8rGHM | 페라리, AOL 인수에 대해 | 목록만 |
| 회사 채널 | https://www.youtube.com/watch?v=_fEsJ613rq0 | "Inside Bending Spoons: Going public, Startup Mode, and AI alter-egos"(사무실·사람) | 목록만 |
| Class CNBC 단독 인터뷰 | https://www.youtube.com/watch?v=6xKYKjfOU6M | 페라리 이탈리아어 인터뷰 | 목록만 |
| 소서리 팟캐스트 | https://www.youtube.com/watch?v=3IUnY8btQQo | 창업자들, 에어테이블·AOL·비메오·이벤트브라이트 인수 | 목록만 |
| 투자자 사이트 | https://investors.bendingspoons.com/ | 보도자료·실적 자료 | 링크만 |
| 기사 캡처 55건 | `production/reel-41/references/captures/` (목록 `_tools/pshot.jsonl`) | 감원·가격 인상·버크셔 기사 제목 | 있음 |
| ZDNet 가격 통지 화면 | 위 F43 기사 안 이메일 캡처 | 250달러 통지 | 기사 안 그림, 미수집 |
| BBC 하베스트 | F53 기사 | 고객 사진, 1500% | 미수집 |

버크셔 주총(2026-05, 에이블 첫 주총) 영상은 이번에 찾지 않았다.

---

## 엇갈리는 보도

1. **10-14 상승률**: CNBC 41%, Yahoo 41%, Benzinga 45%, Reuters 34%(51.10달러 시점), Barron's·RTT 35%, Bloomberg "장중 최대 55%", BigGo 55%. → 쓴 시각이 달라서다. **종가 기준은 +41.2%(37.86→53.46)**, 장중 최고는 +54.7%(58.56). StocksToTrade는 종가 "약 53.25" — Yahoo·Nasdaq 원자료는 53.46.
2. **누가 샀나**: IBD는 "Berkshire Hathaway CEO **Greg Abel** has made a fresh $330 million bet"(에이블 본인 결정처럼 씀). CNBC는 "에이블이 CEO가 된 뒤의 투자 결정"까지만. Motley Fool·billionaires.africa 제목은 "**Warren Buffett's** Berkshire". 회사·SEC 문서는 "Berkshire Hathaway"만 쓰고, 누가 결정했는지 밝힌 1차 자료는 **없다**. 웨슐러가 했다는 보도도 못 찾음. → 대본에서 "버핏이 샀다"는 쓰면 안 된다. "버크셔가"로.
3. **지분 4%가 계산과 안 맞는다**: 6억/29 = 2,069만 주 + 1,000만 = 3,069만 주. 상장 후 주식 6.40억+1,000만 = 6.50억 → **4.7%**. 회사는 "4%". 상장 때 29달러보다 비싸게 샀거나(예: 첫날 시장에서), 분모에 미로 주주 신주·주식보상 등이 들어갔거나, 반올림 기준이 다를 수 있다. 원인을 밝힌 자료 없음. Q3 13F(11월 중순 마감)가 나오면 확인 가능.
4. **상장 때 버크셔 6억 달러를 언제 알았나**: 회사는 10-14에 "상장 때 6억 달러 투자"라고 처음 밝힌 것으로 보인다. 424B4에 버크셔 언급 없음. 7월 보도는 못 찾음. 검색으로 확인 못 했을 뿐 "숨겼다"고 단정하면 안 된다.
5. **10-07 +24%의 이유**: Yahoo "뚜렷한 재료 없음" vs QuiverQuant(AI 작성) "미로 자금 조달·신용등급 상향 늦은 반응". 공시 없음. 공매도 2,014만 주(9-30)와 마지막 30분 거래 폭증은 **숏커버링 가능성**을 시사하지만 이를 말한 보도는 못 찾음(작업자 추정).
6. **52주 최저가**: Yahoo·Nasdaq 원자료 장중 최저 30.11(07-14). Motley Fool·Robinhood는 "29.00"(공모가를 넣은 것으로 보임). → 30.11이 거래된 값.
7. **장중 최고 기록**: Yahoo 기사(10-14)는 "8-11의 58.94가 장중 최고, 10-14는 58달러로 못 미침". 10-15 장중 59.50(Nasdaq 11:15 ET)으로 **기록 경신 중**. 종가는 아직 모름.
8. **트랙티브 인수가**: 회사 2분기 자료 "EV 7.59억 달러(이연 1.15억 포함)" vs Trending Topics "9억 달러(7.7억 유로, 이연 1.19억)". 기준(EV와 총대가)이 다를 수 있다. 영상에는 회사 숫자.
9. **브라이트코브 인수가**: 보스턴닷컴 2.33억 달러, 위키백과 표 2.23억. → 2.33억(기사).
10. **AOL 인수**: 위키백과 본문 2025-10·15억 달러 vs 표 2026-01·14억 달러. 1차 자료 확인 안 함.
11. **비메오 감원 규모**: "대부분, 비디오 팀 전체"(전 직원 게시글 근거, Gizmodo·Engadget) vs 공식 숫자는 뉴욕 사무소 547명 중 132명(WARN)뿐. "대부분"은 확인되지 않은 말.
12. **에어테이블 X 글 주인공**: Fast Company 제목은 "product lead"의 X 글. BI 본문은 X에 글을 쓴 사람이 벤딩스푼스의 Federico Simionato, 블로그 글은 에어테이블 제품 책임 Alessandro Savarese. 다른 요약은 Savarese를 X 글 작성자로 적음 → BI 본문을 따름.
13. **공매도 비율**: Benzinga "short float 5.3%" vs 작업자 계산(거래 가능 공모 물량 대비 30~35%). 분모가 다르다. 대본에 쓰려면 "빌려 판 주식 2,000만 주, 시장에 풀린 주식의 3분의 1쯤"처럼 분모를 밝히고 쓴다.

## 아직 확인 못 한 것

- 10-15 종가와 시간외, 10-16 장전(조사 시각에 미국 장중).
- 10-14 이후 애널리스트 목표가 변경(미즈호 "유지" 기사 본문 못 읽음).
- Reuters·Bloomberg·WSJ·FT 본문(차단). WSJ 9-11 "At Bending Spoons, the Numbers Are the Real Mind-Bender", Forbes 7-6 "AOL·비메오·이벤트브라이트에 33억 달러, 2025 프로포마 이익 2,200만 달러"는 제목만.
- 3분기 실적 발표일.
