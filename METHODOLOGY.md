# 🔬 Algorithm Methodology

> How Pumpfun Early Trending identifies signals before they hit the trending page.

---

## Overview

Our algorithm monitors every single token launched on Pump.fun in real time and assigns it a **score** based on multiple on-chain parameters. Only tokens with the highest scores — that also pass all safety filters — are issued as signals to our Telegram channel.

### V2 — Current Version

The V2 scoring engine represents a significant upgrade over the original system:

- **Coverage**: Every Pump.fun token is scanned — no launches are missed
- **Speed**: 4,000+ tokens analyzed per minute with sub-100ms signal latency
- **Infrastructure**: Persistent database storing all scan data in real time
- **API efficiency**: V2 reduced API call overhead while enabling more granular parameters
- **Scalability**: Architecture designed to add new scoring dimensions without latency impact

**Verified infrastructure stats (48h window, Mar 30–31 2026):**

| Metric | Value |
|--------|-------|
| Total API calls | 251,104 |
| Primary method (gettransaction) | 251,104 calls |
| Peak throughput | ~3.5 req/second |
| Avg gettransaction latency | 99ms |
| Avg gettokenaccounts latency | 117ms |
| Data processing | Real-time, persistent DB |

The goal is not to call everything. It is to score everything — and surface the right signals early, before the market catches on.

---

## Signal Timing

We target tokens in the **$10,000–$20,000 market cap range** that show strong early momentum.

At this stage, the token has not yet attracted significant attention from traders watching the trending page. This gives our subscribers a **3–5 minute head start** before the broader market notices.

Once a token hits the Pump.fun trending feed, the risk/reward ratio has already shifted.

---

## Scoring System

Every token receives a composite score at scan time. The score aggregates all parameters below into a single ranking. Signals are issued for tokens that: (a) pass all hard filters, and (b) rank in the top tier of the current scoring window.

This means we are not just filtering — we are **ranking**. A token can pass all safety checks but still not be called if better opportunities exist in the same window. The highest score wins the signal.

---

## Filtering Criteria

Every token is scored against the following parameters before a signal is issued:

### 1. Bundle Check
We detect coordinated wallet behavior at launch using on-chain pattern analysis.

| Score | Meaning |
|-------|---------|
| 🟢 Low | Acceptable — low coordinated buying |
| 🟡 Medium | Watch closely — some bundling detected |
| 🔴 High | Rejected — coordinated launch likely |

Tokens with High bundle scores are **never called**.

---

### 2. Holder Distribution
We check the concentration of supply among top wallets.

| Metric | Threshold |
|--------|-----------|
| Top Holder | Must be below 5% |
| Top 10 Holders | Must be below 30% |

Highly concentrated tokens are rejected. A healthy distribution suggests organic buying.

---

### 3. Rugcheck.xyz Score
Every signal is cross-referenced against [rugcheck.xyz](https://rugcheck.xyz).

| Score | Action |
|-------|--------|
| 🟢 Good | Eligible for signal |
| 🟡 Warn | Manual review — rarely called |
| 🔴 Danger | Rejected immediately |

---

### 4. Volume / Buy-Sell Ratio
We look for genuine buying momentum, not artificial pump patterns.

A valid signal has:
- Positive buy/sell ratio (more buys than sells)
- Volume growing relative to market cap
- No single wallet responsible for disproportionate volume

---

### 5. Liquidity Depth
We verify that enough liquidity exists at the signal price to allow meaningful entries and exits.

Tokens with thin liquidity create dangerous slippage conditions — we filter these out.

---

### 6. Time Since Launch
We call tokens **early but not too early**. Tokens called at launch (under 2 minutes old) often lack sufficient data for reliable scoring.

Our optimal window: **5–20 minutes post-launch**.

---

## What We Do Not Filter

We do not filter on:
- Token name or narrative (we are theme-agnostic)
- Social media presence (a token does not need a Twitter to be called)
- Price action patterns (we rely on on-chain data, not charts)

---

## Win Rate Calculation

**Win = a called token that reaches 2x or more from its signal market cap.**

We track the market cap at the exact time our alert was sent (timestamp-verified from Telegram) and compare it to the peak market cap recorded within 24 hours of the signal.

Win rate is published every Monday in [`/weekly-reports`](../weekly-reports/).

---

## Graduation Tracking

We also track **bonding curve graduations** — tokens that successfully complete their Pump.fun bonding curve and move to PumpSwap. This is a secondary success metric showing sustained momentum beyond the initial spike.

Example: Commons — graduated in **16 minutes** from signal, +168% MC at graduation.

---

## Limitations

- This algorithm does not guarantee profits. Markets are unpredictable.
- Signals are best used as a starting point for your own DYOR, not as a buy trigger.
- Speed matters: the earlier you act on a signal, the better your entry relative to others.
- Past win rates do not predict future performance.

---

*For questions about methodology, contact [@drako_pi](https://t.me/drako_pi) on Telegram.*
