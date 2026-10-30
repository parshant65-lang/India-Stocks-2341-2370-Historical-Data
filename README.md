# India-Stocks-2341-2370-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2341 to 2370)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2341-2370-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2341 to 2370)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2341 | `SUTLEJTEX` | Sutlej Textiles and Industries Limited | `SUTLEJTEX.NS` |
| 2342 | `SUVEN` | Suven Life Sciences Limited | `SUVEN.NS` |
| 2343 | `SUVIDHAA` | Suvidhaa Infoserve Limited | `SUVIDHAA.NS` |
| 2344 | `SUYOG` | Suyog Telematics Limited | `SUYOG.NS` |
| 2345 | `SVGLOBAL` | S V Global Mill Limited | `SVGLOBAL.NS` |
| 2346 | `SVLL` | Shree Vasu Logistics Limited | `SVLL.NS` |
| 2347 | `SVPGLOB` | SVP GLOBAL TEXTILES LIMITED | `SVPGLOB.NS` |
| 2348 | `SWANDEF` | Swan Defence and Heavy Industries Limited | `SWANDEF.NS` |
| 2349 | `SWARAJ` | Swaraj Suiting Limited | `SWARAJ.NS` |
| 2350 | `SWARAJENG` | Swaraj Engines Limited | `SWARAJENG.NS` |
| 2351 | `SWARNSAR` | Swarnsarita Jewels India Limited | `SWARNSAR.NS` |
| 2352 | `SWASTIKAIN` | Swastika Infra Limited | `SWASTIKAIN.NS` |
| 2353 | `SWELECTES` | Swelect Energy Systems Limited | `SWELECTES.NS` |
| 2354 | `SWISSMLTRY` | Swiss Military Consumer Goods Limited | `SWISSMLTRY.NS` |
| 2355 | `SWSOLAR` | Sterling and Wilson Renewable Energy Limited | `SWSOLAR.NS` |
| 2356 | `SYMBIOTEC` | Symbiotec Pharmalab Limited | `SYMBIOTEC.NS` |
| 2357 | `SYMPHONY` | Symphony Limited | `SYMPHONY.NS` |
| 2358 | `SYNCOMF` | Syncom Formulations (India) Limited | `SYNCOMF.NS` |
| 2359 | `SYSTMTXC` | Systematix Corporate Services Limited | `SYSTMTXC.NS` |
| 2360 | `TAALTECH` | Taal Tech Limited | `TAALTECH.NS` |
| 2361 | `TAINWALCHM` | Tainwala Chemical and Plastic (I) Limited | `TAINWALCHM.NS` |
| 2362 | `TAJGVK` | Taj GVK Hotels & Resorts Limited | `TAJGVK.NS` |
| 2363 | `TAKE` | TAKE Limited | `TAKE.NS` |
| 2364 | `TALBROAUTO` | Talbros Automotive Components Limited | `TALBROAUTO.NS` |
| 2365 | `TAMBOLIIN` | Tamboli Industries Limited | `TAMBOLIIN.NS` |
| 2366 | `TANAA` | Taneja Aerospace & Aviation Limited | `TANAA.NS` |
| 2367 | `TANLA` | Tanla Platforms Limited | `TANLA.NS` |
| 2368 | `TARACHAND` | Tara Chand InfraLogistic Solutions Limited | `TARACHAND.NS` |
| 2369 | `TARAPUR` | Tarapur Transformers Limited | `TARAPUR.NS` |
| 2370 | `TARC` | TARC Limited | `TARC.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SUTLEJTEX 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2341-2370-Historical-Data/main/SUTLEJTEX/1m/2026/10/SUTLEJTEX_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
