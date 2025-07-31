# Deep Learning for NextG Communications

This chapter focuses on deep learning applications in NextG communications, including channel estimation, beamforming, and resource allocation.

**⚠️ Important: Make sure you are in the `Chapter-3` directory before running any commands or scripts.**

## Environment Setup

### Option 1: Using Conda (Recommended)

1. Create a new conda environment with Python 3.10:
   ```bash
   conda create -n chapter3 python=3.10 -y
   ```

2. Activate the environment:
   ```bash
   conda activate chapter3
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Install DeepMIMO:
   ```bash
   pip install git+https://github.com/DeepMIMO/DeepMIMO.git
   ```

### Option 2: Using venv

1. Create a virtual environment with the same name as the chapter:
   ```bash
   python -m venv chapter3
   ```

2. Activate the environment:
   ```bash
   source chapter3/bin/activate  # On Windows, use `chapter3\Scripts\activate`
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Install DeepMIMO:
   ```bash
   pip install git+https://github.com/DeepMIMO/DeepMIMO.git
   ```

## Running the Code

1. Ensure the environment is activated:
   ```bash
   conda activate chapter3  # or source venv/bin/activate
   ```

2. Run the dataset generator:
   ```bash
   c.. 
   python ./Chapter-3/dataset_generator.py
   ```

3. Run the main experiment:
   ```bash
   python ./Chapter-3/ex01.py
   ```

**📝 Note: The `create_models=True` parameter in the code means it will train and create new models. After the first run when models are created, you can change this to `create_models=False` to load existing models instead of retraining them.**

## DeepMIMO Scenario Setup

1. Download a scenario (e.g., 'O1_60'):
   ```bash
   python -c "import deepmimo; deepmimo.download('O1_60')"
   ```

2. If the download fails, check the DeepMIMO documentation for the correct scenario names and download URLs.

3. Use the scenario in your dataset generator:
   ```python
   import deepmimo
   scenario_name = 'O1_60'  # Replace with your scenario name
   parameters = deepmimo.get_params_path(scenario_name)
   dataset = deepmimo.generate_data(parameters)
   ```

## Notes

- Ensure all dependencies are installed in the correct environment.
- Check the DeepMIMO documentation for additional setup instructions.

## Troubleshooting

- If you encounter a `ModuleNotFoundError`, ensure the environment is activated and DeepMIMO is installed.
- If the scenario download fails, verify the scenario name and download URL.

## Directory Structure

- `dataset_generator.py`: Script to generate the dataset using DeepMIMO.
- `requirements.txt`: List of required packages.
- `README.md`: This file, containing setup and usage instructions. 