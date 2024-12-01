
# PostgreSQL Service

This folder contains the configuration to set up a PostgreSQL database using Docker.

---

## 📦 Features

- Runs the latest PostgreSQL version.
- Persistent storage using Docker volumes.
- Customizable environment variables for database name, user, and password.

---

## 🚀 Getting Started

### Prerequisites

- **Docker** and **Docker Compose** installed.

### Steps to Run

1. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```

2. Update the `.env` file with your desired configuration:
   ```env
   POSTGRES_USER=myuser
   POSTGRES_PASSWORD=mypassword
   POSTGRES_DB=mydatabase
   ```

3. Start the PostgreSQL service:
   ```bash
   docker-compose up -d
   ```

4. Access the PostgreSQL service:
   - Default host: `localhost`
   - Default port: `5432`

5. Stop the service:
   ```bash
   docker-compose down
   ```

---

## 🛠️ Configuration

You can modify the following environment variables in the `.env` file:

- `POSTGRES_USER`: The username for the PostgreSQL database.
- `POSTGRES_PASSWORD`: The password for the PostgreSQL database.
- `POSTGRES_DB`: The name of the database to create.

---

## 📂 Persistent Storage

The PostgreSQL data is stored in the `postgres_data` volume, ensuring that your data persists across container restarts.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
