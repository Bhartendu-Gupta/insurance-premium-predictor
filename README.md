# 🚀 Insurance Premium Predictor API

A Machine Learning-powered REST API that predicts an individual's insurance premium category based on user information. The project is built using **FastAPI**, **Scikit-learn**, and **Docker**, demonstrating how a trained machine learning model can be deployed as a scalable and production-ready web service.

---

## ✨ Features

- Predicts insurance premium category using a trained Machine Learning model
- RESTful API built with FastAPI
- Input validation using Pydantic
- Returns prediction confidence score
- Health check endpoint for monitoring
- Interactive Swagger UI documentation
- Dockerized for easy deployment
- Clean and modular project structure

---

## 🛠️ Tech Stack

- Python
- FastAPI
- Scikit-learn
- Pandas
- NumPy
- Pydantic
- Uvicorn
- Docker
- Git
- GitHub

---

## 📂 Project Structure

```text
insurance-premium-predictor/
│
├── app.py
├── Dockerfile
├── requirements.txt
├── README.md
├── .gitignore
│
├── confige/
│   └── city_tier.py
│
├── model/
│   ├── model.pkl
│   └── predict.py
│
└── schema/
    ├── user_input.py
    └── Prediction_response.py
```

---

## ⚙️ Installation

### Clone the repository

```bash
git clone https://github.com/Bhartendu-Gupta/insurance-premium-predictor.git
```

### Navigate to the project

```bash
cd insurance-premium-predictor
```

### Create a virtual environment

```bash
python -m venv myenv
```

### Activate the virtual environment (Windows)

```bash
myenv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the API

```bash
uvicorn app:app --reload
```

The application will start at:

```text
http://127.0.0.1:8000
```

---

## 🐳 Docker

### Build Docker Image

```bash
docker build -t insurance-api .
```

### Run Docker Container

```bash
docker run -p 8000:8000 insurance-api
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/` | Returns welcome message |
| GET | `/health` | Checks API health |
| POST | `/predict` | Predicts insurance premium category |

---

## 📝 Sample Request

```json
{
  "age": 30,
  "weight": 70,
  "height": 175,
  "income_lpa": 10,
  "smoker": false,
  "city": "Indore",
  "occupation": "Engineer"
}
```

---

## ✅ Sample Response

```json
{
  "predicted_category": "Medium",
  "confidence": 0.94,
  "class_probabilities": {
    "Low": 0.02,
    "Medium": 0.94,
    "High": 0.04
  }
}
```

---

## 📖 API Documentation

FastAPI automatically generates interactive API documentation.

Open the following URL after starting the server:

```text
http://127.0.0.1:8000/docs
```

---

## 🚀 Future Improvements

- Deploy the API on Render or Railway
- Add authentication and authorization
- Improve model accuracy with more training data
- Add logging and monitoring
- Implement CI/CD using GitHub Actions

---

## 👨‍💻 Author

**Bhartendu Gupta**

B.Tech in Electronics Engineering

Machine Learning | FastAPI | Python | Docker

GitHub: https://github.com/Bhartendu-Gupta



## ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub.
