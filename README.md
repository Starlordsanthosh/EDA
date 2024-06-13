# EDA Web Application

This project is an Exploratory Data Analysis (EDA) web application built with React for the frontend and Flask for the backend. The application allows users to upload a dataset (CSV file), performs EDA and statistical analysis, generates insights using OpenAI, and provides a compiled Word document with graphs and insights.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Deploying the Frontend](#deploying-the-frontend)
- [Deploying the Backend](#deploying-the-backend)
- [Contributing](#contributing)
- [License](#license)

## Features

- Upload CSV files
- Perform EDA and statistical analysis
- Generate insights using OpenAI
- Compile a Word document with graphs and insights

## Prerequisites

- Node.js and npm
- Python 3.x
- MongoDB
- OpenAI API Key
- Heroku CLI (for deployment)

## Installation

### Backend (Flask)

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/your-repo.git
    cd your-repo/backend
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    Create a `.env` file in the backend directory and add your MongoDB URI and OpenAI API key:
    ```
    MONGO_URI=mongodb://localhost:27017/
    OPENAI_API_KEY=your_openai_api_key
    ```

### Frontend (React)

1. Navigate to the frontend directory:
    ```bash
    cd ../frontend
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

## Running the Application

### Backend

1. Ensure MongoDB is running:
    ```bash
    mongod
    ```

2. Start the Flask server:
    ```bash
    python app.py
    ```

### Frontend

1. Start the React development server:
    ```bash
    npm start
    ```

2. Open your browser and navigate to `http://localhost:3000`

## Deploying the Frontend

The frontend can be deployed using GitHub Pages.

1. Add `homepage` in `package.json`:
    ```json
    "homepage": "https://yourusername.github.io/your-repo"
    ```

2. Install `gh-pages`:
    ```bash
    npm install gh-pages --save-dev
    ```

3. Add the following scripts to `package.json`:
    ```json
    "scripts": {
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build",
        // other scripts
    }
    ```

4. Deploy to GitHub Pages:
    ```bash
    npm run deploy
    ```

## Deploying the Backend

The backend can be deployed using Heroku.

1. Create a `Procfile` in the backend directory:
    ```
    web: python app.py
    ```

2. Create `requirements.txt`:
    ```bash
    pip freeze > requirements.txt
    ```

3. Create `runtime.txt`:
    ```
    python-3.9.1
    ```

4. Initialize a Git repository:
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```

5. Create a Heroku app:
    ```bash
    heroku create your-app-name
    ```

6. Deploy to Heroku:
    ```bash
    git push heroku master
    ```

7. Open your app:
    ```bash
    heroku open
    ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes.

## License

This project is licensed under the MIT License.
