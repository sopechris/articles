# Randomized Trial of Infusion Set Function: Steel Versus Teflon

> **Citation:**  
>
> "Set failure was determined by (1) the meter blood glucose level not decreasing by at least 50 mg/dL an hour after a correction bolus for a blood glucose level greater than 300 mg/dL, (2) blood ketone levels greater than 0.6 mmol/L, or (3) evidence of infection at the infusion site. In reviewing the data, there were eight events where the glucose level was greater than 250 mg/dL for which the subject gave a correction bolus but 1 h later the glucose level had not decreased by 50 mg/dL. When the glucose level did not improve, the patients changed their infusion sets. Subjects stated that they were uncomfortable waiting for the glucose level to go above 300 mg/dL before giving a correction dose. In the data analysis we considered these eight subjects to have failed correction doses because of an infusion site failure."
>
> **Shah, V. N., et al. (2018).** *Randomized Trial of Infusion Set Function: Steel Versus Teflon*. _Diabetes Care_. [https://doi.org/10.2337/dc18-0386](https://doi.org/10.2337/dc18-0386)


---

## 🧠 Objective

> Using failure determining metric from stanford in individuals with type 1 diabetes using insulin pumps. (CGM and injected Bolus data)

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

## 🧩 My Interpretation

- The CGM > 250 mark is surpassed and tried to be corrected quite more often than the > 300.
- The inertia of CGM is higher at the 250 mark, which adds even more sensitivity into the alarm system.

---

## 🛠️ Implementation Notes

- Logic implemented to detect failures based on CGM + bolus timing
- Handling noisy data or missing insulin events
- Two options: more sensitive alarm (boluses when CGM > 250), less sensitive alarm (boluses when CGM > 300)

---

## 📌 To Do / Questions

- [ ] Implement full failure logic in `failure_logic/`
- [ ] Visualize glucose vs. insulin correction windows
- [ ] Compare my detection with paper results

