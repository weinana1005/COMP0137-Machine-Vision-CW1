# COMP0137 Machine Vision CW1
Final Grade: 90/100
- Comments:
  - II-B) Justification of cluster number has slight incorrect reasoning. K should be chosen based on the expected number of color clusters, not the feature dimensionality.
  - II-D,E) Some incorrect ROC curves are produced


# Mixture of Gaussians for Image Classification

This project demonstrates how to use a Gaussian Mixture Model (GMM) to classify image pixels into different categories (e.g., apple vs. non-apple, skin vs. non-skin). It includes:

- **Loading Images and Masks**
  - Reading color images and their corresponding binary mask images (e.g., apples vs. background).
  - Normalizing and preparing image data for further processing.

- **Gaussian Functions**
  - `calcGaussianProb`: Evaluates the likelihood of data under a single Gaussian (mean and covariance).
  - `fixGaussianModel`: Fits a single Gaussian to a set of data points by computing the mean and covariance.

- **Gaussian Mixture Modeling**
  - `mixGaussLikelihood`: Computes the likelihood of data under a mixture of Gaussians.
  - `fitMixGauss`: Implements the Expectation-Maximization (EM) algorithm to fit the GMM parameters (weights, means, and covariances) to the data.

- **Classification with Bayes’ Rule**
  - Uses the learned Gaussian parameters and prior probabilities to compute posterior probabilities for classifying each pixel.

By combining these steps, the project demonstrates basic image segmentation or classification tasks using mixture models. This approach illustrates fundamental techniques in probabilistic modeling, EM optimization, and image processing.

---

## Key Features

1. **Easy Data Loading:** Automated routines for reading image and mask pairs.
2. **Modular Code:** Separate functions for single-Gaussian fitting, mixture likelihood computation, and EM updates.
3. **Pixel-Level Classification:** Demonstrates how to label each pixel based on GMM posterior probabilities.
4. **Extendable:** Easily adaptable to other segmentation or classification tasks by adjusting priors or the number of Gaussian components.

---

## Getting Started

1. **Install Dependencies:**  
   - Required Python libraries: `numpy`, `scipy`, `matplotlib`, `PIL` (or `Pillow`), etc.
2. **Load the Data:**  
   - Place your images in a designated directory and update the file paths in the notebook or script.
3. **Run the Notebook/Scripts:**  
   - Follow the code sections (e.g., Tasks A, B, etc.) to see how data is loaded, models are fitted, and classifications are performed.

---

## Usage

- **Training:**  
  Use the EM algorithm (`fitMixGauss`) to estimate GMM parameters from labeled pixels (e.g., apple vs. non-apple).
  
- **Inference:**  
  Compute the likelihood of new image pixels using `calcGaussianProb` and `mixGaussLikelihood`, then apply Bayes’ rule for classification.



