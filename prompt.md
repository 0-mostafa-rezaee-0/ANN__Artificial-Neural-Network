# Comprehensive MNIST ANN Project Development Prompt

I need your help to develop a comprehensive Artificial Neural Network (ANN) project for MNIST digit recognition. I've already set up a basic Docker project template with the following directory structure:

```
.
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── start.sh
├── data/
├── figures/
├── notebooks/
├── models/
└── scripts/
```

Please help me transform this template into a complete MNIST digit recognition project by following these steps:

## 1. Project Setup and Environment
1. First, examine the Dockerfile and docker-compose.yml to understand the existing environment.
2. Update the docker-compose.yml service name to be "mnist-ann-project" instead of "data-science-project".
3. Review and update requirements.txt to include necessary packages: numpy, pandas, matplotlib, tensorflow, scikit-learn, and seaborn.
4. After these changes, commit them: `git add . && git commit -m "chore: Update project configuration for MNIST ANN"` and push: `git push origin main`.

## 2. Scripts Development
Create three key scripts in the scripts/ directory:

1. **data_prep.py**: 
   - Download the MNIST dataset using TensorFlow/Keras
   - Process the data (normalize, reshape to vectors)
   - Save processed data to data/mnist/ directory
   - DO NOT include the actual mnist/ folder in git (the X_train.npy is too large)

2. **extract_sample_images.py**:
   - Extract sample images from the MNIST dataset
   - Create a grid visualization showing examples of each digit
   - Save individual samples to data/mnist_samples/ folder (20 examples for each digit)
   - Create mnist_samples.csv with features

3. **train_ann.py**:
   - Build an ANN with multiple hidden layers and dropout
   - Train the model with early stopping
   - Generate visualizations (confusion matrix, training history, predictions)
   - Save trained models to models/ directory

Make all scripts executable with chmod +x. After creating these scripts, commit them: `git add scripts/ && git commit -m "feat: Add core ANN scripts for MNIST processing and training"` and push: `git push origin main`.

## 3. Documentation and Figures
For each directory, create detailed README.md files:

1. **Root README.md**:
   - Project overview, table of contents, prerequisites
   - Detailed sections for dataset, ANNs, implementation, running instructions

2. **data/README.md**:
   - Explain the data structure (mnist_samples only, not mnist)
   - Describe sample generation process

3. **figures/README.md**:
   - Document visualization types (mnist_samples.png, training_history.png, etc.)

4. **models/README.md**:
   - Describe the model architecture, performance metrics

5. **scripts/README.md**:
   - Explain each script's purpose and usage

After creating these README files, commit them: `git add */README.md README.md && git commit -m "docs: Add comprehensive documentation for all project components"` and push: `git push origin main`.

## 4. Jupyter Notebook Development
Create a comprehensive notebook (ANN_MNIST-data.ipynb) in the notebooks/ directory that:

- Contains detailed markdown explanations of each step
- Walks through data loading, exploration, preprocessing
- Implements and trains the ANN model
- Evaluates and visualizes results
- Includes plots of sample digits, training history, and confusion matrix

After creating this notebook, commit it: `git add notebooks/ && git commit -m "feat: Add interactive Jupyter notebook for MNIST ANN implementation"` and push: `git push origin main`.

## 5. Data and Sample Generation
Run the scripts to generate samples and visualizations:

1. Run data_prep.py to prepare the dataset (but don't commit the large files)
2. Run extract_sample_images.py to generate the mnist_samples directory
3. Add the mnist_samples directory to git but NOT the mnist directory
4. Commit the sample data: `git add data/mnist_samples/ && git commit -m "feat: Add MNIST digit samples for visualization"` and push: `git push origin main`.

## 6. Visualization Generation
Create visualizations through the scripts and notebook:

1. MNIST samples grid showing examples of each digit (mnist_samples.png)
2. Training history plots showing accuracy and loss curves
3. Confusion matrix for model evaluation
4. Sample predictions visualization showing correct/incorrect classifications

Add these visualizations to the figures/ directory and commit: `git add figures/ && git commit -m "feat: Add visualizations for model training and evaluation"` and push: `git push origin main`.

## 7. Final Review and Cleanup
1. Make sure all Docker configurations are properly set up
2. Remove any unnecessary files or images (e.g., old Docker-related images)
3. Ensure .gitignore excludes the data/mnist folder with large files
4. Verify all scripts run correctly within the Docker container
5. Make final documentation updates

Commit these changes: `git add . && git commit -m "refactor: Final project cleanup and optimization"` and push: `git push origin main`.

## 8. Make sure to handle potential Git LFS issues
If you encounter issues pushing large files:
1. Remove large files from git tracking: `git rm --cached data/mnist/*.npy`
2. Update .gitignore to exclude these files
3. Commit these changes: `git add .gitignore && git commit -m "chore: Update .gitignore to exclude large data files"`
4. Force push if necessary: `git push -f origin main`

Please provide detailed explanations throughout the process, and make sure each component is well-documented with appropriate READMEs. The final project should be a professional, well-structured implementation of an ANN for MNIST digit recognition, with comprehensive documentation and visualizations. 