# NSSVM Python Implementation

This repository contains the Python implementation of the Nonlinear Sparse Support Vector Machine (NSSVM), which is designed for large and sparse datasets. This implementation aims to efficiently optimize a hyperplane to maximally separate two classes, emphasizing sparsity in the solution.

## Features

- Implements the NSSVM algorithm for efficient data classification.
- Handles both dense and sparse data formats seamlessly.
- Includes Jupyter notebooks for easy demonstration and comparison with regular SVMs.

## Quick Start

You can quickly start experimenting with the NSSVM algorithm by accessing Google Colab notebooks:

- [<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" align="left"/>](https://colab.research.google.com/drive/1R36dSVg-jNKD5luLzWQmYLm07Id7jGfK?usp=sharing)  
  **NSSVM Notebook**, explore the implementation and functionality of the Nonlinear Sparse Support Vector Machine tailored for large and sparse datasets.

- [<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" align="left"/>](https://colab.research.google.com/drive/1gUzm_euQRMJ7glNz212Ykw8d2UAgu7AG?usp=sharing)  
  **Regular SVMs for Comparison**, compare the performance of NSSVM against standard SVMs to evaluate improvements in handling sparse data.

## Results

### Test set accuracy

| Dataset | LibSVM | Linear SVM | Our NSSVM |
| ------- | ------ | ---------- | --------- |
| a5a     | 84.72% | 85.41%     | 79.33%    |
| a6a     | 84.68% | 85.06%     | 78.77%    |
| a7a     | 83.09% | 84.06%     | 78.25%    |
| a8a     | 84.74% | 85.81%     | 83.98%    |
| a9a     | 84.56% | 84.77%     | 79.82%    |

### Training set accuracy

| Dataset | LibSVM | Linear SVM | Our NSSVM |
| ------- | ------ | ---------- | --------- |
| a5a     | 86.64% | 84.83%     | 79.20%    |
| a6a     | 86.94% | 85.06%     | 78.36%    |
| a7a     | 87.32% | 85.51%     | 79.46%    |
| a8a     | 87.65% | 85.77%     | 84.59%    |
| a9a     | 86.99% | 85.42%     | 79.28%    |

### Significant time advantage ( in seconds)

| Dataset | LibSVM | Linear SVM | NSSVM |
| ------- | ------ | ---------- | ----- |
| a9a     | 19.59  | 0.56       | 0.05  |
| a7a     | 21.54  | 1.72       | 0.08  |
| a8a     | 2.74   | 0.67       | 0.23  |
| a6a     | 36.47  | 0.70       | 0.10  |
| a5a     | 39.91  | 2.84       | 0.12  |

## Analysis

1. **Accuracy Comparison**:

   - Across multiple datasets (a5a, a6a, a7a, a8a, a9a), NSSVM's accuracy is consistently slightly lower compared to traditional SVM implementations (LibSVM and linear SVM).
   - The accuracy difference between NSSVM and the other methods is marginal, typically within a few percentage points.

2. **Time Advantage**:

   - NSSVM demonstrates a significant time advantage in training compared to both LibSVM and linear SVM across all datasets.
   - Training times for NSSVM are notably lower, indicating its efficiency in computational resource utilization.

3. **Tradeoff Analysis**:

   - Despite a slight sacrifice in accuracy, NSSVM's substantial reduction in training time suggests a favorable tradeoff.
   - The tradeoff between accuracy and training time makes NSSVM a compelling choice, especially in time-sensitive applications where computational efficiency is crucial.

4. **Robustness and Generalization**:
   - NSSVM's consistent performance across different datasets suggests robustness and generalization capabilities.
   - While NSSVM may not always achieve the highest accuracy, its stable performance across diverse datasets underscores its reliability.

In summary, NSSVM's key highlight is its ability to offer significantly faster training times with minimal loss in accuracy compared to traditional SVM implementations. This time advantage positions NSSVM as a promising option for time-sensitive applications, where computational efficiency is paramount.

## Datasets

The following datasets are included in the repository for easy access and testing:

- **a5a, a6a, a7a, a8a, a9a**: Standard datasets commonly used for benchmarking classification models.
- **Sonar, Mines vs. Rocks**: Dataset for distinguishing between sonar signals bounced off a metal cylinder and those bounced off a roughly cylindrical rock.
- **Iris**: Famous dataset for multi-class classification featuring three types of Iris plants.
- **dhrb data**: Custom dataset.

## Usage

To get started with the local setup:

```bash
git clone https://github.com/pavan98765/NSSVM_python.git
cd NSSVM_python
```

### Notebooks

Explore the following Jupyter notebooks to understand and interact with the NSSVM algorithm:

- [**NSSVM Notebook**](./nssvm.ipynb): Demonstrates the python implementation of NSSVM on various datasets. Useful for training and evaluating the model effectively.
- [**Regular SVM Comparison Notebook**](./regular_svm_on_datasets.ipynb): Compares the performance of LibSVM and Linear SVM with NSSVM using the same datasets. Useful for understanding the relative advantages of NSSVM.

These notebooks are designed to provide practical insights and hands-on experience with both NSSVM and traditional SVM techniques.

## Resources

- [NSSVM Paper on IEEE](https://ieeexplore.ieee.org/document/9415153)
- [Original NSSVM MATLAB Implementation on GitHub](https://github.com/ShenglongZhou/NSSVM)

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests with your proposed changes.

### Thank you!
