# Randomized Trial of Infusion Set Function: Steel Versus Teflon

**Citation:**  
Shah, V. N., et al. (2018). *Randomized Trial of Infusion Set Function: Steel Versus Teflon*. Diabetes Care. [https://doi.org/10.2337/dc18-0386](https://doi.org/10.2337/dc18-0386)

---

## 🧠 Objective

> Compare the performance and failure rates of steel vs. Teflon infusion sets in individuals with type 1 diabetes using insulin pumps.

---

## 🧪 Methods

Details on:
- Clinical trial design
- Number of patients / duration
- Failure definition:
  1. BG > 300 mg/dL, no 50 mg/dL drop after 1h correction
  2. Ketones > 0.6 mmol/L
  3. Infection at infusion site
- How failures were adjudicated

---

## 📊 Key Results

- Number of failures per group
- Typical glycemic patterns preceding failure
- Subject behavior (e.g., early bolus, premature set changes)

---

## 🧩 My Interpretation

- Are the failure criteria too strict or too lenient?
- Can this logic be applied to CGM-only datasets?
- Did the material (steel vs. Teflon) affect detection?

---

## 🛠️ Implementation Notes

- Logic implemented to detect failures based on CGM + bolus timing
- Handling noisy data or missing insulin events
- Visualizations or timelines created

---

## 📌 To Do / Questions

- [ ] Implement full failure logic in `failure_logic/`
- [ ] Visualize glucose vs. insulin correction windows
- [ ] Compare my detection with paper results

