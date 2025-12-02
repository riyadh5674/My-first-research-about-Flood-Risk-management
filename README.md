
# README.md – Flood Probability Prediction: From Blind ML to Physics-Guided Intelligence  

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) [![Python 3.9+](https://img.shields.io/badge/python-3.9%2B-blue)](https://python.org) [![LightGBM](https://img.shields.io/badge/LightGBM-winner-brightgreen)](https://lightgbm.readthedocs.io)



## The Journey – Beginning

This repository started as a simple Kaggle notebook… and ended up proving something beautiful:  
**On real-world physics problems, guiding ML with domain knowledge doesn’t just make sense — it wins.**

### The Dataset  
The famous “Playground Series S4E5” synthetic flood dataset (1,117,957 train + 745,682 test rows) with 20 engineered risk factors and a continuous `FloodProbability` target.

### What Everyone Else Did  
- Throw data into XGBoost/LightGBM  
- Tune hyperparameters  
- Submit → R² ≈ 0.957–0.965  
- Celebrate  

### What We Did Differently (and why it mattered)

| Phase | What We Did | Why It Was Game-Changing | Result |
|------|--------------|--------------------------|--------|
| 1    | Discovered the **single biggest silent killer** of physics-guided models: **StandardScaler + monotonic constraints = disaster** | Scaling destroys the true monotonic relationships | Fixed → instant +0.01 R² jump |
| 2    | Fixed some features **infamous DeterioratingInfrastructure bug** puts +1 instead of -1) also put 0 for InadequatePlanning ,PoliticalFactors | One wrong sign kills the entire physics model | From R² 0.71 → 0.96 overnight |
| 3    | Trained 4 state-of-the-art models **with correct physics constraints** | LightGBM, CatBoost, XGBoost,DecisionTree | LightGBM + physics became the undisputed champion |
| 4    | Proved on **real physics** (Bangladesh BMD data) that the same constraints **still win** | Synthetic success → Real-world validation | AUC 0.9517 (Normal) vs 0.7347 (pysics) |


> **Key Insight:** On real physics, the physics-guided model doesn’t just match — it dominates.

> **Key Insight:** But on synthetic data Physics-guided model doesn't perform well.

### The Golden Rules We Learned (and You Should Never Forget)

```text
1. Never, EVER scale features when using monotonic constraints
2. DeterioratingInfrastructure → +1 (higher = worse = more risk)
3. IneffectiveDisasterPreparedness → +1
4. Use raw integer values — tree models love them
5. LightGBM + correct constraints = unstoppable
```

### For Researchers & Students

This repo is the perfect template for:
- Physics-guided ML papers
- Explainable AI projects
- Teaching “why domain knowledge > more data”

### Citation (if you use this work)

```bibtex
@misc{riyadh56742025floodphysics,
  author = {MD RIYAD},
  title = {When Physics Guides ML: Achieving State-of-the-Art Flood Prediction with Monotonic Constraints},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/your-username/flood-physics-ml}
}
```

<p align="center">
  <b>
    <span style="color:#FF6B6B">Made with</span> 
    <span style="color:#4ECDC4">curiosity</span> 
    <span style="color:#FFE66D">caffeine</span> 
    <span style="color:#95E1D3">and a stubborn belief</span> 
    <span style="color:#FF8B94">that ML should respect reality</span>
  </b>
  <br><br>
  <b><span style="font-size:1.3em;">Star ★ if physics-guided ML makes you smile</span></b>
  <br>
  
</p>
```

