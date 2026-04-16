# Smart Route Delivery Planner

<p align="center">
  <a href="https://github.com/Blue-Rangoon/smart-route-delivery-planner">
    <img src="https://img.shields.io/github/license/Blue-Rangoon/smart-route-delivery-planner?style=for-the-badge" alt="License">
  </a>
  <a href="https://github.com/Blue-Rangoon/smart-route-delivery-planner">
    <img src="https://img.shields.io/github/last-commit/Blue-Rangoon/smart-route-delivery-planner?style=for-the-badge" alt="Last Commit">
  </a>
  <a href="https://github.com/Blue-Rangoon/smart-route-delivery-planner">
    <img src="https://img.shields.io/github/issues/Blue-Rangoon/smart-route-delivery-planner?style=for-the-badge" alt="Issues">
  </a>
  <a href="https://github.com/Blue-Rangoon/smart-route-delivery-planner">
    <img src="https://img.shields.io/github/stars/Blue-Rangoon/smart-route-delivery-planner?style=for-the-badge" alt="Stars">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/bootstrap_5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap 5">
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/css3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/leaflet-199EF5?style=for-the-badge&logo=leaflet&logoColor=white" alt="Leaflet">
  <img src="https://img.shields.io/badge/a*-pathfinding-FFD700?style=for-the-badge" alt="A* Algorithm">
</p>

---

AI-powered delivery route optimization platform built with Flask. This application calculates optimal delivery routes using advanced pathfinding algorithms (A*, UCS, Dijkstra, BFS, DFS), reducing delivery times by up to 40% and cutting fuel costs.

## Features

- **AI Route Optimization** - Dijkstra/A*/UCS-powered algorithms for shortest, fastest, and most fuel-efficient routes
- **Live Map Visualization** - Interactive Leaflet maps with real Karachi coordinates and animated route drawing
- **Smart Traffic Intelligence** - Options for speed, fuel efficiency, or road quality optimization
- **Delivery Analytics** - Track distance, ETA, and cost summaries for every delivery run
- **Mobile Responsive** - Fully responsive dashboard for phones, tablets, and desktops
- **Secure Authentication** - Local-first authentication with encrypted user sessions

## Tech Stack

| Category | Technology |
|----------|------------|
| Backend | Python, Flask, Flask-CORS |
| Frontend | HTML5, CSS3, JavaScript |
| UI Framework | Bootstrap 5 |
| Maps | Leaflet.js |
| Algorithms | A*, Uniform Cost Search, Dijkstra, BFS, DFS |

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Blue-Rangoon/smart-route-delivery-planner.git
   cd smart-route-delivery-planner
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

```bash
python app.py
```

The application will start on `http://localhost:5000`. Open your browser and navigate to:

```
http://localhost:5000
```

## Project Structure

```
smart-route-delivery-planner/
├── app.py                 # Main Flask application
├── algorithms/            # Pathfinding algorithms
│   ├── ai_router.py      # AI routing logic
│   ├── astar.py          # A* algorithm
│   ├── bfs.py            # Breadth-First Search
│   ├── dfs.py            # Depth-First Search
│   ├── ucs.py            # Uniform Cost Search
│   └── __init__.py
├── utils/                 # Utility modules
│   ├── data.py           # Graph data & node locations
│   └── __init__.py
├── templates/             # HTML templates
│   ├── index.html       # Main landing page
│   └── dashboard.html # Dashboard page
├── static/               # Static assets
│   ├── index.css       # Styles
│   └── index.js       # Client-side scripts
├── requirements.txt     # Python dependencies
├── .gitignore         # Git ignore rules
└── README.md           # This file
```

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/signup` | POST | Register a new user |
| `/api/login` | POST | User login |
| `/api/logout` | POST | User logout |
| `/api/locations` | GET | Get all node locations |
| `/api/nodes` | GET | Get all nodes |
| `/api/plan_route` | POST | Plan optimal route |
| `/api/graph` | GET | Get graph data |

## Available Nodes

The system includes delivery locations across Karachi:

| Code | Location |
|------|----------|
| A | UIT University, Gulshan Block 7 |
| B | Gulshan Chowrangi |
| C | NIPA Chowrangi |
| D | Liaquatabad |
| E | Teen Hatti |
| F | Guru Mandir |
| G | MA Jinnah Road |
| H | Saddar Karachi |

## Security Notes

- The default secret key in `app.py` is for development only
- In production, generate a secure secret key: `python -c "import secrets; print(secrets.token_hex(32))"`
- Update the `app.secret_key` in `app.py` before deploying

## Built With

- [Flask](https://flask.palletsprojects.com/) - Python web framework
- [Bootstrap](https://getbootstrap.com/) - CSS framework
- [Leaflet](https://leafletjs.com/) - Open-source JavaScript maps

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

<p align="center">Made with ❤️ for modern logistics</p>
