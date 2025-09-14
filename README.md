# Introduction to the Mathematics of Deep Learning

This repository contains **teaching materials** for an **introductory lecture on the mathematics of deep learning**.  
It includes **Python code, Jupyter notebooks, and lecture slides (PowerPoint)** to illustrate key concepts.

⚠️ **Note:** The **lecture slides are in Finnish**, but all **code, comments, and notebooks are in English**.

---

## Contents

* 📂 **Code & Notebooks**
  * Implementations of **linear** and **cubic regression** trained with **stochastic gradient descent (SGD)**.
  * Step-by-step visualization of the training process (loss curves, fitted models).
  * Examples of **forward passes, normalization, gradients, and updates** written in simple Python/Numpy.

* 📂 **Lecture Slides**
  * PowerPoint presentations introducing the **mathematical foundations**.
  * Covers: normalization, gradient descent, loss functions, chain rule, and regression as a gateway to neural networks.
  * 👉 [View the slides on Google Drive](https://docs.google.com/presentation/d/14CdQiG8_UYPg4KA66as-vNcHxabm1BgV/edit?usp=sharing&ouid=113483489228822183710&rtpof=true&sd=true)


---

## Repository Structure

```

lecture-materials/
│
├── notebook/
│   └── height_prediction_demo.ipynb
│
├── slides/
│   ├── lecture.pdf
│   └── lecture.pptx
│
└── README.md

```

---

## Models in Code

* **Linear Model**

$$
\hat{y} = w x + b
$$

* **Cubic Model**

$$
\hat{y} = w_1 x + w_2 x^2 + w_3 x^3 + b
$$

Both trained with **vanilla gradient descent**.

---

## Mathematics

### Normalization

Inputs and outputs are standardized with **z-score normalization**:

$$
x_{norm} = \frac{x - \mu}{\sigma}, \qquad y_{norm} = \frac{y - \mu}{\sigma}
$$

### Loss Function

Training minimizes the **Mean Squared Error (MSE)**:

$$
\mathcal{L}_{\text{MSE}} = \frac{1}{N} \sum_{i=1}^{N} (\hat{y}_i - y_i)^2
$$

### Gradients via Chain Rule

For the cubic model:

$$
\hat{y} = w_1 x + w_2 x^2 + w_3 x^3 + b, \quad e = \hat{y} - y
$$

$$
\frac{\partial \ell}{\partial w_1} = 2 e x, \quad
\frac{\partial \ell}{\partial w_2} = 2 e x^2, \quad
\frac{\partial \ell}{\partial w_3} = 2 e x^3, \quad
\frac{\partial \ell}{\partial b} = 2 e
$$

---

## Learning Objectives

* Understand **how gradient descent works** at the mathematical level.  
* Learn to derive gradients step by step using the **chain rule**.  
* Recognize the basic components of gradient-based **deep learning optimization**.  
* Observe in real time how training updates the model parameters and how this shapes the **loss landscape** and training dynamics.  

---

## How to Use

1. Open the Jupyter notebooks to run the code interactively.
2. Watch the training process step by step (with visual plots).
3. Follow along with the **PowerPoint slides (Finnish)** for mathematical explanations.
4. Compare the performance of **linear vs cubic models**.

---

## Further Resources / Advanced Reading

* *Neural Networks: Zero to Hero* by Andrej Karpathy — [Link to YouTube Playlist](https://youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ&si=F3IJ0zJCk7u9OwVg)
* *Neural Networks and Deep Learning* by Andrew Ng — [Link to YouTube Playlist](https://youtube.com/playlist?list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&si=M0-lH20djjDZpGuZ)
  
---

## License

Free to use for **educational purposes**. Attribution is appreciated when reusing in your own teaching.

---

## Author & University

**Author:** Mikko Saukkoriipi  
**University:** Aalto University  
**Date:** 2025-09-14