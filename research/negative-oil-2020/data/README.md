# 마이너스 유가 조사의 가격 자료

받은 날: 2026-10-11. 전부 실제로 내려받은 파일이다. 손으로 고친 값은 없다.

## 원자료 (`raw/`)

| 파일 | 어디서 | 무엇 | 수정 여부 |
|---|---|---|---|
| `yahoo_CL=F.json` | `https://query2.finance.yahoo.com/v8/finance/chart/CL=F?period1=1575158400&period2=1791676800&interval=1d&events=div,split` | WTI 근월물 연속 선물 일봉 | 근월물을 이어 붙인 계열. 2020-04-20 종가 −37.63, 04-21 10.01(둘 다 5월물), 04-22부터 6월물. EIA RCLC1과 2020년 값이 일치 |
| `yahoo_BZ=F.json` | 같은 주소, `BZ=F` | 브렌트 근월물 | |
| `yahoo_USO.json` | 같은 주소, `USO` | USO 일봉 | `close`는 2020-04-29의 1대8 병합이 반영된 값(병합 전 실제 거래가는 이 값의 1/8). 배당 없음 |
| `yahoo_XLE.json` | 같은 주소, `XLE` | XLE 일봉 | `close`는 2025-12-05의 2대1 분할 반영. `adjclose`는 배당을 재투자한 것으로 친 값 |
| `yahoo_XOP.json`, `yahoo_BNO.json` | 같은 주소 | XOP, BNO | XOP는 2020-03-30 1대4 병합 반영 |
| `yahoo_CL{X26,Z26,F27,H27,M27,Z27,Z28}.NYM.json` | `https://query2.finance.yahoo.com/v8/finance/chart/CLZ26.NYM?range=1mo&interval=1d` | 지금의 WTI 월물별 종가(선물 곡선) | |
| `naver_<종목코드>.txt` | `https://api.finance.naver.com/siseJson.naver?symbol=<코드>&requestType=1&startTime=20191201&endTime=20261011&timeframe=day` | 한국 상장 ETF/ETN 일봉(날짜, 시가, 고가, 저가, 종가, 거래량) | 아래 "한국 계열의 수정 여부" |
| `eia_RCLC1d.xls`, `eia_RCLC2d.xls` | `https://www.eia.gov/dnav/pet/hist_xls/RCLC1d.xls`, `RCLC2d.xls` | EIA: 쿠싱 WTI 선물 1번·2번 계약 일별 정산가 | 1번 계약은 2024-04-05에서 끝난다(EIA가 갱신을 멈춤) |
| `eia_RWTCd.xls`, `eia_RBRTEd.xls` | 같은 곳, `RWTCd.xls`, `RBRTEd.xls` | EIA: WTI 쿠싱 현물, 브렌트 현물 | 2026-10-06까지 |
| `eia_cushing_stocks_weekly.xls` | `https://www.eia.gov/dnav/pet/hist_xls/W_EPC0_SAX_YCUOK_MBBLw.xls` | EIA: 쿠싱 주간 원유 재고(천 배럴) | 2026-10-02까지 |

한국 종목코드: 261220 KODEX WTI원유선물(H), 130680 TIGER 원유선물Enhanced(H), 530031 삼성 레버리지 WTI원유 선물 ETN, 500019 신한 레버리지 WTI원유 선물 ETN(H), 520009 미래에셋 레버리지 원유선물혼합 ETN(H), 550042 QV 레버리지 WTI원유 선물 ETN(H), 218420 KODEX 미국S&P에너지(합성), 219390 RISE(옛 KBSTAR) 미국S&P원유생산기업(합성 H), 271050 KODEX WTI원유선물인버스(H), 217770 TIGER 원유선물인버스(H).

### 한국 계열의 수정 여부

- 네이버 응답에는 수정주가인지 표시가 없다. 대신 `compute.py`가 하루 변동이 +60%를 넘거나 −45% 밑인 날, 10일 넘게 거래가 빈 날을 찾았다. 나온 것은 2020-04-27의 레버리지 ETN 세 종목(−52~−60%, 거래정지가 풀린 날의 하한가)과 2026-03-09의 520009(+60%, 상한가)뿐이다. 병합이나 분할의 흔적(값이 몇 배로 뛰는 날)은 열 종목 어디에도 없다. 즉 이 기간에 병합·분할이 없었거나 네이버가 이미 반영한 값이다. 어느 쪽이든 수익률 계산은 그대로 맞다.
- 500019는 2026-02-25, 520009는 2026-04-09, 550042는 2022-07-27에서 자료가 끝난다(상장폐지 또는 만기. 까닭은 `facts.md`).
- 2020년 4월의 레버리지 ETN 시장가는 실제 가치(지표가치)보다 훨씬 비쌌다(괴리율). 그래서 "2020-03-31이나 04-21에 샀다면"의 ETN 줄은 시장가 기준이고, 그때 산 값에 웃돈이 들어 있다.
- 한국 장은 미국 장보다 먼저 닫는다. 한국 상품의 "2020-04-20" 값에는 그날 밤의 마이너스 유가가 아직 들어 있지 않다. 04-21 값부터 들어간다.
- (H)는 환헤지, 530031은 환노출이다. 218420도 환노출이라 원/달러 환율 변화가 섞여 있다.

## 만든 파일

- `compute.py` → `CL_F.csv`, `BZ_F.csv`, `USO.csv`, `BNO.csv`, `XLE.csv`, `XOP.csv`, `kr_<코드>.csv`, `eia_RCLC1d.csv`, `eia_RWTCd.csv`, `comparison.md`
- `extra.py` → `extra.md` (원금 회복일, 시점별 수익률, 구간별 유가와 ETF의 차이, 2026년 유가, 지금의 선물 곡선, 2020-04의 5월물·6월물, 쿠싱 재고)

다시 돌리기(프로젝트 루트의 `research/negative-oil-2020/`에서. EIA xls를 읽으려면 `xlrd`가 필요해 임시 가상환경을 썼다):

```
python3 -m venv /tmp/xlvenv && /tmp/xlvenv/bin/pip install xlrd
/tmp/xlvenv/bin/python -I data/compute.py data/raw data
/tmp/xlvenv/bin/python -I data/extra.py data/raw data
```

## 계산한 방법

- 수익률 = (나중 날 종가 ÷ 산 날 종가 − 1) × 100. 산 날이 휴장이면 그다음 거래일 종가를 쓴다(표에 날짜를 괄호로 적는다).
- "마지막"은 각 자료의 마지막 거래일이다: 미국 2026-10-09, 한국 2026-10-08.
- 유가가 음수인 날(2020-04-20)에 "샀다면"은 계산하지 않는다. 그래서 04-21(5월물 마지막 날, 10.01달러)을 썼다. 이 값은 만기 하루 전의 5월물이라 실제로 ETF가 들고 있던 값이 아니다. 같은 날 6월물은 11.57달러였다(`extra.md`).
- XLE는 가격만 본 것과 배당을 재투자한 것(Yahoo `adjclose`) 둘 다 냈다. USO와 한국 원유선물 ETF는 분배금이 없어 가격이 곧 수익이다.
- 예: "2020-01-02에 USO를 샀다면 2025-12-30에" = 69.74 ÷ 102.48 − 1 = −31.9%. 같은 기간 WTI 근월물 = 57.95 ÷ 61.18 − 1 = −5.3%.
- 예: "KODEX WTI원유선물(H)가 2020-01-02 종가 21,135원을 처음 다시 넘은 날" = 2020-04-21 뒤로 종가가 21,135원 이상인 첫 날 = 2026-03-09(24,440원).
