# GA-Stacking for Predictive Maintenance

This repository contains the source code for the project **GA-Stacking for Predictive Maintenance**, which allows you to conduct the experiments described in the accompanying report and slides.

## Project Files

- `ga_stacking_for_ai4i.ipynb`: This notebook is designed for experimenting with the AI4I dataset.
- `ga_stacking_for_time_series_prediction.ipynb`: This notebook is designed for experimenting with the Microsoft Azure Predictive Maintenance (PdM) dataset.
- `slide.pptx` and `report.pdf`: These files include the slides and the report of the project.

## Requirements

The code is best run in a Kaggle environment. However, you can also use Google Colab or run it locally with Jupyter Notebook or Jupyter Lab.

### Dependencies

If you're running the code locally, you'll need to install the following libraries:

```bash
pip install numpy pandas matplotlib seaborn tqdm scikit-learn jupyterlab
```

## Running the Code

### Option 1: Running on Kaggle

1. Log in or register for an account on [Kaggle](https://www.kaggle.com/).
2. Upload the source code files to Kaggle.
3. Run the notebooks from start to finish.

By default, the dataset paths in Kaggle are pre-configured:

```python
telemetry_df = pd.read_csv('/kaggle/input/microsoft-azure-predictive-maintenance/PdM_telemetry.csv')
failures = pd.read_csv('/kaggle/input/microsoft-azure-predictive-maintenance/PdM_failures.csv')
machine_info = pd.read_csv('/kaggle/input/microsoft-azure-predictive-maintenance/PdM_machines.csv')
```

### Option 2: Running on Google Colab

1. **Download the Dataset**: The Microsoft Azure Predictive Maintenance dataset includes 5 files:
   - `PdM_telemetry.csv`
   - `PdM_failures.csv`
   - `PdM_machines.csv`
   - `PdM_maint.csv` (unused)
   - `PdM_errors.csv` (unused)

2. **Upload Dataset in Google Colab**:
   - If using **Google Colab**, upload the dataset files to the Colab environment.
   - Modify the file paths in the notebook to point to the location of these datasets.

   Edit the following lines in the "Dataset" section of the notebook:

   ```python
   telemetry_df = pd.read_csv('/path_to_your_data/PdM_telemetry.csv')
   failures = pd.read_csv('/path_to_your_data/PdM_failures.csv')
   machine_info = pd.read_csv('/path_to_your_data/PdM_machines.csv')
   ```

### Option 3: Running Locally with Jupyter Notebook or Jupyter Lab

1. Install the required dependencies as mentioned above.
2. Launch Jupyter Notebook or Jupyter Lab in the directory containing the `.ipynb` files.

```bash
jupyter notebook
```
or
```bash
jupyter lab
```

3. Open and run the notebooks in order from start to finish.

4. **Update Dataset Paths Locally**:
   If running locally, make sure to provide the correct path to the datasets. You can adjust the following code lines in the "Dataset" section:

   ```python
   telemetry_df = pd.read_csv('path_to_your_local_data/PdM_telemetry.csv')
   failures = pd.read_csv('path_to_your_local_data/PdM_failures.csv')
   machine_info = pd.read_csv('path_to_your_local_data/PdM_machines.csv')
   ```

## Dataset Instructions

### For `ga_stacking_for_ai4i.ipynb`:

Simply run the notebook from start to finish. The AI4I dataset is pre-loaded within the code, so no additional steps are required.

### For `ga_stacking_for_time_series_prediction.ipynb`:

If you’re running this notebook on **Google Colab** or **locally**, make sure to follow these steps:

1. **Download the Dataset**: The Microsoft Azure Predictive Maintenance dataset includes 5 files:
   - `PdM_telemetry.csv`
   - `PdM_failures.csv`
   - `PdM_machines.csv`
   - `PdM_maint.csv` (unused)
   - `PdM_errors.csv` (unused)

2. **For Google Colab**:
   - Upload the dataset files to the Colab environment.
   - Update the dataset paths in the notebook as described above.

3. **For Kaggle**:
   - The dataset paths are pre-configured for Kaggle, so no modifications are necessary.

4. **For Local Runs**:
   - Make sure to update the dataset paths to the correct local directory in the code.

After updating the paths, run the notebook from start to finish.

## Additional Notes

- The default paths are set for Kaggle. If you're using Google Colab or running the code locally, ensure to update the paths to match your environment.
- All code is designed to be run sequentially, so please follow the instructions in the notebook to ensure that the data processing and models are executed properly.
