FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV DATABASE_URL = "postgresql://s224169428_user:ksCozU984iGsAqoB7QSniIFRb7HMjhMv@dpg-crah25aj1k6c73bvm0l0-a.oregon-postgres.render.com/s224169428?sslmode=require"

EXPOSE 7000

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "7000"]
