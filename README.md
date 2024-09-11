# Dashboard Application

## Overview

This project is a web application featuring a basic dashboard with multiple types of charts, including Candlestick, Line, Bar, and Pie charts. The frontend is built using Next.js, and the backend is built using Django, which serves the data via API endpoints. The data is fetched dynamically from the Django backend and displayed in the charts on the frontend.

## Setup Instructions

### Prerequisites

- **Node.js** and **npm** (for the frontend)
- **Python** and **pip** (for the backend)
- **Docker** (optional, for containerized deployment)

### Backend (Django API)

1. Navigate to the `charts_backend` directory:

   ```bash
   cd charts_backend
   ```

2. (Optional but recommended) Create a virtual environment:

   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the Django development server:

   ```bash
   python manage.py runserver
   ```

   The Django API will be available at `http://localhost:8000`.

### Frontend (Next.js)

1. Navigate to the `charts-frontend` directory:

   ```bash
   cd charts-frontend
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

   The Next.js frontend will be available at `http://localhost:3000`.

### Running the Application with Docker (Optional)

1. Make sure Docker is installed on your system.

2. In the root directory of the project (where `docker-compose.yml` is located), run the following command:

   ```bash
   docker-compose up --build
   ```

3. The frontend will be accessible at `http://localhost:3000`, and the backend will be accessible at `http://localhost:8000`.

## Libraries and Tools Used

### Frontend

- **Next.js**: React framework for server-side rendering and easy setup.
- **Chart.js**: Charting library for rendering different types of charts.
- **Axios**: HTTP client to fetch data from the backend.

### Backend

- **Django**: Web framework for building the API.
- **Django REST Framework**: For creating API endpoints to serve chart data.

### DevOps

- **Docker**: For containerizing both the frontend and backend.

## Approach and Thought Process

1. **Frontend (Next.js)**:

   - A simple dashboard page is created using Next.js. React components are used to render the Candlestick, Line, Bar, and Pie charts.
   - Data for the charts is fetched dynamically using Axios from the Django API endpoints and passed to the respective chart components.

2. **Backend (Django API)**:

   - The Django REST framework is used to build the API endpoints that return the data for each chart.
   - The data is hardcoded for simplicity and follows the typical data structure expected by the charting library.

3. **Integration**:
   - The frontend makes requests to the Django API, receives JSON data, and renders it in the charts dynamically.
   - Docker is optionally used to containerize the application, making it easy to deploy and run in any environment.

---
