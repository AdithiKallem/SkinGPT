SkinGPT: An AI-Powered Diagnostic System for Skin Condition Analysis and Recommendations

## Introduction to the Problem
1. Skin conditions can vary widely and are often challenging to diagnose accurately without specialized medical expertise.
2. Many individuals lack access to immediate dermatological care and require reliable diagnostic tools.
3. There is a pressing need for a scalable, AI-powered system that can quickly analyze and identify various skin conditions to provide helpful insights and recommendations.

## Solution Outline
1. User Interface:
   - The system provides two user-friendly interfaces:
     * `index.html` for image uploads and initial analysis.
     * `chatbot.html` for querying the diagnostic chatbot.

2. Image Analysis:
   - Uses the YOLOv5 model to identify and classify different skin conditions based on uploaded images.
   - `detect.py` consists of functions for object detection model.
   - Provides a diagnosis and additional context regarding the detected condition.

3. Natural Language Processing (NLP):
   - Utilizes the LLaMA model via Hugging Face Transformers to offer precise, conversational explanations.
   - contains function to generate a response to a query using LLaMA.
   - Users can ask queries and receive recommendations or explanations of their condition.

4. Program Input and Output Examples:
   - Input: Uploading an image via the `index.html` form.
   - Output: Diagnostic results of skin conditions (e.g., "The detected disease is eczema") and follow-up recommendations.

## System Setup and Execution
1. Environment Setup:
   - Ensure Python 3.x is installed along with `pip` for package management.
   - Set up a virtual environment to isolate dependencies.
   - Install required packages using the provided `requirements.txt`.

   ```bash
   python -m venv skingpt_env
   source skingpt_env/bin/activate
   pip install -r requirements.txt

## Dataset
The dataset is directly bought into the image detection model through the yolov5, which is trained in the google colab and imported into the system as ".pt" file. These files cease to exist after a few hours and cannot be rendered.

## Running the System
- Start the Flask server using app.py.
- Access the web interface by visiting http://127.0.0.1:5000 in a browser.
- Upload an image for analysis or interact with the chatbot.
  
  ```bash
  python app.py

