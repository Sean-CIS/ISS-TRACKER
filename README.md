# ISS Tracker

Real-time International Space Station tracking web application with live position updates, pass predictions, and crew information.

![ISS Tracker Screenshot](images/screenshot.png)

## Features

- Live ISS position on interactive world map
- Ground track showing orbital path
- Pass predictions for your location
- Current crew information
- Auto-refresh every 5 seconds

## Tech Stack

- **Backend:** Python, Flask
- **Frontend:** HTML, CSS, JavaScript
- **Mapping:** Leaflet.js
- **APIs:** Open Notify, Celestrak

## Installation
```bash
git clone https://github.com/Sean-CIS/ISS-TRACKER.git
cd ISS-TRACKER
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open `http://localhost:5000` in your browser.

## APIs Used

| API | Endpoint | Purpose |
|-----|----------|---------|
| Open Notify | `api.open-notify.org/iss-now.json` | Real-time ISS position |
| Open Notify | `api.open-notify.org/astros.json` | Current crew |
| Celestrak | `celestrak.org/NORAD/elements/` | TLE orbital data |

## How It Works

1. Backend fetches ISS coordinates from Open Notify API
2. Frontend polls backend every 5 seconds
3. Leaflet.js updates marker position on map
4. Skyfield library calculates pass predictions using TLE data

## What I Learned

- Working with NASA/space data APIs
- Orbital mechanics basics (TLE format, pass prediction)
- Real-time data visualization
- Frontend/backend integration

## Future Improvements

- [ ] 3D globe visualization with Cesium.js
- [ ] Push notifications for visible passes
- [ ] Historical tracking data
- [ ] Multiple satellite support

## License

MIT
