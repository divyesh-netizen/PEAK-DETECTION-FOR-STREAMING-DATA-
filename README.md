# 🔺 Peak Detector in Verilog

## 📌 Overview

This project implements a **Peak Detector** using Verilog HDL.
It detects a **local maximum (peak)** in a stream of input data by comparing three consecutive samples.

A value is considered a peak if:

```
curr > prev AND curr > next
```

---

## ⚙️ Features

* ✅ Real-time peak detection
* ✅ Synchronous design (clock-based)
* ✅ Reset functionality
* ✅ Simple and efficient logic
* ✅ Verified using testbench and waveform

---

## 🧠 Working Principle

The design stores three consecutive values:

* `prev` → previous sample
* `curr` → current sample
* `next` → incoming sample

Peak condition:

```
if (curr > prev) && (curr > next)
    peak = 1;
else
    peak = 0;
```

---

## 📂 Project Structure

```
peak-detector-verilog/
│── src/
│   └── peak_detector.v
│
│── tb/
│   └── tb_peak.v
│
│── constraints/
│   └── peak.xdc
│
│── images/
│   ├── waveform.png
│   └── schematic.png
│
│── README.md
```

---

## ▶️ Simulation (Vivado)

1. Open Vivado and create a project
2. Add:

   * `peak_detector.v` (Design Source)
   * `tb_peak.v` (Simulation Source)
3. Set `tb_peak.v` as **Top Module**
4. Run:

   ```
   Run Simulation → Run Behavioral Simulation
   ```

---

## 📊 Example Output

| Input Sequence | Peak Output |
| -------------- | ----------- |
| 5              | 0           |
| 8              | 0           |
| 12             | 1 ✅         |
| 9              | 0           |

---

## 🧩 RTL Schematic

To view schematic in Vivado:

```
Set peak_detector.v as Top
→ Open Elaborated Design
→ View Schematic
```

---

## 🛠 Tools Used

* Xilinx Vivado
* Verilog HDL

---

## 🚀 Applications

* Signal processing
* Sensor data analysis
* Event detection systems
* Embedded systems

---


## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
