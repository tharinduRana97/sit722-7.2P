# Dockerfile for inventory_management microservice
FROM python:3.11-slim

WORKDIR /app

# Copy the requirements.txt file and install dependencies
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire application code to the /app directory
COPY . .

# Set environment variable for database URL
ENV DATABASE_URL = "postgresql://s224169428_user:ksCozU984iGsAqoB7QSniIFRb7HMjhMv@dpg-crah25aj1k6c73bvm0l0-a.oregon-postgres.render.com/s224169428?sslmode=require"


# Expose the port the application runs on
EXPOSE 7000

# Command to run the application
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "7000"]
