# MAGIC Gamma Telescope Data Classification

## Project Overview

This project aims to classify signals captured by the MAGIC (Major Atmospheric Gamma Imaging Cherenkov Telescope) into gamma (signal) or hadron (background noise caused by cosmic rays in the atmosphere). High-energy gamma rays provide insights into astrophysical phenomena, such as supermassive black holes, neutron stars, and supernovae. The ability to accurately differentiate between gamma and hadron signals is crucial for such studies.

## Dataset Description

The dataset originates from the MAGIC gamma telescope project and simulates the registration of gamma particles. Observations are patterns formed by Cherenkov photons on photomultiplier tubes, termed as 'shower images'. These images aid in distinguishing between primary gamma-induced showers and background noise. 

Attributes include:
- **fLength:** Major axis of the ellipse representing the "shower image".
- **fWidth:** Minor axis of the ellipse.
- **fSize:** Logarithmic representation of the sum of the content of all image pixels.
- **fConc:** Ratio representing the sum of the two brightest image spots over total brightness.
- **fConc1:** Ratio of the brightest image spot over total brightness.
- **fAsym:** Distance from the brightest spot to the image center, projected onto the major axis.
- **fM3Long:** Third root of the third moment along the major axis.

The dataset's labels are:
- **g (gamma):** Represents signal.
- **h (hadron):** Represents background noise.

## Workflow

1. **Data Loading and Exploration:** The dataset was loaded, and an initial exploration was conducted to understand its structure and content.
2. **Data Preprocessing:** 
    - Column names were assigned.
    - The 'class' column was encoded into binary values (g->1, h->0).
    - The dataset was split into training, validation, and testing sets.
3. **Data Visualization:** Histograms were plotted for each feature against the class to understand the data distribution.
4. **Data Scaling and Balancing:** 
    - Standard scaling was applied to bring all features to the same scale.
    - Random over-sampling was applied to handle class imbalance in the training set.
5. **Model Selection:** I have choose to go with k-Nearest-Neighbors (KNN) algorithm, suitable for the classification nature of the dataset.

---

Feedback, bug reports, and contributions are welcome!

---