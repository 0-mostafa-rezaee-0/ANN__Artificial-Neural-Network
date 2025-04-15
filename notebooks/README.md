<div align="center">
  <h1>MNIST Jupyter Notebooks</h1>
</div>

# Table of Contents 
<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-overview"><i><b>1. Overview</b></i></a>
</div>
&nbsp;

<details>
  <summary><a href="#2-notebooks"><i><b>2. Notebooks</b></i></a></summary>
  <div>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#21-ann_mnist-dataipynb">2.1. ANN_MNIST-data.ipynb</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#22-exploratory_analysisipynb">2.2. exploratory_analysis.ipynb</a><br>
  </div>
</details>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-running-the-notebooks"><i><b>3. Running the Notebooks</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#4-notebook-dependencies"><i><b>4. Notebook Dependencies</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#5-best-practices"><i><b>5. Best Practices</b></i></a>
</div>
&nbsp;

# 1. Overview

This directory contains Jupyter notebooks for the MNIST digit recognition project. These notebooks provide an interactive environment to explore the dataset, visualize the data, build and train the Artificial Neural Network (ANN) model, and evaluate its performance.

# 2. Notebooks

## 2.1. ANN_MNIST-data.ipynb

This is the main notebook for the project, covering the entire machine learning pipeline:

1. **Setup and Import**: Loading necessary libraries and setting up the environment
2. **Data Loading and Exploration**: Downloading and exploring the MNIST dataset
3. **Data Preprocessing**: Normalizing and reshaping the data for neural network training
4. **Model Building**: Creating the ANN architecture with multiple hidden layers and dropout
5. **Model Training**: Training the model with early stopping and checkpointing
6. **Evaluation**: Assessing model performance using accuracy metrics and confusion matrix
7. **Visualization**: Generating plots for training history and prediction examples

## 2.2. exploratory_analysis.ipynb

This notebook contains additional exploratory data analysis:
- Basic environment verification
- Simple examples of Python data analysis

# 3. Running the Notebooks

To run these notebooks:

1. Ensure the Docker container is running:
   ```bash
   docker-compose up -d
   ```

2. Access Jupyter via browser:
   ```
   http://localhost:8888
   ```

3. Navigate to the `notebooks` directory and open the desired notebook

Alternatively, you can connect VS Code to the running container and open the notebooks directly in VS Code's Jupyter extension.

# 4. Notebook Dependencies

The notebooks depend on the following Python libraries (installed in the Docker container):
- TensorFlow 2.15.0
- NumPy 1.26.0
- Pandas 2.1.3
- Matplotlib 3.8.0
- Scikit-learn 1.3.2
- Seaborn 0.13.0

# 5. Best Practices

When working with these notebooks:

- Execute cells in order to avoid dependency issues
- Use the kernel selector to ensure you're using the container's Python kernel
- Save your work regularly
- Consider creating copies before making significant changes
- For large changes, consider developing in a new branch 