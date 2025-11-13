# ⚡ Investigating HVDC Integration & Large Industrial Loads in IEEE-30 Bus System  
### *Power System Analysis using PSS®E v34*
---

## 📘 Project Overview  
This project investigates how **HVDC transmission lines** and **large industrial motor loads** affect the stability, voltage profile, and line loading of the *IEEE-30 Bus Test System*.  

The simulations were performed using **PSS/E Xplore 34** and include:
- Base IEEE-30 bus load-flow analysis  
- Adding large induction motor loads  
- Integrating HVDC links between various zones  
- System performance evaluation  
- Mitigation using shunts & parallel lines  

---

## 🏗 System Description  

### **IEEE-30 Bus Network**
- 30 buses (B01–B30)  
- 41 transmission lines  
- 12 transformers  
- 6 generators (G01–G06)  
- Slack bus at B31 (special extension for HVDC)  
- System base frequency: **60 Hz**

### **Added Components**
| Component | Description |
|----------|-------------|
| Industrial Loads | 50 MW & 100 MW Induction Motors at B3 & B4 |
| HVDC System | Rectifier at B31, Inverter at B32, Transformers on both ends |
| Zones | Three zones grouped by voltage profile & load characteristics |

---

## 🔬 Methodology  
### 1️⃣ Base Case  
- Original IEEE-30 bus  
- No industrial loads  
- No HVDC link  

### 2️⃣ Industrial Load Case  
- Added large induction motor loads  
- Observed undervoltage + overloaded lines  

### 3️⃣ HVDC Integration  
HVDC lines were inserted between:
- **B4 → B8**
- **B4 → B11**
- **B6 → B8 (failed to converge)**
- **Zone-1 → Zone-3**

Observations:
- Power-flow divergence in some cases  
- Motor stalling  
- DC control mismatch  
- Overloaded tie-lines  
- Undervoltage in multiple buses  

### 4️⃣ Mitigation Techniques  
To stabilize the system:
- Added fixed shunt capacitors  
- Added parallel transmission lines  
- Improved voltage drops  
- Reduced loading on stressed lines  

---

## 📊 Key Results (Summary)

### ✓ Industrial Load Effects  
- Multiple buses dropped < 0.90 p.u  
- Several lines exceeded 100% loading  
- Heavy reactive power consumption  

### ✓ After HVDC Addition  
- Further undervoltage  
- Overcurrent through multiple corridors  
- Convergence issues in some configurations  

### ✓ After Mitigation  
- Undervoltage mostly corrected  
- Overloaded lines relieved  
- Stable load flow achieved  

---

## 🧠 Limitations  
- IEEE-30 bus is not ideal for long-distance HVDC  
- PSS/E struggles with motor + HVDC nonlinearity  
- Lack of transient models  
- HVDC not stable for some bus pairs  

---

## 🚀 Future Work  
- Real-time HIL simulation  
- Renewable energy integration  
- Advanced HVDC control  
- Cybersecurity analysis  
- Smart grid integration  
- Improved damping & converter models  

---

## 📚 References  
- Grainger & Stevenson — *Power System Analysis*  
- Padiyar — *HVDC Transmission Systems*  
- IEEE PES Test Feeders  
- Zhou & Hu — HVDC Literature Review  

---
## 👨‍🏫 Academic Info
Developed for:  
**EEE 306 – Power System I Laboratory (July 2023)**  
**Bangladesh University of Engineering and Technology (BUET)** 
