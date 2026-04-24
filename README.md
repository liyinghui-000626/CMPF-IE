# CMPF-IE: Causal Multi-Pipeline Fusion for Multimodal Information Extraction

A causal reasoning framework for robust multimodal information extraction (MIE) under cross-domain and low-resource conditions.

---

## Overview

This repository provides the implementation of **CMPF-IE (Causal Multi-Pipeline Fusion for Information Extraction)**, a novel inference-time causal reasoning framework designed to improve robustness in multimodal information extraction.

Unlike traditional correlation-driven models, CMPF-IE reformulates information extraction as a **causal reasoning problem**, enabling models to:

- Distinguish **causal evidence vs. spurious correlations**
- Improve **cross-domain generalization**
- Enhance **interpretability and reliability**

According to our paper, CMPF-IE improves extraction performance by **4–10 F1 points** across multiple benchmarks under zero-shot and few-shot settings. :contentReference[oaicite:1]{index=1}

---

## Method

CMPF-IE decomposes the extraction process into three causal reasoning stages:

### 1️⃣ Structured Causal Modeling
- Extract entities, actions, and relations
- Construct a **causal graph (G)**
- Anchor key elements in structured form

### 2️⃣ Counterfactual Intervention
- Apply **do-intervention** on key actions
- Generate counterfactual samples
- Test whether extracted evidence is **causally necessary**

### 3️⃣ Multi-source Fusion
- Combine:
  - factual reasoning (Y_fact)
  - counterfactual reasoning (Y_cf)
  - causal graph (G)
- Output final robust prediction (Ŷ)

This transforms the process from:

---

## Application: Smart Glasses in Elderly Care

This project explores a real-world deployment scenario:

### Smart-Glasses Elderly-Care Dataset (Private)

We construct a **multimodal dataset** collected via smart glasses in elderly-care environments, including:

-  Patient states (e.g., lying, walking, abnormal posture)
-  Caregiver actions (e.g., assisting, measuring blood pressure)
-  Medical devices (e.g., sphygmomanometer, wheelchair)
-  Egocentric visual perspective (from smart glasses)
-  Synchronized textual annotations

As described in the paper, this dataset is used for **target-domain validation** of cross-domain transfer. :contentReference[oaicite:2]{index=2}

---

##  Dataset Release Plan

Due to **privacy and ethical considerations** in healthcare scenarios:

- The **Smart-Glasses Elderly-Care dataset is currently private**
- Data includes **real-world human subjects and sensitive contexts**

 We plan to release:

-  **Anonymized subset**
-  **Processed annotations**
-  **Synthetic or simulated samples (if necessary)**

Dataset will be made publicly available **after review and approval**.

---

##  Installation

```bash
git clone https://github.com/liyinghui-000626/CMPF-IE.git
cd CMPF-IE


