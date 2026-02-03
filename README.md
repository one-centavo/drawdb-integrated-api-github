# 🚀 drawdb-integrated-api-github

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=61DAFB)
![License](https://img.shields.io/badge/license-AGPL--3.0-blue.svg?style=for-the-badge)

A **Self-Hosted**, fully Dockerized solution for **drawDB**. This repository unifies the Frontend and Backend into a single Docker orchestration, specifically pre-configured to work with the GitHub API for saving diagrams and versions directly to your Gists.



---

## 🌟 Why this version?

If you have ever tried to set up drawDB's frontend and backend separately, you know that connecting the server to enable saving can be a technical challenge. This version solves that by providing:

* **Unified Configuration:** A single `compose.yml` file to manage the entire stack.
* **Cloud Persistence:** Native integration with GitHub Gists so you never lose your diagrams.
* **Pro Remote Access:** Pre-configured for remote network access (perfect for home servers or VPNs like Tailscale).

## 🛠️ Prerequisites

1.  **Docker** and **Docker Compose** installed on your system.
2.  A **GitHub Personal Access Token (Classic)**.
    * *Required permissions:* Check the `repo` and `gist` boxes.



---

## 🚀 Quick Start

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/one-centavo/drawdb-integrated-api-github
    cd drawdb-integrated-api-github
    ```

2.  **Set up the environment:**
    Copy the sample file and edit it with your credentials:
    ```bash
    cp .env.sample .env
    ```
    > 💡 **Note:** Open the `.env` file and make sure to set your real IP address and GitHub Token.

3.  **Deploy with Docker:**
    ```bash
    docker compose up -d
    ```

4.  **Start Designing!**
    Access it via your browser at: `http://localhost:3000` (If it's your case)

---

## ⚙️ Environment Variables (.env)

| Variable | Description | Example Value |
| :--- | :--- | :--- |
| `VITE_BACKEND_URL` | The URL where the browser will look for the API. | `http://localhost:5000` |
| `CLIENT_URLS` | The frontend URL authorized by the server (CORS). | `http://localhost:3000` |
| `GITHUB_TOKEN` | Your GitHub Personal Access Token. | `ghp_YourSecretToken...` |
| `PORT` | Internal port for the Backend server. | `5000` |

---

## 📁 Project Structure

* `/frontend`: The drawDB visual editor (React).
* `/backend`: The integration server (Node.js/Express) that communicates with GitHub.
* `compose.yml`: Defines the network and persistence for the containers.

## ⚖️ License

This project inherits the licenses from its original components:
* **Frontend:** Distributed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.
* **Backend:** Distributed under the **MIT License**.

As a derivative work integrating both, this repository is distributed under the **AGPL-3.0 License**. See the `LICENSE` file for more details.

## 🤝 Credits & Acknowledgments

This project is a community-driven improvement and a Dockerized implementation based on the incredible work of the [drawDB](https://github.com/drawdb-io) team. Special thanks to the original authors of:

* **Frontend Core:** [drawdb](https://github.com/drawdb-io/drawdb) — The intuitive visual database editor.
* **Backend API:** [drawdb-server](https://github.com/drawdb-io/drawdb-server) — The core server for diagram persistence.

Modified and integrated by [one-centavo](https://github.com/one-centavo).

---
⭐ **If you found this useful, don't forget to give it a star!**

---
Built with ❤️ to simplify the workflow for database designers.