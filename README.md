# Vector Control and Maximum Torque Per Ampere (MTPA) Control of Induction Motor

---

## 📌 Project Overview
This project focuses on the **modeling, simulation, and experimental implementation** of
**Indirect Vector Control (IVC)** and **Maximum Torque Per Ampere (MTPA)** control
strategies for a **three-phase induction motor**.

The work demonstrates how **field-oriented control (FOC)** enables independent control
of torque and flux, similar to a DC motor, and shows that **MTPA control significantly
reduces stator current** under light-load conditions, improving overall efficiency.

---

## 🎯 Objectives
- Model the induction motor in the **synchronously rotating reference frame (dq-frame)**
- Implement **Indirect Rotor Flux Oriented Vector Control**
- Implement **Maximum Torque Per Ampere (MTPA)** control
- Compare IV and MTPA control in terms of **current, torque, and efficiency**
- Validate results through **MATLAB/Simulink simulations**
- Perform **experimental verification** using a DSP-based drive system

---

## ⚙️ Motor & System Specifications
- Motor Type: Three-phase squirrel cage induction motor  
- Rated Voltage: 415 V (L–L, RMS)  
- Rated Power: 1.1 kW (1.5 HP)  
- Rated Speed: 1410 rpm  
- Controller: **TMS320F28335 DSP**  
- Inverter: Three-phase VSI (IGBT/IPM based)

---

## 🧠 Control Techniques Implemented

### 🔹 Indirect Vector Control (IVC)
- Rotor flux oriented control (RFOC)
- Decoupled control of flux (`i_d`) and torque (`i_q`)
- Slip speed estimation using rotor time constant
- Implemented using:
  - Current Controlled VSI (CCVSI)
  - Voltage Controlled VSI (VCVSI)

### 🔹 Maximum Torque Per Ampere (MTPA)
- Flux level optimized based on load condition
- Minimizes stator current for a given torque
- Especially suitable for **EV and energy-efficient drives**
- Demonstrates reduced current at light load compared to IV control

---

## 🧪 Simulation Details
- Software: **MATLAB / Simulink**
- Dynamic performance evaluated under:
  - Step change in speed
  - Step change in load torque
- Observed variables:
  - Speed response
  - Electromagnetic torque
  - Phase currents
  - dq-axis rotor flux

---

## 🔬 Experimental Setup
- Three-phase AC supply → Rectifier → DC link → VSI
- Motor coupled with DC generator as load
- Speed measurement using **tachogenerator**
- Current and voltage sensing with isolation
- PWM generation using **DSP TMS320F28335**
- Optocoupler-based gate drive for inverter isolation

---

## 📊 Key Results
- **MTPA control draws less stator current** than IV control
- At no-load:
  - IV control: ~1.75 A
  - MTPA control: ~1.47 A
- At loaded condition:
  - IV control: ~1.85 A
  - MTPA control: ~1.49 A
- Confirms **higher efficiency of MTPA control**

---

## 📁 Repository Structure
- `MATLAB_Simulink/` → Modeling & control simulations  
- `Firmware/` → DSP control code (IV & MTPA)  
- `Hardware/` → Experimental setup & sensor boards  
- `Results/` → Simulation and hardware waveforms  
- `Documentation/` → Detailed project report  

---

## 🚀 Applications
- Electric vehicle (EV) traction drives
- Energy-efficient motor drives
- Industrial variable-speed drives
- Research & academic motor control studies

---

## 🔭 Future Scope
- Online rotor resistance estimation improvement
- Speed sensorless vector control
- Space Vector PWM (SVPWM) implementation
- Extension to high-power traction drives

---

## 📜 License
This project is intended for **academic and research purposes only**.
