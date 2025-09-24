# MinIO Service

This folder contains the configuration to set up a **MinIO** object storage service using Docker.

---

## 📦 Features

- Runs the latest MinIO version.
- Persistent storage using Docker volumes.
- Customizable environment variables for access key, secret key, and bucket name.
- Web-based management console.

---

## 🚀 Getting Started

### Prerequisites

- Docker and Docker Compose installed.

### Steps to Run

1. **Copy the `.env.example` file to `.env`:**

   ```bash
   cp .env.example .env
   ```

2. **Update the `.env` file with your desired configuration:**

   ```env
   MINIO_ROOT_USER=minioadmin
   MINIO_ROOT_PASSWORD=minioadmin
   MINIO_BUCKET=uploads
   ```

3. **Start the MinIO service:**

   ```bash
   docker-compose up -d
   ```

4. **Access the MinIO Console:**

   - Default host: [http://localhost:9001](http://localhost:9001)
   - Default access key: `minioadmin`
   - Default secret key: `minioadmin`

5. **Stop the service:**

   ```bash
   docker-compose down
   ```

---

## 🛠️ Configuration

You can modify the following environment variables in the `.env` file:

- `MINIO_ROOT_USER`: The root access key for MinIO.
- `MINIO_ROOT_PASSWORD`: The root secret key for MinIO.
- `MINIO_BUCKET`: The default bucket name to use.

---

## 📂 Persistent Storage

The MinIO data is stored in the `minio_data` volume, ensuring that your files persist across container restarts.

---

## 📄 License

This project is licensed under the MIT License.