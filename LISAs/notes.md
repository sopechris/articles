# Continuous Glucose Monitoring Enables the Detection of Losses in Infusion Set Actuation (LISAs)

**Citation:**  
Breton, M. D., et al. (2023). *Continuous Glucose Monitoring Enables the Detection of Losses in Infusion Set Actuation (LISAs)*. Diabetes Care. [https://doi.org/10.2337/dc22-1523](https://doi.org/10.2337/dc22-1523)

---

## 🧠 Objective

Replicate results from the grid search in your own dataset
> Example: To evaluate how CGM data can be used to detect partial or total failures in insulin infusion sets that are not flagged by current alarms.

---

# Analysis of LISA Detection Using CGM

## 🧪 Methods

### Study Design
- **Algorithm Training**: Retrospective analysis of 62 infusion set insertions across 20 T1D patients  
- **Validation**: Used independent datasets and the UVA/Padova T1D Simulator (100 virtual subjects, 30-day simulations with 6-hour insulin suspensions)  

### Data Types
- **CGM**: Sampled every 5 minutes  
- **Insulin Delivery**: CSII logs (basal/bolus)  

### LISA Definition
Losses in Infusion Set Actuation due to:  
- Catheter dislodgment/occlusion  
- Insulin leakage  
- Lipohypertrophy at infusion sites  
- Mechanical pump failures  

### Detection Algorithms
| **Algorithm**               | **Mechanism**                                                                 | **Parameters**                     |
|-----------------------------|-------------------------------------------------------------------------------|------------------------------------|
| **Glucose Fault Metric (GFM)** | Accumulates hyperglycemia between SW/LW CGM averages; resets if glucose drops | SW: 30-60 min, LW: 6-12 hrs       |
| **Insulin Fault Metric (IFM)** | Tracks PIE deviations: `IFMₖ = (PIEₖˢʷ / PIEₖᴸʷ) - 1`                          | SW: 60 min, LW: 24 hrs            |
| **Hybrid ML Models**        | Combines supervised (logistic regression) and unsupervised (isolation forests) | Personalized thresholds per patient |

---

## 📊 Key Results

### Detection Performance
| **Metric**         | **Population Model** | **Personalized Model** |
|--------------------|----------------------|------------------------|
| **Sensitivity**    | 71.8%                | 80%                    |
| **False Alarms/Day** | 0.28                 | 0.06                   |
| **Median Lag**     | 120-180 minutes      | 90-150 minutes         |

### CGM Patterns During LISAs
- **Sustained hyperglycemia**: Glucose >180 mg/dL without correction  
- **Rising slope**: Persistent upward trend (>2 mg/dL/min)  
- **Divergence**: Short-window CGM averages exceed long-window baselines by >30%  

### Critical Thresholds
- **GFM**: Alarm at >40 mg/dL·hr accumulation  
- **IFM**: >20% drop in recent vs. historical PIE  
- **Slope**: >1 mg/dL/min sustained for >30 min  

## 💡 Clinical Impact
- **Hyperglycemia Reduction**: 50% decrease in prolonged hyperglycemia (>300 mg/dL)  
- **DKA Prevention**: Enables infusion set replacement before ketosis onset  
- **Closed-Loop Challenge**: Reduced performance in AID systems due to algorithm countermeasures  
