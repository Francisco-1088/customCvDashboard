# customCvDashboard

## Prerequisites

1. Have a working version of Docker in your computer
2. Have a working installation of Python3

## How to use

1. Clone repo into your environment with `git clone https://github.com/Francisco-1088/customCvDashboard.git`
2. Create a virtual environment
3. Install python dependencies with `pip install -r requirements.txt`
4. Zip `model.tflite` and upload to your Meraki Dashboard as described in this document: https://documentation.meraki.com/MV/Video_Analytics/MV_Sense_Custom_Computer_Vision#Artifact_Packaging
5. Assign to a camera and create a new MQTT broker pointing to your computer's IP address and port 1883 (security settings can be left blank)
 * This assumes your camera has IP reachability to your computer
6. Run these commands in your terminal to start a MQTT broker using Docker in your computer
 * `docker pull eclipse-mosquitto:1.6`
 * `docker run -p 1883:1883 eclipse-mosquitto:1.6`
7. Run `python mv_customcv_dashboard.py`
