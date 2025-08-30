Acne-ML-Analyzer
AI-powered facial analysis for acne detection and severity assessment.

The Acne-ML-Analyzer is an open-source machine learning project designed to automatically detect and analyze facial acne. This tool leverages a fine-tuned YOLOv8-seg model and other computer vision techniques to provide a comprehensive analysis of a user's skin, making it useful for dermatological research, personal skincare tracking, and educational purposes.

🌟 Key Features
Our model's core functionalities are:

Facial Zoning: 🗺️ The system uses Mediapipe to accurately divide the face into specific zones (e.g., forehead, cheeks, chin) to localize acne outbreaks and provide zone-specific insights.

Acne Segmentation: 🎯 Using a fine-tuned YOLOv8-seg model, we precisely identify and outline individual acne lesions, distinguishing them from other skin features. This allows for a detailed count and analysis of the affected areas.

Severity Calculation: 📈 Based on the size, density, and distribution of segmented acne, the model calculates a comprehensive severity score, offering a quantifiable measure of the condition.

🚀 How It Works
The model processes an input image of a face and operates in three main steps:

Preprocessing & Facial Zoning: The image is first processed to detect facial landmarks using Mediapipe, which is used to define and map specific facial zones.

Acne Segmentation: A fine-tuned YOLOv8-seg model is then applied to the image to perform instance segmentation, accurately identifying and outlining each individual acne lesion.

Severity Scoring: The segmented acne areas are assigned to their respective facial zones. A custom algorithm then calculates a weighted severity score for each zone based on the lesion area and clinical weights for different acne types. This numeric score is then normalized and translated into a human-readable severity rating: "Clear," "Mild," "Moderate," or "Severe."

Example Output
Here's an example of what the model's output looks like:

![input_05_halfFaceAcne](https://github.com/user-attachments/assets/803fcb2d-fe55-4bd0-a519-d02328cf561e)
![final_analysis_output_05](https://github.com/user-attachments/assets/b252128c-c893-4ffb-a7ac-90c25f9e0f1c)


Before Analysis	After Analysis
A simple input image with acne on the face.	The model's output showing facial zones, segmented acne, and calculated severity.

💾 Dataset
This project uses the Acne Dataset Preparation from Roboflow Universe. This dataset contains a variety of images annotated with bounding boxes and segmentation masks for different types of acne, which were crucial for training and fine-tuning the YOLOv8-seg model.

