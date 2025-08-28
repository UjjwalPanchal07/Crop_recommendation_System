# 🌾 Crop Recommendation System

A machine learning-based web application that recommends the most suitable crops based on soil and climate parameters. Built with Flask, scikit-learn, and modern web technologies.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.3.3-green.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.0-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [API Reference](#api-reference)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## 🌱 Overview

The Crop Recommendation System is an intelligent web application that helps farmers and agricultural professionals make informed decisions about crop selection. By analyzing soil nutrients (Nitrogen, Phosphorus, Potassium), climate conditions (Temperature, Humidity, pH, Rainfall), the system provides personalized crop recommendations to optimize yields and maximize profitability.

### Key Benefits
- **Data-Driven Decisions**: Based on 2200+ agricultural data samples
- **Real-Time Analysis**: Instant recommendations with input validation
- **User-Friendly Interface**: Modern, responsive web design
- **Professional Validation**: Comprehensive input range checking
- **Visual Feedback**: Crop images and animated results

## ✨ Features

### 🌿 Core Functionality
- **Multi-Parameter Analysis**: Considers 7 key agricultural factors
- **22 Crop Support**: Recommends from 22 different crop types
- **Input Validation**: Real-time validation with helpful error messages
- **Range Checking**: Ensures inputs are within realistic agricultural ranges
- **Professional UI**: Modern, responsive design with animations

### 🎨 User Experience
- **Beautiful Interface**: Gradient backgrounds and smooth animations
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Visual Feedback**: Animated plant icons and crop images
- **Error Handling**: Clear, actionable error messages
- **Loading States**: Smooth transitions and user feedback

### 🔧 Technical Features
- **Machine Learning Model**: Trained on comprehensive agricultural dataset
- **Data Preprocessing**: StandardScaler and MinMaxScaler for optimal predictions
- **Image Integration**: Local and Unsplash API image support
- **Form Validation**: Both client-side and server-side validation
- **Error Recovery**: Graceful handling of edge cases

## 🛠️ Technologies Used

### Backend
- **Python 3.8+**: Core programming language
- **Flask 2.3.3**: Web framework for API and routing
- **scikit-learn 1.3.0**: Machine learning library
- **NumPy 1.24.3**: Numerical computing
- **Pandas 2.0.3**: Data manipulation and analysis
- **Pickle**: Model serialization

### Frontend
- **HTML5**: Semantic markup
- **CSS3**: Modern styling with animations
- **Bootstrap 5.3.0**: Responsive UI framework
- **JavaScript**: Interactive elements
- **Google Fonts**: Typography (Nunito)
- **Animate.css**: CSS animations

### External APIs
- **Unsplash API**: Crop images (public source API)
- **Lottie**: Animated graphics

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/crop-recommendation-system.git
   cd crop-recommendation-system
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Access the application**
   Open your browser and navigate to `http://localhost:5000`

## 📖 Usage

### Input Parameters

The system analyzes the following parameters to provide crop recommendations:

| Parameter | Unit | Valid Range | Description |
|-----------|------|-------------|-------------|
| **Nitrogen (N)** | kg/ha | 0-140 | Soil nitrogen content |
| **Phosphorus (P)** | kg/ha | 5-145 | Soil phosphorus content |
| **Potassium (K)** | kg/ha | 5-205 | Soil potassium content |
| **Temperature** | °C | 8-44 | Average temperature |
| **Humidity** | % | 14-100 | Relative humidity |
| **pH** | Unitless | 3.5-10.0 | Soil acidity/alkalinity |
| **Rainfall** | mm | 20-300 | Total precipitation |

### How to Use

1. **Enter Soil Parameters**: Input Nitrogen, Phosphorus, and Potassium values
2. **Enter Climate Data**: Provide Temperature, Humidity, pH, and Rainfall
3. **Get Recommendation**: Click "Get Recommendation" button
4. **View Results**: See the recommended crop with image and details

### Example Input
```
Nitrogen: 50 kg/ha
Phosphorus: 60 kg/ha
Potassium: 40 kg/ha
Temperature: 25°C
Humidity: 70%
pH: 6.5
Rainfall: 150 mm
```

## 🤖 Model Details

### Dataset Information
- **Total Samples**: 2,200 agricultural data points
- **Crop Classes**: 22 different crop types
- **Features**: 7 input parameters
- **Data Balance**: 100 samples per crop (balanced dataset)

### Supported Crops
1. Rice, 2. Maize, 3. Jute, 4. Cotton, 5. Coconut
6. Papaya, 7. Orange, 8. Apple, 9. Muskmelon, 10. Watermelon
11. Grapes, 12. Mango, 13. Banana, 14. Pomegranate, 15. Lentil
16. Blackgram, 17. Mungbean, 18. Mothbeans, 19. Pigeonpeas
20. Kidneybeans, 21. Chickpea, 22. Coffee

### Machine Learning Pipeline
1. **Data Preprocessing**: MinMaxScaler followed by StandardScaler
2. **Model Training**: Classification algorithm (details in notebook)
3. **Prediction**: Real-time crop classification
4. **Output**: Crop recommendation with confidence

## 🔌 API Reference

### Endpoints

#### GET `/`
- **Description**: Main application page
- **Response**: HTML template with input form

#### POST `/predict`
- **Description**: Get crop recommendation
- **Request Body**: Form data with 7 parameters
- **Response**: HTML with recommendation and image

#### GET `/img.jpg`
- **Description**: Serve local crop image
- **Response**: Image file

### Request Format
```json
{
  "Nitrogen": "50",
  "Phosporus": "60", 
  "Potassium": "40",
  "Temperature": "25",
  "Humidity": "70",
  "Ph": "6.5",
  "Rainfall": "150"
}
```

## 📸 Screenshots

### Main Interface
![Main Interface](screenshots/main-interface.png)

### Input Form
![Input Form](screenshots/input-form.png)

### Results Display
![Results](screenshots/results.png)

*Note: Screenshots will be added to the repository*

## 🤝 Contributing

We welcome contributions to improve the Crop Recommendation System!

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
4. **Test thoroughly**
5. **Commit your changes**
   ```bash
   git commit -m "Add: your feature description"
   ```
6. **Push to your branch**
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Create a Pull Request**

### Development Setup
```bash
# Install development dependencies
pip install -r requirements.txt

# Run in development mode
export FLASK_ENV=development
python app.py
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

- **Email**: 611noorsaeed@gmail.com
- **GitHub**: [Your GitHub Profile]
- **LinkedIn**: [Your LinkedIn Profile]

## 🙏 Acknowledgments

- Agricultural research community for data and insights
- Farmers and agricultural professionals for domain knowledge
- Open-source community for tools and libraries
- Unsplash for crop images

---

⭐ **Star this repository if you find it helpful!**

🌱 **Happy Farming!**
