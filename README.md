# Open-Source Finance, Math & Civil Engineering Formula Reference

A clean, verified educational handbook explaining standard mathematical, financial, health, and civil engineering estimation formulas—complete with derivations, step-by-step numerical examples, edge-case notes, and code snippets.

Interactive browser-based tools implementing these formulas are available at **[AI Free Calculator](https://aifreecalculator.com/)**.

---

## Included Formulas & Derivations

### 1. Systematic Investment Plan (SIP)
```text
FV = P * [((1 + r)^n - 1) / r] * (1 + r)
```
- **Example:** Investing `5,000/month` for `10 years` (`n = 120`) at `12% p.a.` (`r = 0.01`) yields `~11,61,695`.
- Interactive tool: [SIP Calculator](https://aifreecalculator.com/finance/sip-calculator/)

### 2. Loan EMI (Reducing Balance)
```text
EMI = [P * R * (1 + R)^N] / [(1 + R)^N - 1]
```
```js
function calculateEMI(principal, annualRatePct, months) {
  if (annualRatePct === 0) return principal / months;
  const r = annualRatePct / 12 / 100;
  const factor = Math.pow(1 + r, months);
  return (principal * r * factor) / (factor - 1);
}
```
- Interactive tool: [Loan EMI Calculator](https://aifreecalculator.com/finance/emi-calculator/)

### 3. Concrete Mix & Dry Volume (1.54 Factor)
```text
Dry Volume = Wet Volume * 1.54
```
For **1 m³ of M20 concrete (`1 : 1.5 : 3`)**:
- Cement: `(1 / 5.5) * 1.54 = 0.28 m³` (~8 bags of 50 kg)
- Sand: `(1.5 / 5.5) * 1.54 = 0.42 m³`
- Coarse Aggregate: `(3 / 5.5) * 1.54 = 0.84 m³`
- Interactive tool: [Concrete Calculator](https://aifreecalculator.com/construction/concrete-calculator/)

### 4. Steel Rebar Unit Weight (IS 1786)
```text
Unit Weight (kg/m) = (pi / 4) * (D / 1000)^2 * 7850 = D^2 / 162.2
```
- `8 mm` = `0.395 kg/m` | `10 mm` = `0.617 kg/m` | `12 mm` = `0.888 kg/m` | `16 mm` = `1.578 kg/m`
- Interactive tool: [RCC Beam Steel Calculator](https://aifreecalculator.com/construction/rcc-beam-steel-calculator/)

### 5. Percentage, Relative Change & BMI
- **Percentage:** `(Part / Whole) * 100` — [Percentage Calculator](https://aifreecalculator.com/math/percentage-calculator/)
- **Roman Numerals:** Subtractive & additive notation — [Roman Numeral Converter](https://aifreecalculator.com/math/roman-numeral-converter/)
- **Body Mass Index:** `Weight (kg) / Height (m)^2` — [BMI Calculator](https://aifreecalculator.com/health/bmi-calculator/)

---

## License

MIT License — free to reference, fork, and share for educational purposes.
