# 폭스바겐 숏 스퀴즈(2008-10) 조사의 가격 자료와 원문

받은 날: 2026-10-13. 전부 실제로 내려받은 파일이다. 손으로 고친 값은 없다(아래 "깨진 하루"만 계산 때 보도 값으로 바꿨고, CSV에는 야후 값을 그대로 뒀다).

## 원자료 (`raw/`)

| 파일 | 어디서 | 무엇 | 수정 여부 |
|---|---|---|---|
| `yahoo_VOW.DE.json` | `https://query2.finance.yahoo.com/v8/finance/chart/VOW.DE?period1=1104537600&period2=1791936000&interval=1d&events=div%2Csplit` (User-Agent를 `Mozilla/5.0`으로 줘야 한다. curl 기본값은 429) | 폭스바겐 **보통주** Xetra 일봉, 2005-01-03 ~ 2026-10-09 | 분할 기록 없음. `close`는 배당을 반영하지 않은 실제 거래가, `adjclose`는 배당을 재투자한 것으로 친 값(2008년 값이 종가의 0.51배쯤). **2008-10-28 줄이 깨져 있다**(아래) |
| `yahoo_VOW3.DE.json` | 같은 주소, `VOW3.DE` | 폭스바겐 **우선주** | 분할 없음 |
| `yahoo_VOW.SG.json`, `yahoo_VOW.MU.json`, `yahoo_VOW.F.json` | 같은 주소 | 보통주의 슈투트가르트, 뮌헨, 프랑크푸르트 거래소 계열 | Xetra의 깨진 하루를 대조하려고 받았다. `VOW.F`는 야후가 0.989배쯤 조정한 값이라 절대값은 쓰지 않는다 |
| `yahoo_VWAGY.json` | 같은 주소 | 미국 장외 ADR(달러) | 대조용 |
| `yahoo_PAH3.DE.json` | 같은 주소 | 포르쉐 SE 우선주 Xetra | 2009-01-28부터만 있다. 2008-10은 없다 |
| `yahoo_PAH3.SG.json` | 같은 주소 | 포르쉐 SE 우선주 슈투트가르트 | 2008-10이 있다. 뒤의 증자(2011)가 반영된 조정값일 수 있어 **등락률만** 쓴다 |
| `yahoo_GDAXI.json` | 같은 주소, `%5EGDAXI` | DAX 지수(배당 포함 지수) | |
| `yahoo_GME.json` | 같은 주소 | 게임스톱 | `close`는 2022-07-22의 4대1 분할 반영. ×4가 2021년의 실제 거래가 |
| `yahoo_XOM.json` | 같은 주소 | 엑슨모빌 | |
| `yahoo_086520.KQ.json` | 같은 주소 | 에코프로(야후) | 네이버 값 대조용 |
| `naver_086520.txt`, `naver_247540.txt` | `https://api.finance.naver.com/siseJson.naver?symbol=<코드>&requestType=1&startTime=20230101&endTime=20261013&timeframe=day` | 에코프로, 에코프로비엠 일봉 | 수정주가다. 2024-04-25의 1대5 액면분할과 2025-02의 2% 주식배당이 반영돼 있어 **×5.1**이 2023년의 실제 거래가에 가깝다(보도된 2023-07-18 종가 1,118,000원, 07-25 1,293,000원, 07-26 1,228,000원과 맞는다) |

받으려다 못 받은 곳: stooq(`https://stooq.com/q/d/l/?s=vow.de&i=d`)는 자바스크립트 확인 화면만 돌려줬다. ariva.de의 CSV는 로그인으로 넘어갔다.

### 깨진 하루: 야후 Xetra 계열의 2008-10-28

야후의 `VOW.DE` 2008-10-28 줄은 시가 500.00, 고가 500.00, 저가 471.00, 종가 500.00이다. 같은 날 슈투트가르트는 고가 981.44, 종가 886.00, 뮌헨은 고가 945.00, 종가 879.00, 미국 ADR은 59.00달러에서 109.75달러로 올랐다. 당시 보도의 Xetra 값은 **장중 최고 1,005.01유로**(Bloomberg 2008-10-28), **종가 945유로**(GoAuto 2008-11-04, df.cl 2008-10-29, Law360의 "82% 상승")다.

`compute.py`는 이 하루만 고가 1,005.01, 종가 945.00으로 바꿔 계산하고, 표에 "(보도 값)"이라고 적는다. `VOW_DE.csv`에는 야후 값(500.00)이 그대로 있으니 **그 CSV로 차트를 그릴 때는 2008-10-28을 고쳐야 한다**. 10-27(종가 520.00, 장중 635.00)과 10-29(종가 517.00)는 야후 값이 다른 거래소 계열, 보도와 맞는다.

Xetra의 공식 일봉 원본(도이체 뵈르제)은 받지 못했다. 945.00과 1,005.01은 보도에서 온 값이다.

## 원문 (`sources/`)

회사와 거래소가 낸 문서만 둔다(기사 본문은 저장하지 않았다. 주소와 인용은 `facts.md`).

| 파일 | 무엇 | 주소 |
|---|---|---|
| `pr_20080303_de.pdf` | 포르쉐 SE 보도자료 2008-03-03: 감독이사회가 50% 초과를 승인 | `https://www.porsche-se.com/medien/pressemitteilungen/pdf/porsche-aufsichtsrat-gibt-gruenes-licht-fuer-mehrheitsbeteiligung-an-vw` |
| `pr_20080310_de.pdf`, `pr_20080310_en.txt` | 2008-03-10: 75% 보도 부인 | `.../pdf/porsche-weist-spekulationen-ueber-aufstockung-auf-75-prozent-bei-vw-zurueck`, 영문 `https://porsche-se.com/en/media/press-releases/detail/porsche-denies-speculations-about-increasing-its-stake-in-vw-to-75-percent-1` |
| `pr_20081026_de.pdf`, `pr_20081026_en.pdf` | 2008-10-26: 42.6% + 31.5% = 74.1% 공개 | `.../pdf/porsche-strebt-beherrschungsvertrag-an`, 영문 `https://www.porsche-se.com/en/media/press-releases/pdf/porsche-heads-for-domination-agreement-1` |
| `pr_20081029_de.pdf` | 2008-10-29: 옵션 최대 5% 풀겠다 | `.../pdf/kursturbulenzen-bei-vw-stammaktien-von-leerverkaeufern-zu-verantworten` |
| `pr_fy0708b_de.pdf`, `pr_fy0708_de.pdf` | 2008-11-17, 11-26: 2007/08 회계연도 실적 | `.../pdf/porsche-konzernergebnis-erneut-deutlich-gestiegen`, `.../pdf/porsche-erzielt-rekorde-bei-gewinn-umsatz-und-absatz` |
| `interim_0809.pdf` | 2008/09 첫 넉 달 중간보고서(영문) | `https://www.porsche-se.com/fileadmin/downloads/investorrelations/mandatorypublications/interimreport/Interim_report_-_Report_on_the_first_four_months_of_the_financial_year_200809.pdf` |
| `pse_hj2009_de.pdf` | 2009-01-31 반기보고서(독문) | `.../report-1-2009/Halbjahresfinanzbericht_zum_31_Januar_2009.pdf` |
| `pr_20090723_en.pdf` | 2009-07-23: 비데킹과 해르터 퇴임 | `https://www.porsche-se.com/en/media/press-releases/pdf/macht-appointed-chairman-of-the-board-of-management-for-porsche-ag-edig-his-deputy-both-also-me-1` |
| `pr_fy0809_de.pdf` | 2009-11-12: 2008/09 세전 −44억 유로 | `.../pdf/porsche-konzernergebnis-durch-sondereinfluesse-gepraegt` |
| `pr_2012_en.pdf` | 2012-07-04: 포르쉐 AG 나머지를 폭스바겐에 | `https://www.porsche-se.com/en/media/press-releases/pdf/porsche-se-and-volkswagen-ag-create-integrated-automotive-group-1` |
| `pr_2013_withdraw.pdf` | 2013-03-06: 미국 소송 현황 | `.../pdf/several-hedge-funds-withdraw-appeals-in-the-proceeding-before-the-us-court-of-appeals-for-the-seco-1` |
| `pse_hj2026.pdf` | 포르쉐 SE 2026년 반기보고서 | `https://www.porsche-se.com/fileadmin/downloads/investorrelations/mandatorypublications/report-1-2009/PSE_HJ2026_E.pdf` |
| `dboerse_20081028.txt` | 도이체 뵈르제 보도자료 2008-10-28: DAX 비중 27%, 10%로 제한 | `https://www.deutsche-boerse.com/dbg-en/investor-relations/announcements-and-services/press-releases/Deutsche-B-rse-Extraordinarily-Adjusts-DAX-Weightings-438008` |

## 만든 파일

- `compute.py` → `VOW_DE.csv`, `VOW3_DE.csv`, `VOW_SG.csv`, `VOW_MU.csv`, `VOW_F.csv`, `VWAGY.csv`, `PAH3_DE.csv`, `PAH3_SG.csv`, `GDAXI.csv`, `GME.csv`, `XOM.csv`, `086520_KQ.csv`, `kr_086520.csv`, `kr_247540.csv`, `computed.md`

다시 돌리기(`research/vw-short-squeeze-2008/`에서):

```
python3 -I data/compute.py data/raw data
```

## 읽을 때 조심할 것

- 폭스바겐 보통주의 마지막 날은 2026-10-09(종가 68.45)다. 10-12 줄은 야후에 종가가 비어 있었다.
- 시가총액 어림에 쓴 보통주 수 294,920,207주는 작업자의 기억이고 연차보고서로 확인하지 못했다. 다만 1,005.01유로를 곱하면 2,964억 유로가 나와 Bloomberg가 쓴 2,960억 유로와 맞는다.
- DAX는 배당을 포함한 지수다. 폭스바겐의 "가격만" 수익률과 나란히 놓으면 폭스바겐이 불리하게 보인다. 배당 재투자 값을 같이 적었다.
- 에코프로 표의 "×5.1"은 2023년 값에만 뜻이 있다. 2024-04-25 뒤의 줄은 "종가(분할 반영)" 열이 실제 거래가다(2025-02의 2% 주식배당 전은 1.02배).
