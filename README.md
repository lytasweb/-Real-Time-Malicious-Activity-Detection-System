# Real-Time Malicious Activity Detection System

This repository contains a Flask-based web application for real-time network traffic analysis, powered by machine learning. The system captures network packets, processes them, and classifies them as either "Malicious" or "Analyzed." It supports real-time data visualization and the ability to upload CSV files for batch analysis.

## Features
- Real-time packet capturing and classification
- Machine learning-based malicious activity detection
- CSV file upload for offline analysis
- Real-time data visualization of network activity
- User authentication through a login page

## Technologies Used
- **Flask**: Python web framework for building the application
- **Scapy**: Packet manipulation and analysis tool
- **Joblib**: Serialization of machine learning models
- **Pandas**: Data manipulation and analysis
- **HTML/CSS**: Frontend for user authentication and data visualization
- **Python**: Backend scripting

## Setup Instructions

### 1. Clone the Repository
Clone this repository to your local machine using the following command:
```bash
https://github.com/lytasweb/-Real-Time-Malicious-Activity-Detection-System.git
```

### 2. Install Dependencies
Install the required Python libraries:

bash
Copy
Edit

```bash
pip install -r requirements.txt
```
### 3. Setup Machine Learning Model
Ensure you have the trained model (malicious_activity_model.pkl) and protocol encoder (protocol_encoder.pkl) files available in the project directory. These files are used to make predictions based on the network packet features.

### 4. Run the Application
Start the Flask application by running the following command:

bash
Copy
Edit
python app.py
The web application will run on http://127.0.0.1:5000/.

### 5. Accessing the Application
Login Page: Access the login page at the root URL (/). Use the following credentials:

Username: admin
Password: 12345678
Real-time Data: View live network traffic data by navigating to /real_time_data.

Upload Data: Upload a CSV file for offline analysis by navigating to /upload.

### 6. File Upload
You can upload CSV files with the following columns:

Protocol: The network protocol (e.g., 'TCP', 'UDP')
Length: The length of the packet
Source_Port: The source port of the packet
Destination_Port: The destination port of the packet

### 7. Supported Protocols
The system supports the following protocols:

ICMP (1)
TCP (6)
UDP (17)
IGMP (2)
GRE (47)
ESP (50)
AH (51)
EIGRP (88)
OSPF (89)
SCTP (132)

### 8. Real-Time Packet Capture
The application captures packets in real-time and classifies them using the trained machine learning model. Packets that are classified as malicious are saved as CSV files and can be accessed via the uploads directory.

### 9. Uploading Malicious Data
If the uploaded CSV contains malicious data, a new file containing only the malicious data will be generated and can be downloaded.

Directory Structure
bash
Copy
Edit
/uploads              # Directory for storing uploaded and processed files
  ├── packets_<timestamp>.csv
  ├── test1_<timestamp>.csv
  └── packets_<timestamp>.json

/app.py                # Main Flask application file
/templates
  └── function.html    # Frontend HTML template for displaying real-time data
/static
  └── style.css        # CSS for styling the login page and other components
/requirements.txt      # List of required Python libraries

### License
### This project is licensed under the MIT License - see the LICENSE file for details.

MIT License
Copyright (c) [2025] [Evis Sylvester]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

#### THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
