# Risquanter — Advanced Simulation‑Based Risk Analytics

Risquanter is an open initiative dedicated to building **next‑generation, simulation‑driven risk analytics software**.  
Our mission is to provide **auditable**, **reproducible**, and **high‑performance** tools for quantitative risk modeling, uncertainty propagation, and decision support.

We focus on modern approaches to risk analytics, including:

- **Reproducible Monte Carlo simulation**
- **Probabilistic modeling using SIPmath / Metalog / HDR distributions**
- **Tree‑structured risk aggregation**
- **Formal logic for vague or probabilistic quantifiers**
- **High‑performance, type‑safe implementations in Scala**

Risquanter aims to bridge the gap between academic research, enterprise‑grade engineering, and practical risk management workflows.

---

## 📦 Open‑Source Repositories

### **1. simulation-util**  
A foundational library for **reproducible Monte Carlo simulation**, random number generation, and distribution utilities.

🔗 https://github.com/risquanter/simulation-util

Key capabilities include:

- High‑quality random number generation (HDR RNGs)
- Metalog distribution utilities
- Reproducible sampling pipelines
- Building blocks for scalable risk aggregation engines

---

### **2. vague-quantifier-logic**  
A Scala 3 implementation of **first‑order logic with vague quantifiers**, translated and extended from academic work by Harrison, Fermüller, and others.

🔗 https://github.com/risquanter/vague-quantifier-logic

Features:

- Fully typed, extensible Scala 3 implementation of first‑order logic formulas and model semantics  
- Support for vague quantifiers such as *“most”*, *“about half”*, *“at least 3/4”*  
- Probabilistic semantics for evaluating vague statements  
- Example domain: cybersecurity risk reasoning  

---

## 🎯 Vision

Risquanter is designed for practitioners who need:

- **Transparent and auditable** risk models  
- **Reproducible** simulation workflows  
- **Composable** risk hierarchies and aggregation logic  
- **Mathematically grounded** semantics for uncertainty and vagueness  
- **Industrial‑grade engineering** with functional programming principles

Our long‑term goal is to provide a commercial‑grade risk registry with first‑class quantitative analytics support, featuring:

- Risk trees with SIPmath‑compatible nodes  
- First‑class support for risk aggregation and analytics  
- Loss exceedance curve generation  
- Scenario modeling and stress testing  
- Domain‑specific logic for risk reasoning  
- High‑performance simulation engines  
- Querying with vague quantifiers  

---

## 🤝 Contributing

We are currently in the process of open‑sourcing existing libraries, and the contribution guidelines are not yet finalized.  
Please reach out to **danago@risquanter.com** before opening a pull request to discuss contribution options.

---

## 📜 License

Each repository contains its own license information.  
Low‑level libraries that implement or directly build on scientific papers are typically licensed under Apache 2.0.  
Advanced risk‑analytics functionality is licensed under AGPL.

If you need a business license or custom functionality, please contact **danago@risquanter.com**.  
We are generally open to business relicensing in individual cases and to custom software development related to our platform.

---

## 📬 Contact

For questions, collaboration, or research discussions, please reach out to **danago@risquanter.com**.

---

*Risquanter — advancing the state of simulation‑based risk analytics.*
