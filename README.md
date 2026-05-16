# Flight Price Prediction

A machine learning web application that predicts Indian domestic flight prices based on travel details such as airline, route, duration, and number of stops.

## Live Demo

[flight-price-prediction.streamlit.app](https://adesiddarthanaik-flight-price-prediction-app-xyjmiu.streamlit.app/)

## Tech Stack

- **ML Model:** XGBoost (trained on AWS SageMaker)
- **Feature Engineering:** scikit-learn Pipelines, ColumnTransformer, feature-engine
- **Frontend:** Streamlit
- **Deployment:** Streamlit Cloud
- **Cloud Services:** AWS SageMaker (model training), AWS S3 (data storage)

## Features

- Predicts flight prices for major Indian airlines and routes
- Handles categorical, numerical, and datetime feature types through a unified preprocessing pipeline
- Custom feature engineering including RBF kernel similarity, time-of-day encoding, and target-based encoding
- Real-time predictions via an interactive web interface

## How It Works

1. User inputs flight details (airline, source, destination, date, time, duration, stops)
2. The preprocessing pipeline transforms raw inputs into model-ready features
3. A trained XGBoost model predicts the fare
4. Predicted price is displayed in INR

## Dataset

The dataset contains Indian domestic flight records with the following attributes:

| Feature | Description |
|---|---|
| airline | Name of the airline |
| date_of_journey | Date of travel |
| source | Departure city |
| destination | Arrival city |
| dep_time | Departure time |
| arrival_time | Arrival time |
| duration | Flight duration in minutes |
| total_stops | Number of stops |
| additional_info | Meal info, baggage, etc. |
| price | Ticket price in INR (target) |

## Project Structure

```
flight-price-prediction/
├── app.py                 # Streamlit web application
├── train.csv              # Training dataset
├── xgboost-model          # Trained XGBoost model
├── requirements.txt       # Python dependencies
└── README.md
```

## Run Locally

```bash
git clone https://github.com/adesiddarthanaik/flight-price-prediction.git
cd flight-price-prediction
pip install -r requirements.txt
streamlit run app.py
```

## License

This project is open source and available for educational purposes.
