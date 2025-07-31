# Statistical Analysis for NextG Communications

This chapter focuses on statistical analysis techniques for NextG communications, including hypothesis testing, time series analysis, and statistical modeling of communication systems.

**⚠️ Important: Make sure you are in the `Chapter-6` directory before running any commands or scripts.**

## Environment Setup

### Option 1: Using Conda (Recommended)

1. Create a new conda environment with Python 3.10:
   ```bash
   conda create -n chapter6 python=3.10 -y
   ```

2. Activate the environment:
   ```bash
   conda activate chapter6
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Option 2: Using venv

1. Create a virtual environment with the same name as the chapter:
   ```bash
   python -m venv chapter6
   ```

2. Activate the environment:
   ```bash
   source chapter6/bin/activate  # On Windows, use `chapter6\Scripts\activate`
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Code

The chapter contains several Python scripts:

- `ex01.py`: Statistical analysis and modeling implementation
- `util_defdistill.py`: Utility functions for statistical analysis

To run any example:

```bash
# Make sure your environment is activated
cd ..
python ./Chapter-6/ex01.py
```

**📝 Note: The `train_model=True` parameter in the code means it will train and create new models. After the first run when models are created, you can change this to `train_model=False` to load existing models instead of retraining them.**

## Directory Structure

- `ex01.py`: Main script for statistical analysis
- `util_defdistill.py`: Utility functions
- `requirements.txt`: List of required packages
- `Plots/`: Directory containing generated plots and visualizations
- `README.md`: This file, containing setup and usage instructions

## Features

- Statistical hypothesis testing
- Time series analysis
- Distribution fitting
- Statistical modeling of communication channels
- Data visualization using seaborn and matplotlib

## Notes

- All examples require the base requirements from the root `requirements.txt`
- Additional statistics-specific packages are included in the chapter's `requirements.txt`
- Some analyses may require significant computational resources
- Generated plots are saved in the `Plots/` directory

## Troubleshooting

If you encounter any issues:

1. Make sure your environment is activated
2. Verify all requirements are installed correctly:
   ```bash
   pip list | grep -E "statsmodels|scipy|pandas|seaborn"
   ```
3. Check if you have the correct Python version (3.10 recommended)
4. For memory issues, try reducing the dataset size or using batch processing 