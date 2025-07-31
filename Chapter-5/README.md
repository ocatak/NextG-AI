# Chapter-5

This chapter contains scripts and notebooks for **[insert your topic here, e.g., "advanced wireless communication techniques" or "deep learning for signal processing"]**.

**⚠️ Important: Make sure you are in the `Chapter-5` directory before running any commands or scripts.**

## Requirements

- Python 3.10 (recommended for best compatibility)
- Conda environment: `chapter5` (recommended)

## Installation

1. **Create the conda environment:**
   ```bash
   conda create -n chapter5 python=3.10
   ```

2. **Activate the environment:**
   ```bash
   conda activate chapter5
   ```

3. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## Running the Code

- The main script is `ex01.py`.
- On the first run, the script will train and save models if they do not already exist.
- On subsequent runs, it will load the saved models.

To run the main script:
```bash
cd ..
python ./Chapter-5/ex01.py
```

**📝 Note: The `create_models=True` parameter in the code means it will train and create new models. After the first run when models are created, you can change this to `create_models=False` to load existing models instead of retraining them.**

## Notes

- All core dependencies are managed in the root `requirements.txt`.
- Add any Chapter 5-specific dependencies to this chapter's `requirements.txt`.
- Make sure you have sufficient disk space for any datasets that will be downloaded.
- Some examples may require a GPU for faster execution.

## Troubleshooting

If you encounter any issues:
1. Make sure your environment is activated.
2. Verify all requirements are installed correctly.
3. Check if you have the correct Python version (3.10 recommended).
4. For GPU-related issues, ensure you have the correct CUDA version installed.

---
