# Vision-Enabled-Chatbot-for-Rice-Leaf-Disease-Classification-using-MobileNetV3-and-GPT-4o

A web-based application that helps users identify rice leaf diseases through image classification and provides interactive explanations and recommendations via an AI-powered chatbot.

## Overview
This project is a web-based application that integrates Computer Vision and Generative AI:
1. The uploaded rice leaf image is processed using a MobileNetV3 model to classify the type of disease.
2. The model predicts the disease category along with a confidence score.
3. The user is then redirected to a GPT-4o-powered chatbot for interactive explanations, including disease details, symptoms, and recommended actions.

## Project Structure

```
├── app.py              # Main application entry point
├── config.py           # Application configuration
├── requirements.txt    # Project dependencies
├── routes/            # Route handlers
│   ├── api_routes.py
│   ├── article_routes.py
│   └── main_routes.py
├── templates/         # HTML templates
│   ├── article/
│   ├── chatbot.html
│   ├── deteksi.html
│   └── index.html
├── static/           # Static files (CSS, JS, images)
├── model/           # H5 model files
└── utils/           # Utility functions
```

## Application Flow

1. **Home Page**
   - Users land on the home page
   - Access to main features: Image Upload and Chatbot
   - Navigation to articles

2. **Image Analysis Process**
   a. **Initial Upload**
      - Users upload an image of a rice leaf
      - Image format validation is performed
   
   b. **GPT-4 Vision Validation**
      - Validates whether the uploaded image indicates the presence of rice leaf disease
      - Rejects unsuitable or invalid images
      - Provides feedback to users if the image is not accepted
   
   c. **MobileNetV3 Model Analysis**
      - Processes validated images using a MobileNetV3-based CNN model
      - Performs detailed analysis of rice leaf conditions
      - Generates prediction results
   
   d. **Results Display**
      - Displays the analysis results to the user
      - Redirects users to the chatbot page for further interaction

3. **Chatbot Interface**
   - Interactive chatbot interface powered by AI
   - Able to retain detection results and conversation context
   - Provides educational information about rice leaf diseases
     
## Setup and Installation

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - Windows: `venv\Scripts\activate`
   - Unix/MacOS: `source venv/bin/activate`
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
5. Create a folder with the name model, then put the keras model (h5) into the folder
6. Run the application:
   ```bash
   python app.py
   ```

## Dependencies

Key dependencies include:
- Flask
- TensorFlow Keras
- Other dependencies listed in requirements.txt

## Results
### Upload Image Page
<img width="1849" height="887" alt="Screenshot 2026-01-04 235822" src="https://github.com/user-attachments/assets/523696c4-22af-43a4-b32d-42a7f44fe88d" />
<img width="1846" height="887" alt="Screenshot 2026-01-05 000014" src="https://github.com/user-attachments/assets/eafbdcbb-e95c-4526-896b-9a7e7211ffa5" />


### Chatbot Page
<img width="1844" height="886" alt="Screenshot 2026-01-05 011744" src="https://github.com/user-attachments/assets/e363e07c-09ee-45be-b069-ad566d50ff05" />



## Future Improvements

1. Improve model accuracy  
2. Add more disease classes  
