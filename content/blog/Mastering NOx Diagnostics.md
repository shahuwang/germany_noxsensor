---
title: Mastering NOx Diagnostics
description: Mastering NOx Diagnostics Using Inlet and Outlet Data for SCR Efficiency
breadcrumbs: true
date: "2023-12-10T00:35:28+08:00"
draft: false
---
### **Mastering NOx Diagnostics: Using Inlet and Outlet Data for SCR Efficiency**

The primary function of the two NOx sensors in a vehicle's exhaust system is to enable the Engine Control Unit (ECU) to calculate the Selective Catalytic Reduction (SCR) conversion efficiency in real-time. This efficiency calculation is the key metric for both emissions control and onboard diagnostics (OBD).

### **The Core Calculation: SCR Conversion Efficiency**

The SCR system’s performance is quantified by how much NOx is converted into harmless N2 (Nitrogen) and H2O (Water). The ECU uses a simple ratio of the two sensor readings to monitor this:

> **SCR Conversion Efficiency (%) = ((Inlet NOx - Outlet NOx) / Inlet NOx) x 100**

### **Interpreting Live Data Scenarios**

Analyzing the relationship between the Upstream (Inlet) and Downstream (Outlet) NOx readings helps pinpoint the root cause of an emissions fault:

| Inlet NOx Reading | Outlet NOx Reading | SCR Efficiency | Diagnosis |
| :--- | :--- | :--- | :--- |
| **High (~800 ppm)** | **Low (~100 ppm)** | **High (~87% - 90%)** | **System Healthy:** DEF dosing is correct, and the SCR catalyst is active. |
| **High** | **High (≈ Inlet)** | **Low (~0% - 30%)** | **Catalyst or Dosing Failure:** The SCR is not reducing NOx. Check DEF system first, then suspect catalyst degradation. |
| **Implausible/Stuck** | **Normal** | **Invalid** | **Inlet Sensor Failure:** The ECU cannot trust the Inlet reading, leading to improper dosing (often based on a backup model). **Replace Inlet Sensor.** |
| **Normal** | **Implausible/Stuck** | **Invalid** | **Outlet Sensor Failure:** The ECU cannot verify compliance. **Replace Outlet Sensor.** |

### **The OBD Monitor and Failure Thresholds**

The ECU constantly monitors this efficiency ratio. If the calculated SCR efficiency drops below a legally mandated OBD threshold (e.g., 80%) for a specified driving period, the ECU logs an efficiency fault code (P420 or P20EE equivalent).

Crucially, an incorrect reading from **either** the Inlet or the Outlet NOx sensor will skew this calculation, leading the ECU to incorrectly flag a catalyst or dosing failure, resulting in unnecessary repair costs.

Our sensors provide validated, stable, and synchronous readings, ensuring the ECU's efficiency calculation is always based on reliable data, allowing technicians to trust the system’s diagnostic conclusions.

---