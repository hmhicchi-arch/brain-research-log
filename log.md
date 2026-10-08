# BRAIN log

## R000 · 2026-10-08 · Short-term reversal (BRAIN tutorial)

- **Expression:** `-returns`
- **Settings:** USA · TOP3000 · delay 1 · decay 4 · neutralization subindustry · truncation 0.08
- **Hypothesis:** One-day moves partly reverse: yesterday's losers beat yesterday's winners.
- **Other side:** on losers, hurried sellers (stop-losses, outflows, news overreaction); on winners, chasers buying after a big up day. Partly bid–ask bounce.
- **Predicted:** sign + · turnover high
- **Variants tested (incl. this one):** 1

**Result**

- Sharpe 1.14 · fitness 0.56 · turnover 81.77% · returns 19.97% · drawdown 15.77%
- **Yearly:** carried by one year (2020: 2.65)
- **Verdict:** kill (turnover + one lucky year)
- **Grade:** sign right · turnover right

## R001 · 2026-10-08 · Price–volume divergence (Alpha#6)

- **Expression:** `-ts_corr(open, volume, 10)`
- **Settings:** USA · TOP3000 · delay 1 · decay 4 · neutralization subindustry · truncation 0.08
- **Hypothesis:** Negative correlation between open price and volume indicates panic selling / institutional liquidations, leading to short-term mean-reversion gains; positive correlation signals buying hype and exhaustion.
- **Other side:** Panicked sellers on forced liquidations (when long); FOMO chasers buying high-volume breakouts (when short).
- **Predicted:** sign + · turnover medium
- **Variants tested (incl. this one):** 1

**Result**

- Sharpe 0.98 · fitness 0.37 · turnover 33.01% · returns 4.74% · drawdown 6.06%
- **Yearly:** unstable, negative years + positive years with low Sharpe and high Sharpe
- **Verdict:** kill (returns + unstable + not enough volume filter to distinct)
- **Grade:** sign right · turnover right

## R002 · 2026-10-08 · Volume-confirmed reversal (Alpha#12)
- **Expression:** sign(ts_delta(volume, 1)) * (-ts_delta(close, 1))  
- **Settings:** USA · TOP3000 · delay 1 · decay 4 · neutralization subindustry · truncation 0.08
- **Hypothesis:** Increasing volume amplifies the price signal reversal, while decreasing volume signals the lack of institutional involvement; therefore, it is less reliable for immediate reversal. 
- **Other side:** Panicked sellers / hungry buyers, with the action of institutional forces created them beforehand.
- **Predicted:** sign + · turnover high
- **Variants tested (incl. this one):** 2

**Result**

- Sharpe 1.16 · fitness 0.4 · turnover 74.99% · returns 8.87% · drawdown 13.26%
- **Yearly:** unstable, huge difference between a good year and a bad year (0.45 vs 2.11)
- **Verdict:** kill (turnover + unstable)
- **Grade:** sign right · turnover right
