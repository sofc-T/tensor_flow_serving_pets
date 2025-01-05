# Deploying a Model with TensorFlow Serving and Flask

This project demonstrates how to deploy a pre-trained TensorFlow model using TensorFlow Serving (with Docker) and create a Flask-based web interface for making predictions.

## Steps to Run

### 1. Start TensorFlow Serving with Docker

- Open a terminal or Command Prompt (as administrator on Windows).
- Run the following command:

```bash
docker run -p 8501:8501 --name=pets -v "C:\pets:/models/pets/1" -e MODEL_NAME=pets tensorflow/serving
```

**Note**: Replace `C:\pets` with your model directory path.

### 2. Set Up and Run Flask

- **Create a virtual environment**:

```bash
python -m venv flaskapp
```

- **Activate the virtual environment**:
    - On macOS/Linux:
    
    ```bash
    source flaskapp/bin/activate
    ```
    
    - On Windows:
    
    ```bash
    flaskapp\Scripts\activate
    ```

- **Install dependencies**:

```bash
pip install -r requirements.txt
```

- **Start the Flask app**:

```bash
python app.py
```

### 3. Open the Web App

Go to `http://localhost:5000` in your browser to use the app.

## Requirements

Install all Python dependencies with:

```bash
pip install -r requirements.txt
```

This guide simplifies the deployment process and sets up the web app for serving model predictions.
