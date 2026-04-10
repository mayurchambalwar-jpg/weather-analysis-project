# ⛅ WeatherScope — India Weather Data Analysis Dashboard

> A full-stack weather analysis website built with **HTML · CSS · JavaScript · Python (Flask)**

---

## 📋 Project Overview

WeatherScope reads a JSON dataset of daily weather records for 5 major Indian cities, processes the data using Python (Flask), and displays rich visualisations using HTML, CSS, and Chart.js.

---

## 🎯 Key Features

- 📍 **Region Analysis** — compare avg, max, min temperature, rainfall & humidity across cities
- 📅 **Monthly Trends** — track weather changes month by month throughout the year
- ⭐ **Smart Insights** — hottest day, coldest day, rainiest day, moving-average trend line
- 🔮 **Temperature Prediction** — linear regression to predict future temperature values
- 📊 **Interactive Charts** — bar, line, and doughnut charts via Chart.js
- 🌙 **Dark-theme Responsive UI** — works on desktop and mobile

---

## 🛠 Technology Stack

| Layer     | Technology                  | Purpose                            |
|-----------|-----------------------------|------------------------------------|
| Backend   | Python 3 · Flask            | Data processing, routing, API      |
| Frontend  | HTML5 · CSS3                | Page structure & dark-theme UI     |
| Charts    | JavaScript · Chart.js 4     | Interactive bar, line, pie charts  |
| Data      | JSON file                   | 240 weather records (5 cities)     |
| Fonts     | Google Fonts (Syne, DM Sans)| Typography                         |

---

## 📁 Project Structure

```
weather_project/
├── app.py                   ← Flask backend (all logic & API)
├── README.md                ← This file
├── data/
│   └── weather_data.json    ← 240 weather records
├── templates/
│   ├── base.html            ← Shared layout + navbar
│   ├── index.html           ← Home page
│   ├── region.html          ← Region analysis page
│   ├── monthly.html         ← Monthly analysis page
│   └── insights.html        ← Insights + prediction page
└── static/
    └── css/
        └── style.css        ← Full stylesheet
```

---

## 🚀 How to Run the Project

### Step 1 — Check Python is installed
```bash
python --version
```
If not installed, download from: https://www.python.org/downloads/

### Step 2 — Extract the ZIP
Unzip `weather_project.zip` to a folder of your choice.

### Step 3 — Install Flask
```bash
pip install flask
```

### Step 4 — Run the Server
```bash
cd weather_project
python app.py
```

You should see:
```
* Running on http://127.0.0.1:5000
```

### Step 5 — Open in Browser
```
http://127.0.0.1:5000
```

> Press `Ctrl + C` in the terminal to stop the server.

---

## 📄 Pages & URLs

| Page             | URL       | What it shows                                              |
|------------------|-----------|------------------------------------------------------------|
| Home             | /         | Overview, animated city ticker, quick stat cards           |
| Region Analysis  | /region   | City comparison — 4 charts + data table                    |
| Monthly Analysis | /monthly  | Month-by-month trends — 3 charts + data table              |
| Insights         | /insights | Key highlights, trend line, prediction chart, summary      |

---

## 📊 Dataset — `data/weather_data.json`

| Field       | Type              | Description                              |
|-------------|-------------------|------------------------------------------|
| date        | String YYYY-MM-DD | Date of the record                       |
| city        | String            | Nagpur / Mumbai / Delhi / Pune / Bangalore |
| temperature | Float (°C)        | Daily temperature (range 7.5°C – 46.2°C)|
| humidity    | Integer (%)       | Relative humidity                        |
| rainfall    | Float (mm)        | Rainfall in millimetres                  |

Data patterns reflect real Indian seasons — hot summers (Apr–Jun), heavy monsoon (Jul–Sep), cool winters (Dec–Jan).

---

## 🔌 API Endpoints

| Endpoint       | Method | Returns                                              |
|----------------|--------|------------------------------------------------------|
| /api/region    | GET    | City-wise mean/max/min temp, total rainfall, humidity|
| /api/monthly   | GET    | Month-wise mean/max/min temp, rainfall, humidity     |
| /api/insights  | GET    | Key highlights, trend data, moving avg, prediction   |

---

## 📈 Charts Used

| Page    | Chart Type         | Data Shown                              |
|---------|--------------------|-----------------------------------------|
| Region  | Bar chart          | Average temperature per city            |
| Region  | Doughnut chart     | Rainfall distribution across cities     |
| Region  | Grouped bar chart  | Max vs Min temperature per city         |
| Region  | Bar chart          | Average humidity per city               |
| Monthly | Line chart         | Monthly average temperature trend       |
| Monthly | Bar chart          | Total monthly rainfall                  |
| Monthly | Line chart         | Monthly average humidity                |
| Insights| Line chart         | All temps + 5-point moving average      |
| Insights| Line chart         | Last 20 actual temps + 3 predicted      |

---

## 🎨 Colour System

| Data Type   | Colour    | Hex Code  |
|-------------|-----------|-----------|
| Temperature | Red       | `#FF4757` |
| Rainfall    | Blue      | `#3B9EFF` |
| Humidity    | Green     | `#00D68F` |
| Prediction  | Orange    | `#FF6B35` |
| Max Temp    | Red       | `#FF4757` |
| Min Temp    | Sky Blue  | `#7ECFFF` |

---

## 🏙 Cities Covered

| City      | State       | Climate                              |
|-----------|-------------|--------------------------------------|
| Nagpur    | Maharashtra | Semi-arid, extreme summers (hottest) |
| Mumbai    | Maharashtra | Tropical wet, high rainfall          |
| Delhi     | NCT         | Semi-arid, coldest winters           |
| Pune      | Maharashtra | Moderate, mild climate               |
| Bangalore | Karnataka   | Tropical savanna, pre-monsoon rain   |

---

## 💡 Tips & Notes

- If `pip install flask` fails, try `pip3 install flask`
- On Mac/Linux use `python3 app.py` if `python` doesn't work
- The JSON file at `data/weather_data.json` can be extended with more records
- All charts update automatically when the JSON data changes
- Press `Ctrl + C` in the terminal to stop the Flask server

---

*WeatherScope — HTML · CSS · JavaScript · Python (Flask)*
