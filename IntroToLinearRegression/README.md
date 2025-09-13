# Intro Linear Regression (Single Variable) – Notebook Overview

## 1. Purpose
This Jupyter notebook (`Intro_Linear_Regression.ipynb`) demonstrates the core mechanics of univariate linear regression using a tiny synthetic housing dataset. It mirrors the early conceptual steps often seen in foundational machine learning courses (e.g., Andrew Ng’s Machine Learning course on Coursera) without reusing proprietary course material.

## 2. Contents Walkthrough
1. Imports  
   - `numpy` for numerical operations  
   - `matplotlib.pyplot` for plotting  
   - Applies a custom Matplotlib style:  
     ```python
     plt.style.use('./deeplearning.mplstyle')
     ```
2. Dataset Definition  
   - `x_train = [1.0, 2.0]` (house sizes in 1000 sqft)  
   - `y_train = [300.0, 500.0]` (prices in $1000s)  
   - Demonstrates shape inspection and indexing.
3. Visualization (Scatter Plot)  
   - Plots raw points to show an approximately linear relationship.
4. Parameter Initialization  
   - Chooses simple illustrative parameters: `w = 200`, `b = 100`.
5. Model Function  
   - Computes predictions: \( f(x^{(i)}) = w x^{(i)} + b \)  
   - Time complexity: O(m). (Could be vectorized: `f_wb = w * x + b`.)
6. Line Fit Plot  
   - Overlays model line against true data.
7. Example Inference  
   - Predicts price for `x = 3.85` (≈1200 sqft):  
     ```
     w * 3.85 + b = 870 (thousand dollars)
     ```

## 3. Key Concepts Illustrated
- Basic data representation (NumPy arrays)
- Linear hypothesis function
- Parameter interpretation (slope/intercept)
- Manual forward pass (no optimization yet)
- Visualization for intuition

## 4. Custom Matplotlib Style (`deeplearning.mplstyle`)
This style centralizes consistent plot aesthetics used across educational notebooks.

Notable settings:
- Line aesthetics: `lines.linewidth: 4`, crisp high-contrast visuals.
- Color cycle (hex, no '#'):  
  - Aqua `0096FF`, Orange `FF9300`, Magenta `FF40FF`, Purple `7030A0`, Dark Red `C00000`.
- Axis + figure:
  - White backgrounds: `axes.facecolor: ffffff`, `figure.facecolor: ffffff`
  - Grid disabled for minimalism.
  - Thicker edges: `axes.linewidth: 3.0`
- Legend styling: `legend.fancybox: true`
- Fonts: Sans‑serif (Verdana preferred), compact base size `8.0` for dense educational layouts.
- Ticks hidden (sizes set to 0) to reduce chart ink.
- SVG text rendered as paths (`svg.fonttype: path`) for portability.
- Emphasis on color-driven differentiation instead of grid lines.

How to use in other notebooks:

import matplotlib.pyplot as plt plt.style.use('./deeplearning.mplstyle')

## 5. Running the Notebook

python -m venv .venv

## 6. Possible Extensions
- Add cost function (MSE)
- Implement gradient descent
- Vectorize `compute_model_output`
- Add residual plot
- Expand dataset to observe under/overfitting

## 7. Citation (Coursera Machine Learning Course)
If this notebook is used in the context of learning inspired by the referenced course, cite it properly:

Plain text:
Andrew Ng. Machine Learning. Coursera. https://www.coursera.org/learn/machine-learning (accessed 2025-09-11).

BibTeX:

@misc{ng_ml_coursera, title        = {Machine Learning}, author       = {Andrew Ng}, howpublished = {Coursera}, year         = {2025}, note         = {Accessed: 2025-09-13}, url          = {https://www.coursera.org/learn/machine-learning} }

The lab material is interesting to help you understand the material of the course but it is the course material that is truly important. I recommend signing up for the course!

## 8. Disclaimer
This repository’s notebook is an independent educational illustration and does not reproduce proprietary course materials. Adjust or expand responsibly for learning or experimentation.
