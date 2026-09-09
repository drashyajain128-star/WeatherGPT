# WeatherGPT
Conversational AI platform for real-time weather forecasting, alerts, climate insights, and actionable weather-based recommendations.
# 🌦️ WeatherGPT

**AI-powered conversational weather platform for forecasts, alerts, climate insights, and actionable recommendations.**

## 📌 About the Project

WeatherGPT is a conversational AI-based weather platform designed to make weather information easier to understand and more useful.

Instead of searching through multiple weather websites and technical data sources, users can interact with the system using natural language and receive relevant weather information, forecasts, alerts, and recommendations.

## 🚀 Key Features

* 🌤️ Real-time weather information
* 💬 Natural-language weather queries
* 📍 Location-based weather forecasting
* ⚠️ Extreme weather alerts
* 📊 Historical weather and climate analysis
* 🤖 AI-powered weather insights using the Gemini API
* 🌐 Multilingual support
* 🎙️ Voice-based interaction
* 🌾 Actionable recommendations based on weather conditions
* 📈 Weather data processing and analysis
* 🔎 Anomaly detection where required

## 🛠️ Technology Stack

* **Frontend:** React
* **Backend:** Python with FastAPI
* **LLM:** Gemini API
* **Weather Data:** Open-Meteo API
* **Weather Authority/Data Source:** India Meteorological Department (IMD), where publicly accessible
* **Database:** SQLite initially
* **Data Processing:** Pandas and NumPy
* **ML/Anomaly Detection:** Scikit-learn only where actually needed
* **Deployment:** Vercel for the frontend and a suitable Python-compatible hosting platform for the backend

## 🎯 Goal

The goal of WeatherGPT is to transform complex weather information into simple, conversational, and actionable insights that can help users make better decisions.

The platform combines weather data from Open-Meteo and publicly accessible IMD sources with AI-powered natural-language interaction. It is designed to present weather information clearly while maintaining appropriate distinction between forecast data, official weather authority information, historical analysis, and AI-generated recommendations.

## 📂 Project Structure

```text
WeatherGPT/
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── README.md
├── backend/
│   ├── app/
│   ├── requirements.txt
│   └── README.md
├── data/
├── database/
│   └── weather.db
├── assets/
└── README.md
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd WeatherGPT
```

### 2. Set up the frontend

Navigate to the frontend directory and install the required dependencies:

```bash
cd frontend
npm install
```

Start the React development server:

```bash
npm run dev
```

### 3. Set up the backend

Open a new terminal, navigate to the backend directory, and create a virtual environment:

```bash
cd backend
python -m venv venv
```

Activate the virtual environment.

On Windows:

```bash
venv\Scripts\activate
```

On macOS or Linux:

```bash
source venv/bin/activate
```

Install the backend dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI development server:

```bash
uvicorn app.main:app --reload
```

The backend API will be available at:

```text
http://127.0.0.1:8000
```

FastAPI documentation will be available at:

```text
http://127.0.0.1:8000/docs
```

### 4. Configure environment variables

Create a `.env` file in the backend directory and add the required configuration:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Additional configuration may be added for database paths, API settings, or deployment environments.

## 🔌 Data Sources and Processing

WeatherGPT uses the following data sources and processing tools:

* **Open-Meteo API** for weather forecasts and related weather data
* **India Meteorological Department (IMD)** data where publicly accessible and applicable
* **SQLite** for initial local data storage
* **Pandas** for tabular data processing and historical analysis
* **NumPy** for numerical operations
* **Scikit-learn** only when machine-learning-based anomaly detection is necessary

The system should identify the source of weather information where appropriate and avoid presenting AI-generated interpretations as official forecasts or warnings.

## 🌐 Deployment

The React frontend can be deployed using **Vercel** for a publicly accessible web application.

The Python and FastAPI backend should be deployed on a platform that supports long-running Python web services. The frontend must be configured to communicate with the deployed backend through an environment-specific API URL.

Before deployment:

* Configure production environment variables
* Secure the Gemini API key on the backend
* Configure the production database path
* Enable appropriate CORS settings
* Verify API rate limits and external data-source availability
* Test fallback behavior when weather services are unavailable

## 👥 Team

Developed as a project for **Smart India Hackathon (SIH)**.

## 📄 License

This project is for educational and hackathon purposes.
