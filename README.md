# GP-Tea: Artificial Intelligence in Healthcare

> A smart healthcare companion mobile application designed to bridge the gap between patients and preliminary medical diagnosis using Artificial Intelligence.

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![AI Assisted](https://img.shields.io/badge/AI_Assisted-Vibe_Coding-7000FF?style=for-the-badge)
![Efficiency](https://img.shields.io/badge/Efficiency-60%25_Faster-success?style=for-the-badge)

## ⚡ GenAI Impact: Accelerating Development
This project demonstrates the power of **AI-Assisted Engineering**. By leveraging tools like Claude 3.5 Sonnet and GPT-4 for code generation and architectural guidance, we achieved a **60% reduction in R&D time**.

<img width="1604" height="898" alt="image" src="https://github.com/user-attachments/assets/231cf494-5a46-4059-bcd0-a95a9880779c" />

*> Comparative analysis showing over 30 hours of development time saved across Research, Coding, and Testing phases.*

## 👩‍💻 My Contribution (Frontend & Integration)
* **UI Development:** Built the complete mobile interface using **Flutter**.
* **System Integration:** Connected the **FastAPI** backend services with the mobile frontend.
* **Feature Assembly:** Orchestrated various AI modules into a cohesive application.
**Challenge**: Artificial Intelligence in Healthcare

A comprehensive healthcare application built with Flutter frontend and FastAPI backends, featuring AI-powered medical analysis tools including symptom checking, medical image classification, and lab report analysis.

## 👥 Team Information

| Name                    | Role               | Email                             |
| ----------------------- | ------------------ | --------------------------------- |
| **Seif-Eldeen Mostafa** | AI Engineer        | seifeldeen.320240021@ejust.edu.eg |
| **Mohamed Ahmed**       | Back End Engineer  | Mohamed.320240078@ejust.edu.eg    |
| **Sara Youssef**        | Front End Engineer | sara.320240074@ejust.edu.eg       |
| **Arwa Waleed**         | Academic Writing   | arwa.320240128@ejust.edu.eg       |
| **Judy Kamal**          | Academic Writing   | Joudy.320240043@ejust.edu.eg      |

## Demo Video
https://drive.google.com/file/d/1d5KCNWoKFrYilVkajv_WNTjq-wIuKZGT/view?usp=sharing

## 📲 Try the Application

You can download and try the latest build of the **AI in Healthcare** application from the link below:

[Download Application](https://drive.google.com/file/d/10opWPUUOJsTkXuGMDGSNiDKNFgaCFS_G/view?usp=sharing)

## 🚀 Project Features Overview

### 🔍 AI-Powered Symptom Checker

- **Intelligent Disease Prediction**: XGBoost machine learning model for accurate symptom analysis
- **Interactive Symptom Selection**: Search and select from 132+ medical symptoms with intuitive UI
- **Confidence Scoring**: Ranked disease predictions with detailed confidence percentages
- **Real-time Analysis**: Fast processing with comprehensive medical insights

### 🖼️ Medical Image Classification

- **Cancer Detection**: Advanced TensorFlow EfficientNetV2S model for medical image analysis
- **Multi-source Input**: Camera capture and gallery upload support
- **Instant Results**: Real-time image processing with detailed confidence scores
- **Professional Analysis**: Structured prediction results with medical interpretations

### 🧪 Lab Report Analysis

- **AI-Powered Document Analysis**: Hugging Face inference for intelligent lab report interpretation
- **Document Processing**: Support for various lab report formats and images
- **Structured Results**: Organized analysis with summary, key findings, and medical interpretations
- **Comprehensive Insights**: Detailed explanations and healthcare recommendations

## 🛠️ Local Development Setup

### Prerequisites

Before setting up the project, ensure you have the following installed:

- **Flutter SDK**: Version 3.0 or higher
- **Python**: Version 3.8 or higher
- **Git**: Latest version
- **Android Studio/VS Code**: For development
- **Python Package Manager**: pip

### 📱 Frontend Setup (Flutter Application)

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Tantawi65/Healthcare.git
   cd Healthcare
   ```

2. **Install Flutter Dependencies**

   ```bash
   flutter pub get
   ```

3. **Configure Flutter Environment**

   ```bash
   flutter doctor
   ```

   Ensure all requirements are met before proceeding.

4. **Run the Flutter Application**

   ```bash
   # For Android
   flutter run

   # For iOS (macOS only)
   flutter run -d ios

   # For Web
   flutter run -d web
   ```

### 🐍 Backend Services Setup

The application consists of three separate FastAPI backend services that need to be started individually.

#### 1. Symptom Checker Service (Port 8002)

```bash
# Navigate to the service directory
cd backend/Text_classification/symptom_checker

# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install required dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --host 0.0.0.0 --port 8002 --reload
```

#### 2. Image Classification Service (Port 8000)

```bash
# Navigate to the service directory
cd backend/Image_classification

# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install required dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

#### 3. Lab Analysis Service (Port 8003)

```bash
# Navigate to the service directory
cd backend/Lab_analysis

# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install required dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env file and add your Hugging Face API key:
# HUGGINGFACE_API_KEY=your-api-key-here

# Start the FastAPI server
uvicorn main:app --host 0.0.0.0 --port 8003 --reload
```

## 🔧 Environment Configuration

### Required Environment Variables

Create a `.env` file in each backend service directory with the following variables:

```env
# Hugging Face API Key for Lab Analysis
HUGGINGFACE_API_KEY=your-huggingface-api-key-here

# API Configuration
SYMPTOM_CHECKER_PORT=8002
IMAGE_CLASSIFICATION_PORT=8000
LAB_ANALYSIS_PORT=8003

# CORS Origins (for production)
CORS_ORIGINS=http://localhost:3000,https://yourdomain.com
```

### Flutter API Configuration

Update the API endpoints in `lib/services/api_service.dart` if needed:

```dart
class ApiService {
  static const String symptomCheckerBaseUrl = 'http://localhost:8002';
  static const String imageClassificationBaseUrl = 'http://localhost:8000';
  static const String labAnalysisBaseUrl = 'http://localhost:8003';
}
```

## 📦 Dependencies

### Flutter Dependencies

- `flutter`: SDK framework
- `http`: API communication
- `image_picker`: Camera and gallery access
- `go_router`: Navigation management
- `provider`: State management

### Python Backend Dependencies

- `fastapi`: Web framework
- `uvicorn`: ASGI server
- `xgboost`: Machine learning (Symptom Checker)
- `tensorflow`: Deep learning (Image Classification)
- `huggingface-hub`: AI inference (Lab Analysis)
- `python-multipart`: File upload handling
- `python-jose`: JWT token handling
- `pillow`: Image processing

## 🧪 Testing the Application

### Verify Backend Services

1. **Health Checks**:

   - Symptom Checker: http://localhost:8002/health
   - Image Classification: http://localhost:8000/health
   - Lab Analysis: http://localhost:8003/health

2. **API Documentation**:
   - Symptom Checker: http://localhost:8002/docs
   - Image Classification: http://localhost:8000/docs
   - Lab Analysis: http://localhost:8003/docs

### Test API Endpoints

```bash
# Test Symptom Checker
curl -X POST "http://localhost:8002/api/check-symptoms" \
     -H "Content-Type: application/json" \
     -d '{"symptoms": ["fever", "cough", "headache"]}'

# Test Image Classification
curl -X POST "http://localhost:8000/api/classify-image" \
     -F "image=@/path/to/medical/image.jpg"

# Test Lab Analysis
curl -X POST "http://localhost:8003/api/analyze-lab" \
     -F "image=@/path/to/lab/report.pdf"
```

## 🚀 Building for Production

### Flutter Build Commands

```bash
# Android APK
flutter build apk --release

# Android App Bundle
flutter build appbundle --release

# iOS (macOS only)
flutter build ios --release

# Web
flutter build web --release
```

### Backend Deployment

For production deployment, consider using:

- **Docker containers** for each service
- **Environment variable management**
- **Load balancing** for high availability
- **API rate limiting** and authentication
- **Database integration** for user data persistence

## ⚠️ Important Notes

- **Model Files**: AI model files are excluded from the repository due to size constraints. You'll need to train your own models or obtain pre-trained models separately.
- **API Keys**: Never commit API keys to version control. Use environment variables for all sensitive configuration.
- **Security**: This application is for educational and research purposes. Implement proper authentication and security measures for production use.

## 📄 Medical Disclaimer

This application is developed for educational and research purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare professionals for medical concerns.

## 📲 Try the Application

You can download and try the latest build of the **AI in Healthcare** application from the link below:

[Download Application](https://drive.google.com/file/d/10opWPUUOJsTkXuGMDGSNiDKNFgaCFS_G/view?usp=sharing)

---

## 🌐 Live Deployment

The backend services are deployed and accessible online for testing and demonstration purposes.  
Each service runs on a separate FastAPI instance with integrated AI models.

### 🔬 Lab Analysis Service
Analyze lab reports using AI-powered document understanding:
👉 [https://tantawi-lab-analyzer.hf.space/](https://tantawi-lab-analyzer.hf.space/)

### 🖼️ Image Classification Service
Classify medical images and detect cancerous patterns:
👉 [https://tantawi-image-class.hf.space/docs](https://tantawi-image-class.hf.space/docs)

### 💬 Symptom Checker (Text Classification)
Predict possible diseases based on user-entered symptoms:
👉 [https://tantawi-text-classification.hf.space/docs](https://tantawi-text-classification.hf.space/docs)

## 🧠 AI Usage

This project integrates **Generative AI tools** throughout the development process to enhance productivity, code quality, and documentation.  
All **screenshots, prompts, and AI responses** used during development are organized and available in the repository under the folder "AI Usage".

## 📞 Support

For technical support or project inquiries, please contact any team member using the email addresses provided above.
---
**Built with ❤️ by the GP-Tea Team for advancing AI in Healthcare**
