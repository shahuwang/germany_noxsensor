---
title: Ammonia Slip -- The Hidden Meaning Behind High Downstream NOx Readings
description: Is it the Probe or the Module? Dissecting the NOx Sensor System for Accurate Repair
breadcrumbs: true
date: "2023-07-18T00:35:28+08:00"
draft: false
---
### **Decoding Ammonia Slip: How NOx Sensors Reveal SCR Over-Dosing**

A common point of confusion in SCR diagnostics is a high NOx reading from the downstream sensor. While this usually indicates NOx is escaping the system, it can also be a tell-tale sign of **Ammonia Slip** (NH3). This phenomenon is critical to understand, as it confirms an over-dosing issue, not necessarily a failed sensor.

### **The NH3 Cross-Sensitivity Principle**

NOx sensors, based on the electrochemical principle of Zirconia cells, are designed to measure NO and NO2. However, they exhibit an unavoidable **cross-sensitivity to Ammonia (NH3)**.

* NH3 is the reductant used in the SCR process. In a healthy system, NH3 is consumed by the catalyst.
* If too much DEF is injected (over-dosing), the catalyst runs out of NOx to react with, and the excess, unreacted NH3 leaks through the system—this is **Ammonia Slip**.
* When the downstream NOx sensor encounters the NH3, it interprets the gas as NOx and reports an inaccurately high NOx value.

### **Diagnosing Ammonia Slip via Live Data**

The pattern of the NOx readings reveals the presence of NH3 slip:

| Parameter | Reading During NH3 Slip | Conclusion |
| :--- | :--- | :--- |
| **Upstream (Inlet) NOx** | Normal or High | Engine is producing NOx. |
| **Downstream (Outlet) NOx** | Unusually **High** and potentially **Spiking** | The reading is artificially high due to NH3 interference. |
| **Calculated SCR Efficiency** | Appears to **Drop Drastically** or go negative | The ECU believes the catalyst is suddenly failing, but the physical issue is DEF over-dosing. |

### **Why NH3 Slip is a Problem**

Ammonia Slip is not just a diagnostic headache; it has real-world consequences:

1.  **Compliance Risk:** Even if the NOx is reduced, high NH3 emissions can violate non-NOx emissions standards and are easily detectable by an acrid odor.
2.  **DEF Waste:** Over-dosing means DEF is being consumed inefficiently.
3.  **Sensor Contamination:** Persistent NH3 slip leads to the formation of solid DEF byproducts on the downstream NOx sensor and the SCR catalyst, accelerating component failure.

Our sensors provide highly responsive and stable readings that allow ECU control logic to quickly identify and correct NH3 slip conditions, protecting both the environment and the entire SCR investment.

---