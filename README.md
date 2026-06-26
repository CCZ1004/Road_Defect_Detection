# RoadSafe AI | Road Defect Detection System 🚀

RoadSafe AI is an end-to-end, real-time computer vision application designed to automate infrastructure monitoring. By combining deep learning object detection with real-time telemetry and mapping, the system automatically detects road anomalies (such as potholes and cracks), logs their exact GPS coordinates, and visualizes them on an interactive analytics dashboard.

---

## 🌟 Key Features

* **Real-Time Computer Vision:** Powered by Ultralytics **YOLOv8** to process video frames asynchronously and extract road defect classifications with high confidence.
* **Live Metadata Logging:** Integrated with Windows Geolocation services (`winsdk`) to capture `latitude` and `longitude` coordinate stamps at the exact moment a defect is identified.
* **Interactive Dashboard:** A modern UI built with HTML5, CSS variables, and JavaScript, featuring:
    * **Live Video Stream:** Real-time canvas overlay showcasing model bounding boxes.
    * **Geospatial Mapping:** Interactive **Leaflet.js** map utilizing **Marker Clustering** to view defect hotspots.
    * **Analytics Charts:** Dynamic historical trend graphs and breakdown distributions powered by **Chart.js**.
* **Robust Storage & Exporting:** Persistent document storage using a local **MongoDB** database, allowing operators to filter and export data directly into clean CSV reports.

---

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **Computer Vision:** OpenCV, Ultralytics YOLOv8
* **Database:** MongoDB (via PyMongo)
* **Hardware Interface:** WinSDK (Windows Devices Geolocation API)
* **Frontend:** HTML5, CSS3 (Modern Responsive Flexbox/Grid), JavaScript (ES6+)
* **Frontend Libraries:** Leaflet.js, Leaflet.markercluster, Chart.js, FontAwesome

---

## 📁 Project Structure

```text
├── app.py                 # Flask Server, YOLO worker thread, & MongoDB pipeline
├── templates/
│   └── index.html         # Main dashboard interface (Map, Stream, Charts)
└── static/
    └── css/
        └── styles.css     # Clean dashboard styling & responsive media queries
