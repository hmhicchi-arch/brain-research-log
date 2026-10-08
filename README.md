# BRAIN research log

WorldQuant BRAIN alpha research, logged hypothesis. Every run is in [log.md](log.md).

## Rule

Every entry states the hypothesis, who takes the other side, the predicted sign and the predicted turnover before any result is pasted. Every kill is logged with its cause: turnover, correlation, wrong sign or one lucky year. Every idea counts its variants.

## How a run is logged

1. Copy the entry template below into log.md.
2. Fill everything above the result line and commit. That commit is the proof the prediction came first.
3. Run the alpha on BRAIN.
4. Paste the result below the line and commit again.

## Entry template

```
## R___ · YYYY-MM-DD · <idea name>
- **Expression:**  
- **Settings:** USA · TOP3000 · delay 1 · decay _ · neutralization _ · truncation _
- **Hypothesis:**  
- **Other side:**  
- **Predicted:** sign _ · turnover low / medium / high
- **Variants tested (incl. this one):** _

**Result**

- Sharpe _ · fitness _ · turnover _% · returns _% · drawdown _%
- **Yearly:** stable / carried by one year
- **Verdict:** keep / kill (turnover | correlation | wrong sign | one lucky year) / submit
- **Grade:**
```

## Platform reference (copied 2026-10-07)

Submission bars, from BRAIN's results checks:
- Sharpe: min _
- Fitness: min _
- Turnover: min _% · max _%
- Self-correlation: max _

Default settings, from a fresh simulation's Settings panel:
- Language: Fast Expression · Instrument type: Equity
- Region: USA
- Universe: TOP3000
- Delay: 1
- Decay: 4
- Neutralization: Subindustry
- Truncation: 0.08
- Pasteurization: On
- Unit handling: Verify
- NaN handling: Off
- Test period: 1 year 0 months
- Lookback: 256 (greyed out)
