 This project implements a machine learning pipeline to predict heart disease using the UCI Heart Disease dataset. It includes data preprocessing, feature selection, PCA, supervised and unsupervised learning, hyperparameter tuning, and a Streamlit UI for real-time predictions, deployed via Ngrok.

 ## Project Structure
 - `data/`: Contains raw and processed datasets (`heart_disease.csv`, `cleaned_heart_disease.csv`, etc.).
 - `notebooks/`: Jupyter notebooks for each step (preprocessing, PCA, etc.).
 - `models/`: Saved model (`final_model.pkl`).
 - `ui/`: Streamlit app (`app.py`).
 - `deployment/`: Ngrok setup instructions (`ngrok_setup.txt`).
 - `results/`: Model evaluation metrics (`evaluation_metrics.txt`).
 - `requirements.txt`: Python dependencies.
 - `.gitignore`: Files/folders to ignore in Git.

 ## Setup Instructions
 1. **Clone the repository**:
    ```bash
    git clone <repository_url>
    cd Heart_Disease_Project
    ```
 2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
 3. **Run notebooks**:
    - Open Jupyter: `jupyter notebook`
    - Execute notebooks in order (01_data_preprocessing.ipynb to 06_hyperparameter_tuning.ipynb).
 4. **Run Streamlit app**:
    ```bash
    streamlit run ui/app.py
    ```
 5. **Deploy with Ngrok**:
    - Install Ngrok: `pip install pyngrok`
    - Run: `ngrok http 8501`
    - Copy the public URL from Ngrok output to access the app.

 ## Dataset
 - UCI Heart Disease dataset (fetched via `ucimlrepo`, id=45).
 - Features: age, sex, cp, trestbps, chol, etc.
 - Target: Binary (0 = no disease, 1 = disease).

 ## Usage
 - Run preprocessing to generate cleaned datasets.
 - Use PCA and feature selection for dimensionality reduction.
 - Train and evaluate models (Logistic Regression, Random Forest, etc.).
 - Use `app.py` for interactive predictions.
 - Check `evaluation_metrics.txt` for model performance.

 ## Ngrok Deployment
 - See `deployment/ngrok_setup.txt` for detailed steps.
 - Example: Run `ngrok http 8501` and share the public URL.

 ## Requirements
 See `requirements.txt` for Python packages.

 ## Notes
 - Ensure Python 3.8+ is installed.
 - Some visualizations require a graphical interface (e.g., matplotlib).
 - For real-time predictions, input raw feature values in the Streamlit UI (preprocessing handled internally).ogl
