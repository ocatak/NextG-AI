# Chapter-4

This chapter contains scripts and notebooks for signal processing and wireless communications using Python.

**⚠️ Important: Make sure you are in the `Chapter-4` directory before running any commands or scripts.**

## Requirements

- Python 3.10 (recommended for better package compatibility)
- Conda environment: chapter4

## Installation

1. Create the conda environment:
   ```bash
   conda create -n chapter4 python=3.10
   ```

2. Activate the environment:
   ```bash
   conda activate chapter4
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Environment Setup

### Option 1: Using Conda (Recommended)

1. Navigate to the Chapter-4 directory:
   ```bash
   cd Chapter-4
   ```

2. Create a new conda environment with Python 3.10:
   ```bash
   conda create -n chapter4 python=3.10 -y
   ```

3. Activate the environment:
   ```bash
   conda activate chapter4
   ```

4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Option 2: Using venv

1. Navigate to the Chapter-4 directory:
   ```bash
   cd Chapter-4
   ```

2. Create a virtual environment:
   ```bash
   python -m venv chapter4
   ```

3. Activate the environment:
   ```bash
   source chapter4/bin/activate  # On Windows, use `chapter4\Scripts\activate`
   ```

4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Code

The chapter contains two Python scripts:

1. `ex01.py`: Channel estimation with adversarial attacks
   - Implements CNN-based channel estimation
   - Includes defensive distillation
   - Demonstrates various adversarial attacks (FGSM, BIM, MIM, PGD)
   - Generates performance comparison tables and plots

To run the examples:

```bash
# Make sure your environment is activated
cd ..
python ./Chapter-4/ex01.py  # For channel estimation
```

**📝 Note: The `create_models=True` parameter in the code means it will train and create new models. After the first run when models are created, you can change this to `create_models=False` to load existing models instead of retraining them.**

The signal processing script will generate a plot showing:
1. The original signal
2. Its Fourier transform
3. Wavelet transform coefficients

Results will be saved as 'signal_processing_results.png' in the current directory.

## Notes

- All examples require the base requirements from the root `requirements.txt`
- Additional signal processing packages are included in the chapter's `requirements.txt`
- Make sure you have sufficient disk space for any datasets that will be downloaded
- Some examples may require GPU for faster execution

## Troubleshooting

If you encounter any issues:

1. Make sure your environment is activated
2. Verify all requirements are installed correctly
3. Check if you have the correct Python version (3.10 recommended)
4. For GPU-related issues, ensure you have the correct CUDA version installed 