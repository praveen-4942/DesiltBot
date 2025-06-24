
# DesiltBot 🚜💧

DesiltBot is an autonomous silt detection and removal system built using Raspberry Pi 4B, a Pi Camera, HX711 load cell, and GPS module. It captures real-time images, measures silt weight, tracks geolocation, and logs data to both Firebase and MySQL, making waterway maintenance smarter and more efficient.

---

## 🔧 Features

- 📷 Real-time image capture using Pi Camera  
- 📍 GPS-based geotagging of silt removal location  
- ⚖️ Calibrated weight estimation using HX711 load cell  
- ☁️ Data upload to Firebase Storage and MySQL  
- 🔁 Continuous monitoring with automated loop execution

---

## 🧠 Tech Stack

**Hardware**
- Raspberry Pi 4B  
- HX711 Load Cell  
- Pi Camera  
- GPS Module

**Software & Libraries**
- Python  
- pynmea2 for GPS parsing  
- RPi.GPIO for GPIO control  
- firebase_admin SDK  
- mysql-connector-python  
- libcamera-still for image capture

---

## ⚙️ Setup

1. Install dependencies  
   pip install firebase-admin mysql-connector-python pynmea2 RPi.GPIO

2. Configure Firebase  
   - Add your service account key as serviceAccountKey.json  
   - Enable Firebase Realtime Database and Storage

3. Set up MySQL  
   - Create a database with a table named DATA  
   - Table fields: Image_download_url, Latitude, Longitude, Weight, Date, Time

4. Connect Hardware  
   - GPIO pins: HX711 DOUT → GPIO6, SCK → GPIO5  
   - Ensure GPS module and Pi Camera are connected correctly

5. Run the Script  
   python desiltbot.py

---

<prev>
<p align="center">
  <img src="Entire setup.jpg" width="500" alt="Circuit Diagram"><br>
  <b> Desilt Bot</b>
</p>
</prev>

---

## 🗃️ Data Schema

| Column             | Description                |
|--------------------|----------------------------|
| Image_download_url | Link to the captured image |
| Latitude           | Latitude from GPS          |
| Longitude          | Longitude from GPS         |
| Weight             | Calibrated weight in grams |
| Date               | Date of data entry         |
| Time               | Time of data entry         |

---

## 🌍 Applications

- Desilting validation in lakes, tanks, and reservoirs  
- Environmental reporting and regulatory compliance  
- Smart civic waterway management

---

## 🧠 Notes

- Update calibration constants for accurate weight readings  
- Ensure WiFi connectivity for real-time cloud updates  
- Clean GPIO and close DB connections on exit

---

## 📬 Contributions

Pull requests and feature suggestions are welcome. Let’s make waterway maintenance smarter—together!

---

## 📄 License

This project is licensed under the MIT License.
