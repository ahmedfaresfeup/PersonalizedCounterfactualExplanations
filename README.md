# prototype
Python version 3.9.22
TensorFlow version: 2.14.1
NumPy version: 1.26.4
scikit-learn version: 1.6.1
Alibi version: 0.9.7.dev0
Keras version: 2.14.0
## Current logical limitations
Methods "regular_gan","countergan", "root-to-leaf" only consider mutable feature in the last stage which does not guarntee the prediction of the counterfactuals

## Objective

Benchmark different methods for generating counterfactual explanations on the German Credit dataset. It evaluates the performance of various counterfactual generation techniques, including GAN-based methods and decision tree-based methods, by comparing their effectiveness using several metrics.

Simulate user interaction cases and reevaluate the benchmark.

Enrich evaluation metrics by evaluating based on personalizing explanation (possibility to adapt according to possible changes like select features, drop features, and/or modify values).



### Key Steps:

1. **Data Preprocessing**:
   - Load and preprocess the German Credit dataset.
   - Encode categorical variables and split the data.

2. **Train Classifier**:
   - Train a Decision Tree classifier.
   - Save the trained classifier.

3. **Autoencoder for Density Estimation**:
   - Train an autoencoder to estimate data density.
   - Compute reconstruction errors.

4. **GAN-based Counterfactuals**:
   - Train a CounterGAN model to generate counterfactuals.
   - Measure latency and compute metrics.

5. **Decision Tree Counterfactuals**:
   - Generate counterfactuals using decision tree branches.
   - Measure latency and compute metrics.

6. **Benchmarking**:
   - Compare methods using metrics like prediction gain, reconstruction error, sparsity, and latency.
   - Summarize results in a benchmark table.

The notebook aims to evaluate the realism, actionability, and computational efficiency of different counterfactual generation techniques.
