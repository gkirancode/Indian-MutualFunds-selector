# Mutual fund ranking

Generated 2026-10-24 13:45. Weights file `D:\Finance\Shares\Tools\AI\MFselector-new\weights.ini` (version 2).

> This is a research and comparison tool, not investment advice and not a recommendation to buy or sell. Scores rank funds only against the other funds in the same run and are based on PAST data; high past returns do not guarantee future returns. A percentile or z-score is relative to the funds supplied, not an absolute measure of safety. Short investment horizons (1-3 years) carry substantial equity risk. Small-cap, sectoral and thematic funds can be concentrated and high-risk; compare within a category and check suitability, exit load, tax and expense ratio yourself.

## Method

- **Scoring method:** percentile (a 0-100 percentile-based `final score` is always shown too).
- **Missing data:** `renormalize_available` -- a fund's score is the weighted average over the metrics it has (weights rescaled to 100%).
- **Coverage floor:** a fund needs 70% of the weight measured to be ranked; otherwise it is listed as INSUFFICIENT_DATA.
- **Low-confidence flag:** a category with fewer than 8 ranked funds is marked LOW CONFIDENCE.
- **Ranked within category.** Funds in different categories are never ranked together except in the clearly labelled exploratory list.
- **Risk-free rate:** 6.5%; rolling window 3 years (month-end); excess-return period 3 years; SIP simulated over 3 years.
- **Returns** are computed from Direct-Growth NAVs (mfapi.in / AMFI); drawdown is the worst peak-to-trough fall in the last 3 years (the same window for every fund).
- **Alpha / beta:** regression of monthly excess returns on the benchmark's over the last 3 years (needs 24+ months).
- **Benchmark:** small cap: Nifty Smallcap 250 TRI via index-fund proxy [Motilal Oswal Nifty Smallcap 250 Index Fund - Direct Plan - Growth] (7.1y history)
- **Data source:** NAV history from mfapi.in (mirrors AMFI); newest NAV dates are shown per category
- **Data source:** holdings files under data/holdings/ where present

### Weights

| Metric | Weight % | Better when |
|---|---|---|
| 1-year return (CAGR) | 5 | higher |
| 3-year return (CAGR) | 10 | higher |
| 5-year return (CAGR) | 15 | higher |
| Sharpe-style ratio | 5 | higher |
| Sortino ratio | 5 | higher |
| Rolling 3y windows positive | 10 | higher |
| SIP XIRR | 5 | higher |
| Maximum drawdown | 10 | smaller fall |
| 3y excess return vs benchmark | 10 | higher |
| Rolling windows beating benchmark | 10 | higher |
| Portfolio quality (0-100) | 5 | higher |
| Downside capture | 0 | lower |
| Time in top half of peers | 0 | higher |
| Jensen's alpha (per year, vs benchmark) | 5 | higher |
| Beta vs benchmark | 5 | lower |

Expense ratio is deliberately not scored.

## small cap

Newest NAV date in this group: 2026-10-23. 15 fund(s) ranked.

| Rank | Fund | Final score (0-100) | Composite | Weight measured | Data flags |
|---|---|---|---|---|---|
| 1 | BANDHAN Small Cap Fund - Direct Plan - Growth | 83.5 | 83.459 | 95% |  |
| 2 | Invesco India Small Cap Fund - Direct Plan - Growth | 79.3 | 79.323 | 95% |  |
| 3 | ITI Small Cap Fund - Direct Plan - Growth Option | 71.8 | 71.805 | 95% |  |
| 4 | BANK OF INDIA SMALL CAP FUND - Direct Plan - Growth | 70.3 | 70.301 | 95% |  |
| 5 | Quant Small Cap Fund - Direct Plan - Growth Option | 59.8 | 59.774 | 95% |  |
| 6 | DSP Small Cap Fund - Direct Plan - Growth | 51.4 | 51.429 | 100% |  |
| 7 | Axis Small Cap Fund - Direct Plan - Growth Option | 49.2 | 49.248 | 95% |  |
| 8 | PGIM India Small Cap Fund - Direct Plan - Direct Growth | 48.1 | 48.120 | 95% |  |
| 9 | Edelweiss Small Cap Fund - Direct Plan - Growth | 46.6 | 46.617 | 95% |  |
| 10 | Union Small Cap Fund - Direct Plan - Growth Option | 46.6 | 46.617 | 95% |  |
| 11 | Nippon India Small Cap Fund - Direct Plan - Growth Option | 44.3 | 44.286 | 100% |  |
| 12 | Sundaram Small Cap Fund - Direct Plan - GROWTH | 42.1 | 42.105 | 95% | DUPLICATE_NAME |
| 13 | UTI Small Cap Fund - Direct Plan - Growth | 25.6 | 25.564 | 95% |  |
| 14 | Aditya Birla Sun Life Small Cap Fund - Direct Plan - GROWTH | 18.0 | 18.045 | 95% |  |
| 15 | Kotak Small Cap Fund - Direct Plan - Growth | 13.5 | 13.534 | 95% |  |

**Excluded before scoring:**
- JPMorgan India Mid and Small Cap Fund - Direct Plan - Growth Option (119869): STALE_NAV(3620d)
- HSBC Small Cap Equity Fund - Growth Direct (120069): STALE_NAV(1428d)
- HSBC - Small Cap Fund - Growth Direct (120077): STALE_NAV(4564d)
- Sundaram Select Small Cap Series II Direct Growth (132985): STALE_NAV(2954d)
- Sundaram Select Small Cap Series III Direct Growth (134297): STALE_NAV(2397d)
- Sundaram Select Small Cap Series IV - Direct Growth (134373): STALE_NAV(2380d)
- IDBI Small Cap Fund - Growth Direct (141475): STALE_NAV(1184d)
- Sundaram Select Small Cap Series V Direct Plan - Growth (141499): STALE_NAV(1948d)
- Sundaram Select Small Cap Series VI Direct Plan - Growth (141561): STALE_NAV(1922d)
- Sundaram Emerging Small Cap Series I Direct Plan - Growth (142533): STALE_NAV(1324d)
- Sundaram Emerging Small Cap Series II Direct Plan - Growth (143010): STALE_NAV(1292d)
- Sundaram Emerging Small Cap Series III Direct Plan - Growth (143226): STALE_NAV(1262d)
- Sundaram Emerging Small Cap Series IV Direct Plan - Growth (143506): STALE_NAV(1229d)
- Sundaram Emerging Small Cap Series V Direct Plan - Growth (144437): STALE_NAV(1166d)
- Sundaram Emerging Small Cap Series VI Direct Plan - Growth (144728): STALE_NAV(1142d)
- Sundaram Emerging Small Cap VII Direct Plan - Growth (144988): STALE_NAV(1120d)
- Principal Small Cap Fund - Direct Plan - Growth Option (147131): STALE_NAV(1758d)
- Mahindra Manulife Small Cap Fund - Direct Plan - Growth (150915): insufficient history, 5y CAGR too low
- LIC MF Small Cap Fund - Direct Plan - Growth (152004): insufficient history, 5y CAGR too low
- QUANTUM SMALL CAP FUND - Direct Plan - Growth Option (152107): insufficient history, 3y CAGR too low, 5y CAGR too low
- Baroda BNP Paribas Small Cap Fund - Direct Plan - Growth Option (152128): insufficient history, 3y CAGR too low, 5y CAGR too low
- Motilal Oswal Small Cap Fund - Direct Plan - Growth (152237): insufficient history, 3y CAGR too low, 5y CAGR too low
- JM Small Cap Fund - Direct Plan - Growth Option (152614): insufficient history, 3y CAGR too low, 5y CAGR too low
- TRUSTMF SMALL CAP FUND - Direct Plan - Growth (152939): insufficient history, 3y CAGR too low, 5y CAGR too low
- Mirae Asset Small Cap Fund - Direct Plan - Growth (153196): insufficient history, 3y CAGR too low, 5y CAGR too low
- Bajaj Finserv Small Cap Fund - Direct Plan - Growth (153612): insufficient history, 3y CAGR too low, 5y CAGR too low
- Samco Small Cap Fund - Direct Plan - Growth (153868): insufficient history, 3y CAGR too low, 5y CAGR too low
- Helios Small Cap Fund - Direct Plan - Growth (153912): insufficient history, 3y CAGR too low, 5y CAGR too low
- Groww Small Cap Fund - Direct Plan - Growth (154063): insufficient history, 3y CAGR too low, 5y CAGR too low
- Abakkus Small Cap Fund - Direct Plan - Growth (154215): insufficient history, 3y CAGR too low, 5y CAGR too low
- The Wealth Company Small Cap Fund - Direct Plan - Growth (154269): insufficient history, 3y CAGR too low, 5y CAGR too low
- Franklin India Small Cap Fund - Direct Plan - Growth (118525): 3y CAGR too low
- Sundaram Small Cap Fund - Direct Plan - GROWTH (119588): 3y CAGR too low, 5y CAGR too low
- ICICI Prudential Small Cap Fund - Direct Plan - Growth (120591): 3y CAGR too low
- SBI SMALL CAP FUND - Direct Plan - Growth (125497): 3y CAGR too low
- HDFC Small Cap Fund - Direct Plan - Growth Option (130503): 3y CAGR too low
- Tata Small Cap Fund - Direct Plan - Growth Option (145206): 3y CAGR too low
- Canara Robeco Small Cap Fund - Direct Plan - GROWTH OPTION (146130): 3y CAGR too low

### #1 BANDHAN Small Cap Fund - Direct Plan - Growth

| Metric | Value | Score 0-100 | Weight % | Effective weight % | Points |
|---|---|---|---|---|---|
| 1-year return (CAGR) | 2.3% | 50 | 5 | 5.3 | 2.6 |
| 3-year return (CAGR) | 22.1% | 100 | 10 | 10.5 | 10.5 |
| 5-year return (CAGR) | 18.0% | 100 | 15 | 15.8 | 15.8 |
| Sharpe-style ratio | 0.75 | 100 | 5 | 5.3 | 5.3 |
| Sortino ratio | 1.40 | 100 | 5 | 5.3 | 5.3 |
| Rolling 3y windows positive | 100.0% | 75 | 10 | 10.5 | 7.9 |
| SIP XIRR | 10.1% | 86 | 5 | 5.3 | 4.5 |
| Maximum drawdown | -22.8% | 79 | 10 | 10.5 | 8.3 |
| 3y excess return vs benchmark | +10.75 pp | 100 | 10 | 10.5 | 10.5 |
| Rolling windows beating benchmark | 80.0% | 64 | 10 | 10.5 | 6.8 |
| Portfolio quality (0-100) | n/a | n/a | 5 | - | - |
| Jensen's alpha (per year, vs benchmark) | +9.59 pp | 100 | 5 | 5.3 | 5.3 |
| Beta vs benchmark | 0.91 | 14 | 5 | 5.3 | 0.8 |

Final score 83.5 (points add up to this); weight measured 95%. Category: Equity Scheme - Small Cap Fund.

- Strengths: 5-year return (cagr) (18.0%, score 100), 3-year return (cagr) (22.1%, score 100), 3y excess return vs benchmark (+10.75 pp, score 100).
- Weak spots: beta vs benchmark (0.91, score 14).
- Not measured: portfolio quality (0-100) (their weight was spread over the measured metrics).
- Risk notes: this category can be concentrated and volatile.
- Portfolio quality: no holdings file matched this scheme

### #2 Invesco India Small Cap Fund - Direct Plan - Growth

| Metric | Value | Score 0-100 | Weight % | Effective weight % | Points |
|---|---|---|---|---|---|
| 1-year return (CAGR) | 2.9% | 57 | 5 | 5.3 | 3.0 |
| 3-year return (CAGR) | 19.5% | 86 | 10 | 10.5 | 9.0 |
| 5-year return (CAGR) | 17.4% | 86 | 15 | 15.8 | 13.5 |
| Sharpe-style ratio | 0.64 | 86 | 5 | 5.3 | 4.5 |
| Sortino ratio | 1.04 | 86 | 5 | 5.3 | 4.5 |
| Rolling 3y windows positive | 100.0% | 75 | 10 | 10.5 | 7.9 |
| SIP XIRR | 9.6% | 71 | 5 | 5.3 | 3.8 |
| Maximum drawdown | -23.4% | 64 | 10 | 10.5 | 6.8 |
| 3y excess return vs benchmark | +8.10 pp | 86 | 10 | 10.5 | 9.0 |
| Rolling windows beating benchmark | 94.0% | 89 | 10 | 10.5 | 9.4 |
| Portfolio quality (0-100) | n/a | n/a | 5 | - | - |
| Jensen's alpha (per year, vs benchmark) | +7.30 pp | 86 | 5 | 5.3 | 4.5 |
| Beta vs benchmark | 0.87 | 64 | 5 | 5.3 | 3.4 |

Final score 79.3 (points add up to this); weight measured 95%. Category: Equity Schemes - Small Cap Fund.

- Strengths: 5-year return (cagr) (17.4%, score 86), rolling windows beating benchmark (94.0%, score 89), 3-year return (cagr) (19.5%, score 86).
- Not measured: portfolio quality (0-100) (their weight was spread over the measured metrics).
- Risk notes: this category can be concentrated and volatile.
- Portfolio quality: no holdings file matched this scheme

### #3 ITI Small Cap Fund - Direct Plan - Growth Option

| Metric | Value | Score 0-100 | Weight % | Effective weight % | Points |
|---|---|---|---|---|---|
| 1-year return (CAGR) | 7.5% | 79 | 5 | 5.3 | 4.1 |
| 3-year return (CAGR) | 20.6% | 93 | 10 | 10.5 | 9.8 |
| 5-year return (CAGR) | 15.9% | 64 | 15 | 15.8 | 10.2 |
| Sharpe-style ratio | 0.67 | 93 | 5 | 5.3 | 4.9 |
| Sortino ratio | 1.17 | 93 | 5 | 5.3 | 4.9 |
| Rolling 3y windows positive | 100.0% | 75 | 10 | 10.5 | 7.9 |
| SIP XIRR | 10.5% | 93 | 5 | 5.3 | 4.9 |
| Maximum drawdown | -24.2% | 43 | 10 | 10.5 | 4.5 |
| 3y excess return vs benchmark | +9.23 pp | 93 | 10 | 10.5 | 9.8 |
| Rolling windows beating benchmark | 57.8% | 43 | 10 | 10.5 | 4.5 |
| Portfolio quality (0-100) | n/a | n/a | 5 | - | - |
| Jensen's alpha (per year, vs benchmark) | +8.39 pp | 93 | 5 | 5.3 | 4.9 |
| Beta vs benchmark | 0.90 | 29 | 5 | 5.3 | 1.5 |

Final score 71.8 (points add up to this); weight measured 95%. Category: Equity Scheme - Small Cap Fund.

- Strengths: 3-year return (cagr) (20.6%, score 93), 3y excess return vs benchmark (+9.23 pp, score 93), rolling 3y windows positive (100.0%, score 75).
- Weak spots: beta vs benchmark (0.90, score 29).
- Not measured: portfolio quality (0-100) (their weight was spread over the measured metrics).
- Risk notes: this category can be concentrated and volatile.
- Portfolio quality: no holdings file matched this scheme

### #4 BANK OF INDIA SMALL CAP FUND - Direct Plan - Growth

| Metric | Value | Score 0-100 | Weight % | Effective weight % | Points |
|---|---|---|---|---|---|
| 1-year return (CAGR) | 16.7% | 100 | 5 | 5.3 | 5.3 |
| 3-year return (CAGR) | 18.8% | 79 | 10 | 10.5 | 8.3 |
| 5-year return (CAGR) | 17.9% | 93 | 15 | 15.8 | 14.7 |
| Sharpe-style ratio | 0.54 | 79 | 5 | 5.3 | 4.1 |
| Sortino ratio | 0.96 | 79 | 5 | 5.3 | 4.1 |
| Rolling 3y windows positive | 100.0% | 75 | 10 | 10.5 | 7.9 |
| SIP XIRR | 13.9% | 100 | 5 | 5.3 | 5.3 |
| Maximum drawdown | -27.1% | 0 | 10 | 10.5 | 0.0 |
| 3y excess return vs benchmark | +7.44 pp | 79 | 10 | 10.5 | 8.3 |
| Rolling windows beating benchmark | 86.0% | 79 | 10 | 10.5 | 8.3 |
| Portfolio quality (0-100) | n/a | n/a | 5 | - | - |
| Jensen's alpha (per year, vs benchmark) | +6.53 pp | 79 | 5 | 5.3 | 4.1 |
| Beta vs benchmark | 0.95 | 0 | 5 | 5.3 | 0.0 |

Final score 70.3 (points add up to this); weight measured 95%. Category: Equity Scheme - Small Cap Fund.

- Strengths: 5-year return (cagr) (17.9%, score 93), 3-year return (cagr) (18.8%, score 79), 3y excess return vs benchmark (+7.44 pp, score 79).
- Weak spots: maximum drawdown (-27.1%, score 0), beta vs benchmark (0.95, score 0).
- Not measured: portfolio quality (0-100) (their weight was spread over the measured metrics).
- Risk notes: this category can be concentrated and volatile.
- Portfolio quality: no holdings file matched this scheme

### #5 Quant Small Cap Fund - Direct Plan - Growth Option

| Metric | Value | Score 0-100 | Weight % | Effective weight % | Points |
|---|---|---|---|---|---|
| 1-year return (CAGR) | 3.8% | 64 | 5 | 5.3 | 3.4 |
| 3-year return (CAGR) | 16.4% | 71 | 10 | 10.5 | 7.5 |
| 5-year return (CAGR) | 16.5% | 79 | 15 | 15.8 | 12.4 |
| Sharpe-style ratio | 0.48 | 71 | 5 | 5.3 | 3.8 |
| Sortino ratio | 0.89 | 71 | 5 | 5.3 | 3.8 |
| Rolling 3y windows positive | 90.0% | 14 | 10 | 10.5 | 1.5 |
| SIP XIRR | 6.2% | 36 | 5 | 5.3 | 1.9 |
| Maximum drawdown | -24.4% | 29 | 10 | 10.5 | 3.0 |
| 3y excess return vs benchmark | +5.07 pp | 71 | 10 | 10.5 | 7.5 |
| Rolling windows beating benchmark | 94.0% | 89 | 10 | 10.5 | 9.4 |
| Portfolio quality (0-100) | n/a | n/a | 5 | - | - |
| Jensen's alpha (per year, vs benchmark) | +4.59 pp | 71 | 5 | 5.3 | 3.8 |
| Beta vs benchmark | 0.88 | 36 | 5 | 5.3 | 1.9 |

Final score 59.8 (points add up to this); weight measured 95%. Category: Equity Scheme - Small Cap Fund.

- Strengths: 5-year return (cagr) (16.5%, score 79), rolling windows beating benchmark (94.0%, score 89), 3-year return (cagr) (16.4%, score 71).
- Weak spots: rolling 3y windows positive (90.0%, score 14), maximum drawdown (-24.4%, score 29).
- Not measured: portfolio quality (0-100) (their weight was spread over the measured metrics).
- Risk notes: this category can be concentrated and volatile.
- Portfolio quality: no holdings file matched this scheme

## Notes on missing data

Nothing is estimated: a metric that cannot be computed (too little history, no benchmark, no holdings file) is left missing and handled by the missing-data policy above. Portfolio quality is missing for funds with no matching, recent AMC holdings file. See the run log for the full list of warnings.
