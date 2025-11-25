🌤️ Weather Search Engine – Full Stack Application

A full-stack weather search engine built as part of a coding challenge.
The application allows users to search for current weather conditions by entering a city name.
It includes:

A Node.js + Express backend that exposes REST APIs

Integration with OpenWeather Current Weather API

An in-memory caching layer for performance

A frontend UI built with HTML, CSS, and JavaScript

Clean code structure, error handling, and fully local execution

🚀 Features
✅ Frontend

Modern UI built with HTML, CSS, JavaScript

City search input with dynamic results

Displays:

Current temperature

Feels-like temperature

Min/Max temperature

Humidity, pressure, visibility

Wind speed, direction, gust

Cloud cover

Sunrise & Sunset

Latitude & Longitude

Data source indicator (cache / live API)

✅ Backend

REST API built using Node.js + Express

Fetches current weather from OpenWeather API

Implements in-memory caching with:

TTL (Time-to-live)

Max entries

Auto clean-up of expired cache

Handles API errors cleanly (city not found, API outage, etc.)

Serves static frontend files

🗂️ Project Structure
weather-search-engine-fullstack/
│
├── backend/
│   ├── src/
│   │   ├── server.js              # Express server + routes
│   │   ├── cache.js               # Custom in-memory cache
│   │   └── openWeatherClient.js   # API client wrapper
│   ├── frontend/                  # Static frontend served by backend
│   ├── package.json
│   └── .env (NOT included in repo)
│
└── README.md

🔑 API Used
OpenWeather – Current Weather Data API

Documentation:
https://openweathermap.org/current

Example endpoint:

https://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}&units=metric


This project uses:

City name search

Temperature data

Weather description & icon

Wind details

Cloud percentage

Sunrise/Sunset timestamps

Coordinates

⚙️ Environment Variables

Create a .env file inside backend/:

OPENWEATHER_API_KEY=your_api_key_here
PORT=4000
CACHE_TTL_MS=300000
CACHE_MAX_ENTRIES=100


⚠️ .env is NOT included in the repo for security reasons.

🛠️ How to Run the Project Locally
1️⃣ Install backend dependencies
cd backend
npm install

2️⃣ Add your .env file
OPENWEATHER_API_KEY=your_api_key_here
PORT=4000
CACHE_TTL_MS=300000
CACHE_MAX_ENTRIES=100

3️⃣ Start the server
npm start


The server will start at:

http://localhost:4000

4️⃣ Use the UI

Open the browser:

http://localhost:4000


Try searching:

Mumbai
Pune
London
New York

🧪 API Endpoints
GET /api/weather?city={name}

Example:

http://localhost:4000/api/weather?city=Mumbai


Response structure:

{
  "source": "live",
  "city": "Mumbai",
  "country": "IN",
  "temperature": {
    "current": 31.5,
    "feelsLike": 35,
    "min": 30,
    "max": 32
  },
  "humidity": 70,
  "pressure": 1010,
  "wind": {
    "speed": 3.5,
    "deg": 260
  },
  "clouds": 75,
  "sunrise": "2025-11-25T01:23:00.000Z",
  "sunset": "2025-11-25T12:13:00.000Z",
  "coordinates": {
    "lat": 19.07,
    "lon": 72.88
  }
}

GET /api/health

Checks server and cache status.

🧰 Tech Stack
Frontend

HTML

CSS

Vanilla JavaScript

Backend

Node.js

Express.js

Axios

dotenv

Other

OpenWeather API

In-memory caching

RESTful design

📦 Submission Requirements (fulfilled)

✔ Full stack: backend + frontend
✔ REST API implemented
✔ Caching implemented
✔ Runs locally
✔ Organized code
✔ Public GitHub repo
✔ README included

📄 License

This project is created as part of a coding challenge and is free to use for evaluation purposes.
