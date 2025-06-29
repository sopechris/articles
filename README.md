This repository contains notes, summaries, and exploratory code based on two clinical research papers focused on detecting insulin infusion set failures using continuous glucose monitoring (CGM) data.

## 🧪 Articles Covered

### 1. [Continuous Glucose Monitoring Enables the Detection of Losses in Infusion Set Actuation (LISAs)](https://doi.org/10.2337/dc22-1523)
**Authors:** Marc D. Breton et al.  
**Journal:** *Diabetes Care*, 2023  
**Focus:** Uses CGM data to identify undetected or progressive failures in insulin delivery (LISAs).  
Includes:
- Direct application of the results
- Prototype code for identifying LISAs from CGM and insulin trends

---

### 2. [Randomized Trial of Infusion Set Function: Steel Versus Teflon](https://doi.org/10.2337/dc18-0386)
**Authors:** Viral N. Shah et al.  
**Journal:** *Diabetes Care*, 2018  
**Focus:** Using Stanford's research group's criteria to determine failure in insulin pumps (using CGM and Bolus data).
Includes:
- Summary of trial design and failure definition
- Code for reproducing their failure logic
- Data review approach based on CGM and insulin events

---

## 📁 Structure

articles/  
├── LISAs/  
│ ├── notes.md  
│ ├── detection_code/  
│ └── figures/  
│  
├── Stanford_InfusionSet_Trial/  
│ ├── notes.md  
│ ├── failure_logic/  
│ └── data_examples/  
│  
├── LICENSE  
└── README.md  


## 🧠 Goals

- Deeply understand methods for detecting insulin infusion set issues using sensor data
- Replicate key elements from each paper
- Build reusable tools and logic for future MedTech or diabetes-related applications

## 📖 Citations

- Breton, M. D., et al. (2023). *Continuous Glucose Monitoring Enables the Detection of Losses in Infusion Set Actuation (LISAs)*. Diabetes Care. [https://doi.org/10.2337/dc22-1523](https://doi.org/10.2337/dc22-1523)  
- Shah, V. N., et al. (2018). *Randomized Trial of Infusion Set Function: Steel Versus Teflon*. Diabetes Care. [https://doi.org/10.2337/dc18-0386](https://doi.org/10.2337/dc18-0386)

---

## ⚖️ License

This work is shared under the MIT License. See [`LICENSE`](LICENSE) for details.
