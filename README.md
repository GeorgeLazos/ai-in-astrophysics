# AI in Astrophysics and Space Science

> Eight weeks of applying modern machine learning to real problems in space physics — from classifying alien-world habitability to reconstructing magnetic fields with physics-informed neural networks and flying a spacecraft around the Moon.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific-013243?logo=numpy&logoColor=white)
![Status](https://img.shields.io/badge/MSc-Coursework-8A2BE2)

---

## About

Coursework, experiments, and end-to-end notebooks from the **MSc in AI & Machine Learning — *AI in Astrophysics and Space Science*** module. Each week tackles a different data-science problem that astrophysicists, heliophysicists, or mission engineers actually face: noisy satellite telemetry, sparse in-situ measurements, image-based solar diagnostics, and trajectory design under real orbital dynamics.

Every assignment is self-contained in a single Jupyter notebook with its dataset folder, ready to be run top-to-bottom.

---

## The 8 Assignments

| # | Notebook | Topic | Methods |
|---|----------|-------|---------|
| 1 | [habitable-worlds-bayes](Week1/habitable-worlds-bayes.ipynb) | Predicting exoplanet habitability from the Habitable Worlds Catalogue | Naive Bayes, feature engineering |

| 2 | [solar-wind-classification](Week2/solar-wind-classification.ipynb) | Classifying solar wind as geoeffective vs. non-geoeffective | Supervised classification on OMNI data |

| 3 | [grace-density-prediction](Week3/grace-density-prediction.ipynb) | Predicting thermospheric density from the GRACE satellite | Gaussian Processes + GMM clustering |

| 4 | [radiation-belt-flux](Week4/radiation-belt-flux.ipynb) | Forecasting Van Allen radiation-belt electron flux | Regression with space-weather drivers |

| 5 | [feature-ranking-nam](Week5/feature-ranking-nam.ipynb) | Interpretable feature ranking with Neural Additive Models | NAMs, attribution, model interpretability |

| 6 | [f107-from-euv](Week6/f107-from-euv.ipynb) | Predicting the F10.7 solar index from SDO EUV images | CNNs on multi-channel solar imagery |

| 7 | [magnetic-field-reconstruction-pinn](Week7/magnetic-field-reconstruction-pinn.ipynb) | Reconstructing an unknown **B**-field from a charged particle's trajectory | Physics-Informed Neural Networks (Lorentz force) |

| 8 | [free-return-trajectory](Week8/free-return-trajectory.ipynb) | Designing an Earth–Moon–Earth free-return trajectory | Numerical integration, orbital mechanics, optimisation |

---

## Highlights

- **Real space-physics datasets** — OMNI solar wind, GRACE accelerometer, SDO/EUV imagery, radiation-belt observations.
- **A full ML stack** — from classical Bayesian classifiers and Gaussian Processes to CNNs and PINNs.
- **Physics-aware learning** — Week 7 enforces the Lorentz force equation directly inside the loss function.
- **Mission-style problems** — Week 8 produces a physically consistent free-return trajectory evaluated on closest-Earth-approach after a lunar flyby.

---

## Repository Structure

```
.
├── Week1/   habitable-worlds-bayes.ipynb        + data/
├── Week2/   solar-wind-classification.ipynb     + data/
├── Week3/   grace-density-prediction.ipynb      + data/
├── Week4/   radiation-belt-flux.ipynb           + data/
├── Week5/   feature-ranking-nam.ipynb           + data/
├── Week6/   f107-from-euv.ipynb                 + data/, processed_data/, predictions/
├── Week7/   magnetic-field-reconstruction-pinn.ipynb + best_B_model.weights.h5
└── Week8/   free-return-trajectory.ipynb
```

Datasets are intentionally **not** committed (see [.gitignore](.gitignore)) — folder structure is preserved via `.gitkeep` files. Drop the corresponding files into each `data/` directory before running.

---

## Running the Notebooks

```bash
git clone https://github.com/GeorgeLazos/ai-in-astrophysics.git
cd ai-in-astrophysics

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install jupyter numpy pandas matplotlib scikit-learn tensorflow scipy
jupyter notebook
```

Then open any `WeekN/*.ipynb` and run all cells.

---

## Author

**George Lazo** — MSc AI & Machine Learning

---

## License

Educational use. Datasets belong to their respective providers (NASA, ESA, NOAA, etc.).
