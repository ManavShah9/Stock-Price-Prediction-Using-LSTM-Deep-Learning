# Stock-Price-Prediction-Using-LSTM-Deep-Learning
📈 Stock Price Prediction using LSTM
This project implements a deep learning model using LSTM (Long Short-Term Memory) neural networks to predict stock prices based on historical closing values. The model architecture is inspired by Krish Naik’s approach and enhanced through detailed understanding and experimentation.

🔧 Technologies Used

Python

NumPy & Pandas

Matplotlib

Scikit-learn

TensorFlow / Keras

LSTM (Sequential Model)

🧠 Model Architecture

model = Sequential()
model.add(LSTM(50, return_sequences=True, input_shape=(100, 1)))
model.add(LSTM(50, return_sequences=True))
model.add(LSTM(50))
model.add(Dense(1))
model.compile(loss='mean_squared_error', optimizer='adam')
Three LSTM layers with 50 units each.

return_sequences=True is used in the first two layers to pass sequences forward.

The final Dense layer outputs a single predicted value (e.g., the next closing price).

The model is compiled using Mean Squared Error (MSE) as the loss and Adam optimizer.

🔢 Dataset
Uses historical stock prices (e.g., from Yahoo Finance).

Focuses on the “Close” price for prediction.

Scaled using MinMaxScaler for better performance.

📊 Visualizations
Actual vs Predicted plots for both training and testing datasets.

Inverse transformation is applied to bring values back to their original scale before plotting.

🧪 Future Prediction
The model also includes logic to forecast stock prices for the next 30 days using a rolling prediction window.

🗂️ Folder Structure
bash
Copy
Edit
├── Stock_Price_Prediction_Using_LSTM.ipynb   # Jupyter notebook with full code
├── AAPL.csv               
├── README.md
