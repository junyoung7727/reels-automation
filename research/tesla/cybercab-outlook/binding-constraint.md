# 사이버캡 투입 속도를 지금 막고 있는 것

조사일: 2026-10-05. 질문은 하나다. "Tesla가 사이버캡(과 Model Y 로보택시)을 유료 무인 운행에 넣는 속도를 지금 실제로 제한하는 것은 무엇인가."

같은 폴더의 `scaling.md`(4장: Tesla 로보택시·사이버캡 숫자)와 `stakeholders.md`(4장: 정부, 5-3: 사고·원격 조작)에 이미 있는 사실은 다시 조사하지 않고 "기존 조사"로 표시해 끌어다 썼다.

## 읽는 법

가설:

| 기호 | 가설 |
|---|---|
| H1 | 연방·주 규제 |
| H2 | 차량 생산 (배터리·부품 포함) |
| H3 | 운영 구축 (차량 기지, 충전, 청소, 원격 인력, 지역별 검증, 의도적인 안전 속도 조절) |
| H4 | 서비스 구역 안의 승객 수요 |
| H5 | 주행 소프트웨어가 아직 충분히 일반적이지 않다 |
| H6 | 경제성 (대당 적자라 더 늘리고 싶지 않다) |

확인 수준:

- **원문 확인(직접 읽음)**: 이번 조사에는 없다. 모든 페이지를 요약 도구(WebFetch)로 읽었다.
- **원문 확인†(요약 도구로 읽음)**: 해당 URL을 열어 요약 도구가 뽑아 준 내용이다. 인용문은 자막에 쓰기 전에 원문과 글자 그대로 대조해야 한다.
- **검색 요약만**: 검색 결과 요약에만 나온 내용이다. 원문을 열지 못했다.
- **기존 조사**: `scaling.md`·`stakeholders.md`에 적힌 사실. 확인 수준은 그 파일의 표기를 따른다.

판별 표기: `+` 지지, `−` 반박, `0` 판별하지 못함(어느 가설과도 양립).

같은 원본을 옮긴 기사(예: Robotaxi Tracker 숫자를 옮긴 Electrek → Electric Viking → KuCoin)는 한 건으로 센다.

---

## 1. Tesla가 직접 한 말

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| 2분기 실적 발표(2026-07-22). Musk: "the constraint is we're -- we want to grow as fast as possible with robotaxi without harm to anyone." | 2026-07-22 | https://www.fool.com/earnings/call-transcripts/2026/08/05/tesla-tsla-q2-2026-earnings-call-transcript/ | 원문 확인† (같은 페이지를 두 번 읽었는데 문구가 조금 달랐다. 대조 필요) | H5+, H3+(안전 속도 조절). H2−, H4− (회사가 스스로 꼽은 제약이 생산·수요가 아니다) |
| Musk: "It's really just about going through what we call the march of nines of reliability, where you need, how many nines of reliability do you need to scale?" | 2026-07-22 | https://www.investing.com/news/transcripts/earnings-call-transcript-tesla-q2-2026-revenue-beats-eps-misses-as-stock-falls-93CH-4807216 | 원문 확인† | H5+ |
| Musk: "If we injure even one person, it'll be worldwide headline news, and regulators will immediately clamp down on our activities." | 2026-07-22 | 위 Investing.com | 원문 확인† | H5+, H3+. H1은 "지금 막는 규제"가 아니라 "사고가 나면 올 규제"다. H1 0 |
| Musk: "One of the things for Cybercab that should be noted is because it is a new vehicle chassis, we need to accumulate driving data that is specific to the Cybercab before we can put a lot of them on the road." Fool 판본에는 운전대·브레이크를 단 사이버캡으로 마일을 쌓아야 한다는 문장이 이어진다 | 2026-07-22 | 위 Investing.com, 위 Fool | 원문 확인† (두 녹취록에서 같은 문장) | H5+ (차종별 검증 필요). H2− (만든 차를 바로 못 넣는다고 스스로 말함) |
| "We have aligned our manufacturing targets to roughly match the projected growth rate of the unsupervised miles." 화자가 Fool 판독에서는 Musk, Investing.com 판독에서는 Elluswamy로 나왔다 | 2026-07-22 | 위 두 녹취록 | 원문 확인† (화자 불일치) | H2− : 생산이 자율주행 속도에 맞춰 정해지는 종속 변수라는 뜻. H5+ |
| Musk: "I don't think we're going to have any demand challenges with Robotaxi." | 2026-07-22 | 위 Investing.com | 원문 확인† | H4− (회사 주장. 독립 증거는 3장) |
| Elluswamy: "We have driven more than 380,000 miles of unsupervised robotaxi now across six cities in two different states. We have had zero notable incidents." "Since the beginning of this year, we have grown at double-digit growth rates to the number of unsupervised miles that the fleet drives every week." | 2026-07-22 | 위 Fool | 원문 확인† | 0 (모든 가설과 양립) |
| Elluswamy: "The reason we have been expanding across different cities instead of just doubling down on a single city is that we want to make sure that our stack is a very general one." | 2026-07-22 | 위 Fool | 원문 확인† | H5 약한 − ("도시마다 따로 맞춰야 한다"는 형태의 H5에 반대). 도시를 여는 것과 도시 안에서 대수를 늘리는 것은 다른 문제 |
| Taneja: "Production growth will be limited by our supply chain. This includes not just batteries, but also electronic components." (차량 전체 생산에 대한 말) | 2026-07-22 | 위 Investing.com | 원문 확인† | H2+ (다만 사이버캡이 아니라 전체 차량 생산) |
| 2분기 주주 자료: "Progress also continued on battery pack capacity expansion – the main limiting factor to near-term vehicle production volume increase." / "Battery: We continue to work on initiatives to increase battery pack capacity as it remains the limiting factor on ramping our vehicle production globally." / "We are also increasing production of 4680 cells to support production ramps of both Cybercab and Tesla Semi and increased production of Model Y." | 2026-07-22 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026049213/exhibit991.htm | 원문 확인† (1차 자료) | H2+ (전체 생산량의 한계. 로보택시 투입 대수와 연결한 문장은 아니다) |
| 전망 문구 변화. 1분기: "Cybercab, Tesla Semi and Megapack 3 are on schedule for volume production starting in 2026." 2분기: "Tesla Semi and Megapack 3 remain on schedule for production starting in 2026." 사이버캡이 문장에서 빠지고 "volume"도 빠졌다 | 2026-04, 2026-07-22 | 1분기 https://www.sec.gov/Archives/edgar/data/0001318605/000162828026026551/exhibit991.htm , 2분기 위 URL | 원문 확인† (두 자료를 각각 읽어 비교) | H2+ (대량 생산이 2026년 안에 오지 않는다). 원인이 배터리인지 자율주행 속도에 맞춘 것인지는 문서만으로 판별 불가 |
| 3분기 생산·인도 발표: 생산 464,391대(Model 3/Y 457,387, Other Models 7,004), 인도 486,532대. 사이버캡·로보택시 언급 없음. 3분기 실적 발표는 2026-10-21 장 마감 후, 중부시간 오후 4:30 | 2026-10-02 | https://www.sec.gov/Archives/edgar/data/0001318605/000162828026064366/exhibit991111111.htm | 원문 확인† (1차 자료) | Model Y는 분기 45만 대가 나온다 → Model Y 로보택시에 대해 H2− (결정적). 사이버캡: Other Models 7,004가 상한 (사이버캡이 이 항목에 들어가는지는 발표문에 없다. 검색 요약만) |
| Other Models 생산 추이: 1분기 13,775 → 2분기 8,822 → 3분기 7,004 | 2026 | 위 세 자료 | 원문 확인† | 사이버캡이 3분기에 수천 대 넘게 나왔을 수 없다는 상한. H2 0 |
| Nevada 청문회, Eric Early(사이버캡 수석 엔지니어): "The 5,000 has always been a ceiling for us. I don't think we'll be in a position by this time next year to deploy 5,000 vehicles, and it's not [because of] the technology. … I think we would be extremely happy and satisfied if we could get ourselves up to 2,500, maybe a bit higher than that in the next year." | 2026-08-20 | https://techcrunch.com/2026/08/20/tesla-uber-and-waymo-all-get-the-ok-to-operate-thousands-of-robotaxis-in-nevada/ | 원문 확인† | H1− (허가가 남는다). H5− (본인이 기술 탓이 아니라고 함). 남는 것은 H2·H3. 무엇 때문인지는 말하지 않았다. Musk의 "march of nines" 발언과 엇갈린다 |
| Musk(X): "Robotaxi operating hours moved from 10pm to 11pm. The main thing we're trying to solve is making sure that we don't run over pets when they're hard to see at night. Literally trying to avoid grey kittens on grey tarmac in the dark." | 2026-10-03 | https://x.com/elonmusk/status/2106239692866019479 (검색 결과 제목에 전문 노출), https://www.notateslaapp.com/news/4766/tesla-fsds-main-issue-with-nighttime-driving-is-avoiding-pets | 원문 확인† (Not a Tesla App). X 원문은 검색 요약만 | H5+ (결정적: 운행 시간을 막는 이유를 인식 성능이라고 직접 말함). 기지·충전·수요·규제로는 밤 11시 이후를 닫을 이유가 설명되지 않는다 |
| Elluswamy(X): 24시간 운행 시점을 묻자 "next month or so. the next tech to merge on the v15 plan will enable it." | 2026-09-04 | https://www.teslarati.com/tesla-robotaxi-24-7-service/ | 원문 확인† | H5+ (운행 시간 확대가 소프트웨어 판올림에 달려 있다) |
| Musk(X): "We are being extremely careful with autonomous safety, just as we are with making Teslas the safest cars in the world for human driving" | 2026-10-03 | https://teslanorth.com/2026/10/04/elon-musk-touts-careful-cybercab-rollout-austin-fleet-169/ | 원문 확인† / 기존 조사 | H3+(의도적 속도 조절), H5+ |
| Musk: "Robotaxi likely will not see material revenue until at least 2027." | 2026-07 | https://electrek.co/2026/07/06/tesla-cybercab-production-before-autonomy/ | 기존 조사 (원문 확인, 2차) | H6 0 (매출이 작다는 말이지 적자라서 안 늘린다는 말이 아니다) |

찾지 못한 것: Musk·Moravy·Early가 사이버캡 주간 생산 대수를 숫자로 말한 발언. 2분기 실적 발표에서 차량 기지·충전·청소·원격 인력에 대한 발언(요약 도구가 해당 단어를 찾지 못했다). Benzinga 녹취록은 403.

---

## 2. 공급: 만든 차와 운행하는 차

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| Giga Texas 출고 주차장에 사이버캡 약 250대 (드론 영상 Air~wave) | 2026-07-21 | https://www.notateslaapp.com/news/4471/over-200-tesla-cybercabs-spotted-at-giga-texas | 원문 확인† | H2− (유료 운행 시작 6주 전에 이미 출시 대수 45대의 5배가 서 있었다) |
| Giga Texas 출고 주차장 100대 이상 | 2026-07-06 | https://electrek.co/2026/07/06/tesla-cybercab-production-before-autonomy/ | 원문 확인† / 기존 조사 | H2− |
| Joe Tegtmeyer 드론 비행: 출고 주차장에 "many more Cybercabs", Starlink 모듈을 단 차가 처음으로 다수. 대수는 없다 | 2026-09-08 | https://teslanorth.com/2026/09/08/tesla-cybercab-starlink-giga-texas/ | 원문 확인† (대수 인용문은 검색 요약만) | H2 약한 − (숫자 없음) |
| Tegtmeyer의 초기 집계: 2026-03-25 36대 이상, 6월 중순 출고 주차장 102대, 6월 약 120대 | 2026-03 ~ 06 | https://x.com/JoeTegtmeyer/status/2036833663866880347 , basenor.com 재인용 | 검색 요약만 | 0 (출시 전) |
| VIN 순번: #2172(08-09 목격), #2493(08-31), #3358(09-19, Texas DMV 등록 명단에 오른 차). 계산: 08-09→09-19 41일에 1,186번, 주 약 200대. 08-31→09-19는 주 약 320대 | 2026-08 ~ 09 | https://x.com/tslaming/status/2101143120046096731 (402로 열지 못함), https://www.basenor.com/blogs/news/cybercab-vin-2172-spotted-how-far-along-is-production | 검색 요약만 (#3358, #2493). #2172는 기존 조사 | H2− 다만 약함: VIN 순번이 생산 대수와 같다는 가정이 필요하고 원문을 열지 못했다 |
| NHTSA 자체 인증 확인 절차 문서의 대상 차량 추정 1,000대 | 2026-09-03 | https://theautowire.com/2026/09/30/tesla-cybercab-nhtsa-special-order-september-30-zoox-exemption/ | 원문 확인† (2차 매체. NHTSA 문서 원본은 열지 않음) | H2− (당국 문서 기준으로도 등록 169대의 약 6배) |
| Texas DMV 등록 사이버캡: 45(08-31) → 49(09-08) → 58(09-18) → 69(09-22) → 125(09-25) → 169(10-02) | 2026-08-31 ~ 10-02 | 기존 조사 `scaling.md` 4-2 | 기존 조사 | 계산: 169 ÷ 3,358 = 5%, 169 ÷ 1,000 = 17%. 어느 분모로도 만든 차 대부분이 등록되지 않았다 → H2− |
| Miami 로보택시 기지에 Florida 번호판 사이버캡 약 21대 (2026-07-12 X 게시물). Miami의 유료 운행 차량은 Model Y 2~3대였다. 10-04 기준 사이버캡 유료 운행은 Austin뿐 | 2026-07-12 | https://www.basenor.com/blogs/news/teslas-miami-robotaxi-hub-6-details-that-matter | 원문 확인† (판매업체 블로그, X 게시물 인용) | H2− (차는 현지에 가 있는데 운행하지 않는다) |
| Houston 주차장에 사이버캡 다수(09-20), 9월에 Houston 기지로 약 45대 수송 | 2026-09 | 기존 조사 `scaling.md`·`stakeholders.md`; 45대는 startupfortune.com | 기존 조사 / 45대는 검색 요약만 | H2− |
| Robotaxi Tracker(목격 제보 집계): Austin에서 승객을 태운 것이 확인된 Tesla 차량이 9월 초 100대 이상 → 09-19 약 18대 → 09-22 8대(7일 기준). 같은 날 Texas 등록 476대(Model Y 409 + 사이버캡 67). 등록 차량 중 번호판이 확인된 것 265대, 30일 안에 목격된 것 179대 | 2026-09-22 | https://electrek.co/2026/09/22/tesla-robotaxi-active-fleet-austin-crashes-8-vehicles/ (Electric Viking·KuCoin 기사는 같은 원본의 재보도) | 원문 확인† | H2− (등록만 늘고 운행은 늘지 않는다). 주의: 제보 기반이라 화제가 식으면 과소 집계된다. "8대"를 실제 운행 대수로 읽으면 안 된다. H4·H3·H5 사이는 판별하지 못함 |
| Robotaxi Tracker: 사이버캡 활동 차량 70대(등록 169대 중), 무감독 전체 240대 | 2026-10 초 | robotaxitracker.com (접속 실패) | 검색 요약만 | 위 "8대"와 맞지 않는다. 집계 기준이 다르거나 9월 말에 실제로 늘었다. 확인 못 함 |
| Model Y 로보택시: 2026-06 중순 7일 활동 차량 31대(Austin 16, Dallas 7, Houston 3, Bay Area 5), 무감독 14대(4월 말 최고 25대에서 감소). 같은 때 Texas 인가 대수 Tesla 42, Waymo 577, Avride 317 | 2026-06-16 | https://electrek.co/2026/06/16/tesla-robotaxi-clean-crash-record-barely-running/ | 원문 확인† | **H2− 결정적**: Model Y는 공급 제약이 없는데 무감독 차량이 14대였다. **H1− 결정적**: 같은 Texas 법 아래 Waymo는 577대를 인가받았다 |
| Miami 무감독 출시 첫날 Model Y 2대, 48시간 안에 3대 | 2026-07-03 | 위 basenor Miami 글 (Elluswamy 발언으로 인용) | 원문 확인† (2차) | H2−, H1− (Florida는 무인 운행을 허용). H5+ 또는 H3+ |

읽는 법: 두 차종 모두 "만든 차 ≫ 등록한 차 ≥ 운행하는 차"다. 특히 Model Y는 분기에 45만 대가 나오는 차라 공급 가설이 설 자리가 없는데도 무감독 차량이 수십 대였다. 사이버캡만 보면 "신차라서 아직 못 만든다"로 읽힐 수 있는 것을 Model Y가 걸러 준다.

---

## 3. 수요 (Austin)

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| 출시일 오후 2시 직후 2.5마일 구간 예상 대기 40~50분, 오후 4시 1시간 이상 | 2026-09-04 | https://www.statesman.com/business/technology/article/austin-tesla-cybercab-launch-pricing-22417796.php | 검색 요약만 (페이지 열리지 않음) | H4− (차보다 호출이 많았다) |
| 같은 1.3마일 구간(Cabana Club → Lustre Pearl East): 사이버캡 $15.24·대기 1시간 이상, Model Y 로보택시 $12.04·약 14분, UberX $7.95·7분, Uber Wait & Save $6.41. 출시 첫날에는 사이버캡이 Model Y의 절반($6 대 $12)이었다. 출처는 Reddit 사용자 u/tmmoo의 화면 | 2026-09-07 | https://www.teslaoracle.com/2026/09/07/high-demand-for-tesla-cybercab-makes-it-more-expensive-than-uber-and-the-model-y-robotaxi/ | 원문 확인† (개인 화면 한 건) | H4− (사이버캡에 한해: 할증이 붙고 대기가 1시간). H6 약한 − (수요가 몰리면 값을 올려 받는다). 단, 같은 순간 Model Y 로보택시는 14분이면 왔다 → 초과 수요는 "로보택시"가 아니라 "사이버캡을 타 보려는 수요"일 수 있다 |
| 다른 비교: 15분 거리 사이버캡 $9.65 대 Uber $21, 3.3마일 $4.31 대 $10.96 | 2026-09 초 | https://finance.yahoo.com/technology/articles/teslas-cybercab-50-cheaper-uber-123020640.html (Benzinga, 09-10) | 원문 확인† (출처·표본 설명 없음) | H4− 약함. H6 0 |
| Robotaxi 앱이 App Store 여행 부문 무료 1위 | 2026-09-05 | https://www.teslaoracle.com/2026/09/05/tesla-tsla-opens-cybercabs-to-the-public-in-austin-texas-robotaxi-app-tops-the-charts-more/ | 원문 확인† | H4− 약함 (전국 내려받기 순위이지 Austin 탑승 수요가 아니다) |
| 첫 달 대기 45분 이상이 잦았다 (CNBC) | 2026-10-03 | https://www.cnbc.com/2026/10/03/tesla-cybercab-pressure-to-expand-after-rocky-first-month-in-austin.html | 검색 요약만 (이번에 403). 기존 조사 `stakeholders.md`는 원문 확인으로 표기 | H4− |
| 최근 대기 16분, 이용 가능 차량 7대 이상 | 2026-10 초 | 출처 불명 (검색 요약에만 나옴) | 검색 요약만 | 등록이 늘자 대기가 줄었다면 H4가 다음 제약이 될 수 있다는 신호. 원문 없음 |
| Tesla가 Austin 승객에게 "사이버캡 차량이 두 배가 됐다"는 앱 알림을 보냈다 (9월 21일 주) | 2026-09 하순 | https://www.notateslaapp.com/news/4768/tesla-extends-robotaxi-hours-in-austin-adds-111-cybercabs | 검색 요약만 (알림 문구) | H4 0 (수요를 끌어오려는 알림일 수도, 단순 공지일 수도 있다) |
| 2분기 유료 로보택시 주행: 1분기 약 110만 마일 → 2분기 약 70만 마일, 36% 감소. Tesla의 누적 도표에서 읽은 값. 같은 분기에 시장은 4곳에서 7곳으로 늘었다 | 2026-07-27 | https://avmarketstrategist.substack.com/p/tesla-q2-2026-3-new-robotaxi-markets (Daniel Abreu Marques) | 원문 확인† (도표 판독 추정치) | 0. 글쓴이 스스로 두 해석을 냈다: 유료 차량을 무감독 검증으로 돌렸다(H5·H3) 또는 이용률 문제(H4). Elluswamy의 "무감독 마일 주간 두 자릿수 성장"과는 모순이 아니다(유료 전체 대 무감독) |
| 서비스 구역: Austin 244 → 264제곱마일(출시 직전), Dallas 81, Houston 21. 사이버캡은 Model Y와 같은 Austin 구역을 쓴다. 한 블로그는 288제곱마일로 적었다 | 2026-09 | https://www.notateslaapp.com/news/4632/tesla-expands-robotaxi-geofences-in-dallas-and-austin , 기존 조사 | 검색 요약만 / 기존 조사 | H4 0. 264제곱마일에 사이버캡 45~169대는 구역 대비 차가 매우 적다 → 대기가 긴 것은 수요가 많아서가 아니라 차가 드물어서일 수 있다 |
| 운행 시간: 오전 6시~오후 10시(6개 도시) → Austin 오후 11시까지(10-03). 그 전 해 대부분은 오전 6시~새벽 2시였다 | 2026-10-03 | 위 Teslarati, Not a Tesla App 4766 | 원문 확인† | H5+ (시간이 오히려 줄었다가 조금 늘었다. 이유는 야간 인식). H4− (심야는 호출 수요가 있는 시간대다) |

찾지 못한 것: Tesla가 공개한 탑승 건수, 차량당 하루 탑승, 이용률. Austin의 Waymo·Uber 마일당 요금과 같은 조건 비교. Sensor Tower·Appfigures의 내려받기 수(검색 요약에 나온 "첫날 iOS 200만 건"은 출처가 없어 쓰지 않았다).

읽는 법: 출시 직후 사이버캡에는 초과 수요가 분명히 있었다. 그러나 표본이 개인 화면 몇 건이고, 같은 시각 Model Y 로보택시는 14분에 왔다. "수요가 부족해서 차를 안 늘린다"(H4)는 출시 첫 달에 대해서는 반박된다. "수요가 무한하다"까지는 확인되지 않는다.

---

## 4. 운영

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| Austin 405 E. St. Elmo Road에 로보택시 충전 기지 허가 신청. 약 128면. 1단계 V4 Supercharger 48기, 2단계 무선 충전기 80기. 기사는 "the first known large-scale deployment of this system"이라고 썼다. 완공 시점은 없다 | 2026-08-19 보도 | https://evwire.com/p/tesla-cybercab-wireless-chargers-austin-robotaxi-hub | 원문 확인† | H3+ : 출시 2주 전에 전용 기지가 아직 허가 단계였다. 무선 충전 80기는 등록 169대의 절반도 안 된다 |
| 지금 운행하는 사이버캡은 뒷범퍼 안쪽 덮개 뒤의 NACS 포트로 DC 급속 충전을 한다. AC 충전은 지원하지 않는다. 무선 충전은 "planned fleet feature" | 2026-09-05 | https://en.wikipedia.org/wiki/Tesla_Cybercab (Not a Tesla App 09-05, TipRanks 08-18 인용), https://www.notateslaapp.com/news/4653/tesla-cybercab-doesnt-support-ac-charging | 원문 확인† (위키백과) / Not a Tesla App은 검색 요약만 | H3+ : 무선 충전이 아직 작동하지 않으므로 사람이 케이블을 꽂아야 한다. 차 한 대를 늘릴 때마다 현장 인력이 든다 |
| 원격 조작자가 몰다 낸 사고 3건(2025-07 Austin, 2026-01 Austin, 2026-05 Houston). 원격 운영자는 Austin·Palo Alto의 자사 직원. 인원수는 비공개 | 2026-07-20 | 기존 조사 `stakeholders.md` 5-3 | 기존 조사 | H3 0 / H5 약한 + (막힌 차를 사람이 원격으로 빼 줘야 한다) |
| Tesla가 Giga Texas에 사이버캡 생산 관련 30개 이상 직무, Austin "Vehicle Operator, Robotaxi" 직무를 공고 | 2026 | https://www.statesman.com/business/technology/article/tesla-cybercab-hiring-gigafactory-texas-robotaxi-21126679.php | 검색 요약만 | 0 (날짜·인원 불명) |
| 안전요원·뒤따르는 차: Austin은 2026-01-22부터 일부 차량에서 요원을 뺐고 처음에는 뒤차에 태웠다. Bay Area는 지금도 운전석에 안전 운전자. 사이버캡에 뒤따르는 차가 붙는지는 검색에 나오지 않았다 | 2026-01 ~ 10 | https://electrek.co/2026/01/22/tesla-didnt-remove-the-robotaxi-safety-monitor-it-just-moved-them-to-a-trailing-car/ (검색 요약만), 기존 조사 | 검색 요약만 / 기존 조사 | H5 + (2026-01 시점). 사이버캡에 대해서는 증거 없음. 보이지 않는다는 것만으로 "없다"고 쓰지 않는다 |
| 사이버캡이 호텔 주차장에서 공사로 한 차로가 막히자 네 바퀴를 돌고 출발 지점에 승객을 내려 줬다 | 2026-09 | https://futurism.com/advanced-transport/cybercab-trapped-hotel-lot | 검색 요약만 | H5+ (일화 한 건) |
| 사이버캡은 고속도로(MoPac, US-183)와 평면 철도 건널목을 피한다. 10분 거리를 70분에 간 사례 | 2026-09-14 | https://electrek.co/2026/09/14/tesla-cybercab-70-minute-austin-detour/ | 원문 확인† / 기존 조사 | H5+ (운행 조건을 좁혀 두었다) |
| Austin 소방국: 운전대·페달이 없어 긴급 시 차를 옮길 수단이 없다는 우려. 시에는 규제 권한이 없다 | 2026-09 | 기존 조사 `stakeholders.md` 4-2 | 기존 조사 | H1 0 (지금 운행을 막지 않는다), H3 약한 + |
| 외부 댓글의 주장: 행사 기간에 Tesla가 모든 차를 원격으로 지켜봤고 그것은 지속할 수 없다 | 2026-09-22 | 위 Electrek 09-22 기사의 독자 댓글 | 원문 확인† (익명 댓글. 근거 없음) | 증거로 쓰지 않는다 |

찾지 못한 것: Austin·Dallas·Houston·Miami의 기지 수와 면적, 청소 방식과 인원, 원격 운영자 수와 차량 대비 비율, 원격 개입 횟수. Tesla는 이 숫자를 내지 않는다. 이 숫자가 없어서 H3(물리적 운영 능력)과 H5(소프트웨어 신뢰도)를 깔끔하게 가르지 못한다. St. Elmo 기지 허가의 날짜·공사 기간(Statesman 기사는 열리지 않았다).

---

## 5. 소프트웨어와 사고

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| 운행 중인 로보택시는 v15 FSD의 초기판을 쓴다(Elluswamy, 2분기 실적 발표). v15 전체 적용은 2026-10 목표, 약 100억 매개변수 | 2026-07-22, 2026-10 | 위 Fool 녹취록, 위 Not a Tesla App 4766 | 원문 확인† | H5+ (24시간 운행을 다음 판에 걸어 두었다) |
| NHTSA 상시 일반 명령(SGO) 보고 누계: 14건(2026-01까지) → 17건(2025-07~2026-03) → 18건(2026-06 중순) → 22건(2026-07-20) | 2026 | 기존 조사, https://electrek.co/2026/06/16/tesla-robotaxi-clean-crash-record-barely-running/ | 기존 조사 / 원문 확인† | 0. 월별 표는 만들지 못했다(NHTSA 원자료를 열지 못함) |
| 2026-07 중순~08-17 신규 2건: 빈 무감독 Model Y가 시속 2마일로 주차장 출구의 쇠사슬에 닿음, 승객 2명을 태운 차가 시속 1마일 미만으로 호텔 진입로 말뚝을 긁음 | 2026-08 | https://buttondown.com/patricknovak1/archive/tesla-ep607-nhtsa-data-shows-tesla-s-robotaxi-fleet/ | 검색 요약만 (접속 실패) | H5 약한 + (저속 좁은 공간 기동이 약점), 중대 사고는 없음 |
| 사이버캡 유료 운행 뒤 중대한 충돌 보고 없음 | 2026-10-03 | 기존 조사 (CNBC, Tesla North) | 기존 조사 | H5 약한 − (한 달, 최대 169대) |
| 사고율 추정: 5만 5천~5만 7천 마일당 1건(Electrek 추정), Goldman Sachs 5만~7만 마일당 1건 | 2026-02 ~ 09 | 기존 조사 `scaling.md` 4-1 | 기존 조사 | H5 0 (분모가 추정이고 대부분 상대 과실) |
| NHTSA 특별 명령(2026-09-10 서명, 21개 항목, 기한 09-30). FMVSS 101·102·108·111·135를 운전대·페달 없는 차가 어떻게 충족하는지 묻는다. "An audit query doesn't pull cars off the road." 자체 인증을 지키지 못하면 Part 555 면제로 가야 하고 상한은 12개월에 2,500대(주 약 48대). Zoox는 특별 명령에서 감사 종결까지 35개월 | 2026-09-30 | https://theautowire.com/2026/09/30/tesla-cybercab-nhtsa-special-order-september-30-zoox-exemption/ | 원문 확인† (2차 매체) | **H1: 지금은 −, 다음 제약 후보로 +**. 지금 등록 169대는 2,500대에 한참 못 미친다. 상한이 걸리면 사이버캡에만 적용되고 Model Y에는 적용되지 않는다 |

도시별 "첫 탑승 → 안전요원 제거" 표:

| 지역 | 첫 유료 탑승 | 출시 때 차 안의 사람 | 무감독 전환 | 걸린 시간 | 출처 / 확인 |
|---|---|---|---|---|---|
| Austin | 2025-06-22 | 조수석 안전요원 | 2026-01-22 (일부 차량, 처음에는 뒤차에 요원) | 약 7개월 | 기존 조사 |
| Bay Area | 2025-07-31 | 운전석 안전 운전자 | 아직 아님 (2026-10 기준 14개월 넘음). 무인 시험·배치 허가가 없고 CPUC 자율주행 여객 허가는 신청하지 않았다 | 미완 | 기존 조사 `stakeholders.md` 4-3 |
| Dallas | 2026-04-18 | 없음(무감독으로 출시) | 출시일 | 0일 | 기존 조사 (Tesla North), 1분기 자료 "launched unsupervised rides in both Dallas and Houston in April" 원문 확인† |
| Houston | 2026-04-18 | 없음 | 출시일 | 0일 | 위와 같음 |
| Miami | 2026-07-03 | 2분기 자료는 "launched unsupervised rides in Miami, Orlando and Tampa". 한 매체는 요원 탑승 여부를 Tesla가 밝히지 않았다고 썼다 | 출시일(회사 표현 기준) | 0일 | 2분기 자료 원문 확인† / 요원 여부는 검색 요약만 |
| Orlando, Tampa | 2026-07-21 | 위와 같음 | 출시일(회사 표현 기준) | 0일 | 위와 같음 |
| Phoenix | 미출시 | | | | 2분기 자료 "준비 중"(기존 조사). Arizona 허가는 무인 운행을 허용하지 않는다(기존 조사, 검색 요약만) |
| Las Vegas | 미출시 | | | | Nevada 5,000대 허가 2026-08-20. 허가 후 120일 안에 운행을 시작해야 한다는 조건은 검색 요약만 |

읽는 법: Austin에서 7개월 걸린 일이 Dallas·Houston·Florida에서는 출시일에 됐다. "도시마다 긴 검증이 필요하다"는 형태의 H5는 약해졌다. 그러나 새 도시는 2~3대로 열었고 몇 달 뒤에도 한 자릿수였다(Dallas 7, Houston 3, 2026-06). 도시를 여는 능력은 생겼고, 도시 안에서 대수를 늘리는 데서 멈춰 있다. California만 규제가 직접 막고 있고, 그마저 Tesla가 신청하지 않은 허가가 있다.

---

## 6. 경제성

| 관찰 | 날짜 | 출처 URL | 확인 | 판별 |
|---|---|---|---|---|
| 2분기 실적 발표에서 로보택시 매출·마일당 비용·손익은 공개되지 않았다. 로보택시 매출은 "Services and other"에 섞여 있다 | 2026-07-22 | 위 Fool·Investing.com 녹취록 | 원문 확인† | H6 0 |
| 2026년 설비투자 약 250억 달러, 2분기 잉여현금흐름 약 −10억 달러 | 2026-07-22 | https://techcrunch.com/2026/07/22/tesla-spending-skyrockets-as-cybercab-semi-megapack-production-timeline-slips/ | 원문 확인† | H6 0 (돈을 아끼려고 속도를 늦추는 회사의 모습은 아니다. 약한 −) |
| 요금: Austin 기본 $3.00 + 마일당 $1.40(2026-03). 사이버캡은 출시 첫날 Model Y의 절반, 사흘 뒤 할증으로 UberX의 약 2배 | 2026-03, 2026-09 | 기존 조사, 3장 | 검색 요약만 / 원문 확인† | H6 0 |
| 증권사 추정 마일당 비용: Morgan Stanley Tesla $0.81, Goldman Sachs 로보택시 일반 $1.34 | 2025-12 ~ 2026-09 | 기존 조사 `scaling.md` 6장 | 기존 조사 | H6 0 (추정이지 관찰이 아니다) |
| Musk 보상안은 로보택시 100만 대 상업 운행을 목표로 건다 | 2025-11 | 기존 조사 `stakeholders.md` 5-1 | 기존 조사 (원문 확인) | H6 약한 − (경영진의 유인은 대수를 늘리는 쪽이다) |

Tesla가 대당 손익을 공개한 적이 없으므로 H6을 지지하거나 반박할 관찰이 원래 존재하지 않는다. 증거가 없다는 것을 H6의 반증으로 세지 않는다.

---

## 가설별 판정

| 가설 | 지지하는 관찰 | 반박하는 관찰 | 판별하지 못하는 관찰 | 판정 |
|---|---|---|---|---|
| H1 규제 | California: 무인 허가 없음. Arizona 허가는 무인 불가. NHTSA 특별 명령이 진행 중이고 지면 연 2,500대 상한 | Texas는 자기인증·무료·상한 없음이고 같은 법으로 Waymo 577대. Nevada 5,000대를 받고도 Tesla가 못 채운다고 말함. NHTSA 절차는 운행을 멈추지 않음. Florida는 무인 허용인데 2~3대로 출시 | Austin 소방국 우려(권한 없음) | **지금 Texas·Florida·Nevada에서는 제약이 아니다.** California에서만 제약이고 일부는 Tesla가 신청하지 않은 것. 사이버캡에 한해 다음 제약 후보 |
| H2 생산 | 2분기 자료: 배터리 팩이 차량 생산의 "main limiting factor". 전망 문구에서 사이버캡 대량 생산이 빠짐. Other Models 생산 7,004대(3분기) | Model Y는 분기 45만 대인데 무감독 차량 14~수십 대. 사이버캡 출고 주차장 약 250대(07-21), VIN #3358(09-19), NHTSA 추정 1,000대 대 등록 169대. Miami·Houston에 차가 먼저 가서 서 있음. "manufacturing targets ... match ... unsupervised miles" | Tegtmeyer의 숫자 없는 관찰 | **지금은 제약이 아니다** (두 차종 모두). 연 수만 대로 가는 단계에서는 제약이 된다 |
| H3 운영 구축 | St. Elmo 기지가 출시 2주 전 허가 단계. 무선 충전 미작동, 사람이 케이블을 꽂음. 원격 조작 사고 3건. Musk "extremely careful". Early "not the technology" | (직접 반박하는 관찰을 찾지 못했다) | 기지·인력 숫자가 비공개라 대부분 판별 불가 | **부분적으로 지지.** "의도적인 안전 속도 조절"은 Tesla가 직접 말한 것이다. 물리적 능력(기지·충전·인력)이 한계인지는 숫자가 없어 확정하지 못함 |
| H4 수요 | 2분기 유료 마일 36% 감소(도표 판독). 같은 시각 Model Y 로보택시는 14분 대기. 9월 하순 목격 집계 급감 | 사이버캡 대기 40~60분 이상, 할증으로 UberX의 2배, 앱 1위. Musk "no demand challenges". 심야 운행을 수요가 아니라 인식 때문에 닫음 | 264제곱마일에 차가 드물어서 생기는 대기 | **출시 첫 달 사이버캡에 대해서는 반박된다.** Model Y 로보택시와 새 도시에 대해서는 열려 있다 |
| H5 소프트웨어 | Musk: "march of nines", "the constraint is ... without harm", 사이버캡 전용 주행 자료 필요, 야간 반려동물 인식 때문에 운행 시간 제한. 24시간 운행을 v15에 걸어 둠. 고속도로·철도 건널목 회피. 주차장에 갇힌 사례. 저속 접촉 사고 | Dallas·Houston·Florida는 출시일부터 무감독. 사이버캡 한 달 동안 중대 사고 없음. Early "it's not [because of] the technology" | 사고율 추정치(분모가 추정) | **가장 강하게 지지된다.** 다만 "도시별 검증" 형태가 아니라 "대수와 시간대를 늘려도 될 만큼의 신뢰도" 형태다 |
| H6 경제성 | (관찰 없음) | 설비투자 250억 달러, 보상안의 유인, 수요가 몰리면 할증 | 대당 손익 비공개 | **판단할 수 없다.** 관찰 가능한 자료 자체가 없다 |

---

## 질문에 대한 답

**답.** 2026-10-05 기준으로 증거가 가장 강하게 가리키는 제약은 **H5(소프트웨어 신뢰도)이고, 그것이 H3의 한 부분인 "의도적인 안전 속도 조절"로 나타난다.** Tesla는 차를 만들 수 있고(H2 아님), Texas·Florida·Nevada에서 허가는 남으며(H1 아님), 출시 첫 달 사이버캡 수요는 차보다 많았다(H4 아님). 그런데도 대수와 운행 시간을 조금씩만 늘린다. 이유를 회사가 직접 말했다: "march of nines", "without harm to anyone", 그리고 밤 11시 이후를 닫는 이유로 야간 반려동물 인식.

이 결론을 가장 잘 가르는 관찰 일곱 가지:

1. Model Y는 분기 45만 대가 나오는데 무감독 로보택시는 2026-06에 14대였다. 생산 가설은 Model Y에서 성립하지 않는다.
2. 같은 Texas 법으로 Waymo는 577대, Tesla는 42대를 인가받았다(2026-06). Nevada는 5,000대를 줬고 Tesla가 못 채운다고 했다. 규제 가설은 이 세 주에서 성립하지 않는다.
3. 사이버캡은 출고 주차장에 약 250대(07-21), VIN 순번 3,358(09-19, 검색 요약만), NHTSA 추정 1,000대인데 등록은 169대다.
4. Musk가 운행 시간을 막는 이유를 인식 성능("grey kittens on grey tarmac in the dark")이라고 말했고, 24시간 운행은 v15 판올림에 걸려 있다. 기지·수요·규제로는 설명되지 않는 제한이다.
5. Musk: 사이버캡은 새 차체라 전용 주행 자료를 쌓아야 "put a lot of them on the road"가 된다. 그리고 생산 목표를 무감독 마일 증가 속도에 맞췄다.
6. 출시 주 사이버캡 대기 1시간 이상, 할증 요금이 UberX의 약 2배. 수요 부족은 아니다.
7. Dallas·Houston·Florida는 출시일부터 무감독이었지만 2~3대로 시작했다. 도시를 여는 것이 아니라 도시 안에서 대수를 늘리는 데서 멈춘다.

**다음에 걸릴 제약.** H5가 풀리면(v15로 24시간·고속도로가 열리고 등록 차량이 실제로 다 운행하면) 순서대로:

- **H3 물리적 운영**: 무선 충전이 아직 작동하지 않아 사람이 케이블을 꽂는다. Austin 전용 기지는 2026-08에 허가 단계였고 계획된 무선 충전기는 80기다. 수백 대까지는 버티겠지만 수천 대에서는 기지·인력이 먼저 모자란다.
- **H2 배터리와 생산**: Tesla가 직접 배터리 팩을 차량 생산의 "main limiting factor"라고 썼고 사이버캡을 2026년 대량 생산 문장에서 뺐다. 연 수만 대 단계의 제약이다.
- **H1 연방 상한(사이버캡만)**: NHTSA가 자체 인증을 받아들이지 않으면 연 2,500대 상한이 걸린다. Nevada에서 Early가 말한 "1년에 2,500대쯤"과 숫자가 같다. 우연인지는 확인하지 못했다.
- **H4 수요**: 차가 수백 대가 되면 264제곱마일 Austin에서 대기 시간과 할증이 사라지는지로 드러난다. 지금은 알 수 없다.

**이 판단을 바꿀 3~6개월 안의 관찰.**

| 관찰 | 바뀌는 판단 |
|---|---|
| 2026-10-21 3분기 실적 발표에서 로보택시 대수·이용률·손익을 공개하거나, 속도의 이유를 생산·배터리로 말한다 | H2 또는 H6 쪽으로 |
| v15가 깔리고 24시간·고속도로 운행이 열렸는데도 등록 대수가 주 수십 대에 머문다 | H5가 아니라 H3(기지·인력)이나 H2가 지금의 제약이었다 |
| v15 뒤 등록이 주 수백 대로 뛰고 Houston·Dallas·Miami에서 사이버캡 유료 운행이 시작된다 | H5가 맞았다. 다음은 H3·H2 |
| 등록이 수백 대로 늘었는데 대기 시간이 5분 안팎, 할증이 사라지고 요금을 내린다 | H4가 다음 제약 |
| NHTSA가 사이버캡 실차 검사를 하거나 Tesla가 Part 555 면제를 신청한다 | H1이 사이버캡의 제약으로 올라온다 |
| 부상자가 나온 사이버캡 사고, 또는 운행 대수·구역 축소 | H5 확정, 일정 전체가 늦어진다 |
| St. Elmo 기지 완공과 무선 충전 가동, 원격 운영자 대량 채용 공고 | H3이 풀리는 중 |
| 출고 주차장의 사이버캡이 줄고 VIN 증가가 주 100대 아래로 떨어진다 | H2가 앞당겨진다 |

**범위.** 이 답은 Texas(주로 Austin)의 2026-09~10 상황에 대한 것이다. California에서는 규제(H1)가 직접적인 제약이다. Nevada·Arizona는 아직 운행 전이라 무엇이 막는지 관찰할 수 없다. H3과 H5는 한 사슬의 두 고리라 완전히 가르지 못했다. "소프트웨어가 덜 믿을 만해서 회사가 일부러 천천히 간다"가 증거에 맞는 서술이고, "소프트웨어는 준비됐는데 기지와 인력이 모자라다"(Early의 발언이 암시하는 쪽)를 배제할 숫자는 없다.

**남은 공백.**

- 모든 출처를 요약 도구로 읽었다. 인용문은 원문 대조 전이다. 특히 "aligned our manufacturing targets"는 화자가 판독마다 달랐고(Musk 또는 Elluswamy), "the constraint is…"는 문구가 두 가지로 나왔다.
- 사이버캡 누적 생산 대수의 공식 숫자가 없다. VIN #3358과 #2493은 X 게시물로 검색 요약에서만 봤다. 3분기 "Other Models 7,004대"에 사이버캡이 들어가는지도 발표문에는 없다.
- 실제 운행 대수를 모른다. Robotaxi Tracker의 "7일 8대"(09-22)와 "사이버캡 70대"(10월 초, 검색 요약만)는 서로 맞지 않고 둘 다 제보 기반이다. robotaxitracker.com과 TexasAVTracker는 접속하지 못했다.
- 원격 운영자 수, 차량당 개입 횟수, 기지 수, 청소 방식은 공개 자료가 없다.
- 9월 3일 이후의 NHTSA SGO 사고 보고와 월별 건수 표는 만들지 못했다(NHTSA 원자료·Buttondown 접속 실패). 사이버캡 전용 사고 건수도 없다.
- CNBC 10-03 기사, Statesman 기사 3건, Benzinga 녹취록, Mitrade(Motley Fool 전재)는 열리지 않았다.
- 대당 손익은 Tesla가 공개한 적이 없다. H6은 판단 불가로 남는다.
- Florida 세 도시에 안전요원이나 뒤따르는 차가 있는지, 사이버캡에 뒤따르는 차가 붙는지 확인하지 못했다.
- 10월 초 "대기 16분"은 출처를 찾지 못했다.
