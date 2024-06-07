# File Sharing Platform FastAPI

This is a simple file management system built with FastAPI and PostgreSQL. It allows users to upload, download, and delete files.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Original-Lily/Fast-File-Share.git
---
2. Install the required dependencies: `pip install -r requirements.txt`
---
3. Set up the PostgreSQL database and configure the environment variables. You can do this by creating a `.env` file in the root directory and adding the following variables:
   ```
   DB_HOST=your_database_host
   DB_PORT=your_database_port
   DB_USER=your_database_user
   DB_PASSWORD=your_database_password
   DB_NAME=your_database_name
   ```
---
4. Run the FastAPI application:
   ```bash
   uvicorn main:app --reload
   ```

# Usage

### Downloading a File

Send a **GET** request to `/download/{filename}` endpoint, with `{filename}` being the name of the file you want to download.

---

### Uploading a File

Send a **POST** request to `/upload` endpoint with the file attached as *multipart/form-data*. Following this you will receive a response containing the name of the file uploaded and a download link.

---

### Deleting a File

Send a **DELETE** request to `/delete/{filename}` endpoint, where `{filename}` is the name of the file you want to delete. The file will be deleted from the host.