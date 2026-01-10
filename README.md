cat > README.md << 'EOF'
# Dhofar Load Forecasting

**Physics-Informed Deep Learning for Grid Station Load Forecasting with Total Load Conservation Constraints**

## Project Overview

This project develops an advanced AI model for predicting electricity load across Dhofar's power grid substations, specifically for Nama Dhofar Services. The model integrates:

- **Temporal Fusion Transformer (TFT)** for spatio-temporal learning
- **Physics-informed constraint networks** for load conservation
- **Continual learning** for daily model improvement
- **Multi-horizon forecasting** (hourly, daily, monthly, yearly)
- **Uncertainty quantification** and explainability analysis

## Key Features

- 🔬 Physics-Informed Neural Networks (PINNs)
- 🧠 Transformer-based architecture with attention mechanisms
- 📊 Multi-horizon hierarchical reconciliation
- 🔄 Continual learning with experience replay
- 📈 Probabilistic forecasting with confidence intervals
- 🎯 Conformal prediction for reliability
- 🌍 Transfer learning from Saudi/UAE grids
- 🎨 PyQt6 GUI for production deployment
- 📦 PyInstaller packaging for Windows distribution

## Dataset

- **Duration:** Jan-Jul 2025 (7 months)
- **Substations:** 11 grid substations in Dhofar region
- **Frequency:** Hourly data (24 hours/day)
- **Features:** Load (MW), Temperature, Humidity, Holiday flags
- **Total Records:** ~5,000+ data points

## Project Structure

dhofar-load-forecasting/
├── data/
│ ├── raw/ # Original Excel files
│ └── processed/ # Cleaned, engineered data
├── notebooks/
│ ├── 01_eda.ipynb
│ ├── 02_feature_engineering.ipynb
│ └── 03_model_training.ipynb
├── src/
│ ├── config.py # Configuration constants
│ ├── data_loader.py # Data loading & preprocessing
│ ├── feature_engineering.py
│ ├── models/
│ │ ├── tft.py # TFT model
│ │ ├── constraint_network.py
│ │ └── losses.py
│ ├── training/
│ │ ├── trainer.py # Main training loop
│ │ └── continual_learning.py
│ ├── evaluation/
│ │ ├── metrics.py
│ │ ├── explainability.py
│ │ └── visualization.py
│ └── app/
│ ├── main_window.py # PyQt6 GUI
│ └── backend.py # FastAPI server
├── tests/
│ ├── test_data_loader.py
│ └── test_models.py
├── requirements.txt # Dependencies
├── setup.py
└── README.md


## Installation

```bash
# Clone repository
git clone https://github.com/yourusername/dhofar-load-forecasting
cd dhofar-load-forecasting

# Create virtual environment
python -m venv venv
source venv/Scripts/activate  # Windows

# Install dependencies
pip install -r requirements.txt
