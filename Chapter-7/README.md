# Chapter 7: Transformer Models

This chapter covers transformer model implementations and applications.

**⚠️ Important: Make sure you are in the `Chapter-7` directory before running any commands or scripts.**

## Environment Setup

### Option 1: Using Conda (Recommended)

```bash
# Navigate to Chapter-7 directory
cd Chapter-7

# Create a new conda environment with Python 3.10
conda create -n chapter7 python=3.10 -y

# Activate the conda environment
conda activate chapter7

# Install all required packages
pip install -r requirements.txt
```

### Option 2: Using venv

```bash
# Navigate to Chapter-7 directory
cd Chapter-7

# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
# .\venv\Scripts\activate

# Install all required packages
pip install -r requirements.txt
```

## Running the Code

The chapter contains several Python scripts for transformer model implementations. To run any example:

```bash
# Make sure your environment is activated
# For conda:
conda activate chapter7
# For venv:
source venv/bin/activate  # (macOS/Linux)
# .\venv\Scripts\activate  # (Windows)

# Run the desired script
cd ..
python ./Chapter-7/ex-amr_mimo.py
python ./Chapter-7/ex-amr_mimo_adv_training
```

**📝 Note: The `train_model_param=True` parameter in the code means it will train and create new models. After the first run when models are created, you can change this to `train_model_param=False` to load existing models instead of retraining them.**

## Available Scripts

- `ex-amr_mimo.py`: Main example for MIMO AMR implementation
- `ex-amr_mimo_adv_training.py`: Advanced training with adversarial examples

## Transformer Model Features

The code includes implementations for:
- Transformer architecture
- Pre-trained model fine-tuning
- Text classification
- Sequence-to-sequence tasks
- Model quantization
- Parameter-efficient fine-tuning

## Notes

- All examples require the base requirements from the root `requirements.txt`
- Additional transformer-specific packages are included in the chapter's `requirements.txt`
- GPU is highly recommended for training transformer models
- The code uses the Hugging Face Transformers library
- Make sure you have sufficient disk space for model weights
- Some models may require significant RAM/GPU memory

## Troubleshooting

If you encounter any issues:

1. Make sure your environment is activated
2. Verify all requirements are installed correctly
3. Check if you have the correct Python version (3.10 recommended)
4. For transformer model issues:
   - Ensure you have sufficient GPU memory
   - Check if the model weights are downloaded correctly
   - Verify input data format and tokenization
5. For GPU-related issues:
   - Ensure you have the correct CUDA version installed
   - Check if PyTorch is installed with CUDA support
   - Verify GPU is recognized by PyTorch using `torch.cuda.is_available()`
6. For memory issues:
   - Consider using model quantization
   - Use gradient checkpointing
   - Implement batch processing
   - Enable mixed precision training

## Directory Structure

- `AMR_MIMO/`: Contains MIMO AMR model implementations
- `AMR_SISO/`: Contains SISO AMR model implementations
- `Plots/`: Directory for saving generated plots
- `Plots_AdvRetrain/`: Directory for adversarial training plots
- `Saved_Models/`: Directory for saving trained models
- `Tables/`: Contains data tables and results 