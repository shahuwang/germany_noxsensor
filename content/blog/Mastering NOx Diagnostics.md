---
title: NOx-Diagnose meistern
description: NOx-Diagnose meistern mithilfe von Einlass- und Auslassdaten für die SCR-Effizienz
breadcrumbs: true
date: "2023-12-10T00:35:28+08:00"
draft: false
---
### **NOx-Diagnose meistern: Verwendung von Einlass- und Auslassdaten für die SCR-Effizienz**

Die Hauptfunktion der beiden NOx-Sensoren im Abgassystem eines Fahrzeugs besteht darin, der Motorsteuerung (ECU) zu ermöglichen, die **Konvertierungseffizienz der selektiven katalytischen Reduktion (SCR)** in Echtzeit zu berechnen. Diese Effizienzberechnung ist die Schlüsselkennzahl sowohl für die Emissionskontrolle als auch für die On-Board-Diagnose (OBD).

### **Die Kernberechnung: SCR-Konvertierungseffizienz**

Die Leistung des SCR-Systems wird dadurch quantifiziert, wie viel NOx in harmloses N2 (Stickstoff) und H2O (Wasser) umgewandelt wird. Die ECU verwendet ein einfaches Verhältnis der beiden Sensorwerte, um dies zu überwachen:

> **SCR-Konvertierungseffizienz (%) = ((NOx am Einlass - NOx am Auslass) / NOx am Einlass) x 100**

### **Interpretation von Live-Datenszenarien**

Die Analyse der Beziehung zwischen den Upstream- (Einlass) und Downstream- (Auslass) NOx-Werten hilft, die Grundursache eines Emissionsfehlers zu lokalisieren:

| NOx-Wert am Einlass | NOx-Wert am Auslass | SCR-Effizienz | Diagnose |
| :--- | :--- | :--- | :--- |
| **Hoch (~800 ppm)** | **Niedrig (~100 ppm)** | **Hoch (~87% - 90%)** | **System intakt:** Die DEF-Dosierung ist korrekt und der SCR-Katalysator ist aktiv. |
| **Hoch** | **Hoch (≈ Einlass)** | **Niedrig (~0% - 30%)** | **Katalysator- oder Dosierfehler:** Die SCR reduziert NOx nicht. Überprüfen Sie zuerst das DEF-System, dann vermuten Sie eine Katalysatordegradation. |
| **Unplausibel/Steckengeblieben** | **Normal** | **Ungültig** | **Fehler des Einlasssensors:** Die ECU kann dem Einlasswert nicht vertrauen, was zu einer unsachgemäßen Dosierung führt (oft basierend auf einem Ersatzmodell). **Einlasssensor ersetzen.** |
| **Normal** | **Unplausibel/Steckengeblieben** | **Ungültig** | **Fehler des Auslasssensors:** Die ECU kann die Einhaltung nicht überprüfen. **Auslasssensor ersetzen.** |

### **Der OBD-Monitor und Fehlerschwellen**

Die ECU überwacht dieses Effizienzverhältnis ständig. Wenn die berechnete SCR-Effizienz für einen bestimmten Fahrzeitraum unter einen gesetzlich vorgeschriebenen OBD-Schwellenwert (z. B. 80 %) fällt, protokolliert die ECU einen Effizienzfehlercode (P420 oder P20EE-Äquivalent).

Entscheidend ist, dass ein falscher Wert von **entweder** dem NOx-Sensor am Einlass **oder** dem NOx-Sensor am Auslass diese Berechnung verfälscht, was die ECU dazu verleitet, fälschlicherweise einen Katalysator- oder Dosierfehler zu melden, was zu unnötigen Reparaturkosten führt.

Unsere Sensoren liefern validierte, stabile und synchrone Messwerte, wodurch sichergestellt wird, dass die Effizienzberechnung der ECU stets auf zuverlässigen Daten basiert, sodass Techniker den diagnostischen Schlussfolgerungen des Systems vertrauen können.