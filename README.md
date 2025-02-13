# Dockerized Jupyter Notebook

A simple setup to run Jupyter Notebook using Docker and Docker Compose, with a `Makefile` for streamlined commands.

## Features
- Jupyter Notebook environment running in a Docker container.
- Persistent storage for notebooks.
- Easy-to-use `Makefile` commands for managing the container.
- Automatically builds and runs the environment with proper user permissions.

---

## Prerequisites
- [Docker](https://www.docker.com/)
- `make` (installed by default on most Linux/Mac systems; on Windows, use WSL or install manually)

---

## Setup and Usage

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Start the Environment
```bash
make up
```
This will build and run the Jupyter Notebook container.

### 3. Access Jupyter Notebook
- Open your browser and go to [http://localhost:8888](http://localhost:8888).
- Use the token provided in the terminal to log in.

### 4. Stop the Environment
To stop the container but keep it intact:
```bash
make stop
```

To stop and remove the container:
```bash
make down
```

### 5. Open a Shell in the Container
```bash
make shell
```
This command will give you shell access inside the running container.

### 6. View Logs
To view the container logs in real time:
```bash
make logs
```

---

## File Structure
```
.
├── docker-compose.yml    # Docker Compose configuration
├── notebooks/            # Directory for Jupyter notebooks (persisted)
├── Makefile              # Commands for managing the environment
└── README.md             # Project documentation
```

---

## Makefile Commands

| Command       | Description                                        |
|---------------|----------------------------------------------------|
| `make up`     | Build and start the Jupyter container.             |
| `make down`   | Stop and remove the container.                     |
| `make stop`   | Stop the container without removing it.            |
| `make shell`  | Open an interactive shell inside the container.    |
| `make logs`   | View container logs in real-time.                  |

---

## License
This project is licensed under the [MIT License](./LICENSE).

Feel free to use, modify, and share this setup!

---

## Contributions
Contributions are welcome! Feel free to open issues or submit pull requests for enhancements.

---

## Author
Chethana Kalpa  
[LinkedIn](https://www.linkedin.com/in/chethana-kalpa/) | [Blog](https://chethana.me/blog)