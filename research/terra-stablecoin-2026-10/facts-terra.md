# 테라(UST)·루나 폭락과 권도형: 사실 조사

조사한 날: 2026-10-16. 조사한 쪽: 하위 조사 작업자(릴스 47). 범위: 2022년 5월 테라·루나 폭락, 앵커 20% 이자의 출처, 권도형의 말과 재판, 한국 피해와 그 뒤의 법. 지금의 규제 스테이블코인(서클 등)은 `facts-circle.md`가 맡는다.

**전제 확인.** 사용자의 질문 틀 "연 20% 이자를 준다던 한국산 코인이 며칠 만에 99% 폭락"은 사실이다. 앵커 예치 이자는 약 19.5%(검찰·SEC 문서는 "약 20%", "19~20%")였고, 루나는 2022-05-07 시가 77.47달러에서 05-13 종가 0.000102달러로 99.99% 넘게 빠졌다(T1, T8). "한국산"은 창업자 둘(권도형, 신현성)이 한국인이고 초기 사업이 한국 결제 앱 차이와 얽혀 있었다는 뜻에서 맞다. 다만 법인 테라폼랩스는 싱가포르 법인이다(기소장 6항). 영상에서 "한국산"이라 하면 "한국인이 만든"이 더 정확하다.

**확인 범위 표기.** 원문 = 원문을 직접 읽음 / 요약 = 요약 도구(WebFetch)를 거쳐 읽음 / 검색 = 검색 요약만 봄 / 기억 = 작업자의 기억. 원문 텍스트는 `sources/`에 옮겨 두었다.

| 약칭 | 문서 | URL | 본 방식 |
|---|---|---|---|
| 기소장 | 미국 뉴욕남부지검 권도형 추가 기소장(S1 23 Cr. 151, 2025-01-02 공개) | https://www.justice.gov/d9/2025-01/do_kwon_superseding_indictment.pdf | PDF 원문, `sources/doj_kwon_superseding_indictment_2025-01.txt`(OCR이라 철자가 깨진 곳이 있다) |
| DOJ 유죄 인정 | 보도자료 "Do Kwon Pleads Guilty To Fraud"(2025-08-12) | https://www.justice.gov/usao-sdny/pr/do-kwon-pleads-guilty-fraud | 웹 아카이브 사본 20260524, `sources/doj_pr_do-kwon-pleads-guilty-fraud.txt` |
| DOJ 선고 | 보도자료 "Crypto-Enabled Fraudster Sentenced For Orchestrating $40 Billion Fraud"(2025-12-11) | https://www.justice.gov/usao-sdny/pr/crypto-enabled-fraudster-sentenced-orchestrating-40-billion-fraud | 웹 아카이브 사본 20261008 |
| DOJ 인도 | 보도자료 "Do Kwon Extradited…"(2025-01-02) | https://www.justice.gov/usao-sdny/pr/do-kwon-extradited-united-states-montenegro-face-charges-relating-fraud-resulting-40 | 웹 아카이브 사본 20260524 |
| SEC 소장 | SEC v. Terraform Labs 수정 소장(23-cv-01346, 2023-04-03 제출) | https://www.sec.gov/files/terraform-labs-pte-ltd-amended-complaint.pdf | 웹 아카이브 사본 20251228(sec.gov 직접은 403) |
| SEC 합의 | SEC 보도자료 2024-73(2024-06-13) | https://www.sec.gov/newsroom/press-releases/2024-73 | 웹 아카이브 사본 20251220 |
| SEC 타이모샨 | SEC 행정명령 Release No. 11349(2024-12-20) | https://www.sec.gov/files/litigation/admin/2024/33-11349.pdf | 웹 아카이브 사본 |
| 지니어스법 | S.1582 GENIUS Act 확정본, 공법 119-27(2025-07-18) | https://www.congress.gov/119/bills/s1582/BILLS-119s1582enr.htm | 원문, `sources/genius_act_*.txt` |
| 가격 | Yahoo Finance 일봉 LUNC-USD, USTC-USD(UTC 날짜) | https://query1.finance.yahoo.com/v8/finance/chart/LUNC-USD | `data/luna_classic_…csv`, `data/ust_classic_…csv` |

---

## 1. 앵커: 20% 이자는 어디서 나왔나

**T1. 앵커는 UST를 맡기면 연 약 20%를 준다고 한 예금 상품이었다.**
- 사실: 앵커 프로토콜은 2021년 3월 무렵 출시됐고 "UST를 맡기면 연 약 20% 수익"을 내세웠다(기소장 12(c)항: "offered an approximately 20% annual return for UST deposited in Anchor"). SEC 소장 35항은 "19-20%"라 적는다. 한국 보도는 "19.5% 이자율"(디지털데일리 2022-04-28). 앵커 첫 화면 문구는 "Better Savings"(더 나은 저축).
- 날짜: 출시 2021-03, 이율은 2022-05-01 전까지 약 19.5%
- 출처: 기소장 12(c)항 / SEC 소장 35항 / https://www.ddaily.co.kr/page/view/2022042811203139194 / https://web.archive.org/web/20220419110722/https://www.anchorprotocol.com/
- 확인 범위: 기소장·SEC 소장 원문. 디지털데일리 요약. 앵커 첫 화면은 아카이브 화면을 직접 캡처해 봄
- 화면에 쓸 실물: `references/terra/anchorprotocol-com_wayback_2022-04-19.png`("Better Savings" + 초록 3D 로고, 검은 바탕). 앱 EARN 화면 틀은 `app-anchorprotocol-earn_…png`(데이터가 안 불러져 APY 0%로 찍힘, 재구성 필요)

**T2. 폭락 직전 UST의 약 70%가 앵커에 들어가 있었다.**
- 사실: 검찰은 "약 70%(유통량 약 185억 달러 중 약 129억 달러)"(기소장 38항), SEC는 "약 190억 UST 중 약 140억, 거의 74%"(SEC 소장 36, 75항)라고 적었다. 두 문서 모두 "2022년 5월 초 폭락 직전"이라고만 적었는데 숫자가 다르다. 차이의 까닭(기준 날짜나 집계 방식)은 확인 못 했다. 영상에서는 두 숫자가 겹치는 "약 70%(10개 중 7개)"만 쓴다. 2021년 초 유통 UST는 3억 개 아래였고 앵커 출시 뒤 두 달 만에 10억 개 가까이 늘었다(SEC 소장 36항). DefiLlama 기준 UST 유통량 정점은 2022-05-07의 187.7억 달러(`data/ust_supply_defillama.csv`, 다른 조사자가 받은 파일).
- 날짜: 2022-05 초
- 출처: 기소장 38항, SEC 소장 36·75항
- 확인 범위: 원문(둘 다). DefiLlama 정점은 CSV에서 직접 계산
- 화면에 쓸 실물: UST 유통량 곡선(DefiLlama CSV)과 그중 앵커 몫을 채운 막대. 영상에서는 "10개 중 7개"가 듣기 쉽다

**T3. 이자는 빌린 사람이 낸 이자만으로 모자랐고, 테라 쪽이 메워 줬다.**
- 사실: 앵커 설명서는 예금 이자가 "대출자가 낸 이자 + 대출 담보(bLUNA, bETH 같은 스테이킹 자산)의 스테이킹 보상"에서 나오고, 목표 이율에 못 미치면 "일드 리저브(yield reserve)에 쌓아 둔 스테이블코인"으로 직접 보조한다고 적었다. 검찰은 "앵커는 대출자에게서 버는 것보다 훨씬 많은 이자를 예금자에게 줬고, 약 20%를 줄 수 있었던 것은 권도형이 LFG 준비금과 테라폼의 돈을 앵커로 돌렸기 때문"이라고 적었다(기소장 38항: "Anchor paid out far more in interest to its depositors than it earned from its borrowers, and Anchor was able to pay its approximately 20% interest rate only because DO HYEONG KWON… caused the diversion of funds from the LFG Reserve and Terraform to Anchor"). 권도형 자신도 앵커에 돈을 맡겨 이 보조금의 혜택을 받았다(같은 항).
- 날짜: 2021-07 ~ 2022-05
- 출처: 앵커 문서 https://docs.anchorprotocol.com/protocol/overview , https://docs.anchorprotocol.com/protocol/money-market/deposit-rate-subsidization (웹 아카이브 2022 사본) / 기소장 38항
- 확인 범위: 앵커 문서는 아카이브 사본 본문을 직접 추출해 읽음. 기소장 원문
- 화면에 쓸 실물: 물탱크 비유 3D(대출 이자 수도꼭지는 가늘고, 빠지는 이자 구멍은 크고, 옆에서 테라가 양동이로 붓는 그림). 기소장 38항 문장 캡처

**T4. 보조금을 두 번 부었다: 2021년 7월 약 7천만 달러, 2022년 2월 4억 5천만 달러.**
- 사실: SEC는 "2021년 7월 테라폼이 약 7천만 달러어치 UST를 일드 리저브에 넣었고, 2022년 초 리저브가 빠르게 바닥나자 루나재단가드(LFG)가 약 4억 5천만 달러어치를 다시 채웠다. 권도형이 지시했다"고 적었다(SEC 소장 78항). 넣기 직전 리저브는 656만 달러까지 줄어 있었다(코인텔레그래프 2022-02-18). LFG 투표 통과는 2022-02-10, 권도형은 2022-02-18 트윗 한 단어 "Funded."로 알렸다.
- 날짜: 2021-07, 2022-02-10(의결), 2022-02-18(입금)
- 출처: SEC 소장 78항 / https://cointelegraph.com/news/terra-injects-450m-ust-into-anchor-reserve-days-before-protocol-depletion
- 확인 범위: SEC 원문. 656만 달러, "Funded."는 요약(코인텔레그래프 본문을 WebFetch로 읽음). "Funded." 트윗 원본은 못 봄
- 화면에 쓸 실물: 리저브 잔고 막대가 바닥에 닿았다가 한 번에 솟는 그래프. "Funded." 한 단어 자막

**T5. 4억 5천만 달러는 두 달 반 만에 절반이 사라졌다.**
- 사실: 2022-04-28 기준 앵커 예치금 134억 달러, 준비금 2억 3,926만 달러. 5월 1일부터 이율을 18%로 내릴 수 있고 이후 한 달에 1.5%포인트씩 움직이게 바뀌었다(디지털데일리 2022-04-28). 
- 작업자 계산(사실 아님): 2022-02-18 약 4억 5,656만 달러(656만 + 4억 5천만) → 04-28 2억 3,926만 달러. 69일에 약 2억 1,700만 달러, 하루 약 315만 달러(약 40억 원)가 빠졌다. 예치금 134억 달러에 19.5%면 1년 이자가 약 26억 달러, 하루 약 720만 달러다. 그중 대출 이자와 담보 보상으로 못 채운 몫이 리저브에서 나간 셈이다. 리저브로 들어온 다른 돈이 있었는지는 확인 못 했으므로 "약"으로만 쓴다.
- 날짜: 2022-02-18 ~ 2022-04-28
- 출처: https://www.ddaily.co.kr/page/view/2022042811203139194 / T4 출처
- 확인 범위: 디지털데일리는 요약. 계산은 작업자
- 화면에 쓸 실물: 모래시계나 새는 금고. 하루 40억 원이 빠지는 카운터

**T6. 권도형은 보조금을 숨기지 않았다. "성장 단계라 가장 매력적인 이자를 유지하겠다."**
- 사실: 2022-01-27 권도형 트윗(SEC 소장 79항에 캡처): "13/ But in the meanwhile, I am resolved to find ways of subsidizing the yield reserve. Anchor is still in the growth phase, and maintaining the most attractive yield in DeFi stable will strengthen that growth & build up moats." 이틀 전(01-25) 투표 트윗: "Don't wanna get another DM about the @anchor_protocol yield reserve. What do you want?"
- 날짜: 2022-01-25, 2022-01-27
- 출처: SEC 소장 24쪽 캡처
- 확인 범위: 원문(트윗 화면 캡처를 직접 봄)
- 화면에 쓸 실물: `references/terra/sec-complaint_p24_kwon-tweet-yield-reserve.png`

**T7. 20%가 위험하다는 경고를 여러 번 받고도 유지했다.**
- 사실: 검찰은 "권도형은 보조금으로 받친 약 20% 이율이 지속 불가능하고 UST 수요를 부풀려 시스템 전체를 흔들 것이라는 경고를 거듭 받았지만 유지했다"고 적었다(기소장 39항). 한국 보도(JTBC를 인용한 블루밍비트, 2022-05)는 익명의 설계 관계자가 "이자율을 3.6%로 계산했으나 권도형 대표가 20%로 하라고 지시했다", "20% 못 만들면 다 자른다고 했다"고 말했다고 전했다.
- 날짜: 기소장은 시점 미특정. JTBC 보도는 2022-05
- 출처: 기소장 39항 / https://bloomingbit.io/feed/news/28354 (JTBC 원 보도는 못 봄)
- 확인 범위: 기소장 원문. 3.6%와 "다 자른다"는 검색 요약만 봄(블루밍비트 페이지 접속 실패). 익명 증언이라 영상에서 쓰려면 JTBC 원문 확인 필요
- 화면에 쓸 실물: 3.6 → 20 숫자가 바뀌는 계산기(JTBC 원문 확인 뒤)

---

## 2. 구조와 폭락

**T8. 구조 한 줄: 1달러어치 루나를 태우면 1 UST가 나오고, 1 UST를 태우면 1달러어치 루나가 나온다.**
- 사실: 테라폼 홍보물은 "1 UST는 언제나 1달러어치 루나로 바꿀 수 있고, 1달러어치 루나는 언제나 1 UST로 바꿀 수 있다"고 했다(기소장 11항, DOJ 보도자료). 테라 공식 영상(2020-10-21)은 이것을 "1달러어치 루나를 1 UST로 바꾸는 기계"로 그렸고 "지구의 자전을 안정시키는 달처럼 루나가 테라의 안정에 필수"라고 했다(기소장 19(b)항). 담보는 없었다: 2020-09-16 사업 파트너가 "그럼 준비금은 없는 거죠?"라고 묻자 권도형은 "no reserve."라고 답했다(기소장 19(a)항).
- 날짜: UST 출시 발표 2020-09, 영상 2020-10-21
- 출처: 기소장 11, 19항 / https://www.youtube.com/watch?v=KqpGMoYZMhY
- 확인 범위: 원문. 영상은 받아서 파일 있음(내용은 재생 못 함, 기소장 캡처로 확인)
- 화면에 쓸 실물: `terra_how-does-terra-work_2020-10-21_KqpGMoYZMhY.mp4`의 기계 애니메이션, 기소장 16쪽 캡처

**T9. 그 기계에는 숨은 조임쇠가 있었다.**
- 사실: 한쪽 방향으로 교환 요청이 몰리면 수수료가 점점 커지게 설계됐고, 2021년 5월 당시 약 2천만 달러어치 환매만 감당하면 수수료 때문에 차익이 사라지는 구조였다. 이 설정은 홍보물 대부분에 없었다(기소장 26항).
- 날짜: 2021-05 기준
- 출처: 기소장 26항
- 확인 범위: 원문

**T10. 정점: UST 약 180억 달러, 루나 약 290억 달러, 둘 합쳐 500억 달러 넘음. 루나 최고가 119달러.**
- 사실: 검찰: 2022년 봄 UST와 루나의 시가총액 합은 500억 달러를 넘었다(기소장 3항, DOJ 보도자료). 1년 사이 UST 시가총액은 약 20억 → 약 180억 달러, 루나는 약 50억 → 약 290억 달러(기소장 37항). Yahoo 일봉 기준 루나 최고가는 2022-04-05 장중 119.18달러(종가 최고 04-04 116.41달러). 검찰은 "115달러 넘게"라고 적었다(기소장 33항).
- 날짜: 2022-04 ~ 05 초
- 출처: 기소장 3, 33, 37항 / `data/luna_classic_LUNC-USD_yahoo_daily_2021-04_2022-06.csv`
- 확인 범위: 원문, CSV 직접
- 화면에 쓸 실물: 루나 가격 곡선(2021-04 ~ 2022-04 상승), 기소장 19쪽 시가총액 그래프

**T11. 폭락 일지(Yahoo 일봉, UTC).**
| 날짜 | UST 종가(장중 저가) | 루나 종가(장중 저가) | 있었던 일 |
|---|---|---|---|
| 05-06 | 0.9996 | 77.46 | |
| 05-07(토) | 0.9969 (0.9927) | 68.25 | 커브·앵커에서 대량 UST 매도 시작(코인데스크 일지, SEC 소장 170항 "one or more sophisticated trading firms… beginning on or about May 7") |
| 05-08 | 0.9964 (0.9905) | 64.08 | LFG가 비트코인 7.5억 달러어치를 마켓메이커에 빌려 방어 시작 |
| 05-09 | 0.7934 | 32.00 | 권도형 "Deploying more capital – steady lads". 같은 날 "LFG 위원회가 15억 달러(BTC 7.5억, UST 7.5억) 투입을 만장일치로 결정" 트윗(기소장 41(f)항). 앵커 예치금 140억 → 90억 달러 아래(코인데스크) |
| 05-10 | 0.7999 (0.6841) | 17.52 | 테라폼이 BTC 33,206개를 UST 11.6억 개와 바꿈(LFG 5-16 발표, 검색 요약) |
| 05-11 | 0.8011 (0.2998) | 1.075 (0.838) | 빗썸·업비트 루나 투자유의종목 지정 |
| 05-12 | 0.4086 | 0.004173 | 테라 체인 정지(블록 7603700), 루나 하루 96% 하락(코인데스크) |
| 05-13 | 0.1540 (0.1331) | 0.000102 (0.000017) | 바이낸스·OKX 거래 중단. 업비트·빗썸·고팍스 거래지원 종료 공지. 권도형 "I am heartbroken" |
- 사실 덧붙임: 코인데스크는 UST가 05-09에 0.35달러까지 내렸다고 적었다. Yahoo 일봉 05-09 저가는 0.793달러라 맞지 않는다(거래소·시간대 차이로 보임. 일봉 저가 0.30달러는 05-11). 영상에서 날짜별 UST 값을 말하려면 Yahoo CSV 한 곳을 기준으로 쓴다.
- 루나 공급은 사흘 만에 약 3.4억~3.5억 개에서 6.5조 개 넘게 불어났다(더블록, 검색 요약).
- 작업자 계산: 05-07 시가 77.47달러에 1천만 원어치 루나를 샀다면 05-13 종가 기준 약 13원이 남는다(0.000102 ÷ 77.47 ≈ 0.0000013). 최고가 119달러에 샀다면 약 9원.
- 출처: `data/…csv` / https://www.coindesk.com/learn/the-fall-of-terra-a-timeline-of-the-meteoric-rise-and-crash-of-ust-and-luna / 기소장 41(f)항 / https://www.theblock.co/post/146762/luna-supply-soared-to-6-5-trillion-coins-before-terras-latest-halt
- 확인 범위: 가격은 CSV 직접. 사건은 코인데스크 요약, 트윗 둘은 기소장 원문(15억 달러)과 검색·요약("steady lads"), 공급량은 검색
- 화면에 쓸 실물: 일봉 차트(로그 축으로 그리면 0.0001까지 계단이 보인다), "1천만 원 → 13원" 카운터

**T12. 사라진 돈의 크기는 매체마다 다르다. 영상에서는 "400억 달러(약 55조 원)"를 쓰고 출처는 미국 검찰.**
| 숫자 | 무엇의 숫자 | 출처 |
|---|---|---|
| 400억 달러 넘는 투자자 손실 | 투자자 손실 | DOJ 보도자료 셋, 기소장 4항 |
| 400억 달러 시장가치 증발 | UST·루나·wLUNA·MIR 시가총액 합의 증발 | SEC 소장 171항, SEC 합의 보도자료 |
| 500억 달러 넘음 | 정점 시가총액 합 | 기소장 3항 |
| 약 450억 달러 | 일주일 시가 증발 | 코리아중앙데일리 2022-05-20(검색 요약) |
| 약 600억 달러 | 테라 "생태계" 규모 | 코인데스크 일지 |
- 확인 범위: DOJ·SEC 원문. 나머지 요약·검색
- 작업자 계산: 400억 달러는 2022-05 환율(달러당 약 1,270원, 기억)로 약 51조 원, 지금 환율로는 다르다. 원화로 말하려면 기준 환율을 brief에 적는다

**T13. 루나재단가드(LFG)의 비트코인 8만 개는 9일 만에 313개가 됐다.**
- 사실: LFG는 2022-02-22 루나 판매로 10억 달러를 모아 비트코인 준비금을 만들겠다고 했고, 3~4월에 사 모았다(코인데스크 일지: 03-28까지 6일 동안 27,000개 넘게, 04-11 39,897.98개). 05-07 보유 80,394 BTC(약 24억 달러, 포춘 2022-05-16), 05-16 남은 것 313 BTC. LFG 발표: 05-08부터 준비금을 UST로 바꿨고, 한 거래 상대에게 BTC 5만 개 넘게 주고 UST 15억 개 넘게 받았다. 나중 감사(JS Held)는 BTC 80,081개와 스테이블코인 4,980만 달러, 합쳐 약 28억 달러를 썼다고 했다. 검찰은 "약 8만 BTC를 포함한 LFG 준비금 약 28억 달러를 썼다고 권도형이 주장했다"고 적고, LFG가 독립 기구라는 것은 거짓이고 권도형이 LFG 자산 수억 달러를 빼돌렸다고 했다(기소장 2(b), 41(e)항).
- 날짜: 2022-02-22 ~ 05-16
- 출처: https://fortune.com/2022/05/16/luna-foundation-guard-dumps-bitcoin-reserves-terra-usd-peg / https://www.theblock.co/post/187488/luna-foundation-guard-says-it-spent-2-8-billion-to-defend-ust-peg / 코인데스크 일지 / 기소장 41(e)항
- 확인 범위: 80,394와 313은 포춘 요약. 거래 상대 수량과 JS Held 감사는 검색 요약. 28억 달러와 8만 개는 기소장 원문. LFG 트윗 원본은 못 봄
- 화면에 쓸 실물: 비트코인 8만 개가 쌓인 3D 금고에서 하루하루 빠져 313개가 남는 그림. `data/btc_BTC-USD_…csv`(그 주 비트코인 값도 같이 빠졌다)

---

## 3. 1년 전의 숨은 구조: 2021년 5월

**T14. 2021년 5월에 이미 한 번 무너질 뻔했다. 살린 것은 알고리즘이 아니라 한 트레이딩 회사였다.**
- 사실: 2021-05-23 UST는 92센트 아래로 내려갔고 루나는 며칠 사이 정점 대비 약 75% 빠졌다. 루나 시가총액이 UST 시가총액 아래로 내려가 "UST 전부를 1달러어치 루나로 바꿔 줄 수 없는" 상태가 됐다(기소장 25항). 권도형은 한 고빈도 트레이딩 회사와 구두로 몰래 약속했다: 그 회사가 UST를 사서 가격을 받치고, 대신 권도형은 그 회사가 받을 루나를 앞당겨 주기로 했다(기소장 27항). 그 회사는 최대 1억 달러까지 쓸 수 있게 승인했고, 05-23 아침 30분 동안 쿠코인 UST 매수의 90% 넘게를 그 회사가 했으며, 시장가보다 비싸게 사는 주문도 냈다(기소장 28~30항). SEC는 05-23 ~ 05-27 순매수 6,200만 UST 넘게라고 적었다(SEC 소장 158항). SEC 타이모샨 명령은 "2천만 달러어치 넘게"(명령 11항).
- Yahoo 일봉: UST 05-23 장중 0.9186달러, 루나 05-15 16.40 → 05-23 장중 3.94달러.
- 그 회사는 점프 트레이딩의 자회사 타이모샨(Tai Mo Shan)이다. 검찰과 SEC 소장은 이름을 쓰지 않았으나, SEC는 2024-12-20 타이모샨에 이 일로 1억 2,310만 달러(부당이득 7,345만 + 이자 1,292만 + 과징금 3,673만 달러)를 물렸다(시인·부인 없이 합의).
- 날짜: 2021-05-19 ~ 05-27
- 출처: 기소장 25~31항 / SEC 소장 157~158항 / SEC 타이모샨 명령 / https://www.theblock.co/post/332096/sec-fines-jump-trading-subsidiary-123-million-for-propping-up-terrausd-stablecoin-during-depeg
- 확인 범위: 기소장·SEC 소장·SEC 명령 원문. 1억 2,310만 달러 구성은 검색 요약(명령 원문의 금액 칸까지는 안 읽음, 7,345만 달러 이익은 원문 13항)
- 화면에 쓸 실물: `doj-indictment_p23-23.png`(30분 동안 90%), `sec-complaint_p46_…png`, 2021-05 UST 일봉

**T15. 대가는 40센트짜리 루나였다. 이익은 10억 달러가 넘었다.**
- 사실: 대출 계약(2020-09-08)상 그 회사는 조건을 채우면 루나 최대 6,500만 개를 개당 0.40달러에 받을 수 있었다. 2021년 5월 뒤 권도형은 조건을 없애고 날짜만 정해 넘겨주기로 바꿨고(2021-07-21 문서화), 그 회사는 "루나가 2차 시장에서 90달러 넘게 거래될 때에도" 0.40달러에 받았다. 2021년 10월 6,500만 개 값으로 약 2,600만 달러를 보냈다(SEC 소장 155, 159, 160항). 이익은 "약 10억 달러"(SEC 소장 161항), "10억 달러 넘게, 그 90% 넘게가 2021-05 ~ 2022-05 사이"(기소장 33항). 포춘(2023-05-15)은 SEC 서류를 인용해 12.8억 달러라 적었다.
- 작업자 계산: 0.40달러에 받아 정점 119달러면 약 300배.
- 날짜: 2020-09-08, 2021-05, 2021-07-21, 2021-10
- 출처: SEC 소장 155~161항 / 기소장 33항 / https://fortune.com/crypto/2023/05/15/jump-trading-billion-propping-up-terra-algorithmic-stablecoin-collapsed
- 확인 범위: SEC·기소장 원문. 12.8억 달러는 검색 요약
- 화면에 쓸 실물: 40센트 동전 하나 옆에 119달러 루나

**T16. 겉으로는 "알고리즘이 스스로 회복했다"고 말했다.**
- 사실: 2021-05-24 테라 공식 트윗 "UST peg is normalizing… We just experienced a black swan."(기소장 34(a)항). 2021-05-29 팟캐스트에서 권도형: "And I think what we've proved is that the Terra Protocol… can survive black swan events"(34(b)항). 2021-10-04 인터뷰에서 "시장조성을 하느냐"는 질문에 "we don't really do much of that anymore… I don't think any of them have a contractual relationship with us. It's just something that they do because they feel like they can make money out of it"(34(d)항). 2022-03-01 그 트레이딩 회사가 진행한 방송에서 "the protocol automatically self-heals"(34(f)항). 속으로는: 직원에게 그 회사가 안 받쳤으면 "fucked"였을 거라 했고, 2021년 테라폼 내부 직원 안내서는 그 회사가 "saved our ass in May this year"라고 적었다(32항).
- 확인 범위: 원문
- 화면에 쓸 실물: 겉(트윗·인터뷰 자막)과 속(내부 문서 문장)을 위아래로 맞붙인 화면

**T17. 1년 뒤 같은 수법은 통하지 않았다. 시장이 9배로 커져 있었다.**
- 사실: 2022년 5월 UST 시장은 1년 전보다 시가총액 약 9배, 하루 거래량 8배 넘게 커져 있었다. 그 회사 트레이더는 폭락 중에 2021년을 "simpler times"라 부르며 "about $100 M[illion] committed was enough to re-peg"였지만 "[u]nfortunately it wasn't so simple this time"이라고 했다(기소장 4, 37, 40항).
- 확인 범위: 원문
- 화면에 쓸 실물: 같은 소방 호스가 작은 불(2021)은 끄고 9배 큰 불(2022)에는 닿지 않는 그림

---

## 4. 그 뒤: 도주, 체포, 유죄, 15년

**T18. 한국 체포영장(2022-09-14) 사흘 뒤 "도망 중 아니다", 한 달 전에는 "꺼지라고 해".**
- 사실: 서울남부지법이 2022-09-14 권도형 등 6명에게 체포영장을 냈고, 검찰은 인터폴 적색수배를 요청했다. 권도형은 2022-09-17 트윗 "I am not 'on the run' or anything similar – for any government agency that has shown interest to communicate, we are in full cooperation and we don't have anything to hide". 그런데 검찰에 따르면 2022년 8월 무렵 녹음된 대화에서 그는 수사기관에 대한 전략이 "tell them to fuck off"이고, 여러 나라에서 "political protection"을 얻고 있으며 인도되지 않을 것이라고 "pretty comfortable"하다고 말했다(기소장 5항, DOJ 선고 보도자료).
- 출처: https://forkast.news/do-kwon-says-not-on-the-run-as-s-korea-calls-for-interpols-red-notice/ / 기소장 5항
- 확인 범위: 트윗과 영장 날짜는 검색 요약. 녹음 대화는 원문
- 화면에 쓸 실물: 트윗 문장과 녹음 문장을 나란히

**T19. 2023-03-23 몬테네그로 공항에서 위조 여권으로 붙잡혔다.**
- 사실: 포드고리차 공항에서 전 재무책임자 한창준과 함께 두바이행 비행기를 타려다 코스타리카 위조 여권으로 체포됐다(짐에서 벨기에 여권도 나옴). 검찰 표현은 "미국과 범죄인 인도 조약이 없는 중동 국가로 가려다"(기소장 5항). 같은 날 미국에서 첫 기소. 2023-06-19 포드고리차 기초법원 위조 문서 사용으로 징역 4개월.
- 출처: 기소장 5항, DOJ 인도 보도자료 / https://www.koreajoongangdaily.com/business/do-kwon-given-4-months-in-prison-by-montenegrin-court/11517212 / 파이낸스피즈 등
- 확인 범위: 체포일·중동행은 원문. 코스타리카·두바이·4개월은 검색 요약
- 화면에 쓸 실물: `press_joongang_2023-06_montenegro.jpg`(삭발, 법원 이송), `press_aljazeera_AP_…jpg`, `press_nbc_…jpg`(2024 포드고리차, 복면 특수경찰 호송)

**T20. 한국과 미국이 서로 데려가려 했고, 몬테네그로는 결정을 여러 번 뒤집은 끝에 미국으로 보냈다. 2024-12-31 미국 도착.**
- 사실: 2024-12-31 몬테네그로에서 미국으로 인도, 2025-01-02 뉴욕 법정 첫 출석(DOJ 인도 보도자료). 그 사이 몬테네그로 법원은 한국 송환 결정을 냈다가 대법원이 무효로 하는 등 번복이 있었다(뉴시스·아주경제 2024-03 보도, 검색 요약).
- 확인 범위: 인도일 원문. 번복 경위는 검색 요약

**T21. 2025-08-12 유죄 인정. 법정에서 한 말: "페그가 왜 회복됐는지 거짓되고 오해를 부르는 말을 했다."**
- 사실: 엥겔마이어(Paul A. Engelmayer) 판사 앞에서 상품사기·증권사기·통신사기 공모 1건과 통신사기 1건에 유죄를 인정했다. 최대 25년, 1,900만 달러 넘게 몰수 합의(DOJ 유죄 인정 보도자료). 법정 진술(보도 인용): "I made false and misleading statements about why it regained its peg by failing to disclose a trading firm's role in restoring that peg", "What I did was wrong." 검찰은 12년 넘게 구형하지 않기로 했다.
- 출처: DOJ 유죄 인정 보도자료 / https://www.nbcnews.com/world/asia/crypto-founder-kwon-sentenced-15-years-prison-40-billion-collapse-rcna248790 / 로이터(검색 요약)
- 확인 범위: 혐의·몰수·판사는 원문. 법정 진술 문장은 NBC 요약과 검색 요약(법정 기록 원문 못 봄)

**T22. 2025-12-11 징역 15년. 검찰 구형 12년보다 무거웠다.**
- 사실: 징역 15년, 1,900만 달러 넘게 몰수(DOJ 선고 보도자료). 검찰 12년, 변호인 5년 이하 요청. 판사: "This was a fraud on an epic, generational scale.", "In the history of federal prosecutions, there are few frauds that have caused as much harm as you have, Mr. Kwon." 권도형: "All of their stories were harrowing and reminded me again of the great losses that I've caused. I want to tell these victims that I am sorry." 플리 합의상 형기 절반을 채운 뒤 해외(한국) 이송을 신청하면 미국 검찰이 반대하지 않는다(NBC, 코리아중앙데일리).
- 출처: DOJ 선고 보도자료 / NBC / https://www.koreajoongangdaily.com/korea/us-court-sentences-disgraced-korean-crypto-mogul-to-15-years-in-prison/12141507
- 확인 범위: 형량·몰수는 원문. 판사와 권도형의 말은 NBC 요약(여러 매체가 같은 문장)
- 화면에 쓸 실물: 법정 스케치(못 구함), 호송 사진

**T23. SEC 민사: 배심원 두 시간도 안 걸려 사기 책임 인정, 합의금 44.7억 달러.**
- 사실: SEC 2023-02-16 제소. 2024-04-05 배심원 만장일치 사기 책임 인정(심리 2시간 미만). 2024-06-13 합의: 테라폼 부당이득 35억 8,688만 달러 + 이자 4억 6,695만 달러 + 과징금 4억 2천만 달러 = 44억 7,383만 달러. 권도형 개인 부당이득 1억 1천만 + 이자 1,432만 + 과징금 8천만 달러. 테라폼은 2024-01-21 델라웨어 파산법원에 챕터 11 신청, 2024-09-20 청산 계획 승인.
- 출처: SEC 합의 보도자료(https://www.sec.gov/newsroom/press-releases/2024-73)
- 확인 범위: 원문(청산 계획 승인일은 검색 요약)

**T24. 한국 재판: 공동창업자 신현성은 2023-04 기소 뒤 3년 가까이 1심 중(2026-02 기준).**
- 사실: 검찰은 2023-04-25 신현성 전 차이코퍼레이션 대표 등 10명을 자본시장법 위반(사기적 부정거래) 등으로 불구속 기소했다. 구속영장은 두 번 기각. 2026-02-11 일요신문 보도: 1심이 3년 가까이 진행 중이고, 신 씨 쪽이 추징보전에 반발해 낸 소송 1심에서 지자 항소했다. 대법원은 2025-01-23 몰수보전 재항고를 기각하며 테라·루나가 자본시장법상 "금융투자상품"이 아니라는 원심 판단을 유지했다(이투데이 2025-02-19). 미국 검찰은 신현성을 기소하지 않았다(디지털애셋 보도, 검색).
- 출처: https://news.nate.com/view/20260211n32197 / https://www.etoday.co.kr/news/view/2446337 / https://www.mt.co.kr/society/2023/04/25/2023042517043522747
- 확인 범위: 이투데이는 요약. 일요신문은 페이지 글자가 깨져 검색 요약 수준. 2026-02 뒤 선고 여부는 못 찾음
- 권도형의 한국 재판: 미국 형기 절반 뒤 이송 가능. 2026년 이송·한국 기소 진행 소식은 못 찾음

---

## 5. 한국의 피해와 그 뒤의 법

**T25. 한국 5대 거래소에서 루나를 가진 사람은 약 28만 명, 700억 개.**
- 사실: 금융위원회가 국회에 낸 자료 기준 2022-05-15 자정 국내 5대 거래소 루나 보유자 약 28만 명, 보유량 약 700억 개(전년 12월 말 약 9만 명). 고승범 금융위원장 2022-05-17 국회 정무위에서 "법적으로 제도화가 돼 있지 않다 보니 구체적으로 파악하는 데 한계가 있다".
- 출처: https://news.mtn.co.kr/news-detail/2022051814520015374 / https://www.blockmedia.co.kr/archives/227727 / 노컷뉴스
- 확인 범위: MTN 요약, 나머지 검색
- 작업자 해석: 700억 개는 폭락 뒤 공급이 불어난 루나(05-15)의 개수라 원래 투자 개수가 아니다. "28만 명"만 쓴다

**T26. 거래소: 5-11 유의종목, 5-13 거래지원 종료 공지(업비트는 5-20 정오 종료).**
- 출처: https://economist.co.kr/2022/05/23/finance/Financial/20220523163435704.html , 뉴시스 2022-05-19(상폐 직전 루나에 몰린 젊은 투자자)
- 확인 범위: 검색 요약. 코인원·코빗은 늦게 결정해 비판받음

**T27. 사람들 반응.**
- 2022-05 서울 성수동 권도형 부부 아파트에 한 남성이 들어가 초인종을 누르고 "남편이 집에 있냐"고 묻고 달아났고, 배우자는 긴급 신변보호 대상이 됐다(블루밍비트). 영어 보도는 그가 루나로 20억~30억 원을 잃었다고 말했다고 전했다(야후, 검색 요약).
- r/terraluna 레딧 운영자가 나라별 자살 예방 상담 번호를 게시판 맨 위에 올렸다(포캐스트, 검색 요약). 투자자 자살 보도는 대부분 일화이고 경찰·공식 기록은 못 찾았다. 영상에서 수를 말하지 않는다.
- SEC 소장 172항: 캘리포니아 약사는 집을 담보로 40만 달러를 빌려 UST를 사서 전부 잃었고, 버몬트 화가는 아들 대학 학비로 모은 2만 달러를 잃었다(원문).
- 선고 때 수백 명이 피해 편지를 냈다. 한 피해자(Ayyildiz Attila, 40만~50만 달러 손실): "My savings, my future, and the results of years of sacrifice disappeared."(NBC 요약)

**T28. 한국: 가상자산이용자보호법 2024-07-19 시행.**
- 사실: 2023-06 국회 통과, 2023-07-18 공포, 2024-07-19 시행. 이용자 예치금 보호, 불공정거래 처벌, 금융위 제재 권한. 금융위는 테라·루나와 FTX 사태로 신뢰가 떨어졌다고 적었다. "루나 사태가 직접 계기"라는 공식 문장은 못 찾았다(2022-05 MTN 기사는 루나 사태 뒤 금융위가 "디지털자산기본법"을 2023년 통과·2024년 시행 목표로 추진한다고 전함).
- 출처: https://m.boannews.com/html/detail.html?idx=131600 / 금융위 보도자료(fsc.go.kr) / MTN 2022-05-18
- 확인 범위: 검색 요약. 공포일 2023-07-18은 기억

**T29. 미국 지니어스법: 발행사가 보유자에게 이자를 주는 것을 금지했다.**
- 사실: GENIUS Act(S.1582, 공법 119-27, 2025-07-18 서명) 4(a)(11)항 "Prohibition on interest.--No permitted payment stablecoin issuer or foreign payment stablecoin issuer shall pay the holder of any payment stablecoin any form of interest or yield (whether in cash, tokens, or other consideration) solely in connection with the holding, use, or retention of such payment stablecoin." 같은 4(a)(1)(A)항은 발행 잔액을 "at least 1 to 1" 준비금(현금, 요구불예금, 만기 93일 이하 국채 등)으로 받치게 했다. 테라 같은 구조("같은 발행자가 만든 다른 디지털 자산의 가치에만 기대어 고정가를 지키는" endogenously collateralized stablecoin)는 금지하지 않고, 재무부가 1년 안에 연구 보고서를 내게 했다(14조).
- 출처: https://www.congress.gov/119/bills/s1582/BILLS-119s1582enr.htm , 공법 https://www.congress.gov/119/plaws/publ27/PLAW-119publ27.htm
- 확인 범위: 원문
- 작업자 해석: 앵커는 발행사(테라폼)가 아니라 별도 프로토콜이 이자를 준 구조였으니, 지니어스법 문구가 그대로 테라를 겨냥했다고 말하면 과장이다. "이제 미국에서 달러 코인 발행사는 이자를 못 준다"까지가 사실이다. 거래소가 주는 "리워드"는 이 조항 밖이라는 논쟁이 2026년에도 이어진다(OCC 규칙안, 검색 요약) — 서클 쪽 조사와 맞춘다
- 화면에 쓸 실물: 법 조문 화면(congress.gov), 4(a)(11)항 문장에 밑줄

**T30. 한국 원화 스테이블코인 법(디지털자산기본법)은 2026-07 기준 미통과. 이자 금지는 "가닥"만.**
- 사실: 시사저널 2026-07-20: 1년 넘게 국회 표류, 9월 정기국회가 분기점, 쟁점은 은행 지분 50%+1주 발행 구조와 거래소 대주주 지분 제한. 이데일리 2026-03-18: 은행 발행 원화 스테이블코인은 이자를 안 주는 방안이 유력하고, 여당 통합 법안도 "스테이블코인 이자 지급은 금지하는 것으로 가닥". 조문은 못 봄. 2026-08 ~ 10 진행은 못 찾음.
- 출처: https://www.sisajournal.com/news/articleView.html?idxno=380303 / https://edaily.co.kr/News/Read?mediaCodeNo=257&newsId=05041366645384632
- 확인 범위: 요약

---

## 사람과 남긴 말(대독 후보)

| 자리 | 말한 사람·날짜 | 원문 | 자연스러운 한국말 | 확인 범위 |
|---|---|---|---|---|
| 시작 전 속마음 | 권도형, 2018-01 이메일(기소장 13항) | "[g]ood returns to be had… depending on your risk appetite / moral constitution ;)" | "수익은 날 수 있죠. 위험을 얼마나 견디느냐, 양심이 얼마나 되느냐에 따라 ;)" | 원문 |
| 같은 이메일 | 권도형, 2018-01 | "[s]tability has not been proven", "catastrophic event (market-wide crash) could de-peg the coin" | "안정성은 증명된 적 없어요. 시장 전체가 무너지면 1달러가 깨질 수 있죠." | 원문 |
| 담보 질문 | 사업 파트너와 권도형, 2020-09-16(기소장 19(a)항) | "so there is no reserve right?" / "no reserve." | "그럼 준비금은 없는 거죠?" / "없어요." | 원문 |
| 자만 | 권도형 트윗, 2020-12(포춘·코리아중앙) | "Bow before the king" | "왕 앞에 엎드려라" | 요약 |
| 비판에 대한 답 | 권도형 트윗, 2021-07(경제학자 프랜시스 코폴라에게) | "I don't debate the poor on Twitter, and sorry I don't have any change on me for her at the moment." | "가난한 사람이랑은 트위터에서 토론 안 해요. 미안하지만 지금 잔돈이 없네요." | 요약(포춘). 끝의 "for her"와 "for them"이 매체마다 다르다. 원본 캡처 못 봄 |
| 숨은 구조 부인 | 권도형, 2021-10-04 인터뷰(기소장 34(d)항) | "I don't think any of them have a contractual relationship with us." | "그 사람들 중 우리랑 계약한 곳은 없을 거예요." | 원문 |
| 속마음 | 테라폼 내부 직원 안내서, 2021(기소장 32항) | "saved our ass in May this year" | "올해 5월에 우리를 살려 줬다" | 원문 |
| 이자 유지 | 권도형 트윗, 2022-01-27(SEC 소장 캡처) | "I am resolved to find ways of subsidizing the yield reserve… maintaining the most attractive yield in DeFi stable will strengthen that growth & build up moats." | "이자 준비금을 메울 방법을 꼭 찾겠습니다. 가장 매력적인 이자를 지켜야 성장도 하고 해자도 쌓입니다." | 원문 |
| 돈 부음 | 권도형 트윗, 2022-02-18 | "Funded." | "채웠습니다." | 요약(코인텔레그래프) |
| 딸 이름 | 권도형 트윗, 2022-04-17(코리아중앙 2022-05-20) | "My dearest creation named after my greatest invention." / "If I ever have a son I shall name him Stable" | "내 가장 소중한 창조물에 내 가장 위대한 발명품의 이름을 붙였다." / "아들을 낳으면 이름은 스테이블로 하겠다." | 요약. 폭락 26일 전 |
| 폭락 첫날 | 권도형 트윗, 2022-05-09 | "Deploying more capital – steady lads" | "돈 더 넣는 중. 다들 버텨." | 검색 요약(코인데스크·유투데이). 원본 캡처 못 봄 |
| 같은 날 | 권도형 트윗, 2022-05-09(기소장 41(f)항) | "The LFG Council just voted to deploy 1.5B in capital (0.75B in BTC, 0.75B in UST)… we made this decision via an unanimous vote of the council." | "재단 위원회가 방금 15억 달러 투입을 만장일치로 정했습니다." (검찰: 위원회는 독립적이지 않았다) | 원문 |
| 사과 | 권도형 트윗, 2022-05-13 | "I am heartbroken about the pain my invention has brought on all of you." | "제 발명품이 여러분께 준 고통에 가슴이 찢어집니다." | 요약(더블록) |
| 도주설 | 권도형 트윗, 2022-09-17 | "I am not 'on the run' or anything similar… we are in full cooperation and we don't have anything to hide" | "도망 다니는 거 아닙니다. 전적으로 협조하고 있고 숨길 것도 없어요." | 검색 요약 |
| 같은 시기 녹음 | 권도형, 2022-08 무렵(기소장 5항) | "tell them to fuck off" | (그대로 더빙하기 어렵다) "꺼지라고 해." | 원문 |
| 폭락 중 트레이더 | 트레이딩 회사 직원, 2022-05(기소장 40항) | "about $100 M[illion] committed was enough to re-peg… Unfortunately it wasn't so simple this time" | "그땐 1억 달러면 다시 붙었는데, 이번엔 그렇게 간단하지 않네." | 원문 |
| 유죄 인정 | 권도형, 2025-08-12 법정(보도) | "I made false and misleading statements about why it regained its peg…" / "What I did was wrong." | "1달러가 왜 돌아왔는지 거짓말을 했습니다." / "제가 한 일은 잘못이었습니다." | 요약·검색 |
| 판결 | 엥겔마이어 판사, 2025-12-11 | "This was a fraud on an epic, generational scale." | "이건 한 세대에 한 번 나올 규모의 사기입니다." | 요약(NBC) |
| 선고 때 | 권도형, 2025-12-11 | "I want to tell these victims that I am sorry." | "피해자분들께 죄송하다고 말씀드리고 싶습니다." | 요약(NBC) |
| 검사장 | 제이 클레이턴 뉴욕남부지검장, 2025-08-12 | "Kwon attracted tens of billions in funds to Terraform's ecosystem by promising a self-stabilizing stablecoin." | "스스로 1달러를 지키는 코인이라며 수백억 달러를 끌어모았습니다." | 원문 |
| 피해자 | 선고 때 피해 편지(NBC) | "My savings, my future, and the results of years of sacrifice disappeared." | "제 저축도, 미래도, 몇 년의 희생도 다 사라졌습니다." | 요약 |

---

## 위기의 재료

- **고른 순간(편한 길과 어려운 길).** 2021년 5월. UST가 92센트 아래로 깨졌을 때 권도형은 "알고리즘이 못 지켰다"고 밝히는 어려운 길 대신, 트레이딩 회사에 40센트 루나를 앞당겨 주고 몰래 사 달라는 편한 길을 골랐다(T14, T15). 그리고 "블랙스완을 견뎠다"고 말했다(T16). 이 선택이 1년 동안 UST를 9배로 키웠다(T17). 둘째 고른 순간: 2022년 1~2월, 이자 준비금이 656만 달러까지 바닥났을 때 이율을 내리는 대신 4.5억 달러를 부었다(T4, T6).
- **바닥(그때 잃은 것).** 2022-05-07 ~ 05-13. 루나 77달러 → 0.0001달러, UST 1달러 → 15센트, 비트코인 8만 개 → 313개, 한국인 약 28만 명(T11, T13, T25). 권도형 개인: 2023-03 위조 여권으로 체포, 2025-12 징역 15년(T19, T22).
- **뒤집힘(크기).** (1) "알고리즘이 지켰다" → 사실은 사람이 돈으로 지켰다(법정에서 본인이 인정, T21). (2) "독립 위원회가 만장일치로 결정" → 권도형이 LFG와 테라폼을 함께 쥐고 있었다(T13). (3) 그 뒤 미국은 "달러 코인 발행사는 이자를 주지 말 것, 1:1 준비금을 둘 것"을 법에 적었다(T29). 유형으로는 "숨겨진 진실의 폭로"와 "규칙이 바뀜". 유형 이름은 `research/writing/crisis-in-short-stories.md` 기준으로 대본 단계에서 다시 맞춘다.

## 어긋나는 짝(아이러니)

1. **"준비금 없음" vs 비트코인 8만 개.** 2020년엔 "no reserve."(T8), 2022년엔 30억 달러어치 비트코인 준비금(T13). 그리고 9일 만에 313개.
2. **"알고리즘이 스스로 회복" vs 쿠코인 매수의 90%가 한 회사.** (T14, T16)
3. **딸 이름 "루나"(2022-04-17) → 26일 뒤 루나 99.99% 폭락.** (대독 표)
4. **"가난한 사람과는 토론 안 한다"(2021-07) → 그 경고(코폴라)가 맞았다.** 코폴라가 무엇을 경고했는지 원문은 못 봄(아래 미확인).
5. **"도망 중 아님, 전적으로 협조"(2022-09) vs "꺼지라고 해"(2022-08 녹음) vs 위조 여권(2023-03).** (T18, T19)
6. **"가장 매력적인 이자로 해자를 쌓겠다"(2022-01) → 그 이자가 UST의 70%를 한곳에 몰아 둑을 무너뜨렸다.** (T2, T6, 기소장 39항 "artificially inflating demand for UST")
7. **40센트에 받은 루나, 119달러 정점.** 지킨 회사는 10억 달러 넘게 벌었고 지켜졌다고 믿은 사람들은 잃었다(T15).
8. **"Funded."(2022-02-18) 한 단어 → 두 달 반 만에 절반이 빠짐.** (T4, T5)

## 투자에서 다르게 할 것(판단의 재료)

- **이자의 출처를 묻는 법.** 앵커 20%의 출처는 (대출 이자 + 담보 보상) + 보조금이었다. 보조금이 하루 약 40억 원씩 빠지고 있었고(작업자 계산, T5) 그 잔고는 공개돼 있었다. 시청자가 가져갈 한 줄: "이자가 시장 금리보다 훨씬 높으면, 누가 그 차이를 내고 있는지와 그 돈이 며칠 버티는지를 본다."
- **비교 잣대.** 2022-05 미국 3개월 국채 금리는 약 1% 안팎(기억, `data/irx_daily.csv`는 2024-10부터라 2022년 값은 없음. 대본에 쓰려면 다시 받는다). 19.5%와의 차이가 곧 보조금의 크기다.
- **지금과의 연결.** 지니어스법은 발행사가 이자를 못 주게 하고 1:1 준비금을 요구한다(T29). 서클 같은 발행사는 준비금(국채) 이자를 자기가 갖는다. "그 20%는 어디서 나왔나"의 반대편이 "지금 그 이자는 누가 갖나"다. 서클 쪽 숫자는 `facts-circle.md`와 맞춘다.
- 이 조사는 사건 쪽이라, 종목의 매수 값·날짜 조건(A14)은 서클 조사가 맡는다.

## 아직 확인 못 한 것(게시 전에 원문으로)

1. "debate the poor" 트윗 원문과 날짜(포춘은 2021년 7월, "for her"). 코폴라가 무엇을 경고했는지. 트윗 원본 캡처.
2. "Deploying more capital – steady lads" 원본 캡처와 정확한 시각(05-09 확인은 검색 요약).
3. LFG 2022-05-16 트윗 원문(80,394 → 313, 거래 상대 5만 BTC ↔ 15억 UST, 테라폼 33,206 BTC).
4. 앵커 이율의 정확한 값(19.5%가 목표, 실제 표시 이율은 19.4%대였다는 기억이 있음)과 그 시점 앱 화면 캡처.
5. JTBC "3.6%로 설계 → 20% 지시" 원 보도와 날짜.
6. 유죄 인정·선고 법정 기록(트랜스크립트) 원문. 판사가 피해 배상 명령을 내리지 않았다는 보도(검색 요약, 날짜 미상).
7. 루나 시가총액 정점 숫자(약 400억 달러라는 기억, 검찰은 2022-05 무렵 약 290억 달러라 적음). 2022-04-05 기준 유통량을 곱해 다시 잴 것.
8. 한국 피해 통계의 최신값(28만 명은 2022-05-15 금융위 집계). 한국 검찰의 피해자 수·피해액(일요신문 2026-02에 "1,541", "830" 같은 숫자가 있었으나 글자가 깨져 단위 확인 못 함). 신현성 1심 선고(2026-02 뒤).
9. 권도형 한국 이송 신청 여부와 수감 장소(2026).
10. 디지털자산기본법의 2026-08 ~ 10 진행과 이자 금지 조문.
11. 원화 환산에 쓸 환율 기준(2022-05 달러당 약 1,270원은 기억).
12. 몬테네그로 공항 체포 순간 사진, 법정 스케치.

찾아본 곳: justice.gov(웹 아카이브 사본), sec.gov(웹 아카이브 사본), congress.gov, Yahoo Finance API(CoinGecko는 365일 제한으로 실패, CryptoCompare는 키 필요), 위키미디어 공용, 코인데스크·코인텔레그래프·포춘·NBC·더블록·코리아중앙데일리, 한국 매체(디지털데일리, MTN, 이투데이, 시사저널, 이데일리, 블루밍비트, 네이트 뉴스).
