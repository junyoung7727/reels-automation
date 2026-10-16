# 데이터

2026-10-11에 네이버 금융 공개 주소에서 받음. 2025-06-02 ~ 2026-10-08.

- `035720_daily.csv`(카카오), `KOSPI_daily.csv`, `035420_daily.csv`(네이버): `https://api.finance.naver.com/siseJson.naver?symbol=<코드>&requestType=1&startTime=20250601&endTime=20261011&timeframe=day`
- `035720_investor_flows.csv`: `https://m.stock.naver.com/api/stock/035720/trend?pageSize=60&bizdate=<날짜>` (외국인·기관·개인 순매수 주식 수, 2025-07-16부터)
- 시가총액·PER·컨센서스는 `https://m.stock.naver.com/api/stock/<코드>/integration`, `/finance/annual` (2026-10-08 기준, 파일로 남기지 않고 facts.md 5.5에 옮김)
