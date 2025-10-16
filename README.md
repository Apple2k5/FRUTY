FRUTY: Smart Farming Revolution

"Turning every farmer's field into a smart farm assistant."

FRUTY is an autonomous, intelligent agricultural robot system designed to automate critical farm tasks, maximize crop yield, and reduce resource waste using real-time data analysis.

🌟 Features

FRUTY tackles key challenges in small-scale farming through four integrated modules:

Pest & Weed Detection: Uses a 3D Camera and the YOLOv5 AI model running on a Raspberry Pi for real-time identification of pests and weed overgrowth.

Automated Weed Management: Executes mechanical cutting of detected weeds with precision-guided rotating blades.

Soil Intelligence: Collects 7-in-1 soil data (NPK, pH, Moisture, EC, Temp) to provide farmers with optimal crop suggestions and historical reports.

Targeted Actuation: Controls automated drip irrigation and applies targeted fertilization only to plants that require it, minimizing fertilizer waste.

🛠️ Technology Stack

Component

Technology

Role

Edge Computing

Raspberry Pi 4 (or similar)

Runs the AI model and controls all actuators/sensors.

Artificial Intelligence

YOLOv5

Real-time object detection for pests and weeds.

Cloud/Database

Firebase

Real-time data storage, alert transmission, and remote control queuing.

Connectivity

Wi-Fi / LoRa

Primary and fallback communication in the field.

Client Application

Android / iOS App

Multi-language UI for alerts, control, and reporting.

🚀 Getting Started

To deploy and test the FRUTY system, you need to set up both the physical robot hardware and the cloud/mobile app infrastructure.

1. Hardware Setup (Raspberry Pi)

Clone the Repository:

git clone [https://github.com/YourOrg/FRUTY.git](https://github.com/YourOrg/FRUTY.git)
cd FRUTY/rpi_code


Install Dependencies:
The core code relies on the following libraries (for sensor communication, motor control, and AI inference):

# Install required packages
pip install firebase-admin numpy opencv-python gpiozero
# Install YOLOv5 dependencies (requires PyTorch)
pip install -r requirements.txt


Connect Peripherals: Ensure the 7-in-1 sensor, 3D camera, and motor drivers are correctly wired to the RPi's GPIO pins as per the /docs/hardware_schema.pdf (not included here, but a good document to add).

Configure Firebase: Download your project's Firebase Service Account JSON file and place it in the rpi_code directory as serviceAccountKey.json.

Run the Main Script:

python3 main_fruty.py


2. Mobile App Setup

The Mobile App is built using Flutter/React Native for cross-platform support.

Navigate to App Directory:

cd FRUTY/mobile_app


Install App Dependencies:

# Example for Flutter
flutter pub get


Connect to Firebase: Configure the app with the Firebase google-services.json (Android) or GoogleService-Info.plist (iOS) files.

Run the App:

flutter run


📚 Documentation & Resources

Software Requirements Specification (SRS): See the detailed requirements document: fruty_srs.md

System Architecture: High-level data flow and component integration.

Sensor Calibration Guide: Details on calibrating the NPK/pH sensors for local soil types.

🤝 Contributing

We welcome contributions! Please feel free to open an issue or submit a pull request if you find bugs, suggest new features, or want to help optimize the AI models.

Contributor Guidelines

Fork the repository.

Create your feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.



Ram Charan Samuel

Hardware/Robotics

[Your GitHub Link]

📝 License

Distributed under the MIT License. See LICENSE for more information.
