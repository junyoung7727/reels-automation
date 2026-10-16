# 스페이스X의 800MHz 주파수 인수와 미국 통신 3사 급락: 사실 정리

- 조사한 날: 2026-10-11(일, KST). 사건: 2026-10-08(목) 미국 장 마감 뒤 발표, 10-09(금) 주가 반응.
- 확인 범위 표기: **[원문]** 원문 페이지를 직접 받아 읽음 / **[요약도구]** 요약 도구를 거쳐 읽음 / **[검색요약]** 검색 결과 요약만 봄 / **[계산]** 받은 가격·공시 숫자로 작업자가 계산 / **[기억]** 작업자의 기억(확인 안 됨).
- 주가는 야후 파이낸스 차트 API(`query1.finance.yahoo.com/v8/finance/chart/<티커>`)에서 일별 종가·배당 내역을 받아 계산했다 **[원문 데이터 + 계산]**. 주식 수·부채·가이던스는 SEC 공시 원문.
- 게시 전에 원문으로 다시 볼 것은 맨 아래 "확인하지 못한 것"에 모았다.

## 0. 전제 확인 (먼저 읽을 것)

| 받은 전제 | 판정 | 근거 |
|---|---|---|
| 10-08 장 마감 뒤 스페이스X가 그레인의 전국 800MHz 면허(최대 14MHz 쌍)를 사기로 했다 | **사실** | 그레인 보도자료, 스페이스X 성명(여러 매체 인용) |
| 값은 약 80억 달러 | **보도일 뿐, 회사 확인 없음** | WSJ가 "소식통"으로 보도, 로이터가 재인용. 두 회사는 금액 비공개 |
| 버라이즌 -8.75%, AT&T -9.81% | **배당락을 뺀 숫자다.** 종가 대 종가로는 -10.14%, -10.82% | 아래 4절. 두 회사 모두 10-09가 배당락일 |
| T모바일 -13.27% 또는 -9.54% | 종가는 **-13.27%**. -9.5%는 장중(오전) 숫자 | 4절 |
| 3사 시가총액 390억 달러 증발 | **금요일 개장 무렵 숫자.** 종가 기준은 약 575억~623억 달러 | 4절 계산 |
| "T모바일이 29억 달러에 판 것을 그레인이 두 달 뒤 80억에 되팔았다" | **부정확.** 29억은 현금만이고 그레인은 600MHz 면허도 넘겼다(T모바일 장부상 합계 36억 달러). 값은 2025-05-30 계약에서 정해졌고 2026-08에 마무리만 됐다. T모바일은 되판 돈의 일부를 받을 수 있는 조항을 갖고 있다 | 2절 |
| AT&T "2000년 이후 최악의 날" | 종가 대 종가(-10.82%)로는 맞다. 그러나 CNBC가 쓴 -9.81% 기준이면 2023-04-20(-10.41%)이 더 나빴다. 숫자와 "이후"를 섞어 쓰면 틀린다 | 4절 |

## 1. 거래의 사실

**1-1. 누가 무엇을.** 그레인 매니지먼트(Grain Management, 디지털 인프라 투자사)가 가진 전국 800MHz 주파수 면허 묶음 100%를 스페이스X가 산다. 확정 계약(definitive agreement). FCC 승인과 통상의 종결 조건이 붙는다.
- 원문: "Grain Management, LLC ("Grain") ... today announced a definitive agreement under which SpaceX will acquire 100% of Grain's nationwide 800 MHz spectrum portfolio. The transaction is subject to FCC approval and other customary closing conditions." (WASHINGTON, Oct. 8, 2026 /PRNewswire/)
- 출처: https://www.morningstar.com/news/pr-newswire/20261008ph67427/grain-management-announces-definitive-agreement-to-sell-nationwide-800-mhz-spectrum-portfolio-to-spacex **[원문]**(PR뉴스와이어 전재). 그레인 자체 페이지 https://graingp.com/grain-management-announces-definitive-agreement-to-sell-nationwide-800-mhz-spectrum-portfolio-to-spacex/ **[요약도구]**
- 그레인 쪽 자문: BDT & MSD Partners(재무), Milbank(법률), Latham & Watkins(규제). 같은 보도자료 **[원문]**

**1-2. 주파수의 크기.** "최대 14MHz 쌍(paired)". 대역은 817~824MHz와 862~869MHz(7MHz + 7MHz).
- 스페이스X 성명 원문(CNBC 인용): "license portfolio of up to 14 megahertz of paired spectrum in the 800 MHz band" — https://www.cnbc.com/2026/10/08/spacex-spectrum-license-att-verizon-tmobile.html **[원문]**
- 대역 번호: Teslarati "up to 14 MHz of paired spectrum in the 817 to 824 MHz and 862 to 869 MHz bands" — https://www.teslarati.com/spacex-direc-cell-att-verizon-t-mobile-challenge/ **[원문]**(2차 매체). 같은 대역이 과거 디시 옵션 기사에서는 "13.5MHz"로 적혔다 **[검색요약]** → **출처 간 차이: 14MHz("up to") 대 13.5MHz.** 대본에는 "최대 14MHz"로.

**1-3. 값.** 두 회사는 금액을 밝히지 않았다. WSJ가 소식통을 인용해 **현금 약 80억 달러**라고 보도했고 로이터·라이트리딩·악시오스가 재인용했다.
- 로이터(글로브앤드메일 전재): "While the companies did not share financial terms of the deal, the Wall Street Journal reported, citing sources, that it is worth US$8-billion." — https://www.theglobeandmail.com/business/article-us-european-telecom-stocks-slide-as-spacex-spectrum-deal-rattles/ **[원문]**
- 라이트리딩: "Financial terms were not disclosed, though the Wall Street Journal reports that SpaceX will be paying $8 billion in cash." — https://www.lightreading.com/satellite/spacex-grain-s-lowband-spectrum-is-our-ticket-to-becoming-major-mobile-carrier- **[원문]**
- WSJ 원문은 열지 못했다. 스페이스X의 8-K 등 공시도 찾지 못했다(SEC 전문 검색 10-01~10-11, 0건) **[원문 검색]**.
- 참고: 8월에 블룸버그는 이 주파수를 "60억 달러로 평가"되는 매물로 보도했고, 스페이스X와 **AST 스페이스모바일**이 모두 관심을 보였다고 했다. 제목 "SpaceX, AST Said Seeking Grain Spectrum Valued at $6 Billion" — https://news.bgov.com/mergers-and-acquisitions/spacex-ast-said-seeking-to-buy-spectrum-valued-at-6-billion **[원문, 앞부분만 공개]**. 즉 두 달 사이 시장 추정 60억 → 보도된 낙찰가 80억. 경쟁에서 진 AST는 금요일 -10.5%(4절).

**1-4. 발표 시각.** 10-08(목) 미 동부 16:15 무렵, 장 마감 직후. 한국 시간 10-09(금) 05:15 무렵.
- X의 @SawyerMerritt 게시 "SpaceX has just officially announced two major milestones..." 작성 시각 20:19:17 UTC — https://x.com/SawyerMerritt/status/2108291161190526979 **[원문, fxtwitter API로 읽음]**
- CNBC 첫 기사 "Published Thu, Oct 8 2026 4:43 PM EDT" **[원문]**

**1-5. 스페이스X의 말(영어 원문).** 스페이스X 사이트(spacex.com/updates)는 스크립트 페이지라 직접 읽지 못했다. 아래는 여러 매체가 같은 문장으로 인용한 것이다.
- "This prime low-band spectrum addresses one of the key remaining technical gaps that will pave the way for Starlink Mobile to become a major mobile carrier in the US." (CNBC, 라이트리딩, 쿼츠 동일) **[원문 2곳 이상]**
- "Once we receive final FCC approval, Starlink Mobile will deploy a flexible architecture combining our satellite-to-mobile constellation in space with an advanced terrestrial deployment that can seamlessly connect devices everywhere" (NBC, 라이트리딩) — https://www.nbcnews.com/business/corporations/elon-musk-spacex-verizon-tmobile-att-rcna602525 **[원문]**
- "While Starlink Mobile's global 2 GHz mid-band spectrum will provide high-bandwidth capacity in the United States, this new low-band spectrum will provide a coverage layer that ensures Starlink Mobile's signal penetrates through obstacles, such as walls, and can provide service to customers' devices even when they are in buildings" — https://www.satellitetoday.com/connectivity/2026/10/08/spacex-moves-to-acquire-nationwide-low-band-spectrum-for-starlink-mobile/ **[원문]**
- "Starlink Mobile can now become the first network operator to deploy both satellite and terrestrial spectrum. One network that provides Americans with a reliable service indoors, outdoors, in cellular dead zones, and everywhere in between" — https://www.theregister.com/networks/2026/10/09/spacex-to-buy-key-spectrum-that-could-help-starlink-mobile-become-major-us-cell-carrier/5302393 **[원문]**
- "Critically, most existing mobile devices already support this underused band" (라이트리딩) **[원문]**
- 스페이스X 공식 X 계정 글(Teslarati에 실린 글): "We announced an agreement to acquire a nationwide low-band spectrum license portfolio that will pave the way for @Starlink to become a major mobile carrier in the US." **[원문, 2차 매체 전재]**

**1-6. 머스크의 말.** X 게시글 자체는 열지 못했다. NBC, 라이트리딩, 벤징가(트윗 전문 삽입), 야후가 같은 문장을 실었다.
- "This is the last critical piece of the spectrum puzzle needed for SpaceX to provide complete phone coverage in America" **[원문 3곳]**
- "very big deal" (CNBC: "In a post on X, SpaceX CEO Elon Musk called it a 'very big deal.'") **[원문]**
- 하루 전(10-07) FCC의 위성 1만5천 기 승인에 대해: "Starlink Mobile (direct-to-cell) V2 satellites are incredible. This @SpaceX constellation will enable more than 100 times the bandwidth of our current V1 system!" — https://www.tikr.com/blog/musk-starlink-mobile-v2-brings-100-times-the-bandwidth-raising-the-stakes-for-verizon-and-att **[원문, 2차 매체]**

**1-7. 무엇을 짓겠다는 것인가.** 위성만이 아니다. **위성(2GHz) + 땅 위의 망(800MHz)을 합친 하이브리드**이고, 서비스 이름은 "Starlink Mobile"(스페이스X의 자회사, NBC).
- FCC에 낸 공익 진술서(라이트리딩·레지스터가 인용): 800MHz로 "operate standards-based advanced wireless equipment", 안테나는 "towers, rooftops and other structures"에. "SpaceX will engineer this overlay to meet the Grain Approval Order's construction benchmarks." 거래는 "will increase competition in the mobile services market." 신속 심사를 요청했다 **[원문, 라이트리딩]**
- 라이트셰드 월트 피에식: 800MHz는 위성에 싣지 않고 지상망의 바닥층으로 쓸 것. "We doubt SpaceX will bother putting this spectrum in its satellites ... Lowband frequencies require massive antennas, which are not ideal for satellites produced at scale." **[원문, 라이트리딩]**

**1-8. 언제.** 이번 800MHz 서비스의 개시 시점은 **밝히지 않았다.** CNBC: "SpaceX didn't immediately respond to a request for further information, including when its new services may come online" **[원문]**.
- 관련 일정(2차 매체, TIKR): 차세대 위성 발사는 2027년 말 시작, 에코스타 주파수는 거래의 뒷단계가 끝나야(2027-11-30까지 예상) 상업적으로 쓸 수 있고, 위성 절반은 2032-10-07까지, 전부는 2035-10-07까지 올려야 한다 **[원문, 2차 매체 — FCC 명령 원문은 못 봄]**
- 8월 실적 발표에서 밝힌 목표: 상용 서비스 "내년 말"(2027년 말) — https://wirelessestimator.com/articles/2026/spacex-wants-to-be-a-fourth-major-network-but-its-building-around-towers-not-on-them/ **[원문, 2차 매체]**
- 에버코어: 5G 수준의 온전한 서비스는 2028년 상반기부터 가능하다고 봄(야후/TIKR 인용) **[원문, 2차 매체]**

**1-9. 같은 주에 있었던 FCC의 일.**
- 10-07(수): FCC가 스타링크 모바일 2세대 위성 1만5천 기를 승인. 지금 궤도의 모바일 위성은 약 650기(TIKR). 통신사에게서 주파수를 빌려야 한다는 규칙도 면제 → 통신사 없이 직접 팔 수 있다 **[원문, 2차 매체 TIKR·벤징가]**
- 10-07: FCC가 위성-휴대폰용 "prime spectrum" 25MHz 경매안을 표결에 부치겠다고 발표. 10-29에는 위성 보완 커버리지용 482MHz 추가 공급안의 의견 수렴 여부를 표결(CNBC) **[원문]**. 라이트리딩은 25MHz를 1675~1695MHz와 2020~2025MHz 대역이라고 적었다 **[원문]**
- FCC 위원장 브렌던 카(CNBC "Squawk on the Street", 10-09): "We're probably going to bring over $100 billion of spectrum into the market over the next two years, so we're seeing a lot of competition." / "There's going to be moves in the market. People are going to try to out-compete, out-innovate, and I think that's great. We're going to see how this plays out. It's not for us ultimately to pick winners and losers." / 경쟁은 "really good news for the American consumers" — https://www.cnbc.com/2026/10/09/verizon-att-tmobile-stocks-spacex-network.html **[원문]**. NBC는 "All of this is going to be really good news for the American consumer"로 적었다(단수) → 인용 표기 차이.

## 2. 이 주파수의 내력 (가장 조심할 곳)

| 때 | 일 | 출처·범위 |
|---|---|---|
| 2020 | 스프린트(그 전에는 넥스텔)의 800MHz가 합병으로 T모바일에 넘어옴. 법무부 합의로 디시가 약 35.9억 달러에 살 수 있는 옵션을 가짐 | **[검색요약]** 라이트리딩·RCR. satnews: "formerly comprised part of Sprint's legacy 800 MHz Specialized Mobile Radio (SMR) band" **[검색요약]** |
| 2023-10 | 디시가 기한 연장 대가로 1억 달러를 선지급, 기한 2024-04-01 | **[검색요약]** |
| 2024 | 디시가 사지 못함. T모바일은 경매에서 "조건에 맞는 입찰이 없었다"고 밝힘 | **[검색요약]** |
| 2025-02 | T모바일이 그레인의 600MHz 면허 26개를 1년 임차. 에어웨이브 리서치는 그 면허 값을 약 6억7520만 달러로 추정 | https://www.lightreading.com/5g/t-mobile-scratches-lowband-itch-with-grain-s-spectrum **[원문]** |
| 2025-03-20 | "T-Mobile Finalizing Sale of 800 MHz Spectrum Portfolio to ... Grain" 발표 | 비즈니스와이어 제목만 **[검색요약]**(403) |
| **2025-05-30** | **T모바일-그레인 계약 체결.** 800MHz를 넘기고 현금 29억 달러 + 그레인의 600MHz 면허를 받음 | T모바일 10-Q(2026-06-30) **[원문]** |
| 2026-07-01 | FCC 승인(800MHz 면허 조건 일부 수정, 그레인에게 경쟁 방식으로 쓸 곳을 찾게 하고 위성 직접통신 길을 조건부로 엶) | 10-Q **[원문]**, 그레인 보도자료 **[원문]**, 블룸버그 **[원문 앞부분]** |
| **2026-08-10~11** | **거래 종결.** T모바일 발표는 8-11 | 라이트리딩 전재(8-11) https://www.lightreading.com/5g/t-mobile-grain-complete-spectrum-swap **[원문]**. 클리어리 로펌은 8-10 종결이라고 함 **[검색요약]** → **날짜 차이: 8-10 대 8-11** |
| 2026-08-12 | 리콘 애널리틱스의 로저 엔트너가 X에 예고: "Grain is not a terminal buyer for the 800MHz it acquired from @TMobile. In my view, it ends up with @Starlink as the foundation of a terrestrial voice layer" | 라이트리딩 **[원문]** |
| 2026-08 | 블룸버그: 스페이스X와 AST가 이 주파수에 관심, 평가액 60억 달러 | **[원문 앞부분]** |
| **2026-10-08** | 그레인 → 스페이스X 계약. 보도된 값 약 80억 달러 | 1절 |

**T모바일 10-Q의 원문(2026-06-30 분기, 주석 6)** — https://www.sec.gov/Archives/edgar/data/1283699/000128369926000101/tmus-20260630.htm **[원문]**
> "On May 30, 2025, we entered into a License and Unit Purchase Agreement with NEWLEVEL IV, L.P. and NEWLEVEL, LLC, both of which are affiliates of Grain Management, LLC ("Grain"), pursuant to which we will sell our 800 MHz spectrum licenses in exchange for cash consideration of $2.9 billion and the receipt of Grain's 600 MHz spectrum licenses, which we are currently utilizing under lease agreements with Grain. **In addition, we may receive a share of certain future proceeds from transactions entered into by Grain that monetize the 800 MHz spectrum licenses, subject to certain terms and conditions and following a certain return on invested capital for Grain.** As of June 30, 2026, **$3.6 billion** of the associated 800 MHz spectrum licenses have been classified as held for sale at cost, with $2.9 billion and $690 million presented in Other current assets and Other assets, respectively ... we expect an increase to our cash income tax liability of approximately $850 million related to the close of this transaction."

**그래서 "29억에 판 것을 80억에 되팔았다"는 어디가 틀리나.**
1. 그레인이 낸 것은 현금 29억 달러 **+ 600MHz 면허 전부**다. T모바일은 이 800MHz를 장부에 36억 달러로 잡았고 그 가운데 6억9000만 달러가 받을 600MHz 몫이다(에어웨이브 추정 6억7520만 달러와 비슷). 그레인의 원가는 **약 36억 달러**로 보는 것이 맞다(600MHz의 그레인 쪽 취득가는 모름).
2. 값은 **2025-05-30**에 정해졌다(발표는 2025-03). "두 달"은 **종결(2026-08) 뒤 두 달**이라는 뜻으로만 맞다. 계약부터는 16개월.
3. T모바일은 그레인이 일정 수익률을 넘기면 **되판 돈의 일부를 받을 수 있다.** 비율과 기준은 공시에 없다. 이번 거래에서 받는지, 얼마인지 확인한 보도를 찾지 못했다.
4. 80억 달러는 WSJ 보도이지 확정 공시가 아니다.

**그레인의 차익(계산, 80억이 맞다는 가정).** 80억 − 36억 = **약 44억 달러, 2.2배**(T모바일 몫을 떼기 전, 세전). 현금 29억만 놓고 "2.8배"라고 하면 600MHz를 빠뜨린 숫자다 **[계산]**.

**야후의 "dumped" 제목.** 핀비즈의 관련 기사 목록에 "SpaceX snaps up the 800 MHz spectrum T-Mobile dumped for $2.9 billion and T-Mobile, Verizon, AT&T stocks are sliding"(머니와이즈)로 보인다 **[원문, 제목만]**. 본문은 403. 이 제목은 위 1~3을 빠뜨렸다.

**어긋나는 짝(대본 재료).** T모바일은 자기가 판 주파수가 자기 사업을 겨누는 데 쓰이게 됐다. 그런데 그 T모바일이 지금 스페이스X 위성으로 "T-Satellite"를 파는 스페이스X의 미국 출시 파트너다(3절). 그리고 되판 돈의 일부를 받을 수도 있다.

## 3. 스페이스X의 앞선 주파수 매입, T모바일과의 관계, 상장

**3-1. 에코스타.**
- 2025-09-08: 에코스타의 AWS-4·H블록을 약 170억 달러에 사기로 함(테크크런치 제목 "SpaceX strikes $17B deal to buy EchoStar's spectrum") **[검색요약]**, 레지스터 "SpaceX's $17 billion purchase of spectrum from satellite biz EchoStar last year" **[원문]**
- 뒤이은 26억 달러짜리 추가 거래(쿼츠: "a follow-on EchoStar deal worth $2.6 billion") **[원문]**. 합계 **65MHz, 196억 달러**(로이터를 인용한 와이어리스 에스티메이터·TIKR·야후) **[원문, 2차 매체]**
- **출처 간 차이:** "65MHz를 170억에"(검색요약의 여러 매체) 대 "두 거래 합계 196억"(로이터 인용 매체). 레지스터는 "50 MHz of exclusive S-band"라고 적었다. 대본에는 "약 170억 달러(뒤에 26억 추가)"가 안전하다.
- 2026-05-12: FCC(무선국·우주국)가 에코스타의 스페이스X·AT&T 매각을 승인. AT&T는 약 50MHz를 약 230억 달러에 **[검색요약]**. 스페이스X 몫의 거래는 아직 다 끝나지 않았다(위 1-8, 더데스크: "the AT&T and SpaceX transactions has not yet closed", 6월 말 기준) — https://thedesk.net/2026/06/dish-network-sling-tv-files-chapter-11-bankruptcy/ **[원문]**
- 이번 800MHz까지 합치면 스페이스X 약 **79MHz**, 3사는 각각 **280~380MHz**(에버코어, 야후/TIKR 인용) — https://finance.yahoo.com/markets/stocks/articles/verizon-stock-fell-10-day-155034414.html **[원문, 2차 매체]**. 14MHz는 한 통신사가 가진 것의 약 4~5% **[계산]**.

**3-2. T모바일과의 관계.**
- 2022년 T모바일과 스페이스X가 제휴 발표(NBC: "In 2022, T-Mobile announced a partnership with SpaceX, but recently dropped the name of the company from parts of its website") **[원문]**
- T모바일의 "T-Satellite"는 스타링크 위성으로 돌아간다. 작년 시작, 다른 통신사 고객에게도 월 15달러에 판다(레지스터) **[원문]**. 다른 안내 사이트는 월 10달러라고 함 **[검색요약]** → 가격 차이, 대본에 쓰려면 T모바일 가격표 확인.
- Teslarati: "T-Mobile is currently SpaceX's launch partner for Starlink Mobile in the US, which makes its position the most complicated of the three." **[원문]**
- CNBC: "T-Mobile has also previously removed mention of Starlink from its T-Satellite promotions." **[원문]**
- 지금 스페이스X의 위성-휴대폰 서비스는 통신사 주파수 약 5MHz를 빌려 쓴다(와이어리스 에스티메이터) **[원문, 2차 매체]**
- 독점 기간: T모바일 CEO가 2분기 실적 발표에서 "올해는 끝나지 않는다"고 했다는 보도와 "끝나 간다"는 보도가 엇갈린다 **[검색요약]**. 쓰지 말 것.

**3-3. 3사의 맞불: 위성 합작사.** 5-14에 원칙 합의, **10-01에 합작 계약 체결**(임시 CEO 폴 로스, 이름·출범일·지분 미공개). 스타링크는 빠져 있다.
- https://wirelessestimator.com/articles/2026/the-big-three-sign-satellite-dead-zone-jv-with-an-interim-ceo-a-shared-spectrum-pool-and-no-name-yet/ **[원문]**, 5월 합의 https://finance.yahoo.com/sectors/technology/articles/t-t-mobile-verizon-form-154658139.html **[원문]**
- CNBC는 "Last week ... formed a joint venture"라고 썼다. 10-01 계약을 가리킨다. 검색 요약 하나는 10-02라고 함 → 10-01(보도자료 날짜)로.

**3-4. 스페이스X의 상장.** 나스닥 **SPCX**, 2026-06-12 상장.
- 공모가 135달러, 약 5억5560만 주, 약 750억 달러 조달(사상 최대) **[검색요약]** + 와이어리스 에스티메이터 "record-breaking IPO ... opened at $135 and quickly peaked at $225.64 on June 16" **[원문]**(여기서 "opened at $135"는 공모가를 가리키는 표현으로 보인다. 첫날 시초가는 150달러라는 보도 **[검색요약]**)
- 첫날 종가 160.95달러(야후 데이터 **[원문 데이터]**). iposcoop은 161.11달러 **[검색요약]** → 차이.
- CNBC: "went public in June in a record IPO and is now valued at over $2 trillion" **[원문]**. NBC는 "Starlink ... was worth $2.2 trillion as of Friday"라고 썼는데 회사 전체 값으로 보인다(NBC의 표현이 부정확).
- 10-08 종가 160.57(-4.19%), 10-09 종가 162.57(**+1.25%**) **[원문 데이터 + 계산]**. CNBC "climbed about 2%", 로이터 "+2.2%"는 장중·시간외 숫자.
- 2분기(상장 뒤 첫 실적): 매출 78.1억 달러, 순손실 5.41억 달러, 설비투자 184억 달러(대부분 AI) — 와이어리스 에스티메이터 **[원문, 2차 매체]**. 스타링크 가입자 1200만(6-30), 통신 부문 매출 42.9억·영업이익 16.6억 달러(CNBC) **[원문]**. 도이체방크 추정 9월 말 1350만(미국 410만) **[원문, CNBC]**

## 4. 주가 (10-08 목, 10-09 금)

야후 차트 API 일별 종가 **[원문 데이터]**, 등락률은 **[계산]**. S&P 500: 10-08 7,765.36(-0.47%), 10-09 7,811.54(**+0.59%**). 시장이 오른 날 통신만 빠졌다.

| 종목 | 10-07 종가 | 10-08 종가(등락) | 10-09 종가 | 종가 대 종가 | 배당락 조정 | 10-09 저가 | 거래량(20일 평균 대비) |
|---|---|---|---|---|---|---|---|
| 버라이즌 VZ | 45.77 | 46.35 (+1.27%) | **41.65** | **-10.14%** | **-8.75%** | 40.81 | 9,507만 주(4.3배) |
| AT&T T | 24.47 | 24.87 (+1.63%) | **22.18** | **-10.82%** | **-9.81%** | 21.96 | 1억5,041만 주(3.9배) |
| T모바일 TMUS | 167.65 | 171.31 (+2.18%) | **148.58** | **-13.27%** | (배당락 아님) | 147.90 | 1,898만 주 |
| 크라운캐슬 CCI | 69.01 | 68.89 (-0.17%) | **79.64** | **+15.60%** | | 고가 79.79 | 1,439만 주 |
| 아메리칸타워 AMT | 166.18 | 166.73 (+0.33%) | **182.24** | **+9.30%** | | | 851만 주 |
| SBA SBAC | 170.38 | 170.01 (-0.22%) | **182.49** | **+7.34%** | | | 236만 주 |
| 스페이스X SPCX | 167.60 | 160.57 (-4.19%) | 162.57 | +1.25% | | | |
| AST ASTS | 60.65 | 56.93 (-6.13%) | 50.965 | **-10.48%** | | 47.57 | 5,412만 주 |
| 컴캐스트 CMCSA | 20.94 | 21.21 | 20.66 | -2.59% | | | |
| 차터 CHTR | 106.96 | 109.67 | 103.38 | -5.74% | | | |

**배당락.** 10-09는 버라이즌과 AT&T **둘 다** 배당락일이었다.
- 버라이즌: 분기 배당 70.75센트, "payable on November 2, 2026 to shareholders of record as of October 9, 2026" — https://www.verizon.com/about/news/verizon-q3-2026-earnings-report-date **[원문]**. 야후 배당 내역에 2026-10-09 0.708 **[원문 데이터]**.
- AT&T: 야후 배당 내역에 2026-10-09 0.278(분기 0.2775달러, 연 1.11달러) **[원문 데이터]**
- 계산: 버라이즌 (46.35 − 0.7075) = 45.6425 → 41.65/45.6425 − 1 = **-8.75%**. AT&T (24.87 − 0.2775) = 24.5925 → 22.18/24.5925 − 1 = **-9.81%**. CNBC의 숫자와 소수 둘째 자리까지 맞는다. 즉 **CNBC의 -8.75%, -9.81%는 배당을 뺀 숫자**이고, 화면의 종가끼리 견주면 -10.14%, -10.82%다.
- 버라이즌이 떨어진 4.70달러 가운데 0.71달러(15%)가 배당이다. 야후/TIKR도 같은 말: "Verizon closed at $41.65, down 10.14%. About $0.71 of the $4.70 decline reflects the 70.75-cent quarterly dividend, since October 9 was also the ex-dividend date." **[원문]**

**"~이후 최악의 날"** (CNBC 원문: "Verizon closed down 8.75% on the news, its worst day since July 2002. Shares of T-Mobile dropped 13.27% while AT&T fell 9.81%, each notching their own worst days since 2013 and 2000, respectively.")
- 버라이즌: 2002-07-22(-11.85%) 이후 가장 큰 하락. 두 기준 모두 맞다 **[계산]**. NBC도 "since 2002".
- AT&T: 종가 대 종가 -10.82%는 2000-12-19(-12.66%) 이후 최대 → "2000년 이후"가 맞다. 그러나 -9.81%로 말하면 2023-04-20(-10.41%)이 더 컸다 **[계산]**. 벤징가는 장중에 "largest one-day decline since April 20, 2023"이라고 썼다 **[원문]**. **"-9.81%, 2000년 이후 최악"처럼 두 기준을 섞으면 틀린다.** (2005년 이전 가격은 SBC 시절)
- T모바일: **출처 충돌.** CNBC "2013년 이후", NBC "2011년 이후". 야후 데이터에서 더 큰 하락은 2013-05-01(메트로PCS 합병일, 주식 병합이 낀 날)뿐이다 → CNBC 쪽이 데이터와 맞는다. 로이터: "its lowest level in over 33 months" **[원문]**. 데이터로는 종가 148.58이 **2023-11-28(148.38) 이후 최저**이고 52주 최저 종가다 **[계산]**.
- 버라이즌 종가는 2026-01-29 이후, AT&T 종가는 2026-07-20 이후 최저 **[계산]**.
- 크라운캐슬 +15.6%는 2008-11-24(+18.06%) 이후 가장 큰 상승 **[계산]**. 그 전 주에 52주 최저(10-01 종가 66.12)였다.

**3사가 잃은 시가총액(종가 기준, 계산).** 주식 수는 가장 최근 10-Q 표지(7월 중순~6월 말) 숫자다. 그 뒤 자사주 매입으로 조금 줄었을 것이라 실제는 약간 작다.

| | 주식 수 | 주당 하락 | 줄어든 값 | 그 가운데 배당 | 배당 뺀 값 | 10-09 시총 |
|---|---|---|---|---|---|---|
| 버라이즌 | 4,154,775,202 (6-30) | 4.70 | 195.3억 | 29.4억 | 165.9억 | 1,730억 |
| AT&T | 6,852,385,650 (7-16) | 2.69 | 184.3억 | 19.0억 | 165.3억 | 1,520억 |
| T모바일 | 1,072,671,613 (7-17) | 22.73 | 243.8억 | 0 | 243.8억 | 1,594억 |
| **합계** | | | **약 623억 달러** | 48.4억 | **약 575억 달러** | 4,844억 |

- 주식 수 출처: SEC XBRL companyfacts(dei:EntityCommonStockSharesOutstanding) **[원문]**
- **출처 충돌:** 벤징가 "about $39 billion ... when the stock market opened Friday morning"(개장 무렵) **[원문, 트레이딩뷰 전재]** / NBC "more than $50 billion in market value before lunch"(점심 전) **[원문]** / 종가 기준 계산 575억~623억. **390억은 종가 숫자가 아니다.** 대본에는 "하루에 약 570억 달러(배당 빼고)" 또는 "600억 달러 가까이"가 맞다. 보도된 인수가 80억의 약 7배.

**장중·시간외 숫자(섞지 말 것).** 목 시간외: AT&T -6.75%, T모바일 -5.4%, 버라이즌 -5%(야후), "약 7%"(스톡트윗), AT&T -3.6%·버라이즌 -3%·T모바일 -2.7%(쿼츠, 더 이른 시각). 금 오전: AT&T -6.44%, T모바일 약 -10%, 버라이즌 -5.7%(라이트리딩) / T모바일 -9.1%, AT&T -7.4%, 버라이즌 -5.9%(로이터) / T모바일 -9.5%, 버라이즌 -7.5%(셰퍼스). 오후 2시 30분: 버라이즌 -10.91%, AT&T -11.28%, T모바일 -12.81%(TIKR, 배당 미조정). 받은 메모의 "TMUS -9.54%"는 오전 숫자다.

**바다 건너.** 도이체텔레콤(T모바일 대주주) -7.1%, 오랑주 -1.8%, 텔레포니카 -3.3%, STOXX 600 통신 지수 -2.4%로 1-30 이후 최저. 캐나다 TSX 통신 지수 -4.5%(로이터) **[원문]**

## 5. 애널리스트의 말 (회사, 이름, 원문)

**통신사에 나쁘다 쪽**
- 에버코어 ISI, 쿠트군 마랄(Kutgun Maral): "The implications for AT&T, T-Mobile, and Verizon are somewhat negative: their defenses against low-band spectrum claims are weakening." (로이터) **[원문]** / "the clearest signal yet that Starlink Mobile is moving from a wholesale coverage layer for carrier partners toward a credible direct-to-consumer US service" / "[T]he window in which incumbents can treat Starlink Mobile as a science project is narrowing." (라이트리딩) **[원문]** / "The carriers' best argument just got weaker"(야후/TIKR) **[원문]** / 스페이스X가 "now has the outline of a real network"(CNBC) **[원문]**. 같은 사람이 14MHz는 "more of a coverage fix than a capacity solution"이라고도 했다.
- 스코샤뱅크, 마허 야기(Maher Yaghi): 목표가 인하. 버라이즌 51.50 → **50**(Outperform 유지), T모바일 217 → **212**(Outperform 유지), AT&T 27.50 → **26.50**(Sector Perform 유지). 스페이스X의 무선 야심이 "more credible"해졌지만 밀집 지역 서비스 능력과 망 구축의 경제성은 증명되지 않았다고 함 **[검색요약]**(스톡트윗 403). AT&T 26.50은 셰퍼스에서 확인 **[원문]**. 낮춘 폭은 2~4%로 주가 하락(9~13%)보다 훨씬 작다.
- 웰스파고, 스티븐 케이홀(Steven Cahall), **9월 8일** CNBC(이번 거래 전): "Telco just facing another competitor, a three player market going to a much smaller fourth player." "That's still a net negative for sure." — 247wallst **[요약도구]**. "처음엔 미국 인구의 약 2%를 겨냥할 수 있다"는 벤징가 한 곳에만 있다("He estimated it could initially target roughly 2% of the U.S. population") **[원문, 벤징가 전재]**. 직접 인용이 아니라 풀어 쓴 문장이고, 이번 거래에 대한 말이 아니다.
- 모건스탠리: "the Grain transaction is a clear sign that SpaceX is going to be a more aggressive acquirer of spectrum"(로이터를 옮긴 트레이더스 에이전시) **[원문, 3차]**. 위협은 농촌부터 서서히.
- 딥워터 진 먼스터: 스페이스X가 만든 전화기가 자기 망에서 통신사보다 싸게 나올 수 있다(벤징가) **[원문]**

**과민 반응이다 쪽**
- JP모건, 세바스티아노 페티(Sebastiano Petti): "SpaceX would likely need to build a terrestrial network using macro towers to deliver a user experience on par with traditional wireless carriers." / "we continue to see limited near-term risk to U.S. wireless incumbents given the time, infrastructure and capital required to build a competitive terrestrial network" (CNBC·NBC) **[원문]**. 이름은 트레이더스 에이전시가 CNBC를 인용해 적음 **[원문, 3차]**. 다음 표적으로 안테릭스의 900MHz(26억 달러 평가)를 꼽음.
- UBS: "We still believe it will take time for SpaceX to scale its wireless ambitions." (NBC) **[원문]**
- 모펫네이선슨, 크레이그 모펫: "SpaceX is still far from having the assets needed to offer a service that would be competitive with the services offered by the Big Three carriers." / "Starlink's only path to creating a viable competitor to the Big Three carriers would be to secure an MVNO agreement from one of the three of them." (라이트리딩) **[원문]**
- TD 코웬, 그레고리 윌리엄스: "SPCX may be bluffing to keep wireless down and get an [MVNO agreement], but needs to be taken seriously"(CNBC를 옮긴 트레이더스 에이전시) **[원문, 3차]**. 지상망 구축비 **800억 달러 이상**(야후/TIKR) **[원문, 2차]**. 10-05 발표 설문: 스타링크 모바일로 바꿀 생각이 있는 소비자 34% **[검색요약]**
- 뉴스트리트 리서치: 스페이스X는 저대역에서 3사에 "significantly lag". FCC 승인은 "fairly straightforward"(라이트리딩) **[원문]**
- TMF 어소시에이츠 팀 패러: "it's still a very limited amount of spectrum and to get reliable building penetration in urban areas SpaceX would have to deploy towers on the ground." (CNBC) **[원문]**
- 번스타인(8-31 노트, 더글러스 하네드 팀): 미국 독자망 구축비 **500억~1,300억 달러**(와이어리스 에스티메이터가 인베스팅닷컴을 인용) **[원문, 3차]**

**증권가 숫자(버라이즌).** 9-30 → 10-09 사이 투자의견 매수 8·아웃퍼폼 3·보유 15 → 8·2·16. 최고 목표가 71 → 62달러. **최저 목표가 44달러도 금요일 종가(41.65)보다 높다**(야후/TIKR) **[원문, 2차]**. AT&T: 29곳 가운데 18곳이 매수 이상, 매도 0, 평균 목표가 28.48달러(셰퍼스) **[원문]**.

## 6. "그래서 지금 살 만한가"에 댈 숫자

**6-1. 값(10-09 종가 기준).**

| | 버라이즌 | AT&T | T모바일 |
|---|---|---|---|
| 종가 | 41.65 | 22.18 | 148.58 |
| 연 배당 | 2.83(0.7075×4) | 1.11 | 4.08(1.02×4) |
| **배당수익률** [계산] | **6.79%** | **5.00%** | **2.75%** |
| 2026 조정 EPS 가이던스 | **4.99~5.04**(2분기에 상향, 두 분기 연속) | **2.25~2.35** | (EPS 가이던스 없음. 상반기 GAAP EPS 5.26) |
| **이익 대비 주가** [계산] | **8.3배**(중간값 5.015) | **9.6배**(중간값 2.30) | 약 14배(상반기 5.26을 두 배 한 어림) |
| 2026 잉여현금흐름 | 전년 대비 +9~10% | 180억 달러 이상 | 184억~188억 달러(상향) |
| 잉여현금흐름 수익률 [계산] | TIKR 13.8%(향후 12개월) | 약 11.8%(180억/1,520억) | 약 11.7%(186억/1,594억) |
| 순부채 | 1,287억(순무담보부채, EBITDA의 2.5배) | 1,264억 | 841억(타워 채무 제외) |
| 52주 최고가 종가 | 51.45(2026-09-15) → -19% | 29.10(2026-03-27) → -24% | 230.09(2025-10-20) → **-35%** |
| 올해 수익률(배당 포함) | **+9.1%** | -6.4% | **-25.6%** |
| 가입 | 무선 소매 회선 1억4,695만(후불 전화 9,410만) | 무선 소매 가입자 1억980만(후불 전화 7,492만) | 후불 계정 3,470만(회선 수는 2026년부터 공시 안 함) |
| 다음 실적 | **10-26(월)** 자료 07:00 ET = **KST 20:00**, 설명회 08:30 ET = KST 21:30 | **10-21(수)** 개장 전, 설명회 08:30 ET = **KST 21:30** | **10-28(수)** 자료 16:05 ET = **KST 10-29(목) 05:05**, 설명회 05:30 |

- 출처: 버라이즌 2분기 보도자료 https://www.verizon.com/about/news/verizon-delivers-record-2q26-results **[원문]**("Adjusted EPS of $4.99 to $5.04", "net unsecured debt ... $128.7 billion", "2.5 times"), 버라이즌 10-Q **[원문]**. AT&T 8-K 첨부 https://www.sec.gov/Archives/edgar/data/732717/000073271726000294/t-2q2026exhibit991.htm **[원문]**("Adjusted EPS of $2.25 to $2.35 in 2026", "Free cash flow of $18 billion+ in 2026", "net debt was $126.4 billion", "annualized common stock dividend of $1.11 per share"), AT&T 10-Q **[원문]**. T모바일 8-K 첨부 https://www.sec.gov/Archives/edgar/data/1283699/000128369926000100/tmus06302026ex991.htm **[원문]**, 팩트북("Net debt, excluding tower obligations ... $84.1 billion") **[원문]**. 실적 날짜: 버라이즌 사이트 **[원문]**, AT&T·T모바일 보도자료(핀비즈 전재) **[원문]**
- TIKR: 버라이즌 향후 12개월 P/E 9.02배(9-30) → 8.21배(10-09), AT&T 9.21배, 도이체텔레콤 10.24배 **[원문, 2차]**
- 시차: 10월은 미 동부 서머타임(UTC-4), 한국은 +13시간.
- 3분기 실적은 7~9월 치라 이번 거래의 영향이 숫자에 없다. 볼 것은 경영진의 말(가이던스 유지, 도매 계약에 대한 태도).

**6-2. 14MHz는 얼마나 되나.** 스페이스X 79MHz(에코스타 65 + 그레인 14) 대 3사 각 280~380MHz(에버코어) → 5분의 1~4분의 1. 14MHz만으로는 한 통신사의 약 4~5% **[계산]**. 3사는 10년 동안 약 1,100억 달러를 들여 미국 저대역을 거의 다 샀다(야후/비인크립토, 출처는 "that report") **[원문, 3차 — 약함]**.

**6-3. 전국 망을 짓는 값과 디시의 전례.**
- 추정 구축비: TD 코웬 800억 달러 이상, 번스타인 500억~1,300억 달러(5절).
- 디시(에코스타): 스프린트 합병 때 "네 번째 통신사"로 세워졌다. 부스트 가입자는 인수 때 약 940만 → 2026년 1분기 753만 **[검색요약]**. 5G망에 설비투자 100억 달러 예산, 망 관련 손상차손 164.8억 달러 **[검색요약]**. 2025-11-15에 자체 망의 통신을 AT&T 망으로 옮겼고 **[검색요약]**, 주파수는 AT&T와 스페이스X에 팔았다.
- 2026-06-30: 디시 DBS와 디시 와이어리스가 챕터 11 신청, 자체 5G망은 철거 중. "Dish Wireless, whose facilities-based 5G network is being decommissioned" — 더데스크 **[원문]**. 디시 와이어리스 채무 88억 달러 넘는 채권자가 동의.
- 타워 3사는 디시 와이어리스 파산 사건에서 임대료 약 **76억 달러**를 청구 중, 조정은 11-04까지(와이어리스 에스티메이터) **[원문, 2차]**
- 뜻: 주파수와 돈이 있던 네 번째 사업자가 6년 만에 망을 접었다. 다만 스페이스X는 디시와 다르다: 시총 2조 달러, 위성 1만 기 이상, 분기 설비투자 184억 달러. "디시처럼 실패한다"는 전례로 단정할 수 없다(작업자의 해석).

**6-4. 스페이스X가 스스로 한 말은 "타워를 빌린다"가 아니었다.** 8월 실적 발표에서 숏웰은 스타링크 접시와 같은 장비에 넣는 "these little femtocells"를 말했고, 덕분에 "10 or many billions of dollars"를 먼저 쓰지 않아도 된다고 했다. 머스크는 비싸고 자리 잡기 어려운 큰 기지국 대신 작은 기지국을 많이 깐다고 했다 — https://wirelessestimator.com/articles/2026/spacex-wants-to-be-a-fourth-major-network-but-its-building-around-towers-not-on-them/ **[원문, 2차]**. 반면 이번 FCC 서류는 "towers, rooftops and other structures"를 적었다(1-7). 타워주 급등은 "아직 임대 계약을 맺지 않은 세입자"에 건 것이다.

**6-5. 전례: 새 경쟁자 공포로 통신주가 빠진 날과 그 뒤.** 야후 일별 수정종가(배당 포함)로 계산 **[계산]**. 거래일 기준(+21일 ≈ 한 달, +42 ≈ 두 달, +63 ≈ 석 달), 사건일 종가 대비.

| 사건 | 당일 | +5일 | +21일 | +42일 | +63일 |
|---|---|---|---|---|---|
| **2025-09-08 스페이스X-에코스타 170억 달러 거래**(같은 종류의 공포) | VZ -2.4%, T -2.3%, TMUS -3.9% | +1.3, +2.5, -1.3 | -4.4, -9.5, -6.3 | **-6.8, -14.1, -15.7** | -2.1, -11.6, -13.3 |
| 2026-06-29~30(이틀, 원인 미확인. 스페이스X 상장 직후) | VZ -5.2/-4.0, T -4.0/-5.1, TMUS -4.8/-3.6 | | | | 7-16 대비 9-15: VZ +17%, T +22%, TMUS -6% |
| 2023-07-17 납 케이블 공포(경쟁자 공포는 아님, 큰 하루 하락의 전례) | VZ -7.5%, T -6.7% | +8.0, +10.5 | +5.7, +4.5 | +8.2, +11.3 | -0.4, +8.2 (126일 뒤 +29.7, +25.8) |
| 2025-04-25 T모바일 실적 실망 | TMUS -11.2% | +6.9 | +4.5 | -0.2 | +2.7 (126일 뒤 -5.8) |
| 2026-07-23 T모바일(2분기 실적일) | TMUS -10.7% | +1.7 | +7.4 | -4.2 | |

- 읽는 법: **가장 닮은 전례(2025-09 에코스타)에서는 반등하지 않고 두 달 더 빠졌다.** T모바일 -15.7%, AT&T -14.1%, 버라이즌 -6.8%. (그 사이 2025-10-06에도 버라이즌 -5.1%, AT&T -4.4%의 하락일이 있었다. 원인은 조사하지 않음.) 반면 사업과 무관한 공포였던 2023년 납 케이블 때는 한 주 만에 8~10% 되돌렸다.
- 그 밖에 받은 메모에 있던 사건: 2026-07 세마포의 "스페이스X가 주파수를 찾는다" 보도 때 통신주 -4%(야후/비인크립토) **[원문, 3차]**, 2026-08-04 숏웰 발언 뒤 시간외 -4% 넘게 **[검색요약]**, 스페이스X-차터 제휴 협의 보도(블룸버그) **[검색요약]**. 구글 파이(2015), 아마존-디시 소문은 이번에 숫자를 뽑지 않았다.
- 타워주의 전례: 2025-09-08에는 타워도 같이 빠졌다(CCI -2.4%, AMT -2.4%, SBAC -3.2%). 이번에는 반대로 올랐다. 5년 수익률은 AMT -30% 넘게, SBAC 약 -45%, CCI 약 -55%(CNBC를 옮긴 트레이더스 에이전시) **[원문, 3차]**

## 7. 사람

| 사람 | 직함 | 한 말(원문)·한 일 | 출처 | 사진 |
|---|---|---|---|---|
| 일론 머스크 | 스페이스X CEO | "This is the last critical piece of the spectrum puzzle needed for SpaceX to provide complete phone coverage in America" / "very big deal". **같은 날(10-08) 백악관 행사에서 트럼프에게 국가과학훈장을 받았다**(트럼프: "our modern-day Thomas Edison") | NBC·CNBC **[원문]**, Teslarati **[원문]**, NBC "Just this week, Trump gave Musk an award for achievements in science" | 10-08 훈장 사진(Teslarati 캡션: "Elon Musk holds the National Medal of Science alongside President Donald Trump ... October 8, 2026") |
| 그윈 숏웰 | 스페이스X 사장 겸 COO | 8월 실적 발표: "I anticipate us to be able to acquire quite a few of their customers because I think our service will be better" / 에코스타 주파수는 "does have terrestrial components, so we definitely intend to build out the terrestrial component" / 3사가 한 해 걷는 약 6,000억 달러를 시장으로 짚음 | Teslarati **[원문]**, 와이어리스 에스티메이터 **[원문]** | 흔함 |
| 댄 슐먼 | 버라이즌 CEO | 9-09 골드만삭스 커뮤나코피아: "I do not see it as a viable competitor in the medium and even longer term" / 위성은 "just can't compete without a terrestrial network in urban and suburban"(매출의 95~98%) / "no, 0, discernible impact" / "we see absolutely no advantage in extending an MVNO to any LEO provider nor are there any backdoors whatsoever to any of our existing MVNO relationships" | 야후/TIKR **[원문, 2차]** | 흔함 |
| 버라이즌(회사 성명) | | 10-09 NBC에: "Acquisition of spectrum alone does not provide the network or infrastructure to offer true nationwide coverage or to compete with mobile providers. A company can have billions of dollars of spectrum, but if they do not have the network to use it, it's just empty airwaves." | NBC **[원문]** | |
| 스리니 고팔란(Srinivasan Gopalan) | T모바일 사장 겸 CEO | 이번 거래에 대한 본인 발언은 못 찾음(X @SriniGopalan, 링크드인 확인 못 함). 5월 합작 발표 때 "deliver the best possible service to customers" | T모바일 8-K(7-07)에 직함 **[원문]**, 야후 **[원문]** | 흔함 |
| 존 소(John Saw) | T모바일 기술 총괄 사장 | 10-09 링크드인: "I have tremendous respect for what SpaceX has accomplished in space" / "You can acquire spectrum in a single transaction. You cannot acquire a nationwide, high-performing wireless network overnight." 망을 짓는 데 "years of engineering" | NBC **[원문]** | 링크드인 글 캡처 가능(확인 안 함) |
| 존 스탱키 | AT&T 회장 겸 CEO | 9-29 악시오스: 스페이스X 계획은 "not a viable strategy" / 집마다 기지국을 다는 안은 "It would cost as much to do that as it would to build a macro network" / "You can't radiate cellular signals from somebody's house without their permission." 7월: "they're coming to the game very late after this industry has been established." 9월 골드만 행사: 위성은 "solving the last 2%". 10-09 AT&T는 NBC의 논평 요청에 답하지 않음 | 와이어리스 에스티메이터 **[원문, 2차]**, 야후 **[원문]**, 쿼츠 **[원문]**, NBC **[원문]** | 흔함 |
| 데이비드 그레인 | 그레인 매니지먼트 창업자 겸 CEO(2007년 설립) | "For nearly twenty years, we have built Grain to see opportunity where others see complexity." / "This agreement with SpaceX brings that capability to bear at extraordinary scale, with the potential to change where and how Americans connect." / "Spectrum is a finite resource with an expanding role in the economy." 경력: 피너클 타워스(뒤의 글로벌 시그널)를 파산에서 상장까지 이끎, AT&T 브로드밴드 뉴잉글랜드 수석부사장, 모건스탠리 하이일드. 델·서던컴퍼니·뉴포트리스 이사 | 보도자료 **[원문]**, 회사 소개 https://graingp.com/team/david-grain/ **[요약도구]** | 회사 사이트에 있음(확인 안 함). 재산 추정은 믿을 만한 출처 없음 |
| 브렌던 카 | FCC 위원장 | 1-9의 인용. 승인권자 | CNBC **[원문]** | CNBC 방송 화면 |
| 로저 엔트너 | 리콘 애널리틱스 창업자 | 8-12에 "스타링크로 간다"고 예고(2절) | 라이트리딩 **[원문]** | |

**어긋나는 짝.** 슐먼이 "중장기에도 경쟁자가 못 된다"고 한 지 한 달 뒤, 버라이즌은 2002년 이후 가장 크게 빠졌다. 스탱키가 "실내를 못 뚫는다"고 한 지 열흘 뒤, 스페이스X는 벽을 뚫는 주파수를 샀다(@SawyerMerritt의 10-08 글이 이 대비를 그대로 씀: "AT&T CEO: Starlink Mobile won't be able to penetrate walls. SpaceX: We've acquired 800 MHz spectrum..." **[원문]** — 스탱키의 그 발언 원문은 직접 확인하지 못함).

## 8. 타워주는 왜 올랐나

- 논리: 800MHz 저대역은 "궤도에서는 쓰기 어렵고 타워에서는 쓰기 쉬운" 주파수다(큰 안테나가 필요). 스페이스X가 이것을 샀다는 것은 땅 위에 장비를 단다는 뜻이고, 그러면 타워 회사에 새 세입자가 생긴다. "위성 시대에 타워는 쓸모없어진다"는 걱정이 물러났다.
- 번스타인, 매디슨 레자이(Madison Rezaei): 이 거래는 "chips away at the 'towers are obsolete in a [direct to device] world' narrative, with which we have long vehemently disagreed" / "lends credibility to a potential new buyer of tower capacity, whether the eventual build is large scale or more selective" / "SPCX is keeping the terrestrial network build option very much alive"(CNBC를 옮긴 트레이더스 에이전시) **[원문, 3차 — CNBC 타워 기사 원문은 못 찾음]**. 핀비즈 목록에 "SpaceX's Wireless Ambitions Could Be A Windfall For CCI — Bernstein Analyst Calls It The Best Beneficiary" 제목 **[제목만]**
- 모건스탠리: 타워 회사에 "incrementally constructive"(로이터) **[원문]**. 골드만삭스: 그레인 주파수는 미국 타워에 긍정적(와이어리스 에스티메이터) **[원문, 2차]**
- 반론: 새 통신사가 3사의 가입자를 뺏으면 타워 회사의 가장 큰 고객 셋이 약해진다(3사 비중: SBA 미국 매출의 66%, 크라운캐슬 임대 매출의 약 75%, 아메리칸타워 미국·캐나다 부문의 약 86%). 디시도 "새 세입자"였다가 76억 달러의 미수 청구로 끝났다. 스페이스X는 8월에 큰 타워를 피하겠다고 했다(6-4). — 와이어리스 에스티메이터 https://wirelessestimator.com/articles/2026/spacexs-8-billion-800-mhz-buy-sends-crown-castle-american-tower-and-sba-shares-soaring-on-a-tenant-that-hasnt-signed-a-lease/ **[원문]**
- 크라운캐슬이 가장 크게 오른 까닭: 가장 많이 빠져 있었다(10-05 52주 최저 65.65, 올해 약 -22%), 미국 타워만 한다, 디시 청구액이 가장 크다(같은 기사) **[원문, 2차]**

## 9. 10-10(토)~10-11(일)

- 이 거래에 대한 새 사실(가격 확인, T모바일의 몫, FCC 일정, 통신사 경영진의 새 발언)은 **찾지 못했다.** 찾아본 곳: 웹 검색 세 번(주말 날짜, 머스크 인터뷰, T모바일 반응), SEC 공시 목록(T모바일·AT&T·버라이즌 10-09 이후 8-K 없음, 10-11 조회).
- 10-10(토): 머스크가 기가 텍사스의 "X Takeover"에서 화상 인터뷰를 하기로 돼 있었다(Teslarati 예고) **[원문]**. 스타링크 모바일에 대해 무슨 말을 했는지는 확인하지 못했다.
- 10-10자 2차 기사(주가 해설)만 있음. 다음 거래일은 10-12(월).

## 10. 대본을 쓸 때 틀리기 쉬운 것

1. **"버라이즌 -8.75%"와 "41.65달러"를 같이 쓰면서 전날 46.35달러를 보여 주는 것.** 화면의 두 종가로는 -10.14%다. -8.75%는 배당 0.7075달러를 뺀 숫자. 하나만 골라 쓰고, 고른 기준을 지킨다. AT&T도 같다(-9.81% 대 -10.82%).
2. **"AT&T 2000년 이후 최악"을 -9.81%와 함께 쓰는 것.** 그 기준이면 2023-04-20이 더 나빴다.
3. **"T모바일 2011년 이후 최악"**(NBC) 대 "2013년 이후"(CNBC). 데이터는 2013 쪽. 안전한 말은 "T모바일 주가는 2023년 11월 이후 가장 낮다".
4. **"시총 390억 달러 증발."** 개장 무렵 숫자다. 종가로는 약 570억~620억 달러.
5. **"80억 달러에 샀다"를 확정처럼 말하는 것.** WSJ 보도다. "약 80억 달러로 알려졌다".
6. **"T모바일이 29억에 판 걸 두 달 만에 80억에."** 그레인의 원가는 약 36억(현금 29억 + 600MHz), 값은 2025년 5월에 정해졌고, T모바일은 차익의 일부를 받을 수 있다. "T모바일이 헐값에 버렸다"는 확인되지 않는다.
7. **"스페이스X가 통신사가 됐다 / 서비스를 시작한다."** FCC 승인 전이고 개시 시점도 밝히지 않았다. 위성은 2027년 말부터 쏜다.
8. **"위성으로 실내까지 터진다."** 800MHz는 위성이 아니라 땅 위의 안테나로 쓸 가능성이 크다(피에식, 스페이스X의 FCC 서류). "벽을 뚫는 주파수"는 맞지만 "위성 신호가 벽을 뚫는다"는 아니다.
9. **"스페이스X가 타워를 빌린다"를 사실처럼.** 계약 없음. 8월에는 작은 기지국을 말했다.
10. **"14MHz"의 크기를 빼고 "마지막 퍼즐"만 전하는 것.** 3사는 각각 280~380MHz. 머스크의 말은 머스크의 말로.
11. **웰스파고 "미국 인구 2%"**를 이번 거래에 대한 분석처럼 쓰는 것. 9월 발언이고 벤징가의 풀어 쓴 문장 하나뿐.
12. **"스페이스X 주가 급등."** 금요일 +1.25%, 전날 -4.19%. 이틀 합치면 내렸다.
13. **"에코스타 170억"과 "196억"**, **65MHz와 50MHz**가 매체마다 다르다.
14. **"3사 합작사를 지난주에 세웠다."** 5월 원칙 합의, 10-01 계약. 아직 이름도 출범일도 없다.
15. **"T-Satellite 월 10달러/15달러"**, **독점 종료 시점**은 출처가 엇갈린다.
16. 스페이스X 상장 첫날 종가 160.95 대 161.11.

## 11. 판단: 급락 뒤 버라이즌·AT&T·T모바일은 살 만한가 (작업자의 해석)

**결론 한 문단.** 금요일의 급락은 "당장 이익이 줄어서"가 아니라 "3사 과점이 깨질 수 있다"는 값 매김이다. 이익이 실제로 다치는 때는 빨라야 2028년이고(위성 발사 2027년 말, 에버코어의 5G 수준 2028년 상반기, 구축비 500억~1,300억 달러), 그 전까지 버라이즌은 이익의 8.3배에 배당 6.8%, AT&T는 9.6배에 5.0%를 준다. 그래서 **"싸다"는 숫자로 맞다.** 그러나 **"급락했으니 바로 반등한다"는 전례가 받쳐 주지 않는다.** 가장 닮은 전례(2025-09 에코스타 거래)에서 3사는 두 달 동안 7~16% 더 빠졌고, 스페이스X는 2025-09, 2026-06, 2026-08, 2026-10에 한 걸음씩 나올 때마다 통신주를 눌렀다. 다음 걸음(10-29 FCC 표결, 주파수 경매, 추가 매입, 요금 발표)도 예정돼 있다. 셋 가운데 고르라면 **버라이즌**이다: 가장 싸고(8.3배), 배당이 가장 크고(6.79%), 올해 가이던스를 두 번 올렸고, 떨어진 폭의 15%는 배당이며, 증권가의 가장 낮은 목표가(44달러)가 지금 주가보다 높다. **T모바일은 가장 조심할 쪽**이다: 배당이 2.75%라 기다리는 값이 작고, 성장 프리미엄이 깎이는 중이며(52주 최고 대비 -35%, 2023-11 이후 최저), 스페이스X의 협력자에서 경쟁자로 자리가 바뀌는 당사자다. 다만 잉여현금흐름 수익률은 이제 11.7%로 AT&T와 같아졌고, 그레인 차익의 일부를 받을 수 있는 유일한 회사다.

**받치는 숫자.** 버라이즌 P/E 8.3배(9-30의 9.0배에서), 배당 6.79%, 순부채 EBITDA 2.5배, 2026 조정 EPS 4.99~5.04(+6~7%), 후불 전화 순증 2분기 18.4만. 스페이스X 79MHz 대 3사 280~380MHz. JP모건 "limited near-term risk", 모펫 "still far". 2023-07 급락 뒤 126거래일 +26~30%.

**거스르는 숫자.** 2025-09-08 뒤 42거래일: 버라이즌 -6.8%, AT&T -14.1%, T모바일 -15.7%. FCC 위원장이 "2년 안에 1,000억 달러 넘는 주파수"를 풀겠다고 했고 승인은 "fairly straightforward"로 예상된다. 에버코어 "The carriers' best argument just got weaker". 스페이스X는 분기에 184억 달러를 설비에 쓰는 회사다. 3사 가운데 하나가 스페이스X에 망을 빌려주면(MVNO) 나머지 둘이 더 다친다(모펫의 시나리오). 버라이즌의 순부채 1,287억, AT&T 1,264억 달러는 요금 경쟁이 붙으면 배당의 여유를 줄인다.

**틀렸다고 볼 값과 날짜.**
- 버라이즌: **10-26 실적에서 조정 EPS 4.99~5.04 가이던스를 낮추거나**, 슐먼이 "위성 사업자에게 MVNO를 줄 이유가 없다"는 말을 누그러뜨리거나, 종가가 **금요일 저가 40.81달러 아래**로 내려가 실적 뒤에도 못 올라오면 "싸니까 버틴다"는 판단은 틀린 것이다. 반대로 2026년 말까지 배당락 조정 전 종가 45.64달러(금요일 낙폭의 시작점)를 되찾으면 과민 반응이었다는 쪽이 맞다.
- AT&T: 10-21 실적에서 "2026 잉여현금흐름 180억 달러 이상"과 연 배당 1.11달러 유지가 깨지면 틀림. 가격으로는 7-01 종가 20.48달러(52주 최저) 이탈.
- T모바일: 10-28(한국 10-29 새벽) 실적에서 후불 계정 순증 95만~105만 가이던스가 내려가거나, 그레인 거래에서 받을 몫이 없다고 밝혀지면 더 나쁨. 반대로 몫의 크기가 공개되면 뜻밖의 호재.
- 셋 모두: **10-29 FCC 표결**과 그레인 거래의 FCC 승인 시점, 스페이스X의 요금·출시일 발표가 다음 고비.

**답이 물러선 말이 되지 않게.** "지금 3사를 다 사라"도 "다 팔아라"도 숫자가 받치지 않는다. 받치는 말은 이것이다: **"배당을 받으며 2028년까지 기다릴 사람에게 버라이즌은 싸다. 다음 달 반등을 노리는 사람에게는 전례가 나쁘다."**

## 12. 화면에 쓸 실물이 있는 곳

- 그레인 보도자료(PR뉴스와이어), 스페이스X 공식 X 글과 머스크의 X 글(캡처 필요, 직접 열지 못함), @SawyerMerritt 글.
- T모바일 10-Q 주석 6의 문단("we may receive a share of certain future proceeds") — SEC 원문 화면.
- CNBC 기사 제목 "Verizon posts worst day since 2002 as SpaceX U.S. network plans whack cell provider stocks", NBC 제목 "Elon Musk's growing SpaceX empire sends AT&T, Verizon and T-Mobile shares plunging".
- CNBC "Squawk on the Street"의 브렌던 카 인터뷰(10-09), 존 소의 링크드인 글, 버라이즌 성명.
- 10-08 백악관 과학 행사의 머스크와 트럼프(국가과학훈장).
- 실제 주가 데이터: 야후 차트 API의 일봉(위 표). 10-09의 거래량 4배 막대.
- 스페이스X 사진: CNBC 캡션 "A worker installs fencing at the SpaceX facility in Hawthorne on the day of the company's IPO, in Hawthorne, California, June 12, 2026."

## 13. 확인하지 못한 것 (게시 전에 원문으로 볼 목록)

1. **WSJ 원문**(80억 달러, 현금 여부, 소식통 표현). 로이터·라이트리딩의 재인용만 봄.
2. **스페이스X 성명 원문**(spacex.com/updates)과 **머스크·스페이스X의 X 글 원문.** 매체 인용만 봄.
3. **T모바일이 이번 거래에서 받는 몫**(비율, 기준 수익률, 금액). 공시에 없고 보도도 못 찾음. T모바일의 8-11 종결 보도자료(403)와 10-28 실적에서 확인할 것.
4. 그레인의 600MHz 취득 원가, 그레인의 실제 차익.
5. FCC 문서 원문: 7-01 그레인 승인 명령(구축 기준, 경쟁 선정 절차), 10-07 2세대 위성 승인, 스페이스X의 공익 진술서, 10-29 회의 안건.
6. 스코샤뱅크 목표가 변경(검색 요약 + 셰퍼스의 AT&T 한 줄만 원문), 번스타인 레자이·JP모건 페티의 이름과 문장(CNBC 타워 기사 원문 못 찾음, 3차 인용), 웰스파고 "2%"(벤징가 한 곳).
7. 디시의 총투자액과 가입자 숫자(검색 요약), 디시 옵션의 내력(검색 요약).
8. 에코스타 거래의 정확한 금액 구성(170억 + 26억)과 MHz(65 대 50), 종결 상태.
9. T-Satellite의 가격·가입자 수·독점 기간.
10. 2026-06-29~30, 2025-10-06 통신주 급락의 원인(가격만 계산).
11. 주말(10-10~11)의 새 발언. 머스크의 10-10 인터뷰 내용.
12. T모바일 CEO 고팔란의 이번 거래에 대한 발언, AT&T의 공식 반응.
13. 시가총액 계산의 주식 수는 7월 공시 기준(그 뒤 자사주 매입 미반영).
14. 3사의 주파수 보유량(280~380MHz)과 "10년간 1,100억 달러"는 2차·3차 인용.
15. 스탱키의 "실내를 못 뚫는다" 발언 원문(메리트의 요약만 봄).
