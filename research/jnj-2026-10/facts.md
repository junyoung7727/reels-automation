# 존슨앤드존슨: 이익은 넘었는데 하루 −5.73% (2026-10-13)

조사한 때: 2026-10-14(수) 18:20~ KST (미국 동부 05:20~, 10-14 개장 전). 미국주식 분석 시리즈 4편 후보 A의 심화 조사. 앞 조사 `research/us-series-4-2026-10-14/candidates.md`의 A절에서 확인된 것은 다시 하지 않고, 원문으로 올리거나 숫자를 더했다.

확인 표기: **원문 읽음** = 회사·기관·기자의 원문을 직접 받아 읽음 / **시세** = 야후 차트 API(배당 반영 수정가 포함)와 나스닥 일별 API로 받은 값 / **계산** = 그 자료로 직접 계산(스크립트는 `data/scripts/`) / **2차 자료** = 원 보도를 옮긴 글이나 녹취 요약만 읽음 / **검색 요약** = 검색 결과 요약뿐, 원문 미확인.

시세: 야후 `query1.finance.yahoo.com/v8/finance/chart/<T>`(2009-01-02~2026-10-13, 사본 `data/prices/JNJ.json`, `SPY.json`)를 기준으로 쓰고, 나스닥 일별 API(2016-10-13~, `data/prices/nasdaq_jnj.json`)로 10-13, 10-12, 2025-04-01, 2025-03-31, 2018-12-14, 2018-12-13, 2019-10-18, 2019-10-17 종가를 맞춰 봤다. 다른 값은 없었다. 총수익(배당 포함)은 야후 수정 종가(adjclose)로 쟀다. 1개월·3개월·1년은 21·63·252 거래일 뒤 종가.

원문 사본: `data/sec/`(8-K 첨부 99.1, 99.2, 10-K·10-Q 발췌 텍스트), `data/web/`(모틀리풀 녹취, CNBC, 야후, FactSet 10-09).

---

## 1. 한 문단

존슨앤드존슨(J&J)은 2026-10-13 개장 전 3분기 실적을 냈다. 매출 253.99억 달러(+5.9%), 조정 주당이익 2.59달러로 예상(LSEG 2.54, Zacks 2.53, FactSet 2.50)을 넘었고 2026년 조정 주당이익 전망 가운데값을 11.04 → 11.10달러로 올렸다. 그런데 주가는 263.73 → 248.61달러(−5.73%)로 떨어졌다. S&P500 ETF는 그날 −0.01%였다. **2010년 이후 J&J가 실적을 낸 날(8-K 2.02 제출일 71번) 가운데 가장 큰 하락**이고, 그다음은 2018-01-23의 −4.26%다. 까닭은 매출의 34%인 의료기기(MedTech)다: 86.42억 달러(+2.5%)로 두 분기 연속 예상에 못 미쳤고, 미국 밖 의료기기는 41.30억 달러로 +0.1%, 사실상 제자리였다(2분기에는 +3.2%). 예상과의 차이는 6,800만~9,800만 달러(전체 매출의 0.3~0.4%)인데, 그날 시가총액은 약 364억 달러가 줄었다. 하락 전 J&J는 올해 +27.4%로 S&P500(+14.1%)의 두 배를 올랐고, 그사이 2026년 이익 전망(보고 기준)은 오히려 11.53 → 11.10달러로 내려갔다. 값은 2026 예상 이익의 22.4배로, 자기 10년 평균(약 16~17배)과 S&P500(19.1배)보다 높다.

---

## 2. 3분기 숫자 (8-K, 2026-10-13)

출처: 첨부 99.1 https://www.sec.gov/Archives/edgar/data/200406/000020040626000189/a2026q3exhibit991.htm , 첨부 99.2(지역·사업별 매출) https://www.sec.gov/Archives/edgar/data/200406/000020040626000189/a2026q3exhibit992.htm . 사본 `data/sec/q3_2026_ex991.txt`, `q3_2026_ex992.txt`.

| F | 사실 | 확인 |
|---|---|---|
| F1 | 매출 253.99억 달러(전년 239.93억, +5.9%, 환율 뺀 영업 성장 +6.0%). 미국 149.59억(+9.1%), 미국 밖 104.40억(+1.5%) | 원문 읽음 |
| F2 | 의약품(Innovative Medicine) 167.57억 달러, +7.7%(영업 +7.9%). 미국 104.47억(+11.1%), 미국 밖 63.10억(+2.4%) | 원문 읽음 |
| F3 | **의료기기(MedTech) 86.42억 달러, +2.5%**(영업 +2.5%). **미국 45.12억(+4.8%), 미국 밖 41.30억(+0.1%, 전년 41.24억)** | 원문 읽음 |
| F4 | 매출에서 의료기기의 몫: 86.42 ÷ 253.99 = **34.0%(약 3분의 1)**. 의약품 66.0%. 미국 밖 의료기기만은 전체의 16.3% | 계산 |
| F5 | 의료기기 사업별(3분기, 전년 대비 보고 기준): 심혈관 23.07억(+4.3%. 그 안에 전기생리 14.87억 +4.9%, **아비오메드 4.12억 −2.3%**, 쇼크웨이브 3.25억 +16.8%) / 수술 25.28억(−0.6%, 미국 +3.7%, 미국 밖 −3.4%) / 시력 14.61억(+4.4%) / **정형외과 23.45억(+3.2%. 엉덩이 4.19억, 무릎 3.86억, 외상 8.44억, 척추·스포츠 등 6.97억)** | 원문 읽음 |
| F6 | 정형외과는 의료기기의 27.1%, 전체 매출의 9.2% | 계산 |
| F7 | 조정 주당이익 2.59달러(전년 2.80, −7.5%). 보고 주당이익 0.09달러(전년 2.12). 보고 순이익 2.10억 달러: 난소암 활석 소송 해결 55억 달러 등 일회성 비용. 조정 이익에는 파이어플라이 바이오 인수의 연구개발비 약 10억 달러가 들어 있다 | 원문 읽음(8-K, 녹취) |
| F8 | 예상 대비: LSEG 2.54달러(+5센트, CNBC), Zacks 2.53달러(+6센트, 나스닥·벤징가 자료), FactSet 평균 2.50달러(FactSet Earnings Insight 10-09: "Johnson & Johnson (to $2.50 from $3.02)", 6월 30일보다 낮아진 것은 파이어플라이 비용 때문) | 원문 읽음(CNBC, FactSet PDF), 2차 자료(Zacks 값은 벤징가 페이지 데이터) |
| F9 | 매출 예상 252.8억 달러(LSEG)를 넘었다 | 원문 읽음(CNBC 인베스팅클럽 10-13) |
| F10 | 의료기기 예상: LSEG 87.1억 달러(CNBC 본기사), StreetAccount 87.4억 달러(CNBC 장중 정리). 차이 6,800만~9,800만 달러 | 원문 읽음(CNBC), 계산 |
| F11 | **2026 전망(10월 vs 7월 29일)**: 조정 주당이익 11.05~11.15, 가운데값 **11.10달러**(7월 29일 10.96~11.11, 가운데값 11.04). 보고 매출 1,010억~1,014억, 가운데값 1,012억 달러(+7.4%)(7월 29일 가운데값 1,011억). 영업 매출 성장 가운데값 6.9%(7월 6.8%) | 원문 읽음 |
| F12 | 올해 조정 주당이익 전망의 변화: 1월 21일 11.43~11.63(가운데값 11.53) → 7월 15일 11.60~11.75(11.68) → 7월 29일 10.96~11.11(11.04, 파이어플라이·세일 거래 반영) → 10월 13일 11.05~11.15(11.10). 거래 영향을 빼면 지금 전망은 11.74달러 꼴(11.10 + 0.64) | 원문 읽음(2025년 4분기 8-K 첨부 99.1, 2026년 2분기 8-K 첨부 99.1, 사본 `data/sec/q4_2025_ex991.txt`, `q2_2026_ex991.txt`), 계산 |
| F13 | 의약품 주요 제품(3분기): 트렘피어 23.96억(+68.3%), 다잘렉스 42.39억(+15.4%), 스텔라라 7.16억(−54.4%, 복제약), 폐동맥고혈압 8.97억(−19.5%, 그중 옵서밋 3.72억 −35.7%), 자렐토 6.53억(+2.7%, 미국만), 카플리타 3.98억(+66.1%), 스프라바토 6.24억(+36.1%), 카빅티 7.10억(+35.5%) | 원문 읽음 |
| F14 | 의료기기 2분기와 비교: 미국 밖 의료기기 영업 성장 2분기 **+3.2%** → 3분기 **+0.1%**. 미국 밖 수술 2분기 +0.5% → 3분기 −4.2%(영업). 미국 밖 정형외과 +5.3% → +2.9% | 원문 읽음(2분기 8-K 첨부 99.2, `data/sec/q2_2026_ex992.txt`) |
| F15 | 3분기 미국 밖 의료기기가 2분기의 속도(+3.2%)로 자랐다면 약 42.6억 달러였다. 실제와의 차이 약 1.3억 달러(전체 분기 매출의 0.5%). 중동·유럽·중국·아비오메드를 다 합친 미국 밖 둔화의 크기가 이 정도다 | 계산 |
| F16 | 하락으로 줄어든 시가총액: 발행주식 24억 990만 주(2026-07-17, 2분기 10-Q 표지) × 15.12달러 = **약 364억 달러** | 원문 읽음(10-Q), 계산 |

## 3. 경영진의 말 (원문)

녹취: 모틀리풀 "J&J (JNJ) Q3 2026 Earnings Call Transcript" https://www.fool.com/earnings/call-transcripts/2026/10/13/jj-jnj-q3-2026-earnings-call-transcript/ (사본 `data/web/fool_q3_2026_transcript.txt`). J&J 공식 녹취 PDF는 아직 없다(2분기 것은 `s203.q4cdn.com/.../2026/q2/JNJ-USQ_Transcript_2026-07-15.pdf`에 있으나 3분기 같은 경로는 404, 10-14 18:30 KST).

| F | 누가, 어디서 | 원문 | 확인 |
|---|---|---|---|
| F17 | **조 월크 CFO, CNBC 인터뷰**(10-13. 실적 콜이 아님) | "These are countries that still value and actually want premium healthcare systems, think Kuwait, UAE, Saudi Arabia. They pride themselves on having solid healthcare, very good healthcare," … "But their budgets now are being resourced and allocated towards defense." / 중동 분쟁·유럽 긴축·중국 가격이 계속 눌렀고 "but maybe in a little bit more pronounced way." https://www.cnbc.com/2026/10/13/jnj-earnings-q3-2026.html | 원문 읽음. **모틀리풀 콜 녹취에는 쿠웨이트·UAE·사우디라는 말이 없다** |
| F18 | 월크, 야후 파이낸스 인터뷰(10-13) | "If you think about the war in the Middle East, it's not that the demand isn't there," … "It's just that budgets are now being allocated from some of the surrounding countries on defense versus healthcare. But because the demand is there, we think that passes over time, because we know these are countries that do prioritize top, premium healthcare. So we think that'll remedy itself as we move into 2027." https://finance.yahoo.com/markets/article/johnson--johnson-stock-falls-despite-strong-earnings-as-investors-focus-on-medtech-unit-161450981.html | 원문 읽음 |
| F19 | **팀 슈미드 의료기기 총괄, 콜 질의응답**(씨티 조앤 웬쉬의 질문에) | "And to be clear, our performance is below the standard. We have set internally and below the expectations we previously communicated to investors. **Simply put, we can do better, and we absolutely will.** And right now, we are focused solely on the actions needed to deliver stronger results in the fourth quarter and beyond." 이어서 압박은 두 곳이라고 했다: "Firstly, our performance outside of the U.S. … And secondly, Abiomed globally". 중동은 "We did introduce a new headwind, which is really the incremental pressure that we are seeing on the business due to the conflict in The Middle East." | 원문 읽음(녹취의 마침표 위치는 녹취사 표기. CNBC는 "below the standard we have set internally"로 이어 적었다) |
| F20 | 슈미드, 레이먼드제임스 제이슨 베드퍼드가 "중동과 중국 집중구매(VBP)의 영향을 숫자로 말해 줄 수 있나" 묻자 | 숫자는 주지 않았다. "the effect is no longer limited to a few markets as we initially thought. We have seen increased disruption to ordering patterns, tender timing in spending decisions across a wider group of countries, unfortunately. … governments and health care systems become more cautious in their spending priorities" / "we would expect many of these opportunities to be deferred rather than permanently lost." | 원문 읽음 |
| F21 | 월크, 콜 첫머리 | "We are clear on where med tech performance needs to improve. Specifically cardiovascular and surgery outside The U.S. and are taking action to strengthen results. While disappointing, the underlying fundamentals of the med tech business remains strong" / 골드만 질문에 "it is an urgency to fix what we currently have." | 원문 읽음 |
| F22 | 호아킨 두아토 회장 겸 CEO, 실적 발표문 | "Johnson & Johnson's strong third-quarter performance and increased sequential growth reflect the accelerating momentum of our focused portfolio." / "…gives us clearer line of sight to double-digit growth by the end of the decade." | 원문 읽음(8-K) |
| F23 | 두아토, 콜 | "we are on track to meet our guidance and exceed $100 billion in annual revenue for the first time in our company's 140 year history." / 맺음말: "these drivers position Johnson & Johnson as 1 of the cleanest growth stories in healthcare." | 원문 읽음(녹취) |
| F24 | 슈미드, 아비오메드 | "Abiomed remains a temporary headwind as you saw in Q3 … The slowdown we are seeing continues to be the same issue we highlighted in the quarter before, which is the study outside of the U.S. Focused on high risk PCI" / "a study where we actually believe that the methodology employed did not follow well established practices" | 원문 읽음 |
| F25 | J.P.모건 로비 마커스(CNBC 인용) | J&J 결과를 업계 전체로 넓혀 읽기 어렵다: 중국 공급 문제, 정형외과 분사, 그리고 "likely greater exposure to disruption in the Middle East" | 원문 읽음(CNBC가 옮긴 말) |
| F26 | 같은 날 다른 의료기기 주식 | 보스턴사이언티픽 약 −3%, 인튜이티브서지컬 약 −2% | 원문 읽음(CNBC). 종가는 확인 안 함 |

## 4. 중동은 얼마나 큰가 — 회의적인 질문에 대한 답

| F | 사실 | 확인 |
|---|---|---|
| F27 | **J&J는 중동 매출을 따로 밝히지 않는다.** 지역은 미국 / 유럽 / 미국 밖 서반구 / 아시아태평양·아프리카 넷뿐이고, 중동이 어느 칸에 드는지도 적지 않는다(2025 10-K: 미국 밖 매출 약 43% = 유럽 23%, 미국 밖 서반구 5%, 아시아태평양·아프리카 15%) | 원문 읽음(10-K 2026-02-11, `jnj-20251228.htm`) |
| F28 | 3분기 지역 매출: 유럽 54.05억(−0.6%, 영업 +1.0%), 아시아태평양·아프리카 36.50억(+1.0%), 미국 밖 서반구 13.85억(+12.5%) | 원문 읽음(첨부 99.2) |
| F29 | 2분기 10-Q(2026-07-23): "The financial impact of known existing conflicts in the fiscal second quarter of 2026 was not material." 3분기 10-Q는 아직 나오지 않았다 | 원문 읽음 |
| F30 | 슈미드는 콜에서 중동 영향을 숫자로 묻는 질문에 숫자를 주지 않았다(F20). 시틀라인(메드텍 인사이트)도 "did not quantify the impact of the Middle East situation and VBP"라고 썼다 https://insights.citeline.com/medtech-insight/business/earnings/jj-medtech-falls-short-in-q3-as-middle-east-china-and-abiomed-weigh-on-growth-PP3B7GWYDZHGPA3KJNGAKDGVEU/ | 원문 읽음(녹취), 2차 자료(시틀라인은 앞부분만 읽힘) |
| F31 | 그래서 말할 수 있는 크기의 상한: 미국 밖 의료기기 둔화 전체가 분기 약 1.3억 달러(F15), 의료기기 예상과의 차이가 6,800만~9,800만 달러(F10). 중동은 그 가운데 일부다. 회사 전체 매출의 0.5%를 넘지 않는다 | 계산 |

## 5. 영국 심장 펌프 연구

| F | 사실 | 확인 |
|---|---|---|
| F32 | 연구: **CHIP-BCIS3**(Controlled trial of High-risk coronary Intervention with Percutaneous left ventricular unloading). 영국 21개 병원, 환자 300명(평균 73세). 제품: 아비오메드(J&J) **임펠라 CP** 심장 펌프. 고위험 관상동맥 시술(PCI) 때 미리 펌프를 넣은 쪽과 안 넣은 쪽을 비교 | 원문 읽음(TCTMD 2026-03-29 https://www.tctmd.com/news/impella-support-high-risk-pci-doesnt-help-might-harm-chip-bcis3) |
| F33 | 발표: 2026-03-29 미국심장학회(ACC 2026, 뉴올리언스), 같은 날 NEJM 게재. 주 평가에서 표준 치료가 앞섰다(승률비 0.85, P=0.30). 심혈관 사망 26.7% 대 14.5%(위험비 1.91). 발표자 디바카 페레라(런던 세인트토머스 병원): "These results will give pause for thought in that we need to reconsider routine use of it." | 원문 읽음(TCTMD) |
| F34 | 메드텍다이브(2026-04-01): 사망 47명 대 33명. 페레라: "Our findings strongly suggest that we shouldn't be using this device routinely without more evidence of benefit." 임펠라는 2025년 J&J 매출에 17.5억 달러를 보탰다. J&J 대변인: "We remain committed to studying this vulnerable population using targeted therapies." https://www.medtechdive.com/news/johnson-jnj-impella-heart-pump-ACC-no-patient-benefit-2-trials/816332/ | 원문 읽음 |
| F35 | 결과: 아비오메드 매출 2분기 4.40억(−2.0%) → 3분기 4.12억(−2.3%), 두 분기 연속 감소. J&J는 2022년 166억 달러에 아비오메드를 샀다. 회사는 더 큰 연구 PROTECT IV(약 1,250명) 결과를 2027년에 기다린다 | 원문 읽음(8-K 첨부 99.2, 메드텍다이브 10-13, 녹취) |
| F36 | 월크가 야후에 꼽은 두 문제: "a study earlier this year in the UK questioning the company's heart pump benefits in some high-risk procedures, and geopolitical conflict" — 이 연구가 CHIP-BCIS3인 것은 시기·나라·제품이 맞아 사실상 확실하다. 2분기 시틀라인 제목도 "J&J Blames UK Impella Trial For Abiomed Decline As Q2 Cardiovascular Slips" | 원문 읽음(야후 기사 문장), 연결은 추론(높음) |

## 6. 값: 같은 자로 잰 PER과 배당 (2026-10-13 종가)

자: 주가는 야후 10-13 종가, 이익 예상은 나스닥 analyst API(Zacks 집계, `data/prices/zacks_forecast_*.json`), 배당은 야후 배당 기록(최근 1회 × 4 = 지시 배당, 지난 12개월 합 = 실제). 스크립트 `data/scripts/val.py`.

| F37 | 종목 | 10-13 종가(그날) | 2026 예상 EPS(명) | 2026 PER | 2027 예상 EPS(명) | 2027 PER | 지시 배당수익률(지난 12개월) |
|---|---|---|---|---|---|---|---|
| | **J&J** | **248.61 (−5.73%)** | 11.09 (6) | **22.4배** | 12.33 (6) | **20.2배** | **2.16%** (2.12%) |
| | 머크 MRK | 141.98 (−2.39%) | 2.66 (8)* | 53.4배* | 9.27 (8) | 15.3배 | 2.39% (2.39%) |
| | 애브비 ABBV | 274.36 (−2.40%) | 13.95 (7) | 19.7배 | 16.04 (10) | 17.1배 | 2.52% (2.49%) |
| | 화이자 PFE | 28.37 (−0.11%) | 2.96 (9) | 9.6배 | 2.95 (9) | 9.6배 | 6.06% (6.06%) |
| | 일라이릴리 LLY | 1,166.51 (−1.36%) | 34.79 (9) | 33.5배 | 46.82 (9) | 24.9배 | 0.59% (0.57%) |
| | 애보트 ABT | 102.61 (+0.78%) | 5.52 (11) | 18.6배 | 6.08 (11) | 16.9배 | 2.46% (2.42%) |
| | 메드트로닉 MDT | 93.01 (+1.17%) | 5.98 (11, 2027년 4월 끝 회계연도) | 15.6배 | 6.36 (9, 2028년 4월) | 14.6배 | 3.10% (3.07%) |
| | 스트라이커 SYK | 282.55 (−0.02%) | 14.96 (11) | 18.9배 | 16.63 (11) | 17.0배 | 1.25% (1.25%) |

확인: 시세, 원문 읽음(집계값), 계산.

| F | 사실 | 확인 |
|---|---|---|
| F38 | S&P500 앞으로 12개월 PER **19.1배**: 5년 평균 19.8배보다 낮고 10년 평균 19.1배와 같다. 뒤 12개월 PER 26.0배. (FactSet Earnings Insight, **2026-10-09** 발행, 10-08 종가 7,765.36 기준) https://advantage.factset.com/hubfs/Website/Resources%20Section/Research%20Desk/Earnings%20Insight/EarningsInsight_100926.pdf | **원문 읽음**(앞 조사에서는 검색 요약이었다. PDF를 받아 확인. 사본 `data/web/factset_earnings_insight_2026-10-09.txt`) |
| F39 | S&P500 배당수익률 1.04%(multpl.com, 10-13) | 앞 조사(candidates.md)의 값을 그대로 씀. 이번에 다시 열지 않음 |
| F40 | 같은 FactSet: 6월 30일 뒤 헬스케어 업종 이익 예상이 −4.1%로 두 번째로 크게 줄었는데 업종 주가는 +5.9%로 세 번째로 많이 올랐다. 이익 예상 감소에 가장 크게 기여한 회사가 J&J(3분기 예상 3.02 → 2.50달러) | 원문 읽음 |
| F41 | 2027 기준 PER: J&J 20.2배, 비교 일곱 회사의 가운데값 16.9배(머크 15.3, 애브비 17.1, 화이자 9.6, 릴리 24.9, 애보트 16.9, 메드트로닉 14.6, 스트라이커 17.0). J&J보다 비싼 것은 릴리 하나 | 계산 |
| F42 | J&J의 앞으로 12개월 PER(S&P500과 같은 꼴로 맞추면): 2026의 1/4 + 2027의 3/4 가중 → 이익 12.02달러, **20.7배**. 분기 예상 넷(4분기 2.93 + 2027년 1~3분기 2.76·2.96·2.92, 2027년 분기는 1명뿐)을 더하면 11.57달러, 21.5배 | 계산 |

**견줄 때 조심할 것**
- 머크의 2026 EPS 2.66달러는 일회성 비용(인수 연구개발비로 짐작, 까닭은 확인 안 함) 때문에 눌린 값이라 2026 PER 53배는 쓸 수 없다. 2027 열로 견준다.
- 메드트로닉은 회계연도가 4월에 끝난다. 2027년 4월 끝 연도를 "2026"칸에 넣었다.
- J&J의 2026 EPS 11.09달러에는 파이어플라이·세일 거래의 일회성 연구개발비 0.64달러가 들어 있다(J&J 조정 이익은 인수 연구개발비를 빼지 않는다). 그걸 빼면 11.74달러, PER 21.2배.
- J&J의 2027 예상 12.33달러에 세일 옵션 행사 비용(1.28달러)이 들어 있는지는 알 수 없다(F57).
- S&P500은 "앞으로 12개월" 이익, 종목들은 "역년" 이익이다. 같은 꼴로 맞춘 J&J 값은 F42.
- Zacks 집계는 표본이 적다(J&J 6명). FactSet·LSEG의 J&J 컨센서스는 받지 못했다.
- 벤징가 페이지의 J&J "forwardPE"는 19.6배로, 이 표와 기준이 다르다. 섞어 쓰지 않는다.

## 7. J&J 자기 역사의 PER

FactSet·모닝스타 같은 곳의 "J&J 앞으로 12개월 PER 5년·10년 평균"은 찾지 못했다(검색에 나온 사이트들의 값은 회계 이익 기준이거나 날짜·방법이 불분명해 쓰지 않음). 그래서 직접 쟀다.

방법: 회사가 매년 1월 4분기 실적 발표에서 밝힌 그해 **조정 주당이익(실제)** 을 SEC 8-K 첨부 99.1에서 읽고(`data/sec/annual_q4_releases/`), 야후 연말 종가로 나눴다. "연초 PER" = 전년 말 종가 ÷ 그해 실제 조정 EPS(그해 이익을 미리 알았다면의 앞 PER). "연말 PER" = 그해 말 종가 ÷ 그해 조정 EPS. 스크립트 `data/scripts/pe.py`.

| F43 | 연도 | 조정 EPS(실제) | 전년 말 종가 | 연초 PER | 그해 말 종가 | 연말 PER |
|---|---|---|---|---|---|---|
| | 2016 | 6.73 | 102.72 | 15.3 | 115.21 | 17.1 |
| | 2017 | 7.30 | 115.21 | 15.8 | 139.72 | 19.1 |
| | 2018 | 8.18 | 139.72 | 17.1 | 129.05 | 15.8 |
| | 2019 | 8.68 | 129.05 | 14.9 | 145.87 | 16.8 |
| | 2020 | 8.03 | 145.87 | 18.2 | 157.38 | 19.6 |
| | 2021 | 9.80 | 157.38 | 16.1 | 171.07 | 17.5 |
| | 2022 | 10.15 | 171.07 | 16.9 | 176.65 | 17.4 |
| | 2023 | 9.92 | 176.65 | 17.8 | 156.74 | 15.8 |
| | 2024 | 9.98 | 156.74 | 15.7 | 144.62 | 14.5 |
| | 2025 | 10.79 | 144.62 | 13.4 | 206.95 | 19.2 |
| | 평균 2016~2025 | | | **16.1** | | **17.3** |
| | 평균 2021~2025 | | | **16.0** | | **16.9** |
| | 2026(전망 11.10) | 11.10 | 206.95 | 18.6 | 10-12: 263.73 → **23.8** / 10-13: 248.61 → **22.4** | |

- 확인: 원문 읽음(EPS: 2016~2024년 1월 8-K, 2025는 2026-01-21 8-K "$10.79"), 시세, 계산.
- 조심: 2023년 8월 켄뷰(소비자 사업) 분리, 2024년부터 인수 연구개발비를 조정 이익에서 빼지 않는 것으로 바뀜 등 기준이 해마다 같지 않다. "대략 16~17배"로만 쓴다.

## 8. 전례: 하루 5% 넘게 빠진 날 (2010-01-01 ~ 2026-10-13)

방법: 야후 일별 종가로 전일 대비 −5% 이하인 날을 모두 찾고, 그날 종가에서 21·63·252 거래일 뒤까지의 주가 수익률과 총수익률(배당 포함, 수정가)을 쟀다. S&P500은 SPY 총수익률. 스크립트 `data/scripts/drops.py`. **2010~2017년에는 그런 날이 하나도 없었다.**

| F44 | 날짜 | J&J 그날 | SPY 그날 | 까닭 | J&J 1개월 / 3개월 / 1년 (배당 포함) | SPY 같은 기간(배당 포함) |
|---|---|---|---|---|---|---|
| | 2018-02-05 | −5.29% | −4.18% | 시장 전체 급락일 | −0.4% / −4.6% / +4.8% | +3.4% / +1.5% / +5.3% |
| | **2018-12-14** | **−10.04%** | −1.85% | 로이터: "J&J는 수십 년 동안 활석에 석면이 있다는 것을 알았다" 보도. 16년여 만의 최대 하락 | −3.7% / +4.8% / +9.6% | +0.8% / +9.5% / +25.1% |
| | **2019-10-18** | **−6.22%** | −0.44% | FDA가 베이비파우더 한 병에서 석면 흔적 → 3만 3천 병 회수 | +5.6% / +17.7% / +16.1% | +4.7% / +11.7% / +17.0% |
| | 2020-03-11 | −6.95% | −4.87% | 코로나 폭락 | +7.2% / +12.9% / +24.0% | +2.0% / +17.0% / +46.1% |
| | 2020-03-16 | −5.33% | −10.94% | 코로나 폭락 | +16.1% / +11.9% / +30.4% | +16.5% / +28.8% / +68.1% |
| | 2020-03-19 | −5.86% | +0.21% | 코로나 폭락 기간 | +19.4% / +13.7% / +29.4% | +17.8% / +30.4% / +65.5% |
| | 2020-03-20 | −5.64% | −4.87% | 코로나 폭락 | +24.8% / +20.8% / +37.5% | +19.3% / +35.5% / +74.3% |
| | 2020-03-23 | −7.30% | −2.56% | 코로나 폭락(시장 바닥 날) | +37.7% / +29.9% / +48.2% | +25.2% / +39.9% / +77.5% |
| | **2025-04-01** | **−7.59%** | +0.28% | 파산법원 로페스 판사가 자회사 레드리버탈크의 파산(활석 소송 일괄 해결안)을 기각(3-31) | +0.8% / +2.4% / +63.0% | −0.4% / +10.9% / +18.3% |
| | **2026-10-13** | **−5.73%** | −0.01% | 3분기 실적: 의료기기 두 분기 연속 미달 | — | — |

- 확인: 시세·계산(수익률), 까닭은 검색 요약(2018-12-14: 알자지라·바이오센추리 기사 제목과 요약, 2019-10-18: 알자지라 등, 2025-04-01: 블룸버그 로 기사 요약. 2018-02-05·2020-03은 SPY 움직임으로 판단).
- 주가 수익률(배당 제외)은 `drops.py` 출력에 같이 있다(예: 2025-04-01 1년 +58.6%).

| F | 사실 | 확인 |
|---|---|---|
| F45 | 시장과 무관하게 J&J만 5% 넘게 빠진 날은 세 번(2018-12, 2019-10, 2025-04)이고 **셋 다 활석 소송**이었다. 이번이 **실적 때문에 5% 넘게 빠진 첫날**이다(2010년 이후) | 계산, 검색 요약 |
| F46 | 그 세 번의 뒤: 3개월 총수익 J&J +4.8 / +17.7 / +2.4%(평균 +8.3%) 대 SPY +9.5 / +11.7 / +10.9%(평균 +10.7%). 1년 J&J +9.6 / +16.1 / +63.0% 대 SPY +25.1 / +17.0 / +18.3%. 3번 가운데 3개월은 1번, 1년은 1번만 시장을 이겼다. 표본이 셋이라 법칙으로 쓰지 않는다 | 계산 |
| F47 | **실적일 하락 순위**(8-K 2.02 제출일 71번, 2010-01-26 ~ 2026-10-13. 실적 발표 외 몇 건이 섞였을 수 있음): ① 2026-10-13 −5.73% ② 2018-01-23 −4.26% ③ 2017-04-18 −3.10% ④ 2023-04-18 −2.81% ⑤ 2026-07-15 −2.69%. 실적일에 빠진 비율 51%, 평균 +0.30%, 가운데값 −0.03%. 짐 크레이머의 "J&J는 실적일에 약하다"는 숫자로는 뚜렷하지 않다 | 계산(`data/scripts/earn.py`, 날짜는 EDGAR 제출 기록) |
| F48 | 이번 하락 전 3.5% 넘게 빠진 마지막 날은 2026-07-30(−3.66%): 파이어플라이·세일 거래로 2026 전망을 내린 다음 날. CNBC 인베스팅클럽도 같은 날짜를 적었다 | 시세, 원문 읽음 |

## 9. 2027년 특허 만료와 일회성 비용

| F | 사실 | 확인 |
|---|---|---|
| F49 | 월크 CFO, 도이체방크 헬스케어 서밋(2026-09-17): "There's about $4 billion to $4.5 billion of products that are losing exclusivity." / "You think about XARELTO, loss of exclusivity, I don't think it's really appreciated. About $2 billion." / "The Pulmonary Arterial Hypertension franchise, about $1.5 billion." / "SIMPONI and STELARA combined, another $1 billion." / "That's more than what we experienced STELARA's loss of exclusivity impact in year one" | 2차 자료(인베스팅닷컴 녹취 https://www.investing.com/news/transcripts/johnson--johnson-at-deutsche-bank-healthcare-summit-growth-outlook-lifts-93CH-4906149 를 웹 도구로 읽음. 사이트가 curl은 막았다. J&J 공식 녹취 아님) |
| F50 | 40억~45억 달러는 2026 매출 전망(1,012억 달러)의 4.0~4.4% | 계산 |
| F51 | 같은 자리에서 2027 매출: "you're going to have equivalent reported growth, but actually operational growth a little bit better". 콜에서 웰스파고 비겔슨은 이를 "53주 효과 1%p를 맞추면 2027 보고 성장 약 5.4%"로 정리했고 월크는 부정하지 않았다 | 2차 자료(인베스팅닷컴), 원문 읽음(콜 녹취) |
| F52 | 파이어플라이 바이오(10억 달러, 7-29 인수 완료): 2026년 조정 EPS −0.46달러, 2027년 −0.08달러 | 원문 읽음(8-K 2026-07-29 첨부 99.1) |
| F53 | 세일 바이오메디슨(체내 CAR-T 제휴): 초기 7.85억 달러, 옵션 행사 시 25.8억 달러 추가. "Assuming exercise of the option" 2026년 −0.18달러, **2027년 −1.28달러** | 원문 읽음(같은 8-K 첨부 99.2) |
| F54 | 콜에서 월크: "For this year, the IPR&D dilution is $0.64. And for next year, the combination of those deals is $1.36." 이익 성장은 매출 성장보다 "a little bit better", "after adjusting for the $1.36 adjustment". 2027 전망은 12-08에 더 분명히 주고 정형외과 분리를 반영한 수치도 줄 것 | 원문 읽음(녹취) |

## 10. 정형외과(디퓨이 신테스) 분리

| F | 사실 | 확인 |
|---|---|---|
| F55 | 발표 2025-10-14: 정형외과를 별도 회사 "DePuy Synthes"로 분리, "targeting completion within 18 to 24 months". 2024년 매출 약 92억 달러. 방식은 "explore multiple paths". 대표 나말 나와나 | 원문 읽음(J&J 보도자료, 웹 도구) |
| F56 | 2025년 정형외과 매출 92.58억 달러(+1.1%). 2026년 1~9월 71.46억 달러(+4.8%) | 원문 읽음(10-K, 3분기 8-K 첨부 99.2) |
| F57 | 2026-09-14 블룸버그 보도(2차 글로 읽음): 아폴로가 디퓨이 신테스 인수를 협상 중, 가치 약 200억 달러, "몇 주 안에" 합의할 수 있으나 깨질 수도 있다. 다른 길로 다른 매수자 또는 분사. J&J와 아폴로는 논평 거부 | 2차 자료(pipelineroad 2026-09-14가 Private Equity Wire를 거쳐 옮김). 블룸버그 원문 미열람. WSJ는 "엉덩이·무릎 사업"이라 했다는 것은 검색 요약 |
| F58 | 10-13 콜에서 월크: "we remain on track for the planned separation of the DePuy Synthes by mid-2027 … we are leaning towards a spin as being the …" / "That has always been our base plan" | 원문 읽음(녹취. 문장 일부가 녹취에서 끊김) |
| F59 | 월크, 야후: "As we moved forward and through the process, we do appreciate that medtech valuations are down," … "And so if you think about potential acquirers, they're going to utilize those valuations to their advantage. That's not optimal for the long-term J&J shareholder." | 원문 읽음 |
| F60 | 가벨리 펀드 다니엘 바라사: 의료기기 값이 낮아 "probably made it harder to complete a sale of the orthopedic business, which may also be weighing on the stock." | 원문 읽음(CNBC) |
| F61 | 3분기 비용: "Orthopaedics separation related" 3.69억 달러(1~9월 7.46억) | 원문 읽음(첨부 99.2) |

## 11. 애널리스트 반응

| F | 사실 | 확인 |
|---|---|---|
| F62 | **10-14 05:20 ET까지 실적 뒤의 목표가·의견 변경은 찾지 못했다.** 벤징가 가격목표 페이지의 최근 기록은 10-07(구겐하임 매수 287달러 유지)이고, 마켓비트도 10-08이 마지막이다 | 원문 읽음(벤징가 페이지 데이터, 마켓비트) |
| F63 | 실적 전 기록: 스티펠 보유·260달러 유지(10-12), RBC 아웃퍼폼 287 → 290(10-06), 씨티 매수 298 → 303(10-05), JP모건 중립 270 → 285(9-29), BofA 중립 278 유지(9-29), HSBC 매수 290 → 320(9-10), UBS 매수 280 → 320(9-02) | 원문 읽음(벤징가·마켓비트 표), 스티펠은 검색 요약 |
| F64 | 평균 목표가 276.22달러(25명, 최고 320, 최저 210, 마켓비트). 다른 집계는 279.82(야후, S&P 글로벌 23명), 285.82(팁랭크스). 10-13 종가보다 11~15% 위 | 원문 읽음(마켓비트), 검색 요약(나머지) |
| F65 | CNBC 인베스팅클럽(짐 크레이머 운용 포트폴리오, 10-13): 매수 의견과 목표가 275달러 유지. 제목 "J&J's 6% slide on an imperfect quarter is a gift to prospective buyers". 크레이머: "You buy 100 shares here. If it goes down another 5%, you buy another 100 shares." 중동은 "deferred sales, not lost revenue"라는 경영진 말을 근거로 듦 https://www.cnbc.com/investingclub/2026/10/13/jj-falls-6percent-on-an-imperfect-quarter-why-this-is-a-good-chance-to-buy.html | 원문 읽음 |
| F66 | Zacks 집계에서 지난 4주 동안 J&J 2026 EPS를 내린 사람 2명·올린 사람 0명, 2027은 올림 2·내림 3 | 원문 읽음(집계값, 실적 전 기록이 섞였을 수 있음) |

## 12. 일정

| F | 사실 | 확인 |
|---|---|---|
| F67 | **2026-12-08 Enterprise Business Review(사업설명회)는 그대로다.** 10-13 콜에서 월크: "I am really looking forward to and hope you join us for the enterprise business review on December 8th. At that event, we will provide additional perspective on our 2027 outlook"; 슈미드·두아토도 12월 8일을 말했다. 처음 알린 것은 1분기 실적(2026-04-14) | 원문 읽음(녹취, 8-K 2026-04-14) |
| F68 | **4분기 실적: 2027-01-26(화).** 3분기 콜 안내문(2026-08-31): "Please note the fourth-quarter date of Tuesday, January 26th, 2027." | 원문 읽음(J&J 보도자료 PDF https://s203.q4cdn.com/636242992/files/doc_news/Johnson--Johnson-to-Host-Investor-Conference-Call-on-Third-Quarter-Results-2026.pdf ) |
| F69 | 다음 배당: 1.34달러, 배당락 2026-11-24, 지급 2026-12-08(10-13 선언) | 2차 자료(벤징가 페이지의 배당 데이터. J&J 원문은 열지 않음) |

## 13. 배당

| F | 사실 | 확인 |
|---|---|---|
| F70 | 2026-04-14: 분기 배당 1.30 → **1.34달러(+3.1%)**, "marking the **64th year** of consecutive increases". 연 5.36달러 | 원문 읽음(8-K 첨부 99.3 https://www.sec.gov/Archives/edgar/data/200406/000020040626000076/a2026q1exhibit993.htm) |
| F71 | 앞 조사의 "62년"(TIKR 글 제목)은 틀렸다. 64년이 맞다 | 원문 읽음 |
| F72 | 10-13 종가 기준 2.16%(지시), 지난 12개월 실제 지급 합 5.28달러 → 2.12%. S&P500 1.04%의 약 두 배 | 시세, 계산 |
| F73 | 월크(9-17): "The dividend, we have got dividend king status." / "I do not think Joaquin nor I want to be the one to break that streak, to be quite frank." | 2차 자료(인베스팅닷컴 녹취) |

## 14. 주가의 자리

| F | 사실 | 확인 |
|---|---|---|
| F74 | 10-14 개장 전(05:20 ET = 18:20 KST) 250.15달러(+0.62%) | 원문 읽음(나스닥 info API, 그 시각 값) |
| F75 | 올해(2025-12-31 종가 206.95 기준): 10-12까지 **+27.4%**(SPY +14.1%) → 10-13 **+20.1%**(SPY +14.1%). 배당 포함 J&J +22.1%, SPY +15.0% | 시세, 계산 |
| F76 | 1년(2025-10-13 190.90 기준): J&J +30.2%(배당 포함 +33.2%), SPY +17.3%(+18.6%) | 시세, 계산 |
| F77 | 종가 최고 278.43(2026-09-03), 장중 최고 281.07. 10-13 종가는 최고 대비 −10.7%. 52주 최저 184.66달러(장중) | 시세, 계산, 2차 자료(52주 최저는 벤징가 데이터) |
| F78 | 거래량 10-13 1,665만 주(나스닥), 9~10월 평소 400만~1,100만 주 | 시세 |
| F79 | 실적 전 2주의 흐름: 9-28 271.95 → 10-05 252.93(−7.0%) → 10-12 263.73. 10-13 종가는 10-05보다 낮다 | 시세, 계산 |

## 15. 값 때문인가 — 판정 재료

| F | 사실 | 확인 |
|---|---|---|
| F80 | 올해 J&J PER의 움직임: 연초 206.95 ÷ 1월 전망 11.53 = **17.9배** → 10-12 263.73 ÷ 10월 전망 11.10 = **23.8배**(일회성 연구개발비를 뺀 11.74로는 22.5배) → 9-03 고점 278.43 ÷ 11.10 = 25.1배 → 10-13 **22.4배**. 주가 +27%는 이익 전망이 아니라 배수가 오른 것이다(보고 기준 전망은 오히려 −3.7%, 일회성 제외로는 +1.8%) | 계산 |
| F81 | 자기 10년 평균(F43) 약 16~17배, S&P500 19.1배(F38), 비교 일곱 회사 2027 가운데값 16.9배(F41)보다 높다. 하락 뒤에도 그렇다 | 계산 |
| F82 | 의료기기 예상 미달(6,800만~9,800만 달러)과 시가총액 감소(약 364억 달러)의 크기 차이: 약 370~540배 | 계산 |
| F83 | FactSet(10-09): 3분기에 헬스케어 업종은 이익 예상이 줄었는데 주가는 올랐다(F40). 업종 전체에 "이익 없이 오른 값"이 있었다 | 원문 읽음 |
| F84 | 반대 증거: 같은 날 의료기기 동종(보스턴사이언티픽 −3%, 인튜이티브 −2%)도 빠졌다. 값만이 아니라 "의료기기 업종에 대한 걱정"도 섞였다 | 원문 읽음(CNBC) |

---

## 엇갈리는 보도

| 무엇 | 한쪽 | 다른 쪽 | 맞아 보이는 쪽과 까닭 |
|---|---|---|---|
| 하락 폭 | 종가 −5.73%(248.61, 나스닥·야후 같은 값) | CNBC "more than 6%"(장중 기사), 벤징가 "약 6%", 마켓비트 −5.62%(248.90, 15:59 값) | −5.73%. 공식 종가다. 영상에서 "6% 가까이"는 맞고 "6% 넘게"는 틀림 |
| 쿠웨이트·UAE·사우디 말이 나온 곳 | CNBC: 월크가 "in an interview" | 앞 조사(candidates.md)의 대독 후보 표는 출처만 CNBC로 적음 | 실적 콜이 아니라 **CNBC 인터뷰**다. 콜 녹취(모틀리풀)에는 나라 이름이 없다. 대본에서 "실적 발표회에서"라고 쓰면 틀림 |
| 의료기기 예상치 | LSEG 87.1억 달러 | StreetAccount 87.4억 달러 | 둘 다 맞다(집계사가 다름). "예상보다 1억 달러 가까이 적었다"로 쓰면 둘 다 덮음 |
| 매출 | LSEG 예상 252.8억 → 넘음(CNBC) | 벤징가 데이터: 매출 "surprise −1.69%"(못 미침) | LSEG 쪽. CNBC가 직접 숫자를 댔고, 벤징가 값은 거래 반영 전 낡은 예상치일 가능성. 다만 확인 안 됨 |
| 주당이익 넘은 폭 | LSEG +5센트(2.54) | Zacks +6센트(2.53), FactSet +9센트(2.50) | 다 맞다(집계사 차이). "예상을 넘었다"까지만 쓴다 |
| 하락의 무게 | CNBC: 중동·유럽·중국 | 야후: 영국 심장 펌프 연구 + 지정학 / 콜의 슈미드: ① 미국 밖 ② 아비오메드, 중동은 "새 역풍" / 가벨리: 정형외과 매각 어려움 / JP모건 마커스: J&J만의 사정 | 원문(콜)의 순서가 가장 믿을 만하다: 미국 밖 전체(중국 집중구매, 수술 구조조정, 아시아 경쟁, **그리고 새로 중동**)와 아비오메드. 중동은 **여러 까닭 가운데 새로 더해진 하나**. 2분기 10-Q는 분쟁 영향이 "not material"이었다고 적었다 |
| 아비오메드 감소 | 8-K −2.3%(보고 기준) | 모틀리풀 요약 −1.5% | 둘 다 맞다. −1.5%는 환율 뺀 영업 기준 |
| 콜 녹취의 "SHOCK-III study" | 녹취: "1.25 thousand patients, 4x more than the SHOCK-III study" | 실제 영국 연구 이름은 CHIP-BCIS3(300명) | 녹취 오기로 본다. 1,250 ÷ 300 ≈ 4배가 맞아떨어진다 |
| 두아토의 "29개 제품" | 모틀리풀 요약: "at least $2 billion in annual sales" | 같은 녹취 본문: "at least $1 billion in annual sales" | 본문 쪽(10억 달러). 요약이 틀렸다. 쓰려면 회사 원문으로 다시 확인 |
| 정형외과 매출 | J&J 2025-10 보도자료: 2024년 약 92억 | 블룸버그(2차): 2025년 93억 | 둘 다 맞다(연도가 다름). 10-K의 2025년 값은 92.58억 |
| 아폴로 협상 범위 | 블룸버그: 정형외과 사업 | WSJ: 엉덩이·무릎 사업(검색 요약) | 판단 못 함. 둘 다 원문 미열람 |
| 2027 특허 만료 | 인베스팅닷컴 녹취: 40억~45억 달러 | 다른 요약 한 곳: "20억~45억" | 40억~45억. 품목 합(20+15+10)이 45억이다 |
| 연속 배당 증액 | J&J 원문: 64년 | TIKR 글 제목: 62년 | 64년 |
| 올해 상승률 | 야후: "up more than 27% this year"(하락 전) | 앞 조사: 1-02 종가 기준 +27.2% | 둘 다 맞다(기준일 차이). 12-31 종가 기준 +27.4%, 하락 뒤 +20.1% |
| PER | 이 문서 22.4배(2026 역년) | 벤징가 forwardPE 19.6배 | 기준이 다르다. 한 자로만 쓴다(이 문서 6절) |

---

## 판단 재료

**지금 주가를 움직이는 하나의 변수: 12월 8일 사업설명회에서 회사가 내놓을 2027년 주당이익 전망.**

- 까닭: 올해 주가 +27%는 이익이 아니라 배수(17.9배 → 23.8배)가 올린 것이다(F80). 이번 하락은 "의료기기가 이 배수를 받을 만한가"를 다시 잰 것이다. 미달 금액은 매출의 0.3~0.4%인데 시가총액은 364억 달러가 빠졌다(F82). 그러므로 다음 움직임도 3분기 숫자가 아니라 "2027년 이익이 22배를 정당화하나"에서 나온다.
- 방향: 2027 전망이 지금 예상(12.33달러)을 받쳐 주면 주가는 2027 기준 20배(약 247달러) 근처에서 버틴다. 전망이 그보다 낮으면 배수와 이익이 함께 내려간다.

**시장이 반영한 것과 놓쳤을 수 있는 것**
- 반영한 것: 의료기기 두 분기 연속 미달, 미국 밖 의료기기 +0.1%(2분기 +3.2%), 아비오메드 두 분기 감소. 하루 만에 PER이 23.8 → 22.4배.
- 놓쳤을 수 있는 것 ①(나쁜 쪽, 계산이며 해석 주의): 월크의 말대로라면 일회성 비용을 뺀 2027 이익은 11.74 × 1.055~1.07 ≈ 12.4~12.6달러, 여기서 세일·파이어플라이 비용 1.36달러를 빼면 **보고 기준 약 11.0~11.2달러**다. 지금 컨센서스 12.33달러(최저 11.42)는 이 비용, 특히 세일 옵션의 1.28달러를 다 넣지 않은 값으로 보인다(옵션 행사가 확정이 아니어서). 12월 8일 전망이 이 비용을 넣은 숫자로 나오면 "2027 이익 전망 컨센서스 하회"라는 제목이 붙을 수 있다. 다만 일회성이라 시장이 걸러 볼 수도 있다.
- 놓쳤을 수 있는 것 ②(좋은 쪽): 매출의 66%인 의약품은 +7.7%, 미국 의약품 +11.1%, 트렘피어 +68%다. 의료기기 가운데 정형외과(의료기기의 27%, 전체의 9%)는 2027년 중반에 떨어져 나간다. 남는 J&J는 지금보다 의약품 비중이 더 크다. 2027 특허 만료 40억~45억 달러(매출의 4~4.4%)는 회사가 이미 숫자로 말했다.
- 확인할 수 없는 것: 중동이 "미뤄진 매출"이라는 경영진 말(F20). 회사는 중동 크기를 밝히지 않았고 2분기에는 "not material"이었다.

**사는 계획 후보 (아래 가격선은 작업자가 조사 숫자로 만든 선이다. 사용자가 정하지 않았다. Z4)**
- 지금 248.61달러에서는 사지 않는다. 2027 예상의 20.2배로, 비교 일곱 회사 가운데값(16.9배)보다 19%, S&P500(19.1배)보다 6% 비싸고, 2027 이익 숫자 자체가 12월 8일에 바뀔 수 있다.
- 1차(절반): 2026-12-08 사업설명회에서 **일회성 연구개발비를 뺀 2027 조정 주당이익 가운데값이 12.3달러 이상**이면(= 지금 컨센서스 수준), 주가가 **235달러 이하**(12.33 × S&P500 배수 19.1)일 때 산다.
- 2차(나머지 절반): 2027-01-26 4분기 실적에서 **미국 밖 의료기기 영업 성장이 다시 +2% 이상**(2분기 +3.2%, 3분기 +0.1%의 중간)이면, 235달러 이하에서 산다. 또는 조건과 무관하게 **213달러**(12.33 × 자기 10년 평균 연말 PER 17.3)까지 내려오면 산다.
- 틀렸다고 볼 기준: ① 12-08에 일회성을 뺀 2027 이익 가운데값이 12.3달러 아래(이익 성장이 매출 성장보다 느림 = 월크의 9-17·10-13 말과 어긋남), ② 1-26 실적에서 미국 밖 의료기기가 또 0% 이하, ③ 정형외과 분리가 2027년 중반에서 미뤄짐. 하나라도 나오면 사지 않는다.
- 반대 의견(같이 보여 줄 것): CNBC 인베스팅클럽은 지금 사고 5% 더 빠지면 더 사라고 했다(F65). 평균 목표가 276달러(F64)는 지금보다 11% 위. 지난 세 번의 "J&J만의 급락" 뒤 1년 수익은 +9.6%, +16.1%, +63.0%로 모두 플러스였다(F46. 다만 셋 다 소송 사건이었고, 시장을 이긴 것은 한 번).

---

## 못 찾은 것

- J&J 공식 3분기 콜 녹취 PDF(아직 미게시). 모틀리풀 녹취로 대신했다.
- J&J 중동 매출 규모(공시 없음).
- 실적 뒤(10-13~10-14) 증권사 목표가 변경(10-14 05:20 ET 기준 없음).
- FactSet·LSEG의 J&J 2027 컨센서스와, 컨센서스에 세일 옵션 비용이 들어 있는지.
- J&J 앞으로 12개월 PER의 5년·10년 평균(제공처의 원 자료). 대신 7절의 직접 계산.
- 머크 2026 EPS가 눌린 까닭.
- 블룸버그의 아폴로 보도 원문, WSJ 보도 원문.
