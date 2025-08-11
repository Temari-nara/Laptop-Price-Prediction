# Laptop Price Prediction Application

A machine learning-powered web application that predicts laptop prices based on hardware specifications and features. Built with Streamlit for an interactive user experience.

## 🚀 Features

- **Interactive Web Interface**: User-friendly Streamlit interface for easy specification input
- **Comprehensive Specification Options**: Supports multiple laptop brands, types, and configurations
- **Real-time Price Prediction**: Instant price predictions based on selected specifications
- **Hardware Configuration Support**: Covers CPU, GPU, RAM, storage, display, and other key features

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Backend**: Python
- **Machine Learning**: Scikit-learn (pickled model)
- **Data Processing**: NumPy, Pandas

## 📋 Specifications Supported

### Hardware Components
- **Brands**: Multiple laptop manufacturers
- **Types**: Various laptop categories (Gaming, Ultrabook, Workstation, etc.)
- **RAM**: 2GB to 64GB options
- **Storage**: HDD (0-2048GB) and SSD (0-1024GB) configurations
- **Processors**: Multiple CPU brands and models
- **Graphics**: Various GPU options

### Display Features
- **Screen Size**: 10.0" to 18.0" (slider input)
- **Resolution**: Multiple resolution options (1366x768 to 3840x2160)
- **Display Type**: IPS and non-IPS options
- **Touchscreen**: Yes/No selection

### Additional Features
- **Weight**: Numeric input for laptop weight
- **Operating System**: Multiple OS options

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7+
- pip (Python package manager)

### Required Dependencies
```bash
pip install streamlit numpy pickle
```

### Project Structure
```
laptop-price-prediction/
│
├── app.py                 # Main Streamlit application
├── pipe.pkl              # Trained ML model (pipeline)
├── df.pkl                # Dataset/feature information
├── README.md             # Project documentation
└── requirements.txt      # Python dependencies
```

### Running the Application

1. **Clone the repository**
   ```bash
   git clone https://github.com/Temari-nara/Laptop-Price-Prediction.git
   cd laptop-price-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Streamlit app**
   ```bash
   streamlit run app.py
   ```

4. **Open your browser**
   - The application will automatically open at `http://localhost:8501`
   - If not, navigate to the URL shown in your terminal

## 📊 How It Works

1. **Select Specifications**: Choose from dropdown menus and input fields to specify your desired laptop configuration
2. **Configure Display**: Set screen size, resolution, and display features
3. **Choose Storage & Memory**: Select RAM, HDD, and SSD configurations
4. **Predict Price**: Click the "Predict Price" button to get an estimated price

### Price Calculation Process
- The application processes your inputs and calculates PPI (Pixels Per Inch) from resolution and screen size
- Features are transformed and fed into the pre-trained machine learning pipeline
- The model returns a logarithmic prediction which is converted back to actual price format

## 🔧 Model Information

- **Model Type**: Machine Learning Pipeline (saved as `pipe.pkl`)
- **Input Features**: 12 different laptop specifications
- **Output**: Predicted laptop price in currency units
- **Preprocessing**: Includes feature encoding and scaling within the pipeline

## 📁 Required Files

Make sure these files are present in your project directory:
- `pipe.pkl` - The trained machine learning model
- `df.pkl` - Dataset containing feature options and categories
- `app.py` - Main application file

## 🎯 Usage Example

1. Select "Dell" as brand
2. Choose "Gaming" as type
3. Set RAM to 16GB
4. Enter weight as 2.5
5. Select "Yes" for touchscreen
6. Choose screen size and resolution
7. Configure CPU, storage, and GPU options
8. Click "Predict Price" for instant results

## 🚀 Deployment Options

### Local Development
- Run using `streamlit run app.py`

### Cloud Deployment
- **Streamlit Cloud**: Push to GitHub and deploy via Streamlit Cloud
- **Heroku**: Deploy using Heroku with appropriate buildpacks
- **AWS/GCP**: Deploy on cloud platforms with container services

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## 📝 Future Enhancements

- Add more laptop brands and models
- Include additional features like battery life, build quality metrics
- Implement price comparison with market prices
- Add visualization of price trends
- Support for bulk predictions via CSV upload

## 📞 Support

For questions, issues, or contributions, please:
- Open an issue on GitHub
- Contact the development team
- Check the documentation for common troubleshooting

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Note**: Ensure you have the required model files (`pipe.pkl` and `df.pkl`) in your project directory before running the application. These files contain the trained model and dataset information necessary for price predictions.