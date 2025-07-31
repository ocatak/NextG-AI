# NextG Communications with AI - Setup Guide

This guide provides comprehensive instructions for setting up the development environment for all chapters in the NextG Communications with AI project.

## System Requirements

- **Python**: 3.10 (recommended for best compatibility)
- **Operating System**: macOS, Linux, or Windows
- **Memory**: Minimum 8GB RAM (16GB+ recommended for deep learning)
- **Storage**: At least 10GB free space for datasets and models
- **GPU**: Optional but highly recommended for faster training (CUDA-compatible)

## Quick Start

### 1. Clone the Repository
```bash
git clone <repository-url>
cd NextG-Communications-with-AI
```

### 2. Install Base Dependencies
```bash
# Install the main requirements (used by all chapters)
pip install -r requirements.txt
```

### 3. Chapter-Specific Setup

Each chapter has its own requirements file. You can install them individually or all at once:

#### Option A: Install All Chapter Dependencies
```bash
# Install dependencies for all chapters
pip install -r Chapter-2/requirements.txt
pip install -r Chapter-3/requirements.txt
pip install -r Chapter-4/requirements.txt
pip install -r Chapter-5/requirements.txt
pip install -r Chapter-6/requirements.txt
pip install -r Chapter-7/requirements.txt
```

#### Option B: Install Only Required Chapter Dependencies
```bash
# Navigate to the specific chapter
cd Chapter-X  # Replace X with chapter number

# Install chapter-specific requirements
pip install -r requirements.txt
```

## Virtual Environment Setup (Recommended)

### Using Conda (Recommended)

```bash
# Create environment for specific chapter
conda create -n chapterX python=3.10  # Replace X with chapter number
conda activate chapterX

# Install requirements
pip install -r requirements.txt  # Main requirements
pip install -r Chapter-X/requirements.txt  # Chapter-specific requirements
```

### Using venv

```bash
# Create virtual environment
python -m venv chapterX_env  # Replace X with chapter number

# Activate environment
# On macOS/Linux:
source chapterX_env/bin/activate
# On Windows:
# .\chapterX_env\Scripts\activate

# Install requirements
pip install -r requirements.txt  # Main requirements
pip install -r Chapter-X/requirements.txt  # Chapter-specific requirements
```

## Chapter-Specific Requirements

### Chapter 2: Adversarial Attacks and Defenses
- **Focus**: FGSM, BIM, PGD, MIM, CW attacks
- **Key Dependencies**: cleverhans, tensorflow, keras
- **Setup**: `pip install -r Chapter-2/requirements.txt`

### Chapter 3: Deep Learning for NextG Communications
- **Focus**: DeepMIMO, channel modeling, beamforming
- **Key Dependencies**: DeepMIMO (from GitHub), tensorflow, keras
- **Setup**: 
  ```bash
  pip install -r Chapter-3/requirements.txt
  pip install git+https://github.com/DeepMIMO/DeepMIMO.git
  ```

### Chapter 4: Signal Processing and Channel Estimation
- **Focus**: CNN-based channel estimation, adversarial attacks
- **Key Dependencies**: tensorflow, keras, cleverhans, scipy
- **Setup**: `pip install -r Chapter-4/requirements.txt`

### Chapter 5: Spectrum Sensing and Adversarial Defense
- **Focus**: U-Net models, spectrum sensing, defensive distillation
- **Key Dependencies**: opencv-python, tensorflow, keras
- **Setup**: `pip install -r Chapter-5/requirements.txt`

### Chapter 6: Statistical Analysis and Defensive Distillation
- **Focus**: Statistical analysis, defensive distillation, hypothesis testing
- **Key Dependencies**: statsmodels, scipy, tensorflow, keras
- **Setup**: `pip install -r Chapter-6/requirements.txt`

### Chapter 7: MIMO Systems and LSTM Models
- **Focus**: LSTM models, MIMO systems, adaptive modulation recognition
- **Key Dependencies**: h5py, tensorflow, keras, scipy
- **Setup**: `pip install -r Chapter-7/requirements.txt`

## Running the Code

### General Instructions
1. **Activate your environment**:
   ```bash
   conda activate chapterX  # or source venv/bin/activate
   ```

2. **Navigate to chapter directory**:
   ```bash
   cd Chapter-X
   ```

3. **Run the main script**:
   ```bash
   python ex01.py  # or the specific script for the chapter
   ```

### Chapter-Specific Instructions

#### Chapter 2
```bash
cd Chapter-2
python ex01_FGSM.py    # Fast Gradient Sign Method
python ex02_BIM.py     # Basic Iterative Method
python ex03_PGD.py     # Projected Gradient Descent
python ex04_MIM.py     # Momentum Iterative Method
python ex05_CW.py      # Carlini & Wagner Attack
python ex06_AT.py      # Adversarial Training
python ex07_DD.py      # Deep Defense
```

#### Chapter 3
```bash
cd Chapter-3
python dataset_generator.py  # Generate DeepMIMO dataset
python ex01.py               # Main deep learning experiment
```

#### Chapter 4
```bash
cd Chapter-4
python ex01.py  # Channel estimation with adversarial attacks
```

#### Chapter 5
```bash
cd Chapter-5
python ex01.py  # Spectrum sensing with adversarial defense
```

#### Chapter 6
```bash
cd Chapter-6
python ex01.py  # Statistical analysis and defensive distillation
```

#### Chapter 7
```bash
cd Chapter-7
python ex-amr_mimo.py              # MIMO AMR implementation
python ex-amr_mimo_adv_training.py # Adversarial retraining
```

## Troubleshooting

### Common Issues

1. **Import Errors**
   - Ensure you're in the correct virtual environment
   - Verify all requirements are installed: `pip list`
   - Check Python version: `python --version`

2. **TensorFlow Issues**
   - For macOS: Use `tensorflow-macos` (already in requirements)
   - For GPU support: Install `tensorflow-gpu` instead
   - Check CUDA compatibility if using GPU

3. **Memory Issues**
   - Reduce batch sizes in the code
   - Use smaller datasets for testing
   - Close other applications to free memory

4. **DeepMIMO Issues (Chapter 3)**
   - Ensure you have the correct scenario files
   - Check the DeepMIMO documentation for setup instructions
   - Verify the dataset folder path in the code

5. **Package Version Conflicts**
   - Create a fresh virtual environment
   - Install packages in the order specified in requirements files
   - Use `pip install --upgrade` for specific packages if needed

### Getting Help

1. **Check the chapter-specific README files** for detailed instructions
2. **Review the setup_checker.py** in Chapter-2 for package management
3. **Check the logs** generated by the scripts for error details
4. **Verify your Python version** matches the requirements (3.10 recommended)

## Development Environment

### Recommended IDEs
- **VS Code** with Python extension
- **PyCharm** Professional/Community
- **Jupyter Notebooks** for interactive development

### Code Style
- The project uses standard Python conventions
- Consider using `black` for code formatting (included in requirements)
- Use `flake8` for linting (included in requirements)

## GPU Support (Optional)

For faster training, consider using GPU acceleration:

1. **Install CUDA Toolkit** (if using NVIDIA GPU)
2. **Install cuDNN** (NVIDIA Deep Neural Network library)
3. **Install tensorflow-gpu** instead of tensorflow-macos:
   ```bash
   pip uninstall tensorflow-macos
   pip install tensorflow-gpu==2.13.0
   ```

## Contributing

When adding new dependencies:
1. Update the main `requirements.txt` for shared dependencies
2. Update the chapter-specific `requirements.txt` for chapter-specific dependencies
3. Update this setup guide if needed
4. Test the installation process on a clean environment

## License

This project is licensed under the terms specified in the LICENSE file. 