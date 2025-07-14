# Stock Price Prediction using LSTM Neural Networks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohamedsaif21/NM_saif_DS/blob/sa/Stock_Price_Prediction.ipynb)

### 🎓 Program Background

This project was conducted as part of the **Naan Mudhalvan** program by **Oracle Company**. It represents a mandatory course completion from the Naan Mudhalvan team's 1-month intensive session focused on Data Science. This project demonstrates the practical application of machine learning concepts learned during the comprehensive Data Science course offered through this program.


## 📈 Project Overview

This project implements a Long Short-Term Memory (LSTM) neural network to predict stock prices using historical data. The model is trained on Apple stock data and uses deep learning techniques to forecast future price movements based on past 60-day sequences.



## 🎯 Features

- **Time Series Prediction**: Uses LSTM neural networks for sequential data analysis
- **Data Preprocessing**: Implements MinMaxScaler for data normalization
- **Sequence Creation**: Creates 60-day sliding windows for training
- **Visualization**: Provides clear comparisons between actual vs predicted prices
- **Model Persistence**: Saves trained model for future use
- **Google Colab Integration**: Ready-to-run notebook in Colab environment

## 🛠️ Technologies Used

- **Python 3.x**
- **TensorFlow/Keras** - Deep learning framework
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Scikit-learn** - Data preprocessing and scaling
- **Matplotlib** - Data visualization
- **Jupyter Notebook** - Interactive development environment

## 📊 Dataset

The project uses Apple stock price data (`Apple Dataset (2).csv`) containing historical stock information including:
- Open, High, Low, Close prices
- Volume data
- Date information

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy tensorflow scikit-learn matplotlib
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/mohamedsaif21/NM_saif_DS.git
cd NM_saif_DS
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Open the Jupyter notebook:
```bash
jupyter notebook Stock_Price_Prediction.ipynb
```

### Running in Google Colab

Click the "Open in Colab" badge at the top of this README or the notebook to run directly in Google Colab.

## 📋 Project Structure

```
NM_saif_DS/
├── Stock_Price_Prediction.ipynb    # Main notebook with LSTM implementation
├── Apple Dataset (2).csv           # Apple stock price dataset
├── README.md                       # Project documentation
├── mohamed saif hackathon submission.docx.pdf
├── Mohamed saif Phase 2.pdf
├── Mohamed saif Phase-3.docx.pdf
└── Mohamed saif Phase1.pdf
```

## 🔧 Model Architecture

The LSTM model consists of:

1. **Input Layer**: 60-day sequences of normalized stock prices
2. **LSTM Layer 1**: 50 units with return_sequences=True
3. **Dropout Layer 1**: 20% dropout for regularization
4. **LSTM Layer 2**: 50 units
5. **Dropout Layer 2**: 20% dropout for regularization
6. **Dense Output Layer**: Single unit for price prediction

### Model Parameters:
- **Sequence Length**: 60 days
- **Training Split**: 80% training, 20% testing
- **Optimizer**: Adam
- **Loss Function**: Mean Squared Error
- **Epochs**: 20
- **Batch Size**: 32

## 📈 Results

The model provides:
- Visual comparison between actual and predicted stock prices
- Training and validation loss metrics
- Saved model file (`lstm_stock_model.keras`) for future predictions

## 🎨 Visualization

The project includes matplotlib visualizations showing:
- Actual vs Predicted stock prices
- Model performance over time
- Clear trends and patterns in stock price movements

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Usage Example

```python
# Load and preprocess data
df = pd.read_csv("Apple Dataset (2).csv")
data = df[['Close']].values
scaled_data = scaler.fit_transform(data)

# Create sequences and train model
X, y = create_sequences(scaled_data, 60)
model.fit(X_train, y_train, epochs=20)

# Make predictions
predictions = model.predict(X_test)
```

## 🔮 Future Enhancements

- [ ] Add more technical indicators (RSI, MACD, Moving Averages)
- [ ] Implement multi-stock prediction
- [ ] Add real-time data fetching
- [ ] Create web interface for predictions
- [ ] Implement ensemble methods
- [ ] Add more sophisticated evaluation metrics

## 📊 Performance Metrics

The model's performance can be evaluated using:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Visual inspection of prediction plots

## ⚠️ Disclaimer

This project is for educational and research purposes only. Stock price predictions should not be used as the sole basis for investment decisions. Always consult with financial advisors and do your own research before making investment choices.

## 👨‍💻 Author

**Mohamed Saif**
- GitHub: [@mohamedsaif21](https://github.com/mohamedsaif21)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- TensorFlow team for the excellent deep learning framework
- The open-source community for valuable resources and tutorials
- Financial data providers for making historical stock data available

---

⭐ If you found this project helpful, please give it a star!

