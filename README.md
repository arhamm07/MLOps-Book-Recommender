# 📚 MLOps Book Recommender System

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B)](https://streamlit.io/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML%20Model-F7931E)](https://scikit-learn.org/)
[![MLOps](https://img.shields.io/badge/MLOps-Enabled-00A98F)](https://ml-ops.org/)

A production-ready book recommendation system built with MLOps best practices, featuring collaborative filtering and an interactive web interface.

## 🚀 Features

- **Collaborative Filtering** using k-Nearest Neighbors
- **End-to-End MLOps Pipeline**
- **Interactive Web Interface** with Streamlit
- **Modular & Scalable Architecture**
- **Configuration Management** with YAML
- **Comprehensive Logging & Error Handling**

## 🏗️ Architecture

```
MLOps-Book-Recommender/
├── artifacts/                  # Stores all generated artifacts
│   ├── dataset/                # Raw and processed datasets
│   ├── serialized_objects/     # Pickle files for model and data
│   └── trained_model/          # Trained recommendation model
├── books_recommender/          # Core package
│   ├── components/             # Pipeline components
│   ├── config/                 # Configuration management
│   ├── constant/               # Constants and paths
│   ├── entity/                 # Configuration entities
│   ├── exception/              # Custom exceptions
│   ├── logger/                 # Logging configuration
│   ├── pipeline/               # Training pipeline
│   └── utils/                  # Utility functions
├── config/                     # Configuration files
├── logs/                       # Application logs
├── app.py                      # Streamlit web application
├── main.py                     # Training pipeline entry point
└── requirements.txt            # Python dependencies
```

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/MLOps-Book-Recommender.git
   cd MLOps-Book-Recommender
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🚦 Usage

### 1. Run the Training Pipeline
```bash
python main.py
```

### 2. Start the Web Application
```bash
streamlit run app.py
```

### 3. Using the Web Interface
1. Click **"Train Recommender System"** to process data and train the model
2. Select a book from the dropdown menu
3. Click **"Show Recommendation"** to get similar book suggestions

## 🔄 Pipeline Stages

1. **Data Ingestion**
   - Downloads book dataset from GitHub
   - Extracts and organizes raw data

2. **Data Validation**
   - Validates CSV files
   - Cleans and preprocesses data
   - Serializes processed objects

3. **Data Transformation**
   - Creates book-rating pivot table
   - Transforms data into sparse matrix format

4. **Model Training**
   - Trains k-NN model
   - Saves model artifacts

## 🧠 Algorithm

The system uses **Collaborative Filtering** with these key components:

- **k-Nearest Neighbors (k-NN)** with brute-force algorithm
- **Sparse Matrix Optimization** for efficient similarity computation
- **User-Item Interaction Matrix** for finding similar books

## 📦 Dependencies

- Python 3.7+
- scikit-learn
- pandas
- numpy
- PyYAML
- streamlit

## 📝 Configuration

Edit `config/config.yaml` to customize:
- Dataset paths
- Model parameters
- Directory structures
- API endpoints


## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
