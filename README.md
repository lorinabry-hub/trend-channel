# Pumpfun Early Trending 📡

> **Called first. Scam-filtered. Win rate verified.**

Algorithm-powered signal tool for Pump.fun tokens on Solana.  
We call tokens **3–5 minutes before** they hit the trending page — with scam filtering built in.

---

## 📊 Live Stats (Updated Weekly)

| Metric | Current |
|--------|---------|
| 🏆 Best call (March 2026) | **Deadwhale — 84x** |
| ⚡ Tokens analyzed per minute | **4,000+** |
| 🕐 Signal latency | **< 100ms** |
| 📡 API calls processed (48h) | **251,104** |
| 🚫 Scam tokens filtered | [500,000+] |
| 👥 Telegram subscribers | **8,200+** |
| 📅 Tracking since | December 2025 |

> Win rate = % of called tokens that reached at least 2x from signal price.  
> Updated every Monday. All calls are timestamp-verified.

---

## 🥇 Top 10 Calls — March 2026

| Rank | Token | Multiplier | Peak MC |
|------|-------|-----------|---------|
| 🥇 | Deadwhale | **84x** | $1.5M |
| 🥈 | BELLATOR | **61x** | $797.4K |
| 🥉 | PQC | **52x** | $871.1K |
| 4️⃣ | umi | **42x** | $885.4K |
| 5️⃣ | Kirkski | **39x** | $638.8K |
| 6️⃣ | PUMPPERPS | **28x** | $447.0K |
| 7️⃣ | RAM | **28x** | $670.6K |
| 8️⃣ | Land | **24x** | $497.7K |
| 9️⃣ | Retardcoin | **24x** | $463.9K |
| 🔟 | OnlyFarms | **20x** | $300.8K |

> All calls sourced from [@pumpfunearlytrending](https://t.me/pumpfunearlytrending).  
> Multiplier = peak MC ÷ signal MC. Timestamp-verified from Telegram alerts.

---

## ⚡ How It Works — Algorithm V2

```
Every token launched on Pump.fun is captured instantly
          ↓
  4,000+ tokens analyzed per minute
  251,104 on-chain calls processed in 48h (verified)
  < 100ms signal latency
          ↓
  V2 Scoring Engine assigns a score to every token
  based on: bundle check · holder distribution ·
  liquidity depth · buy/sell ratio · rug patterns
  + additional parameters (expanding with each update)
          ↓
  Only the highest-scoring clean tokens trigger a signal
          ↓
  Alert sent to Telegram 3–5 min before trending
  Data saved to persistent database in real time
          ↓
  You act. Others catch up later.
```

**V2 upgrade** reduced API overhead while adding more granular scoring parameters. Every token that launches on Pump.fun gets a score. Only the top scores become signals.

Each signal includes:
- 📌 Contract address
- 💰 Market cap at signal time
- 🕐 Time since launch
- 📊 Volume + buy/sell breakdown
- 🔍 Rugcheck.xyz score
- 👤 Top holder % + top 10 holders %
- 📦 Bundle check (Low / Medium / High)

---

## 🚫 What We Filter Out

We actively remove tokens showing signs of:

- **Bundled launches** — coordinated wallet buys at launch
- **Insider concentration** — top holder above 5% threshold
- **Suspicious sell pressure** — abnormal sell/buy ratio at signal time
- **Rug mechanics** — locked liquidity issues, honeypot patterns
- **Low holder distribution** — top 10 holders controlling >30%

Every scam we catch is logged in [`/scam-filtered`](./scam-filtered/).

---

## 📁 Repository Structure

```
pumpfun-early-trending/
├── README.md                  ← You are here
├── calls-log/                 ← All signals issued, week by week
│   ├── 2026-W13.md
│   └── ...
├── scam-filtered/             ← Tokens we caught and rejected
│   ├── 2026-W13.md
│   └── ...
├── weekly-reports/            ← Monday win rate summaries
│   ├── 2026-W13.md
│   └── ...
└── docs/
    ├── METHODOLOGY.md         ← How the algorithm works
    ├── HOW-TO-READ-SIGNALS.md ← Signal format explained
    └── FAQ.md                 ← Common questions
```

---

## 📬 Follow the Signals

| Platform | Link |
|----------|------|
| 📱 Telegram | [@pumpfunearlytrending](https://t.me/pumpfunearlytrend) |
| 🐦 X / Twitter | [@PumpEarlyTrend](https://x.com/PumpEarlyTrend) |
| 🤖 Buy Bot | [@pumpfunearlytrendingbot](https://t.me/pumpfunearlytrendingbot) |

---

## ⚠️ Disclaimer

This is not financial advice. All signals are algorithmic outputs for informational purposes only.  
Pump.fun tokens are highly speculative. Never invest more than you can afford to lose. DYOR.

---

*Updated every Monday. Last update: March 30, 2026.*
