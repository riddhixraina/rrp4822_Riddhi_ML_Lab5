# rrp4822_Riddhi_ML_Lab5  
**Convolution**

This lab explored the properties and applications of convolutional layers in PyTorch.

---

## **Part 1: Manual 2D Convolution**

**Goal:**  
Implement the 2D convolution operation from scratch.

**Outcome:**  
We built a function using basic tensor loops that accurately replicated the behavior of PyTorch's `nn.Conv2d`.  
The custom convolution function passed all tests, including those involving **stride**, **padding**, and **bias**.

---

## **Part 2: CNN on MNIST**

**Goal:**  
Train a CNN to classify handwritten digits from the MNIST dataset.

**Experiment:**  
Three models were trained with only the **kernel size** changed: **3×3**, **5×5**, and **7×7**.

**Outcome:**  
All models trained successfully.  
The **5×5** and **7×7** kernel models achieved the highest performance, with approximately **98.3% test accuracy**.

---

## **Part 3: Translation Equivariance**

**Goal:**  
Demonstrate that convolutions are *translation equivariant* — shifting the input results in a shifted output feature map.

**Experiment:**  
We compared outputs of the following two computations:

- `Conv(Translate(Input))`  
- `Translate(Conv(Input))`

**Outcome:**  
The experiment confirmed translation equivariance:

- **Stride = 1:**  
  Output shift perfectly matched the input shift  
  Example: input shift **(5, 5)** → output shift **(5, 5)**  
- **Stride = 2:**  
  Output shift scaled by the stride  
  Example: input shift **(6, 6)** → output shift **(3, 3)**

---
