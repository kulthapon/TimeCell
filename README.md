## Time Cell
Time Cell is a web-based artificial intelligence system for analyzing and classifying white blood cells from body fluid images. The system is developed as a web application, enabling users to access and utilize its features through web browsers on both desktop and mobile devices.

The web application is built using  `React`, `node.js`, `express.js`, `javascript`, `MySQL`, `python` and `FastAPI`, integrated with Artificial Intelligence (AI). The system utilizes the `YOLO11m` model for white blood cell detection and localization, and `MobileNetV3` for cell classification. 

The system can classify five types of white blood cells from body fluid:

* Basophil
* Eosinophil
* Lymphocyte
* Monocyte
* Neutrophil
---
## File Structure 

```
TimeCell/
├── al/ # AI Services (FastAPI)
│   ├── ml/
│   ├── models/
│   ├── routers/
│   ├── config.py
│   ├── Dockerfile
│   ├── Dockerfile.base
│   ├── image_utils.py
│   ├── main.py
│   └── requirements.txt
│
├── client/ # Frontend (React)
│   ├── node_modules/
│   ├── public/
│   │    ├── icon/
│   │    ├── images/
│   │    ├── logo/
│   │    ├── index.html
│   │    ├── manifest.json
│   │    └── robots.txt
│   ├── src/
│   │    ├── components/
│   │    ├── context/
│   │    ├── pages/
│   │    ├── App.css
│   │    ├── App.jsx
│   │    └── index.js
│   ├── Dockerfile
│   ├── package-lock.json
│   └── package.json
│
├── server/ # Backend (Node.js/Express)
│   ├── node_modules/
│   ├── controller/
│   ├── middleware/
│   ├── routes/
│   ├── utils/
│   ├── db/
│   ├── server.js
│   ├── Dockerfile
│   ├── package-lock.json
│   └── package.json
│
├── node_modules/
├── package-lock.json
├── package.json
│
├── docker-compose.yml
├── Dockerfile
│
├── .gitignore
└── README.md
```
---
## Features

- Real-time white blood cell analysis
- Automated detection and classification of five white blood cell types
- White blood cell counting and quantitative analysis
- Integrated knowledge base for white blood cell identification and learning
- User authentication and account management
- Multi-language support (Thai and English)
- Theme customization with Light and Dark modes

---
## Requirements

- Python version 3.13.7 https://www.python.org/downloads/release/python-3137/
- Node.js https://nodejs.org/en/download
- Visual Studio Code https://code.visualstudio.com/download
- MySQL Community https://dev.mysql.com/downloads/mysql/8.0.html
- MySQL Workbench https://dev.mysql.com/downloads/workbench/
  * Create a database connection using Port 3307
  * Username: root
  * Password: 1234
- Docker https://www.docker.com/products/docker-desktop/

---
## Installation

Follow the steps below using a command-line interface. Make sure Docker Desktop is running throughout the installation process.

1. Clone the Repository
   ```bash
   git clone https://github.com/kulthapon/TimeCell.git
   ```
   ```bash
   cd TimeCell
   ```
2. Build the AI Service Base Image
   ```bash
   cd ai 
   ```
   ```bash
   docker build -f Dockerfile.base -t timecell-ai-base . 
   ```
3. Build and Run the Containers
   ```bash
   cd ..
   ```
   ```bash
   docker-compose build --no-cache && docker-compose up
   ```
4. Access the Application via http://localhost:3000/
---
