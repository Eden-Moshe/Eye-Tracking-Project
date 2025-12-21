# 🐶 Evaluation of Human-Oriented Canine Communication Using Eye Tracking

![Python](https://img.shields.org/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)
![Data Science](https://img.shields.org/badge/Data-Analysis-green?style=for-the-badge)
![Status](https://img.shields.org/badge/Status-Phase_B-orange?style=for-the-badge)

## 👁️ Project Overview

This research project explores how humans interpret emotional cues from dogs, specifically focusing on the differences between **Brachycephalic** (flat-faced) and **Normocephalic** (long-snouted) breeds. By utilizing **Eye-Tracking Technology (Tobii Pro Spark)**, we record and analyze human gaze patterns to understand which facial or body areas (AOIs) are most critical for emotion recognition.

**Phase B Focus:** This repository contains the **algorithmic implementation** for processing raw eye-tracking data, identifying gaze fixations, and generating statistical models such as **Gaze Transition Matrices**.

---

## 🚀 Key Features & Methodology

The core of this phase is a custom Python pipeline designed to transform raw gaze coordinates into behavioral insights.

### 1. Data Ingestion 📂
* Parsing raw `.csv` exports from **Tobii Pro Lab**.
* Cleaning data and filtering invalid samples (e.g., blinks, track loss).

### 2. Fixation Identification (I-VT Algorithm) 📍
We implement the **Velocity-Threshold Identification (I-VT)** algorithm to classify gaze data:
* **Fixations:** Stable gaze points (velocity < threshold).
* **Saccades:** Rapid eye movements between points.

### 3. Dynamic AOI Mapping 🗺️
Since the stimuli are dynamic videos, our algorithm maps fixations to **Dynamic Areas of Interest (DAOIs)**:
* Mapping $(x, y)$ coordinates to specific polygons (e.g., *Eyes*, *Mouth*, *Torso*) frame-by-frame.

### 4. Transition Matrix Generation 📊
We generate **Gaze Transition Matrices** to visualize the scan path strategies:
* Calculating the probability of shifting attention from a **Source AOI** to a **Destination AOI**.
* Visualizing results using Grayscale Heatmaps (inspired by *Raptis et al., 2017*).

---

## 🛠️ Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Eye Tracking Logic:** Custom implementation of I-VT

---
## 👩‍💻 Authors

* **Yaniv Shtein**
* **Eden Moshe**

**Supervisors:** Dr. Julia Sheidin, Dr. Samah Idrees-Ghazawi  
*Braude College of Engineering, Software Engineering Department*

---

## 📝 Citation & References

This project builds upon methodologies from:
* *Iwauchi et al. (2023)* - Algorithm for scan-path length calculation.
* *Raptis et al. (2017)* - Gaze transition entropy and matrix visualization.
* *Correia-Caeiro et al. (2020)* - Inter-species eye-tracking study design.

---
