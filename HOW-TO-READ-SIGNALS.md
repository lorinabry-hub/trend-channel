# 📡 How To Read Our Signals

Every alert sent to [@pumpfunearlytrending](https://t.me/pumpfunearlytrending) follows the same format. Here is how to decode it.

---

## Signal Format

```
🔥 [Token Name] New Trending

💰 MC $13,319 · 🕐 12m ago
📌 CA:
BJpEUmcVNjQT45KDwvSkVps5KZAQAxjuWpbrhrXBpump

📊 $25,110 Vol
🟢 429 Buys | 🔴 266 Sells

🔍 rugcheck.xyz 🟢 Good
👤 Top Holder 3.8%
👥 Top 10 Holders 24.2%
📦 Bundle Check 🟡 Low
└ 14 wallets · 5.9%
```

---

## Field-by-Field Breakdown

| Field | What It Means |
|-------|--------------|
| `💰 MC` | Market cap **at the moment we sent the signal** — this is your reference entry point |
| `🕐 Xm ago` | How many minutes since the token launched — we target 5–20 min |
| `📌 CA` | Contract address — copy this to trade on GMGN, Axiom, or your preferred DEX |
| `📊 Vol` | Total trading volume since launch |
| `🟢 Buys / 🔴 Sells` | Raw transaction count — more buys than sells = positive pressure |
| `🔍 rugcheck.xyz` | Third-party rug risk score — we only call 🟢 Good tokens |
| `👤 Top Holder` | Largest single wallet as % of supply — lower is healthier |
| `👥 Top 10 Holders` | Combined top 10 wallets — we reject tokens above 30% |
| `📦 Bundle Check` | Coordinated launch detection — 🟢 Low is ideal, 🔴 High is rejected |

---

## Follow-Up Alerts

After the initial signal, you may see:

**📈 Up Xx alert**
```
🚀 Commons is up 3x ⚡️
from 📡 Trending Signal

$13,319 → $40,774
```
This tracks the token's progress from our signal price. The left number is the signal MC, the right is current MC.

---

**🎓 Graduation alert**
```
🎓 LULU just graduated!
Bonding curve 100% — now live on PumpSwap 🔥

💰 MC $26,657 +90% from signal
💧 Liquidity $12,763
🕐 Reached in 42m from signal
```
Graduation means the token completed its Pump.fun bonding curve and moved to PumpSwap. This typically signals sustained momentum.

---

## Quick Trading Links

Every signal includes direct links to trade:

- **GMGN bot** — Telegram-based trading bot, fastest execution
- **Axiom** — Web-based DEX aggregator for Solana
- **Dexscreener** — Chart and liquidity view
- **Pump.fun** — Original token page

---

## Timing Is Everything

The signal MC shown is the price **when we sent the alert**. By the time you read it, the token may already be 10–20% higher. The faster you act, the closer to the signal price your entry will be.

This is why our 3–5 minute head start over the trending page matters.

---

## What To Do Before Buying

Even with our filters, always verify:

1. Check the CA on rugcheck.xyz yourself
2. Look at top holder % on Dexscreener
3. Check if volume looks organic or artificially spiked
4. Size your position to what you can afford to lose — this is speculative territory

We do the filtering. You do the final DYOR.

---

*Questions? Reach out via [@drako_pi](https://t.me/drako_pi)*
