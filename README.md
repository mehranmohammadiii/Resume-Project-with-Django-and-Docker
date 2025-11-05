# Dockerized Django + React Resume/Portfolio

<p align="center">
  <img src="URL_TO_YOUR_MAIN_PAGE_IMAGE" alt="Main Page Screenshot" width="45%">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="URL_TO_YOUR_SECOND_PAGE_IMAGE" alt="Second Page Screenshot" width="45%">
</p>

A full-stack, containerized personal resume and portfolio application. This project features a **Django** backend serving a REST API, a **React** frontend for a dynamic user experience, and a **PostgreSQL** database for data persistence. The entire stack is orchestrated using **Docker Compose** for a seamless, one-command setup.

**Note:** The resume data populated in this project is for demonstration purposes only and consists of placeholder/random information.

---

## 🏛️ Architecture Overview

This project follows a modern, decoupled architecture, with each component running in its own isolated Docker container:

*   **`frontend`:** A **React** application responsible for rendering the user interface. It communicates with the backend via API calls.
*   **`backend`:** A **Django** application built with **Django REST Framework** that exposes a set of APIs for managing resume data (e.g., education, experience, skills).
*   **`db`:** A **PostgreSQL** database container that serves as the persistent data store for the backend.

All three services are networked and managed by a single `docker-compose.yml` file, ensuring a consistent and reproducible development environment.

## 🛠️ Key Technologies

*   **Backend:** Python, Django, Django REST Framework
*   **Frontend:** JavaScript, React
*   **Database:** PostgreSQL
*   **Containerization:** Docker, Docker Compose

---

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Make sure you have Git and Docker (with Docker Compose) installed on your system.
*   [Git](https://git-scm.com/downloads)
*   [Docker](https://docs.docker.com/get-docker/)

### Installation & Running

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd YOUR_REPO_NAME
    ```

3.  **Create a local environment file:**
    Create a `.env` file in the `backend` directory and add your secret key:
    ```
    # backend/.env
    SECRET_KEY='your-super-secret-key'
    DEBUG=True
    ```

4.  **Build and run the services using Docker Compose:**
    This single command will build the images for the frontend and backend, pull the PostgreSQL image, and start all three containers in detached mode.
    ```sh
    docker compose up --build -d
    ```

5.  **Access the applications:**
    *   **Frontend (React App):** [http://localhost:3000](http://localhost:3000)
    *   **Backend (Django API):** [http://localhost:8000/api/](http://localhost:8000/api/)

6.  **To stop the services:**
    When you're done, you can stop all running containers with:
    ```sh
    docker compose down
    ```

---

## 🎨 Credits & Acknowledgements

This project was built upon an excellent foundation provided by **hadimh**. A huge thank you for the original UI/UX design and the React frontend implementation.

*   Check out the original creator's profile on GitHub: **[hadimh](https://github.com/hadimh)**

---
