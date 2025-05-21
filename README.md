# Social Media Project Setup

## 📚 Table of Contents

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Description

This project serves as a scaffolding tool for building Python applications that are production-ready. It emphasizes **modularity**, **scalability**, and a clear **separation of concerns**, providing a solid foundation for developing maintainable and well-structured codebases.

Whether you're starting a new project or looking to standardize your development practices, this scaffold helps you adopt best practices from the ground up.

## Installation

Clone the repo and run docker compose:

```bash
git clone https://github.com/MrChike/social_media_project.git
cd social_media
docker-compose up --build
```

- A detailed tutorial is available here: <https://dev.to>
- Below is the project structure with the defined responsibility of each file

```bash
social_media/
├── __init__.py
│
├── movies/                      # Module for handling movies
│   ├── __init__.py
│   ├── router.py                # Defines API endpoints and maps them to the controller for movies
│   ├── controller.py            # Handles request-response cycle for movies; invokes movie services
│   ├── service.py               # Business logic for movies: processing, filtering, etc.
│   ├── model.py                 # ORM model for movies (e.g., SQLAlchemy Movie table)
│   ├── schema.py                # Pydantic models for request validation and response serialization (movies)
│   ├── dependencies.py          # Dependency-injected functions or classes shared within movies module
│   └── test.py                  # Unit tests for movies
│
├── tv_series/                   # Module for handling TV series
│   ├── __init__.py
│   ├── router.py                # Defines API endpoints and maps them to the controller for TV series
│   ├── controller.py            # Handles request-response cycle for TV series; invokes services
│   ├── service.py               # Business logic for TV series: logic for seasons, episodes, etc.
│   ├── model.py                 # ORM model for TV series (e.g., SQLAlchemy Series table)
│   ├── schema.py                # Pydantic models for request validation and response serialization (TV series)
│   ├── dependencies.py          # Dependency-injected functions or classes shared within tv_series module
│   └── test.py                  # Unit tests for TV series
│
├── music/                       # Module for handling music
│   ├── __init__.py
│   ├── router.py                # Defines API endpoints and maps them to the controller for music
│   ├── controller.py            # Handles request-response cycle for music; invokes services
│   ├── service.py               # Business logic for music: logic for songs, albums, artists
│   ├── model.py                 # ORM model for music (e.g., SQLAlchemy Song or Album table)
│   ├── schema.py                # Pydantic models for request validation and response serialization (music)
│   ├── dependencies.py          # Dependency-injected functions or classes shared within music module
│   └── test.py                  # Unit tests for music
│
├── static/                      # Static files (e.g., CSS, JS, images)
│   ├── movie_posters/           # Folder containing movie poster images
│   ├── tv_series_posters/       # Folder containing TV series poster images
│   └── album_covers/            # Folder containing album cover images
│
├── templates/                   # HTML or templating engine files (e.g., Jinja2)
│   ├── movie_detail.html        # Template for rendering movie details
│   ├── tv_series_detail.html    # Template for rendering TV series details
│   └── music_detail.html        # Template for rendering music details
│
├── docs/
│   └── journal.md               # Documentation or project notes
│
├── shared/
│   ├── config/                  # Project-wide configurations, e.g., settings.py
│   ├── db/                      # Database connection logic, session handling
│   ├── dependencies/            # Shared dependencies across modules
│   ├── middleware/              # Project-wide middleware (e.g., CORS, authentication)
│   └── utils/                   # Utility functions or helpers used across the app
│
├── scripts/
│   ├── __init__.py              # Initialization for utility scripts
│   └── connect_with_me.py       # Personal script (e.g., LinkedIn automation or social connection)
│
├── tests/                       # Integration, system, and E2E tests
│   ├── __init__.py
│   ├── movies/                  # Integration tests for movies module
│   ├── tv_series/               # Integration tests for tv_series module
│   └── music/                   # Integration tests for music module
│
├── .coverage                    # Coverage report generated by testing
├── main.py                      # Entrypoint of the FastAPI application
├── nginx.conf                   # Nginx configuration – reverse proxy, rate limiting, static file serving
├── pytest.ini                   # Pytest configuration
├── requirements.txt             # Python dependencies
├── docker-compose.yaml          # Docker Compose configuration
├── Dockerfile                   # Docker build file for the FastAPI application
├── Dockerfile.nginx             # Docker build file for the Nginx reverse proxy
└── README.md                    # Project overview and usage documentation
```

## Usage

Run the command `docker-compose up --build` at the project root folder to get it up & running on your local

## Features

- 🎬 Modular architecture for Movies, TV, and Music domains
- 🧩 Scalable microservice-like design using FastAPI
- 🧪 Robust testing setup with unit and integration tests
- 🐳 Dockerized for local and production environments
- ⚙️ Centralized config and dependency injection for maintainability

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

## Acknowledgements

- Firstly, I want to acknowledge myself for staying committed to continuous learning and growth in a challenging field.
- This section will be updated as the project evolves...

## Contact

Feel free to connect with me on

- 💼 [LinkedIn](https://www.linkedin.com/in/chikeegonu/)
- 🐙 [Github](https://github.com/MrChike)
