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

### 1. **Risquanter Register — Quantitative Risk Registry**
**An in-progress Quantitative Risk Registry and Monte Carlo simulation engine for hierarchical risk portfolios.**

**Short description:** The `register` repository implements a reproducible, auditable registry for quantitative risk portfolios and a Monte Carlo engine optimized for hierarchical portfolios and sparse trial storage. It is designed for deterministic parallel execution, provenance capture, and composable mitigation primitives suitable for production risk workflows.

**Key capabilities include:**
- **Hierarchical Risk Trees:** Model complex portfolios with nested portfolios and leaves representing individual risk items.
- **Sparse Trial Storage:** Memory‑efficient representation that stores only non‑zero losses per trial to scale large simulations.
- **Deterministic Parallelism:** Reproducible parallel execution using a hierarchical HDR PRNG seed scheme to ensure full reproducibility across runs and environments.
- **Distribution Support:** Expert‑opinion (Metalog) and parametric distributions (e.g., lognormal) with confidence‑interval parameterization and percentile/quantile interfaces.
- **Mitigation Primitives:** Composable transforms such as reduction, deductible, cap, layered coverage, and policy aggregation to model real‑world insurance and mitigation constructs.
- **Provenance & Auditability:** Complete metadata capture for each run, including HDR seed hierarchy and configuration, enabling full audit trails and reproducible results.
- **HTTP API:** Endpoints for submitting portfolio definitions, configuring `nTrials`, running simulations, and retrieving LEC and other metrics with provenance metadata.

**Example portfolio (request body)**
```json
{
  "name": "Cyber Portfolio",
  "root": {
    "type": "portfolio",
    "id": "cyber-root",
    "name": "All Cyber Risks",
    "children": [
      {
        "type": "leaf",
        "id": "ransomware",
        "name": "Ransomware Attack",
        "distributionType": "lognormal",
        "probability": 0.15,
        "minLoss": 50000,
        "maxLoss": 5000000,
        "confidenceInterval": 0.90
      },
      {
        "type": "leaf",
        "id": "data-breach",
        "name": "Data Breach",
        "distributionType": "expert",
        "probability": 0.25,
        "percentiles": [0.1, 0.5, 0.9],
        "quantiles": [10000, 75000, 500000]
      }
    ]
  },
  "nTrials": 10000
}
```


### **2. simulation-util**  
A foundational library for **reproducible Monte Carlo simulation**, random number generation, and distribution utilities.

🔗 https://github.com/risquanter/simulation-util

Key capabilities include:

- High‑quality random number generation (HDR RNGs)
- Metalog distribution utilities
- Foundations for reproducible sampling pipelines
- Building blocks for scalable risk aggregation engines

---

### **3. vague-quantifier-logic**  
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
