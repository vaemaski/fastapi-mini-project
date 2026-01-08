# FastAPI Mini Project

A simple social media application built with FastAPI backend and Streamlit frontend, featuring user authentication, image uploads, and post management.

## Features

- 🔐 User authentication and registration
- 📸 Image upload with ImageKit integration
- 📝 Create and view posts with captions
- 🎨 Modern Streamlit web interface
- 🗄️ SQLite database with async SQLAlchemy
- 🔄 JWT-based authentication

## Tech Stack

- **Backend**: FastAPI, SQLAlchemy, FastAPI Users
- **Frontend**: Streamlit
- **Database**: SQLite (aiosqlite)
- **Image Storage**: ImageKit.io
- **Authentication**: JWT tokens

## Installation

1. Clone the repository:
```bash
git clone https://github.com/vaemaski/fastapi-mini-project.git
cd fastapi-mini-project
```

2. Install dependencies:
```bash
pip install -r requirements.txt
# or if using uv
uv sync
```

3. Set up environment variables:
Create a `.env` file with:
```
IMAGEKIT_PUBLIC_KEY=your_public_key
IMAGEKIT_PRIVATE_KEY=your_private_key
IMAGEKIT_URL_ENDPOINT=your_url_endpoint
```

4. Run the database setup:
```bash
python main.py
# This will create tables on startup
```

## Usage

### Running the Backend
```bash
python main.py
```
The API will be available at `http://localhost:8000`

### Running the Frontend
```bash
streamlit run frontend.py
```
The web app will be available at `http://localhost:8501`

## API Endpoints

- `POST /auth/jwt/login` - User login
- `POST /auth/register` - User registration
- `POST /upload` - Upload image with caption
- `GET /posts` - Get all posts
- `GET /users/me` - Get current user info

## Project Structure

```
├── app/
│   ├── app.py          # Main FastAPI application
│   ├── db.py           # Database models and setup
│   ├── schemas.py      # Pydantic schemas
│   ├── users.py        # User management
│   └── images.py       # ImageKit configuration
├── frontend.py         # Streamlit web interface
├── main.py            # Application entry point
├── pyproject.toml     # Project dependencies
└── README.md          # This file
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License