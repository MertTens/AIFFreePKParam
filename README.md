# AIF-Free PK Parameter Estimation in DCE-MRI

This repository contains code for a novel machine learning approach to estimate PK parameters and the Arterial Input Function (AIF) directly from measured contrast-time curves in Dynamic Contrast-Enhanced MRI (DCE-MRI). The approach is designed to enhance the accuracy and reliability of PK parameter estimation without the need for explicit AIF measurement.

## Overview

The project leverages two neural networks:
- **AIF Network:** Learns the AIF that generated the contrast-time curves.
- **PK Parameter Network:** Estimates Ktrans and Kep associated with the first contrast-time curve.

### Key Steps
1. **Initial Training:** The AIF network is trained on population average AIF data.
2. **Joint Training:** Both networks are trained together using the Tofts model to minimize the error between the predicted and actual contrast-time curves.
3. **Advanced Training:** Multiple runs of the networks are performed with swapped inputs, and the best predictions are selected for backpropagation.

### Future Research
The next steps include refining the model by selecting the AIF and PK parameter combination with the best loss during multiple runs, rather than relying on averaging.

## Usage
Run the ipynb in google colab

Please email alex.mertens@mail.utoronto.ca if there are questions are issues
