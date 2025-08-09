# Chapter-2

This chapter contains scripts and notebooks for adversarial attacks and defenses using TensorFlow and CleverHans.

**⚠️ Important: Make sure you are in the `Chapter-2` directory before running any commands or scripts.**

## Requirements

- Python 3.10
- Conda environment: chapter2

## Installation

1. Create the conda environment:
   ```bash
   conda create -n chapter2 python=3.10
   ```

2. Activate the environment:
   ```bash
   conda activate chapter2
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Scripts

To run the adversarial attack scripts, ensure you are in the `Chapter-2` directory and the `chapter2` environment is activated. For example:

```bash
conda activate chapter2
python ex05_CW.py
```

## Notes

- Ensure that the `tqdm` and `ipywidgets` packages are installed for progress bars in Jupyter notebooks.
- The scripts use TensorFlow and CleverHans for generating adversarial examples.

## Environment Setup

### Option 1: Using Conda (Recommended)

1. Navigate to the Chapter-2 directory:
   ```bash
   cd Chapter-2
   ```

2. Create a new conda environment with Python 3.10:
   ```bash
   conda create -n chapter2 python=3.10 -y
   ```

3. Activate the environment:
   ```bash
   conda activate chapter2
   ```

4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Option 2: Using venv

1. Navigate to the Chapter-2 directory:
   ```bash
   cd Chapter-2
   ```

2. Create a virtual environment with the same name as the chapter:
   ```bash
   python -m venv chapter2
   ```

3. Activate the environment:
   ```bash
   source chapter2/bin/activate  # On Windows, use `chapter2\Scripts\activate`
   ```

4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Code

The chapter contains several Python scripts:

- `ex01_FGSM.py`: Fast Gradient Sign Method implementation
- `ex02_BIM.py`: Basic Iterative Method implementation
- `ex03_PGD.py`: Projected Gradient Descent implementation
- `ex04_MIM.py`: Momentum Iterative Method implementation
- `ex05_CW.py`: Carlini & Wagner attack implementation
- `ex06_AT.py`: Adversarial Training implementation
- `ex07_DD.py`: Defensive Distillation implementation

To run any example:

```bash
# Make sure your environment is activated
python ex01_FGSM.py
```

## Notes

- All examples require the base requirements from the root `requirements.txt`
- Additional ML-specific packages are included in the chapter's `requirements.txt`
- Make sure you have sufficient disk space for any datasets that will be downloaded
- Some examples may require GPU for faster execution

## Troubleshooting

If you encounter any issues:

1. Make sure your environment is activated
2. Verify all requirements are installed correctly
3. Check if you have the correct Python version (3.10 recommended)
4. For GPU-related issues, ensure you have the correct CUDA version installed 
